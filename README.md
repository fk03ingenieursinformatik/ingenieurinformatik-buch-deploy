# Ingenieurinformatik 1 – Binder & Notebook Deployment

**Wichtig:** Dieses Repository ist **kein Arbeitsrepository**.

Es dient ausschließlich:

- der **Binder-Anbindung** für interaktive Code-Ausführung auf der Kurs-Website:  
  `https://ingenieurinformatik-buch-fcbc5c.pages.gitlab.lrz.de/intro.html`
- dem **Deployment von Jupyter-Notebooks** für die Nutzung im JupyterHub

Die Inhalte (Markdown / MyST) werden **nicht** in diesem Repository gepflegt.

---

## Zweck dieses Repositories

- **Live-Code auf der Website (Binder)**: Damit Live-Code auf der interaktiven Website ausgeführt werden kann, benötigt Binder eine definierte Laufzeitumgebung. Diese wird automatisch als Container-Image gebaut; die Konfiguration liegt in `binder/`.
  - Hinweis: Für Live-Code werden **keine Notebook-Dateien** benötigt. Ausgeführt wird der Zellcode im von Binder bereitgestellten Jupyter-Kernel im Container; der Browser kommuniziert dabei über das Website-Theme (Sphinx) mit Binder.

- **Fallback: JupyterHub (Notebooks)**: Falls Live-Code nicht verfügbar ist, stellen wir die Inhalte zusätzlich als Jupyter-Notebooks im JupyterHub bereit. Auf der Website ist der HM-JupyterHub bereits verlinkt: `https://datahub.cs.hm.edu/hub/spawn`. Beim Klick auf den JupyterHub-Button wird dieses Repository automatisch in die Nutzerumgebung geklont. Die Notebooks werden automatisch in dieses repository gepushed. Gebaut werden sie im Arbeitsrepo auf gitlab LRZ in der GitLab CI-Pipeline:  
  `https://gitlab.lrz.de/fk03ingenieurinformatik/Ingenieurinformatik-buch/-/pipelines`

## Inhalte & Mitarbeit

**Das eigentliche Arbeitsrepository liegt auf GitLab (HM):**

- Inhaltliche Änderungen
- Korrekturen
- Feedback

Bitte **ausschließlich dort** einreichen:

- Arbeitsrepository (GitLab): `https://gitlab.lrz.de/fk03ingenieurinformatik/Ingenieurinformatik-buch`

---

## Keine Issues / PRs hier

Bitte **keine Issues oder Pull Requests** in diesem GitHub-Repository anlegen.  
Dieses Repository wird **automatisiert verwaltet**.

Vielen Dank!
