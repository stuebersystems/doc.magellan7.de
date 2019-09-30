# Access-Anbindung an die Firebird-Datenbank

Möchten Sie Bescheinigungen, Listen oder Zeugnisse drucken, so bietet Ihnen MAGELLAN standardmäßig die Ausdruckmöglichkeit über Crystal Reports an.
Alternativ können Sie auch Abfragen oder Berichte unter Microsoft Access erstellen. Hierzu müssen Sie auf Basis einer ODBC-Verbindung eine Verknüpfung zwischen Access und der Firebird-Datenbank herstellen,um mit Access auf die Daten zugreifen zu können.

!!! info "Hinweis"

	 Um einen unbefugten Zugriff per Access auf die MAGELLAN-Datenbank zu verhindern, muss auf die Anzahl der Benutzer von Access bereits über das Betriebssystem eingeschränkt werden.

Für Access müssen die folgenden Schritte berücksichtigen, die in den nachfolgenden Abschnitten dieses Kapitels ausführlich erläutert werden:

1. Schritt: Prüfen ob mit 32- oder 64-Bit-Access gearbeitet wird.
2. Schritt: Erstellen einer ODBC-Verbindung zu Firebird-Datenbank
3. Schritt: Ein neue Access-Datenbank anlegen
4. Schritt: Tabellen verknüpfen

## Access als 32- oder 64-Bit-Ausgabe

Als erstes müssen Sie prüfen, ob Sie mit einer 32- oder 64-Bit-Officeversion arbeiten. Je nach Officeversion kann die Stelle dazu abweichen, wir beschreiben hier die Stelle für Office 365.
Öffnen Sie bitte Access und wechseln auf `Datei > Konto > Infos zu Access`. Noch über der `Product ID` wird die Version gezeigt, am Ende der Zeile gibt es den Hinweis auf 32- oder 64-Bit.

!!! warning "Wichtig"

    Wenn mit einer 64-Bit Officeausgabe arbeiten, führen Sie bitte diese Schritt aus. Nutzen Sie eine 32-Bit-Ausgabe, überspringen Sie bitte den nächsten Punkt.

## 64-Bit Ausgabe von Access mit Firebird verknüpfen

Installieren Sie bitte **parallel** zur 32-Bit-Ausgabe von Firebird eine 64-Bit Ausgabe, das Installationpaket finden Sie unter [64-bit Classic, Superclassic & Superserver](https://firebirdsql.org/en/firebird-2-5-9/#Win64).

Zusätzlich brauchen Sie noch den passenden ODBC-Treiber, dieser darf natürlich **nicht** den von MAGELLAN verwendeten Treiber ersetzen, sondern soll zusätzlich an einem anderen Ort Ihrer Wahl abgelegt werden.
Die zur Verfügung stehenden Dateien finden Sie hier: [https://firebirdsql.org/en/odbc-driver/](https://firebirdsql.org/en/odbc-driver/). Bitte wählen Sie ein Ziparchiv (keine *.exe), in der rechten Spalte der Tabelle steht `Win 64-bit DLL`. Dieses Paket entpacken Sie an beliebiger Stelle. Im Unterverzeichnis `bin` finden Sie den Treiber `fbclient.dll`. 

!!! warning "Wichtig"

    Auf diese Datei werden Sie im folgenden beim Einrichten der ODBC-Anbindung verweisen, wählen Sie als Ablagestelle **NICHT** `C:\WINDOWS\system32\` um nicht versehentlich den von MAGELLAN verwendeten Treiber zu überschreiben.

## ODBC-Verbindung zur Firebird-Datenbank erstellen

Öffnen Sie in der Systemsteuerung den Punkt `Verwaltung > ODBC-Datenquellen`. Fügen Sie eine neue `ODBC-Verbindung` hinzu.

![ODBC-Datenquellen-Administrator](/assets/images/magellan.administrator/02.png)

Feld|Eintrag
--|--
Data Source Name (DNS) |freiwählbare Bezeichnung
Descritption | frei wählbar
Database | Nutzen Sie die Schaltfläche `Browse` und verweisen auf die gewünschte Datenbank.
Client | Nutzen Sie die Schaltfläche `Browse` und verweisen Sie auf die gesondert gespeicherte 64-bit `fbclient.dll`
Database Account | Tragen Sie Ihre MAGELLAN-Anmeldedaten ein, das Feld `Role` bleibt leer.
Character Set | Wählen Sie hier bitte `UTF8` aus.
Options / Transaction | keine Auswahl treffen
Options / Extendet identifier properties |Bitte alle aktivieren

Testen Sie abschließend die Verbindung, indem Sie auf `Test connection` klicken.

## Neue Access-Datenbank anlegen

Nachdem Sie die ODBC-Verbindung im ersten Schritt erstellt haben, müssen Sie jetzt eine Access-Datenbank anlegen, welche mit der neuen ODBC-Verbindung eine Verknüpfung zur MAGELLAN-Datenbank aufbaut. Die Vorgehensweise wird exemplarisch unter Microsoft Access 2000 vorgestellt:

1. Starten Sie Microsoft Access.

2. Klicken Sie auf `Datei` und dann auf `Neu`.

3. Wählen Sie im Dialog `Neu` auf der Registerkarte `Allgemein `die Option `Datenbank` und klicken Sie dann auf `OK`.

4. Speichern Sie die neue Datenbank unter einem Namen ab, z.B. unter `C:\Stueber System\MAGELLAN 7\Datenbank\MAGELLAN7.accdb`.

## Leere Access-Datenbank mit Firebirddatenbank verknüpfen

1. Wählen Sie bitte `Externe Daten > Neue Datenquelle > aus anderen Quellen > ODBC-Datenbank`.

2. Wählen Sie im nächsten Fenster bitte die Option `Erstellen Sie eine Verknüpfung zur Datenquelle, indem Sie eine verknüpfte Tabelle erstellen`.
3. Im nächsten Fenster wechseln Sie bitte auf den Reiter `Computerdatenquelle` und wählen die von Ihnen vorab erstellte ODBC-Anbindung aus.

4. Im Dialogfenster `Tabellen verknüpfen` werden Ihnen jetzt alle Tabellen der MAGELLAN-Datenbank zur Auswahl angeboten. Markieren Sie hier durch Mehrfachmarkierung alle Tabellen, die nicht den Präfix „tbl“ (z.B. tblLehrer) besitzen. Wenn Sie das Kennwort der ODBC-Verbindung nicht bei jedem Aufruf eines Access-Berichts später eingeben wollen, müssen Sie zusätzlich das Optionsfeld `Kennwort speichern` anwählen. Klicken Sie abschließend auf `OK`.

Während der Erstellung der Tabellenverknüpfungen werden Sie bei einigen Tabellen aufgefordert, eindeutige Datensatzbezeichner auszuwählen. Hier können Sie jeweils auf `Abbrechen` klicken, da diese Einstellungen für das Drucken nicht relevant sind.

Die Verknüpfung zwischen der Firebirddatenbank und der Access-Datenbank ist jetzt erstellt. Über die Tabellen haben Sie einen direkten Zugriff auf die originale Firebird MAGELLAN-Datenbank MAGELLAN7.fdb.

!!! warning "Wichtig"

    Bitte denken Sie daran, dass das nicht der Weg ist um Daten in MAGELLAN einzupflegen, der ID-Generator innerhalb von Magellan "weiß" nichts von diesem Zugriff. Legen Sie beispielweise hier eine Klasse an und versuchen anschließend eine Klasse in MAGELLAN an, wird versucht die über Access genutzte ID erneut zu verwenden. Diese Anbindung ist rein zur Auswertung gedacht!

!!! info "Hinweis"

      Beim Erstellen der Verknüpfungen zu der Tabelle „Schueler“ unter Microsoft Access erhalten Sie von Access die Rückmeldung, dass eine Verknüpfung nicht möglich ist. Die Tabellen „Schueler“ und „Lehrer“ enthalten mehr als 32 Datenbankindizes. Microsoft Access kann maximal 32 Datenbankindizes verarbeiten. Eine Verknüpfung über den von uns mitgelieferten aktuellen Firebird Open Source Treiber erzeugt daher die korrekte Fehlermeldung. Sie können in der MAGELLAN-Datenbank anstelle der Tabellen „Schueler“ bzw. „Lehrer“ das View „Schueler2“ bzw. „Lehrer2“ verwenden. Beim Verknüpfen von Views werden in Access keine Indizes erzeugt, so dass es keine Probleme mehr gibt. Die beiden View „Schueler2“ bzw. „Lehrer2“ verweisen auf alle Felder der Tabelle „Schueler“ bzw. „Lehrer“.
