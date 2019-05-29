# Erzeugen der Datei SAXSVS.xml

Die Schnittstelle exportiert eine Datei im XML-Format. Dies bedeutet Sie erhalten eine strukturierte Textdatei nach vorgegebenem Format. 
Allgemeine Informationen zum grundsätzlichen Verständnis von XML-Dateien finden Sie auf z.B. auf [Wikipedia](https://de.wikipedia.org/wiki/Extensible_Markup_Language).

Hier ein kleiner Ausschnitt aus der SaxSVS-Schnittstelle:

```xml
<saxsvs-bbs xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.3.xsd" zeit="TDateTime Today (2001-12-17T09:30:47-05:00)" schuljahr="Zeitraeume.Ausdruck2 (2018/2019)" dienststelle="Mandanten.Schulnummer">
	<schueler extern_id="Schueler.ID">
		<an_vname>Schueler.Vorname</an_vname>
		<an_name>Schueler.Nachname</an_name>
		<an_gebdat>Schueler.Geburtsdatum (YYYY-MM-DD)</an_gebdat>
		<an_gebort>x</an_gebort>
		<an_geschlecht schluessel="K101" extern_id="1">männl.</an_geschlecht>
		<al_kennziffer>SchuelerAusbildung.Bildungsgang</al_kennziffer>
		<al_schulart schluessel="S0502" extern_id="110">BS/BS</al_schulart>
		<al_status schluessel="S1920" extern_id="1">Auszubildender/Schüler</al_status>
		<al_zeitform schluessel="S1832" extern_id="1">v</al_zeitform>
		<al_abschl_dat>Schueler.VoraussichtlichesEnde (2016-01-01)</al_abschl_dat>
		<al_laufb_kl>SchuelerLaufbahn.Klasse (BK19A)</al_laufb_kl>
	</schueler>
</saxsvs-bbs>
```

### XML-Dateien prüfen

Ein Vorteil von XML-Dateien ist, dass diese über eine weitere Datei, genannt Schemadatei (Dateiformat .XSD) geprüft werden kann. Das Schema gibt vor, wie eine XML-Datei auszusehen hat und z.B. welche Werte grundsätzlich erlaubt sind.
Die Schemadatei für die SAXSVS-Schnittstelle finden Sie [hier](https://web1.extranet.sachsen.de/bbsp/public/XMLSchema/saxsvs-bbs-2.3.xsd).
Um die fertige XML-Datei mit der Schemadatei prüfen zu können, benötigen Sie ein entsprechendes Programm, z.B. XML-Spy oder ähnliches. Es gibt auch Online-Prüfungen, in denen Sie den Text der XML-Datei kopieren können und den Link zur Prüfdatei im Netz angeben (**Achten Sie auf den Datenschutz bei Prüfungen im Internet**). Die Prüfungen geben üblicherweise recht gute Fehlerbeschreibungen aus, wenn etwas in der XML-Datei nicht stimmt. STÜBER SYSTEMS hat auch eine einfache automatische Prüfung eingebaut, die über den MSXML-Parser angeboten wird. Die Ausgaben der Fehlerbeschreibungen sind allerdings von Hause aus etwas kryptisch und können nur einen Anhaltspunkt geben.


## Statistikdaten erstellen

Für die Erstellung der Exportdatei rufen Sie bitte aus dem Menü `Schüler` den Reiter `Extras` auf und wählen den Unterpunkt `Export`. <br/><br/>
![Daten aus MAGELLAN exportieren über `Schüler > Export > Export...`](/assets/images/sachsen/export.saxsvs01.png)

Es startet der Exportassistent, bitte wählen Sie die Schnittstelle `SAX-SVS (BBS)` und fügen über das Plus den gewünschten Exportzeitraum hinzu. Klicken Sie auf `Weiter`! <br/><br/>
![Wählen Sie die Schnittstelle und den Zeitraum aus!](/assets/images/sachsen/export.saxsvs02.png)

Auf der Folgekarte wählen Sie einen Speicherort (Exportordner) und klicken auf `Weiter`!<br/><br/>
![Bitte wählen Sie einen Speicherort!](/assets/images/sachsen/export.saxsvs04.png)

Starten Sie die Erstellung der Exportdatei oder die Prüfung per Klick auf `Fertigstellen`! <br/><br/>
![Starten Sie die Erstellung!](/assets/images/sachsen/export.saxsvs05.png)


## Probleme?

Sollte Ihnen in der Auswahl im Exportassistenten nicht der Punkt `SAXSVS` gezeigt werden, ist vermutlich im Willkommensassistenten nicht die Bundeslandauswahl "Sachsen" getroffen worden. 

**So geht's**

1. Schließen Sie bitte MAGELLAN und starten Sie bitte den MAGELLAN ADMINISTRATOR und wechseln in den Menüpunkt `Datenbankverbindungen`. 
2. Klicken Sie doppelt auf Ihre Verbindungszeile, es öffnet sich das Fenster `Verbindungsdetails`.
3. Rufen Sie den Punkt `Datenbank` auf und tragen im Feld `Region` "Sachsen" ein. <br/>Im Anschluss starten Sie MAGELLAN wieder, unter `Extras > Export > Export...` sollte jetzt auch die Auswahl `SAXSVS` zur Verfügung stehen!