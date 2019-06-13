# Tabelle SchuelerFoerderungen


| Name              | Typ | Größe | Funkt. | Bemerkung                                |
|-------------------|-----|-------|--------|------------------------------------------|
| Mandant           | I   | -     | PV     | Verweis auf Tabelle **Mandanten**        |
| ID                | I+  | -     | P      | -                                        |
| Schueler          | I   | -     | V      | Verweis auf Tabelle **Schueler**         |
| Behinderung       | A   | -     | V      | Verweis auf Tabelle **Behinderungsarten** |
| Beeintraechtigung | A   | 200   | -      | -                                        |
| Schwerpunkt1      | A   | -     | V      | Verweis auf Tabelle **FoerderSchwerpunkte** |
| Schwerpunkt2      | A   | -     | V      | Verweis auf Tabelle **FoerderSchwerpunkte** |
| Bedarf            | A   | -     | V      | Verweis auf Tabelle **SopaedFoerderungen** |
| Ausgleich         | A   | -     | V      | Verweis auf Tabelle **Nachteilsausgleiche** |
| Stunden1          | N   | -     | -      | -                                        |
| Stunden2          | N   | -     | -      | -                                        |
| Status            | S   | -     | -      | -                                        |
| Von               | D   | -     | -      | -                                        |
| Bis               | D   | -     | -      | -                                        |

