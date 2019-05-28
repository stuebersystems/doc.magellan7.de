# Fehlermeldung "Tabelle '' konnte nicht gefunden werden"

Gibt Ihr Bericht beim Aufrufen in MAGELLAN die Meldung "Tabelle '' konnte nicht gefunden werden" aus, wenn Sie nicht als SYSDBA angemeldet sind? 

> #### primary::Hinweis
>
> Wenn dieser Bericht einer unserer Originalberichte (bitte nennen Sie uns den genauen Dateinamen) ist, [lassen Sie es uns bitte wissen](http://support.stueber.de), wir korrigieren es.

Ist es Ihr selbst erstellter oder ein von Ihnen angepasster Bericht, starten Sie den Bericht bitte mit Crystal Reports und öffnen bitte den Punkt `Datei > Berichtsoptionen`. 
Hier darf das Häkchen für `Beim ersten Regenerieren überprüfen` nicht gesetzt sein. Wichtig ist, dass Sie diese Option für den Hauptbericht und für alle Unterberichte überprüfen.
 


![Dieses Häkchen darf für weder für den Bericht, noch für einen Unterbericht gewählt sein ](../images/cr.beim.ersten.regenerieren.png)