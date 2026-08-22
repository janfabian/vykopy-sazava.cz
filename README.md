# vykopy-sazava.cz

Web pro výkopové práce minibagrem — **Ionut Gabor**, Sázava a okolí (okres Benešov,
Posázaví).

Jednostránkový statický web, bez závislostí a build kroku. Design vychází z návrhu
z Claude Design („blueprint" styl, písmo Barlow / Barlow Condensed).

## Struktura

- `index.html` — celá stránka (sekce: hero, služby, proč malý bagr, realizace, ceník,
  o mně, oblast působení, reference, kontakt)
- `assets/ds.css` — design systém (barevné tokeny a komponenty)
- `FOTKY.md` — prompty pro AI generátor obrázků + návod, jak fotku vložit

Otevři `index.html` v prohlížeči — nic víc není potřeba.

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
