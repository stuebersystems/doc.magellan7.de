# Kopfzeilen der *.keys

Jede dieser Dateien muss als CSV-Datei aufgebaut sein, d.h. sie besteht jeweils aus einer Kopfzeile und
ein oder mehreren Zeilen mit den zu importierenden Inhalten. Die einzelnen Felder sind durch
Semikolon getrennt und mit Anführungszeichen abgegrenzt.

Die Importdatei für Fachstatus (00_Fachstati.keys) kann z.B. folgenden Aufbau haben

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
"1PF";"1PF";"1. Prüfungsfach";"01.08.2006";""
"2PF";"2PF";"2. Prüfungsfach";"01.08.2006";""
"3PF";"3PF";"3. Prüfungsfach";"01.08.2006";""
"1PFBLL";"1PFBLL";"1. Prüfungsfach und Besondere Lernleistung";"01.08.2006";""
````

Die Felder entsprechen dem sog. System Data Format (SDF), d.h. bei einem Semikolon, Komma, Sonderzeichen oder einem Leerzeichen im String wird der String in Anführungszeichen gesetzt, z.B. dieBezeichnung "1. Prüfungsfach und Besondere Lernleistung " wird 
;“ 1. Prüfungsfach und Besondere Lernleistung“;... und nicht ; 1. Prüfungsfach und Besondere Lernleistung;... geschrieben.
Besitzt der Inhalt selbst Anführungszeichen, so sind doppelte Anführungszeichen anzugeben. Welche Felder pro Datei eingelesen werden, ist den nachfolgenden Abschnitten pro Datei zu entnehmen.

!!! info "Hinweis"

    Zeilenumbrüche sind in einer CSV-Datei nicht erlaubt. Das Datenformat bestimmt jede Zeile als einen Datensatz. Ein Umbruch mitten in der Zeile kann nicht verarbeitet werden.
Ändern Sie bitte vor dem Import die Dateiendung in *.keys.

Nachstehend finden Sie die Kopfzeilen der CSV-Dateien für den Import nach MAGELLAN.

Weitere Informationen finden Sie im Abschnitt [Administration > Importe und Exporte > Eigene oder mitgelieferte Schlüsselverzeichnisse importieren](https://doc.magellan.stueber.de/schulverwaltung/admin/datenaustausch/#eigene-kataloge-importieren-benutzer).

## Benennung der Kataloge

Beispiele:

* 00_Faecher.keys
* AS_Faecher.keys
* BS_Faecher.keys

Benennung                                     | Anmerkung
--------------------------------------------- | ---------
Dateinamenanfang "AS_"                        | Schlüsseldateien die mit "AS_" bezeichnet sind, werden beim Aufruf `für allgemeinbildende Schulen` zum Import angeboten
Dateinamenanfang "BS_"                        | Schlüsseldateien die mit "BS_" bezeichnet sind, werden beim Aufruf `für berufsbildende Schulen` zum Import angeboten
Dateinamenanfang "00_"                        | Schlüsseldateien die mit "00_" bezeichnet sind, werden beim Aufruf `für allgemeinbildende Schulen` und beim Aufruf `für berufsbildende Schulen` zum Import angeboten
Text ab Zeichen 4<br/>(im Beispiel "Faecher") | Anhand dieser Bezeichnung wird das Schlüsselverzeichnis identifiziert.

## Benennung und Aufbau der *.keys

### A

#### Abgangsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Abordnungsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Abschlussarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### AbschluesseExtern

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis";"Kategorie";"BedeutungVeraendert"
````

Feld | Inhalt
--------- | ------
Kategorie | 0 = Allgemeinbildender Abschluss<br/>1 = Berufsbildender Abschluss<br/>2 = Allgemeinbildender und Berufsbildender Abschluss

#### AbschluesseIntern

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis";"BedeutungVeraendert"
````

#### Abschlussjahrgaenge

````
"Kuerzel";"Bezeichnung";"Kategorie";"Von";"Bis"
````

Feld | Inhalt
--------- | ------
Kategorie | 0 = Abitur<br/>1 = Berufschule(Jahresnoten)<br/>2 = Berufsschule (Halbjahresnoten)
Von | TT.MM.JJJJ
Bis | TT.MM.JJJJ

#### Amtsbez

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Arbeitsaemter

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Aufnahmepruefungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### B

#### Behinderungsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Berufe

````
"Kuerzel";"Schluessel";"BezeichnungM";"BezeichnungW";"Fachrichtung";"Berufsfeld";"GueltigVon";"GueltigBis"
````
!!! info "Hinweis"

    Fachrichtung und Berufsfeld sind weitere Schlüsselverzeichnisse, die im gleichen Durchlauf oder vorher eingelesen werden müssen. Der Wert im Verzeichnis Berufe muss in diesen beiden Feldern das Kürzel aus den jeweiligen Unterverzeichnissen sein. Ein nachträgliches Zuweisen per Import ist nicht möglich.

#### Berufsfelder

````
Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Beschaeftigungsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Beschaeftigungsverh

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Besoldungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### BetreuungenAusserschulisch

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### BetreuungenInnerschulisch

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Betreuungsformen

````
Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Bevollmaechtigungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Bewerbungsempfehlungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Bewerbungsziele

````
Kuerzel;Schluessel;Bezeichnung;Bezeichnung2;GueltigVon;GueltigBis
````

#### Bildungsgaenge

````
"Kuerzel";"Schluessel";"Bezeichnung";"Bezeichnung2";"Berufsfeld";"Schulform";"Organisation";"Unterrichtsform";"Fachrichtung";"Schwerpunkt";"Klassenstufe";"GueltigVon";"GueltigBis"
````

!!! info "Hinweis"

    Die Felder `Fachrichtung`, `Berufsfeld`, `Schulform`, `Organisation`, `Unterrichtsform`, `Klassenstufe` und `Schwerpunkt` sind weitere Schlüsselverzeichnisse, die im gleichen Durchlauf (wenn sie importierbar sind) oder vorher eingelesen/angelegt werden müssen. Der Wert im Verzeichnis Bildungsgaenge muss als Kürzel in dem Verzeichnis existieren. Ein nachträgliches Zuweisen per Import ist nicht möglich.

#### Branchen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### D

#### Dienstbez

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Dienstherren

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Dienstverh

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Disziplinen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### E 

#### Einschulmerkmale

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Empfehlungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Entscheidungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### F

#### Faecher

````
"Kuerzel";"Schluessel";"Bezeichnung";"Kategorie";"Aufgabenbereich";"Gruppe";"GueltigVon";"GueltigBis"
````

Eintrag|Kategorie
---|---
0 | Fremdsprache
1 | Religion/Ethik
2 | Deutsch
3 | Mathematik
4 | Kunst
5 | Musik
6 | Sport
9 | Informatik
10 | Philosophie
11 | Geschichte
12 | Physik
13 | Chemie
14 | Biologie
15 | Erdkunde
16 | Sozialkunde
17 | Wirtschaft
18 | Politik
19 | Darstellendes Spiel
20 | Evangelische Religion
21 | Katholische Religion
26 | Technik
27 | Pädagogik
28 | Sport-Theorie
29 | BWL/RW
30 | BWL/VWL
31 | VWL
32 | Seminar
33 | Gesundheit
34 | Psychologie
35 | Recht

Wert|Aufgabenbereich
---|---
0 | sprachl.-lit.-künstlerisch
1 | gesellschaftswiss.
2 | mathem.-nat.-technisch
3 | Religion
4 | Sport

!!! info "Hinweis"

    Gruppe: Die Fachgruppe (hier Gruppe) ist ein weiteres Schlüsselverzeichnis, das im gleichen Durchlauf oder vorher eingelesen werden muss. Der Wert im Verzeichnis Faecher muss in diesem Feld dem Kürzel aus dem Verzeichnis Fachgruppe entsprechen. Ein nachträgliches Zuweisen per Import ist nicht möglich.

#### Fachgruppen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Fachniveaus

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Fachrichtungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Fachschwerpunkte

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Fachstati

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Fahrkarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Foerderungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### H

#### Haertefaelle

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Herkunftsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis";"BedeutungVeraendert"
````

#### Herkunftsunterlagen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis";"BedeutungVeraendert"
````

### I

#### Integrationsmerkmale

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis";"BedeutungVeraendert"
````

### K

#### Kammern

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Klassenmerkmale

````
"Kuerzel";"Schluessel";"Bezeichnung";"Bereich";"GueltigVon";"GueltigBis"
````

Bereichswert|Für Feld
---|---
0 | Merkmal A1
1 | Merkmal A2
2 |Merkmal A3
3 | Merkmal A4
4 | Merkmal A5
5 | Merkmal A6
6 | Merkmal S1
7 | Merkmal S2
8 | Merkmal S3
9 | Merkmal S4

#### Klassenorganisationen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Klassenstufen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Konfessionen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### L

#### Lehraemter

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### LehrerFehlgruende

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### LehrerAusbildung

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### LehrerAusbildungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### LehrerFunktionen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### LehrerAbgaenge

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### LehrerPruefungsbezuege

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Lehrermerkmale

````
"Mandant";"Bereich";"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

Bereichswert|für Feld
---|---
0 | Merkmal A1
1 | Merkmal A2
2 | Merkmal A3
3 | Merkmal A4
4 | Merkmal A5
5 | Merkmal A6
6 | Merkmal S1
7 | Merkmal S2
8 | Merkmal S3
9 | Merkmal S4

#### LehrerZugaenge

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### M

#### MandantenMerkmale

````
"Mandant";"Bereich";"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

Bereichswert|für Feld
---|---
0 | Merkmal A1
1 | Merkmal A2
2 | Merkmal A3
3 | Merkmal A4
4 | Merkmal A5
5 | Merkmal A6

#### Muttersprachen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### N

#### Nachpruefungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Noten

````
"Notenkuerzel";"Notenwert";"Notenart";"Bezeichnung";"AlternativBez";"GueltigVon";"GueltigBis"
````
Eintrag|Notenart
---|---
0 | Notenwert
1 | Punktwert
2 | Füllwert

### O

#### Organisationen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### Q

#### Qualifikationsniveaus

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### R

#### Raeume

````
"Kuerzel";"Schluessel";"Bezeichnung“
````

#### RelTeilnahmen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### RelGruende

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### RelWuensche

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### S

#### SchuelerFunktionen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SopaedFoerderungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SchuelerProfile

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SorgebeFunktionen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SchulenMerkmale

````
"Mandant";"Bereich";"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

Bereichswert|für Feld
---|---
0 | Merkmal A1
1 | Merkmal A2
2 | Merkmal A3
3 | Merkmal A4
4 | Merkmal A5
5 | Merkmal A6

#### SchuelerArten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Schularten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SchulartenHerkunft

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SchuelerMerkmale

````
"Mandant";"Bereich";"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

Bereichswert|für Feld
---|---
0 | Merkmal A1
1 | Merkmal A2
2 | Merkmal A3
3 | Merkmal A4
4 | Merkmal A5
5 | Merkmal A6
6 | Merkmal S1
7 | Merkmal S2
8 | Merkmal S3
9 | Merkmal S4
10 | Merkmal S5
11 | Merkmal S6
12 | Merkmal S7
13 | Merkmal S8
14 | Merkmal S9
15 | Merkmal S10

#### Schulformen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SchulformenHerkunft

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### SchulformenUebergang

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Schulstati

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Schulstellen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Schultraeger

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Schulzweige

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Schwerpunkte

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Sprachgruppen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Sprachreferenzen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Staatsangehoerigkeiten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### U

#### Uebergangsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Umschulungsmerkmale

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### Unterrichtsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Unterrichtsformen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Unterstuetzungen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### V

#### Verkehrsmittel

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Versetzungsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Versicherungsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Vertragsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

### W

#### Wiederholungsarten

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````

#### Wohnformen

````
"Kuerzel";"Schluessel";"Bezeichnung";"GueltigVon";"GueltigBis"
````
