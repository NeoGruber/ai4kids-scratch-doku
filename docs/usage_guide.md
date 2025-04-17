# Anleitung um Github zu aktualisieren

1. Unter `docs` neues markdown file hinzfügen.
2. Innerhalb der `mkdocs.yml` die neue markdown datei eintragen: 
```
site_name: AI4Kids
nav:
  - Home: index.md
  - Projekt 1: project_1.md
  - Projekt 2: project_2.md
  - Deine neue Seite: foo.md # hier fügst du die Seite hinzu
theme: readthedocs
```
3. Schauen wie es aussieht: `mkdocs serve` und unter `http://127.0.0.1:8000/` ansehen
4. Die Seite builden: `mkdocs build`
5. Auf github pushen: `git add .` und `git commit -m "commit message"` und 
```
mkdocs gh-deploy --config-file ./mkdocs.yml --remote-branch documentation
```
6. Changes auf https://neogruber.github.io/ai4kids-scratch-doku/ ansehen