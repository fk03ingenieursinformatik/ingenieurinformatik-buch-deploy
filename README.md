# Ingenieurinformatik-buch – Deployment

**Dieses Repository ist kein Arbeits-Repository. Es wird automatisiert verwaltet und dient ausschließlich dem Deployment.**

Das Arbeits-Repository befindet sich im [Ingenieurinformatik-buch repository auf GitLab (LRZ)](https://gitlab.lrz.de/fk03ingenieurinformatik/Ingenieurinformatik-buch). Dort werden Inhalte der interaktiven Website bzw. des Skripts gepflegt.

Dieses repository dient ausschließlich:

- der Binder-Anbindung für interaktive Code-Ausführung auf der Kurs-Website: [Ingenieurinformatik 1](https://ingenieurinformatik-buch-fcbc5c.pages.gitlab.lrz.de/intro.html)
- dem Deployment von Jupyter-Notebooks für die Nutzung im JupyterHub


## Zweck und Funktionsweise

### Live-Code auf der Website (Binder)

Damit Live-Code auf der interaktiven Website ausgeführt werden kann, benötigt Binder eine definierte Laufzeitumgebung. Diese wird automatisch als Container-Image erstellt; die Konfiguration liegt in `binder/`.

Hinweis: Für Live-Code werden keine Notebook-Dateien benötigt. Ausgeführt wird der Zellcode in dem von Binder bereitgestellten Jupyter-Kernel im Container; der Browser kommuniziert über das Website-Theme (Sphinx) mit Binder.

### Fallback: JupyterHub (Notebooks)

Falls Live-Code nicht verfügbar ist, werden die Inhalte zusätzlich als Jupyter-Notebooks im JupyterHub bereitgestellt: [JupyterHub FK07 (HM)](https://datahub.cs.hm.edu/hub/spawn).

Ablauf beim Klick auf den JupyterHub-Button auf der Website:

- Weiterleitung zum JupyterHub der Hochschule München
- Anmeldung über Shibboleth
- Öffnen des Notebooks, das zur aktuellen Seite gehört

Technisch wird das dadurch ermöglicht, dass dieses Deployment-Repository automatisiert auf dem JupyterHub geklont wird und das passende Notebook per URL-Redirect ausgewählt wird.

Bereitstellung der Notebooks:

- Build im Arbeits-Repository per CI-Pipeline (aus Markdown/MyST werden Notebooks generiert)
- Die generierten Notebooks werden anschließend automatisch in dieses Repository gepusht.

## Inhalte & Mitarbeit

Das eigentliche Arbeits-Repository liegt auf GitLab (LRZ).

- Inhaltliche Änderungen
- Korrekturen
- Feedback

Bitte ausschließlich dort einreichen: [Issue erstellen](https://gitlab.lrz.de/fk03ingenieurinformatik/Ingenieurinformatik-buch/-/issues)

**Bitte keine Issues oder Pull Requests in diesem GitHub-Repository anlegen!**

Vielen Dank!
