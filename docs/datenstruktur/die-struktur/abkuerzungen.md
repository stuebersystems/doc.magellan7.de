#	Abkürzungen

Das nächste Kapitel listet alle relevanten Tabellen und Ansichten und deren Felder auf. Die einzelnen Felder besitzen einen Namen, einen Datentyp und evtl. eine Größenangabe. Folgende Datentypen werden in der Datenbank verwendet:

Kürzel	|Allgemeine Beschreibung|	Technische Beschreibung
---|---|---
A	|Textfeld mit fixer Länge|	Textfeld [Flag]
B	|Binärdaten	|Blob-Feld
D	|Datumsangabe	|Date-Feld
DT|	Datumzeitangabe	|DateTime-Feld
I|	Ganze Zahl	|32-Bit-Integer [Bigint]
I+	|Ganze Zahl 	|64-Bit-AutoInc-Integer [ID]
L	|Ja/Nein|	Textfeld der Größe 1 mit den möglichen Werten „J“ oder „N“
M|	Textfeld mit variabler Länge|	Memofeld
N|	Kommazahl|	Numeric [Numeric1804]
S|	Ganze Zahl|	16-Bit-Integer [Smallint]
T|	Zeitangabe|	Time-Feld

Einige Felder haben auch eine bestimmte Funktion innerhalb der Tabelle oder Ansicht. Diese Funktion wird ebenfalls durch ein Kürzel gekennzeichnet:

Kürzel|	Beschreibung
---|---
P	|Primärindex: Die P-Felder in einer Tabelle/Ansicht dienen zur eindeutigen Unterscheidung eines Datensatzes
V	|Verweis: Dieses Feld verweist auf einen Datensatz in einer anderen Tabelle/Ansicht
