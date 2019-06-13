# Katalog der Tabellen

Eine Tabelle in einer Datenbank ist der physikalische Speicherort für eine strukturierte Form von Daten. So enthält beispielsweise die Tabelle tblLehrer alle in MAGELLAN gespeicherten Lehrer.
Eine Ansicht (der Fachbegriff ist VIEW) definiert mit Hilfe einer SQL-Abfrage eine bestimmte Sichtweise auf eine oder mehrere Tabellen. Die Daten sind weiterhin in den entsprechenden Tabellen gespeichert. So definiert beispielsweise die Ansicht Lehrer eine Sichtweise auf die Tabelle tblLehrer.
Die Ansichten in der MAGELLAN Datenbank werden im Abschnitt [Ansichten  (Views)](https://doc.magellan7-datenstruktur.stueber.de/ansichten)behandelt.


Wenn Sie sich die Datenstruktur von MAGELLAN näher betrachten, werden Sie feststellen, dass es neben den vielen Tabellen auch eine Reihe von Ansichten gibt. In einigen Fällen ist der Zugriff auf bestimmte Daten einer Tabelle nur über entsprechende Ansichten möglich.
Als Beispiel sei hier das Zusammenspiel zwischen der Tabelle tblLehrer und der Ansicht Lehrer genannt. Während die Tabelle tblLehrer stets alle Lehrer auflistet, sorgt die Ansicht Lehrer dafür, dass in den meisten Fällen nur der Lehrer aufgelistet wird, der zum aktuellen Benutzer passt. Der Hintergrund hierbei: Ein normaler Lehrer soll nur seine eigenen Personaldaten sehen können und nicht die seiner Kollegen. Der direkte Zugriff auf die Tabelle tblLehrer ist somit gesperrt.
Ansichten verhalten sich nach außen hin genauso wie Tabellen, so dass Sie in der Regel nichts weiter beachten müssen.

