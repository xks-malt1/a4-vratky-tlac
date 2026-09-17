# a4-vratky-tlac

Jednoduchý nástroj v prehliadači na tlač **A4 krycích hárkov na palety a klietky s vratkami**.
Nahrádza ručné písanie fixkou — hárky sú vždy čitateľné a rovnaké.

Bez inštalácie, bez servera, bez internetu. Stačí otvoriť `index.html` v prehliadači.

## Ako to funguje

1. Klikneš na tlačidlo klienta → pridá sa jeden hárok (predvolene **VRATKY**).
2. Prípadne zvolíš iný typ (T Return, T Return COD, Claim Assistant) alebo napíšeš vlastný.
3. **Vytlačiť všetko** → každý riadok v zozname sa vytlačí ako samostatná A4.

Rozloženie hárku:

- **1. riadok:** `KLIENT VRATKY` — vždy na jednom riadku, písmo sa automaticky prispôsobí dĺžke
- **2. riadok:** iba ak je zvolený špeciálny typ (napr. `T RETURN COD`)
- **stred:** vyznačená zóna na nalepenie expedičného štítku (dá sa vypnúť)
- **vpravo dole:** dátum (voliteľný, používa sa len výnimočne)

Ďalšie voľby: červená / čierna farba, orientácia na šírku alebo na výšku, počet kópií.

## Zoznam klientov

V repozitári sú len **ukážkové** hodnoty (`KLIENT A`, `KLIENT B`, ...). Nahraď ich vlastnými.
Priorita načítania:

1. **`klienti.js`** — načíta sa automaticky pri každom otvorení stránky.
   Jeden klient na riadok, v úvodzovkách, s čiarkou na konci.
2. **`klienti.txt`** — načítaš tlačidlom *„Načítať klientov z .txt"* priamo v aplikácii.
   Jeden klient na riadok, riadky začínajúce `#` sa ignorujú. Uloží sa do prehliadača,
   takže pri ďalšom otvorení sa načítavať nemusí.
3. **Vstavaný zoznam** v `index.html` — záloha, ak prvé dve možnosti chýbajú.

Tlačidlo *„Predvolený zoznam"* vráti vstavané hodnoty.

## Súbory

| Súbor | Popis |
|---|---|
| `index.html` | celá aplikácia (HTML + CSS + JS v jednom súbore) |
| `klienti.js` | zoznam klientov načítaný automaticky |
| `klienti.txt` | alternatívny zoznam načítaný tlačidlom |

## Tipy pri tlači

- V dialógu tlače nastav **okraje na minimum** a vypni hlavičky a päty prehliadača.
- Orientáciu papiera nastav rovnako ako v aplikácii (na šírku / na výšku).
