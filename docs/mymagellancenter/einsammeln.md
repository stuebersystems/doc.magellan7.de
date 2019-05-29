# Einsammeln von Daten

## Noteneingabe über MyMAGELLAN

Die Noteneingabe in MyMAGELLAN ist der gesonderten Dokumentation [MyMAGELLAN](https://doc.MyMAGELLAN6.stueber.de/) zu entnehmen.


## Aktueller Stand?

Wenn die von den Kollegen mit Zeugnisdaten befüllten Dateien wieder an der Stelle abgelegt werden, an die sie beim Verteilen auch erzeugt wurden, erhalten Sie über das MyMAGELLAN CENTER einen Überblick wessen Datei bereits gefüllt wieder vorliegt. 

Das MyMAGELLAN CENTER zeigt Ihnen per Symbol, wessen Datei erzeugt wurde oder nicht, wessen Datei bereits gefüllt ist und wessen Datei bereits wieder nach MAGELLAN eingelesen wurde. Sie haben so jederzeit den Überblick, ob alle für den Zeugnisdruck notwendigen Daten bereits übermittelt wurden.



|Symbol | Bedeutung |
|--|-- |
| ![](/assets/images/mymagellan/close-circle-red.png) | Datei fehlt |
| ![](/assets/images/mymagellan/export.png) | Datei erzeugt |
| ![](/assets/images/mymagellan/pencil-blue.png) | Datei bearbeitet |
| ![](/assets/images/mymagellan/import-green.png) | Datei nach MAGELLAN importiert |

## Dateien einsammeln

Wenn die Dateien der Kollegen wieder vorliegen, können sie einzeln oder gesammelt wieder in die Datenbank übertragen werden. Markieren Sie dazu die Zeilen der Kollegen, deren gefüllte Dateien Sie einsammeln möchten und aktivieren den Prozess über die Schaltfläche am oberen Fensterrand des MAGELLAN ADMINISTRATORS:


![Starten Sie das Einsammeln der Zeugnisdaten](/assets/images/mymagellan/22.png)

Es startet der Assistent, bitte bestätigen Sie das Einlesen der Daten in die Datenbank mit `Fertigstellen`.

![Schließen Sie den Assistenten über `Fertigstellen` ab!](/assets/images/mymagellan/23.png)



## MyMAGELLAN-Dateien einsammeln

Nachdem die Noteneingabe der MyMAGELLAN-Teilnehmer erfolgt ist, müssen diese ihre MyMAGELLAN-Dateien wieder in den gleichen MyMAGELLAN-Ordner unter dem gleichen Dateinamen kopieren. Hierbei wird die bestehende, zuvor exportierte MyMAGELLAN-Datei überspielt, wenn sie noch im Ordner vorliegt. Hat die MyMAGELLAN-Datei ein neueres Dateidatum als der letzte Export, so wird in der Statusspalte das Symbol angezeigt. Sie wissen dann direkt, ob der Teilnehmer seine mit MyMAGELLAN bearbeitete MyMAGELLAN-Datei zurückgebracht hat.

So starten Sie das Einsammeln der MyMAGELLAN-Dateien:

1. Markieren Sie die Teilnehmer, deren MyMAGELLAN-Dateien Sie einsammeln wollen.

2. Klicken Sie auf `Umgebung `und dann auf `Daten einsammeln`.

3. Klicken Sie im Assistenten auf `Weiter`.

4. Klicken Sie auf `Fertigstellen` um das Einsammeln zu starten.

**Durch das Einsammeln der MyMAGELLAN-Dateien werden alle entsprechenden Daten in Magellan mit den neuen Werten überschrieben!** Nach dem erfolgreichen Einsammeln wird die Importdatum in der Spalte „Letzter Import“ der jeweiligen MyMAGELLAN-Datei gesetzt und in der Statusspalte wird das Symbol angezeigt. Für die Statusspalte gibt es somit vier Modi.

Statusspalte |Bedeutung
--|--
kein Symbol |Keine MyMAGELLAN-Datei im angegebenen Ordner.
roter Pfeil|MyMAGELLAN-Datei erzeugt: MyMAGELLAN-Datei existiert im angegebenen Ordner.
blauer Pfeil|MyMAGELLAN-Datei bereit zum Import: MyMAGELLAN-Datei existiert im angegebenen Ordner und hat ein jüngeres Dateidatum als das letzte Exportdatum.
grüner Pfeil|MyMAGELLAN-Datei erfolgreich importiert: MyMAGELLAN-Datei existiert im angegebenen Ordner und hat ein älteres Dateidatum als das letzte Importdatum und ein jüngeres Dateidatum als das letzte Exportdatum.

!!! info "Hinweis"

	Beim Einlesen der MyMAGELLAN-Dateien richtet sich das Verhalten beim Import der Felder „Fehlstunden“, „Fehlstunden unentschuldigt“, „Fehltage“ und „Fehltage unentschuldigt“ nach den Einstellungen beim Verteilen der MyMAGELLAN-Dateien.a

## Löschen der MyMAGELLAN-Dateien

Im MyMAGELLAN CENTER können Sie keine mym-Dateien löschen und auch nicht beim Neuverteilen überschreiben. Sollten Sie beim Verteilen versuchen eine Datei zu erzeugen, die mit dem eingestellten Dateinamen an dem Speicherort bereits existiert, wird Ihnen eine Meldung ausgegeben. 
MyMAGELLAN-Dateien können Sie direkt in Ihrem Verzeichnis auf Dateiebene löschen oder in eine anderes Verzeichnis archivieren.


## MyMAGELLAN Dateien erneut importieren

Fällt nach dem Import auf, dass noch weitere Änderungen vorzunehmen sind, können MyMAGELLAN-Dateien auch erneut importiert werden.


### Bemerkungen

!!! info "Hinweis"

	Wichtig bei den Bemerkungen, wie eigentlich auch bei allen anderen Zeugnisinformationen ist: Sind die MyMAGELLAN-Dateien beim Lehrer darf nichts in MAGELLAN verändert werden!

Bemerkungen, die später in der MyMAGELLAN-Datei noch ergänzt werden, können einfach ergänzt oder auch bereits eingelesene noch geändert werden.
Beim erneuten Einlesen werden die Bemerkungen in MAGELLAN gelöscht und durch die neu eingelesenen ergänzt. Es würden aber auch Bemerkungen gelöscht, die zwischenzeitlich in MAGELLAN mit eingefügt wurden!!!

### Fehlzeiten

![Bei Fehlzeiten richtet es sich danach, welche Option Sie beim Erzeugen der MyMAGELLAN-Datei gewählt haben.](/assets/images/mymagellan/mym_13.fehlzeitoptionen.png)



Die Option "Fehlstunden/-tage in MAGELLAN beim Einsammeln addieren" ist ungeeignet fürs erneute Einlesen, da die Werte dann wieder aufsummiert werden, also die doppelte Anzahl von Fehlzeiten das Ergebnis wäre.

Gut geeignet ist die Option "Fehlstunden/-tage in MAGELLAN beim Einsammeln überschreiben".


!!! warning "Wichtig"

	Kein Eintrag oder eine Null aus den Fehlzeiten in MyMAGELLAN überschreibt keinen MAGELLAN-Eintrag!
