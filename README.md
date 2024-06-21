# Apache NiFi PoC

Dieses Repository enthält eine Docker-basierte Konfiguration für Apache NiFi als Teil eines Enterprise Integration Layer PoC.

## Konfiguration

### Lokale Verwendung
1. Kopieren Sie die `.env.example` Datei zu `.env`:
```
cp .env.example .env
```

2. Passen Sie die Werte in der `.env` Datei nach Bedarf an.

### Verwendung mit Gitpod

Für die Verwendung mit Gitpod müssen Sie die folgenden Gitpod Secret Variables in Ihren Gitpod-Einstellungen konfigurieren:

- NIFI_WEB_HTTPS_PORT
- NIFI_USERNAME
- NIFI_PASSWORD

So richten Sie Gitpod Secret Variables ein:

1. Gehen Sie zu [https://gitpod.io/variables](https://gitpod.io/variables)
2. Klicken Sie auf "New Variable"
3. Geben Sie den Namen der Variable (z.B. NIFI_USERNAME) und den Wert ein
4. Wählen Sie den Scope (normalerweise Ihr Repository)
5. Wiederholen Sie dies für alle benötigten Variablen

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/flobotde/apache-nifi-poc)

Klicken Sie auf den "Open in Gitpod" Button, um die Umgebung automatisch zu starten. Die .env-Datei wird automatisch aus den Gitpod Secret Variables erstellt.

## Lokale Verwendung

1. Stellen Sie sicher, dass Docker und Docker Compose installiert sind.
2. Klonen Sie dieses Repository.
3. Kopieren Sie `.env.example` zu `.env` und passen Sie die Werte an.
4. Führen Sie `docker-compose up` im Hauptverzeichnis aus.
5. Öffnen Sie https://localhost:8443/nifi in Ihrem Browser.
