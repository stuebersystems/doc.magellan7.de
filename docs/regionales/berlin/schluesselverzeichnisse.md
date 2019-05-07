#	Berliner Schlüsselverzeichnisse

In den Berliner Masken gibt es zusätzliche oder anders benannte Felder. Nachstehend finden Sie eine Übersicht welches Schlüsselverzeichnis hinter den einzelnen Feldern liegt. Für die MAGELLAN-Standardansicht wird diese Zuordnung im MAGELLAN-Benutzerhandbuch im Abschnitt [Referenz > Schlüsselverzeichnisse](https://doc.magellan6.stueber.de/reference/catalogs.html) beschrieben. 

## Legende

Spaltenkopf|Bedeutung
---|---
**Verzeichnis**|Name des Verzeichnisses in der MAGELLAN-Oberfläche
**Datenstruktur**|Name des Verzeichnisses in der MAGELLAN-Datenstruktur
**Mandant**|ist das Verzeichnis mandantenübergreifend (nein) oder pro Mandant vorhanden (ja)
**Ansicht**|Stelle, an der Felder in MAGELLAN auf dieses Verzeichnis verweisen
***.keys**|Hinweis darüber, ob die Schlüssel in importierbarer Form (*.keys) zur Verfügung gestellt werden

## Tabelle der Berliner Schlüsselverzeichnisse

Spalte|Inhalt
---|---
**Verzeichnis**|**Abgangsarten (Lehrer)**
Datenstruktur|LehrerAbgaenge
Mandant|Nein
Ansicht|Lehrkraft > Daten2
*.keys|ja
**Verzeichnis**| **Abgangsarten (Schüler)**
Datenstruktur| Abgangsarten
Mandant| Nein
Ansicht| Schüler > Zugang/Abgang > Abgangsarten
*.keys|ja
**Verzeichnis**|**Abordnungsarten**
Datenstruktur|Abordnungsarten
Mandant|Nein
Ansicht|Lehrkraft > Daten3 > Art1<br/>Lehrkraft > Daten3 > Art2
*.keys|nein
**Verzeichnis**|**Abschlussarten**
Datenstruktur|Abschlussarten
Mandant|Nein
Ansicht|Schüler > Laufbahn > Abschluss > Abschlussart1<br/>Schüler > Laufbahn > Abschluss > Abschlussart2
*.keys|Nein
**Verzeichnis**|**Abschlüsse (Extern)**
Datenstruktur|AbschluesseExtern
Mandant|Nein
Ansicht|Schüler > Daten2 > Höchster Abschluss ABS > Abschluss<br/>Schüler > Daten2 > Höchster Abschluss BBS > Abschluss
*.keys|Ja
**Verzeichnis**|**Abschlüsse (Intern)**
Datenstruktur|AbschluesseIntern
Mandant|Nein
Ansicht|Schüler > Laufbahn > Abschluss > Abschluss1<br/>Schüler > Laufbahn > Abschluss > Abschluss2<br/>Schüler > Berufsbildung > Schullaufbahn ABS > Abschluss<br/>Schüler > Berufsbildung > Schullaufbahn BBS > Abschluss<br/>Bewerber > Berufsbildung > Schullaufbahn ABS > Abschluss<br/>Bewerber > Berufsbildung > Schullaufbahn BBS > Abschluss<br/>Schüler > SekII > Schullaufbahn > Abschluss<br/>Bewerber > SekII > Schullaufbahn > Abschluss<br/>Schüler > SekI > Schullaufbahn > Abschluss<br/>Bewerber > SekI > Schullaufbahn > Abschluss<br/>Schüler > Grundstufe > Schullaufbahn > Abschluss<br/>Bewerber > Grundstufe > Schullaufbahn > Abschluss
*.keys|Ja
**Verzeichnis**|**Abschlussjahrgänge**
Datenstruktur|Abschlussjahrgaenge
Mandant|Ja
Ansicht|Abitur > Qualifikation > Abiturjahrgang
*.keys|Nein
**Verzeichnis**|**Abteilungen**
Datenstruktur|Abteilungen
Mandant|Ja
Ansicht|Klassen > Daten > Abteilung<br/>Lehrkraft > Daten2 > Abteilung1<br/>Lehrkraft > Daten2 > Abteilung2<br/>Lehrkraft > Daten2 > Abteilung3
*.keys|Nein
**Verzeichnis**|**Amtsbezeichnungen**
Datenstruktur|Amtsbez
Mandant|Nein
Ansicht|Lehrkraft > Daten2 > Amtsbez
*.keys|Ja
**Verzeichnis**|**Arbeitsämter**
Datenstruktur|Arbeitsaemter
Mandant|Nein
Ansicht|Betriebe > Daten1 > Arbeitsamt
*.keys|Nein
**Verzeichnis**|**Arten**
Datenstruktur|ASVArten
Mandant|Nein
Ansicht|Schüler > Zeugnis > Arbeits-und Sozialverhalten
*.keys|nein
**Verzeichnis**|**Aufnahmeprüfungen**
Datenstruktur|Aufnahmepruefungen
Mandant|Nein
Ansicht|Schüler > Laufbahn > Aufnahmeprüfung
*.keys|Nein
**Verzeichnis**|**Ausbildungen (Lehrer)**
Datenstruktur|LehrerAusbildung
Mandant|Nein
Ansicht|Lehrkraft > Daten2 > Ausbildung
*.keys|Ja
**Verzeichnis**|**Banken**
Datenstruktur|Banken
Mandant|Nein
Ansicht|Mandanten > Daten2 > Bank<br/>Schüler > Daten4 > Bank<br/>Bewerber > Daten4 > Bank
*.keys|Ja
**Verzeichnis**|**Behinderungsarten**
Datenstruktur|Behinderungsarten
Mandant|Nein
Ansicht|Klassen > Daten > Behinderung<br/>Bewerber > Daten3 > Behinderung<br/>Bewerber > Grundstufe > Förderschwerpunkt<br/>Bewerber > SekI > Förderschwerpunkt<br/>Bewerber > SekII > Förderschwerpunkt<br/>Bewerber > Berufsbildung > Förderschwerpunkt<br/>Schüler > Daten3 > Behinderung<br/>Schüler > Grundstufe > Förderschwerpunkt<br/>Schüler > SekI > Förderschwerpunkt<br/>Schüler > SekII > Förderschwerpunkt<br/>Schüler > Berufsbildung > Förderschwerpunkt
*.keys|Ja
**Verzeichnis**|**Berufe**
Datenstruktur|Berufe
Mandant|Nein
Ansicht|Betriebe > Daten2 > Berufe<br/>Klasse > Daten > Beruf<br/>Schüler > Ausbildung > Beruf<br/>Bewerber > Ausbildung > Beruf<br/>Bewerber > Berufsbildung > Schullaufbahn BBS > Beruf<br/>Schüler > Berufsbildung > Schullaufbahn BBS > Beruf<br/>Bewerber > Berufsbildung > Ausbildung/Praktikum > Beruf<br/>Schüler > Berufsbildung > Ausbildung/Praktikum > Beruf
*.keys|Ja
**Verzeichnis**|**Berufsfelder**
Datenstruktur|Berufsfelder
Mandant|Nein
Ansicht|Klasse > Daten > Berufsfeld
*.keys|Ja
**Verzeichnis**|**Beschäftigungsverhältnisse**
Datenstruktur|Beschaeftigungsverh
Mandant|Nein
Ansicht|Lehrkraft > Daten2 > Besch-verh.
*.keys|Nein
**Verzeichnis**|**Besoldungen**
Datenstruktur|Besoldungen
Mandant|Nein
Ansicht|Lehrkraft > Daten2 > Besoldung
*.keys|Ja
**Verzeichnis**|**Betreuungen außerschulisch (Schüler)**
Datenstruktur|BetreuungenAusserschulisch
Mandant|Nein
Ansicht|Schüler > Extras > Außerschulisch 1<br/>Schüler > Extras > Außerschulisch 2<br/>Schüler > Extras > Außerschulisch 3<br/>Bewerber > Extras > Außerschulisch 1<br/>Bewerber > Extras > Außerschulisch 2<br/>Bewerber > Extras > Außerschulisch 3
*.keys|Ja
**Verzeichnis**|**Betreuungen innerschulisch (Schüler)**
Datenstruktur|BetreuungenInnerschulisch
Mandant|	Nein
Ansicht|	Schüler > Extras > Innerschulisch 1<br/>Schüler > Extras > Innerschulisch 2<br/>Schüler > Extras > Innerschulisch 3<br/>Bewerber > Extras > Innerschulisch 1<br/>Bewerber > Extras > Innerschulisch 2<br/>Bewerber > Extras > Innerschulisch 3
*.keys|	Ja
**Verzeichnis**|**Betreuungsformen(Mandanten)**
Datenstruktur|Betreuungsformen
Mandant|Nein
Ansicht|	Mandant > Daten1 > Betreungsform
*.keys|Nein
**Verzeichnis**|**Bevollmächtigungen**
Datenstruktur|Bevollmaechtigungen
Mandant|	Nein
Ansicht|	Lehrkraft > Daten2 > Bevollmächtigung
*.keys|Nein
**Verzeichnis**|**Bewerbungsempfehlungen**
Datenstruktur|Bewerbungsempfehlungen
Mandant|	Nein
Ansicht|	Bewerber > SekII > Vornoten > OG-Berechtigungen<br/>Bewerber > SekI > Anmeldung/Förderprognose > Empfehlung
*.keys|	Ja
**Verzeichnis**|**Bewerbungsziele**
Datenstruktur|Bewerbungsziele
Mandant|Nein
Ansicht|	Bewerber > Daten1 > Für Ziel 1-Für Ziel 4<br/>Bewerber > SekII > Anmeldung > Für Ziel 1-Für Ziel 4<br/>Bewerber > Berufsbildung > Für Ziel 1-Für Ziel 2
*.keys|Nein
**Verzeichnis**|**Bewertungen**
Datenstruktur|ASVBewertungen
Mandant|	Nein
Ansicht|Schüler > Zeugnis > Arbeits- und Sozialverhalten
*.keys|Nein
**Verzeichnis**|**Bildungsgänge**
Datenstruktur|Bildungsgaenge
Mandant|	Nein
Ansicht|Betriebe > Daten2 > Bildungsgänge<br/>Klassen > Daten > Bildungsgang<br/>Schüler > Ausbildung > Bildungsgang<br/>Schüler > Daten2 > Höchster Abschluss ABS > Bildungsgang<br/>Schüler > Daten2 > Höchster Abschluss BBS > Bildungsgang<br/>Bewerber > Ausbildung > Bildungsgang<br/>Bewerber > Berufsbildung > Ausbildung/Praktikum > Bildungsgang<br/>Schüler > Berufsbildung > Ausbildung/Praktikum > Bildungsgang
*.keys|Ja
**Verzeichnis**|**Branchen**
Datenstruktur|Branchen
Mandant|Nein
Ansicht|Betriebe > Daten1 > Betriebe
*.keys|Nein
**Verzeichnis**|**Dienstbezeichnungen**
Datenstruktur|Dienstbez
Mandant|Nein
Ansicht|Lehrkraft > Daten2 > Dienstbez	
*.keys|Ja
**Verzeichnis**|**Dienstherren**
Datenstruktur|Dienstherren
Mandant|Nein
Ansicht|Lehrkraft > Daten2 > Dienstherr
*.keys|Nein
**Verzeichnis**|**Dienstverhältnisse**
Datenstruktur|Dienstverh
Mandant|Nein
Ansicht|Lehrkraft > Daten2 > Dienstver	
*.keys|Ja
**Verzeichnis**|**Disziplinen**
Datenstruktur|Disziplinen
Mandant|Ja
Ansicht|Sportfeste > Disziplinen und Ergebnisse
*.keys|Nein
**Verzeichnis**|**Einschulmerkmale**
Datenstruktur|Einschulmerkmale
Mandant|	Nein	
Ansicht|Schüler > Daten1 > Einschulmerkmal<br/>Schüler > Grundstufe > Einschulmerkmal<br/>Schüler > SekI > Einschulmerkmal<br/>Schüler > SekII > Einschulmerkmal<br/>Schüler > Berufsbildung > Einschulmerkmal<br/>Bewerber > Daten1 > Einschulmerkmal<br/>Bewerber > Grundstufe > Einschulmerkmal<br/>Bewerber > SekI > Einschulmerkmal<br/>Bewerber > SekII > Einschulmerkmal<br/>Bewerber > Berufsbildung > Einschulmerkmal
*.keys|	Nein
**Verzeichnis**|**Empfehlungen**
Datenstruktur|Empfehlungen
Mandant|Nein	
Ansicht|Schüler > Laufbahn > Empfehlung
*.keys|	Ja
**Verzeichnis**|**Entscheidungen**
Datenstruktur|Entscheidungen	
Mandant|Nein	
Ansicht|Schüler > Laufbahn > Entscheidung
*.keys|	Nein
**Verzeichnis**|**Fächer**
Datenstruktur|Faecher
Mandant|Ja
Ansicht|Schüler > Zeugnis > Fächer > Fach<br/>Bewerber/Schüler > Daten3 > Fremdspachenfolge > 1.FS- 4.FS<br/>Bewerber/Schüler > Daten3 > Fremdspachenfolge > 1.FS- 4.FS<br/>Bewerber/Schüler > Grundstufe > Kurs1-Kurs2<br/>Bewerber/Schüler > SekI > Profilfächer > Fach 1-Fach 6<br/>Bewerber/Schüler > SekI > Sprachenfolge und Sprachenwahl > FS1 –FS4<br/>Bewerber/Schüler > SekII > Sprachenfolge und Sprachenwahl > FS1 –FS4<br/>Bewerber/Schüler > SekII > Wahlpflichtfächer und Kurse > Wahlfach 1-6<br/>Bewerber/Schüler > Berufsbildung > Sprachenfolge und Sprachenwahl > FS1 –FS4<br/>Bewerber/Schüler > Berufsbildung > Wahlpflichtfächer und Kurse > Wahlfach 1-4
*.keys|	Ja
**Verzeichnis**|**Fachgruppen**
Datenstruktur|Fachgruppen
Mandant|	Nein
Ansicht|	Verzeichnisse > Fächer > Gruppe
*.keys|	Nein
**Verzeichnis**|**Fachniveaus**
Datenstruktur|Fachniveaus	
Mandant|Nein	
Ansicht|Schüler > Zeugnis > Fächer > Niveau
*.keys|	Ja
**Verzeichnis**|**Fachrichtungen**
Datenstruktur|Fachrichtungen
Mandant|	Nein
Ansicht|	Verzeichnisse > Bildungsgänge > Fachrichtung<br/>Verzeichnisse > Berufe > Fachrichtung
*.keys|Ja
**Verzeichnis**|**Fachschwerpunkte**
Datenstruktur|Fachschwerpunkte
Mandant|	Nein
Ansicht|	Schüler > Zeugnis > Fächer > Schwerpunkt
*.keys|	Nein
**Verzeichnis**|**Fachstatus**
Datenstruktur|Fachstati	
Mandant|Nein
Ansicht|	Schüler > Zeugnis > Fächer > Fachstatus<br/>Abitur > Qualifikation > Fachstatus<br/>Berufsschule > Matrix > Fachstatus<br/>Verzeichnisse > Fachtafeln > Fachtafelfächer > Fachstatus	
*.keys|Ja
**Verzeichnis**|**Fachtafeln**
Datenstruktur|Fachtafel	
Mandant|Ja
Ansicht|	Verzeichnisse > Fachtafeln
*.keys|	Nein
**Verzeichnis**|**Fachthemen**	
Datenstruktur|FaecherThemen
Mandant|Ja	
Ansicht|Verzeichnisse > Fachthemen	
*.keys|Nein
**Verzeichnis**|**Fahrkarten**
Datenstruktur|Fahrkarten
Mandant|	Nein	
Ansicht|Schüler > Daten4 > Fahrkarten<br/>Bewerber > Daten4 > Fahrkarten
*.keys|	Nein
**Verzeichnis**|**Fehlgründe (Lehrer)**
Datenstruktur|LehrerFehlgruende
Mandant|	Nein	
Ansicht|Lehrkraft > Fehlzeiten > Grund	
*.keys|Nein
**Verzeichnis**|**Förderbedarf**
Datenstruktur|SopaedFoerderungen
Mandant|	Nein	
Ansicht|Schüler > Daten4 > Sonstige Daten > Förderbedarf<br/>Bewerber > Daten4 > Sonstige Daten > Förderbedarf<br/>Schüler > Sekundarstufe II > Besondere Schülerdaten > Schularzt
*.keys|Nein
**Verzeichnis**|**Förderungen**
Datenstruktur|Foerderungen
Mandant|Nein	
Ansicht|Schüler > Daten4 > Förderung > Förderung<br/>Bewerber > Daten4 > Förderung > Förderung	
*.keys|Nein
**Verzeichnis**|**Funktionen (Lehrer)**
Datenstruktur|LehrerFunktionen
Mandant|	Nein	
Ansicht|Lehrkraft > Daten3 > Funktion1-8	
*.keys|Nein
**Verzeichnis**|**Funktionen (Schüler)**
Datenstruktur|SchuelerFunktionen
Mandant|	Nein	
Ansicht|Schüler > Daten3 > Funktion1-8<br/>Bewerber > Daten3 > Funktion1-8	
*.keys|Nein
**Verzeichnis**|**Funktionen (Sorgeberechtigte)**
Datenstruktur|SorgebeFunktionen
Mandant|Nein	
Ansicht|Sorgeberechtigte > Daten > Funktion1-8	
*.keys|Nein
**Verzeichnis**|**Härtefälle**
Datenstruktur|Haertefaelle
Mandant|Nein	
Ansicht|Bewerber > SekI > Anmelde/Förderprognose	
*.keys|Nein
**Verzeichnis**|**Herkunftsarten**
Datenstruktur|Herkunftsarten
Mandant|Nein	
Ansicht|Schüler > Zugang/Abgang > Bereits besuchte Schulen > Herkunftsart<br/>Bewerber > Zugang > Bereits besuchte Schulen > Herkunftsart<br/>Bewerber > Grundstufe > Laufbahn > Herkunftsart<br/>Bewerber > SekI > Laufbahn > Herkunftsart<br/>Bewerber > SekII > Laufbahn > Herkunftsart<br/>Bewerber > Berufsbildung > Laufbahn > Herkunftsart<br/>Schüler > Grundstufe > Laufbahn > Herkunftsart<br/>Schüler > SekI > Laufbahn > Herkunftsart<br/>Schüler > SekII > Laufbahn > Herkunftsart<br/>Schüler > Berufsbildung > Laufbahn > Herkunftsart
*.keys|Ja
**Verzeichnis**|**Herkunftsunterlagen**
Datenstruktur|Herkunftsunterlagen	
Mandant|Nein	
Ansicht|Schüler > Zugang/Abgang > Bereits besuchte Schulen > Herkunftsunterlagen<br/>Bewerber > Zugang > Bereits besuchte Schulen > Herkunftsunterlagen<br/>Bewerber > Grundstufe > Laufbahn > Herkunftsunterlagen<br/>Bewerber > SekI > Laufbahn > Herkunftsunterlagen<br/>Bewerber > SekII > Laufbahn > Herkunftsunterlagen<br/>Bewerber > Berufsbildung > Laufbahn > Herkunftsunterlagen<br/>Schüler > Grundstufe > Laufbahn > Herkunftsunterlagen<br/>Schüler > SekI > Laufbahn > Herkunftsunterlagen<br/>Schüler > SekII > Laufbahn > Herkunftsunterlagen<br/>Schüler > Berufsbildung > Laufbahn > Herkunftsunterlagen
*.keys|Nein
**Verzeichnis**|**Inhaltetafeln**
Datenstruktur|ASVInhaltetafeln
Mandant|Ja
Ansicht|Schüler > Zeugnis > Arbeits- und Sozialverhalten
*.keys|	Nein
**Verzeichnis**|**Integrationsmerkmale**
Datenstruktur|Integrationsmerkmale
Mandant|Nein	
|Klassen > Daten > Integration
*.keys|	Ja
**Verzeichnis**|**Kammern**
Datenstruktur|Kammern
Mandant|Nein	
Ansicht|Betriebe > Daten1 > Kammern	
*.keys|Nein
**Verzeichnis**|**Kategoriegruppen**
Datenstruktur|ASVKategoriegruppen	
MandantMandant|Nein	
Ansicht|Schüler > Zeugnis > Arbeits- und Sozialverhalten
*.keys|Nein
**Verzeichnis**|**Kategorien**
Datenstruktur|ASVKategorien	
Mandant|Nein	
Ansicht|Schüler > Zeugnis > Arbeits- und Sozialverhalten	
*.keys|Nein
**Verzeichnis**|**Kategorien (Adressen)**
Datenstruktur|Adressenkategorien
Mandant|Nein
Ansicht|Adressen > Daten > Kategorie
*.keys|	Nein
**Verzeichnis**|**Kategorien (Lehrer)**
Datenstruktur|Lehrerkategorien
Mandant|Nein
Ansicht|Lehrkraft > Daten1 > Kategorie
*.keys|Nein
**Verzeichnis**|**Kategorien (Mandanten)**
Datenstruktur|Mandantenkategorien	
Mandant|Nein	
Ansicht|Mandant > Daten1 > Schulform	
*.keys|Nein
**Verzeichnis**|**Kategorien (Personen)**
Datenstruktur|Personenkategorien	
Mandant|Nein
Ansicht|Personen > Daten > Kategorie	
*.keys|Nein
**Verzeichnis**|**Kategorietafeln**
Datenstruktur|ASVTafelkategorien	
Mandant|Ja	
Ansicht|Schüler > Zeugnis > Arbeits- und Sozialverhalten
*.keys|Nein
**Verzeichnis**|**Klassenmerkmale**
Datenstruktur|Klassenmerkmale	
Mandant|Ja	
Ansicht|Klassen > Merkmale > Merkmal A1-A6<br/>Klassen > Merkmale > Merkmal S1-S4
*.keys|Nein
**Verzeichnis**|**Klassenorganisationen**
Datenstruktur|Klassenorganisationen	
Mandant|Nein	
Ansicht|Klassen > Daten > KL-Organisation
*.keys|Ja
**Verzeichnis**|**Klassenstufen**
Datenstruktur|Klassenstufen	
Mandant|Nein	
Ansicht|Klasse > Zeiträume > Allgemein > Klassenstufen	
*.keys|Ja
**Verzeichnis**|**Konfessionen**
Datenstruktur|Konfessionen	
Mandant|Nein	
Ansicht|Schüler > Daten1 > Konfession<br/>Bewerber > Daten1 > Konfession<br/>Schüler > Grundstufe > Besondere Schülerdaten > Konfession<br/>Bewerber > Grundstufe > Besondere Schülerdaten > Konfession<br/>Schüler > SekI > Besondere Schülerdaten > Konfession<br/>Bewerber > SekI > Besondere Schülerdaten > Konfession<br/>Schüler > SekIIBesondere Schülerdaten > Konfession<br/>Bewerber > SekII > Besondere Schülerdaten > Konfession<br/>Schüler > Berufsbildung > Besondere Schülerdaten > Konfession<br/>Bewerber > Berufsbildung > Besondere Schülerdaten > Konfession	
*.keys|Ja
**Verzeichnis**|**Krankenkassen**
Datenstruktur|Krankenkassen	
Mandant|Nein
Ansicht|Schüler > Daten4 > Krankenkasse<br/>Bewerber > Daten4 > Krankenkasse
*.keys|Nein
**Verzeichnis**|**Lehrämter**
Datenstruktur|Lehraemter
Mandant|Nein
Ansicht|Lehrkraft > Daten3 > Lehrämter > Lehramt
*.keys|Ja
**Verzeichnis**|**Lehrermerkmale**
Datenstruktur|Lehrermerkmale
Mandant|Ja	
Ansicht|Lehrkraft > Merkmale > MerkmalA1-A6<br/>Lehrkraft > Merkmale > MerkmalS1-S4
*.keys|Nein
**Verzeichnis**|**Lehrer-Soll-Schlüssel**
Datenstruktur|LehrerSollSchluessel
Mandant|Ja
Ansicht|Lehrkraft > Sollberechnung
*.keys|Nein
**Verzeichnis**|**Mandantenmerkmale**
Datenstruktur|MandantenMerkmale	
Mandant|Nein
Ansicht|Mandanten > Merkmale > A1-A6	
*.keys|Nein
**Verzeichnis**|**Muttersprachen**
Datenstruktur|Muttersprachen
Mandant|Nein
Ansicht|Schüler > Daten2 > Muttersprache<br/>Bewerber > Daten2 > Muttersprache
*.keys|Ja
**Verzeichnis**|**Nachprüfungen**
Datenstruktur|Nachpruefungen
Mandant|	Nein	
Ansicht|Schüler > Laufbahn > Allgemein > Nachprüfung	
*.keys|Nein
**Verzeichnis**|**Noten**	
Datenstruktur|Noten	
Mandant|Ja	
Ansicht|Schüler > Zeugnis > Leistungen > Endnote<br/>Schüler > Zeugnis > Leistungen > Schriftl.Note1-4<br/>Schüler > Zeugnis > Leistungen > Mündl.Note<br/>Schüler > Zeugnis > Leistungen > Zusatz Note 1-3<br/>Schüler > Zeugnis > Leistungen > Endnote (Gesamt)<br/>Abitur > Qualifikation > 11/1-13/2<br/>Abitur > Prüfung > Prüfungsfächer<br/>Zeugnis > Details > Verhalten<br/>Zeugnis > Details > Mitarbeit<br/>Berufsschule > Matrix > J1 Note –J9 Note<br/>Berufsschule > Matrix > Zusatznote1-5
*.keys|Ja
**Verzeichnis**|**Organisationen**
Datenstruktur|Organisationen	
Mandant|Nein	
Ansicht|Klasse > Daten > Organisation
*.keys|Ja
**Verzeichnis**|**Postleitzahlen**
Datenstruktur|Postleitzahlen
Mandant|	Nein
Ansicht|Schüler > Daten1 > Postleitzahl<br/>Schüler > Grundstufe > Postleitzahl<br/>Schüler > SekI > Postleitzahl<br/>Schüler > SekII > Postleitzahl<br/>Schüler > Berufsbildung > Postleitzahl<br/>Bewerber > Daten1 > Postleitzahl<br/>Bewerber > Grundstufe > Postleitzahl<br/>Bewerber > SekI > Postleitzahl<br/>Bewerber > SekII > Postleitzahl<br/>Bewerber > Berufsbildung > Postleitzahl<br/>Lehrkraft > Daten1 > Postleitzahl<br/>Betriebe > Daten > Postleitzahl<br/>Mandanten > Daten > Postleitzahl<br/>Personen > Daten > Postleitzahl<br/>Sorgeberechtigte > Postleitzahl<br/>Adressen > Daten > Postleitzahl
*.keys|Ja
**Verzeichnis**|**Profile (Schüler)**
Datenstruktur|SchuelerProfile
Mandant|	Nein	
Ansicht|Schüler > Daten3 > Verschiedenes > Profil<br/>Bewerber > Daten3 > Verschiedenes > Profil
*.keys|Nein
**Verzeichnis**|**Prüfungsbezüge (Lehrer)**
Datenstruktur|LehrerPruefungsbezuege
Mandant|	Nein
Ansicht|	Lehrkraft > Daten3 > Lehrämter > Prüfungsbezug
*.keys|Nein
**Verzeichnis**|**Qualifikationsniveaus**
Datenstruktur|Qualifikationsniveaus
Mandant|	Nein	
Ansicht|Verzeichnisse > Bildungsgänge > DQR-Stufe<br/>Verzeichnisse > Berufe > DQR-Stufe
*.keys|	Nein
**Verzeichnis**|**Räume**
Datenstruktur|Raeume	
Mandant|Ja
Ansicht|	Klassen > Zeiträume > Klassenraum
*.keys|	Nein
**Verzeichnis**|**Religion (Teilnahmen)**
Datenstruktur|RelTeilnahmen	
Mandant|Nein
Ansicht|	Schüler > Daten1 > Rel.-Teilnahme<br/>Bewerber > Daten1 > Rel.-Teilnahme	
*.keys|Nein
**Verzeichnis**|**Religion (Wahlgründe)**
Datenstruktur|RelGruende
Mandant|	Nein	
Ansicht|Schüler > Daten1 > Rel.-Grund<br/>Bewerber > Daten1 > Rel.-Grund
*.keys|Nein
**Verzeichnis**|**Religion (Wünsche)**
Datenstruktur|*RelWuensche
Mandant|	Nein
Ansicht|	Schüler > Daten1 > Rel.-Wunsch<br/>Bewerber > Daten1 > Rel.-Wunsch
*.keys|Nein
**Verzeichnis**|**Schulenmerkmale**
Datenstruktur|SchulenMerkmale
Mandant|	Nein	
Ansicht|Schulen > Daten > Merkmal A1-A6	
*.keys|Nein
**Verzeichnis**|**Schülerarten**
Datenstruktur|SchuelerArten	
Mandant|Nein
Ansicht|	Schüler/Bewerber > Extras > Schülerart > Schülerart
*.keys|Nein
**Verzeichnis**|**Schularten**
Datenstruktur|Schularten
Mandant|Nein
Ansicht|Schüler > Laufbahn > Allgemein > Schulart<br/>Klassen > Daten > Schulart<br/>Lehrer > Daten2 > Schulart
*.keys|Ja
**Verzeichnis**|**Schularten (Herkunft)**
Datenstruktur|SchulartenHerkunft
Mandant|Nein	
Ansicht|Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulart<br/>Bewerber > Zugang > Bereits besuchte Schulen > Schulart<br/>Bewerber > Grundstufe > Laufbahn > Schulart<br/>Bewerber > SekI > Laufbahn > Schulart<br/>Bewerber > SekII > Laufbahn > Schulart<br/>Bewerber > Berufsbildung > Laufbahn > Schulart<br/>Schüler > Grundstufe > Laufbahn > Schulart<br/>Schüler > SekI > Laufbahn > Schulart<br/>Schüler > SekII > Laufbahn > Schulart<br/>Schüler > Berufsbildung > Laufbahn > Schulart	
*.keys|Ja
**Verzeichnis**|**Schülermerkmale**
Datenstruktur|SchuelerMerkmale
Mandant|Ja	
Ansicht|Schüler/Bewerber > Merkmale > Merkmale A1-A6<br/>Schüler/Bewerber > Statistik > Merkmale S1-S10
*.keys|Ja
**Verzeichnis**|**Schulformen**
Datenstruktur|Schulformen	
Mandant|Nein
Ansicht|	Klassen > Daten > Schulform<br/>Verzeichnisse > Bildungsgänge > Schulform	
*.keys|Ja
**Verzeichnis**|**Schulformen (Herkunft)**
Datenstruktur|SchulformenHerkunft
Mandant|	Nein	
Ansicht|Schüler > Zugang/Abgang > Bereits besuchte Schulen > Schulform<br/>Bewerber > Zugang > Bereits besuchte Schulen > Schulform<br/>Bewerber > Grundstufe > Laufbahn > Schulform<br/>Bewerber > SekI > Laufbahn > Schulform<br/>Bewerber > SekII > Laufbahn > Schulform<br/>Bewerber > Berufsbildung > Laufbahn > Schulform<br/>Schüler > Grundstufe > Laufbahn > Schulform<br/>Schüler > SekI > Laufbahn > Schulform<br/>Schüler > SekII > Laufbahn > Schulform<br/>Schüler > Berufsbildung > Laufbahn > Schulform
*.keys|Ja
**Verzeichnis**|**Schulformen (Übergang)**
Datenstruktur|SchulformenUebergang
Mandant|	Nein
Ansicht|	Schüler > Zugang/Abgang > Abgang > an Schulform
*.keys|	Ja
**Verzeichnis**|**Schulstati**<
Datenstruktur|Schulstati	
Mandant|Nein
Ansicht|Mandant > Daten1 > Schulstatus
*.keys|	Nein
**Verzeichnis**|**Schulstellen**
Datenstruktur|Schulstellen
Mandant|	Nein
Ansicht|	Klasse > Daten > Schulstelle	
*.keys|Nein
**Verzeichnis**|**Schulträger**
Datenstruktur|Schultraeger
Mandant|Nein
Ansicht|Mandant > Daten1 > Schulträger
*.keys|	Ja
**Verzeichnis**|**Schulzweige**
Datenstruktur|Schulzweige	
Mandant|Nein	
Ansicht|Lehrer > Daten2 > Schulzweig	
*.keys|Nein
**Verzeichnis**|**Schwerpunkte**
Datenstruktur|Schwerpunkte
Mandant|Nein	
Ansicht|Verzeichnis > Bildungsgänge > Schwerpunkt 1<br/>Verzeichnis > Bildungsgänge > Schwerpunkt 2	
*.keys|Nein
**Verzeichnis**|**Sportfeste**
Datenstruktur|Sportfeste
Mandant|	Ja
Ansicht|Sportfeste > Disziplinen und Ergebnisse > Sportfest	
*.keys|Nein
**Verzeichnis**|**Sprachgruppen**
Datenstruktur|Sprachgruppen
Mandant|Nein
Ansicht|Schüler/Bewerber > Daten2 > Sprachgruppe	
*.keys|Ja
**Verzeichnis**|**Sprachreferenzen**
Datenstruktur|Sprachreferenzen
Mandant|	Nein	
Ansicht|Schüler/Bewerber > Daten3 > Referenz	
*.keys|Ja
**Verzeichnis**|**Staatsangehörigkeiten**
Datenstruktur|Staatsangehoerigkeiten
Mandant|	Nein
Ansicht|	Schüler/Bewerber > Daten2 > Staatsangehörigkeit > Staatsangeh.1 und Staatsangeh.2<br/>Schüler/Bewerber > Daten1 > Geburtsland<br/>Schüler/Bewerber > Grundstufe > Geburtsland<br/>Schüler/Bewerber > Grundstufe > Staatsangeh.1 und Staatsangeh.2<br/>Schüler/Bewerber > SekI > Geburtsland<br/>Schüler/Bewerber > SekI > Staatsangeh.1 und Staatsangeh.2<br/>Schüler/Bewerber > SekII > Geburtsland<br/>Schüler/Bewerber > SekII > Staatsangeh.1 und Staatsangeh.2<br/>Schüler/Bewerber > Berufsbildung > Geburtsland<br/>Schüler/Bewerber > Berufsbildung > Staatsangeh.1 und Staatsangeh.2<br/>Lehrkraft > Daten1 > Staatsangeh.
*.keys|	Ja
**Verzeichnis**|**Typen**
Datenstruktur|ASVTypen	
Mandant|Nein	
Ansicht|Schüler > Zeugnis > Arbeits- und Sozialverhalten
*.keys|	Nein
**Verzeichnis**|**Übergangsarten**
Datenstruktur|Uebergangsarten
Mandant|Nein
Ansicht|Schüler > Zugang/Abgang > Abgang > Übergang
*.keys|Ja
**Verzeichnis**|**Umschulungsmerkmale**
Datenstruktur|Umschulungsmerkmale	
Mandant|Nein	
Ansicht|Schüler/Bewerber > Daten2 > Umschulung	
*.keys|Nein
**Verzeichnis**|**Unterrichtsarten**
Datenstruktur|Unterrichtsarten
Mandant|	Nein
Ansicht|Schüler > Zeugnis > Fächer > Unterrichtsarten<br/>Verzeichnisse > Fachtafeln > Fachtafelfächer > Unterrichtsart<br/>Abitur > Qualifikation > Unterrichtsart<br/>Berufsschule > Matrix > Unterrichtsart
*.keys|Ja
**Verzeichnis**|**Unterrichtsformen**
Datenstruktur|Unterrichtsformen
Mandant|Nein
Ansicht|	Klassen > Zeiträume > Zeitraum > Unterrichtsform
*.keys|	Nein
**Verzeichnis**|**Unterstützungen**
Datenstruktur|Unterstuetzungen
Mandant|Nein
Ansicht|	Schüler/Bewerber > Daten3 > Verschiedenes > Unterstützung	
*.keys|Nein
**Verzeichnis**|**Verkehrsmittel**
Datenstruktur|Verkehrsmittel
Mandant|	Nein	
Ansicht|Schüler/Bewerber > Daten4 > Beförderung > Verkehrsmittel
*.keys|Nein
**Verzeichnis**|**Verordnungen**
Datenstruktur|Verordnungen
Mandant|	Nein
Ansicht|Abitur > Prüfung > Prüfungsverordnung<br/>Abitur > Qualifikation > Prüfungsverordnung<br/>Berufsschule > Matrix > Verordnung<br/>Schüler > Zeugnis > Leistungen > Prüfungsordnung
*.keys|Nein
**Verzeichnis**|**Versetzungsarten**
Datenstruktur|Versetzungsarten
Mandant|	Nein
Ansicht|Schüler > Laufbahn > Allgemein > Versetzungsart
*.keys|Nein
**Verzeichnis**|**Versicherungsarten**
Datenstruktur|Versicherungsarten
Mandant|	Nein
Ansicht|	Schüler > Daten4 > Sonstige Daten > Versicherungart	
*.keys|Nein
**Verzeichnis**|**Vertragsarten**
Datenstruktur|Vertragsarten
Mandant|	Nein	
Ansicht|Schüler/Bewerber > Ausbildung > Vertragsart<br/>Schüler > Berufsbildung > Ausbildung/Praktikum > Vertragsart
*.keys|Nein
**Verzeichnis**|**Wettkämpfe**
Datenstruktur|Wettkaempfe	
Mandant|Ja
Ansicht|	Sportfeste > Disziplinen und Ergebnisse > Wettkämpfe
*.keys|	Nein
**Verzeichnis**|**Wiederholungsarten**
Datenstruktur|Wiederholungsarten
Mandant|Nein	
Ansicht|Schüler > Laufbahn > Allgemein > Wiederholungsart
*.keys|	Ja
**Verzeichnis**|**Wohnformen**
Datenstruktur|Wohnformen	
Mandant|Nein	
ansicht|Schüler/Bewerber > Daten1 > Wohnform	
*.keys|Nein
**Verzeichnis**|**Zeiträume**
Datenstruktur|Zeitraeume
Mandant|Nein
Ansicht|allgemein
*.keys|Nein
**Verzeichnis**|**Zeugnisbemerkungen**
Datenstruktur|Zeugnisbemerkungen
Mandant|Ja
Ansicht|Schüler > Zeugnis > Zeugnis > Zeugnisbemerkungen<br/>Abitur > Zeugnis > Zeugnisbemerkungen<br/>Berufsschule > Zeugnis > Zeugnisbemerkungen
*.keys|Nein
**Verzeichnis**|**Zeugnisbeurteilungen**
Datenstruktur|Zeugnisbeurteilungen
Mandant|Ja
Ansicht|Schüler > Zeugnis > Leistungen
*.keys|Nein
**Verzeichnis**|**Zeugnisformulare**
Datenstruktur|Zeugnisformulare
Mandant|Ja
Ansicht|Schüler > Zeugnis > Zeugnis > Zeugnisformulare
*.keys|Nein
**Verzeichnis**|**Zugangsarten (Lehrer)**
Datenstruktur|LehrerZugaenge
Mandant|	Nein
Ansicht|	Lehrkraft > Daten2 > Zugangsart
*.keys|	Ja







