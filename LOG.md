# Windows IT-Support-Lab

Mein Lernprojekt für Windows im Support- und Admin-Alltag: Windows 11, Windows Server, Active Directory, PowerShell, Microsoft 365 und ein selbst gehostetes Ticketsystem. Ich komme aus der Linux-Welt (WIFI Linux-Systemadministrator, Homelab) und baue hier gezielt die Windows-Seite auf.

Alles läuft in virtuellen Maschinen mit Evaluierungsversionen. Jeder Block hat eine eigene Dokumentation in `docs/`. Mein Arbeitsprotokoll steht in [LOG.md](LOG.md).

## Umgebung

| Teil | Wert |
|---|---|
| Host | _(z. B. Fedora mit KVM/virt-manager)_ |
| Windows Server | _(Version)_ |
| Windows 11 Client | _(Version)_ |
| Netz | isoliertes virtuelles Netz, kein Zugriff auf mein Heimnetz |

## Checkliste

Reihenfolge nach Abhängigkeit. Erledigt ist ein Punkt, wenn ich ihn selbst ohne Anleitung nachbauen kann und die Doku dazu steht.

### 0. Umgebung
- [ ] Virtualisierung einrichten (KVM oder UTM)
- [ ] Evaluierungs-ISOs von Windows 11 und Windows Server besorgen
- [ ] Isoliertes virtuelles Netz anlegen
- [ ] Snapshots testen: Zustand sichern, kaputt machen, zurückspielen

### 1. Windows-11-Client im Support-Alltag
- [ ] Ereignisanzeige, Dienste, Geräte-Manager, Task-Manager
- [ ] Lokale Benutzer und Gruppen
- [ ] Windows Update: Verlauf, Fehlersuche, Updates verwalten
- [ ] Drucker einrichten, mehrere Bildschirme
- [ ] Remotedesktop und Remotehilfe
- [ ] Netzwerk-Werkzeuge: `ipconfig`, `ping`, `nslookup`, `tracert`
- [ ] Was ist neu in Windows 11 gegenüber Windows 10?

### 2. Windows Server und PowerShell-Grundlagen
- [ ] Server Manager, Rollen und Features
- [ ] Statische IP, Hostname, Firewall
- [ ] PowerShell: `Get-Help`, `Get-Command`, Pipeline, Objekte statt Text
- [ ] `Get-Service`, `Get-WinEvent`, `Get-Process`

### 3. Active Directory
- [ ] AD DS installieren, Domäne anlegen
- [ ] DNS (AD-integriert) und DHCP (Bereich, Reservierung)
- [ ] Organisationseinheiten, Benutzer, Gruppen
- [ ] Windows-11-Client in die Domäne aufnehmen
- [ ] Support-Aufgaben: Passwort zurücksetzen, Konto entsperren
- [ ] Gruppenrichtlinien (GPO): Laufwerk verbinden, Passwortregeln
- [ ] Dateiserver: Freigaben und NTFS-Berechtigungen
- [ ] Druckerserver

### 4. Netzwerk vertiefen
- [ ] VLAN, Routing und Switching
- [ ] IPv6-Grundlagen
- [ ] WLAN-Grundlagen
- [ ] Ein Szenario im Simulator nachbauen

### 5. Microsoft 365, Entra ID und Intune
- [ ] Testtenant einrichten
- [ ] Benutzer und Lizenzen verwalten
- [ ] Postfach (Exchange Online) und Teams in den Grundzügen
- [ ] MFA aktivieren
- [ ] Gerät in Intune registrieren
- [ ] Hybrid-Szenarien als Konzept verstehen

### 6. Azure-Grundlagen
- [ ] Abonnement, Ressourcengruppe, virtuelle Maschine, virtuelles Netzwerk
- [ ] Ein kleines Beispiel aufbauen und wieder löschen (Kosten im Blick behalten)

### 7. PowerShell vertiefen
- [ ] Benutzer aus einer CSV-Datei anlegen
- [ ] Einen Bericht erzeugen (z. B. inaktive Konten)
- [ ] Vergleich Bash und PowerShell dokumentieren

### 8. Support-Prozesse
- [ ] Ticketsystem selbst hosten (osTicket oder Zammad)
- [ ] Ein paar Tickets von Anfang bis Ende durchspielen
- [ ] Begriffe: Incident, Problem, Change, SLA

### 9. Optional
- [ ] Fundamentals-Prüfung (z. B. AZ-900), falls sie in Stellenanzeigen gefordert wird. Vorher prüfen, ob die Prüfung noch angeboten wird.

## So dokumentiere ich

1. **Während der Arbeit:** Eine Zeile pro Schritt in [LOG.md](LOG.md): was gemacht, was kaputt, wie gelöst. Nicht formulieren, nur mitschreiben.
2. **Am Ende jedes Blocks:** Aus dem Protokoll eine kurze Doku in `docs/` machen (15 bis 20 Minuten), danach committen.
3. **Aufbau jeder Doku:**
   - Ziel
   - Umgebung
   - Vorgehen (Stichpunkte, nur Befehle, die nicht offensichtlich sind)
   - Probleme und Lösungen
   - Ergebnis
4. **Keine Zugangsdaten und keine echten IP-Adressen** aus meinem Heimnetz in diesem Repository.
