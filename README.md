# DIS08 Projekt – Mieten & Wohnungsmerkmale in Nordrhein-Westfalen (NRW)

## Projektziel
Ziel dieses Projekts ist die Analyse von Angebotsmieten für Wohnungen in Nordrhein-Westfalen (NRW).
Untersucht wird, wie sich die Miete pro Quadratmeter zwischen Städten unterscheidet und welche Wohnungsmerkmale
(z. B. Wohnfläche, Balkon, Küche, Baujahr, Heizungsart) mit höheren oder niedrigeren Mietpreisen zusammenhängen.

Das Projekt folgt dem in der Vorlesung vorgestellten **OSEMN-Framework (Obtain, Scrub, Explore, Model, Interpret)**
und nutzt Tools/Methoden aus den begleitenden Folien und Jupyter-Notebooks.

## Motivation
Steigende Wohnkosten sind ein zentrales gesellschaftliches Thema. Durch die Auswertung offener Angebotsdaten
lassen sich regionale Unterschiede und Preisfaktoren sichtbar machen (als Marktindikator, nicht als Vertragsmiete).

## Datensatz
**Quelle:** *Apartment rental offers in Germany* (Kaggle)  
Enthält Wohnungsinserate aus ganz Deutschland mit Mietpreis- und Objektmerkmalen.

Speicherort im Repo: `data/raw/immo_data.csv`

**Wichtige Spalten (Auswahl):**
- Bundesland: `regio1`
- Stadt/Kreis: `regio2`
- Kaltmiete: `baseRent`
- Gesamtmiete: `totalRent` (teilweise fehlend)
- Wohnfläche: `livingSpace`
- Zimmer: `noRooms`
- Merkmale: z. B. `balcony`, `hasKitchen`, `heatingType`, `yearConstructed`, `newlyConst`

## Forschungsfragen
1. Wie unterscheiden sich die Angebotsmieten pro Quadratmeter zwischen Städten in NRW?
2. Sind kleinere Wohnungen pro Quadratmeter teurer als größere Wohnungen?
3. Haben bestimmte Wohnungsmerkmale (z. B. Balkon, Küche, Neubau) einen messbaren Einfluss auf den Quadratmeterpreis?
4. Lassen sich **statistisch signifikante** Unterschiede zwischen Wohnungsgruppen nachweisen?
5. Lassen sich Inserate in NRW in **Cluster** einteilen (z. B. „günstig/klein“, „teuer/modern“), basierend auf Preis und Merkmalen?

## Methodisches Vorgehen (OSEMN)

### Obtain
- Datensatz laden und auf NRW filtern (`regio1 == "Nordrhein_Westfalen"`)

### Scrub (Data Cleaning)
- Auswahl relevanter Spalten
- Umgang mit fehlenden Werten (z. B. `totalRent`)
- Entfernen unrealistischer Werte (z. B. extrem hohe €/m²)
- Neue Variable: `price_per_sqm = baseRent / livingSpace`

### Explore
- Deskriptive Statistiken (Median, Quartile)
- Stadtvergleiche (Median €/m² pro `regio2`)
- Visualisierungen (Histogramm, Boxplots, Balkendiagramme)

### Model
- Hypothesentests (z. B. kleine vs. große Wohnungen; Gruppen nach Merkmalen)
- Optional/Erweiterung: Clustering auf Basis standardisierter numerischer Variablen + codierter Merkmale

### Interpret
- Ergebnisse zusammenfassen, Limitierungen erklären (Angebotsdaten ≠ Vertragsmieten)
- Grafiken/Ergebnisse für Poster und Doku nutzbar machen

## Tools & Technologien
- Python, Jupyter Notebook
- pandas, NumPy
- matplotlib
- Git/GitHub (Versionierung, Dokumentation)

## Repository-Struktur
```text
data/
  raw/        # Originaldaten (lokal; nicht zwingend im Repo, je nach .gitignore)
  processed/  # Bereinigte/abgeleitete Daten
docs/         # Projekt-Dokumentation / Poster
notebooks/    # Analyse-Notebooks
src/          # Wiederverwendbare Funktionen/Skripte
README.md
project_plan.md

## Hinweis zur Interpretation

Dieses Projekt analysiert Angebotsmieten aus Inseraten. Die Ergebnisse zeigen Marktindikatoren und Trends,
aber bilden nicht exakt tatsächliche Vertragsmieten ab.