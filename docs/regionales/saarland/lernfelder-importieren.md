# Saarland: Lernfelder importieren

Das Saarländische Ministerium stellt ein Liste von Lernfeldern für die Beruflichen Schulen zur Verfügung, die ab der Version 6.0.177 in das Verzeichnis Fächer in MAGELLAN importiert werden kann.

Die Datei enthält eine vollständige Liste der aktuell möglichen Lernfelder. Diese Lernfelder werden in das Verzeichnis Fächer importiert und enthalten die Werte Kürzel, Bezeichnung und das Merkmal  (Zeugnismerkmal aus ```Verzeichnisse > Fächer > Merkmal```), das von den zur Verfügung stehenden Zeugnisberichten  ausgewertet wird.
 
> #### warning::Wichtig!
>
> Wir empfehlen diese Datei nicht vollständig zu importieren, sondern vor dem Import auf die Zeilen zu reduzieren, die an Ihrer Schule benötigt werden. 
 
Die Datei ist nicht direkt im Verzeichnis `Importe > Saarland` zu finden, sondern im Unterordner `Lernfelder`, damit nicht versehentlich die gesamte Fächerliste in die Datenbank eingelesen wird. Bitte kürzen Sie die Datei in einem Texteditor, speichern sie und legen sie dann direkt unter `Importe > Saarland` ab.  Anschließend importieren Sie die Datei wie gewohnt über den MAGELLAN-ADMINISTRATOR Unterpunkt `Datenimport > Schlüsselverzeichnisse importieren > Saarland`.

> #### warning::Wichtig!
>
> Beim Import werden aus Ihrem Verzeichnis Fächer alle bisher nicht verwendeten Fächer entfernt und die neuen Fächer mit eingefügt. Gefüllt werden die Felder Kürzel, Bezeichnung und Merkmal. Im Merkmal wird zum Beispiel der Wert LF1 eingetragen. An diesem Wert erkennen die entsprechend vorbereiteten Zeugnisberichte das Lernfeld 1. 

Folgende Berichte arbeiten mit diesen Werten (Berichte > Zeugnisse > Saarland > Ministerium):

* SAR-BS-AS-Lernfeld A3 MBK.rpt (erstellt vom Ministerium für Bildung und Kultur Saarland)
* SAR-BS-HJZ-Lernfeld MBK.rpt (erstellt vom Ministerium für Bildung und Kultur Saarland)
* SAR-Klassen-Notenliste Abgeschlossene Lernfelder MBK.rpt (erstellt vom Ministerium für Bildung und Kultur Saarland)

## BS_Faecher.keys bearbeiten

Die Datei BS_Faecher.keys befindet sich bei Standardinstallationen auf Ihrem Serverrechner unter:

`C:\Users\Public\Documents\Stueber Systems\Magellan 6\Skripte\Saarland\Lernfelder`

Öffnen Sie einen Editor (Windows Texteditor)und aus dem Programm heraus die Importdatei. 

![Wählen Sie "Alle Dateien" um die BS_Faecher.keys gezeigt zu bekommen](/images/keys_editieren.png)

Achten Sie darauf, dass unten rechts im Öffnendialog die Auswahl auf "Alle Dateien (*.*)" steht, um auch die Datei mit der Endung *.keys zu sehen.

![Inhalt der Datei](/images/keys.png)

Löschen Sie bitte die Zeilen, die an Ihrer Schule nicht benötigt werden oder kopieren Sie (dann bitte auch die Kopfzeile) die benötigten Zeilen in eine neue Textdatei. 

> #### warning::Wichtig!
>
>  Die Lernfelder pro Ausbildungsberuf erkennen Sie am Kürzel. Sie finden eine Kürzel-Beruf-Legende im Abschnitt [**Abkürzungsverzeichnis der Berufe**](../abkurzungsverzeichnis_berufe.md).

Achten Sie darauf, dass die Struktur nicht durch Leerzeilen oder ähnliches verändert wird. Speichern Sie das Ergebnis und legen die Datei an folgender Stelle ab:

`C:\Users\Public\Documents\Stueber Systems\Magellan 6\Skripte\Saarland`

## BS_Faecher.keys importieren

Für den Import öffnen Sie bitte das Modul MAGELLAN ADMINISTRATOR und wählen den Punkt ```Datenimporte```.

Wählen Sie bitte die nachfolgenden Einstellungen um gezielt das bearbeitete Verzeichnis einzulesen. 


![Importdialog](/images/keys_importieren.png)


> #### warning::Wichtig!
>
> Beim Import werden aus Ihrem Verzeichnis Fächer alle bisher nicht verwendeten Fächer entfernt und die neuen Fächer mit eingefügt. Gefüllt werden die Felder Kürzel, Bezeichnung und Merkmal. Im Merkmal wird zum Beispiel der Wert LF1 eingetragen. An diesem Wert erkennen die entsprechend vorbereiteten Zeugnisberichte das Lernfeld 1. 

## Abkürzungsverzeichnis Berufe

In der Datei BS_Faecher.keys werden die folgenden Abkürzungen pro Beruf verwendet:

Ausbildungsberufe|Abkürzung
-----------------|-----------
Anlagenmechaniker/-in |Am
Anlagenmechaniker/-in für Sanitär Heizung Klima|AmSHK
Augenoptiker|Aug
Ausbaufacharbeiter/-in im SP Estricharbeiten|AbfaEst
Ausbaufacharbeiter/-in im SP Fliesen-, Platten- und Mosaikarbeiten|AbfaFli
Ausbaufacharbeiter/-in im SP Stukkateurarbeiten|AbfaStuc
Ausbaufacharbeiter/-in im SP Zimmerarbeiten|AbfaZim
Automobobilkaufmann/-frau|Akfm
Bäcker/-in|Bäc
Bankkaufmann/-frau|Bakfm
Baugeräteführer/-in|Baug
Bauten- und Objektbeschichter/-in|BauOb
Bauwerksmechaniker für Abbruch und Betontrenntechnik|BaumAB
Bauzeichner/-in SP Architektur|BauzA
Bauzeichner/-in SP Ingenieurbau|BauzI
Bauzeichner/-in SP Tief-, Straßen-, Landschaftsbau|BauzTSL
Berufskraftfahrer/-in|Ber
Beton- und Stahlbetonbauer/-in|Bet
Biologielaborant/-in|Bio
Chemielaborant/-in|Che
Dachdecker/-in|Dac
Eisenbahner/-in|Eis
Elektroniker/-in FR Automatisierungstechnik|EleA
Elektroniker/-in FR Energie- und Gebäudetechnik|EleEG
Elektroniker/-in für Automatisierungstechnik|EleAT
Elektroniker/-in für Betriebstechnik|EleBT
Elektroniker/-in für Geräte und Systeme|EleGS
Elektroniker für Maschinen und Antriebstechnik|EleMA
Estrichleger/-in |Est
Fachinformatiker/-in FR Anwendungsentwicklung|FainA
Fachinformatiker/-in FR Systemintegration|FainS
Fachkraft für Kurier-, Express- und Postdienstleistungen|FakKEP
Fachkraft für Lagerlogistik|FakL
Fachkraft für Metalltechnik FR Konstruktionstechnik|FakMK
Fachkraft für Metalltechnik FR Montagetechnik|FakMM
Fachkraft für Metalltechnik FR Umform- und Drahttechnik|FakMUD
Fachkraft für Metalltechnik FR Zerspanungstechnik|FakMZ
Fachkraft für Möbel-, Küchen- und Umzugsservice|FakMKU
Fachkraft für Veranstaltungstechnik|FakV
Fachkraft im Gastgewerbe|FakG
Fachlagerist/-in|Fal
Fachmann/-frau für Systemgastronomie|FaSys
Fachverkäufer/-in im Lebensm. SP Bäckerei/Konditorei|FvkBä
Fachverkäufer/-in im Lebensm. SP Fleischerei|FvkFl
Fahrradmonteur/-in|Fahm
Fahrzeuglackierer/-in|Fahrz
Feinwerkmechaniker/-in SP Feinmechanik|FeiF
Feinwerkmechaniker/-in SP Maschinenbau|FeiM
Feinwerkmechaniker/-in SP Werkzeugbau|FeiW
Fertigungsmechaniker/-in|Fer
Fleischer/-in|Fle
Fliesen-, Platten-, Mosaikleger/-in|Fli
Friseur/-in|Fri
Geomatiker/-in|Geo
Gestalter/-in für visuelles Marketing|Ges
Gießereimechaniker/-in|Gie
Glaser FR Fenster- und Glasfassadenbau|GlaFG
Glaser FR Verglasung und Glasbau|GlaVG
Gleisbauer/-in|Gle
Hauswirtschafter/-in|Hau
Hochbaufacharbeiter/-in|Hoc
Hotelfachmann/-frau|Hofa
Hotelkaufmann/-frau|Hokfm
Immobilienkaufmann/-frau|Imkfm
Industrieelektriker/-in FR Betriebstechnik|IneB
Industrieelektriker/-in FR Geräte und Systeme|IneGS
Industriekaufmann/-frau|Inkfm
Industriemechaniker/-in|Inme
Informatikkaufmann/-frau|Infkfm
Informationselektroniker/-in SP Bürosystemtechnik|InfeB
Informationselektroniker/-in SP Geräte- und Systemtechnik|InfeGS
IT-System-Elektroniker/-in|IT-SE
IT-System-Kaufmann/-frau|IT-Skfm
Karosserie- und Fahrzeugbaumechaniker/-in FR Karosserie und Fahrzeugb|KarKF
Karosserie- und Fahrzeugbaumechaniker/-in FR Karosserieinstandhaltung|KarK
Kaufmann/-frau für Büromanagement|KfmB
Kaufmann/-frau für Dialogmarketing|KfmD
Kaufmann/-frau für Marketingkommunikation|KfmM
Kaufmann/-frau für Spedition und Logistikdienstleistungen|KfmSL
Kaufmann/-frau für Tourismus und Freizeit|KfmTF
Kaufmann/-frau für Versicherungen und Finanzen FR Finanzen|KfmVFF
Kaufmann/-frau für Versicherungen und Finanzen FR Versicherungen|KfmVFV
Kaufmann/-frau im Einzelhandel|KfmEH
Kaufmann/-frau im Gesundheitswesen|KiG
Kaufmann/-frau im Groß- und Außenhandel FR Außenhandel|KfmGHA
Kaufmann/-frau im Groß- und Außenhandel FR Großhandel|KfmGHG
Klempner/-in|Kle
Koch/Köchin|Koc
Konditor/-in|Kon
Konstruktionsmechaniker/-in|Kom
Kraftfahrzeugmechatroniker/-in SP Karosserietechnik|KfZK
Kraftfahrzeugmechatroniker/-in SP Motorradtechnik|KfZM
Kraftfahrzeugmechatroniker/-in SP Nutzfahrzeugtechnik|KfZN
Kraftfahrzeugmechatroniker/-in SP Personenkraftwagentechnik|KfZP
Kraftfahrzeugmechatroniker/-in SP System- und Hochvolttechnik|KfZSH
Land- und Baumaschinenmechatroniker|Lam
Maler/-in und Lackierer/-in FR Gestaltung und Instandhaltung|MalGI
Maurer/-in|Mau
Mechatroniker/-in für Kältetechnik|MecK
Mechatroniker/-in|Mec
Mediengestalter/-in Bild Ton|MedBT
Mediengestalter/-in Digital und Print FR Beratung,Planung|MedDPB
Mediengestalter/-in Digital und Print FR Gestaltung und Technik|MedDPG
Mediengestalter/-in Digital und Print FR Konzeption, Visualisierung|MedDPK
Medientechnologe/-in Druck|MedtD
Medientechnologe/-in Siebdruck|MedtS
Medizinische/-r Fachangestellte/-r|MFa
Metallbauer/-in FR Konstruktion|MetK
Notarfachangestellte/-r|Nofa
Pferdewirt/-in|Pfe
Pharmazeutisch-kaufmännische/-r Angestellte/-r|PkA
Polster- und Dekonäher/-in|Pol
Raumausstatter/-in|Rau
Rechtsanwaltsfachangestellte/-r|Refa
Restaurantfachmann/-frau|Rest
Schilder- und Lichtreklamehersteller/-in|Schi
Schornsteinfeger/-in|Scho
Servicekraft Dialogmarketing|SerD
Sport- und Fitnesskaufmann/-frau|SFkfm
Straßenbauer/-in|Strab
Straßenwärter/-in|Straw
Stuckateuer/-in|Stuc
Technische/-r Modellbauer/-in FR Gießerei|TecMG
Technische/-r Produktdesigner FR Maschinen- und Anlagenkonstruktion|TecPM
Technische/-r Produktdesigner FR Produktgestaltung|TecPP
Technische/-r.Systemplaner/-in FR Elektrotechnische Systeme|TecSE
Technische/-r Systemplaner/-in FR Stahl-, Metallbautechnik|TecSS
Technische/-r Systemplaner/-in FR Versorgungs- und Ausrüstungstechnik|TecSV
Tiefbaufacharbeiter/-in|Tief
Tiermedizinische/-r Fachangestellte/-r|TFa
Tischler/-in|Tis
Tourismuskaufmann/-frau|Tkfm
Veranstaltungskaufmann/-frau|Vkfm
Verfahrensmechaniker für Kunststoff- und Kautschuktechnik FR Bauteile|VmKKB
Verfahrensmechaniker für Kunststoff- und Kautschuktechnik FR Formteile|VmKKF
Verfahrensmechaniker für Kunststoff- und Kautschuktechnik FR Halbzeuge|VmKKH
Verfahrensmechaniker für Kunststoff- und Kautschuktechnik FR Kunststoff|VmKKK
Verkäufer/-in|Vk
Vermessungstechniker/-in|Verm
Verwaltungsfachangeste/-r|Verw
Werkstoffprüfer/-in|Werp
Werkzeugmechaniker/-in|Werm
Zahnmedizinische/-r Fachangestellte/-r|ZFa
Zahntechniker/-in|Zat
Zerspanungsmechaniker/-in|Zerm
Zimmerer/-in|Zim
Zweiradmechatroniker/-in FR Fahrradtechnik|ZwF
Zweiradmechatroniker/-in FR Motorradtechnik|ZwM
