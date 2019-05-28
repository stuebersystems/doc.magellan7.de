# Personalisieren von Zeugnisbemerkungen in Crystal Reports

Wenn Sie für selbst erstellte Zeugnisberichte die Zeungnisbemerkungen personalisieren möchten, können Sie dafür folgendermaßen vorgehen:

Im Menü `Schüler` unter `Zeugnis > Zeugnis` oder im Menü `Abitur` unter `Zeugnis` können Sie Zeugnisbemerkungen anlegen. Diese Zeugnisbemerkungen können Sie an dieser Stelle direkt eintippen oder zuvor unter `Verzeichnisse > Zeugnisbemerkungen` vordefinierte Zeugnisbemerkungen (auch per Sammelzuweisung) zuordnen.

Man kann diese Zeugnisbemerkungen über Platzhalter auch personalisieren, die Umsetzung der schülerbezognenen Inhalte erfolgt dann im Crystal Reportsbericht selbst. Einen Platzhalter definieren Sie über `<<` zum Beginn und `>>` zum Ende Ihres Platzhalters, z.B. so: `<<hier steht Ihr Platzhalter>>`.  

## Beispiel

`<<Name>>` hat sich ehrenamtlich engagiert. Wir möchten uns bei `<<ihm_ihr>> ` für die tolle Arbeit bedanken.
`Hans Herbert von Müller `hat sich ehrenamtlich engagiert. Wir möchten uns bei `ihm `für die tolle Arbeit bedanken.

Möglich sind:

formula = Replace (formula,"<<Vorname>>" , Vorname)
formula = Replace (formula,"<<VornameV>>" , VornameV)
formula = Replace (formula,"<<Nachname>>" , Nachname)
formula = Replace (formula,"<<NachnameV>>" , NachnameV)
formula = Replace (formula,"<<Name>>" , Name)

Platzhalter     | füllt das Feld in CR mit folgendem Wert
--------------- | -----------
`<<Vorname>>`   | Vorname des Schülers (Beispiel: Hans)
`<<VornameV>>`  | Vorname, Vorname2 (Beispiel: Hans Herbert)
`<<Nachname>>`  | Nachname des Schülers (Beispiel: Müller)
`<<NachnameV>>` | Zusatz und Nachname des Schülers (Beispiel: von Müller)
`<<Name>>`      | Vorname, Vorname2, Namenszusatz und Nachname des Schülers (Beispiel: Hans Herbert von Müller)
`<<Er_Sie>>`    | Er/Sie (je nach Geschlecht des Schülers)
`<<er_sie>>`    | er/sie (je nach Geschlecht des Schülers)
`<<Seine_Ihre>>`|Seine/Ihre (je nach Geschlecht des Schülers)
`<<seine_ihre>>`|seine/ihre (je nach Geschlecht des Schülers)
`<<Ihm_Ihr>> `    |Ihm/Ihr (je nach Geschlecht des Schülers)
`<<ihm_ihr>>  `   |ihm/ihr (je nach Geschlecht des Schülers)
`<<Seinen_Ihren>>`|Seinen/Ihren (je nach Geschlecht des Schülers)
`<<seinen_ihren>>`|seinen/ihren (je nach Geschlecht des Schülers)
`<<DerSchueler_DieSchuelerin>>`|Der Schüler/Die Schülerin (je nach Geschlecht des Schülers)
`<<derSchueler_dieSchuelerin>>`|der Schüler/die Schülerin (je nach Geschlecht des Schülers)
`<<DemSchueler_DerSchuelerin>>`|Dem Schüler/Der Schülerin (je nach Geschlecht des Schülers)
`<<demSchueler_derSchuelerin>>`|dem Schüler/der Schülerin (je nach Geschlecht des Schülers)


## Schritte in Crystal Reports

Zuerst müssen Sie bitte die Tabelle „Schüler“ mit der Tabelle „SchuelerZeugnisbemerkungen“ oder „SchuelerABIZeugnisbemerkungen“  verknüpfen – die Verknüpfungsoption muss `Linke äußere Verknüpfung` sein – siehe Abbildung:

![Der Datenbank-Assistent in Crystal Reports](../images/cr-schuelerzeugnisbemerkungen.jpg)

 
Nun müssen Sie das Feld „SchuelerZeugnisbemerkungen.Bemerkung“ oder „SchuelerABIZeugnisbemerkungen.Bemerkung“ durch folgende Formel ersetzen:

```` 
' Varianten des Namens:
'   1. Vorname   = Hans                        <<Vorname>>
'   2. VornameV  = Hans Peter                  <<VornameV>>  - Neu
'   3. Nachname  = Müller                      <<Nachname>>
'   4. NachnameV = von Müller                  <<NachnameV>> - Neu
'   5. Name      = Hans Peter von Müller       <<Name>>      - Neu


dim Vorname as string
dim VornameV as string
dim Nachname as string
dim NachnameV as string
dim Name as string


' Variante 1:
Vorname = {Schueler.Vorname}

' Variante 2:
if not isnull({Schueler.Vorname2}) then
    VornameV = Vorname + " " + {Schueler.Vorname2}
end if

' Variante 3:
Nachname = {Schueler.Nachname}

' Variante 4: 
if not isnull({Schueler.Namenszusatz}) then
    NachnameV = {Schueler.Namenszusatz} + " " + Nachname
end if

' Variante 5:
Name = VornameV + " " + NachnameV


formula = {SchuelerZeugnisbemerkungen.Bemerkung}

if ("<<" in formula) then
    formula = Replace (formula,"<<Vorname>>" , Vorname)
    formula = Replace (formula,"<<VornameV>>" , VornameV)
    formula = Replace (formula,"<<Nachname>>" , Nachname)
    formula = Replace (formula,"<<NachnameV>>" , NachnameV)
    formula = Replace (formula,"<<Name>>" , Name)

    if not isnull({Schueler.Geschlecht}) and {Schueler.Geschlecht} = "M" then
        formula = Replace (formula,"<<Er_Sie>>" ,"Er")    
        formula = Replace (formula,"<<er_sie>>" ,"er")
        formula = Replace (formula,"<<Seine_Ihre>>" ,"Seine")            
        formula = Replace (formula,"<<seine_ihre>>" ,"seine")
        formula = Replace (formula,"<<Ihm_Ihr>>" ,"Ihm")
        formula = Replace (formula,"<<ihm_ihr>>" ,"ihm")
        formula = Replace (formula,"<<Seinen_Ihren>>" ,"Seinen")
        formula = Replace (formula,"<<seinen_ihren>>" ,"seinen")
        formula = Replace (formula,"<<DerSchueler_DieSchuelerin>>" ,"Der Schüler")
        formula = Replace (formula,"<<derSchueler_dieSchuelerin>>" ,"der Schüler")
        formula = Replace (formula,"<<DemSchueler_DerSchuelerin>>" ,"Dem Schüler")
        formula = Replace (formula,"<<demSchueler_derSchuelerin>>" ,"dem Schüler")

    elseif not isnull({Schueler.Geschlecht}) and {Schueler.Geschlecht} = "W" then
        formula = Replace (formula,"<<Er_Sie>>" ,"Sie")    
        formula = Replace (formula,"<<er_sie>>" ,"sie")
        formula = Replace (formula,"<<Seine_Ihre>>" ,"Ihre")
        formula = Replace (formula,"<<seine_ihre>>" ,"ihre")
        formula = Replace (formula,"<<Ihm_Ihr>>" ,"Ihr")
        formula = Replace (formula,"<<ihm_ihr>>" ,"ihr")
        formula = Replace (formula,"<<Seinen_Ihren>>" ,"Ihren")
        formula = Replace (formula,"<<seinen_ihren>>" ,"ihren")
        formula = Replace (formula,"<<DerSchueler_DieSchuelerin>>" ,"Die Schülerin")
        formula = Replace (formula,"<<derSchueler_dieSchuelerin>>" ,"die Schülerin")
        formula = Replace (formula,"<<DemSchueler_DerSchuelerin>>" ,"Der Schülerin")
        formula = Replace (formula,"<<demSchueler_derSchuelerin>>" ,"der Schülerin")
    end if
End if


````
