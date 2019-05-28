 # Umlaute werden nicht korrekt dargestellt



## Problem 

Beim Seriendruck mit Word kann das Problem auftreten, dass statt des gewünschten Textes eine Folge von Sonderzeichen/Zeichen aus fremden Sprachen (z.B. Chinesisch)gezeigt wird. 

## Lösung

Seit der Version 6.5.31 übergeben wir an Word mit den Datensätzen fest die Information, das von Word der Zeichensatz UTF8 zu verwenden ist.

Hatten Sie vor der 6.5.31 das Problem der "chinesischen Zeichen", war die alte Lösung der Eintrag eines DWORD-Wertes in der Registry. Dieser Eintrag muss bitte entfernt werden.

## Verwenden Sie die 6.5.31 und die Anzeige der Sonderzeichen stimmt dennoch nicht?

Prüfen Sie im Problemfall bitte, ob im Registrierungseditor unter `HKEY_CURRENT_USER \ Software \ Microsoft \ Office \ [VERSIONSNUMMER siehe unten] \ Word \ Options` ein Schlüssel mit dem Namen „DefaultCPG“ (DWORD-WErt mit 4e4 (Hexadezimal) bzw. 1252 (Dezimal)) erfasst wurde. Dieser Wert muss bitte wieder entfernt werden.


| Versionsnummer | Wordversion |
|----------------|-------------|
| -              | -           |
| 9.0            | Word 2000   |
| 10.0           | Word XP     |
| 11.0           | Word 2003   |
| 12.0           | Word 2007   |





