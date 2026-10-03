# mybluevan.nl

Statische website van My Blue Van: alleen HTML, CSS en een beetje JavaScript. Er is geen CMS, database of plugin nodig.

## Wat staat waar

| Bestand | Wat |
|---|---|
| `index.html` | De hele site |
| `lyrics.js` | Songteksten; plak nieuwe teksten hier |
| `img/` | Foto's, hoezen, video-previews en de achtergrondclip |
| `fonts/` | Lettertypen (lokaal, dus geen verzoeken naar Google) |
| `favicon.svg` | Het icoontje in het browsertabblad |
| `.nojekyll` | Zorgt dat GitHub Pages de bestanden ongewijzigd serveert |

## Online zetten met GitHub Pages (gratis)

1. Log in op GitHub en maak een nieuwe repository, bijvoorbeeld `mybluevan-site` (Public).
2. Klik op **Add file → Upload files** en sleep de **inhoud** van deze map erin (dus `index.html`, `img`, `fonts`, enzovoort, niet de map zelf). Klik op **Commit changes**.
3. Ga naar **Settings → Pages**. Kies bij *Source* **Deploy from a branch**, branch **main**, map **/ (root)**, en klik op **Save**.
4. Na een minuut staat de site op `https://<jouw-gebruikersnaam>.github.io/mybluevan-site/`.

## Eigen domein mybluevan.nl koppelen

1. Vul in GitHub bij **Settings → Pages → Custom domain** `mybluevan.nl` in en klik op **Save**.
2. Pas bij Strato de DNS van mybluevan.nl aan:
   - **A-records** voor `@` (het domein zelf), alle vier:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - **CNAME** voor `www` → `<jouw-gebruikersnaam>.github.io`
   - Verwijder oude A- of AAAA-records die nog naar de Strato-webhosting wijzen.
3. Wacht tot GitHub het domein heeft gecontroleerd (dat kan van een paar minuten tot een paar uur duren). Vink daarna **Enforce HTTPS** aan.
4. Werkt alles? Dan kun je het webhostingpakket bij Strato opzeggen. Houd alleen de domeinregistratie aan.

## Iets aanpassen

- **Tekst:** open `index.html` in GitHub, klik op het potloodje, pas aan en klik op **Commit**. Binnen een minuut staat het online.
- **Songteksten:** op dezelfde manier in `lyrics.js`.
- **Nieuwe foto:** upload hem in de map `img` en verwijs ernaar in `index.html`.

Tip: maak een gratis GitHub-*organisatie* (bijvoorbeeld "mybluevan") en zet de repository daar. Dan kunnen Bas en Dennis ook wijzigingen doen, en staat de site niet aan één persoonlijk account vast.
