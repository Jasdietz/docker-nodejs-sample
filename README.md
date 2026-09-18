# Docker ToDo-App

## Projektbeschreibung
Diese Applikation ermöglicht es, eine ToDo-Liste lokal laufen zu lassen und zu verwalten. Sie basiert auf Node.js mit Express und speichert die Daten in einer Datenbank.

## Voraussetzungen

-Installieren Sie [Node.js](https://nodejs.org/) oder in PowerShell 
`winget install OpenJS.NodeJS.LTS`
-Installieren Sie [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Kopieren Sie den folgenden Link: https://github.com/ICT-BLJ/docker-nodejs-sample.git

## Repository klonen
Gehen Sie auf das Bash-Terminal und geben Sie den folgenden Link ein:
```bash
git clone <Die-REPO-URL>
cd docker-nodejs-sample
```

## Pakete installieren
Installieren Sie die benötigten Pakete des Projekts:
```bash
npm install
```

## Anwendung lokal starten
Starten Sie die Anwendung lokal:
```bash
npm run dev
```

Die Anwendung läuft standardmässig auf Port 3000 und ist somit unter folgender Adresse erreichbar: http://localhost:3000

## Docker-Image erstellen
Erstellen Sie ein Docker-Image
```bash
docker build -t todo-app .
```

## Anwendung mit Docker starten
Jetzt starten Sie die Applikation mit Docker
```bash
docker run --name todo-container -p 3000:3000 todo-app
```

Die Anwendung läuft standardmässig auf Port 3000 und ist somit unter folgender Adresse erreichbar: http://localhost:3000

## Anwendung mit Docker Compose starten

```bash
docker compose up --build
```

Im Hintergrund starten:

```bash
docker compose up -d
```

## Anwendung stoppen

Ohne Compose:

```bash
docker stop todo-container
docker rm todo-container
```

Mit Compose:

```bash
docker compose down
```
