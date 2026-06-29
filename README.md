# Kalkulator cięcia laserowego

Standalone HTML — szybka wycena cięcia laserowego blach (stal czarna / nierdzewna / aluminium),
z walidacją grubości, ściągawką w wysuwanym panelu, kosztami własnymi i wyliczaniem zysku.

Całość to jeden plik `index.html` — działa offline, bez backendu, bez budowania.

## Uruchomienie lokalne

Otwórz `index.html` w przeglądarce. To wszystko.

## Wdrożenie na Render (static site)

1. Wepchnij to repo na GitHub (patrz niżej).
2. Na https://dashboard.render.com kliknij **New +** → **Static Site**.
3. Podłącz konto GitHub i wybierz to repozytorium → **Connect**.
4. W formularzu:
   - **Build Command:** zostaw puste
   - **Publish Directory:** wpisz `.` (kropka)
5. Kliknij **Deploy Static Site**.

Render zbuduje stronę i da adres `*.onrender.com`. Każdy push na gałąź `main` automatycznie ją zaktualizuje.

> Alternatywnie: w repo jest `render.yaml` — możesz użyć **New + → Blueprint**, wskazać repo i Render skonfiguruje się sam.

## Alternatywa: GitHub Pages (jeszcze prościej, też darmowe)

Settings → Pages → Source: `main` / folder `/ (root)` → Save. Adres `*.github.io` w ~minutę.

## Aktualizacja

Edytuj `index.html`, zatwierdź i wypchnij:

```bash
git add index.html
git commit -m "Aktualizacja kalkulatora"
git push
```

Render (lub Pages) wdroży zmiany automatycznie.
