# Vor- und Nachname in Crystal Reports-Berichten

Vor- und Nachnamen in Crystal Reports Berichten lassen sich mit dieser Formel ausgeben:

```
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
VornameV = {Schueler.Vorname}

' Variante 2:
if ({Schueler.Vorname2} <> "") then
    VornameV = Vorname + " " + {Schueler.Vorname2}
end if

' Variante 3:
Nachname = {Schueler.Nachname}
NachnameV = {Schueler.Nachname}

' Variante 4: 
if ({Schueler.Namenszusatz} <> "") then
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

    if ({Schueler.Geschlecht}<> "") and {Schueler.Geschlecht} = "M" then
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

    elseif ({Schueler.Geschlecht}<> "") and {Schueler.Geschlecht} = "W" then
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
```


!!! warning "Wichtig"

    Sollten Sie in Ihrem Bericht in den Berichtsoptionen unter "Allgemeine Einstellungen" den Haken nicht vor "Null Werte in Datenbank zu Standard konvertieren" aktiviert haben, verwenden Sie bitte die nachstehende Formel.  

![Nullwerte in Datenbank zu Standard konvertieren](/assets/images/knowledgebase/CR.Berichtsoptionen02.png)





