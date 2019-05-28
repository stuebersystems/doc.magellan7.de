## Gemeindekennziffern nachträglich setzen

Erfasst man Adressdaten über die MAGELLAN-Oberfläche kann nach dem Eintippen der Postleitzahl (oder des Ortes) die Tab-Taste gedrückt werden, die Folgefelder werden, wenn die Postleitzahl eindeutig ist, vorbesetzt. 

Ist die Postleitzahl nicht eindeutig, also gehören zur Postleitzahl mehrere Zeilen im Postleitzahlverzeichnis, erscheint ein Fenster und Sie können aus den angezeigten Einträgen die korrekte Zeile wählen.

![Auswahlfenster, wenn die Eingabe mehreren Einträgen zugeordnet werden könnte](images/gemeinde.png)



Importieren Sie Daten über unser MAGELLAN-Importformat oder spielen Sie ein neues Postleitzahlverzeichnis ein, ist die Verbindung zwischen den Adressdaten des Schülers (Lehrers, Betriebs) erst einmal nicht vorhanden. Die Gemeindekennziffer ist für statistische Abfragen aus MAGELLAN in vielen Bundesländern die Grundlage. Ein Nachtragen per Hand wäre sehr aufwändig.

Dafür gibt es eine Funktion im Modul MAGELLAN ADMINISTRATOR, dass die Postleitzahl und den Ort der Adresse mit den Eintragungen im Verzeichnis der Postleitzahlen vergleicht und bei Übereinstimmung die Gemeindekennziffer zuweist.

Die Funktion können Sie im Modul MAGELLAN ADMINISTRATOR aufrufen:

1. Melden Sie sich als sysdba am MAGELLAN ADMINISTRATOR an.
2. Rufen Sie bitte `Datenbankpflege > Datenbank überprüfen > Gemeinden synchronisieren` auf und starten den Assistenten.

Der Assistent prüft die Postleitzahl und den Ort, stimmt beides mit einem Eintrag des Verzeichnisses überein, wird die Gemeindekennzahl für den Datensatz ergänzt.

Um Einträge in der Datenbank finden zu können, die eine ungültige Postleitzahl oder einen ungültigen Ort hinterlegt haben, gibt es einen Prüfbericht. Bitte öffnen Sie MAGELLAN und rufen das Druckfenster im Menü `Mandanten` auf. Sie finden den Bericht "Mandanten (Ausgabe Schueler ohne Gemeindekennziffer).rpt". Der Bericht zeigt Ihnen pro Halbjahr die Schüler an, deren Adressdaten Sie bitte prüfen und korrigieren sollten. Lassen Sie im Anschluss den Assistenten unter `Datenbankpflege > Datenbank überprüfen > Gemeinden synchronisieren` bitte erneut laufen. Ist der Prüfbericht im Anschluss leer, sind bei allen Schülern die Gemeindekennziffern gesetzt.

![Prüfbericht im Menü Mandanten](images/gemeinde1.png)

