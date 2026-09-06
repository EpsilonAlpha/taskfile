# Taskfile

Gemeinsame [Task](https://taskfile.dev/)-Tasks fuer Linux-Server. Die erste
Task fuehrt die regelmaessige APT-Wartung auf Debian- und Ubuntu-Systemen aus:

1. `apt-get update`
2. `apt-get upgrade -y`
3. `apt-get autoremove -y`

## Direkt aus GitHub ausfuehren

Installiere zuerst die aktuelle [Task-Version](https://taskfile.dev/installation/).
Anschliessend kann die Task direkt von GitHub geladen und ausgefuehrt werden:

```sh
task --taskfile https://raw.githubusercontent.com/EpsilonAlpha/taskfile/main/Taskfile.yml apt-maintenance
```

Beim ersten Abruf einer Remote-Taskfile fragt Task, ob der Host vertraut werden
soll. Fuer nichtinteraktive Ausfuehrungen kann dies bewusst bestaetigt werden:

```sh
task --yes --taskfile https://raw.githubusercontent.com/EpsilonAlpha/taskfile/main/Taskfile.yml apt-maintenance
```

Die Task fordert bei Bedarf das `sudo`-Passwort an. Sie ist absichtlich auf
Debian- und Ubuntu-basierte Systeme beschraenkt und bricht auf anderen
Distributionen mit einer klaren Fehlermeldung ab.