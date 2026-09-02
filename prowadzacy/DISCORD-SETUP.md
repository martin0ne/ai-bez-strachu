# Discord — setup serwera „OSNOWA EDU" (krok po kroku, ~20 min)

> Wykonujesz raz. Po tym: link zaproszenia wchodzi na stronę onboardingową i do maili.

---

## Krok 1 — Serwer (2 min)

1. Discord → lewy dolny **+** → „Utwórz własny serwer" → „Dla mnie i moich znajomych"
2. Nazwa: **`OSNOWA EDU — Grupa 1`** (kohorta #1; kolejne kohorty = osobne serwery albo osobne kategorie — decydujemy po pilotażu)
3. Ikona: dowolna neutralna (bez brandu MATKA-00/Osnowa — embargo)

## Krok 2 — Ustawienia bezpieczeństwa (5 min, ważne!)

Ustawienia serwera (nazwa → ikonka zębatki):

- **Zabezpieczenia → Poziom weryfikacji: „Średni"** (musi być zarejestrowany 5+ min) — bloki boty
- **Zabezpieczenia → Filtr treści: skanuj wiadomości wszystkich członków** (40+ grupa — mniejsza spam-elastyczność)
- **Role → Utwórz role:**
  - `Prowadzący` (Ty) — kolor ciemny, wszystkie uprawnienia
  - `Uczestnik` — domyślna dla zaproszonych: pisze wszędzie, NIE zarządza
  - `Gość` — na czekanie przed weryfikacją (opcja)
- **Członkowie → wyłącz „Zezwalaj na DM od członków serwera"** dla roli Uczestnik (ochrona uczestników przed sobą nawzajem; prowadzący może DM zawsze)

## Krok 3 — Kanały tekstowe (5 min)

Utwórz **kategorie** i kanały (dokładnie te nazwy — spójne z INFRA i materiałami):

**Kategoria: 📌 START (ktoś, kto wchodzi, widzi to pierwsze)**
- `#start-tutaj` — pin: 3 kroki onboarding + linki (Drive, repo, ściągawka)
- `#ogloszenia` — TYLKO prowadzący pisze (uprawnienia: Uczestnik = tylko czyta)
- `#przedstaw-sie` — imię (lub pseudonim) + czego oczekujesz od kursu

**Kategoria: 📚 SESJE**
- `#sesja-1-pierwsze-kroki`
- `#sesja-2-przepisy`
- `#sesja-3-maile-i-formula`
- `#sesja-4-bezpieczenstwo-i-nawyk`
  *(nazwy kanałów = kolejność z PLAN-KURSU; po każdej sesji pinujesz materiały z Drive)*

**Kategoria: 🔄 PRAKTYKA (między sesjami — tu żyje kurs na co dzień)**
- `#dziennik` — codziennie 1 zdanie „co dziś zrobiłem z AI" (mikro-zadania tu wracają)
- `#pokaz-wynik` — peer review: prompt + wynik; każdy komentuje 2 obce
- `#pytania` — wszystko o AI, kursie i zadaniach (merytoryka)

**Kategoria: 🛠 SERWIS**
- `#pomoc-techniczna` — konto, Zoom, dźwięk (nie merytoryka!)
- `#feedback` — ZEEBOT: sukces / problem / idea (patrz Krok 5)
- `#oflagowane-do-marcina` — tylko Ty widzisz sprawy eskalowane

## Krok 4 — Pin #start-tutaj (treść gotowa do wklejenia)

```
WITAJ W OSNOWA EDU — GRUPA 1

ZASADY (krótko):
1. Czerwona lista obowiązuje też tutaj — żadnych danych osobowych w wątkach
   (PESEL, hasła, dane innych, dokumenty zdrowotne). Pytaj „wkleiłbym to obcej
   osobie w mailu?" — jeśli nie, nie wklejaj.
2. Możesz używać pseudonimu. Decyzja Twoja.
3. Pytania merytoryczne → kanały sesji / #pytania-merytoryczne
   Technika (konto, dźwięk) → #pomoc-techniczna
   Feedback → #feedback
4. Każdy komentuje 2 obce wyniki w #pokaz-wynik — tak działa grupa.

LINKI:
- Biblioteka kursu (GitHub): https://github.com/martin0ne/ai-bez-strachu
- Materiały (Google Drive): [LINK PO UTWORZENIU]
- Ściągawka A4: [LINK PO UTWORZENIU]
- Instrukcja asystenta: [LINK PO UTWORZENIU]

PIERWSZE ZADANIE: [wpisujesz wg PLAN-KURSU — mikro-zadanie 24 h]
```

## Krok 5 — Kolektor feedbacku (2 wersje)

**Wersja NATYCHMIASTOWA (bez configu):**
- Kanał `#feedback` = uczestnicy piszą dowolnie; Ty raz w tygodniu eksportujesz (kopiujesz) zawartość i **wklejasz mi do Hermes** — robię syntezę wg formatu raportu (CO DZIAŁA / CO NIE DZIAŁA / IDEA / FLAGI).

**Wersja AUTOMATYCZNA (15 min, przed Live 1):**
1. Google Sheets → nowy arkusz `KOLEKTOR-FEEDBACK` (kolumny: DATA | KANAŁ | UCZESTNIK | TEKST | TYP | MODUŁ)
2. Discord → Ustawienia serwera → Integracje → **Webhooks** → Nowy webhook → kanał `#feedback` → skopiuj URL
3. W arkuszu: Rozszerzenia → Apps Script → wklej skrypt (podeślę gotowy) → konfiguracja triggera co 6 h
4. Discord z kolektora → raz w tygodniu: skrypt LLM robi syntezę → wynik do `/Feedback/Raporty` na Drive + webhook do `#ogloszenia`

*(Wybieramy wersję natychmiastową na start; automatyczną stawiamy razem, gdy grupa żyje.)*

## Krok 6 — Zaproszenie

- Ustawienia serwera → Zaproszenia → utwórz link: **nigdy nie wygasa, max 1 użycie na osobę** (kontrola kohorty)
- Link wchodzi: mail onboardingowy + strona onboardingowa (CTA „Dołącz do grupy")

---

*Zasady prywatności: pseudonimy OK · zero PII w wątkach · #oflagowane tylko dla Ciebie · raporty tygodniowe anonimizowane („uczestnik A")*
