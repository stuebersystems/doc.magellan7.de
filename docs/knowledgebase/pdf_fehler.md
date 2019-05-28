# Fehler beim PDF-Export

Stand: 04.01.2016. 
Alle hier gemachten Aussagen repräsentieren den aktuellen Stand der Entwicklung - Irrtümer vorbehalten - und können im Rahmen der Fortentwicklung der Software revidiert werden.

 
## Die Fehlerbeschreibung

Wenn Sie in MAGELLAN im Rahmen des Druckens von Crystal Reports Berichten 
*	gleichzeitig ins PDF-Format exportieren oder
*	aus der Vorschau heraus ins PDF-Format exportieren wollen
können Sie die folgende Fehlermeldung erhalten: 
 
![Fehlermeldung](images/pdf_fehler00.png) 

## Die Ursache

Microsoft hat Ende November 2015 das Serviceupdate KB3102429 für Windows 8.1, Windows RT 8.1, Windows Server 2012 R2, Windows 8, Windows RT, Windows Server 2012, Windows 7 Service Pack 1 (SP1) und Windows Server 2008 R2 SP1 veröffentlicht. 
Mit diesem Serviceupdate wurden unter anderem diverse Schriftarten des Betriebssystems von Microsoft (wie z.B. Arial, Calibri, Segoe, Times) in der Version aktualisiert. Diese Aktualisierung führt in Kombination mit der von uns in MAGELLAN verwendeten Zugriffskomponente für Crystal Reports Berichte zu dem oben beschriebene Fehler. Diese Problemstellung ist Microsoft bekannt.
Bei einer Installation von MAGELLAN unter Microsoft Windows 10 tritt der Fehler mit dem PDF-Export nach unserem Kenntnisstand nicht auf.
Wir müssen nun abwarten, wie Microsoft bzw. SAP (Hersteller von Crystal Reports) auf dieses Problem reagieren.
Aktuell können wir Ihnen die nachfolgende beschriebene Zwischenlösung anbieten, die das Problem zwischenzeitlich behebt.

## Die Zwischenlösung 

Diese Lösung basiert auf der Idee, das Microsoft Serviceupdate KB3102429 zu deinstallieren bzw. für zukünftige Ser-viceupdates von Microsoft auszublenden.
Prüfen Sie dazu zunächst, ob das Microsoft Serviceupdate KB3102429 bereist auf Ihrem Rechner installiert ist. Dazu gehen Sie exemplarisch unter Windows 8 wie folgt vor: 
 
Rufen Sie `Systemsteuerung > Windows Update > Updateverlauf anzeigen` auf.
1.	Prüfen Sie in der Liste, ob Update für Windows 8.1 für x64-Systeme (KB3102429) installiert ist.

![Updateliste](images/pdf_fehler01.png) 
 

### Fall A: Serviceupdate KB3102429 ist installiert

Ist das Serviceupdate bereits installiert, gehen Sie wie folgt vor:
1.	Rufen Sie `Systemsteuerung > Windows Update > Einstellungen ändern` auf.
2.	Wenn unter Wichtige Updates der Wert Updates automatisch installieren eingestellt ist, so müssen die Einstellung ändern auf Updates herunterladen, aber Installation manuell durchführen.

![ Updates herunterladen, aber Installation manuell durchführen](/images/pdf_fehler02.png)  

3.	Gehen Sie zurück auf `Systemsteuerung > Windows-Update`.
4.	Wählen Sie Updateverlauf anzeigen und klicken Sie auf den im oberen Text blau markierten Link `Installierte Updates` (siehe nachfolgende Abbildung).

 ![Installierte Updates](/images/pdf_fehler03.png)  

5.	Markieren Sie den Eintrag Update für Windows 8.1 für x64-Systeme (KB3102429) in der Microsoft Gruppe und klicken Sie auf Deinstallieren, um das Serviceupdate zu deinstallieren.
6.	Starten Sie anschließend den Computer neu
7.	Rufen Sie nach dem Neustart Systemsteuerung > Windows Update > Nach Updates suchen auf.

![ Nach Updates suchen](/images/pdf_fehler04.png)  
 

8.	Das Serviceupdate Update für Windows 8.1 für x64-Systeme (KB3102429) wird erneut als verfügbar angezeigt.

 ![ Wichtiges Update ist verfügbar](/images/pdf_fehler05.png) 

9.	Markieren Sie unter Wichtig den Eintrag Update für Windows 8.1 für x64-Systeme (KB3102429) und wählen Sie über die rechte Maustaste den Menüpunkt Update ausblenden.

  ![ Update ausblenden](/images/pdf_fehler06.png) 

10.	Wenn unter Punkt 2 zuvor unter Wichtige Updates den Wert Updates automatisch installieren eingestellt hat-ten, so müssen diese Einstellung dort wieder auf den ursprünglichen Wert Updates automatisch installieren zu-rückstellen.

Fall B: Serviceupdate KB3102429 ist NICHT installiert
Ist das Serviceupdate noch nicht installiert, so folgen Sie nur den Anweisungen der Punkt 3. – 9. aus dem Fall B.
