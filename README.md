# DateUp Pages

Publiczny mini-serwis dla projektu DateUp, przygotowany do publikacji przez GitHub Pages.

Repo zawiera gotowe statyczne strony, ktore mozna podpiac m.in. w:

- Google Play
- App Store Connect
- materialach supportowych i legalowych projektu

## Co jest w repo

- `index.html` - strona startowa "Legal Hub"
- `privacy.html` - publiczna polityka prywatnosci
- `delete-account.html` - publiczna strona usuwania konta
- `styles.css` - style calego mini-serwisu
- `site.js` - prosty przelacznik jezyka PL / EN
- `.nojekyll` - wylaczenie przetwarzania Jekyll w GitHub Pages
- `privacy-policy-pl.md` - robocza wersja tresci polityki prywatnosci

## Jak to dziala

To jest zwykly statyczny serwis HTML/CSS/JS.

Nie wymaga buildu, frameworka ani instalacji zaleznosci. Po wlaczeniu GitHub Pages repo moze byc publikowane bezposrednio z glownego branchu `main` i z folderu root.

## Uruchomienie lokalne

Najprosciej:

1. Otworz `index.html` w przegladarce.

Albo lokalnie przez prosty serwer, jesli wolisz testowac jak strone webowa:

```powershell
python -m http.server 8000
```

Potem otworz:

`http://localhost:8000`

## Co trzeba uzupelnic przed publikacja

Przed podaniem linkow do sklepow lub uzytkownikow podmien wszystkie placeholdery:

- `[UZUPELNIJ: ...]`
- `[FILL IN: ...]`

Najwazniejsze miejsca do uzupelnienia:

- dane administratora danych
- adres e-mail do spraw prywatnosci
- adres e-mail lub formularz do usuwania konta
- okresy retencji danych
- finalna lista dostawcow / podmiotow przetwarzajacych
- informacje o platnosciach po uruchomieniu Premium

## Publikacja w GitHub Pages

Aktualny uklad repo zaklada publikacje z katalogu glownego repozytorium, czyli z `/(root)`.

Po publikacji adres bedzie mial zwykle format:

`https://NAZWA-UZYTKOWNIKA.github.io/DateUp-pages/`

Podstrony:

- `https://NAZWA-UZYTKOWNIKA.github.io/DateUp-pages/privacy.html`
- `https://NAZWA-UZYTKOWNIKA.github.io/DateUp-pages/delete-account.html`

## Klikniecia w GitHub

Po wypchnieciu repo na GitHub:

1. Wejdz w repozytorium `DateUp-pages`.
2. Kliknij `Settings`.
3. W lewym menu kliknij `Pages`.
4. W sekcji `Build and deployment` ustaw `Source` na `Deploy from a branch`.
5. W sekcji `Branch` wybierz:
   - branch: `main`
   - folder: `/(root)`
6. Kliknij `Save`.
7. Poczekaj, az GitHub pokaze publiczny adres strony.

## Po publikacji

Warto od razu sprawdzic:

- czy otwiera sie `index.html`
- czy dziala `privacy.html`
- czy dziala `delete-account.html`
- czy przelacznik jezyka PL / EN dziala poprawnie
- czy nie zostaly zadne placeholdery typu `[UZUPELNIJ]` albo `[FILL IN]`

## Uwaga

Jesli kiedys przeniesiesz pliki do folderu `docs`, wtedy w GitHub Pages trzeba bedzie zmienic zrodlo publikacji z `/(root)` na `/docs`.
