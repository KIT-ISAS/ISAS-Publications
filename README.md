# ISAS-Publications
Liste der Publikationen des ISAS.

## Benutzung in Papers
- Overleaf Import: "New File" → "From External URL" → `https://raw.githubusercontent.com/KIT-ISAS/ISAS-Publications/master/ISASPublikationen.bib`
- In LaTeX Präambel:
   - `\usepackage[style=numeric-verb, backend=biber, sorting=none, maxbibnames=20, sorting=none, eprint=false]{biblatex}`
   - Achtung: `style=ieee` ändert die Kapitalisierung wo nicht mit geschweiften Klammern geschützt.
   - `\addbibresource{ISASPublikationen.bib}`
- In LaTeX Dokument: `\printbibliography`
- Siehe auch `test.tex` als einfaches Beispiel

## Benutzung auf Mitarbeiterseite
Auf der ISAS-Publikationsseite (isas.iar.kit.edu/Publications.php) werden die Publikationen nach "Hanebeck" gefiltert. Auf der Mitarbeiterseite kann man sich eine **persönliche Publikationsliste** anlegen, die nach dem eigenen Namen filtert und somit auch eigene Arbeiten, die zuvor an anderen Instituten angefertigt wurden, anzeigen kann.


## Wichtige Dateien
- **ISASPublikationen.bib** : LaTeX bib-file mit den >600 Publikationen des ISAS.
- **ISASPublikationen_laufend.bib** : Neue Einträge zunächst hier hinein, zur leichteren Fehlersuche.
- **test.tex** : LaTeX-Dokument, welches alle Einträge zu Testzwecken zitiert.


## Links
- https://isas.iar.kit.edu/Publications.php
- https://github.com/KIT-ISAS/ISAS-Publications
- https://github.com/KIT-ISAS/bibtexToTable
- https://github.com/FlorianPfaff/bibtex_tools
- https://goo.gl/forms/SjZtQ0oNeip9LFyU2
- https://dbkit.bibliothek.kit.edu/login
- https://github.com/KIT-ISAS/Scopus-API


## Aufgaben des Literatur-Maintainers

1. (TODO DF: Skript einrichten) In Google Forms ein Google Skript einbinden, das dann alles Weitere erledigt. Code: https://github.com/FlorianPfaff/bibtex_tools/blob/main/form_to_bibtex.gs

1. (TODO DF: Formular einrichten) Wenn man dieses Formular "Paperstatus melden" ausfüllt, dann wird automatisch Bibtex-Code an den Maintainer verschickt (leider füllt es nicht jeder aus), der muss dann nur zu Konsistenzzwecken etwas angepasst werden.)

2. BibTeX-Eintrag erstellen bzw. prüfen
   - Chicago-Kapitalisierung: https://capitalizemytitle.com/
   - Name von Prof. Hanebeck exakt als `Uwe D. Hanebeck` geschrieben
   - ggf Kompilieren in `test.tex`

4. Wenn man auf das Repository auf Github pusht, wird automatisch durch eine Github Action die neue Table erzeugt (die auch auf der ISAS HP eingebunden ist).
   - Prüfen ob erfolgreich: https://github.com/KIT-ISAS/ISAS-Publications/commits/master/
   - Ein häufiger Fehler ist, dass der Name von Herrn Hanebeck nicht exakt als `Uwe D. Hanebeck` geschrieben ist. 

5. PDFs muss man auf dem i81server hinterlegen. Den Dateinamen muss man als Attribut im Bibtex-Eintrag einbinden (bspw.   PDF = {IFAC23_Fennel.pdf}, )
   - Hier hinterlegen:
      - Linux: `smb://i81server.iar.kit.edu/WWWMaterial/ISAS-Publikationen/PDF/`
      - Windows: `\\i81server.iar.kit.edu\WWWMaterial\ISAS-Publikationen\PDF`
    
6. Literaturliste auf Server synchronisieren. 
   - Auf Server einloggen: `ssh i81server.iar.kit.edu`
   - (Alternativ PDF hier hinterlegen: `/localhome/isaswebwiki/ISASPublikationen/PDF`)
   - Synchronisieren: `sudo bibTexUpdate.sh`

7. Website prüfen: https://github.com/KIT-ISAS/ISAS-Publications/commits/master/ 

8. Gelegentlich sollte man die Paper auch bei der KIT-Datenbank eintragen (gibt dort ein Formular dafür, leider kann man nur jeden Eintrag einzeln per LaTeX importieren).


## TODO

### Abgleich mit Scopus
- [x] `ISASPublikationen.bib` auf Vollständigkeit und Korrektheit überprüfen
- [x] DOIs und URLs einfügen

### Abgleich mit IEEE Xplore
- [ ] `ISASPublikationen.bib` auf Vollständigkeit und Korrektheit überprüfen
- [ ] DOIs und URLs einfügen

### Abgleich mit KITopen
- [ ] Fehlende Artikel auf KITopen hochladen
- [ ] Postprint-PDFs auf KITopen hochladen
- [ ] KITopen DOI in `ISASPublikationen.bib` eintragen, wenn sonst keine DOI verfügbar

### Weitere Verbesserungen
- [ ] fehlende Postprints einfügen
- [ ] Links überprüfen
- [ ] alle PDF-Dateinamen gleich korrespondierendem Bib-Key
- [ ] JAIF auf neue Links umstellen, wenn verfügbar



