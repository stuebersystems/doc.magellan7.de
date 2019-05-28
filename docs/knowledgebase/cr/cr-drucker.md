# Standarddrucker für CR-Berichte

Ihr Bericht soll beim Druck den Standarddrucker des Rechners wählen? 
Wenn Sie einen Bericht mit MAGELLAN verwenden, wird in der Regel der Standarddrucker des Rechners gewählt. Diese Einstellung wird nicht durch MAGELLAN selbst voreingestellt, sondern über die integrierte Runtimeversion von Crystal Reports wird die Einstellung im Bericht gelesen.

**Welches Problem kann entstehen?** Meist ist der bei der Erstellung des Berichtes vorhandene Standarddrucker des Rechners eingestellt. Das stellt in vielen Fällen kein Problem dar, da dieser Drucker dann auf dem Rechner, auf dem Sie den Bericht verwenden, nicht verfügbar ist und alternativ der Standarddrucker des Rechners verwendet wird.
Ist aber auf dem Rechner, auf dem der Bericht erstellt wurde, zum Beispiel der XPS-Document Writer von Mircosoft voreingestellt, wird dieser dann auch später auf den Bericht-ausführenden Rechnern gefunden und immer verwendet.
Um das von vornherein auszuschließen sollten Sie in Ihren Berichten bitte folgenden Einstellung wählen:

1. Starten Sie den Bericht mit Crystal Reports!
2. Öffnen Sie `Datei > Seite einrichten > Druckeroptionen` und setzen bitte das Häkchen für `Kein Drucker (für die Bildschirmanzeige optimieren)`! 

![Wählen Sie diese Option um immer den Standarddrucker für den Druck zu verwenden!](../images/cr-drucker.png)

