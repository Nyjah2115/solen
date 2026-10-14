# Solen® — strona do nagrania rolki

Otwórz `index.html` w Chrome lub Safari, włącz pełny ekran i scrolluj.

## Skróty
- **A**: auto-scroll przez całą stronę (ok. 16 s, równe tempo, najlepszy do nagrywania). Ponowne A zatrzymuje, kółko myszy też.
- **C**: ukryj / pokaż kursor.
- **0**: powrót na górę.

## Co jest czym
- `frames/hero/`: klatki wideo hero, kamera jedzie nad modelkę (Kling 3.0, OpenArt).
- `frames/product/`: klatki obrotu okularów, start z widoku z przodu (Kling 3.0, OpenArt).
- `source/`: oryginały z OpenArt (obrazy GPT Image 2 + oba wideo .mp4); `source/old/` to pierwsza wersja.

## Przejście (jak w rolce)
1. Hero kończy się widokiem z góry, okulary na środku.
2. Modelka się rozmywa, tło zostaje jasne.
3. Ostre okulary produktowe pojawiają się dokładnie na jej okularach (`mix-blend-mode: screen`, wyrównanie w `MATCH`).
4. Tło gaśnie do czerni, okulary rosną i zaczynają się obracać.

## Strojenie (w `index.html`)
- `.track { height: 900vh }`: długość scrolla (więcej = wolniej).
- `T = { ... }`: kiedy gra hero, kiedy jest „fade”, kiedy obraca się produkt.
- `data-in` / `data-out` na `.callout`: kiedy pojawiają się teksty.
- `AUTO_SECONDS`: czas auto-scrolla.
