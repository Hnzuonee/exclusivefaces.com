# Exclusive Faces — statický prezentační web

Jednoduchý, rychlý a plně statický one-page web pro českou modelingovou a talentovou agenturu **Exclusive Faces**.

Projekt je postavený v čistém **HTML + CSS + JS**, aby byl co nejjednodušší na editaci, nahrání do GitHubu a nasazení na **Cloudflare Pages**.

## Co projekt obsahuje

- one-page homepage
- responzivní layout
- sticky header
- anchor navigaci
- mobilní menu
- 404 stránku
- `robots.txt`
- `sitemap.xml`
- favicon placeholder
- OG image placeholder
- základní SEO metadata

## Struktura projektu

```bash
exclusivefaces-site/
├── assets/
│   ├── favicon.svg
│   └── og-placeholder.svg
├── 404.html
├── index.html
├── README.md
├── robots.txt
├── script.js
├── sitemap.xml
└── styles.css
```

## Lokální spuštění

Stačí otevřít `index.html` v prohlížeči.

Pro pohodlnější lokální náhled můžeš spustit jednoduchý server například takto:

### Varianta 1: Python

```bash
python3 -m http.server 8080
```

Pak otevři:

```bash
http://localhost:8080
```

### Varianta 2: VS Code Live Server

Pokud používáš VS Code, můžeš otevřít projekt a pustit ho přes rozšíření **Live Server**.

## Nahrání na GitHub

### 1. Vytvoř nový repozitář
Například:

- `exclusivefaces-web`

### 2. Nahraj soubory do repozitáře

Přes terminál:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/TVUJ-UCET/TVUJ-REPO.git
git push -u origin main
```

## Nasazení na Cloudflare Pages

### 1. Přihlas se do Cloudflare
Otevři **Workers & Pages** → **Create application** → **Pages**.

### 2. Propoj GitHub repozitář
Vyber svůj repozitář s tímto projektem.

### 3. Build nastavení
Protože jde o čistý statický web, nastav:

- **Framework preset:** None
- **Build command:** nechat prázdné
- **Build output directory:** `/`

Poznámka: některé účty Cloudflare Pages chtějí místo `/` prázdnou hodnotu nebo `.`. Když by `/` neprošlo, použij `.`.

### 4. Deploy
Cloudflare projekt nasadí automaticky.

## Napojení vlastní domény

V Cloudflare Pages otevři nasazený projekt a jdi do:

- **Custom domains**

Pak:

1. klikni na **Set up a custom domain**
2. zadej svoji doménu
3. potvrď DNS nastavení

Pokud máš doménu už ve stejném Cloudflare účtu, bývá napojení skoro automatické.

## Kde co upravit

### 1. Název značky
Uprav v souboru:

- `index.html`
- `404.html`
- `README.md`
- `assets/og-placeholder.svg`

Hledej text:

- `Exclusive Faces`

### 2. Texty webu
Většina textů je přímo v:

- `index.html`

### 3. E-mail
Uprav v:

- `index.html`

Hledej:

- `hello@zvlastnitypy.cz`

### 4. Instagram
Uprav v:

- `index.html`

Hledej:

- `https://instagram.com/zvlastnitypy`
- `@zvlastnitypy`

### 5. Telefon
Uprav v:

- `index.html`

Hledej:

- `+420000000000`
- `+420 000 000 000`

### 6. Město
Uprav v:

- `index.html`

Hledej:

- `Praha`

### 7. Metadata a SEO
Uprav v:

- `index.html`
- `robots.txt`
- `sitemap.xml`

Důležité položky:

- `<title>`
- `meta description`
- `canonical`
- `og:title`
- `og:description`
- `og:url`
- `og:image`
- URL v `robots.txt`
- URL v `sitemap.xml`

### 8. Doména
Až bude finální doména jiná než `exclusivefaces.com`, uprav:

- `index.html`
- `robots.txt`
- `sitemap.xml`

Hledej:

- `https://exclusivefaces.com/`

### 9. Obrázky a assety
Momentálně jsou použité placeholdery.

Můžeš nahradit:

- `assets/favicon.svg`
- `assets/og-placeholder.svg`

Pokud budeš chtít doplnit skutečné fotky nebo vizuály, doporučený postup je vytvořit třeba složku:

```bash
assets/images/
```

A pak je vložit do `index.html` místo placeholder bloků v hero sekci.

## Doporučení

Tenhle projekt je záměrně jednoduchý.

Nepřidávej zbytečnosti jako:

- backend
- formuláře
- CMS
- blog
- těžké animace
- složité knihovny

Smysl toho webu je:

- působit profesionálně
- být důvěryhodný
- být rychlý
- být snadno upravitelný
- být bezproblémově nasaditelný

