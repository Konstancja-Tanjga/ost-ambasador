# Generatory grafik Ogólnopolskiej Strefy Talentu

Dwie strony, na których ambasadorki, ambasadorzy i sympatycy Ogólnopolskiej
Strefy Talentu (OST) robią z własnego zdjęcia grafikę do posta albo story.
Zdjęcie nie opuszcza przeglądarki.

- Dla ambasadorów: [ost-ambasador.vercel.app/ambasador](https://ost-ambasador.vercel.app/ambasador/)
- Dla wspierających: [ost-ambasador.vercel.app/wsparcie](https://ost-ambasador.vercel.app/wsparcie/)

## Skąd ten projekt

OST poprosiła kilkanaście osób, żeby ogłosiły start programu w swoich mediach
społecznościowych. Część z nich zapytała o ramkę, w którą mogłyby wstawić
swoje zdjęcie.

W pierwszej wersji ramki koralowy pasek przechodził ambasadorowi przez szyję
jak pasek cenzury w kryminale. Druga wersja wymagała programu graficznego, a
kilkanaście osób oznaczało kilkanaście pytań „gdzie mam kliknąć?”. Zamiast
pliku do samodzielnego składania zrobiłam więc narzędzie, które składa
grafikę samo: wgrywasz zdjęcie, wybierasz hasło i format, pobierasz PNG.

## Jak zbudowana jest grafika

Znak OST składa się z dwóch symboli logiki: **∀** („dla każdego”) i **∃**
(„istnieje”). Razem czytają się jako hasło programu: *dla każdego ucznia
istnieje talent*.

Zdjęcie stoi w ramie ∃, bo osoba na zdjęciu mówi, że taki program istnieje i
że go wspiera. Żaden element graficzny nie zachodzi na zdjęcie, więc twarz
zostaje nietknięta. Koralowa kreska ucznia stoi obok zdjęcia, nad hasłem. Na
dole grafiki są podpis „Bo dla każdego ucznia istnieje talent.” i adres
www.ost.edu.pl.

Zdjęcia z telefonu, z konferencji, z ogrodu i z pokoju nauczycielskiego nie
pasują do siebie kolorem. Generator domyślnie nakłada na nie duotone w
kolorach OST, granacie i ciepłej bieli, dzięki czemu posty kilkunastu osób
układają się w jedną kampanię. Przycisk „Oryginalne” zostawia kolory zdjęcia.

## Dwa generatory

| Strona | Dla kogo | Hasło na grafice |
| --- | --- | --- |
| `/ambasador` | Ambasadorki i ambasadorzy programu | „Jestem ambasadorką Ogólnopolskiej Strefy Talentu.” albo „Jestem ambasadorem Ogólnopolskiej Strefy Talentu.” |
| `/wsparcie` | Wszyscy, którzy chcą pokazać, że są z nami | „Wspieram inicjatywę Ogólnopolska Strefa Talentu.”, „Kibicuję Ogólnopolskiej Strefie Talentu.” albo „Popieram Ogólnopolską Strefę Talentu.” |

## Jak użyć

1. Wgraj zdjęcie, najlepiej pionowe, z twarzą w górnej części kadru.
2. Wybierz hasło.
3. Wybierz format: post 4:5 (1080 × 1350 px) albo story 9:16
   (1080 × 1920 px).
4. Przeciągnij zdjęcie na podglądzie, żeby ustawić kadr. Suwak powiększa
   zdjęcie do trzech razy. Z klawiatury strzałki przesuwają zdjęcie, a plus i
   minus zmieniają powiększenie.
5. Zostaw „Kolory OST” albo wybierz „Oryginalne”.
6. Pobierz grafikę. Plik PNG ma nazwę w rodzaju
   `OST_ambasador_ambasadorka_post.png`.

## Prywatność

Zdjęcie nie opuszcza urządzenia. Generatory nie mają serwera aplikacji, bazy
danych ani logowania. Grafika powstaje w przeglądarce i trafia prosto do
folderu z pobranymi plikami. Z zewnątrz strona pobiera tylko fonty z Google
Fonts.

## Technicznie

Każdy generator to jeden plik `index.html` z HTML, CSS i JavaScriptem, bez
zależności i bez kroku budowania. Do publikacji wystarczy dowolny hosting
plików statycznych; wersja publiczna stoi na Vercelu.

Oba pliki różnią się tylko tytułem, wstępem i wartością `version`, która
wybiera zestaw haseł. Zmianę wyglądu albo działania trzeba więc wprowadzić w
obu plikach.

Żeby uruchomić generator lokalnie, otwórz `ambasador/index.html` albo
`wsparcie/index.html` w przeglądarce.

## Autorka

Identyfikację wizualną OST z konceptem „∀∃ Dla każdego istnieje”, pomysł na
generatory i ich kod przygotowała **Konstancja Tanjga**.
Portfolio: [konstancja-tanjga.github.io/portfolio-site](https://konstancja-tanjga.github.io/portfolio-site/)
