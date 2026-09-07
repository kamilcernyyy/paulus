# Paulus Coffee — web

Statická stránka ve vizuálním stylu **Monte** (terakota #b84b30 / krém #f8f4e9).
Jeden soubor `index.html`, žádný build step — nasadí se na Vercel jako statický projekt
(stejně jako teaser). Grafiky jsou vloženy přímo v HTML (base64), takže stránka funguje
i bez `assets/`. Složka `assets/` obsahuje ilustrace navíc pro další použití.

## Fonty (náhrady dle Monte style guide)
- Riposte → **DM Serif Display** (nadpisy, eyebrow, wordmark)
- body → **Source Serif 4** (delší text, navigace, tlačítka)
- Apercu Mono → **JetBrains Mono** (data: čas, souřadnice, ceny)

Až budeš mít licenci na Riposte / Apercu Mono, stačí vyměnit `@import` fontů
a proměnné `--font-display` / `--font-mono`.

## Co doplnit (hledej v kódu komentáře `TEXT:`, `FOTO:`, `LOGO:`)
- **Logo** — nav i patička mají dočasný textový wordmark `paulus`.
- **Texty** — hero claim, úvod, „Náš přístup", „U stolu", menu a ceny jsou ukázkové.
- **Fotky** — šedé bloky `Foto — …` (interiér 3:2, galerie 16:9, mapa/vchod 4:3).
- **OG obrázek** — `assets/og-image.jpg` 1200×630 pro sdílení na sítích.
- **Kontakt** — adresa, telefon, e-mail, IG/FB (v HTML i v JSON-LD strukturovaných datech).
- **Doména** — všude je placeholder `pauluscoffee.cz` (canonical, OG, robots, sitemap, JSON-LD).

## Ilustrace (assets/)
Tvoje přiložené kresby překreslené do palety Monte, průhledné pozadí:
- `toast_cream.png` — ruce s kávou, krém (použito v heru)
- `table_black.png` — stůl s kávami shora, černá (použito v sekci „U stolu")
- `toast_bordeaux` / `toast_black` / `table_corten` / `table_bordeaux` — varianty barev navíc

## Animace (drží se tvých konvencí)
Jen transform/opacity, easing tokeny, UI do 300 ms, plné `prefers-reduced-motion`,
hover jen na `hover:hover`. Otáčející se textový kruh + jemné plování ilustrace v heru,
tiché odhalení sekcí (jen opacita), karusel galerie na vanilla JS.

## SEO / AEO
`index.html` prošlo interním auditem **25/25**: title, meta description, canonical,
robots, Open Graph + Twitter, JSON-LD `CafeOrCoffeeShop` (adresa, geo, otevírací doba)
i `FAQPage` pro hlasové asistenty, jeden `<h1>`, sémantické landmarky, alt texty,
skip-link, focus-visible. Přiloženy `robots.txt` a `sitemap.xml`.
