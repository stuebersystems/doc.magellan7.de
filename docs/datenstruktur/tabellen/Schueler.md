# Tabelle Schueler



| Feldname                      | Typ | Größe | Funktion | Bemerkung                                |
|-------------------------------|-----|-------|----------|------------------------------------------|
| Mandant                       | I   | -     | PV       | Verweis auf Tabelle<br/> **Mandanten**   |
| ID                            | I+  | -     | P        | -                                        |
| EnbreaID                      | A   | 24    | -        | Externer Identifikator aus ENBREA        |
| GUID                          | A   | 32    | -        | -                                        |
| IDIntern                      | I   | -     | -        | -                                        |
| IDExtern                      | I   | -     | -        | -                                        |
| GUIDExtern                    | A   | 36    | -        | -                                        |
| Barcode                       | A   | 20    | -        | -                                        |
| BarcodePrint                  | A   | 20    | -        | -                                        |
| Nachname                      | A   | 100   | -        | -                                        |
| NachnameNative                | A   | 100   | -        | -                                        |
| Namenszusatz                  | A   | 100   | -        | -                                        |
| NamenszusatzNative            | A   | 100   | -        | -                                        |
| Vorname                       | A   | 100   | -        | -                                        |
| VornameNative                 | A   | 100   | -        | -                                        |
| Vorname2                      | A   | 100   | -        | -                                        |
| Vorname2Native                | A   | 100   | -        | -                                        |
| Anrede                        | A   | 1     | -        | **Mögliche Werte:**<br/>0 = Frau<br/>1 = Herr<br/>2 = Frau Dr.<br/>3 = Herr Dr.<br/>4 = Frau Prof.<br/>5 = Herr Prof.<br/>6 = Frau Prof. Dr.<br/>7 = HerrProf. Dr.<br/>: = Ms.<br/>; = Mrs.<br/>< = Mr. |
| Geschlecht                    | A   | 1     | -        | **Mögliche Werte:**<br/>W = Weiblich<br/>M = Männlich |
| Geburtsdatum                  | D   | -     | -        | -                                        |
| Geburtsort                    | A   | 100   | -        | -                                        |
| Geburtskreis                  | A   | 100   | -        | -                                        |
| Geburtsland                   | A   | -     | -        | Verweis auf Tabelle **Staatsangehoerigkeiten** |
| Geburtsname                   | A   | 50    | -        | -                                        |
| Strasse                       | A   | 100   | -        | -                                        |
| Adresszusatz                  | A   | 200   | -        | -                                        |
| Land                          | A   | 3     | -        | -                                        |
| PLZ                           | A   | 5     | -        | -                                        |
| Ort                           | A   | 100   | -        | -                                        |
| Ortsteil                      | A   | 100   | -        | -                                        |
| Adressgebiet                  | A   | 300   | -        | -                                        |
| Gemeinde                      | A   | -     | V        | Verweis auf Tabelle **Gemeinden**        |
| Stadtbezirk                   | A   | -     | V        | Verweis auf Tabelle **Stadtbezirke**     |
| Telefon                       | A   | 30    | -        | -                                        |
| Telefax                       | A   | 30    | -        | -                                        |
| Mobil                         | A   | 30    | -        | -                                        |
| EMail                         | A   | 100   | -        | -                                        |
| Wohnform                      | A   | -     | V        | Verweis auf Tabelle **Wohnformen**       |
| Staatsangeh1                  | A   | -     | V        | Verweis auf Tabelle **Staatsangehoerigkeiten** |
| Staatsangeh2                  | A   | -     | V        | Verweis auf Tabelle **Staatsangehoerigkeiten** |
| Muttersprache                 | A   | -     | V        | Verweis auf Tabelle **Muttersprachen**   |
| Verkehrssprache               | A   | -     | V        | Verweis auf Tabelle **Muttersprachen**   |
| Sprachgruppe                  | A   | -     | V        | Verweis auf Tabelle **Sprachgruppen**    |
| Konfession                    | A   | -     | V        | Verweis auf Tabelle **Konfessionen**     |
| RelWunsch                     | A   | -     | V        | Verweis auf Tabelle **RelWuensche**      |
| NichtDeutscheHerkunft         | L   | -     | -        | -                                        |
| RelTeilnahme                  | A   | -     | V        | Verweis auf Tabelle **RelTeilnahmen**    |
| RelGrund                      | A   | -     | V        | Verweis auf Tabelle **RelGruende**       |
| RelAbmeldungVon               | D   | -     | -        | -                                        |
| RelAbmeldungBis               | D   | -     | -        | -                                        |
| Umschulung                    | A   | -     | V        | Verweis auf Tabelle **Umschulungsmerkmale** |
| Funktion1                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Funktion2                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Funktion3                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Funktion4                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Funktion5                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Funktion6                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Funktion7                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Funktion8                     | A   | -     | V        | Verweis auf Tabelle **SchuelerFunktionen** |
| Personalnr                    | A   | 15    | -        | -                                        |
| Behinderung                   | A   | -     | V        | Verweis auf Tabelle **Behinderungsarten** |
| Krankenkasse                  | A   | -     | V        | Verweis auf Tabelle **Krankenkassen**    |
| Versicherungsart              | A   | -     | V        | Verweis auf Tabelle **Versicherungsarten** |
| NotfallPerson                 | A   | 50    | -        | -                                        |
| NotfallTelefon                | A   | 30    | -        | -                                        |
| Fahrschueler                  | L   | -     | -        | -                                        |
| Fahrstrecke                   | A   | 50    | -        | -                                        |
| FahrstreckeKM                 | N   | -     | -        | -                                        |
| Einstiegsstelle               | A   | 50    | -        | -                                        |
| Verkehrsmittel                | A   | -     | V        | Verweis auf Tabelle **Verkehrsmittel**   |
| Fahrgeld                      | N   | -     | -        | -                                        |
| FahrgeldbewVon                | D   | -     | -        | -                                        |
| FahrgeldbewBis                | D   | -     | -        | -                                        |
| Fahrkarte                     | A   | -     | V        | Verweis auf Tabelle **Fahrkarten**       |
| FahrkarteGueltigVon           | D   | -     | -        | -                                        |
| FahrkarteGueltigBis           | D   | -     | -        | -                                        |
| KFZ                           | A   | 15    | -        | -                                        |
| Status                        | S   | -     | -        | **Mögliche Werte:**<br/>0 = Bewerber (unbestätigt)<br/>1 = Bewerber<br/>2 = Neu (Keine Klasse / Kein Zeitraum)<br/>3 = Eingeschult (aktiv in Klasse undZeitraum)<br/>4 = Abgänger (inaktiv in Klasse und Zeitraum)<br/>5 = Vorlage Bewerber<br/>6 = Vorlage Schüler<br/>7 = Abwesend/Pausiert |
| Anmeldestatus                 | S   | -     | -        | **Mögliche Werte:**<br/>0 = LABO<br/>1 = Angemeldet ( und angenommen)<br/>2 = AAG (Antrag, Aufnahme an andere Grundschule) |
| Profil                        | A   | -     | V        | Verweis auf Tabelle **SchuelerProfile**  |
| Aussiedler                    | L   | -     | -        | -                                        |
| AussiedlerSeit                | D   | -     | -        | -                                        |
| Auslaender                    | L   | -     | -        | -                                        |
| AuslaenderSeit                | D   | -     | -        | -                                        |
| InDeutschlandSeit             | D   | -     | -        | -                                        |
| AufenthaltserlaubnisBis       | D   | -     | -        | -                                        |
| SchulpflichtErfuellt          | L   | -     | -        | -                                        |
| Bafoeg                        | L   | -     | -        | -                                        |
| BafoegBis                     | D   | -     | -        | -                                        |
| Integrationsschueler          | L   | -     | -        | -                                        |
| Gastschueler                  | L   | -     | -        | -                                        |
| GastschulgeldUeberwiesen      | L   | -     | -        | -                                        |
| Bildungskarte                 | L   | -     | -        | **Mögliche Werte:**<br/>0 = B1 (Berlin)<br/>1 = B2 (Berlin)<br/>2 = L (Berlin) |
| BildungskarteBis              | D   | -     | -        | -                                        |
| Foerderung                    | A   | -     | V        | Verweis auf Tabelle **Foerderungen**     |
| Foerdernr                     | A   | 8     | -        | -                                        |
| Foerderbetrag                 | N   | -     | -        | -                                        |
| Unterstuetzung                | A   | -     | V        | Verweis auf Tabelle **Unterstuetzungen** |
| Betreuung                     | S   | -     | -        | **Mögliche Werte:**<br/>0 = Heim<br/>1 = Hort<br/>2 =Internat |
| BetreuungAdresse              | I   | -     | V        | Verweis auf Tabelle **Adressen**         |
| MittagessenTeilnahme          | L   | -     | -        | -                                        |
| GanztagbetriebGebunden        | S   | -     | -        | **Mögliche Werte:**<br/>0 = Früh mit Ferien<br/>1 = Früh und spät mit Ferien<br/>2 = Spät und Ferien<br/>3 = Nur Ferienbetreuung |
| GanztagbetriebOffen           | S   | -     | -        | Mögliche Werte:<br/>0 = Früh<br/>1 = Nachmittags<br/>2 = Früh und nachmittags<br/>3 = Nachmittags und spät<br/>4 = Früh, nachmittags und spät<br/>5 = Nur Ferienbetreuung |
| BewerbungAm                   | D   | -     | -        | -                                        |
| Bewerbungsziel1               | A   | -     | V        | Verweis auf Tabelle **Bewerbungsziele**  |
| Bewerbungsziel2               | A   | -     | V        | Verweis auf Tabelle **Bewerbungsziele**  |
| Bewerbungsziel3               | A   | -     | V        | Verweis auf Tabelle **Bewerbungsziele**  |
| Bewerbungsziel4               | A   | -     | V        | Verweis auf Tabelle **Bewerbungsziele**  |
| BewerberStatus                | S   | -     | -        | **Mögliche Werte:**<br/>0 = Auf Warteliste<br/>1 = Angenommen für Bildungsziel 1<br/>2 = Angenommen für Bildungsziel 2br/>3 = Angenommen für Bildungsziel 3<br/>4 = Nicht angenommen<br/>5 = Angenommen für Bildungsziel 4<br/>6 = Beratungstest<br/>7 = Beratungsgespräch<br/>8 = Nicht zum Gespräch/Testerschienen <br/>9 = Aufnahmebescheid<br/>10 = Zusage nicht zurück<br/>11 = Abgemeldet<br/>12 = Rückmeldung |
| BewerberStatusAm              | D   | -     | -        | -                                        |
| BewerberNote                  | N   | -     | -        | Gesamtdurchschnitt                       |
| BewerberHFNote                | N   | -     | -        | Hauptfächerdurchschnitt                  |
| BewerberPunkte                | N   | -     | -        | -                                        |
| BewerberRangzahl              | S   | -     | -        | -                                        |
| BewerberRangzahlZiel1         | S   | -     | -        | -                                        |
| BewerberRangzahlZiel2         | S   | -     | -        | -                                        |
| BewerberRangzahlZiel3         | S   | -     | -        | -                                        |
| BewerberRangzahlZiel4         | S   | -     | -        | -                                        |
| Fremdsprache1                 | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Fremdsprache1Von              | S   | -     | -        | -                                        |
| Fremdsprache1Bis              | S   | -     | -        | -                                        |
| Fremdsprache1Note             | N   | -     | -        | -                                        |
| Fremdsprache1Status           | S   | -     | -        | Mögliche Werte:<br/>0 = Unterricht an berichtender Schule<br/>1 = Unterricht an anderer Schule<br/>2 = Unterricht anerkannt<br/>3 =Unterricht abgewählt<br/>4 = Wahlunterricht<br/>5 = Fach<br/>6 = Hauptfach<br/>7 = Ergänzendes Fach |
| Fremdsprache1Status2          | S   | -     | -        | **Mögliche Werte:**<br/>0 = Pflichtfach/Wahlpflichtfach<br/>1 = Wahlfach (fakultative FS)<br/>2 = Arbeitsgemeinschaft<br/>3 = Förderunterricht<br/>4 = Pflichtfach<br/>5 = Wahlpflichtfach<br/>6 = Neigungsunterricht<br/>7 = Muttersprachl. Unterricht<br/>8 = Basiskurs<br/>9 = Erweiterungskurs<br/>10 = Gymnasialkurs |
| Fremdsprache1Referenz         | I   | -     | V        | Verweis auf Tabelle **Sprachreferenzen** |
| Fremdsprache2                 | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Fremdsprache2Von              | S   | -     | -        | -                                        |
| Fremdsprache2Bis              | S   | -     | -        | -                                        |
| Fremdsprache2Note             | N   | -     | -        | -                                        |
| Fremdsprache2Status           | S   | -     | -        | **Mögliche Werte:**<br/>0 = Unterricht an berichtender Schule<br/>1 = Unterricht an anderer Schule<br/>2 = Unterricht anerkannt<br/>3 = Unterricht abgewählt<br/>4 = Wahlunterricht<br/>5 = Fach<br/>6 = Hauptfach<br/>7 = Ergänzendes Fach |
| Fremdsprache2Status2          | S   | -     | -        | **Mögliche Werte:**<br/>0 = Pflichtfach/Wahlpflichtfach<br/>1 = Wahlfach (fakultative FS)<br/>2 = Arbeitsgemeinschaft<br/>3 = Förderunterricht<br/>4 = Pflichtfach<br/>5 = Wahlpflichtfach<br/>6 = Neigungsunterricht<br/>7 = Muttersprachl. Unterricht<br/>8 = Basiskurs<br/>9 = Erweiterungskurs<br/>10 = Gymnasialkurs |
| Fremdsprache2Referenz         | I   | -     | V        | Verweis auf Tabelle **Sprachreferenzen** |
| Fremdsprache3                 | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Fremdsprache3Von              | S   | -     | -        | -                                        |
| Fremdsprache3Bis              | S   | -     | -        | -                                        |
| Fremdsprache3Note             | N   | -     | -        | -                                        |
| Fremdsprache3Status           | S   | -     | -        | **Mögliche Werte:**<br/>0 = Unterricht an berichtender Schule<br/>1 = Unterricht an anderer Schule<br/>2 = Unterricht anerkannt<br/>3 = Unterricht abgewählt<br/>4 = Wahlunterricht<br/>5 = Fach<br/>6 = Hauptfach<br/>7 = Ergänzendes Fach |
| Fremdsprache3Status2          | S   | -     | -        | **Mögliche Werte:**<br/>0 = Pflichtfach/Wahlpflichtfach<br/>1 = Wahlfach (fakultative FS)<br/>2 = Arbeitsgemeinschaft<br/>3 = Förderunterricht<br/>4 = Pflichtfach<br/>5 = Wahlpflichtfach<br/>6 = Neigungsunterricht<br/>7 = Muttersprachl. Unterricht<br/>8 = Basiskurs<br/>9 = Erweiterungskurs<br/>10 = Gymnasialkurs |
| Fremdsprache3Referenz         | I   | -     | V        | Verweis auf Tabelle **Sprachreferenzen** |
| Fremdsprache4                 | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Fremdsprache4Von              | S   | -     | -        | -                                        |
| Fremdsprache4Bis              | S   | -     | -        | -                                        |
| Fremdsprache4Note             | N   | -     | -        | -                                        |
| Fremdsprache4Status           | S   | -     | -        | **Mögliche Werte:**<br/>0 = Unterricht an berichtender Schule<br/>1 = Unterricht an anderer Schule<br/>2 = Unterricht anerkannt<br/>3 = Unterricht abgewählt<br/>4 = Wahlunterricht<br/>5 = Fach<br/>6 = Hauptfach<br/>7 = Ergänzendes Fach |
| Fremdsprache4Status2          | S   | -     | -        | **Mögliche Werte:**<br/>0 = Pflichtfach/Wahlpflichtfach<br/>1 = Wahlfach (fakultative FS)<br/>2 = Arbeitsgemeinschaft<br/>3 = Förderunterricht<br/>4 = Pflichtfach<br/>5 = Wahlpflichtfach<br/>6 = Neigungsunterricht<br/>7 = Muttersprachl. Unterricht<br/>8 = Basiskurs<br/>9 = Erweiterungskurs<br/>10 = Gymnasialkurs |
| Fremdsprache4Referenz         | I   | -     | V        | Verweis auf Tabelle **Sprachreferenzen** |
| Grundschuleintritt            | D   | -     | -        | -                                        |
| Latinum                       | L   | -     | -        | -                                        |
| Graecum                       | L   | -     | -        | -                                        |
| Einschulung                   | S   | -     | -        | **Mögliche Werte:**<br/>0 = Vorzeitige Einschulung<br/>1 = Fristgerechte Einschulung<br/>2 = Verspätete Einschulung |
| HoechsterBildungsgangABS      | A   | -     | V        | Verweis auf Tabelle **Bildungsgaenge**   |
| HoechsterAbschlussABS         | A   | -     | V        | Verweis auf Tabelle **AbschluesseExtern** |
| HoechsterAbschlussABSAm       | D   | -     | -        | -                                        |
| HoechsterAbschlussABSNote     | N   | -     | -        | -                                        |
| HoechsterAbschlussABSSchule   | I   | -     | V        | Verweis auf Tabelle **SchuelerSchulen**  |
| HoechsterBildungsgangBBS      | A   | -     | V        | Verweis auf Tabelle **Bildungsgaenge**   |
| HoechsterAbschlussBBS         | A   | -     | V        | Verweis auf Tabelle **AbschluesseExtern** |
| HoechsterAbschlussBBSAm       | D   | -     | -        | -                                        |
| HoechsterAbschlussBBSBeruf    | A   | -     | V        | Verweis auf Tabelle **Berufe**           |
| HoechsterAbschlussBBSNote     | N   | -     | -        | -                                        |
| HoechsterAbschlussBBSSchule   | I   | -     | V        | Verweis auf Tabelle **SchuelerSchulen**  |
| HoechsterAbschlussBBSAustritt | S   | -     | -        | **Mögliche Werte:**<br/>0 = Abschluss<br/>1 = Abgang<br/>2 = Abbruch |
| Berufsjahre                   | N   | -     | -        | -                                        |
| Ausbildung                    | I   | -     | V        | Verweis auf Tabelle **SchuelerAusbildung** |
| ZugangAm                      | D   | -     | -        | 1. Zugangsdatum                          |
| Zugang2Am                     | D   | -     | -        | 2. Zugangsdatum                          |
| HerkunftSchule                | I   | -     | V        | Verweis auf Tabelle **SchuelerSchulen**  |
| EinschulungAntrag             | L   | -     | -        | -                                        |
| EinschulungAbgebendeSchule    | I   | -     | V        | Verweis auf Tabelle **Schulen**          |
| Einschulmerkmal               | A   | -     | V        | Verweis auf Tabelle **Einschulmerkmale** |
| Einschulmerkmal2              | A   | -     | V        | Verweis auf Tabelle **Einschulmerkmale** |
| Einschulmerkmal3              | A   | -     | V        | Verweis auf Tabelle **Einschulmerkmale** |
| EinschulungBemerkung          | M   | -     | -        | -                                        |
| VoraussichtlichesEnde         | D   | -     | -        | -                                        |
| Ueberweisung                  | L   | -     | -        | -                                        |
| UeberweisungAm                | D   | -     | -        | -                                        |
| Abgang                        | A   | -     | V        | Verweis auf Tabelle **Abgangsarten**     |
| AbgangAm                      | D   | -     | -        | -                                        |
| Abgang2Am                     | D   | -     | -        | -                                        |
| Uebergang                     | A   | -     | V        | Verweis auf Tabelle **Uebergangsarten**  |
| UebergangAm                   | D   | -     | -        | -                                        |
| UebergangAnSchule             | I   | -     | V        | Verweis auf Tabelle **Schulen**          |
| UebergangAnSchulform          | A   | -     | V        | Verweis auf Tabelle **SchulformenUebergang** |
| UebergangKlassenstufe         | A   | -     | V        | Verweis auf Tabelle **Klassenstufen**    |
| UebergangUnterlagen           | L   | -     | -        | -                                        |
| UebergangFoerderUnterlagen    | L   | -     | -        | -                                        |
| UebergangZeugnis              | L   | -     | -        | -                                        |
| UebergangGeaendertAm          | DT  | -     | -        | -                                        |
| UebergangGeaendertVon         | A   | 20    | -        | -                                        |
| Bemerkung                     | M   | -     | -        | -                                        |
| Passfoto                      | B   | -     | -        | -                                        |
| MerkmalA1                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalA2                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalA3                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalA4                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalA5                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalA6                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS1                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS2                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS3                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS4                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS5                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS6                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS7                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS8                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS9                     | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalS10                    | A   | -     | V        | Verweis auf Tabelle **Schuelermerkmale** |
| MerkmalB1                     | A   | 100   | -        | -                                        |
| MerkmalB2                     | A   | 100   | -        | -                                        |
| MerkmalB3                     | A   | 100   | -        | -                                        |
| MerkmalB4                     | A   | 100   | -        | -                                        |
| MerkmalT1                     | A   | 100   | -        | -                                        |
| MerkmalT2                     | A   | 100   | -        | -                                        |
| MerkmalT3                     | A   | 100   | -        | -                                        |
| MerkmalT4                     | D   | -     | -        | -                                        |
| MerkmalD1                     | D   | -     | -        | -                                        |
| MerkmalD2                     | D   | -     | -        | -                                        |
| MerkmalD3                     | D   | -     | -        | -                                        |
| MerkmalD4                     | D   | -     | -        | -                                        |
| MerkmalU1                     | D   | -     | -        | -                                        |
| MerkmalU1                     | D   | -     | -        | -                                        |
| Auskunft                      | S   | -     | -        | **Mögliche Werte:**<br/>0 = Keine Angabe<br/>1 = Geheim |
| AuswaertigerSchueler          | A   | -     | V        | Verweis auf Tabelle **SchuelerArten**    |
| AusstellungBehoerde           | A   | 100   | -        | -                                        |
| AusstellungBehoerdeDatum      | D   | -     | -        | -                                        |
| BetreuungInnerschulisch1      | A   | -     | V        | Verweis auf Tabelle **BetreuungenInnerschulisch** |
| BetreuungInnerschulisch2      | A   | -     | V        | Verweis auf Tabelle **BetreuungenInnerschulisch** |
| BetreuungInnerschulisch3      | A   | -     | V        | Verweis auf Tabelle **BetreuungenInnerschulisch** |
| BetreuungAusserschulisch1     | A   | -     | V        | Verweis auf Tabelle **BetreuungenAusserschulisch** |
| BetreuungAusserschulisch2     | A   | -     | V        | Verweis auf Tabelle **BetreuungenAusserschulisch** |
| BetreuungAusserschulisch3     | A   | -     | V        | Verweis auf Tabelle **BetreuungenAusserschulisch** |
| AkteAngefordert               | L   | -     | -        | -                                        |
| LMAnteil                      | S   | -     | -        | Lernmittelanteil in Prozent vom Regelbeitrag |
| LMZahlungsstand               | S   | -     | -        | **Mögliche Werte:**<br/>0 = Unbezahlt<br/>1 = Mahnung 1<br/>2 = Mahnung 2<br/>3 = Mahnung 3<br/>4 = Bezahlt<br/>5 = Teilbezahlt |
| LMZahlungsstandDatum          | D   | -     | -        | -                                        |
| LMZusatzbeitrag               | N   | -     | -        | -                                        |
| LMBefreit                     | L   | -     | -        | -                                        |
| LMBefreitBis                  | D   | -     | -        | -                                        |
| AusweisAusgestelltAm          | D   | -     | -        | -                                        |
| AusweisBemerkung              | M   | -     | -        | -                                        |
| Wahlfach1                     | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Wahlfach2                     | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Wahlfach3                     | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Wahlfach4                     | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Wahlfach5                     | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| Wahlfach6                     | I   | -     | V        | Verweis auf Tabelle **Faecher**          |
| HoechsterAbschlussBBSBerufAm  | D   | -     | -        | -                                        |
| SchuelerausweisBis            | D   | -     | -        | -                                        |
| BLZ                           | I   | -     | -        | Bankleitzahl                             |
| Bank                          | I   | -     | V        | Verweis auf Tabelle **Banken**           |
| Bankkonto                     | A   | 20    | -        | Bankkonto 1                              |
| BankIBAN                      | A   | 28    | -        | -                                        |
| BankInhaber                   | A   | 300   | -        | -                                        |
| BankInfo                      | A   | 300   | -        | -                                        |
| BankBemerkung                 | A   | 300   | -        | -                                        |
| Bank2                         | I   | -     | V        | Verweis auf Tabelle **Banken**           |
| Bank2konto                    | A   | 20    | -        | Bankkonto 2                              |
| Bank2IBAN                     | A   | 28    | -        | -                                        |
| Bank2Inhaber                  | A   | 300   | -        | -                                        |
| Bank2Info                     | A   | 300   | -        | -                                        |
| Bank2Bemerkung                | A   | 300   | -        | -                                        |
| Rechnung1Name1                | A   | 100   | -        | Rechnungsadresse 1                       |
| Rechnung1Name2                | A   | 100   | -        | -                                        |
| Rechnung1Strasse              | A   | 100   | -        | -                                        |
| Rechnung1Adressgebiet         | A   | 300   | -        | -                                        |
| Rechnung1Land                 | A   | 3     | -        | -                                        |
| Rechnung1PLZ                  | A   | 5     | -        | -                                        |
| Rechnung1Ort                  | A   | 100   | -        | -                                        |
| Rechnung1Ortsteil             | A   | 100   | -        | -                                        |
| Rechnung1Adresszusatz         | A   | 200   | -        | -                                        |
| Rechnung2Name1                | A   | 100   | -        | Rechnungsadresse 2                       |
| Rechnung2Name2                | A   | 100   | -        | -                                        |
| Rechnung2Strasse              | A   | 100   | -        | -                                        |
| Rechnung2Adressgebiet         | A   | 300   | -        | -                                        |
| Rechnung2Land                 | A   | 3     | -        | -                                        |
| Rechnung2PLZ                  | A   | 5     | -        | -                                        |
| Rechnung2Ort                  | A   | 100   | -        | -                                        |
| Rechnung2Ortsteil             | A   | 100   | -        | -                                        |
| Rechnung2Adresszusatz         | A   | 200   | -        | -                                        |
| HeimatName1                   | A   | 100   | -        | Heimatadresse                            |
| HeimatName2                   | A   | 100   | -        | -                                        |
| HeimatStrasse                 | A   | 100   | -        | -                                        |
| HeimatAdressgebiet            | A   | 300   | -        | -                                        |
| HeimatLand                    | A   | 3     | -        | -                                        |
| HeimatPLZ                     | A   | 5     | -        | -                                        |
| HeimatOrt                     | A   | 100   | -        | -                                        |
| HeimatOrtsteil                | A   | 100   | -        | -                                        |
| HeimatAdresszusatz            | A   | 200   | -        | -                                        |
| HeimatGemeinde                | A   | -     | V        | Verweis auf Tabelle **Gemeinden**        |
| PassNr                        | A   | 100   | -        | -                                        |
| PassGueltigBis                | D   | -     | -        | -                                        |
| VisumNr                       | A   | 100   | -        | -                                        |
| VisumAblaufAm                 | D   | -     | -        | -                                        |
| VisumAusstellungsort          | A   | 300   | -        | -                                        |
| Sozialversicherungsnummer     | A   | 100   | -        | -                                        |
| Aufenthaltsbemerkung          | A   | 300   | -        | -                                        |
| SYNC                          | S   | -     | -        | -                                        |



