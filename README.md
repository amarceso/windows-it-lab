# Windows Lab

Da ich Windows nur als Anwender kenne und mich seit Jahren mit Linux beschäftige, möchte ich mein Wissen rund um Windows auffrischen und vertiefen. Deshalb gibt es dieses Projekt. Die Themengebiete, die ich mir dadurch aneignen will, umfassen: Windows 11, Windows Server, Active Directory, PowerShell, Microsoft 365 und ein selbst gehostetes Ticketsystem.

Alles läuft in virtuellen Maschinen. Jeder Punkt hat eine eigene Dokumentation in `docs/`. Mein Arbeitsprotokoll steht in [LOG.md](LOG.md).

## Umgebung

| System | Version / Einstellung |
|---|---|
| Host | Fedora Linux 44 & KVM/QEMU mit virt-manager |
| Windows Server | _(Version)_ |
| Windows 11 Client | _(Version)_ |
| Netz | isoliertes virtuelles Netz, kein Zugriff auf mein Heimnetz |

## Checkliste

Reihenfolge nach Abhängigkeit. Erledigt ist ein Punkt, wenn ich ihn selbst ohne Anleitung nachbauen kann und die Dokumentation dafür fertig ist.

### 0. Umgebung
- [ ] Virtualisierung einrichten (KVM)
- [ ] Evaluierungs-ISOs von Windows 11 und Windows Server besorgen & installieren
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

## So dokumentiere ich

1. **Protokollierung:** Grobe Zusammenfassung basierend auf meinen privaten Notizen, die am Ende der Arbeitssession in [LOG.md](LOG.md) eingetragen werden:

   Datum, Themengebiet, was ich gemacht hab, was kaputt war, wie ich es gelöst habe und was mir vielleicht noch fehlt, damit der Unterpunkt / Themenblock fertig ist.

2. **Am Ende jedes Punktes:** Aus dem Protokoll eine kurze Dokumentation in `docs/` machen.

3. **Aufbau der Dokumentation:**
   - Ziel
   - Umgebung
   - Vorgehen (Stichpunkte, nur Befehle, die nicht offensichtlich sind)
   - Probleme und Lösungen
   - Ergebnis

4. **Es werden natürlich keine echten Zugangsdaten, echten IP-Adressen, Lizenzkeys etc.** in diesem Repository verwendet.
