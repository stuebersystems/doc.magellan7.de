#	Schüler-Kurswahlen von Untis übernehmen
In der Stundenplansoftware werden die Schüler Kursen zugeordnet, z.B. wird die Schüler Fachwahl „Deutsch“ durch die Kursangabe ergänzt, indem die Kursnummer zugeordnet wird, Z.B. „D2“. D.h. diese Schuler-Kurszuordnungen müssen wieder aus der Stundenplansoftware nach MAGELLAN übernommen werden.

Um die Schüler-Kurswahlen aus Untis nach MAGELLAN zu übertragen müssen Sie in zwei Schritten vorgehen
**
1.	Schuldatentransferdatei aus Untis exportieren: **In Untis muss die Schüler-Kurswahlen in eine Schuldatentransferdatei exportiert werden.
2.	**Schuldatentransferdatei nach MAGELLAN importieren: **Die von Untis erzeugte Schuldatentransferdatei muss in MAGELLAN importiert werden.

Diese beiden Schritte sind in den nachfolgenden Abschnitten ausführlich erklärt.


> #### warning::Wichtig!
>
>  Im Folgenden wird die Datenübergabe aus dem Stundenplanprogramm Untis beschrieben. Für DAVINCI gilt die analoge Vorgehensweise. 


##	Schuldatentransferdatei aus Untis exportieren

> #### warning::Wichtig!
>
> Bitte vergewissern Sie sich, dass in Untis das Bundesland "Berlin" gewählt ist.

So können Sie in Untis eine Schuldatentransferdatei exportieren:

1.	Starten Sie Untis und wählen Sie dort `Datei > Import/Export > Deutschland > Schuldatentransferformat`.
2.	Geben Sie im Dialogfenster `Schuldatentransferformat `auf der Registerkarte `Export `unter Exportdatei die Exportdatei im Schuldatentransferformat an.
 
![Dialogfenster für den Export nach MAGELLAN in Untis](/images/berlin/von.untis/von.untis1.png)

3.	Klicken Sie auf `Exportieren `um den Export auszuführen.

##	Schuldatentransferdatei nach MAGELLAN importieren
Durch den Import der zuvor aus Untis erzeugten Schuldatentransferdatei können folgende Daten für die Oberstufe aus Untis nach MAGELLAN übernommen werden:

Was |Anmerkung
---|---
Schüler-Kurswahlen|Die in Untis gewählte Kurszuordnung kann für jeden Schüler für den aktuellen Zeitraum übernommen werden.
Lehrer-Unterricht|Neben der eigentlichen Kurszuordnung kann auch der Lehrer-Unterricht für jeden Schüler übernommen werden

So starten Sie in MAGELLAN den Import der aus Untis erzeugten Schuldatentransferdatei
1.	Wählen Sie `Extras > Import > Untis`.
 
![Startansicht des Assistenten für den MAGELLAN-Datenaustausch mit Untis](/images/berlin/von.untis/von.untis2.png)

2.	Klicken Sie im "MAGELLAN-Datenaustausch mit Untis"-Assistenten auf `Weiter`.
3.	Wählen Sie unter` Übertrage Daten aus folgender SDTF-Datei` die zuvor aus Untis exportierte Schuldatentransferdatei aus. Die Felder Zeitraum und Mandant sind bereits vorbesetzt. Klicken Sie auf `Weiter`.
 
![Hier wählen Sie die aus Untis exportierte Schuldatentransferdatei aus.](/images/berlin/von.untis/von.untis3.png)

4.	Sie müssen jetzt entscheiden was Sie importieren wollen. 
 
![Sie müssen jetzt festlegen, was Sie importieren wollen.](/images/berlin/von.untis/von.untis4.png)

Durch den Import der zuvor aus Untis erzeugten Schuldatentransferdatei können folgende Daten für die Oberstufe aus Untis nach MAGELLAN übernommen werden:

Was |Anmerkung
---|---
Schüler-Kurswahlen| Die in Untis gewählte Kurszuordnung kann für jeden Schüler für den aktuellen Zeitraum übernommen werden.
Lehrer-Unterricht|Neben der eigentlichen Kurszuordnung kann auch der Lehrer-Unterricht für jeden Schüler übernommen werden

Beide Möglichkeiten werden in den beiden nachfolgenden Abschnitten „Schüler-Kurswahlen übernehmen“ und „Lehrer-Unterricht importieren“ näher erläutert.

##	Schüler-Kurswahlen übernehmen
Um die Schüler-Kurswahlen aus Untis zu importieren, müssen Sie müssen Sie im Assistenten für den MAGELLAN-Datenaustausch mit Untis die Option Übernehme Schülerkurswahlen und standardmäßig die Variante` Alle Daten` markieren.

### Import ohne weitere Zusatzoptionen
 
![ Datenimport nach MAGELLAN mit der Standardoption „alle Daten“ ohne weitere Zusatzoptionen](/images/berlin/von.untis/von.untis5.png)

Wenn Sie keine weiteren Zusatzoptionen auswählen, erfolgt die Übernahme der Schülerkurswahlen nach folgender Regel: 

Wird der in Untis vorhandene Schüler in MAGELLAN gefunden, so werden diesem Schüler unter Ansicht `„Schüler“ > Zeugnis > Fächer` alle seine bestehenden Einträge gelöscht und diese durch die Werte aus Untis ersetzt. Dabei werden die nachfolgenden Werte 

*	Fach,
*	Unterrichtsart,
*	Fachstatus,
*	Kursummer und
*	Position

in der unter Ansicht `„Schüler“ > Zeugnis > Fächer` pro erkanntem Schüler neu gefüllt.

Ansicht „Schüler  > Zeugnis > Fächer“ je Schüler|Nach MAGELLAN übernommen|SDTF-Datensatz P1 Feld 
---|---|---
Fach	|Neu	|Feld 21: Fachkürzel
Unterrichtsart	|Neu	|Feld 34: Unterrichtsart-Kürzel
Fachstatus|	Neu	|Feld 35: Fachstatus-Kürzel
Kursummer	|Neu|	Feld 33: Kursnummer
Position	|Neu	|Wird automatisch inkrementell errechnet nach der Reihenfolge der importierten Fächer

Tabelle 2: Wertübernahmen je Schüler nach MAGELLAN wenn nur die Schülerkurswahlen übernommen werden ohne Lehrer-Unterricht in der Schuldatentransferdatei (SDTF)


### Import mit „Übertrag auch in die Fachwahlen“

Wenn Sie die Zusatzoption `Übertrag auch in die Fachwahlen` auswählen, werden die Einträge unter Ansicht `„Abitur“ > Fachwahl` pro erkanntem Schüler zusätzlich aktualisiert. 
**Dabei gelten folgende Regeln:** ist das zu übertragende Fach mit seiner Unterrichtsart bereits in der Fachwahl in MAGELLAN vorhanden, so wird die gesamte Fachzeile mit den neuen Werte aus Untis überschrieben. Andernfalls wird eine neue Fachzeile mit den Werten aus Untis eingefügt.
 
![Datenimport nach MAGELLAN mit der Zusatzoption „Übertrag auch in die Fachwahlen“](/images/berlin/von.untis/von.untis6.png)

> #### primary::Hinweis
>
> Ist unter `Extras > Optionen > Einstellungen` die Option `Abgleich Qualifikation/Fachwahl im Abitur` aktiviert, werden die Aktualisierung unter Ansicht `„Abitur“ > Fachwahl` mit der Registerkarte Ansicht `„Abitur“ > Qualifikation` abgeglichen.

### Import mit „Bestehende Schülerkurswahlen zuvor nicht löschen“
Wenn Sie die Zusatzoption Bestehende Schülerkurswahlen zuvor nicht löschen auswählen, werden die Einträge unter Ansicht `„Schüler“ > Zeugnis > Fächer` pro erkanntem Schüler vor dem eigentliche Import nicht gelöscht. 

> #### primary::Hinweis
>
> Die Datenübernahme der Schülerdaten über `Übernehme Schülerkurswahlen` mit der Option `Alle Daten` und der Zusatzoption `bestehende Schülerkurswahlen nicht zuvor löschen` ist die empfohlene Einstellung für die Übernahme aus Untis.
Für die Aktualisierung der Einträge unter Ansicht` „Schüler“ > Zeugnis > Fächer` gelten dann folgende Regeln:
 
 Was|Bedeutung
 ---|---
Ansicht `„Schüler“  > Zeugnis > Fächer`|	Es werden folgende Werte aus der Stundenplansoftware nach MAGELLAN übernommen
Fach mit der Unterrichtsart ist bereits vorhanden	|- Fachstatus (Schlüssel)<br/>- Kursnummer (<kein Eintrag  >  , 0, 1, 2…)  
Fach mit der Unterrichtsart ist neu |-	Fach (Kürzel und Schlüssel)<br/>- Unterrichtsart (Schlüssel)<br/>- Fachstatus (Schlüssel)<br/>- Kursnummer (<kein Eintrag  >  , 0, 1, 2…)<br/>- Position (0, 1, 2…)

 
![Datenimport nach MAGELLAN mit der Zusatzoption „Bestehende Schülerkurswahlen zuvor nicht löschen“.
Import mit „Fehlende Klasse anlegen“](/images/berlin/von.untis/von.untis7.png)

Mit der Zusatzoption können Klassen automatisch in MAGELLAN angelegt werden, wenn diese Untis neu angelegt wurden aber noch nicht in MAGELLAN existieren. Der mit aus Untis übertragene Schüler wird aber noch nicht mit seiner Kurswahl importiert, da er zuerst in MAGELLAN angelegt und in diese neue angelegte Klasse in MAGELLAN eingeschult werden muss.
 
![Datenimport nach MAGELLAN mit der Zusatzoption „Fehlende Klassen anlegen“.](/images/berlin/von.untis/von.untis8.png)

> #### primary::Hinweis
>
> Klassen wie auch Schüler sollten grundsätzlich in MAGELLAN angelegt sein, da MAGELLAN hierzu das führende System ist.

### Import mit „Nur geänderte Daten“
Mit der Option Nur geänderte Daten werden nur solche die Schüler für den Import berücksichtigt, deren Daten sich zwischen MAGELLAN und der zu importierenden Schuldatentransferdatei in der Kurswahl unterscheiden. Die Unterscheidung erfolgt auf Basis der Unterschiede 

*	in der Fachkombinationsnummer oder
*	oder in der Kombination aus Fach, Unterrichtsart, Fachstatus, Kursummer, Schwerpunkt und Merkmal 

Zur Berücksichtigung reicht ein einzigen solcher Unterschied aus.
 
![Datenimport nach MAGELLAN mit der Option „Nur geänderte Daten“.](/images/berlin/von.untis/von.untis9.png)

### Lehrer-Unterricht importieren

Der Lehrer-Unterricht ist die Zuordnung, welche Lehrer in welcher Klasse welches Fach bzw. welchen Kurs unterrichtet. Um den Lehrer-Unterricht aus Untis nach MAGELLAN zu importieren, müssen Sie im Assistenten für den MAGELLAN-Datenaustausch mit Untis die Option `Übernehme Lehrer-Unterricht` markieren.
  
 ![Die Übernahme des Lehrer-Unterrichts aus Untis nach MAGELLAN ist aktiviert.](/images/berlin/von.untis/von.untis10.png)
 
Bei der Übernahme des Lehrer-Unterrichts aus Untis werden durch den Import der Schuldatentransferdatei nach MAGELLAN aufgrund der Veranstaltungsliste pro Klasse in Untis die Lehrer übernommen. Es werden bei allen Schülern einer Klasse, die Fächer in MAGELLAN haben, die in der Schuldatentransferdatei zugeordneten Lehrer der gleichen Klasse zugeordnet. 

Durch die Übernahme des Lehrer-Unterrichts wird pro Schüler unter Ansicht `„Schüler“ > Zeugnis > Fächer` jedem Fach der unterrichtende Fachlehrer aus Untis zugeordnet. 

Dabei prüft MAGELLAN nach folgender Regel: 

Unterrichtet der Lehrer 
*	das gleich Fach mit
*	gleicher Unterrichtsart,
*	gleichem Fachstatus und 
*	gleicher Kursnummer in
*	der gleiche Klasse,

so wird er dem Schüler in diesem Fach zugeordnet.
Der Lehrer-Unterrichts kann selbstverständlich nur bei den Schülern in MAGELLAN zuordnet werden, denen bereits Fächer zugeordnet wurden.
 

Ansicht „Schüler  > Zeugnis > Fächer“ je Schüler|	Nach MAGELLAN übernommen	|SDTF-Datensatz U1 Feld 
---|---|---
Lehrer	|Aktualisieren	|Feld 4: Lehrerkürzel

Tabelle 3: Wertübernahme je Schüler nach MAGELLAN wenn der Lehrer-Unterricht übernommen wird in der Schuldatentransferdatei (SDTF)

> #### primary::Hinweis
>
> 	Es wird nicht nur der Lehrer-Unterricht der Oberstufe abgeglichen  Die Übernahme des Lehrer-Unterrichts erfolgt nicht nur für die Oberstufen-Klassen sondern für alle Klassen des gewählte Import-Zeitraums.
>
> Die Übernahme des Lehrer-Unterrichts und der Schülerkurswahlen kann in einem Importschritt erfolgen.


## Nachträgliches Ändern von Kursen in Untis
Sie können in Untis bei Bedarf die Zuordnung von Kursen für ein gewähltes Fach vornehmen. Beispielweise können bereits alle Kurswahlen der Schüler von Untis nach MAGELLAN übertragen worden sein. Anschließend muss aber eine Korrektur der Kurszuordnung bei bestimmten Schülern vorgenommen werden.

Der Schüler kann beispielsweise aus dem Leistungskurs Deutsch 1 (Darstellung in Untis: De_LK_1) herausgenommen werden und de, Leistungskurs Deutsch 2 (Darstellung in Untis: DE_LK_2) zugeordnet werden.

In diesem Fall erfolgt der Export analog der Beschreibung im vorangehenden Kapitel „Schüler-Kurswahlen von Untis “.

## Logik bei Import der Exportdatei aus Untis
Im Rahmen des Imports der aus Untis exportierten Schuldatentransferdatei nach MAGELLAN wird unter anderem der Zeilentyp P1 des Schuldatentransferformats bei der Übernahme der Schülerkurswahlen ausgewertet. Dabei gilt folgende Logik für den Import der Kombination der Felder „Fachkürzel“, „Unterrichtsart Kürzel“ und „Kursnummer“ im Zeilentyp P1:

### Identifkation einer bereits vorhandenen Schüler-Fachwahl 
Eine Schüler-Fachwahl in MAGELLAN ist vorhanden unter Ansicht `Abitur > Fachwahl` bzw. unter Ansicht `Schüler > Zeugnis > Fächer`, wenn das Fach (=“Fach-Kürzel“ im Zeilentyp P1) und die zugehöriger Unterrichtsart (=“Unterrichtsart-Kürzel“ im Zeilentyp P1) als Zeile vorhanden ist. 

### Import der Kombination [Fach, Unterrichtsart, Kursnummer=-1]

Import mit Option „Alle Daten“ und…|	Beschreibung
---|---
ohne weitere Optionen	|Das Fach wird nicht beim Import berücksichtigt.Bestehende Schülerkurswahlen nicht zuvor löschen	|Das Fach wird nicht beim Import berücksichtigt.
Übertrag auch in die Fachwahlen	|Das Fach wird unter Ansicht Abitur > Fachwahl des Schülers neu eingetragen, falls die Fach dort noch nicht vorhanden ist.

### Import der Kombination [Fach, Unterrichtsart, Kursnummer=<kein Eintrag  >  ]


Import mit Option „Alle Daten“ und…|	Beschreibung
---|---
ohne weitere Optionen|	Nach dem Löschen der Fächer des Schülers unter Ansicht `Schüler > Zeugnis > Fächer`, wird das Fach mit seiner Unterrichtsart unter Ansicht `Schüler > Zeugnis > Fächer` mit einer leerer Kursnummer eingefügt.
Bestehende Schülerkurswahlen nicht zuvor löschen |Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` vorhanden, so werden für diesen Eintrag die Werte Fachstatus und Kurs mit den importierten Daten überschrieben. Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` nicht vorhanden, so wird das Fach beim Schüler neu eingefügt.
Übertrag auch in die Fachwahlen|Nach dem Löschen der Fächer des Schülers wird geprüft, ob das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` vorhanden ist. Ist dies der Fall so werden für diesen Eintrag die Werte Fachstatus und Kurs mit den importierten Daten überschrieben. Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` nicht vorhanden, so wird das Fach beim Schüler neu eingefügt. <br/><br/>Zusätzlich wird das Fach wird unter Ansicht Abitur > Fachwahl des Schülers neu eingetragen, falls die Fach dort noch nicht vorhanden ist.
Übertrag auch in die Fachwahlen<br/><br/>Bestehende Schülerkurswahlen nicht zuvor löschen|Import „Alle Daten“ ": Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer `vorhanden, so werden für diesen Eintrag die Werte Fachstatus und Kurs mit den importierten Daten überschrieben. Ist das Fach beim Schülers unter Ansicht S`chüler > Zeugnis > Fächer` nicht vorhanden, so wird das Fach beim Schüler neu eingefügt. <br/>Zusätzlich wird das Fach wird unter Ansicht `Abitur > Fachwahl `des Schülers neu eingetragen, falls die Fach dort noch nicht vorhanden ist.


### Import der Kombination [Fach, Unterrichtsart, Kursnummer=0,1,2…]

Import mit Option „Alle Daten“|	Beschreibung
---|---
ohne weitere Optionen|	“ Nach dem Löschen der Fächer des Schülers unter Ansicht` Schüler > Zeugnis > Fächer`, wird das Fach mit seiner Unterrichtsart unter Ansicht `Schüler > Zeugnis > Fächer` mit der Kursnummer eingefügt.
Bestehende Schülerkurswahlen nicht zuvor löschen|Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` vorhanden, so werden für diesen Eintrag die Werte Fachstatus und Kurs mit den importierten Daten überschrieben. Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` nicht vorhanden, so wird das Fach beim Schüler neu eingefügt.
Übertrag auch in die Fachwahlen|Nach dem Löschen der Fächer des Schülers wird geprüft, ob das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` vorhanden ist. Ist dies der Fall so werden für diesen Eintrag die Werte Fachstatus und Kurs mit den importierten Daten überschrieben. Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` nicht vorhanden, so wird das Fach beim Schüler neu eingefügt. <br/><br/>Zusätzlich wird das Fach wird unter Ansicht `Abitur > Fachwahl` des Schülers neu eingetragen, falls die Fach dort noch nicht vorhanden ist.
Übertrag auch in die Fachwahlen<br/><br/>Bestehende Schülerkurswahlen nicht zuvor löschen|Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` vorhanden, so werden für diesen Eintrag die Werte Fachstatus und Kurs mit den importierten Daten überschrieben. Ist das Fach beim Schülers unter Ansicht `Schüler > Zeugnis > Fächer` nicht vorhanden, so wird das Fach beim Schüler neu eingefügt.<br/>Zusätzlich wird das Fach wird unter Ansicht `Abitur > Fachwahl` des Schülers neu eingetragen, falls die Fach dort noch nicht vorhanden ist.


