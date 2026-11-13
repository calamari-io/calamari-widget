# Strona widżetu Calamari

Opublikowana strona prototypu rozszerzenia Chrome do Calamari.
**To repozytorium jest publiczne, bo tylko z publicznego repo działa GitHub Pages
na planie Free.** Trafia tu wyłącznie treść, która i tak jest publiczna: copy strony,
zrzuty interfejsu i paczka rozszerzenia.

Kod rozszerzenia, testy i rozpoznanie API siedzą w prywatnym
[`calamari-io/calamari-chrome-extension`](https://github.com/calamari-io/calamari-chrome-extension).

| Adres | Plik | Dla kogo |
| --- | --- | --- |
| [`/`](https://calamari-io.github.io/calamari-widget/) | `index.html` | adres zachowany z poprzedniego hostingu |
| [`/v1/`](https://calamari-io.github.io/calamari-widget/v1/) | `v1/index.html` | wersja dla pracownika |
| [`/v2/`](https://calamari-io.github.io/calamari-widget/v2/) | `v2/index.html` | wersja dla managera |

Wszystkie trzy strony pobierają tę samą paczkę z `v1/calamari.zip`.
`calamari.zip` w katalogu głównym to kopia pod starym linkiem.

## Publikacja

Nie ma kroku wdrożenia. `git push` na `main` i GitHub Pages przebudowuje stronę
(zwykle poniżej minuty).

Nowe wydanie rozszerzenia = podmiana `v1/calamari.zip` i `calamari.zip` oraz numeru
wersji w `?v=` i w treści wszystkich trzech stron. Do 13.11.2026 robił to skill
`zaktualizuj-wtyczke` przez FTP na `87media.pl`; po przeprowadzce robi to push tutaj.

## Dlaczego ścieżki są względne

Na starym hostingu strona stała w `/calamari/`, więc odwołania były bezwzględne
(`/calamari/assets/...`). Teraz są względne, dzięki czemu ta sama treść działa pod
adresem Pages, pod własną domeną i otwarta wprost z dysku.
