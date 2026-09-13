# Paulus Café — web

Jeden `index.html`, self-contained (grafika, animace i GSAP vložené) → funguje i po stažení
a otevření lokálně, nebo nasazený na Vercel. `assets/` = animace + ilustrace zvlášť.

## Barvy
Burnt Terracotta `#C34811` · Gallery Blue `#0B369A` · Stone Linen `#D9D1CA` · ink `#1a1c33`.

## Pozadí — Bubble Background (celá stránka)
Bublinové pozadí ve stylu animate-ui, přebarvené do naší palety: světlá gradientní základna
+ měkké terakota/modré „bubliny" se slučovacím (goo) SVG filtrem, které GSAP nekonečně posouvá.
Na desktopu jedna bublina jemně sleduje kurzor (interactive). Drženo světlé kvůli čitelnosti;
obsah má tmavý text / modré ilustrace = dobrý kontrast (ověřeno).

## Hero
- Běžící **vlnitý text** „NOVĚ OTEVŘENÁ KAVÁRNA · PAULUS CAFÉ" (nadpisový font Bricolage),
  teče a **animuje se přes barvy**. Skrytý `<h1>` pro SEO.
- **Animace** (tvůj webp) jako velký hlavní prvek přes celou šířku — přebarvená do Gallery Blue s průhledným pozadím
  (prosvítá bublinové pozadí), teď v **bezztrátové kvalitě** (ostrá, bez artefaktů).

## Vlnitý text místo marquee
Původní běžící lišty jsou nahrazené stejným vlnitým textem (nadpisový font, barevná animace):
„POCTIVÁ KÁVA · ČERSTVÉ PEČIVO · DOBRÉ RÁNO · OLOMOUC" a „PAULUS CAFÉ · OLOMOUC · EST. 2026 ·
POCTIVÁ KÁVA", plus „ZRNO · VODA · ČAS". Vše bez bílého pozadí — přímo na bublinách.

## Odstraněno
Bílý pruh „Nejlepší nápady vznikají u kávy" (ilustrace + text) je pryč.

## Animace — vše GSAP (v3.12.5 + ScrollTrigger, vloženo napevno)
Bubliny + interaktivní kurzorová bublina, vlnitý text (tok + barevná vlna), odhalování sekcí,
kaskáda menu, plování/drift ilustrací, draw-in. Přes `gsap.matchMedia` → při omezeném pohybu
se pohyb vypne (bubliny statické) a obsah je plně viditelný.

## Optimalizace
Ověřeno na desktopu (1280/1440) i mobilu (390 px): hero i s CTA nad přehybem, čitelnost,
žádný vodorovný přesah, bez JS chyb, SEO/AEO 22/22.

## Pozn. k velikosti
Animace je vložená bezztrátově (~2,3 MB) kvůli kvalitě → `index.html` je cca 4,4 MB. Pokud
budeš chtít lehčí soubor, načti animaci externě z `assets/animace.webp` místo vložené.

## Co doplnit (`TEXT:`, `FOTO:`, `LOGO:`)
Logo, finální texty/ceny, fotky (šedé sloty), OG obrázek, kontakt (HTML i JSON-LD), doména.
