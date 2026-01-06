# DIS08 Projekt – Mieten in Nordrhein-Westfalen
## Projektziel
Ziel dieses Projekts ist die Analyse von Angebotsmieten für Wohnungen in Nordrhein-Westfalen (NRW).
Untersucht wird, wie sich die Miete pro Quadratmeter zwischen Städten unterscheidet und welche Wohnungsmerkmale (z. B. Wohnfläche, Ausstattung, Baujahr) mit höheren oder niedrigeren Mietpreisen zusammenhängen.

Das Projekt folgt dem in der Vorlesung vorgestellten OSEMN-Framework (Obtain, Scrub, Explore, Model, Interpret) und nutzt ausschließlich Tools und Methoden aus den begleitenden Folien und Jupyter Notebooks.
## Motivation
Steigende Wohnkosten sind ein zentrales gesellschaftliches Thema.
Ziel dieses Projekts ist es, mithilfe offener Daten zu untersuchen:
<br>
<li>Wie stark sich Mietpreise zwischen Städten in NRW unterscheiden,</li>
<li>Wie verbreitet günstige bzw. teure Mietangebote sind,</li>
<li>Ob kleinere Wohnungen pro Quadratmeter teurer sind als größere.</li>

## Datensatz

<b>Quelle:</b><br>
Apartment rental offers in Germany (Kaggle)
<li>Angebotsdaten von Wohnungsinseraten</li>

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
<ol>1. Wie unterscheiden sich die Angebotsmieten pro Quadratmeter zwischen Städten in NRW?</ol>
<ol>2. Sind kleinere Wohnungen pro Quadratmeter teurer als größere Wohnungen?</ol>
<ol>3. Haben bestimmte Wohnungsmerkmale (z. B. Balkon, Neubau) einen messbaren Einfluss auf den Quadratmeterpreis? (> 80 m²)?</ol>
<ol>4. Lassen sich statistisch signifikante Unterschiede zwischen Wohnungsgruppen nachweisen?</ol>

## Methodisches Vorgehen
Das Projekt orientiert sich an den in der Vorlesung behandelten Phasen:
### Datenaufbereitung (Data Cleaning)
<li>Entfernen fehlender oder unrealistischer Werte</li>
<li>Berechnung des Mietpreises pro Quadratmeter</li>
<li>Filterung extremer Ausreißer</li>

### Exploration
<li>Deskriptive Statistiken (Mittelwert, Median, Quartile)</li>
<li>Verteilungen der Quadratmeterpreise</li>
<li>Stadtvergleiche mittels Aggregationen und Visualisierungen</li>

### Datenstrukturen & Gruppierung
<li>Einteilung von Wohnungen nach Größe (z. B. klein / groß)</li>
<li>Gruppierung nach Städten und Wohnungsmerkmalen</li>

### Hypothesentests
<li>Formulierung von Null- und Alternativhypothesen</li>
<li>Vergleich von Gruppen (z. B. kleine vs. große Wohnungen)</li>
<li>Einsatz statistischer Tests gemäß Vorlesungsinhalt</li>

## Tools & Technologien
<li>Python</li>
<li>Jupyter Notebook</li>
<li>pandas</li>
<li>matplotlib</li>
<li>numpy</li>

Alle verwendeten Tools wurden im Rahmen der Vorlesung behandelt.
