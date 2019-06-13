#	Katalog der Auswahltabellen

Auswahltabellen dienen einzig und allein dem Zweck kurzfristig für den Druck von Crystal Reports Berichten mit den Eckdaten des Drucks gefüllt zu werden. Diese Eckdaten entsprechen der Auswahl der Druckdaten in Ihrem MAGELLAN-Modul (MAGELLAN, MAGELLAN-Bibliothek, MAGELLAN-Haushalt&Inventar etc.). Die Daten dienen als Ausgang, um Berichte in Crystal Reports zu erzeugen.
Alle folgenden Tabellen werden über ihre Ansichten angesprochen. Die Benennung der Ansichten ist gleich der Tabellen ohne den Prefix `tbl`.


!!! info "Hinweis"

    Die Auswahltabellen und Ansichten haben temporären Charakter. Sie speichern die aktuelle Datensatz-Auswahl in MAGELLAN und dienen als Schnittstelle für die Berichtserstellung in Crystal Reports oder MS-Access. 
    Wenn Sie beispielsweise in der Schüler-Gesamtliste mehrere Schüler markieren und dann einen Bericht drucken wollen, so werden die Verweise auf die markierten Schüler in der entsprechenden Auswahl-Ansicht festgehalten. 


Es existieren folgende Auswahl-Ansichten:


| Ansicht                | Enthält                                  |
|------------------------|------------------------------------------|
| AuswahlAdressen        | Auswahl der Adressen                     |
| AuswahlBetriebe        | Auswahl der Betriebe                     |
| AuswahlBewerber        | Auswahl der Bewerber                     |
| AuswahlBuchungen       | Auswahl der Buchungen                    |
| AuswahlHaushalt        | Auswahl der Haushaltsjahre, Haushaltstitel und Haushaltsstellen |
| AuswahlInventar        | Auswahl des Inventars                    |
| AuswahlKlassen         | Auswahl der Klassen                      |
| AuswahlKurslisten      | Auswahl der Klassen/Jahrgänge und Fächer/Kurse beim Kurslistendruck. |
| AuswahlLehrer          | Auswahl der Lehrer                       |
| AuswahlMandanten       | Auswahl der Mandanten                    |
| AuswahlMedien          | Auswahl der Medien                       |
| AuswahlMedienAusleiher | Auswahl der Medienausleiher              |
| AuswahlMedienVorgaenge | Auswahl der Medienvorgänge               |
| AuswahlPersonen        | Auswahl der Personen                     |
| AuswahlPruefungslisten | Auswahl der Prüfungslisten im Abitur     |
| AuswahlSchueler        | Auswahl der Schüler                      |
| AuswahlSchulen         | Auswahl der Schulen                      |
| AuswahlSorgebe         | Auswahl der Sorgeberechtigten            |
| AuswahlSportfeste      | Auswahl der Sportfeste                   |
| AuswahlZeugnisse       | Auswahl der Schüler beim Zeugnisdruck    |




Bei den meisten Auswahl-Ansichten werden neben der eigentlichen Auswahl immer auch der aktuelle Mandant und der aktuelle Zeitraum hinterlegt.

##	Sonstige Tabellen und Ansichten

Es gibt noch einige Tabellen und Ansichten, die bisher nicht erwähnt wurden. Diese spielen bei Betrachtung der Datenstruktur eine eher untergeordnete Rolle. Hierzu zählen das Postleitzahlverzeichnis in der Tabelle Postleitzahlen, sowie die undokumentierte Ansicht Benutzer für die Benutzerverwaltung.

