# SERVIS PC Závada — web

Statický web (3 stránky: Domů / Služby / Kontakt). Žádný build krok — čisté HTML + CSS + lokální fonty/obrázky. Nasaditelné na jakýkoli statický hosting (Vercel, Netlify, …).

## Struktura
- `index.html`, `sluzby.html`, `kontakt.html` — stránky
- `styles.css` — sdílený design systém (barvy/fonty/komponenty v `:root`)
- `assets/` — fonty (Archivo, Source Sans 3) + obrázky
- `vercel.json` — cache hlavičky pro `/assets/*`, bezpečnostní hlavičky
- `sitemap.xml`, `robots.txt`

## Nasazení na Vercel
1. Push do GitHubu (viz níže).
2. vercel.com → **Add New → Project → Import** tento repozitář.
3. Framework Preset: **Other**, Build Command: *(prázdné)*, Output Directory: `./`.
4. **Deploy** → dostaneš URL `…vercel.app`, kterou pošleš dál.

## Poznámka
`<link rel=canonical>`, `sitemap.xml` a Open Graph míří na `https://www.pczavada.cz`.
Při nasazení na jinou (preview) doménu je to v pořádku; před ostrým spuštěním nastav
v repu cílovou doménu.

Zdroj pro úpravy (mimo tento repo): `~/pcz-aurora/_spa-source.html` + `node build-pages.mjs`.
