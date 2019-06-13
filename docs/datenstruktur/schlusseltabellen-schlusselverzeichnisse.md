#	Katalog der Schlüsseltabellen (Schlüsselverzeichnisse)

Schlüsseltabellen sind Tabellen die überwiegend dazu genutzt werden Listen von Stammdaten zu halten, um diese kontextbezogen anzuzeigen und einzugeben und in diesem Kontext in der Datenbank festzuhalten. Während die Schlüsseltabellen selbst nur die Liste dieser Daten halten, werden die Primärfelder (meistens das Feld „Kürzel“) in der entsprechenden Kontexttabelle mit dem Verweis auf die Schlüsseltabelle gespeichert. 

Am Beispiel der Tabelle „Staatsangehoerigkeiten“. Diese wird kontextbezogen in den Tabellen „Schüler“ und „Lehrer“ und „Sorgeberechtigte“ gespeichert.
Bei den Schülern und Lehrern in den entsprechenden Feldern für die Staatsangehörigkeit, bei den Sorgeberechtigten im Feld für das Geburtsland.
Einige dieser Schlüsseltabellen sind speziell für Statistiken wichtig, deshalb halten diese die Felder „Schluessel“. Diese speziellen Tabellen benennen wir auch als „Schlüsselverzeichnisse“.

## Tabellenname und Name in der MAGELLAN-Oberfläche


| Tabelle                    | Oberflächenbezeichnung            |
|----------------------------|-----------------------------------|
| ASVArten                   | Arten (ASV)                       |
| ASVBewertungen             | Bewertungen (ASV)                 |
| ASVInhaltetafelInhalte     | Inhaltetafel-Inhalte (ASV)        |
| ASVInhaltetafeln           | Inhaltetafeln (ASV)               |
| ASVKategoriegruppen        | Kategoriegruppen (ASV)            |
| ASVKategorien              | Kategorien (ASV)                  |
| ASVTafelKategorien         | Tafelkategorien (ASV)             |
| ASVTafeln                  | Tafeln (ASV)                      |
| ASVTypen                   | Typen (ASV)                       |
| Abgangsarten               | Abgangsarten (Schüler)            |
| Abordnungsarten            | Abordnungsarten                   |
| AbschluesseExtern          | Abschlüsse (Extern)               |
| AbschluesseIntern          | Abschlüsse (Intern)               |
| Abschlussarten             | Abschlussarten                    |
| Abschlussjahrgaenge        | Abschlussjahrgänge                |
| Abteilungen                | Abteilungen                       |
| Adressenkategorien         | Kategorien (Adressen)             |
| Amtsbez                    | Amtsbezeichnungen                 |
| Arbeitsaemter              | Arbeitsämter                      |
| AssessmentEntries          | Bewertungseinträge                |
| AssessmentGroups           | Bewertungsgruppen                 |
| AssessmentProfiles         | Bewertungsprofile                 |
| Aufnahmepruefungen         | Aufnahmeprüfungen                 |
| Banken                     | Banken                            |
| Behinderungsarten          | Behinderungsarten                 |
| Berufe                     | Berufe                            |
| Berufsfelder               | Berufsfelder                      |
| Beschaeftigungsarten       | Beschäftigungsarten               |
| Beschaeftigungsverh        | Beschäftigungsverhältnisse        |
| Besoldungen                | Besoldungen                       |
| Besonderheiten             | Besonderheiten                    |
| BetreuungenAusserschulisch | Betreuungen (außerschulisch)      |
| BetreuungenInnerschulisch  | Betreuungen (innererschulisch)    |
| Betreuungsformen           | Betreuungsformen                  |
| Bevollmaechtigungen        | Bevollmächtigungen                |
| Bewerbungsempfehlungen     | Bewerbungsempfehlungen            |
| Bewerbungsziele            | Bewerbungsziele                   |
| Bezirke                    | Bezirke                           |
| Bildungsgaenge             | Bildungsgänge                     |
| Branchen                   | Branchen                          |
| Buchungsbereiche           | Buchungsbereiche                  |
| Bundeslaender              | Bundesländer                      |
| Dienstbez                  | Dienstbezeichnungen               |
| Dienstherren               | Dienstherren                      |
| Dienstverh                 | Dienstverhältnisse                |
| Disziplinen                | Disziplinen                       |
| Einschulmerkmale           | Einschulmerkmale                  |
| Empfehlungen               | Empfehlungen                      |
| Entscheidungen             | Entscheidungen                    |
| Erscheinungsweisen         | Erscheinungsweisen                |
| FachNiveaus                | Fachniveaus                       |
| Fachgruppen                | Fachgruppen                       |
| Fachrichtungen             | Fachrichtungen                    |
| Fachschwerpunkte           | Fachschwerpunkte                  |
| Fachstati                  | Fachstatus                        |
| FachtafelFaecher           | Fachtafel - Fächer                |
| Fachtafeln                 | Fachtafeln                        |
| Faecher                    | Fächer                            |
| FaecherThemen              | Fächer (Themen)                   |
| FaecherUnterpunkte         | Fächer (Unterpunkte)              |
| Fahrkarten                 | Fahrkarten                        |
| FoerderSchwerpunkte        | Förderschwerpunkte                |
| Foerderungen               | Förderungen                       |
| Gemeinden                  | Gemeinden                         |
| GradeEntries               | Notensystemeinträge               |
| GradeSystems               | Notensysteme                      |
| GradeTypes                 | ?                                 |
| Haertefaelle               | Härtefälle                        |
| Herkunftsarten             | Herkunftsarten                    |
| Herkunftsunterlagen        | Herkunftsunterlagen               |
| Integrationsmerkmale       | Integrationsmerkmale              |
| InventarKategorien         | Kategorien (Inventar)             |
| Kammern                    | Kammern                           |
| KlassenMerkmale            | Merkmale (Klassen)                |
| Klassenorganisationen      | Klassenorganisationen             |
| Klassenstufen              | Klassenstufen                     |
| Konfessionen               | Konfessionen                      |
| Krankenkassen              | Krankenkassen                     |
| Kreise                     | Kreise                            |
| Kurssprachen               | Kurssprachen                      |
| Lehraemter                 | Lehrämter                         |
| LehrerAbgaenge             | Abgangsarten (Lehrer)             |
| LehrerAusbildung           | Ausbildung (Lehrer)               |
| LehrerFehlgruende          | Fehlgründe (Lehrer)               |
| LehrerFunktionen           | Funktionen (Lehrer)               |
| LehrerMerkmale             | Merkmale (Lehrer)                 |
| LehrerPruefungsbezuege     | Prüfungsbezüge (Lehrer)           |
| LehrerSollSchluessel       | Lehrer-Soll-Schlüssel             |
| LehrerZugaenge             | Zugangsarten (Lehrer)             |
| Lehrerkategorien           | Kategorien (Lehrer)               |
| MandantenMerkmale          | Merkmale (Mandanten)              |
| Mandantenkategorien        | Kategorien (Mandanten)            |
| MedienKategorien           | Kategorie (Medien)                |
| MedienZustaende            | Medienzustände                    |
| Medienarten                | Medienarten                       |
| Medienformate              | Medienformate                     |
| MedizinArten               | Medizinarten                      |
| MedizinKategorien          | Kategorien (Medizin)              |
| Muttersprachen             | Muttersprachen                    |
| Nachpruefungen             | Nachprüfungen                     |
| Nachteilsausgleiche        | Nachteilsausgleiche               |
| Noten                      | Noten                             |
| Organisationen             | Organisationen                    |
| Personenkategorien         | Kategorien (Personen)             |
| Postleitzahlen             | Postleitzahlen                    |
| Qualifikationsniveaus      | Qualifikationsniveaus             |
| Raeume                     | Räume                             |
| RegionTypes                | Gebietsarten                      |
| Regions                    | Gebiete                           |
| RelGruende                 | Religion (Wahlgründe)             |
| RelTeilnahmen              | Religion (Teilnahmen)             |
| RelWuensche                | Religion (Wünsche)                |
| Schlagworte                | Schlagworte                       |
| SchuelerArten              | Schülerarten                      |
| SchuelerFehlgruende        | Fehlgründe (Schüler)              |
| SchuelerFunktionen         | Funktionen (Schüler)              |
| SchuelerMerkmale           | Merkmale (Schüler)                |
| SchuelerProfile            | Profile (Schüler)                 |
| Schularten                 | Schularten                        |
| SchulartenHerkunft         | Schularten (Herkunft)             |
| SchulenMerkmale            | Merkmale (Schulen)                |
| Schulformen                | Schulformen                       |
| SchulformenHerkunft        | Schulformen (Herkunft)            |
| SchulformenUebergang       | Schulformen (Übergang)            |
| Schulgeldarten             | Schulgeldarten                    |
| Schulstati                 | Schulstati                        |
| Schulstellen               | Schulstellen                      |
| Schultraeger               | Schulträger                       |
| Schulzweige                | Schulzweige                       |
| Schwerpunkte               | Schwerpunkte                      |
| SopaedFoerderungen         | Förderbedarf                      |
| SorgebeFunktionen          | Funktionen (Sorgeberechtigte)     |
| Sponsoren                  | Sponsoren                         |
| Sportfeste                 | Sportfeste                        |
| Sprachen                   | Sprachen                          |
| Sprachgruppen              | Sprachgruppen                     |
| Sprachreferenzen           | Sprachreferenzen                  |
| Staaten                    | Staaten                           |
| Staatsangehoerigkeiten     | Staatsangehörigkeiten             |
| Stadtbezirke               | Stadtbezirke                      |
| TransportationLines        | Verkehrslinien                    |
| TransportationMethods      | Verkehrsmittel (Transportmethode) |
| TransportationRoutes       | Fahrtstrecken                     |
| TransportationStops        | Haltestellen                      |
| Uebergangsarten            | Übergangsarten                    |
| Umschulungsmerkmale        | Umschulungsmerkmale               |
| Unterrichtsarten           | Unterrichtsarten                  |
| Unterrichtsformen          | Unterrichtsformen                 |
| Unterstuetzungen           | Unterstuetzungen                  |
| Verkehrsmittel             | Verkehrsmittel                    |
| Verordnungen               | Verordnungen                      |
| Versetzungsarten           | Versetzungsarten                  |
| Versicherungsarten         | Versicherungsarten                |
| Vertragsarten              | Vertragsarten                     |
| Waehrungen                 | Währungen                         |
| Wettkaempfe                | Wettkämpfe                        |
| WettkampfDisziplinen       | Wettkampf - Disziplinen           |
| Wiederholungsarten         | Wiederholungsarten                |
| Wohnformen                 | Wohnformen                        |
| Zeitraeume                 | Zeiträume                         |
| Zeugnisbemerkungen         | Zeugnisbemerkungen                |
| Zeugnisbeurteilungen       | Beurteilungen (Zeugnis)           |
| Zeugnisformulare           | Zeugnisformulare                  |


