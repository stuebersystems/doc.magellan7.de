# Mehrere Datenbanken auf einem Server

Wenn Sie die Datenbanken mehrerer Schulen auf einem Server zusammen ablegen wollen, sollten Sie die folgenden Punkte beachten.

**Sollten die nachstehenden Punkte dennoch Fragen offen lassen, können Sie uns für eine genauere Beratung beauftragen. Bitte wenden Sie sich für ein Angebot an unsere Office-Team unter `office@stueber.de`.**

## Version

Bitte stellen Sie sicher, dass beide Schulen die selbe Version von MAGELLAN und von Firebird einsetzen.

## Passworte der Nutzer

Die Benutzerkonten sind zum Teil in der MAGELLAN.fdb der Schule angelegt, die verschlüsselten Passworte zu den Benutzern sind in einer zweiten Firebirddatenbank gespeichert die automatisch bei der Installation von Firebird angelegt wurde.  Wenn beide Datenbanken auf einem Rechner liegen, dann gibt es nur eine Firebirdinstallation, damit nur eine Passwortdatenbank (security.fdb). Als erstes sollten Sie sich entscheiden welche der beiden Passwortdatenbanken Sie für den gemeinsamen Server übernehmen wollen. Es richtet sich sicher schlicht nach der Menge der angelegten Nutzer, also die Datenbank mit den meisten Nutzereinträge, deren security.fdb wird mit auf den neuen Server übernommen. Wenn Sie identifiziert haben, welche Schule mehr Nutzer angelegt hat, dann kopieren Sie bitte die security.fdb aus dem Firebirdverzeichnis und legen sie nach der Firebirdinstallation auf dem neuen Serverrechner anstelle der per Installation angelegten security.fdb ab.
Ablagepfad bei Standardinstallation von Firebird: C:\Program Files (x86)\Firebird\Firebird_x_x

Wenn die Schulverwaltungsdatenbanken (MAGELLAN.fdb) übertragen wurde, melden Sie sich an der Datenbank an deren security.fdb sie nicht übernommen haben und tragen die Passworte der Nutzer ein. Dazu klicken Sie bitte in der Benutzerverwaltung die Benutzer nacheinander doppelt an, tragen ein 8-stelliges Passwort (keine Umlaute, kein ß) ein und bestätigen. Durch das Ändern des Passwortes werden die Benutzer der Schulverwaltungsdatenbank damit in die jetzt gemeinsam genutzte Passwortdatenbank.

Ab Version 10 steht Ihnen eine Funktion zur Verfügung, mit deren Hilfe Sie für mehrere Nutzer einer Datenbank parallel zufällige Passworte erstellen können, die in einer CSV-Datei gespeichert werden. In der Datei werden die Kürzel, die Passworte und ggfs. aus die übernommene E-Mailadresse gespeichert. Die Datei kann als Basis für eine Sammel-E-Mail genutzt werden. Nach dem ersten Anmelden an MAGELLAN haben die Nutzer die Möglichkeit über `MAGELLAN > Datenbank > Passwort ändern` ein eigenes Passwort anzulegen.
Bitte schauen Sie unsere Anleitung dazu hier an: [https://doc.magellan.stueber.de/schulverwaltung/admin/users/#passworte-gesammelt-vergeben-und-e-mail-adressen](https://doc.magellan.stueber.de/schulverwaltung/admin/users/#passworte-gesammelt-vergeben-und-e-mail-adressen)

## sysdba und dbadmin

### sysdba

Der `sysdba` gilt als Administrator über alle Datenbanken auf dem Server, also in Ihrem Fall jetzt für beide Schulen, das Passwort sollten Sie ändern (`MAGELLAN Administrator > Benutzerverwaltung > Administratoren`) und den Schulen nicht mehr zur Verfügung stellen.

### dbadmin

Wenn die Schule selbst Nutzer anlegen darf, selbst Schlüssel für die eigene Datenbank importieren darf, also alle administrativen Aufgabe im MAGELLAN Administrator für die eigene Datenbank übernehmen darf, dann richten Sie bitte ein Passwort für den `dbadmin` der Schuldatenbank ein und stellen Sie diese Kennung den Schulen zur Verfügung.
Übrigens könnte somit auch jemand von der Schule die Passworte für die Benutzer anlegen.

### Datenordner

Bei den Datenordnern müssten Sie entscheiden, ob Sie Inhalte von den Schulen gemeinsam verwenden lassen oder es trennen wollen.
Unsere Empfehlung wäre folgende Konstellation, es sind aber sicher noch andere Varianten denkbar:

Muss je Schule existieren (`x` dient hier als Platzhalter für die jeweilige Versionsnummer):

"C:\Users\Public\Documents\Stueber Systems\Magellan x\Dokumente"

Sollten je Schule existieren:

"C:\Users\Public\Documents\Stueber Systems\Magellan x\Berichte"

"C:\Users\Public\Documents\Stueber Systems\Magellan x\Vorlagen"

Können gemeinsam genutzt werden:

"C:\Users\Public\Documents\Stueber Systems\Magellan x\Skripte"

"C:\Users\Public\Documents\Stueber Systems\Magellan x\Importe"

Unser Vorschlag hier wäre auf dem Server die Standardinstallation auszuführen und die Verzeichnis auch an der Stelle zu lassen. Für die schulindividuellen Verzeichnisse erstellen Sie bitte eine Kopie der Verzeichnisse und legen diese doppelt ab. Erstellen Sie jeweils Freigaben für die beiden Schulen. Bei Updates werden diese drei Verzeichnisse so nicht erreicht, was für die Verzeichnisse Dokumente und Vorlagen aber auch nicht nötig ist. Der Ordner Berichte sollte allerdings schon aktualisiert werden. Hier würden wir vorschlagen, dass Sie sich ein Tool zur Synchronisation des Verzeichnisses einrichten und nach dem Update neue oder geänderte Berichtsdateien aus dem Standardordner in die schulindividuellen Ordner zu übertragen.