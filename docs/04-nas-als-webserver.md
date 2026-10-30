# 04 – Kann mein NAS der Webserver sein?

## Kurzantwort

**Technisch ja, als Dauerlösung für die Firmen-Website aber nicht empfehlenswert.**
Das NAS ist ein großartiger **Datenspeicher**: für Backups, Original-Fotos und Videos und als Testumgebung. Die **öffentliche** Website läuft besser bei einem Hoster für **2–3 € im Monat**, siehe [03 – Hosting-Vergleich](03-hosting-vergleich.md).

---

## Vergleich: NAS zu Hause vs. Webhosting

| Kriterium | NAS zu Hause | Webhosting (z. B. netcup/Hetzner) |
|---|---|---|
| **Laufende Kosten** | ✅ kein Hosting-Entgelt; Strom ca. 31–92 €/Jahr bei 10–30 W Dauerbetrieb und 0,35 €/kWh (fällt nicht zusätzlich an, wenn das NAS ohnehin läuft) | ca. 29–32 €/Jahr inkl. Domain und E-Mail |
| **Erreichbarkeit** | ⚠️ Bei Stromausfall, Router-Neustart, Internet-Störung, NAS-Update oder Umzug ist die Seite offline | ✅ Rechenzentrum mit Notstrom und redundanter Anbindung |
| **Internet-Anschluss** | ⚠️ Viele Anschlüsse (v. a. Kabel und manche Glasfaser) laufen mit **DS-Lite**: keine eigene öffentliche IPv4-Adresse, **Portfreigaben über IPv4 funktionieren dann nicht** | ✅ kein Thema |
| **Geschwindigkeit** | ⚠️ begrenzt durch deinen **Upload** (typisch: DSL 10–40 Mbit/s, Kabel 25–100 Mbit/s, Glasfaser je nach Tarif mehr). Jeder Video-Zuschauer braucht ca. 5 Mbit/s dauerhaft. Bei 10 Mbit/s Upload ruckelt es schon ab 2 gleichzeitigen Zuschauern, und dein eigenes Internet (Videocalls, Uploads) wird langsamer | ✅ Gigabit-Anbindung |
| **Sicherheit** | ❌ Ein aus dem Internet erreichbares NAS mit **privaten Daten und Kundendaten** ist ein beliebtes Angriffsziel. Beispiel: Die Ransomware **DeadBolt** verschlüsselte Anfang 2022 laut Berichten ca. 5.000 von rund 130.000 online erreichbaren QNAP-NAS, kurz darauf auch ASUSTOR-Geräte | ✅ Website getrennt von deinen Daten; Hoster patcht Server und Webserver |
| **Wartung** | ⚠️ alles selbst: NAS-Updates, Webserver/PHP, Zertifikate, Firewall, Backups, Monitoring | ✅ Hoster übernimmt den Großteil |
| **E-Mail** | ❌ Ein Mailserver am Privatanschluss ist praktisch unbrauchbar, weil Mails von privaten IP-Adressen oft als Spam gelten. Du brauchst also **trotzdem** einen E-Mail-Anbieter | ✅ Postfächer inklusive |
| **Vertrag / Recht** | ⚠️ Privatkunden-Internettarife sind für private Nutzung gedacht. Ob gewerblicher Serverbetrieb erlaubt ist, steht in den **AGB deines Providers**; bitte prüfen (nicht verifiziert). Datenschutz: Du bist selbst Betreiber (Server-Logs mit IP-Adressen usw.) | ✅ AV-Vertrag mit dem Hoster, klare Verantwortlichkeiten |
| **Speicher** | ✅ reichlich | ✅ 10–100 GB, laut Rechnung mehr als genug |

---

## Wenn du es trotzdem ausprobieren möchtest (z. B. als Test- oder Vorschau-Seite)

So geht es mit dem geringsten Risiko:

1. **Statische Website** (reines HTML/CSS/JS) statt WordPress auf dem NAS. Ohne PHP und Datenbank gibt es kaum Angriffsfläche.
2. Die Website **isoliert** betreiben: eigener freigegebener Ordner nur für die Website, z. B. Synology *Web Station* oder ein Docker-Container mit *nginx*. Keine anderen NAS-Dienste (Fotos, Dateien, Admin-Oberfläche) nach außen freigeben.
3. **Keine Portfreigabe** am Router, sondern **Cloudflare Tunnel** (kostenlos). Ein kleines Programm auf dem NAS (*cloudflared*, z. B. als Docker-Container) baut eine ausgehende Verbindung zu Cloudflare auf. Das funktioniert **auch mit DS-Lite**, deine Heim-IP bleibt verborgen, und Cloudflare filtert Angriffe vorher heraus.
   - Dafür muss die Domain bei Cloudflare eingebunden werden (Nameserver bei INWX auf Cloudflare umstellen, Free-Plan).
   - **Einschränkungen:** Cloudflare behält sich vor, im Free-Plan die Auslieferung von **Videos und vielen großen Dateien** einzuschränken. Das Video daher besser woanders hosten. Außerdem verarbeitet Cloudflare (USA) den gesamten Datenverkehr; das muss in die Datenschutzerklärung.
4. **NAS absichern:** Zwei-Faktor-Anmeldung, Standard-Admin-Konto deaktivieren, automatische Sicherheitsupdates, Firewall, keine Fernzugriffs-Dienste ohne Not, **Snapshots plus ein Offline-Backup** (externe Festplatte).
5. Die Seite als **„Vorschau“** nutzen, z. B. um Kunden einen Entwurf zu zeigen, und den **Live-Betrieb beim Hoster** machen.

---

## Empfehlung: So nutzt du das NAS sinnvoll

| Aufgabe | Wie |
|---|---|
| **Backup der Website** | Regelmäßig Website-Dateien und Datenbank vom Hoster aufs NAS sichern, z. B. mit dem Backup-Plugin des CMS (Export als Datei) oder per SFTP-Programm bzw. rsync. Zusätzlich zu den Backups des Hosters |
| **Archiv der Originale** | RAW-Fotos, 4K-Videos und Projektdateien liegen auf dem NAS, auf die Website kommen nur die verkleinerten Web-Versionen |
| **Testumgebung (Staging)** | Neue Website-Versionen erst lokal auf dem NAS testen (nur im Heimnetz erreichbar), dann zum Hoster hochladen |

**Fazit:** NAS = Speicher und Sicherheit im Hintergrund. Website = beim Hoster. Das kostet ca. 30 € im Jahr, und du bist auf der sicheren Seite.

---

## Quellen

- Synology Web Station (Funktionsumfang): <https://www.synology.com/en-nz/dsm/7.2/software_spec/web_station>
- Erfahrungsbericht Website auf Synology (Vor- und Nachteile): <https://www.windowscentral.com/how-set-website-synology-nas>
- Cloudflare Tunnel (keine offenen Ports, keine öffentliche IP nötig): <https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/>
- Cloudflare zu Video und großen Dateien im Free-Plan: <https://developers.cloudflare.com/fundamentals/reference/policies-compliances/delivering-videos-with-cloudflare/> · <https://blog.cloudflare.com/updated-tos/>
- DS-Lite: keine IPv4-Portfreigabe möglich (Praxis-Erklärungen): <https://www.ssdnodes.com/learn/lang/de/reach-a-home-server-behind-ds-lite-or-cgnat>, <https://forum.heimnetz.de/threads/portfreigabe-fuer-nextcloud-server-bei-ds-lite-verbindung.5152>
- DeadBolt-Ransomware auf NAS-Systemen: <https://www.computerbase.de/2022-02/ransomware-deadbolt-verschluesselt-auch-nas-systeme-von-asustor/>, <https://securityaffairs.com/129373/malware/qnap-nas-deadbolt-ransomware.html>
- Eigene Rechnungen (Upload, Strom): siehe [02 – Speicherbedarf](02-speicherbedarf.md)
