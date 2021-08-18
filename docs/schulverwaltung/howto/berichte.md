# Formulare, Listen und Zeugnisse

[1]:/assets/images/formulare/formulare1.png
[2]:/assets/images/formulare/formulare2.png
[3]:/assets/images/formulare/formulare3.png
[4]:/assets/images/formulare/formulare4.png
[5]:/assets/images/formulare/formulare5.png
[6]:/assets/images/formulare/formulare6.png
[7]:/assets/images/formulare/formulare7.png
[8]:/assets/images/formulare/formulare8.png
[9]:/assets/images/formulare/formulare9.png
[10]:/assets/images/formulare/formulare10.png
[11]:/assets/images/formulare/formulare11.png

Dieses Kapitel beschreibt das Drucken von Formularen, Listen und Zeugnissen mit MAGELLAN. Grundlage für die Druckmöglichkeiten bilden Berichte, die im Berichtsgenerator Crystal Reports erstellt worden sind. Zum Ausdruck können Sie entweder auf von uns erstellte Berichte zurückgreifen oder Sie erstellen Berichte nach Ihren eigenen Bedürfnissen.

!!! info "Hinweis"

	Der Seriendruck über Word und die Exportmöglichkeiten nach Excel bzw./ werden im Kapitel [„Seriendruck, Serienemail, Dokumentenverwaltung und Exportieren“](https://doc.magellan.stueber.de/schulverwaltung/howto/seriendruck/) vorgestellt.

## MAGELLAN Crystal-Reports

### Allgemeines

Berichte definieren in MAGELLAN das Layout und den Inhalt von Ausdrucken in Form von Zeugnissen, Übersichten, Formularen, Listen usw. Diese Berichte sind in MAGELLAN standardmäßig in dem Berichtsgenerator Crystal Reports erstellt worden. 

Mit MAGELLAN wird eine große Anzahl von Crystal Reports-Berichten kostenlos mitgeliefert. Eine Übersicht über die vorhandenen Berichte finden Sie über den MAGELLAN-Berichts-Explorer. Alle darin erwähnten Crystal Reports-Berichte für Listen und Zeugnisse können mit dem kostenlos mitgelieferten Runtime-Modul von MAGELLAN ausgedruckt werden. Wenn Sie lediglich die mitgelieferten Zeugnisformulare verwenden, ohne Änderungen am Layout vorzunehmen, benötigen Sie keinen Druckreportgenerator, da bereits eine Runtime-Version des in MAGELLAN verwendeten Crystal Reports-Berichtsgenerators mitinstalliert wird. 

!!! info "Hinweis"

	 Wenn Sie Berichte selbst verändern oder erstellen möchten, benötigen Sie Crystal Reports. Der Vertrieb der Crystal Reports Lizenzen erfolgt ausschließlich über SAP. Bitte wenden Sie sich direkt.

### Unterstützte Crystal Reports Versionen

MAGELLAN verfügt über eine Drucktechnologie, die Crystal Reports 9, 10, XI ... 2016 unterstützt. Die Berichte werden aktuell in Crystal Reports 2016 zur Verfügung gestellt, die abwärtskompatibel bis zur Version 9 von Crystal Reports sind. 

## Berichte organisieren

Alle Berichte in MAGELLAN sind den entsprechenden Bereichen für Schüler, Bewerber, Klassen, Lehrer, Sorgeberechtigte, Betriebe, Personen, Adressen, Schulen, Mandanten zugeordnet. Zusätzlich gibt es noch die gesonderten Bereiche Zeugnisse und Kurslisten für Schüler. Alle Berichte können auf Basis der Auswahllisten der jeweiligen Bereiche gedruckt werden. Wie Sie die Berichte ausdrucken, erfahren Sie im nachfolgenden Abschnitt „Berichte drucken“. Die Verwaltung der Berichte öffnen Sie über `Extras > Berichte organisieren`.

[![Das Fenster "Berichte organisieren" besteht aus einer Schnellstartleiste auf der linken Seite, die den Bereichen in MAGELLAN entsprechen.][1]][1]

Klicken Sie beispielsweise auf den Ordner `Klassen`, so erscheinen auf der rechten Seite alle Berichte, die für Klassen existieren. Über die Funktion `Kopieren > Einfügen` können Sie die einzelnen Berichte in den gewünschten Ordner verschieben. Alle Berichte, die sich in dem Ordner „Kurslisten“ befinden, werden ebenfalls dem Bereich der Klassen zugeordnet. Berichte im Ordner `Zeugnisse` werden dem Bereich der Schüler zugeordnet. Über die Schaltfläche `Dokumente importieren` können Sie Ihre Berichtsverwaltung um eventuell selbst erstellte Berichte erweitern.

## Berichte drucken

### Formulare und Listen

Sie drucken Listen bzw. Formulare, indem Sie in die entsprechende Auswahlliste wechseln und dort die gewünschten Einträge markieren, für die ein Bericht gedruckt werden soll. Wollen Sie z.B. einen Bericht für Schüler ausdrucken, dann müssen Sie einen oder mehrere Schüler im Bereich `Schüler > Auswahl` markieren und über `Start > Drucken > Bericht drucken` aufrufen. Es öffnet sich das Fenster Bericht drucken, in dem Sie den gewünschten Bericht auswählen können.

[![Klicken Sie auf „Vorschau“, um den Bericht nur in der Vorschau zu öffnen.][2]][2]

Wenn Sie im Schüler-Drucken Fenster auf `Export nach PDF` klicken, wird zunächst der Berichte für alle markierten Schüler pro Schüler ins PDF-Format exportiert und dann erfolgt der eigentliche Druck. Zusätzlich gibt es auch die Funktion `Export nach PDF`, das nur die PDF-Version speichert. Diese Funktion können Sie beispielsweise nutzen um den letzten Stand des Zeugnisdrucks abschließend für die Schüler in ihren Schülerunterverzeichnissen zu speichern. Diese Schaltflächen sind zusätzlich zur Schaltfläche `Drucken` nur dann aktiv, wenn Sie unter `Datenbank > Optionen > Dokumente` den Export ins PDF-Format eingestellt haben.

[![Einstellungen in den MAGELLAN Optionen][9]][9]

Andernfalls ist nur die Schaltfläche `Drucken` aktiv. Berichte im Menü `Mandanten` beziehen sich auf alle Daten des aktuellen Zeitraums des markierten Mandanten. Hier finden Sie z.B. Übersichtslisten über alle Schüler des Mandanten, Bewerberranglisten über alle Bewerber des Mandanten usw.

!!! info "Hinweis"

	Sie können alle Berichte optional nach Excel, Word oder ins PDF-Format exportieren. Rufen Sie dazu die Seitenvorschau des Berichtes auf und klicken oben links `Bericht exportieren`. Wählen Sie anschließend das gewünschte Export-Format (z.B. Excel-Format) und legen Sie einen Speicherort fest. Sie können die Berichte dann z.B. im Excel-Format weiterverarbeiten.

[![Druckvorschau][10]][10]

### Kurslisten

Um Kurslisten zu drucken, müssen Sie die entsprechende(n) Klasse(n) im Menü `Klassen > Auswahl` markieren und über `Start > Drucken > Kurslisten drucken... ` wählen. Es öffnet sich das Fenster `Kursliste drucken`.

[![Aufruf "Kurslisten drucken..."][11]][11]

[![Stellen Sie hier die gewünschten Filter ein. Klicken Sie dann auf OK und wählen Sie den gewünschten Bericht zum Druck aus.][4]][4]

### Prüfungslisten

Prüfungslisten basieren auf den Daten in des Menüs `Abitur`. Um Prüfungslistenlisten zu drucken, müssen Sie die entsprechende(n) Schüler(n) im Menü `Abitur` markieren und dann mit der rechten Maustaste den Befehl `Prüfungslistenlisten drucken` wählen. Es öffnet sich das Fenster `Prüfungsliste drucken`.
 
[![Stellen Sie hier die gewünschten Filter für die Prüfungsliste ein. Klicken Sie dann auf `OK` und wählen Sie den gewünschten Bericht zum Druck aus.][5]][5]

### Zeugnisse

So drucken Sie Zeugnisse:

1. Um Zeugnisse zu drucken, müssen Sie den bzw. die entsprechenden Schüler im  Menü `Schüler` markieren und dann mit der rechten Maustaste den Befehl `Zeugnisse drucken` wählen.

[![Dialog „Zeugnisse drucken“][6]][6]

2. Wählen Sie den gewünschten Report aus und klicken Sie auf `Vorschau`.

[![Zeugnis in der Seitenvorschau][7]][7] 

Klicken Sie dann auf `Drucken` und der gewünschte Report wird gedruckt. Wenn Sie auf `Drucken und Export nach PDF` klicken, wird zunächst das Zeugnis für alle markierten Schüler pro Schüler ins PDF-Format exportiert und dann erfolgt der eigentliche Druck. Diese Schaltfläche ist anstatt der Schaltfläche `Drucken` nur dann sichtbar, wenn Sie in den Optionen den Export ins PDF-Format eingestellt haben (siehe „Einstellung für Crystal Reports Berichte“). Andernfalls lautet die Schaltfläche nur `Drucken`.

!!! info "Hinweis"

	Sie können alle Zeugnisse optional nach Excel, Word oder ins PDF-Format exportieren. Rufen Sie dazu die Seitenvorschau des Berichtes auf und klicken Sie links oben auf das Symbol für "Bericht exportieren". Wählen Sie anschließend das gewünschte Export-Format (z.B. Acrobat-Format) und legen Sie einen Speicherort fest. Sie können die Zeugnisse dann z.B. im Word-Format weiterverarbeiten.

[![Druckvorschau, Bericht exportieren][10]][10] 

So drucken Sie beim Schüler hinterlegte Zeugnisse: 

Um die beim Schüler hinterlegten Zeugnisse automatisiert zu drucken, müssen Sie den bzw. die entsprechenden Schüler im  Menü `Schüler` markieren und dann über  `Start > Drucken > Zeugnisformulare drucken...` wählen. Weitere Informationen finden Sie dazu im Abschnitt [Zeugnisformulare](https://doc.magellan.stueber.de/schulverwaltung/howto/zeugnisdaten/#zeugnisformulare).

[![Es kann ggf. nach einem Typ gefiltert werden, wenn Sie diesen im `Schlüsselverzeichnis > Zeugnisformulare` bei den Formularen hinterlegt haben.][8]][8] 

## Eigene Berichte erstellen

Wenn Sie neue Berichte erstellen bzw. vorhandene verändern möchten,  benötigen Sie einen Berichtsgenerator, d.h. ein Programm, mit dem Sie Berichte erstellen und verändern können. MAGELLAN verwendet ausschließlich den Berichtsgenerator Crystal Reports. In MAGELLAN werden daher nur Crystal Reports Berichte mitgeliefert.
Die Datenstruktur der MAGELLAN Datenbank wird im Dokument [MAGELLAN Datenstruktur](https://doc.magellan7-toolbox.stueber.de/datenstruktur/) beschrieben.

STÜBER SYSTEMS bietet zudem Schulungen zur Berichtserstellung in MAGELLAN an, die Ihnen eine Einführung geben bzw. Ihr Wissen vertiefen, unsere Schulungstermine können Sie auf unserer Webseite unter [Schulungen](https://www.stueber.de/training.php) einsehen. 

Außerdem bietet STÜBER SYSTEMS speziellen Support zur Berichtserstellung mit MAGELLAN und Crystal Reports, die Unterstützung in Fragen rund um die Berichtserstellung oder -anpassung ist nicht Teil des MAGELLAN Supportvertrages. Um Berichte selbst erstellen zu können, benötigen Sie sehr gutes Wissen in der Berichtserstellung in Crystal Reports und der MAGELLAN Datenstruktur. 
In der Regel ist es bei der Erstellung eigener Berichte am einfachsten, einen der mitgelieferten Berichte zu nehmen und diesen entsprechend abzuändern. Das Erlernen dieses Wissens ist nicht sehr schwer, aber auch nicht ganz einfach. Wenn Sie sich die Zeit und den Einarbeitungsaufwand sparen möchten, können Sie STÜBER SYSTEMS beauftragen, Ihre Zeugnisse und andere Berichte zu erstellen. Sie erhalten dann von STÜBER SYSTEMS die entsprechenden Crystal Reports Berichtsdateien, die Sie lediglich in das entsprechende Berichtsverzeichnis kopieren müssen. Schicken Sie dazu Ihre Papiervorlagen an STÜBER SYSTEMS. Sie erhalten dann ein Angebot über die Kosten für die Erstellung der Berichte.
