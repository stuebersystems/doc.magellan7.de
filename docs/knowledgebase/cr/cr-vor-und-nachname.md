# Vor- und Nachname in Crystal Reports-Berichten

Vor- und Nachnamen in Crystal Reports Berichten lassen sich mit dieser Formel ausgeben:

```
' Ergebnis ist Vorname
formula = {Schueler.Vorname}

' Wenn Vorname 2 gefüllt, dann Vorname und Vorname 2 zusammensetzen
if ( {Schueler.Vorname2} <> "" ) then
 formula = formula + " " + {Schueler.Vorname2}
end if

' Wenn Namenszusatz gefüllt, dann an bisheriges Ergebnis Namenszusatz anhängen#
if ( {Schueler.Namenszusatz} <> "" ) and ({Schueler.Nachname} <> "") then
  formula = formula + " " + {Schueler.Namenszusatz}
end if

' Abschließend am bisherigen Ergebnis Nachnamen anhängen
formula = formula + " " + {Schueler.Nachname}
```

> #### info::Hinweis
>
> Sollten Sie in Ihrem Bericht in den Berichtsoptionen unter "Allgemeine Einstellungen" den Haken nicht vor "Null Werte in Datenbank zu Standard konvertieren" aktiviert haben, verwenden Sie bitte folgende Formel:  
> ![!\[\]\(/assets/CR.Berichtsoptionen01.png\)](../assets/CR.Berichtsoptionen02.png)

```
' Ergebnis ist Vorname
formula = {Schueler.Vorname}

' Wenn Vorname 2 gefüllt, dann Vorname und Vorname 2 zusammensetzen
if (not IsNull({Schueler.Vorname2})) and ( {Schueler.Vorname2} <> "" ) then
 formula = formula + " " + {Schueler.Vorname2}
end if

' Wenn Namenszusatz gefüllt, dann an bisheriges Ergebnis Namenszusatz anhängen#
if (not IsNull({Schueler.Namenszusatz})) and (not ISNull({Schueler.Nachname})) and ( {Schueler.Namenszusatz} <> "" ) and ({Schueler.Nachname} <> "") then
  formula = formula + " " + {Schueler.Namenszusatz}
end if

' Abschließend am bisherigen Ergebnis Nachnamen anhängen
formula = formula + " " + {Schueler.Nachname}
```



