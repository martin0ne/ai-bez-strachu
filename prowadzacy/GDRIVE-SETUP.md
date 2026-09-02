# Google Drive — setup bazy wiedzy kursu (krok po kroku, ~15 min)

> Folder = zamknięta przestrzeń kohorty. Zasada pochodzenia: pliki rodzą się w repo (GitHub, master) → wersje dla uczestników trafiają tu (Drive) → linki w Discordzie. Nie edytujemy materiałów „w" Drive — edytujemy w repo, aktualizujemy w Drive.

---

## Krok 1 — Struktura folderów (3 min)

Drive → Moje dysk → Nowy folder: **`OSNOWA EDU — Grupa 1`**

```
OSNOWA EDU — Grupa 1/
├── 00-START-TUTAJ
├── 01-Materiały-sesji
│   ├── S1-pierwsze-kroki
│   ├── S2-przepisy
│   ├── S3-maile-i-formula
│   └── S4-bezpieczeństwo-i-nawyk
├── 02-Narzędzia
├── 03-Twoje-dokumenty      (szablony do skopiowania — uczestnik ma „Plik → Utwórz kopię")
├── 04-Feedback
│   ├── Kolektor (arkusz)
│   └── Raporty-tygodniowe
└── 05-Onboarding
```

Udostępnij folder główny: **kohorta = „Współtwórca" na folderach 02–03 (muszą tworzyć kopie), „Komentator" na 01, „Czytelnik" na 00 i 05.** Prościej na start: udostępnij cały folder jako Współtwórca zaufanej grupie #1 i pilnuj porządku.

## Krok 2 — Pliki do wgrania (5 min)

| Plik (z repo) | Format w Drive | Gdzie |
|---|---|---|
| Ściągawka A4 (HTML → PDF przez Chrome: Otwórz → Drukuj → Zapisz jako PDF) | **PDF** (do druku, nie do edycji) | 02-Narzędzia |
| Instrukcja asystenta (poziom grupy) | **Dokument Google** (do skopiowania uczestnikiem) | 02-Narzędzia |
| Plan JEŚLI-TO (z pustymi liniami) | **Dokument Google** — uczestnik robi „Utwórz kopię" i wypełnia | 03-Twoje-dokumenty |
| 3-check weryfikacja | **Dokument Google** | 02-Narzędzia |
| Czerwona lista | **PDF** (poster do druku) | 02-Narzędzia |
| Checklist onboarding D−3/D−1 | **Dokument Google** | 05-Onboarding |
| Notatka po sesji (prowadzący, tylko Ty) | **Dokument Google** | 01-Materiały-sesji/S1 |

**Konwersja MD → Dokument Google:** otwórz .md, zaznacz wszystko, wklej do nowego Dokumentu — nagłówki popraw ręcznie (albo użyj `pandoc -s plik.md -o plik.docx` i wgraj .docx — Drive sam skonwertuje; pandoc masz przez homebrew).

## Krok 3 — Dokument „00-START-TUTAJ" (treść gotowa)

Nowy Dokument Google, tytuł: **START — przeczytaj to pierwsze**. Treść:

```
START — 3 kroki przed pierwszą sesją

KROK 1 (dzień −3, 10 min)
Przeczytaj: czym jest AI (bardzo zaawansowana podpowiedź następnego fragmentu —
nie wie, nie sprawdza, ale dobrze układa). Link do bazy wiedzy: [LINK]

KROK 2 (dzień −1, 10–15 min)
Załóż konto AI (ChatGPT / Gemini / Claude / Kimi — wybierz JEDNO) i wyślij
pierwsze pytanie z listy. Kreator: [LINK strona onboardingowa]

KROK 3 (dzień 0)
Wchodzisz na sesję. Masz konto i pierwszą rozmowę za sobą.

ZANIM COKOLWIEK WKLEISZ DO AI:
„Wkleiłbym to obcej osobie w mailu?" Jeśli nie — nie wklejaj.
(czerwona lista: folder 02-Narzędzia)

GDZIE CO ZNAJDZIESZ:
- Materiały po sesjach: 01-Materiały-sesji
- Ściągawka, instrukcja asystenta, plan JEŚLI-TO: 02-Narzędzia
- Twoje dokumenty (rób „Utwórz kopię"!): 03-Twoje-dokumenty
- Pytania i rozmowa: Discord → [LINK]
```

## Krok 4 — Uprawnienia i higiena (2 min, ważne)

- **„Ustawienia udostępniania" folderu głównego → wyłącz „Widzący mogą pobierać, drukować i kopiować"** TYLKO dla dokumentów z danymi uczestników (raporty feedbacku) — materiały kursowe niech będą normalne (uczestnicy drukują ściągę).
- **Brak „każdy z linkiem"** na folderach z komentarzami uczestników — tylko konkretni ludzie.
- Twoje dokumenty robocze (notatki po sesjach, raporty feedbacku przed anonimizacją) → NIE w tym folderze, tylko w Twoim prywatnym Drive. Do kohorty idą już anonimizowane.

## Krok 5 — Rytm (jak Drive żyje w tygodniu)

| Moment | Co robisz |
|---|---|
| Po każdej sesji ( tego samego dnia) | wgrywasz do `01-Materiały-sesji/SX`: PDF ściągii (jeśli nowa), notatka prowadzącego (prywatna), link do nagrania (jeśli będzie) → link + ogłoszenie na Discordzie |
| Niedziela (10 min) | eksport feedbacku → synteza → raport do `04-Feedback/Raporty-tygodniowe` |
| Przed sesją | checklisty/onboarding do `05-Onboarding` |

---

*Powiązane: DISCORD-SETUP.md (linki między środowiskami) · INFRA-DISCORD-GOOGLE.md (architektura) · REPO-SZKIELET (GitHub = master)*
