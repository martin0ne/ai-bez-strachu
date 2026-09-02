# OSNOWA EDU — architektura programów edukacyjnych (system „jak leki")

**Data:** 02.09 · v1.1 (korekty po DR wiek-nauka + DECYZJE-DYDAKTYCZNE ✅) · **Status:** ZATWIERDZONY.
**Model potwierdzony dowodowo:** poziomy = KOMPETENCJE (triage wykonaniowy), wiek = warstwa opakowania (tempo, przykłady, wsparcie). Metaanaliza 8 776 efektów: prior knowledge przewiduje wynik niezależnie od wieku (H1 ✅). Autonomia = funkcja znajomości domeny, nie wieku (H6 obalona).

---

## 1. Model: recepta, nie półka

Uczestnik nie wybiera „kursu dla swojego rocznika". Przechodzi **triage** (3 pytania past-behavior na starcie, nie formularz-marketingowy) i dostaje **ścieżkę**:

```
TRIAGE (3 pytania)
├─ O1: Jak często otwierasz jakiekolwiek AI?        (styczność)
├─ O2: Co ostatnio zrobiłeś ręcznie, co mogło pójść do AI?  (świadomość)
└─ O3: Znasz pojęcia: konto w chmurze, plik PDF, udostępnianie linku?  (technika)
        ↓
ŚCIEŻKA = moduły z puli OSNOWA EDU + rytm + format dopasowane do wyniku
```

**Trzy osie:**

| Oś | Wartości | Co decyduje |
|---|---|---|
| **Grupa (kohorta)** | 10–15 · 15–25 · 26–35 · 36–50 · 50+ | ton, przykłady, tempo, format społeczności, RODO/rodzice |
| **Styczność z AI** | zero · niby-używający · mocny | punkt wejścia w drabinie (zaufanie vs mapa vs workflow) |
| **Poziom techniczny** | niski · średni · wysoki | głębokość modułów technicznych, długość setupu |

## 2. Nazwy poziomów (dawkowanie — bez cyfr)

Cyfry wiekowe w nazwie = „ten kurs nie jest dla mnie". Poziomy entry mówią **od czego startujesz**:

| Poziom | Dla kogo (styczność × technika) | Metafora | Odpowiednik stary |
|---|---|---|---|
| **OSNOWA START** | zero styczności, technika niska | „pierwsze kroki" | był 40+ |
| **OSNOWA HORIZON** | niby-używający, technika średnia | „widzisz horyzont, nie znasz mapy" | był 20+ (część) |
| **OSNOWA FLOW** | niby-używający/mocny, technika średnia/wysoka | „z czatu do przepływu" | był 20+ (rdzeń) |

*(Dalsze poziomy — PRAXIS: automatyzacje i własne systemy; załoga: AI w firmie — są w mapie produktowej, nie teraz.)*

**Weryfikacja nazw (etyka, nie gust):** „Start/Horizon/Flow" nie rani, nie dzieli po wieku, działa po polsku i w nazwie domeny. Do testu z 5 osobami (kohorta) — bramka ludzka przed kanonem.

## 3. Mapa 5 grup × poziomy (macierz produkowa)

| Grupa | START | HORIZON | FLOW | Uwagi formatowe |
|---|---|---|---|---|
| **10–15** | ✓ (kontekst szkolny, **zgoda rodzica**, bezpieczeństwo = priorytet #1, RODO-minor) | — (za wcześnie) | — | stacjonarnie/klub, rodzic w pętli; nie v1 |
| **15–25** | ✓ (nie-techniczni) | ✓ (głównie ta grupa w HORIZON) | ✓ (techniczni, studenci IT-adjacent) | Discord = naturalne środowisko |
| **26–35** | rzadko | ✓ | ✓ | praca + freelancerzy + młodzi przedsiębiorcy |
| **36–50** | ✓ (dużo) | ✓ | rzadko | praca biurowa, „niby-używający" często |
| **50+** | ✓ (głównie) | rzadko | — | wolniejsze tempo, Sesja 0 częściej, Zoom + stacjonarnie |

**Treść modułów = wspólna pula; grupa decyduje o DOBORZE i OPAKOWANIU** (przykłady, tempo, platforma), nie o napisaniu wszystkiego od nowa. To jest cała ekonomia systemu: jeden rdzeń modułów, 5 opakowań.

## 4. Progresja modułów — wspólna pula, różne drabiny

```
PULA MODUŁÓW (rdzeń OSNOWA EDU):
M0  Setup + konto                    (START, część HORIZON)
M1  Zaufanie: co to AI, pierwsze pytanie        (START)
M2  Czytanie/streszczanie — gotowe przepisy     (START)
M3  Maile + iteracja                            (START, HORIZON)
M4  Formuła promptu KIM→CO→FORMA                (START późno, HORIZON, FLOW szybko)
M5  Workflow: kontekst, etapy, szablony         (HORIZON końcówka, FLOW)
M6  Mapa możliwości: pliki, projekty, pamięć, DR (FLOW; HORIZON w skrócie)
M7  Własne workflow ×2 (nauka/praca/firma)      (FLOW)
M8  Granice: prywatność, prawa, uczciwość       (wszyscy — pozycja zależna od poziomu)
M9  Nawyk: JEŚLI-TO + follow-up D14             (wszyscy, zawsze na końcu)
M10 Załoga: AI w mikrofirmie                   (FLOW, segment przedsiębiorców)
```

| Poziom | Drabina | Rytm |
|---|---|---|
| **START** | M0 → M1 → M2 → M3 → M4 → M8(mini) → M9 | 3–4 tyg., sesje 90 min, mikro 5–15 min |
| **HORIZON** | M4 → M5 → M6(skrót) → M8 → M9 | 2–3 tyg., hybryda kohortowa |
| **FLOW** | M6 → M5 → M7 → M10 → M8 → M9 | 3 tyg., hybryda + Discord centralnie |

**Kryterium sukcesu wspólne:** ≥3 realne zadania bez prowadzącego w 14 dni po ostatniej sesji (miara behawioralna, jedna dla całego systemu — porównywalność między grupami).

## 5. Co się zmienia w istniejących plikach (przemapowanie)

| Było | Staje się |
|---|---|
| kurs-ai-40+ („AI bez strachu") | **START** (grupy 36–50 i 50+; nazwa kursu zostaje „AI bez strachu" jako tytuł produktu dla 50+? — patrz bramka ludzka niżej) |
| kurs-ai-20+ („AI 20+") | rdzeń rozpada się na **HORIZON** (M4–M6 skrót) i **FLOW** (M6–M10) |
| PLAN-7-DNI | wariant intensywny START (pozostaje) |
| KONCEPT 20+ §segmenty | wpisane w macierz §3 (student/early career/przedsiębiorca = warianty FLOW/HORIZON) |

**OSNOWA (folder warsztatowy):** `~/OSNOWA/projekty/` dostaje nowy folder-łączący **`osnowa-edu/`** (system: triage, macierz, naming, infra) — kursy wiekowe zostają jako archiwa robocze ich pierwszych wersji. Repo GitHub: struktura przechodzi na `start/ · horizon/ · flow/ · wspolne/`.

## 6. Bramka ludzka (decyzje Marcina przed kanonem)

1. **Nazwy poziomów:** START / HORIZON / FLOW — ok, czy proponujesz własne? (kontrtest na 5 osobach przy kohorcie)
2. **„AI bez strachu"** — zostaje jako tytuł produktu START dla 50+ (godność, spokój — NAMING.md), czy odchodzi do archiwum?
3. **10–15:** wchodzimy w ogóle w minorów w v1 (RODO-minor, zgody rodziców, bezpieczeństwo jako moduł #1)? Moja rekomendacja: **nie** — v1 = 15+, minorzy jako osobna decyzja produktowa z prawnikiem.
4. **Triage 3-pytaniowy** — ok jako wejście do systemu?

## 7. Następne kroki (po decyzjach z §6)

1. `osnowa-edu/` — plik-system (ten dokument uzupełniony o decyzje) + triage
2. Repo GitHub: restrukturyzacja na poziomy (start/horizon/flow/wspolne) + redirect starej struktury
3. Scenariusze: S1 START już jest; najbliższe = HORIZON Live 1 (mapa możliwości wg sylabusa 20+)
4. Strona onboardingowa: triage zamiast „wybierz kurs" — 3 pytania → ścieżka → Discord

---

*Powiązane: KONCEPT 20+ (segmenty) · PLAN-KURSU 40+ · NAMING.md (wiral vs produkt) · INFRA-DISCORD-GOOGLE.md (kanały per kohorta)*
