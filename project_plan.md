Project Plan – Mietpreise NRW (DIS08 Project)
1. Thema / Motivation

Mietpreise in NRW steigen seit Jahren. Besonders in Städten wie Köln, Düsseldorf, Bonn und Münster gibt es Wohnraummangel und hohe Preissteigerungen.
Ziel des Projekts ist es, Open Data zu Mietpreisen mit selbst gescrapten Daten (z. B. Immobilienportale, Stadt-Webseiten, Wikipedia) zu kombinieren, um Trends zu analysieren.

Warum interessant?

Relevantes gesellschaftliches Thema

Gute Datenlage (Open Data + Web Scraping)

Viele Analyse-Möglichkeiten

Gut für Machine Learning später (Preisvorhersage)

2. Basis-Datasets (Open Data)

Geplante Datengrundlagen:

NRW Open Data Portal

Mietspiegel NRW

Kommunale Mietdaten

Bevölkerungszahlen
Quelle: https://open.nrw/

Köln Open Data Portal

Stadtteile, Demografie, Haushaltsgrößen
Quelle: https://offenedaten-koeln.de/

Statistisches Bundesamt

Verbraucherpreisindex Wohnen
Quelle: https://www-genesis.destatis.de/

3. Geplante Data Enrichment (Web Scraping)

Du wirst zusätzlich scrapen:

Immoscout24 (Wohnungsgrößen, Kaltmiete, Lageinformationen)

Wikipedia Stadtteilseiten (Einwohnerzahl, Fläche, Bevölkerungsdichte)

Tools:

requests

BeautifulSoup

selbst entwickelter Scraper

4. Research Questions

Wie haben sich Mietpreise in NRW seit 2010 entwickelt?

Welche Städte/Stadtteile sind am teuersten – und warum?

Wie korrelieren Mietpreise mit Faktoren wie Bevölkerungsdichte, Einkommen oder Haushaltsgröße?

Kann ein einfaches Machine-Learning-Modell Mietpreise sinnvoll vorhersagen?

Sind bestimmte Plattformen (z. B. Immoscout) teurer als offizielle Mietspiegel?

5. Roadmap (Milestone Plan)
Milestone 1 – 07.11.2025

Thema festlegen ✔

Datasets auswählen ✔

Research Questions formulieren ✔

Roadmap erstellen ✔

Milestone 2 – 12.12.2025

Web Scraper bauen

Daten herunterladen

Daten bereinigen

Dataset anreichern (Mietdaten + Stadtteilinfos)

Pipeline-Prototyp erstellen

Neue Daten online hosten (z. B. GitHub)

Milestone 3 – 19.01.2026

Analyse (Statistik + Visualisierung)

Machine-Learning-Teil

Poster erstellen

Code + Notebook fertig

Präsentation