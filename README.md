# Fischer Design: Domain & Hosting für die neue Website

Recherche für die Firmen-Website von **Fischer Design**. Stand: **30.10.2026**, Namensideen und Budget-Setup ergänzt am **31.10.2026**.
Alle Preise inkl. 19 % MwSt., soweit nicht anders angegeben. Preise ändern sich häufig, maßgeblich ist der Warenkorb beim Anbieter.

---

## Das Wichtigste in 30 Sekunden

| Frage | Antwort |
|---|---|
| **Aktueller Favorit?** | ⭐ **`fischerdg.de`** („Fischer DG“ = **F**ischer **D**esign **G**ermany): 12 Zeichen, frei (31.10.2026), dazu sind `fischer-dg.de`, `fischerdg.com` und `fischerdg.eu` frei. Im Budget z. B. `fischerdg.de` + `fischer-dg.de` für **7,82 €/Jahr**. → [Ideen rund um fischerdg.de](docs/06-namensideen-domains.md#runde-3-31102026-alles-rund-um-fischerdgde) |
| **Welcher Name passt zu Folierung, Werbetechnik und CAD?** | 🆕 **Fischer Designwerk** → `fischerdesignwerk.de` + Kurz-Domain **`fdwerk.de`** (9 Zeichen). Alternativen: **Fischer Designtechnik** (`fdtechnik.de`), **Fischer Design Lab**, **Fischer Designgarage** (`fdgarage.de`). Ohne Umbenennung: **Fischer DG** (`fischerdg.de`) oder `fischer-design.de` (steht zum Verkauf). Namen wie „Fischer Werbetechnik“, „Folien Fischer“ oder „Fischer CAD“ sind **schon von Firmen in deiner Branche belegt**. → [Namensideen & Domain-Check](docs/06-namensideen-domains.md) |
| **Geht die Website für max. 20 €/Jahr?** | 🆕 **Ja**, mit **ca. 4–8 €/Jahr**: Domain(s) bei INWX, Website kostenlos auf **Cloudflare Pages**, E-Mail kostenlos (Zoho Mail Free oder Weiterleitung). Klassisches Webhosting (29–32 €/Jahr) passt nur im Aktionspreis. → [Budget-Setup](docs/07-budget-website-unter-20-euro.md) |
| **Ist `fischer-design-germany.de` frei?** | ✅ **Ja** (DENIC-Abfrage 30. und 31.10.2026), aber mit 25 Zeichen lang. „Germany“ ist neben `.de` doppelt gemoppelt |
| **Wo kaufe ich die Domain heute?** | ⭐ **INWX**: **5,02 €** im 1. Jahr, danach **3,91 €/Jahr**. Das ist der günstigste Dauerpreis eines deutschen Anbieters, mit voller DNS-Kontrolle, DynDNS und ohne Lock-in. → [Anleitung](docs/01-domain-registrieren.md#4-schritt-für-schritt-heute-registrieren-inwx) |
| **Wie viel Speicher brauche ich?** | Realistisch **≈ 0,7 GB**, maximal **≈ 2,2 GB** inkl. 30 % Puffer. **Jedes Paket ab 10 GB reicht**, der Speicher ist also kein Auswahlkriterium. → [Rechnung](docs/02-speicherbedarf.md) |
| **Welcher Server später?** | Im 20-€-Budget: **Cloudflare Pages** (kostenlos), siehe oben. Mit mehr Budget: **netcup Webhosting 1000** (2,69 €/Monat, `.de`-Domain + 100 E-Mail-Adressen + SSL inklusive) oder **Hetzner Webhosting S** (1,90 €/Monat, monatlich kündbar, Domain extra). → [Vergleich](docs/03-hosting-vergleich.md) |
| **Kann das NAS der Server sein?** | Technisch ja, für die Firmen-Website aber **nicht empfohlen**: Ausfälle, Upload-Grenzen, DS-Lite, Sicherheitsrisiko für deine Daten, kein E-Mail-Betrieb. Nutze das NAS für **Backups, Originale und Tests**. → [Bewertung](docs/04-nas-als-webserver.md) |

---

## Heute zu erledigen: Domain sichern

0. **Namen festlegen**, z. B. einen der Favoriten aus [06 – Namensideen](docs/06-namensideen-domains.md).
1. Konto bei [INWX](https://www.inwx.de) anlegen und 2-Faktor-Anmeldung aktivieren.
2. Eine **sofortige Zahlungsart** wählen (z. B. PayPal oder Kreditkarte). Eine Überweisung dauert 1–2 Tage.
3. Die Wunschdomain(s) suchen (z. B. `fischerdg.de` + Tippfehler-Schutz `fischer-dg.de`), in den Warenkorb legen, 1 Jahr Laufzeit.
4. Inhaberdaten **exakt wie im Ausweis** eintragen. Als Einzelunternehmer bist du **natürliche Person**; Pflicht sind außerdem eine **Telefonnummer** und eine **E-Mail-Adresse**.
5. Bestellen und den **Bestätigungslink in der E-Mail** sofort anklicken (neue DENIC-Pflicht).
6. Nameserver vorerst unverändert lassen. Die Website kommt später.

Details, Alternativen (Hetzner, netcup, STRATO …) und die neuen DENIC-Regeln stehen in **[01 – Domain registrieren](docs/01-domain-registrieren.md)**.

---

## Kosten im Überblick

| Variante | 1. Jahr | Folgejahre | Enthalten |
|---|---:|---:|---|
| **Nur Domain bei INWX** (heute) | **5,02 €** | 3,91 € | Domain, DNS, DynDNS |
| 🆕 **Spar-Setup** (2 Domains + Cloudflare Pages + Zoho Mail Free) | **10,04 €** | **7,82 €** | 2 Domains, Website-Hosting, SSL, E-Mail (Web) → [07](docs/07-budget-website-unter-20-euro.md) |
| Domain + **netcup Webhosting 1000** | 32,28 € | 32,28 € | Domain, Webspace 25 GB, 100 E-Mail-Adressen, SSL |
| Domain bei Hetzner + **Hetzner Webhosting S** | 28,63 € (+ ggf. 9,90 € Einrichtung) | 28,63 € | Domain, Webspace 10 GB, E-Mail, SSL, Backups |
| ALL-INKL Privat+ (Komfort) | 87,45 € (1. Monat gratis) | 95,40 € | 5 Domains, 100 GB, E-Mail, SSL, DynDNS |
| Homepage-Baukasten (STRATO bis Squarespace) | 77 € bis ca. 228 $ | 84 € bis ca. 228 $ | Editor im Browser, Domain, teils E-Mail |
| NAS zu Hause | Domain 5,02 € + Strom | Domain 3,91 € + Strom | Website ja, **E-Mail nicht**, keine Ausfallsicherheit |

---

## Dokumente

| Nr. | Dokument | Inhalt |
|---|---|---|
| 01 | [Domain registrieren](docs/01-domain-registrieren.md) | Verfügbarkeit, Preisvergleich aller Registrare, Empfehlung, Schritt-für-Schritt, neue DENIC-Regeln (NIS2) |
| 02 | [Speicherbedarf](docs/02-speicherbedarf.md) | 3 Szenarien mit 30 % Puffer, Video-Größen, Traffic, Optimierungstipps |
| 03 | [Hosting-Vergleich](docs/03-hosting-vergleich.md) | Webhosting, Baukästen, Gratis-Hosting, VPS: Preise, Laufzeiten, 3-Jahres-Kosten, Empfehlung |
| 04 | [NAS als Webserver](docs/04-nas-als-webserver.md) | Machbarkeit, Risiken, sichere Test-Variante (Cloudflare Tunnel), sinnvolle NAS-Nutzung |
| 05 | [Checkliste Website-Start](docs/05-checkliste-website-start.md) | To-dos von der Domain bis zum Livegang, inkl. Impressum/Datenschutz |
| 06 | [Namensideen & Domain-Check](docs/06-namensideen-domains.md) | Namen mit „Fischer (Design)“ passend zu Folierung/Werbetechnik/CAD, Kürzel, Verfügbarkeit von 196 Domains, Marken- und Konkurrenz-Check, Empfehlung |
| 07 | [Website für max. 20 € im Jahr](docs/07-budget-website-unter-20-euro.md) | Spar-Setup (Domain + kostenloses Hosting + E-Mail), Einrichtung, Einschränkungen, Aktionspreise |

---

## Methodik

- **Domain-Verfügbarkeit:** direkte Abfrage beim RDAP-Dienst der DENIC (`rdap.denic.de`), Gegenprobe mit vergebenen Domains.
- **Preise:** direkt von den Anbieter-Websites abgerufen (30.10.2026). Wo das technisch nicht ging (netcup-Domainpreis), aus Vergleichsportalen, entsprechend gekennzeichnet.
- **Speicherbedarf:** eigene Rechnung mit dokumentierten Annahmen (Bildgrößen, Video-Bitraten, CMS-Größe).
- Keine Rechts- oder Steuerberatung. Alle Angebote vor der Bestellung im Warenkorb prüfen.
