# ISAS-Publications
Liste der Publikationen von Prof. Hanebeck. Verwendung in Publikationsliste auf der Homepage sowie als Bibliothek für neue Papers.


## Important Files
- **ISASPublikationen.bib** : LaTeX bib-file mit den >500 Publikationen des ISAS.
- **ISASPublikationen_laufend.bib** : Neue Einträge zunächst hier hinein, zur leichteren Fehlersuche.
- **test.tex** : LaTeX-Dokument, welches alle Einträge zu Testzwecken zitiert.


## Links
- https://isas.iar.kit.edu/Publications.php
- https://github.com/KIT-ISAS/ISAS-Publications
- https://github.com/FlorianPfaff/bibtex_tools
- https://goo.gl/forms/SjZtQ0oNeip9LFyU2
- https://dbkit.bibliothek.kit.edu/login


## Aufgaben des Literatur-Maintainers

1. In Google Forms ein Google Skript einbinden, das dann alles Weitere erledigt. Code: https://github.com/FlorianPfaff/bibtex_tools/blob/main/form_to_bibtex.gs

1. Wenn man dieses Formular "Paperstatus melden" ausfüllt, dann wird automatisch Bibtex-Code an den Maintainer verschickt (leider füllt es nicht jeder aus), der muss dann nur zu Konsistenzzwecken etwas angepasst werden.

2. Wenn man auf das Repository auf Github pusht, wird automatisch durch eine Github Action die neue Table erzeugt (die auch auf der ISAS HP eingebunden ist).

3. PDFs muss man auf dem i81server hinterlegen. Den Dateinamen muss man als Attribut im Bibtex-Eintrag einbinden (bspw.   PDF = {IFAC23_Fennel.pdf}, )
- - Hier hinterlegen: `smb://i81server.iar.kit.edu/WWWMaterial/ISAS-Publikationen/PDF/`
- - Auf Server einloggen: `ssh i81server.iar.kit.edu`
- - Alternativ hier hinterlegen: `/localhome/isaswebwiki/ISASPublikationen/PDF`
- - Synchronisieren: `sudo bibTexUpdate.sh`

4. Gelegentlich sollte man die Paper auch bei der KIT-Datenbank eintragen (gibt dort ein Formular dafür, leider kann man nur jeden Eintrag einzeln per LaTeX importieren).


## TODO

### Abgleich mit Scopus
- Scopus-API
- Python-Library: https://pybliometrics.readthedocs.io/en/stable/
- Titel überprüfen
- DOIs nachtragen

### Verbesserungen
- Überall Postprints + offizieller Link + DOI
- GitHub Action
- - Validieren des BibTeX Codes
- - Verfügbarkeit des PDFs
- Links überprüfen
- alle PDF-Dateinamen gleich Bib-Key
- PostPrints auf KITopen hochladen





