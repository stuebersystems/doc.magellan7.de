# Fehler in Crystal Reports 9	 


## Das Problem

In einem selbsterstellten Crystal Reports 8.5 Bericht werden unterschiedliche Tabellen von MAGELLAN  miteinander verknüpft, um die gewünschte Ausgabe im Bericht zu erzielen.
Bei der Verknüpfung kann der Fall eintreten, dass eine Tabelle mehrfach Verwendung findet. Die mehrfach verwendeten Tabellen dürfen dabei nicht den gleichen Namen haben und mit der gleichen Tabelle verknüpft sein. Dazu führt Crystal Reports einen sogenannten ALIAS ein.


Beispiel: 
Um den 1. und 2. Klassenlehrer einer Klasse mit Namen auszugeben, muss man zweimal die Tabelle Lehrer mit der Tabelle KlassenZeitraeume verknüpfen. Standardmäßig erhält die erste Tabelle den gleichen ALIAS wie die Tabelle selbst (LEHRER) und die zweite Verwendung der Tabelle Lehrer zur Unterscheidung einen anderen ALIAS (z.B. LEHRER_1).
  

Die Benennung von mehr als einem ALIAS für eine Tabelle führt bei der Konvertierung nach Crystal Reports 9 genau dann zu einem Fehler, wenn der eine ALIAS keinen Unterstrich enthält (z.B. LEHRER), ein weiterer einen Unterstrich hat (z.B. LEHRER_1) und beide mit der gleichen Tabelle (KlassenZeitraeume) verknüpft sind.

## Die Lösung

Besitzt ein ALIAS für die gleiche Tabelle einen Unterstrich und der andere keinen, so müssen Sie den ALIAS ohne Unterstrich umbenennen. Dabei muss der ALIAS ohne Unterstrich ebenfalls einen Unterstricht erhalten.

Beispiel: 
Sie verwenden für die Tabelle Lehrer den ALIAS LEHRER und LEHRER_1. Führen Sie eine Umbenennung des ALIAS LEHRER in z.B. LEHRER_2 durch, um das Konvertierungsproblem zu beheben. Nach der Umbenennung sind LEHRER_1 und LEHRER_2 mit KlassenZeitraeume verknüpft.
Um die ALIASE in Ihrem Bericht zu überprüfen und ein evtl. Umbenennung vornehmen zu können, gehen Sie wie folgt vor:

1.	Starten Sie Crystal Reports 8.5 oder 9.
2.	Öffnen Sie Ihren Bericht, den Sie bisher verwendet haben.
3.	Rufen Sie 'Datenbank > Alias' festlegen auf.
4.	Durchsuchen Sie die Auflistung der ALIASE nach dem oben beschriebenen Problemfall.
5.	Tritt ein solcher Fall auf, so können Sie über Alias festlegen im Dialogfenster direkt die gewünschte Umbenennung vornehmen.
6.	Besitzt Ihr Bericht auch Unterberichte, so müssen Sie diese Vorgehensweise auch für alle Unterberichte durchführen.

Hinweis: Nach den beschriebenen Änderungen müssen Sie im Menüpunkt „Datenbank“ die Option „Datenbank überprüfen“ durchführen.
