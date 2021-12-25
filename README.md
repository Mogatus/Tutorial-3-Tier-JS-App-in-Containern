# Tutorial 3-Tier JS-App in Containern

Ziel: Ein Tutorial, in der möglichst einfach eine JavaScript Applikation erstellt wird, in der verschiedene 
Schichten genutzt werden:

1. DB-Layer auf einer MySQL DB
2. Service-Layer in JS für den Zugriff auf die Datenstrukturen der DB
3. Business Layer für die fachlichen Funktionen als Service
4. HTML-GUI zur Anzeige und Modifikation der Daten

Die Umsetzung soll so erfolgen, dass möglichst wenig Installationen auf dem Entwicklungsrechner notwendig sind. Daher
werden Docker Container eingesetzt.

Inhalt des Tutorials soll die Verwaltung von Kursen beliebiger Aktien oder Kryptowährungen sein.

# Voraussetzungen

1. Unter Windows: WSL 2
2. Docker, bzw. Docker Desktop unter Windows

Anleitung dazu unter https://docs.docker.com/desktop/windows/install/


# Laden der benötigten Docker Images

## Test der Umgebung

Nach erfolgreicher Installation von wsl und Docker sollte sich eine Linux-Konsole starten lassen (Windows "wsl") und docker aufrufbar sein.

## MySQL Image laden und starten

Eine Anleitung zum Laden und Starten von MySQL findet sich auf DockerHub unter https://hub.docker.com/_/mysql
Wir nutzen docker-compose mit einem yaml-File zum Start der DB

YAML-File:
> siehe mysql.yml

Start des Containers mit:
> docker-compose -f mysql.yml up

## JavaScript 