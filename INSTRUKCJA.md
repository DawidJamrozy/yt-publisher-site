# Publikacja aplikacji Google (żeby logowanie nie wygasało co 7 dni)

Pliki w tym folderze: index.html (strona główna), privacy.html (polityka prywatności). Nazwa aplikacji na stronie = „YT Publisher” — w Google musi być TA SAMA nazwa.

## A. GitHub Pages (~3 min)
1. github.com → New repository → nazwa `yt-publisher-site` → **Public** (darmowe Pages działa tylko dla publicznych) → Create.
2. „uploading an existing file” → przeciągnij index.html i privacy.html → Commit changes.
3. Settings → Pages → Source: „Deploy from a branch” → Branch: `main`, folder `/ (root)` → Save.
4. Po 1–2 min strona działa pod: `https://<TWÓJ_LOGIN>.github.io/yt-publisher-site/` (sprawdź też `.../privacy.html`).

W repo są tylko te 2 strony — żadnych kluczy ani danych.

## B. Google Cloud (~3 min) — console.cloud.google.com, projekt z EA Uploader
1. Google Auth Platform → **Branding**:
   - App name: `YT Publisher`
   - User support email: Twój Gmail
   - Application home page: `https://<TWÓJ_LOGIN>.github.io/yt-publisher-site/`
   - Application privacy policy link: `https://<TWÓJ_LOGIN>.github.io/yt-publisher-site/privacy.html`
   - Authorized domains: `<TWÓJ_LOGIN>.github.io`
   - Developer contact: Twój Gmail → Save.
2. **Audience** → „Opublikuj aplikację” (Publish app) → potwierdź. Status: „W wersji produkcyjnej”.
   - Jeśli Google proponuje weryfikację — NIE wysyłaj, nie jest potrzebna (użytek własny). Jeśli publikacja się nie da — zrób zrzut ekranu dla Claude'a.

## C. Potem (z Claude)
Napisz „aplikacja opublikowana”. Claude zmieni uprawnienia na jedno (`youtube.force-ssl`) i poprosi o jednorazowe `setup.sh --reauth` (wybór kanału Everyday Ancestor). Od tej chwili logowanie nie wygasa.
