# 📈 ETF Booster – Dokumentation  

Ein modulares **Python-basiertes Monitoring-Tool**, das aktuell über 600 nach Kriterien wie TER gefilterten ETF-Positionen (Datenbestand hat über 2600) überwacht, **antizyklische Kauf-/Verkaufssignale** erkennt und diese per **Telegram-Benachrichtigung** verschickt.  

> ⚠️ **Hinweis:** Dieses Repository dient lediglich **Dokumentations- und Demonstrationszwecken**.  
> Der Quellcode ist vertraulich und wird nicht öffentlich bereitgestellt. Diese Unterlagen dienen zur **Strategie-, Architektur- und Konzeptübersicht**.

---

## 📊 Erste Ergebnisse

📈 Performance: Outperformte den MSCI World um **+4 %** in den ersten 3 Monaten (Performance kann schwanken)  
🧪 Umfangreiche Tests: Mehrere ETFs weltweit, verschiedene Zeitrahmen  
⏳ Status: WIP – Backtesting und Budget-Split-Logik in Entwicklung

---

## 🎯 Zielsetzung
- 🚫 Keine manuelle Marktbeobachtung mehr  
- 🤖 Automatische Identifikation von Kauf- und Verkaufszeitpunkten
- Weniger Handlungen auf Basis von Gefühlen  
- 💰 Steueroptimierte Gewinne durch Freibetrag- und Teilfreistellungslogik  
- 📲 Minimal-invasiv: Benachrichtigt nur bei relevanten Chancen  

---

## 🧠 Strategie-Übersicht
- **Drawdown-Analyse (MDD)**: Erkennung signifikanter Kursrückgänge  
- **ATR-basierte Valley Detection**: Identifikation lokaler Tiefpunkte in Relation zur Volatilität  
- **Momentum-Gates**: Bestätigung durch Aufwärtstrend, um Fehlsignale zu vermeiden  
- **Opportunity-Scoring**: Kombiniert technische Signalqualität, Liquidität und steuerliche Optimierung  

---

## 📸 Demo – Telegram Alert  

<img src="./assets/mdd-booster-demo.png" alt="ETF Booster Demo" width="500"/>  

*Beispiel: Telegram-Benachrichtigung mit Valley-Ranking und Recovery-Infos. Dieser Screenshot dient nicht zur Finanzberatung.*  

---

## 🖥️ Architektur (vereinfachter Überblick)
```mermaid
flowchart TD
    A[Kursdaten yfinance] --> B[Analyse-Engine MDD & ATR-Logik]
    B --> C[Momentum-Gate und Opportunity-Score]
    C --> D[Trigger-Logik]
    D --> E[Persistenz: CSV oder SQLite]
    D --> F[Benachrichtigung via Telegram API]
```
---

## 🚀 Geplante Erweiterungen  

- 💾 Rebalancing-Vorschläge  
- 🧮 Backtesting der Monats-Empfehlungen  
- 🌐 UI mit Streamlit oder Web-Dashboard  
- 🧠 LLM-Parsing von Transaktionen aus Freitext  

---

## 🛠 Technologien & Tools  

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)  
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)  
![yfinance](https://img.shields.io/badge/yfinance-003B57?style=flat)  
![Telegram](https://img.shields.io/badge/Telegram-26A5E4?style=flat&logo=telegram&logoColor=white)  

---

## 📄 Lizenz & Status  

🔒 **Code privat** – Nur Konzept und Dokumentation öffentlich  
📌 **Status:** Work in Progress  
