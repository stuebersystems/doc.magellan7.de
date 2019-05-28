# Erste Schritte in MAGELLAN - Beispieldatenbank für den Echtbetrieb vorbereiten

Nach der Installation von MAGELLAN ist automatisch eine Beispieldatenbank hinterlegt, damit man sich anhand von Beispieldaten das Programm ansehen kann.
Um in den Echtbetrieb zu wechseln werden der Reihe nach folgende Schritte ausgeführt, Ziel ist eine leere Datenbank mit den Bundeslandspezifischen Statistik-schlüsseln vorzubereiten.

### Die Datenbank leeren

Starten Sie den MAGELLAN-Administrator und führen den Punkt ´Datenbankpflege > Datenbankinhalt´ löschen aus. Dabei bitte alles leeren, auch die angebotenen Häkchen für Verzeichnisse deaktivieren.

## Die IDs zurücksetzen

Führen Sie den Punkt ´Datenbankpflege > Datenbank überprüfen > Generatoren synchronisieren´ aus, um die in der Beispieldatenbank bereits verwendeten IDs wieder für Ihren MAGELLAN-Einsatz freizugeben. Damit würde der erste Schüler dann auch wieder die ID 1 erhalten.

## Postleitzahlen importieren

Wählen Sie bitte unter ´Datenimporte > Postleitzahlen importieren´ die Auswahl ´Deutschland´. Sie erhalten ein vollständiges Postleitzahlverzeichnis für Deutschland, inklusive der Gemeindekennziffern u.a., das für statistische Erhebungen später wichtig ist.
Berliner Schulen importieren bitte das Postleitzahlverzeichnis ´Berlin´, da hier zusätzlich die Berliner Stadtbezirke hinterlegt wurden. Für Schweizer Schulen steht ebenfalls ein Verzeichnis zur Verfügung.

## Schlüsselverzeichnisse importieren

Die Schlüsselverzeichnisse (zum Beispiel Fächer, Staatsangehörigkeiten, Noten u.a.) können unter dem Punkt ´Datenimporte > Schlüsselverzeichnisse importieren´ in die leere Datenbank eingelesen werden.
Bitte wählen Sie: Ihr Bundesland, wählen ob Sie Schlüssel für allgemeinbildende oder berufsbildende Schulen einlesen möchten, Ihre Schule und wählen bitte ´alle Kataloge´.
Gibt es für Ihre Region kein Angebot, wählen Sie bitte als Wert `Deutschland`aus, damit werden die mindestens für MAGELLAN-Abläufe wichtigen Verzeichnisse gefüllt.

## Schulen importieren

In MAGELLAN können für Schüler Herkunftsschulen oder auch bei Abgängern die neue Schule vermerkt werden. Für einige Bundesländer gibt es auch eine vordefinierte Liste der Schulen, die nach MAGELLAN eingelesen werden kann.
Rufen Sie den Punkt ´MAGELLAN-Administrator >  Datenim-porte > Daten über MAGELLAN-Importformat importieren´ auf. Auf der zweiten Karte wählen Sie den Single-Import und geben als Pfad den Pfad zu Ihrem Verzeichnis `MAGELLAN 7 > Importe > Ihr Bundesland` an und wählen dort die Datei ´Schulen.csv´ aus.

## Zeiträume anlegen

Starten Sie MAGELLAN und wechseln zum Einrichten eines Zeitraumes bitte auf `Verzeichnisse > Zeiträume`. Klicken Sie auf die Schaltfläche ´Schuljahre anlegen´ und stellen die Anzahl der zu erstellenden Schuljahre ein und klicken auf OK.

## Ihre Schuldaten eintragen

Wechseln Sie bitte in das Menü Mandanten, markieren die vorhandene Zeile und wechseln auf die Karte Daten. Bitte ändern Sie die Daten unserer Beispieldatenbank auf Ihre eigenen Daten ab. Fertig!
Sie können jetzt beginnen Ihre Schülerdaten eintragen. Wenn Sie Daten importieren möchten, können Sie dazu unser MAGELLAN-Importformat nutzen, die notwendigen Schritte beschreiben wir [Dokument MAGELLAN Import](https://doc.magellan6-import.stueber.de/).
