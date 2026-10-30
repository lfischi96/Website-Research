# 02 – Speicherbedarf der Website (mit 30 % Puffer)

> Ziel: eine einfache Firmen-Website für **Fischer Design** (kein Shop) mit
> 50–100 Projektbildern, ein paar Animationen und einem 1-minütigen Video.

---

## Ergebnis auf einen Blick

| Szenario | Was dahintersteckt | Summe | **+ 30 % Puffer** |
|---|---|---:|---:|
| **A – schlank** | statische Website (HTML/CSS), Bilder fürs Web optimiert, Video in Full HD | 135 MB | **≈ 0,2 GB** |
| **B – realistisch** | WordPress o. ä. CMS, Bilder vor dem Hochladen verkleinert | 540 MB | **≈ 0,7 GB** |
| **C – großzügig** | WordPress, Original-Kamerafotos hochgeladen, zusätzlich 4K-Video, GIF-Animationen | 1.690 MB | **≈ 2,2 GB** |

**Fazit:** Selbst im großzügigsten Fall brauchst du **unter 3 GB**. Plane **mindestens 5 GB** ein. Jedes der Angebote in [03 – Hosting-Vergleich](03-hosting-vergleich.md) bietet **10 GB oder mehr**. Der Speicher ist deshalb **kein Auswahlkriterium**. Entscheidend sind Preis, E-Mail, Support und Laufzeit.

> **Achtung E-Mail:** Bei manchen Paketen teilen sich Website und E-Mail-Postfächer denselben Speicher.
> Ein Geschäftspostfach wächst über die Jahre leicht auf 2–5 GB (z. B. durch Anhänge mit Entwürfen).
> Mit E-Mail im selben Paket sind **10 GB oder mehr** sinnvoll, was alle empfohlenen Pakete erfüllen.

---

## Annahmen im Detail

| Bestandteil | A – schlank | B – realistisch | C – großzügig |
|---|---|---|---|
| **Bilder** (100 Stück, oberes Ende deiner Schätzung) | 0,75 MB/Bild: 1 Großansicht (ca. 2560 px, WebP/JPEG) + Vorschaubild → **75 MB** | 2 MB/Bild: Upload ca. 0,8 MB + die vom CMS automatisch erzeugten Zwischengrößen → **200 MB** | 10 MB/Bild: Originalfoto ca. 8 MB + Zwischengrößen → **1.000 MB** |
| **Animationen** (ca. 10 Stück) | Lottie/SVG oder kurze WebM-Loops, je ca. 1 MB → **10 MB** | MP4-Loops, je ca. 3 MB → **30 MB** | GIFs, je ca. 10 MB → **100 MB** |
| **Video** (1 Minute) | Full HD (1080p, ca. 5 Mbit/s) + Vorschaubild → **40 MB** | Full HD + zweite, kleinere Version für Smartphones → **60 MB** | 4K (ca. 20 Mbit/s) **und** Full HD → **190 MB** |
| **Website selbst** | HTML, CSS, JS, Schriften, Logos → **10 MB** | CMS-Kern, Theme, Plugins → **230 MB** + Datenbank **20 MB** | CMS mit Page-Builder und vielen Plugins → **350 MB** + Datenbank **50 MB** |
| **Summe** | **135 MB** | **540 MB** | **1.690 MB** |
| **+ 30 % Puffer** | **176 MB** | **702 MB** | **2.197 MB** |

Bei nur **50 Bildern** sinkt Szenario B auf ca. 440 MB, mit Puffer **≈ 0,6 GB**.

### Video: Wie groß ist eine Minute?

| Qualität | Größe pro Minute | Empfehlung |
|---|---:|---|
| Full HD, ca. 5 Mbit/s (H.264/MP4) | ≈ 38 MB | ✅ ideal für die Website |
| Full HD, ca. 8 Mbit/s | ≈ 60 MB | ok |
| 4K, ca. 20 Mbit/s | ≈ 150 MB | unnötig groß fürs Web |
| Kamera-Original 4K, ca. 100 Mbit/s | ≈ 750 MB | ❌ nicht hochladen, gehört auf das NAS |

---

## Wie viel Datenverkehr (Traffic) entsteht?

Beispielrechnung: **1.000 Besucher/Monat**, je 3 Seitenaufrufe à ca. 3 MB, und 20 % der Besucher schauen das Video (40 MB):

> 1.000 × 3 × 3 MB + 200 × 40 MB ≈ **17 GB pro Monat**

Alle empfohlenen Hoster haben **unbegrenzten Traffic**. Für das NAS spielt dagegen die **Upload-Geschwindigkeit** deines Internetanschlusses eine Rolle, siehe [04 – NAS als Webserver](04-nas-als-webserver.md).

---

## Tipps, damit die Seite klein und schnell bleibt

1. **Bilder vor dem Hochladen verkleinern:** längste Kante 2000–2560 px, Format **WebP** (oder JPEG mit Qualität ca. 80). Das spart 80–90 % gegenüber Kamera-Originalen.
2. **Originale (RAW, 4K-Video, Projektdateien) auf dem NAS archivieren**, nicht auf dem Webspace.
3. **Video** als MP4 (H.264) in 1080p mit ca. 4–6 Mbit/s exportieren, z. B. mit HandBrake, Preset „Web“. Dazu ein Vorschaubild (Poster) anlegen.
4. **Animationen** möglichst als Lottie/SVG/CSS oder kurze MP4/WebM-Loops anlegen, **keine großen GIFs**.
5. **Lazy Loading** nutzen: Bilder erst laden, wenn man hinscrollt. Das ist bei aktuellen CMS Standard.
