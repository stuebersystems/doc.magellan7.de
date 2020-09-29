# Mit mehreren Mandanten arbeiten

MAGELLAN BIBLIOTHEK ist wie das Basismodul mandantenfähig. Dies bedeutet, dass Sie die Bibliotheksdaten unterschiedlicher organisatorischer Gliederungen in einer Datenbank verwalten können. Dieses Datenbankkonzept erfordert, dass mindestens ein Mandant angelegt ist, da alle Daten in MAGELLAN bezogen auf bestimmte Mandanten gespeichert werden.

!!! info "Hinweis"

    Mandanten können nur im Basismodul angelegt werden. Wie Sie dabei vorgehen, entnehmen Sie bitte dem Kapitel [Datenbank vorbereiten](../../schulverwaltung/howto/preparation.md) im MAGELLAN-Benutzerhandbuch.

Die meisten Anwender von MAGELLAN und MAGELLAN BIBLIOTHEK arbeiten mit nur einem Mandanten. In diesem Fall müssen Sie im Bibliotheksmodul keine weiteren Einstellungen vornehmen. Der im Basismodul angelegte Mandant wird beim Programmstart automatisch als aktueller Mandant voreingestellt. Der Name des aktivierten Mandanten wird auf der Schaltfläche `Mandant` in der Symbolleiste des Programmfensters angezeigt.

Wenn Sie allerdings mit mehreren Mandanten arbeiten, müssen Sie im Vorfeld den Mandanten auswählen, dessen Daten Sie bearbeiten wollen.

Gehen Sie dazu bitte folgendermaßen vor:

1. Betätigen Sie die Schaltfläche `Mandant` in der Symbolleiste des Programmfensters.
2. Markieren Sie im Aufklappmenü den gewünschten Mandanten und bestätigen Sie Ihre Auswahl mit `OK`.

![Mandantenauswahl](/assets/images/bibliothek/mandanten01.png)

Der Name des ausgewählten Mandanten erscheint auf der Schaltfläche `Mandant`. Die Daten, die für diesen Mandanten gespeichert wurden, sind nun in den einzelnen Ansichten verfügbar.
Sie können darüberhinaus im Vorfeld festlegen, welcher Mandant beim Start von MAGELLAN-BIBLIOTHEK aktiv gesetzt sein soll.

Um diese Einstellung vorzunehmen, gehen Sie bitte folgendermaßen vor:

1. Rufen Sie den Menüpunkt `Datenbank > Optionen` auf
2. Bleiben Sie in der Navigation links auf `Start`.
3. Betätigen Sie die Pfeilschaltfläche des Auswahlfeldes `Mandant` und markieren Sie im Aufklappmenü den gewünschten Eintrag.
4. Bestätigen Sie Ihre Angaben abschließend mit `OK`.
Der gewählte Mandant wird nun beim nächsten Programmstart automatisch als aktueller Mandant voreingestellt.

![In der Navigation `Start` des Dialogfensters `Optionen` stellen Sie den Startmandanten ein.](/assets/images/bibliothek/mandanten02.png)

Die Liste der in MAGELLAN angelegten Mandanten können Sie in der Ansicht `Mandanten` auf der Registerkarte `Auswahl` einsehen. Auf der Registerkarte `Daten` ist für jeden Mandanten eine Karteikarte mit den wesentlichen Kontaktinformationen hinterlegt.

![Ansicht der angelegten Mandanten in MAGELLAN](/assets/images/bibliothek/mandanten03.png)
