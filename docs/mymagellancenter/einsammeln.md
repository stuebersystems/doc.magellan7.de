# Einsammeln von Daten

## Noteneingabe über MyMagellan

Die Noteneingabe in MyMagellan ist der gesonderten Dokumentation [MyMagellan](https://doc.mymagellan.stueber.de/) zu entnehmen.

## Aktueller Stand?

Wenn die von den Kollegen mit Zeugnisdaten befüllten Dateien wieder an der Stelle abgelegt werden, an die sie beim Verteilen auch erzeugt wurden, erhalten Sie über das MyMagellan Center einen Überblick wessen Datei bereits gefüllt wieder vorliegt. 

Das MyMagellan Center zeigt Ihnen per Symbol, wessen Datei erzeugt wurde oder nicht, wessen Datei bereits gefüllt ist und wessen Datei bereits wieder nach Magellan eingelesen wurde. Sie haben so jederzeit den Überblick, ob alle für den Zeugnisdruck notwendigen Daten bereits übermittelt wurden.


|Symbol | Bedeutung |
|--|-- |
| <img src="/assets/images/mymagellan/close-circle-red.png"> | Datei fehlt |
| <img src="/assets/images/mymagellan/export.png"> | Datei erzeugt |
| <img src="/assets/images/mymagellan/pencil-blue.png"> | Datei bearbeitet |
| <img src="/assets/images/mymagellan/import-green.png">  | Datei nach Magellan importiert |

## Dateien einsammeln

Wenn die Dateien der Kollegen wieder vorliegen, können sie einzeln oder gesammelt wieder in die Datenbank übertragen werden. Markieren Sie dazu die Zeilen der Kollegen, deren gefüllte Dateien Sie einsammeln möchten und aktivieren den Prozess über die Schaltfläche am oberen Fensterrand des Magellan ADMINISTRATORS:


![Starten Sie das Einsammeln der Zeugnisdaten](/assets/images/mymagellan/22.png)

Es startet der Assistent, bitte bestätigen Sie das Einlesen der Daten in die Datenbank mit `Fertigstellen`.

![Schließen Sie den Assistenten über `Fertigstellen` ab!](/assets/images/mymagellan/23.png)

## MyMagellan-Dateien einsammeln

Nachdem die Noteneingabe der MyMagellan-Teilnehmer erfolgt ist, müssen diese ihre MyMagellan-Dateien wieder in den gleichen MyMagellan-Ordner unter dem gleichen Dateinamen kopieren. Hierbei wird die bestehende, zuvor exportierte MyMagellan-Datei überspielt, wenn sie noch im Ordner vorliegt. Hat die MyMagellan-Datei ein neueres Dateidatum als der letzte Export, so wird in der Statusspalte das Symbol angezeigt. Sie wissen dann direkt, ob der Teilnehmer seine mit MyMagellan bearbeitete MyMagellan-Datei zurückgebracht hat.

So starten Sie das Einsammeln der MyMagellan-Dateien:

1. Markieren Sie die Teilnehmer, deren MyMagellan-Dateien Sie einsammeln wollen.

2. Klicken Sie auf `Umgebung` und dann auf `Daten einsammeln`.

3. Klicken Sie im Assistenten auf `Weiter`.

4. Klicken Sie auf `Fertigstellen` um das Einsammeln zu starten.

**Durch das Einsammeln der MyMagellan-Dateien werden alle entsprechenden Daten in Magellan mit den neuen Werten überschrieben!** Nach dem erfolgreichen Einsammeln wird die Importdatum in der Spalte „Letzter Import“ der jeweiligen MyMagellan-Datei gesetzt und in der Statusspalte wird das Symbol angezeigt. Für die Statusspalte gibt es somit vier Modi.

Statusspalte |Bedeutung
--|--
kein Symbol |Keine MyMagellan-Datei im angegebenen Ordner.
roter Pfeil|MyMagellan-Datei erzeugt: MyMagellan-Datei existiert im angegebenen Ordner.
blauer Pfeil|MyMagellan-Datei bereit zum Import: MyMagellan-Datei existiert im angegebenen Ordner und hat ein jüngeres Dateidatum als das letzte Exportdatum.
grüner Pfeil|MyMagellan-Datei erfolgreich importiert: MyMagellan-Datei existiert im angegebenen Ordner und hat ein älteres Dateidatum als das letzte Importdatum und ein jüngeres Dateidatum als das letzte Exportdatum.

!!! info "Hinweis"

	Beim Einlesen der MyMagellan-Dateien richtet sich das Verhalten beim Import der Felder „Fehlstunden“, „Fehlstunden unentschuldigt“, „Fehltage“ und „Fehltage unentschuldigt“ nach den Einstellungen beim Verteilen der MyMagellan-Dateien.a

## Löschen der MyMagellan-Dateien

Im MyMagellan Center können Sie keine mym-Dateien löschen und auch nicht beim Neuverteilen überschreiben. Sollten Sie beim Verteilen versuchen eine Datei zu erzeugen, die mit dem eingestellten Dateinamen an dem Speicherort bereits existiert, wird Ihnen eine Meldung ausgegeben. 
MyMagellan-Dateien können Sie direkt in Ihrem Verzeichnis auf Dateiebene löschen oder in eine anderes Verzeichnis archivieren.

## MyMagellan Dateien erneut importieren

Fällt nach dem Import auf, dass noch weitere Änderungen vorzunehmen sind, können MyMagellan-Dateien auch erneut importiert werden.

### Bemerkungen

!!! info "Hinweis"

	Wichtig bei den Bemerkungen, wie eigentlich auch bei allen anderen Zeugnisinformationen ist: Sind die MyMagellan-Dateien beim Lehrer darf nichts in Magellan verändert werden!

Bemerkungen, die später in der MyMagellan-Datei noch ergänzt werden, können einfach ergänzt oder auch bereits eingelesene noch geändert werden.
Beim erneuten Einlesen werden die Bemerkungen in Magellan gelöscht und durch die neu eingelesenen ergänzt. Es würden aber auch Bemerkungen gelöscht, die zwischenzeitlich in Magellan mit eingefügt wurden!!!

### Fehlzeiten

![Bei Fehlzeiten richtet es sich danach, welche Option Sie beim Erzeugen der MyMagellan-Datei gewählt haben.](/assets/images/mymagellan/mym_13.fehlzeitoptionen.png)

Die Option "Fehlstunden/-tage in Magellan beim Einsammeln addieren" ist ungeeignet fürs erneute Einlesen, da die Werte dann wieder aufsummiert werden, also die doppelte Anzahl von Fehlzeiten das Ergebnis wäre.

Gut geeignet ist die Option "Fehlstunden/-tage in Magellan beim Einsammeln überschreiben".

!!! warning "Wichtig"

	Kein Eintrag oder eine Null aus den Fehlzeiten in MyMagellan überschreibt keinen Magellan-Eintrag!
