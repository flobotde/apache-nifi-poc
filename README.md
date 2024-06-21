# Apache NiFi PoC

Dieses Repository enthält eine Docker-basierte Konfiguration für Apache NiFi als Teil eines Enterprise Integration Layer PoC.

## Verwendung mit Gitpod

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/flobotde/apache-nifi-poc)

### Einrichtung der Gitpod Secret Variables

Bevor Sie den "Open in Gitpod" Button verwenden, müssen Sie folgende Secret Variables in Ihren Gitpod-Einstellungen konfigurieren:

1. NIFI_WEB_HTTPS_PORT (z.B. 8443)
2. NIFI_USERNAME (Ihr gewünschter Benutzername für NiFi)
3. NIFI_PASSWORD (Ihr Passwort für NiFi, mindestens 12 Zeichen lang)
4. NIFI_KEYSTORE_PASSWORD (Passwort für den Keystore, mindestens 12 Zeichen)
5. NIFI_KEY_PASSWORD (Passwort für den privaten Schlüssel, mindestens 12 Zeichen)
6. NIFI_TRUSTSTORE_PASSWORD (Passwort für den Truststore, mindestens 12 Zeichen)

So richten Sie Gitpod Secret Variables ein:

1. Gehen Sie zu [https://gitpod.io/variables](https://gitpod.io/variables)
2. Klicken Sie auf "New Variable"
3. Geben Sie den Namen der Variable (z.B. NIFI_WEB_HTTPS_PORT) und den Wert ein
4. Wählen Sie den Scope (normalerweise Ihr Repository)
5. Wiederholen Sie dies für alle benötigten Variablen

Nachdem Sie diese Variablen eingerichtet haben, klicken Sie auf den "Open in Gitpod" Button, um die Umgebung automatisch zu starten.

## Lokale Verwendung

1. Stellen Sie sicher, dass Docker und Docker Compose installiert sind.
2. Klonen Sie dieses Repository.
3. Kopieren Sie `.env.example` zu `.env` und passen Sie die Werte an:
```
cp .env.example .env
```

4. Bearbeiten Sie die `.env`-Datei und setzen Sie die oben genannten Variablen.
5. Führen Sie `docker-compose up` im Hauptverzeichnis aus.
6. Öffnen Sie https://localhost:8443/nifi in Ihrem Browser (ersetzen Sie 8443 durch den von Ihnen gewählten Port).

## Sicherheitshinweise

- Verwenden Sie starke, einzigartige Passwörter für alle Sicherheitsvariablen.
- Ändern Sie die Standard-Ports in Produktionsumgebungen.
- Halten Sie NiFi und alle zugehörigen Komponenten stets auf dem neuesten Stand.

## Fehlerbehebung

Wenn Sie Probleme beim Starten von NiFi haben, überprüfen Sie die Log-Dateien im `./nifi/logs`-Verzeichnis für weitere Details.
