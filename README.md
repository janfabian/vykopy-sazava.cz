# vykopy-sazava.cz

Web pro výkopové práce minibagrem — **Ionut Gabor**, Sázava a okolí (okres Benešov,
Posázaví).

Jednostránkový statický web, bez závislostí a build kroku. Design vychází z návrhu
z Claude Design („blueprint" styl, písmo Barlow / Barlow Condensed).

## Struktura

- `index.html` — celá stránka (sekce: hero, služby, proč malý bagr, realizace, ceník,
  o mně, oblast působení, reference, kontakt)
- `assets/ds.css` — design systém (barevné tokeny a komponenty)
- `assets/img/` — fotky ze zakázek

Otevři `index.html` v prohlížeči — nic víc není potřeba.

## Nasazení

- Hostováno na **Cloudflare Pages** (projekt `vykopy-sazava`).
- **Každý push do `main`** spustí GitHub Actions (`.github/workflows/deploy.yml`), který
  web nasadí na Cloudflare Pages přes wrangler. Potřebné secrets v repu:
  `CLOUDFLARE_API_TOKEN`, `CLOUDFLARE_ACCOUNT_ID`.
- Domény: **`vykopy-sazava.cz`** (+ `www`) míří na tento projekt.
  **`minibagr-sazava.cz`** (+ `www`) 301 přesměrovává na `vykopy-sazava.cz`
  (samostatný Pages projekt `minibagr-redirect` s catch-all `_redirects`).

## Co ještě doplnit

- **Fotky** — placeholdery nahradit reálnými snímky (viz `FOTKY.md`)
- **Ceny** — v ceníku jsou `[CENA]` k doplnění
- **IČO** — v patičce `[doplnit]`
- **E-mail** — web počítá s `info@vykopy-sazava.cz`
- **Formulář** — poptávka teď otevírá e-mailového klienta (`mailto`). Pro odesílání na
  pozadí nasadit Netlify Forms nebo Formspree (obsluha je v `<script>` na konci
  `index.html`).

## Poznámky

- Tajné hodnoty patří do `.env` (je v `.gitignore`, necommituje se).
