# DIS08 Projekt – Mieten in Nordrhein-Westfalen
## Thema
Analyse von Angebotsmieten in Nordrhein-Westfalen (NRW) mit Fokus auf Mietpreise pro Quadratmeter, Unterschiede zwischen Städten und Wohnungsgrößen.

Das Projekt folgt dem in der Vorlesung vorgestellten OSEMN-Framework (Obtain, Scrub, Explore, Model, Interpret) und nutzt ausschließlich Tools und Methoden aus den begleitenden Folien und Jupyter Notebooks.
## Motivation
Steigende Wohnkosten sind ein zentrales gesellschaftliches Thema.
Ziel dieses Projekts ist es, mithilfe offener Daten zu untersuchen:
<br>
<li>wie stark sich Mietpreise zwischen Städten in NRW unterscheiden,</li>
<li>wie verbreitet günstige bzw. teure Mietangebote sind,</li>
<li>ob kleinere Wohnungen pro Quadratmeter teurer sind als größere.</li>

## Datensatz

<b>Quelle:</b><br>
Apartment rental offers in Germany (Kaggle)
<link>https://www.kaggle.com/datasets/corrieaar/apartment-rental-offers-in-germany</link>

## Speicherort
<code>data/raw/immo_data.csv</code>

## Beschreibung
Der Datensatz enthält Wohnungsinserate aus ganz Deutschland mit Informationen u. a. zu:
<li>Bundesland <code>(regio1)</code></li>
<li>Stadt <code>(regio2)</code></li>
<li>Kaltmiete <code>(baseRent)</code></li>
<li>Wohnfläche <code>(livingSpace)</code></li>
<li>Anzahl Zimmer <code>(noRooms)</code></li>
<li>Gesamtmiete <code>(totalRent)</code></li>
<br>
Für die Analyse wurde ausschließlich Nordrhein-Westfalen betrachtet.

## Forschungsfragen
<ol>Wie unterscheiden sich die Angebotsmieten pro Quadratmeter zwischen Städten in NRW?</ol>
<ol>Welcher Anteil der Wohnungen liegt unter bzw. über bestimmten Mietschwellen (z. B. < 10 €/m², > 15 €/m²)?</ol>
<ol>Sind kleinere Wohnungen (< 50 m²) pro Quadratmeter teurer als größere Wohnungen (> 80 m²)?</ol>

