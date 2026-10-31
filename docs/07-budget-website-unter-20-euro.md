# 07 – Website für max. 20 € im Jahr

> Stand: **31.10.2026**. Preise inkl. MwSt., soweit nicht anders angegeben.

## Ergebnis

**Ja, das geht.** Mit kostenlosem Hosting für eine statische Website und günstigen `.de`-Domains kostet alles zusammen **ca. 4–8 € pro Jahr**, inklusive E-Mail-Adresse mit eigener Domain.

Klassisches Webhosting passt dagegen **nicht** ins Budget: netcup Webhosting 1000 kostet 32,28 €/Jahr, Hetzner S plus Domain 28,63 €/Jahr. Ausnahme ist ein Aktionspreis, siehe Variante 2.

---

## Variante 1: Spar-Setup (empfohlen)

| Baustein | Anbieter | Kosten pro Jahr |
|---|---|---:|
| Hauptdomain, z. B. `fischerdesignwerk.de` | INWX | 3,91 € (1. Jahr 5,02 €) |
| Kurz-Domain, z. B. `fdwerk.de` (optional) | INWX | 3,91 € (1. Jahr 5,02 €) |
| DNS-Verwaltung | Cloudflare (Free) | 0 € |
| Website-Hosting | **Cloudflare Pages** (Free): laut Cloudflare unbegrenzt Seiten, Anfragen und Bandbreite, SSL inklusive | 0 € |
| E-Mail `info@…` | **Zoho Mail Free**: bis 5 Nutzer, 5 GB je Postfach, senden **und** empfangen über die Zoho-Oberfläche ¹ | 0 € |
| **Summe** | | **3,91–7,82 €** (1. Jahr 5,02–10,04 €) |

¹ Laut Zoho gibt es den Gratis-Tarif **„nur in ausgewählten Rechenzentren“**. Ob er im **EU-Rechenzentrum** angeboten wird, zeigt sich erst bei der Anmeldung. Falls nicht, nimm aus Datenschutzgründen besser **Zoho Mail Lite im EU-Rechenzentrum** oder die **Weiterleitung per Cloudflare** (Tabelle unten).

### Alternativen für die E-Mail

| Lösung | Was sie kann | Kosten pro Jahr | Hinweis |
|---|---|---:|---|
| **Zoho Mail Free** | richtiges Postfach über die Zoho-Oberfläche, **kein IMAP/POP**, also nicht in Outlook oder Apple Mail | 0 € | nur in ausgewählten Rechenzentren; EU-Verfügbarkeit bei der Anmeldung prüfen |
| Zoho Mail Lite | wie oben, plus Nutzung in Mail-Programmen am PC und Handy | ca. 12 $ je Nutzer (+ ggf. MwSt.) | mit 2 Domains wird es knapp über 20 €; mit 1 Domain ca. 16–19 € |
| Cloudflare Email Routing | **nur Weiterleitung** von `info@…` an dein bestehendes Postfach | 0 € | Antworten kommen von deiner privaten Adresse |
| INWX E-Mail „Easy“ | 20 Weiterleitungen, kein eigenes Postfach | 2,88 € (0,24 €/Monat, 12 Monate) | nur, wenn die DNS bei INWX bleiben soll |

### So wird es eingerichtet

1. **Domain(s) bei INWX registrieren** (Anleitung: [01 – Domain registrieren](01-domain-registrieren.md#4-schritt-für-schritt-heute-registrieren-inwx)).
2. **Cloudflare-Konto** (kostenlos) anlegen, die Domain hinzufügen und bei INWX die **Nameserver auf Cloudflare** umstellen. Das ist nötig, damit die Hauptdomain ohne „www“ mit Cloudflare Pages funktioniert.
3. **Website als statische Seite bauen** (HTML/CSS/Bilder, ohne WordPress), z. B. mit dem kostenlosen Programm *Publii*, einem anderen Editor mit HTML-Export oder von Hand. Das kann ich auch für dich übernehmen.
4. In **Cloudflare Pages** den fertigen Website-Ordner hochladen (Direct Upload per Drag & Drop oder über GitHub) und die Domain verbinden.
5. **Zoho Mail** einrichten: Domain bestätigen und die von Zoho angezeigten MX-, SPF- und DKIM-Einträge bei Cloudflare eintragen.
6. Die Kurz-Domain (`fdwerk.de`) per Weiterleitungsregel bei Cloudflare auf die Hauptdomain zeigen lassen.

### Das musst du wissen

| Punkt | Was das heißt |
|---|---|
| **Max. 25 MiB pro Datei** (Cloudflare Pages) | Das 1-Minuten-Video als MP4 in 1080p mit ca. 3 Mbit/s exportieren (≈ 22 MB) oder in 720p. Alternativ YouTube/Vimeo per 2-Klick-Lösung einbinden |
| **Nur statische Seiten** | kein WordPress, kein PHP. Für eine Firmen-Website mit Leistungen, Referenzen, Galerie und Kontakt reicht das völlig |
| **Kontaktformular** | Am einfachsten Telefon, E-Mail-Link und WhatsApp-Button. Ein Formular bräuchte einen Zusatzdienst |
| **Datenschutz (DSGVO)** | Cloudflare (USA, Teilnehmer am EU-US Data Privacy Framework) und Zoho (EU-Rechenzentrum): bei beiden den **Auftragsverarbeitungsvertrag** abschließen und sie in der Datenschutzerklärung nennen |
| **Support** | kein Telefon-Support, alles per Selbstbedienung bzw. über mich |

---

## Variante 2: Klassisches Webhosting zum Aktionspreis (wenn verfügbar)

netcup bietet sein **Webhosting 1000** regelmäßig in Aktionen an, deren Preis dann **dauerhaft** gilt.
Beispiel Dezember 2025: **1,08 €/Monat (12,96 € pro Jahr) inklusive `.de`-Domain**, 12 Monate Abrechnung. Diese Aktion ist abgelaufen. Ähnliche Angebote gab es auch in der **Black Week Ende November** (2025: 25.–29.11.).

**Falls so ein Angebot kommt:** Domain, Webspace, PHP/WordPress und **100 echte Postfächer mit IMAP** für ca. 13 € pro Jahr. Das wäre die komfortabelste Lösung im Budget.
Die heute bei INWX registrierte Domain kann dann als Inklusivdomain zu netcup umziehen.

> Ob und wann es wieder eine Aktion gibt, ist nicht sicher. Die netcup-Aktionsseite blockiert automatische Abrufe, ich konnte sie also nicht prüfen.

---

## Variante 3: Website auf dem eigenen NAS

Hier kostet nur die Domain (3,91 €/Jahr). Wegen Ausfallrisiko, Upload-Grenzen und Sicherheit bleibt meine Empfehlung aber: **nicht für den Live-Betrieb**, siehe [04 – NAS als Webserver](04-nas-als-webserver.md).

---

## Kostenvergleich pro Jahr (ab dem 2. Jahr)

| Lösung | Kosten pro Jahr | Im Budget? |
|---|---:|:---:|
| **Spar-Setup** mit 1 Domain + Zoho Free | **3,91 €** | ✅ |
| **Spar-Setup** mit 2 Domains + Zoho Free | **7,82 €** | ✅ |
| Spar-Setup mit 1 Domain + Zoho Mail Lite (IMAP) | ca. 16–19 € | ✅ knapp |
| netcup Webhosting 1000 **im Aktionspreis** (falls verfügbar) | ca. 13 € | ✅ |
| Hetzner Webhosting S + Domain | 28,63 € | ❌ |
| netcup Webhosting 1000 regulär | 32,28 € | ❌ |
| Homepage-Baukasten | ab 84 € | ❌ |

---

## Quellen

- Cloudflare Pages (Free: unbegrenzt Seiten, Anfragen, Bandbreite): <https://pages.cloudflare.com/> · Limits (25 MiB je Datei): <https://developers.cloudflare.com/pages/platform/limits/>
- Cloudflare Email Routing/Email Service: <https://developers.cloudflare.com/email-routing/>
- Zoho Mail Preise (Free: 5 Nutzer, 5 GB, kein IMAP/POP; Mail Lite 1 US$/Nutzer/Monat): <https://www.zoho.com/de/mail/zohomail-pricing.html>
- INWX E-Mail-Hosting (Easy 0,24 €/Monat): <https://www.inwx.de/de/hosting/email>
- INWX Preisliste: <https://www.inwx.de/de/domain/pricelist>
- netcup-Aktion Dez. 2025 (abgelaufen): <https://www.mydealz.de/deals/netcup-webhosting-1000-2703948> · netcup Black Week 2025: <https://www.mydealz.de/deals/netcup-black-week-2025-deals-rabatt-auf-rootserver-webhostingpakete-etc-2668621>
