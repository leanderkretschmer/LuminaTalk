# LuminaTalk - Roadmap

## I. Vision

Eine flexible, sichere und erweiterbare Chat-Plattform, die über Web, native Apps und Integrationen mit Drittanbieterdiensten wie Discord zugänglich ist.  Fokus auf Benutzerfreundlichkeit, Sicherheit und Erweiterbarkeit.

## II. Phasen

### Phase 1:  Grundlegende Chat-Funktionalität (MVP)

*   **Ziel:**  Erstellung eines minimal funktionsfähigen Produkts mit den Kernfunktionen.
*   **Dauer:**  8-12 Wochen
*   **Features:**
    *   [ ]  Backend Setup (Node.js/Express, MongoDB/PostgreSQL)
    *   [ ]  LDAP-Login
    *   [ ]  Google & Apple Login (Passport.js)
    *   [ ]  JWT-Authentifizierung
    *   [ ]  Admin-Benutzerverwaltung (Freischaltung)
    *   [ ]  Frontend (React): Login, Chat-Übersicht (Seitenleiste), Chat-Ansicht
    *   [ ]  Echtzeit-Chat (WebSocket/Socket.IO)
    *   [ ]  Senden und Empfangen von Textnachrichten
    *   [ ]  Grundlegendes Styling (KI-Chatbot-Look)
    *   [ ]  Deployment (Docker/Kubernetes - optional)

### Phase 2: Erweiterte Funktionen und 3rd-Party-Integration

*   **Ziel:**  Erweiterung der Kernfunktionen und Integration von Discord.
*   **Dauer:** 6-8 Wochen
*   **Features:**
    *   [ ]  Medien-Upload (Bilder, Videos, Dateien)
    *   [ ]  Discord-Integration:
        *   [ ]  Nachrichten von SynapseChat zu Discord (als Benutzer)
        *   [ ]  Nachrichten von Discord zu SynapseChat (als Benutzer)
        *   [ ]  Handhabung großer Mediendateien (Link zu SynapseChat)
    *   [ ]  Benachrichtigungen (Push-Benachrichtigungen für Web & Mobile)
    *   [ ]  Suche (Chat-Verlauf)

### Phase 3:  API und Custom Apps

*   **Ziel:**  Bereitstellung einer öffentlichen API für die Entwicklung von Custom Apps.
*   **Dauer:**  8-10 Wochen
*   **Features:**
    *   [ ]  Definition und Dokumentation der SynapseChat API (RESTful)
    *   [ ]  Authentifizierung für API-Zugriff (OAuth 2.0)
    *   [ ]  Unterstützung für Webhooks (Ereignisbenachrichtigungen)
    *   [ ]  Beispiel-Apps (Dokumentation & Code-Beispiele)
    *   [ ]  API-Rate-Limiting & Monitoring

### Phase 4:  Mobile Apps (iOS & Android)

*   **Ziel:**  Entwicklung nativer Mobile Apps für iOS und Android.
*   **Dauer:**  10-12 Wochen (pro Plattform)
*   **Features:**
    *   [ ]  iOS App (Swift/Objective-C oder React Native)
    *   [ ]  Android App (Kotlin/Java oder React Native)
    *   [ ]  Native Push-Benachrichtigungen
    *   [ ]  Offline-Unterstützung (begrenzt)
    *   [ ]  Optimierung für Mobile Devices

## III. Detaillierte Feature-Liste (Backlog)

*   **Benutzerverwaltung:**
    *   [ ]  Rollenbasierte Zugriffskontrolle (RBAC)
    *   [ ]  Gruppenverwaltung
    *   [ ]  Benutzerprofile (Avatar, Status, etc.)
*   **Chat-Funktionen:**
    *   [ ]  Direktnachrichten (1:1)
    *   [ ]  Gruppenchats
    *   [ ]  Öffentliche Kanäle
    *   [ ]  Threads
    *   [ ]  Reaktionen auf Nachrichten (Emojis)
    *   [ ]  Umfragen
    *   [ ]  Code-Snippets
    *   [ ]  Sprachnachrichten
    *   [ ]  Videoanrufe (später)
*   **Integrationen:**
    *   [ ]  Weitere 3rd-Party-Dienste (z.B. Jira, Trello)
    *   [ ]  Webhooks für eingehende Nachrichten
*   **Sonstiges:**
    *   [ ]  Ende-zu-Ende-Verschlüsselung (E2EE)
    *   [ ]  Audit-Logs
    *   [ ]  Compliance (DSGVO, etc.)
    *   [ ]  Internationalisierung (i18n)
    *   [ ]  Barrierefreiheit (WCAG)

## IV. Technologie Stack (aktualisiert)

*   **Backend:**
    *   Node.js (Express)
    *   Datenbank: MongoDB (oder PostgreSQL)
    *   LDAP (ldapjs)
    *   OAuth 2.0 (Passport.js)
    *   JSON Web Tokens (JWT)
    *   WebSocket (Socket.IO)
    *   REST API
*   **Frontend:**
    *   React
    *   Styled-Components / Material-UI
*   **Mobile Apps:**
    *   Swift/Objective-C (iOS) oder Kotlin/Java (Android)  *oder* React Native
*   **DevOps:**
    *   Docker
    *   Kubernetes (optional)
    *   CI/CD (GitHub Actions, etc.)

## V.  API Design (Vorläufig)

(Beispiel - muss noch detailliert werden)

*   `/api/v1/users`:  Benutzerverwaltung (GET, POST, PUT, DELETE)
*   `/api/v1/chats`:  Chats auflisten, erstellen (GET, POST)
*   `/api/v1/chats/{chatId}/messages`:  Nachrichten abrufen, senden (GET, POST)
*   `/api/v1/media`:  Medien-Upload (POST), Abruf (GET)

**Authentifizierung:**  OAuth 2.0 (Client Credentials Grant für Apps, Authorization Code Grant für Benutzer)

## VI. Discord-Integration (Details)

*   **Bot-Konto:**  SynapseChat benötigt ein Bot-Konto auf dem Discord-Server.
*   **Webhooks:**  SynapseChat verwendet Webhooks, um Nachrichten in Discord zu posten.
*   **Discord-Befehle:**  Benutzer können Discord-Befehle verwenden, um Aktionen in SynapseChat auszulösen (z.B. `/synapsechat send <message>`).
*   **Mapping:**  Ein Mapping zwischen SynapseChat-Benutzern und Discord-Benutzern muss existieren.
*   **Berechtigungen:**  Die Discord-Integration muss die Berechtigungen der Benutzer in SynapseChat respektieren.

## VII.  Qualitätsmerkmale

*   **Sicherheit:**  Sichere Authentifizierung, Autorisierung, Datenschutz.
*   **Skalierbarkeit:**  Horizontale Skalierung des Backends.
*   **Performance:**  Schnelle Ladezeiten, reaktionsschnelle Benutzeroberfläche.
*   **Benutzerfreundlichkeit:**  Intuitive Bedienung, ansprechendes Design.
*   **Erweiterbarkeit:**  Einfache Integration neuer Funktionen und Dienste.
*   **Testbarkeit:**  Umfassende Unit- und Integrationstests.
*   **Wartbarkeit:**  Gut dokumentierter Code, klare Architektur.
