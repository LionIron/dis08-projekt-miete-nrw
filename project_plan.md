# DIS08 Projektplan – Mieten & Wohnkosten in NRW

## 1. Thema und Motivation

Ich untersuche Angebotsmieten von Wohnungen in Deutschland mit Fokus auf Nordrhein-Westfalen (NRW).  
Mich interessiert, wie hoch die Mieten in verschiedenen Städten sind, wie sie sich nach Wohnungsgröße unterscheiden und welcher Anteil der Wohnungen als „relativ günstig“ oder „teuer“ gelten kann.

## 2. Datensätze

**Basis-Datensatz**

- **Apartment rental offers in Germany**
- Plattform: Kaggle
- Beschreibung: Enthält Wohnungsinserate aus Deutschland mit Informationen wie Stadt, Mietpreis, Wohnfläche, Zimmeranzahl usw.
- Geplanter Speicherort im Repository: `data/raw/apartment_rentals_germany.csv` (oder Original-Dateiname)

**Mögliche Zusatzdaten (später zur Anreicherung)**

- Bevölkerungszahlen je Stadt / Region in NRW  
- Durchschnittseinkommen oder Kaufkraft in NRW  
- Evtl. weitere offene Datensätze zu Wohnen / Stadtstruktur

## 3. Forschungsfragen

1. **Wie unterscheiden sich die Angebotsmieten pro Quadratmeter zwischen verschiedenen Städten in NRW?**
2. **Welcher Anteil der angebotenen Wohnungen in NRW liegt unter bestimmten Mietschwellen**  
   (z. B. unter 10 €/m² oder unter 700 € Kaltmiete)?
3. **Sind kleinere Wohnungen (z. B. < 50 m²) pro Quadratmeter teurer als größere Wohnungen (z. B. > 80 m²) in NRW?**

Optional später:

4. Verändert sich das Mietniveau je nach Ausstattung (z. B. Balkon, Einbauküche, etc.), falls im Datensatz vorhanden.

## 4. Geplante Schritte (Roadmap)

### Phase 1 – Datenbeschaffung (Obtain)

- Kaggle-Datensatz herunterladen
- Rohdaten in `data/raw/` ablegen
- Erste Sichtung der Spaltenstruktur

### Phase 2 – Datenbereinigung (Scrub)

- Filterung auf NRW (z. B. anhand von Bundesland / Städte-Liste)
- Umgang mit fehlenden Werten (NaN) in Mietpreis, Wohnfläche, Stadt
- Entfernen klar fehlerhafter Einträge (z. B. 0 m², negativen Preisen etc.)
- Auswahl relevanter Spalten (z. B. Stadt, Kaltmiete, Wohnfläche, Zimmer)

### Phase 3 – Exploration (Explore)

- Deskriptive Statistiken (Mittelwert, Median, Min/Max, Quartile)
- Verteilungen der Miete pro m² (Histogramme, Boxplots)
- Vergleich von Städten (z. B. Köln, Düsseldorf, Essen, Dortmund, …)

### Phase 4 – Analyse (Model)

- Berechnung von Kennzahlen zur Beantwortung der Forschungsfragen:
  - Miete pro m² je Stadt
  - Anteile unter bestimmten Schwellen (z. B. < 10 €/m², < 700 €)
  - Vergleich kleiner vs. großer Wohnungen
- Evtl. einfache Modelle / Korrelationen (z. B. Wohnfläche vs. €/m²)

### Phase 5 – Interpretation und Präsentation (Interpret)

- Ergebnisse verständlich zusammenfassen
- Grafiken für Poster und Notebook erstellen
- Limitierungen des Datensatzes beschreiben (z. B. nur Angebotsmieten, Zeitbezug)

## 5. Technische Umsetzung

- Programmiersprache: Python
- Tools:
  - Jupyter Notebook (`notebooks/projekt.ipynb`)
  - `pandas`, `matplotlib` / `seaborn`
- Datenorganisation:
  - `data/raw/` für Originaldaten
  - `data/processed/` für bereinigte / gefilterte Daten
