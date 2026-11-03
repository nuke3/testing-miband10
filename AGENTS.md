# AGENTS.md

## Projekt
Aplikacja Android (Kotlin) do odczytu danych z Mi Band 10 przez BLE.
Źródło prawdy: `docs/spec.md`. Nie zgaduj protokołu.

## Zasady
- Nie zmieniaj plików poza zakresem zadania.
- Nie zapisuj do opaski (write/characteristic write) bez wyraźnej zgody człowieka.
- Nie loguj auth key, adresów MAC ani danych zdrowotnych poza lokalnymi logami debugowania wyłączonymi w buildzie release.
- Dane przechowuj tylko lokalnie. Brak wysyłki w chmurze.
- Jeśli brakuje informacji, zapisz pytanie w `docs/open-questions.md` zamiast zgadywać.
- Każdą zmianę kończ podsumowaniem: co zmieniono, jakie testy uruchomiono, wynik.

## Komendy
- Build: `./gradlew assembleDebug`
- Testy: `./gradlew test`
- Lint: `./gradlew lint`

## Struktura
- `ble/` – skanowanie, połączenie, GATT
- `protocol/` – parsowanie ramek (po weryfikacji protokołu)
- `docs/` – spec, protocol, open-questions
