# Fächer mit hochgestellter Ziffer für einen Verweis auf eine Fußnote 

**Problem: **Ihr Bericht soll hinter Fächern eine hochgestellte Ziffer zeigen, die auf eine Fußnote verweist. Wenn diese Ziffer gezielt nur bei einigen Schülern und auch nur bei einigen Fächern gezeigt werden soll, gehen Sie bitte wie nachstehend beschrieben vor.


**Lösung:**
1. Fügen Sie die Erläuterung  der Fußnote an der gewünschten Stelle im Bericht ein.
2. Erstellen Sie im Bericht folgende Formel für die Ausgabe der Fachbezeichnung. Anstatt die Fachbezeichnung ziehen Sie in die Entwurfsansicht die erstellte Formel. 

> #### warning::Wichtig!
>
> In der nachstehenden Formel wird eine zusätzliche Angabe pro Schülerfachzeile im Feld `Merkmal `erwartet, wenn eine Fachbezeichnung um eine Ziffer ergänzt werden soll.



```
' Das Ergebnis der Formel ist grundsätzlich die Fachbezeichnung
formula = {Faecher.Bezeichnung}

' In den Schülerfachdaten tragen Sie in der Spalte Merkmal 1 (für Hoch1) oder 2 (für Hoch2) ein
if not IsNull({SchuelerFachdaten.Merkmal}) then

  ' Wenn im Merkmal eine 1 steht dann:
  if  ({SchuelerFachdaten.Merkmal} = "1") then
    formula = formula + chr(185)    
  end if

  ' Wenn im Merkmal eine 2 steht dann: 
  if  ({SchuelerFachdaten.Merkmal} = "2") then
    formula = formula + chr(178)    
  end if

end if
```

Die Formel gibt also die Fachbezeichnung eventuell ergänzt um eine hochgestellte Ziffer aus. 
**
Beispiel:**
Wird in Feld `Merkmal` eine 2 gefunden, wird aus "Mathematik" "Mathematik²".


Hier noch einige Ausgaben für Sonderzeichen in Formeln:


| Eingabe            | Anzeige       |
|--------------------|---------------|
| formula = chr(185) | hoch 1        |
| formula = chr(178) | hoch 2        |
| formula = chr(179) | hoch 3        |
| formula = chr(174) | copyright     |
| formula = chr(13)  | Zeilenumbruch |

