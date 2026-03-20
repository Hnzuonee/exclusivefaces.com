# Zvláštní typy — statický prezentační web

Jednoduchý one-page prezentační web pro modelingovou a talentovou agenturu **Zvláštní typy**.
Projekt je postavený v **Astro** jako čistý statický web bez backendu, formulářů a databáze.

## Co projekt obsahuje

- one-page web (Hero, O agentuře, Koho zastupujeme, Pro koho jsme, Jak fungujeme, Kontakt, Footer)
- responzivní layout + mobilní menu
- sticky header + anchor navigace
- základní SEO metadata + Open Graph
- `404` stránku
- `robots.txt`
- `sitemap.xml`
- placeholder favicon
- připravené pro nasazení přes GitHub + Cloudflare Pages

## Lokální spuštění

### 1) Instalace závislostí

```bash
npm install
```

### 2) Vývojový server

```bash
npm run dev
```

Web poběží na adrese uvedené v terminálu (typicky `http://localhost:4321`).

### 3) Produkční build

```bash
npm run build
```

Build se vygeneruje do složky `dist/`.

## Nasazení na GitHub

1. Vytvoř nový repozitář na GitHubu.
2. V kořenu projektu spusť:

```bash
git init
git add .
git commit -m "Initial static website"
git branch -M main
git remote add origin https://github.com/TVUJ-UCET/TVUJ-REPO.git
git push -u origin main
```

## Nasazení na Cloudflare Pages

1. V Cloudflare otevři **Pages** → **Create a project**.
2. Připoj GitHub repozitář.
3. Nastav build:
   - **Framework preset:** Astro
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
4. Potvrď deploy.

## Napojení vlastní domény

1. V Cloudflare Pages otevři projekt → **Custom domains**.
2. Klikni na **Set up a custom domain**.
3. Přidej doménu (např. `zvlastnitypy.cz` a `www.zvlastnitypy.cz`).
4. Cloudflare automaticky vytvoří potřebné DNS záznamy (nebo nabídne kroky).

## Kde co upravit

### Název značky

- `src/pages/index.astro` → proměnná `brandName` nahoře.

### Texty všech sekcí

- `src/pages/index.astro` → obsah jednotlivých sekcí (`Hero`, `O agentuře`, `Koho zastupujeme`, ...).
- `src/pages/404.astro` → text 404 stránky.

### E-mail, Instagram, město, telefon

- `src/pages/index.astro` → sekce `Kontakt` + `Footer`.

### SEO metadata

- `src/pages/index.astro` → `pageTitle`, `pageDescription`, `og:*`, `canonicalUrl`.

### Doména

- `astro.config.mjs` → `site`
- `public/robots.txt` → URL sitemapy
- `public/sitemap.xml` → `<loc>`
- `src/pages/index.astro` → `canonicalUrl`

### Styly a vzhled

- `public/styles.css`

### Favicon

- `public/favicon.svg`

### Placeholder OG obrázek

- Aktuálně je použit odkaz `/og-placeholder.svg` v metadatech.
- Nahraj vlastní obrázek do `public/` a uprav cestu v `src/pages/index.astro`.
