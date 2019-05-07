# Datenpflege in MAGELLAN 6

Um die SAXSVS.xml sinnvoll füllen zu können, müssen die korrekten Schlüssel in der Datenbank den verwendeten Datensätzen zugewiesen worden sein (vorheriger Abschnitt) und die Felder, die die Schnittstelle abfragt, in MAGELLAN auch gefüllt sein. 
Die nachstehenden Schritte zeigen die Felder auf, die Sie befüllen müssen.


Nachstehend finden Sie eine Auflistung der relevanten Felder und der jeweiligen Stelle, an der Sie in MAGELLAN eingepflegt werden.
Ggf. haben wir nach XML-Elementen aufgeteilt.

> #### danger::Achtung
>
> Möchten Sie Schüler von der Statistik ausschließen, z.B. weil sie statistisch
> an einer anderen Schule geführt werden, dann müssen Sie den Schüler als ***Gastschüler*** markieren.
> Dazu setzen Sie in MAGELLAN unter `Schüler > Daten 3 > Verschiedenes > Gastschüler` den Haken.


### Kopfbereich ( saxsvs-bbs )
```xml
<saxsvs-bbs xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xsi:noNamespaceSchemaLocation="https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.2.xsd" 
  zeit="TDateTime Today (2001-12-17T09:30:47-05:00)" 
  schuljahr="Zeitraeume.Von (2017/2018)" 
  dienststelle="Mandanten.Schulnummer">
```

Titel|Inhalt
---|---
**Statistikfeld**| **... > saxsvs-bbs > zeit **
Beschreibung| Für dieses Feld wird automatisch ein aktueller Datums-/Zeitstempel eingefügt.
**Statistikfeld**| **... > saxsvs-bbs > schuljahr** 
Beschreibung|`MAGELLAN > Verzeichnisse > Zeitraeume > Von`<br/> Aus dem Eintrag wird der geforderte Wert im Format **JJJJ/JJJJ** gebildet, als Beispiel: 2018/2019
**Statistikfeld**| **... > saxsvs-bbs > dienststelle** 
Beschreibung|`MAGELLAN > Schulnummer` 

    
### Schüler ( saxsvs-bbs > schueler )

#### Ausbildung

Ohne Angaben zur Ausbildung beim Schüler wird der Schüler nicht in die XML-Datei gespielt und Sie erhalten eine entsprechenden Hinweis beim Durchlauf.
Alle folgenden Felder der Ausbildung **müssen** gepflegt sein, sind damit **Pflichtfelder**.

Titel|Inhalt
---|---
**Statistikfeld**| ** saxsvs-bbs > schueler > extern_id** 
Beschreibung|`Schüler > Ausbildung > GUID`  <br/><br/> 1. Wenn Sie aktuell MAGELLAN 6 nutzen und zum ersten mal in MAGELLAN 7 den Export durchlaufen, dann existieren noch keine GUIDs.<br/> Diese werden dann für bestehende aktuelle Ausbildungen angelegt und in der Datenbank gespeichert.<br/> 2. Schüler ohne eine aktuelle Ausbildung im ausgewählten Exportzeitraum werden <b>nicht berücksichtigt</b>. Berufsschülern muss auf der Ausbildungskarte in MAGELLAN 6 ein Bildungsgang zugewiesen werden (Schüler > Bearbeiten > Sammelzuweisung), Oberstufenschüler wird nach der Datenübernahme nach MAGELLAN 7 per Sammelzuweisung die Schulform zugewiesen. 
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_kennziffer** 
Beschreibung| `MAGELLAN > Schüler > Ausbildung > Bildungsgang [BS_Bildungsgaenge]`<br/>**Hinweis:** Auch Oberstufenschüler benötigen einen Bildungsgang, lesen Sie [Berufliches Gymnasium - Oberstufenschüler]().
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_schulart** 
Beschreibung| `MAGELLAN > Schüler > Ausbildung > Schulform [BS_Schulformen]`<br/>Nur in MAGELLAN 7<br/>. Bitte lesen Sie ["Datenpflege in MAGELLAN 7"](https://doc.magellan7.stueber.de/regionales/sachsen/datenpflege7.html)
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_zeitform** 
Beschreibung| `MAGELLAN > Schüler > Ausbildung > Organisation [BS_Organisationen]`<br/>Nur in MAGELLAN 7<br/>Bitte lesen Sie den Abschnitt ["Ausbildung in MAGELLAN 6 und MAGELLAN 7"](https://doc.magellan7.stueber.de/regionales/sachsen/datenpflege7.html#ausbildung-in-magellan-6-und-magellan-7)


#### Förderbedarf

 Ab MAGELLAN 7 sind mehrere Einträge für Förderungen möglich (Stichwort: Liste der Förderungen). <br/>
 Bitte lesen zum Förderbedarf auch den Abschnitt ["Förderbedarf in MAGELLAN 6 und MAGELLAN 7"](https://doc.magellan7.stueber.de/regionales/sachsen/datenpflege7.html#f%C3%B6rderbedarf-in-magellan-6-und-magellan-7)

Titel|Inhalt
---|--- 
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderungen > af_int > schluessel** 
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Maßnahme/Bedarf [BS_SopaedFoerderungen]`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderungen > af_int > extern_id** 
Beschreibung| `Wert (S1060) wird von MAGELLAN automatisch eingetragen.`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_von**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Von`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_bis**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Bis`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_rs_std**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Stunden 1`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_fs_std**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Stunden 2`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_foerdersw > schluessel**
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Förderschwerpunkt 1`
**Statistikfeld**| **... > saxsvs-bbs > schueler > foerderung > af_int_foerdersw > extern_id**
Beschreibung| `Wert (S1075) wird von MAGELLAN automatisch eingetragen.`
**Statistikfeld**| **... > saxsvs-bbs > schueler > migration > an_migr_daz** 
Beschreibung| `MAGELLAN > Schüler > Daten 4 > Förderungen > Maßnahme/Bedarf` <br/> Eines der Listeneinträge in MAGELLAN 7 muss im Feld den Wert DAZ-3 haben, um dieses spezielle Migrationsfeld in der Statistik auszugeben.


#### Allgemeines

Titel|Inhalt
---|---
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_vname** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Vorname`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_name** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Nachname`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_gebname**
Beschreibung|  `MAGELLAN > Schüler > Daten 1 > Geburtsname`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_gebdat**
Beschreibung|  `MAGELLAN > Schüler > Daten 1 > Geburtsdatum`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_gebort**
Beschreibung|  `MAGELLAN > Schüler > Daten 1 > Geburtsort`
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_geschlecht > schluessel** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Geschlecht`<br/> Notwendiger Eintrag wird aus der Eingabe berechnet.
**Statistikfeld**| **... > saxsvs-bbs > schueler > an_geschlecht > extern_id** 
Beschreibung| `MAGELLAN > Schüler > Daten 1 > Geschlecht`<br/> Notwendiger Eintrag wird aus der Eingabe berechnet.
**Statistikfeld**| **... > saxsvs-bbs > schueler > migration > an_migr_grund** 
Beschreibung| `MAGELLAN > Schüler > Daten 2 > NDH`<br/> Wenn Migrationshintergrund besteht den Haken bitte aktivieren.
**Statistikfeld**| **... > saxsvs-bbs > schueler > migration > an_migr_dat** 
Beschreibung| `MAGELLAN > Schüler > Statistik > MerkmalU2`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_status** 
Beschreibung| `MAGELLAN > Schüler > Statistik > Merkmal S1 [BS_SchuelerMerkmale]`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_abschl_dat** 
Beschreibung| `MAGELLAN > Schüler > Zugang / Abgang > Voraus. Ende`
**Statistikfeld**| **... > saxsvs-bbs > schueler > al_laufb_kl** 
Beschreibung| `MAGELLAN > Schüler > Auswahl > Klasse`<br />MAGELLAN übernimmt automatisch die Klasse in dem der Schüler eingeschult ist.


## Berufliches Gymnasium - Oberstufenschüler

Auch Schüler des beruflichen Gymnasiums müssen einen Bildungsgang zugewiesen bekommen. Diesen können Sie auch über die Sammelzuweisung vergeben.
Folgende Bildungsgänge sind für BGY gedacht:

Kennziffer|Bildungsgang|Schulart|Zeitform
---|---|---|---
83000002| Ernährungswissenschaft|	BGY| v
82000003| Gesundheit und Sozialwesen| BGY| v
43000001| Informations- und Kommunikationstechnologie| 	BGY|	v
43000002| Technikwissenschaft| BGY|	v
32000001| Technikwissenschaft/Bautechnik|	BGY| v
43000003| Technikwissenschaft/Datenverarbeitungstechnik| BGY|	v
26000001| Technikwissenschaft/Elektrotechnik|	BGY|	v
25000001| Technikwissenschaft/Maschinenbautechnik| BGY|	v
71000002| Wirtschaftswissenschaft| BGY|	v