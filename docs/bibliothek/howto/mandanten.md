# Mit mehreren Mandanten arbeiten

[1]:/assets/images/bibliothek/mandanten01.png
[2]:/assets/images/bibliothek/mandanten02.png
[3]:/assets/images/bibliothek/mandanten03.png

Magellan Bibliothek ist wie das Basismodul mandantenfähig. Dies bedeutet, dass Sie die Bibliotheksdaten unterschiedlicher organisatorischer Gliederungen in einer Datenbank verwalten können. Dieses Datenbankkonzept erfordert, dass mindestens ein Mandant angelegt ist, da alle Daten in Magellan bezogen auf bestimmte Mandanten gespeichert werden.

!!! info "Hinweis"

    Mandanten können nur im Basismodul angelegt werden. Wie Sie dabei vorgehen, entnehmen Sie bitte dem Kapitel [Datenbank vorbereiten](../../schulverwaltung/howto/preparation.md) im Magellan-Benutzerhandbuch.

Die meisten Anwender von Magellan und Magellan Bibliothek arbeiten mit nur einem Mandanten. In diesem Fall müssen Sie im Bibliotheksmodul keine weiteren Einstellungen vornehmen. Der im Basismodul angelegte Mandant wird beim Programmstart automatisch als aktueller Mandant voreingestellt. Der Name des aktivierten Mandanten wird auf der Schaltfläche `Mandant` in der Symbolleiste des Programmfensters angezeigt.

Wenn Sie allerdings mit mehreren Mandanten arbeiten, müssen Sie im Vorfeld den Mandanten auswählen, dessen Daten Sie bearbeiten wollen.

Gehen Sie dazu bitte folgendermaßen vor:

1. Betätigen Sie die Schaltfläche `Mandant` in der Symbolleiste des Programmfensters.
2. Markieren Sie im Aufklappmenü den gewünschten Mandanten und bestätigen Sie Ihre Auswahl mit `OK`.

[![Mandantenauswahl][1]][1]

Der Name des ausgewählten Mandanten erscheint auf der Schaltfläche `Mandant`. Die Daten, die für diesen Mandanten gespeichert wurden, sind nun in den einzelnen Ansichten verfügbar.
Sie können darüberhinaus im Vorfeld festlegen, welcher Mandant beim Start von Magellan-Bibliothek aktiv gesetzt sein soll.

Um diese Einstellung vorzunehmen, gehen Sie bitte folgendermaßen vor:

1. Rufen Sie den Menüpunkt `Datenbank > Optionen` auf
2. Bleiben Sie in der Navigation links auf `Start`.
3. Betätigen Sie die Pfeilschaltfläche des Auswahlfeldes `Mandant` und markieren Sie im Aufklappmenü den gewünschten Eintrag.
4. Bestätigen Sie Ihre Angaben abschließend mit `OK`.
Der gewählte Mandant wird nun beim nächsten Programmstart automatisch als aktueller Mandant voreingestellt.

[![In der Navigation `Start` des Dialogfensters `Optionen` stellen Sie den Startmandanten ein.][2]][2]

Die Liste der in Magellan angelegten Mandanten können Sie in der Ansicht `Mandanten` auf der Registerkarte `Auswahl` einsehen. Auf der Registerkarte `Daten` ist für jeden Mandanten eine Karteikarte mit den wesentlichen Kontaktinformationen hinterlegt.

[![Ansicht der angelegten Mandanten in Magellan][3]][3]

