# Scenariusz Live 1 — HORIZON (OSNOWA EDU)

**Sesja 1 · 90 min · live (Zoom/„Sala główna") · moduł M6: Mapa możliwości**
**Grupa:** niby-używający AI (15–25 studenci/techniczni, 26–35 praca/freelance, 36–50 biurowi) — triage zakładające: otwierają AI, nie budują procesów.
**Cel uczestnika po Live 1:** widzi własną lukę „używam ≠ wykorzystuję" w liczbach (swojego audytu T0), zna 8 funkcji z mapy, uruchomił pierwszy mini-workflow z własnej top-3 luki.
**Fundamenty (eval GO):** H1 luka power-features (<10% casual users używa custom instructions) · worked-example effect (CLT) · peer learning = najsilniejszy czynnik 15–25 (profil grupy) · H6: autonomia rośnie z opanowaniem, nie z wieku.
**Materiały na ekran:** audyt T0 uczestników (przyniesiony) · strona onboardingowa (mapa) · lab-1 · repo (github.com/martin0ne/ai-bez-strachu).
**Mikro-po-Live (24 h):** przetestuj 2. funkcję z top-3 na realnym zadaniu (SYLABUS §Mikro T1).

---

## PRZED SESJĄ (checklista prowadzącego, −30 min)

- [ ] Discord otwarty na „Sala główna" (live TU, nie Zoom — jeśli grupa gotowa; fallback Zoom)
- [ ] Triage uczestników przeglądnięty: kto FLOW w grupie HORIZON (będzie tematem „test-out")
- [ ] Audyty T0: policzone średnie grupy (ile % Q/T/C/I/M) — przygotuj do pokazania na slajdzie
- [ ] Przygotowane 2 worked-examples na żywo (pierwszy: „zwykły prompt vs projekt+pliki"; drugi: custom instructions na własnym koncie)
- [ ] Discord: kanały sesji utworzone, pin materiałów gotowy

---

## 0:00–0:08 · OTWARCIE — „jestem tu z powodu"

**Prowadzący:**

„Nie będę was uczyć, czym jest AI — macie to za sobą i to jest dokładnie Wasza przewaga. Jestem tu z innego powodu: **każdy z was zostawia na stole 90% tego narzędzia**. Nie dlatego, że jest głupie — dlatego, że narzędzie rośnie szybciej niż nawyki. Ten kurs to nie nauka AI. To przebudowa sposobu, w jaki pracujecie."

**Runda skrócona (30 sek/os.):** imię + **jedno zadanie z ostatniego tygodnia, które robiłeś ręcznie, choć podejrzewasz, że AI dałoby radę**.

**Prowadzący zapisuje listę na żywo (widoczna dla wszystkich)** — to będzie „bank zadań" grupy do końca kursu. Zero komentowania jakości — tylko zbieranie.

*Dlaczego tak: personal relevance (Knowles) od pierwszej minuty; dla HORIZON nie budujemy zaufania — budujemy mapę własnych braków.*

## 0:08–0:20 · AUDYT GRUPY NA LICZBACH

**Udostępnij slajd/arkusz: średnie T0 grupy.**

**Prowadzący:**

„Zebrałem wasze 20 zapytań z audytu. Rozbiliśmy je na 5 typów: Q (pytanie-odpowiedź), T (zadanie), C (kontekst/pliki), I (iteracja), M (wieloetapowe). Oto nasza grupa: [pokaż liczby]. To jest typowy obraz: ~80% to Q, C/I/M bliskie zeru."

**Punchline:**

„To, co robicie, to **czat**. Nazywa się workflow — i to jest cała różnica między ludźmi, dla których AI jest gadającą wyszukiwarką, a ludźmi, dla których jest pracownikiem. Dziś zaczynamy przechodzenie. I jeden dowód, że to nie jest kwestia wieku czy umysłu: badania na tysiącach uczących się pokazują, że to, co decyduje, to **poziom startowy, nie metryka urodzenia**. Dlatego niektórzy z was dostali rekomendację FLOW mimo młodego wieku, i odwrotnie."

*Źródło: [H1 — metaanaliza 8776 efektów; Eval wiek-nauka].*

## 0:20–0:50 · MAPA MOŻLIWOŚCI — 8 funkcji, których nie dotykasz

**Format: worked-example na żywo dla KAŻDEJ funkcji — 2 min „zwykły prompt vs z funkcją".** Uczestnik nie notuje teorii — notuje, **które 3 funkcje go uderzyły** (top-3 luki).

1. **Pliki i źródła** — wrzucasz dokument, AI pracuje NA nim (nie wklejka)
2. **Projekty / pamięć** — trwały obszar roboczy: instrukcje + pliki + historia (nie „folder dla AI" — kontekst wstrzykiwany do każdego zapytania)
3. **Custom instructions** — „kto jestem, jak pracuję" ustawione raz, działa zawsze (67% power users vs <10% casual — to jest Wasza luka w jednej liczbie)
4. **Praca wieloetapowa (chaining)** — brief → plan → dowody → analiza → szkic → kontrola (zamiast jednego mega-promptu)
5. **Deep research** — agent: plan → wieloetapowe wyszukiwanie → synteza z cytatami (wolniejszy, daje ślad audytowy)
6. **Structured output** — wymuś format (tabela/checklista); uwaga: wymuszony format obniża dokładność wartości — antidotum: pole „Uzasadnienie" przed odpowiedzią
7. **Głos** — dyktowanie i rozmowa (praca bez klawiatury)
8. **Integracje** — Google Workspace, eksporty (poziom 2 — tu tylko mapujemy)

**Ważne dla prowadzącego:** nie tylko mów — **KAŻDĄ pokazuj na własnym koncie w 30–60 sekund**. Worked-example effect działa przez obserwację, nie opis. [M11]

**Na koniec bloku:** „Zapiszcie swoje top-3. To będzie Wasz plan na tydzień — każdy z was będzie przestawiał 3 swoje stare nawyki na te funkcje."

## 0:50–1:10 · MINI-WORKFLOW NA ŻYWO — pierwsza funkcja w akcji

**Prowadzący:**

„Bierzemy teraz top-1 z mojej listy i robimy NA ŻYWO: z pytań-odpowiedzi robimy mały proces. Wybieram zadanie z waszego banku zadań [z rundy] — [przykład z grupy]."

**Na żywo (uczestnicy równolegle na swoim przykładzie):**

1. **Brief** — co jest celem, jakie kryterium uznaje zadanie za zrobione
2. **Kontekst** — wgranie/wklejenie materiałów („kartka na biurku asystenta")
3. **Plan** — „nie rób jeszcze — najpierw zaproponuj plan w 3 etapach" (plan-and-execute)
4. **Wykonanie etapu 1** — tylko etap 1
5. **Kontrola** — co zweryfikuję, zanim pójdę dalej (protokół 3-check: źródła/liczby/logika)

**Peer moment:** 2–3 uczestników pokazują w 30 sekund swój mini-workflow (wymiana: „ja to zrobiłem na [funkcja]"). To pierwsza odsłona zasady grupy: **każdy komentuje 2 obce**.

**Granice mini-BHP (30 sekund, HORIZON v2 — inaczej niż w 40+):**

„Znacie podstawy, przypominam dwie konkretne: **dane klientów/uczelni/firmy nie wchodzą do publicznego czatu** (DPA/ZDR to temat sesji 4) i **uczelnia/firma mają własne regulaminy AI** — sprawdźcie swoje przed użyciem na zaliczeniach/pismach."

## 1:10–1:20 · JAK TO SIĘ MA DO WASZEJ ŚCIEŻKI (test-out + poziomy)

**Prowadzący:**

„System, w którym jesteście, ma 3 poziomy: START (pierwsze kroki), HORIZON (wy), FLOW (własne workflow). Poziom dostaje się **zadaniem, nie wiekiem** — na trafieliście tu z triage'u. Jeśli w trakcie kursu okaże się, że jesteś już w FLOW — robimy test-out i przeskakujesz. I odwrotnie: zawrócenie nie jest wstydem, jest ekonomią."

**Mikro-zadanie na teraz:** „Napisz na Discordzie w #dziennik: która funkcja z mapy jest Twoim numerem 1 do przebudowy i dlaczego. To Wasz pierwszy wpis — codziennie po jednym zdaniu."

*Dlaczego: dla 15–25 peer/kanały są motywatorem #1; pierwszy wpis obniża próg wejścia do #dziennika.*

## 1:20–1:30 · MIKRO-TYGODNIE + GRANICE skrót + zamknięcie

**Mikro-zadania T1 (dni 1–5, 10–15 min dziennie — SYLABUS):**
- D1: przetestuj 2. funkcję z top-3 na realnym zadaniu
- D2: 3. funkcja
- D3: przebuduj 1 stare zapytanie używając nowej funkcji — porównaj wyniki
- D4: office hour (opcjonalnie) / peer review na Discordzie
- D5: wybierz obszar na własny workflow (nauka / praca / firma)

**Narzędzia do wzięcia:**
- **Audyt startowy** — już zrobiony (T0), wracamy do niego na Live 2
- **Instrukcja asystenta HORIZON** — wklejacie do swojego asystenta; on zna tryb waszego poziomu
- **3-check** — od dziś przy każdym ważnym wyniku
- **Ściąga HORIZON** (jeśli jest gotowa) — link w Drive

**Zamknięcie:**

„Za tydzień robimy dwie rzeczy: porównujemy, co zmieniło przebudowanie waszych starych zapytań, i budujecie pierwszy WŁASNY workflow. Dziś każdy z was zobaczył własną lukę w liczbach. Nie da się jej niewidzieć. Do usłyszenia na #dziennik."

**Po sesji (10 min, prowadzący):** notatka — frekwencja, kto nie oddał T0, słowa „co mnie zaskoczyło" z feedbacku → do scenariusza v2.

---

## Metryki S1 HORIZON (wpisz po sesji)

- Obecność: __/__ · audyt T0 oddany: __/__
- Top-3 luki wskazane przez uczestników: ____
- Pierwsze wpisy w #dziennik (24 h): __/__ ← **wskaźnik ryzyka drop-off**
- Feedback „najbardziej wartościowe": ________________

## PUŁAPKI PROWADZĄCEGO (HORIZON-specyficzne)

- ❌ Tłumaczenie podstaw („co to jest LLM") — grupa to zna; to zabija wiarygodność. Zamiast tego: mechanika na poziomie „co widzi model".
- ❌ Mega-prompt jako wzór — zawsze pokazuj podział na etapy.
- ❌ Teoria bez ekranu — każda funkcja z pokazaniem; werbalna mapa nie działa.
- ❌ Grupowanie wszystkich wieków w jedną ankietę feedbacku — formularz po sesji uwzględnij segment (student/praca/firma), bo use-case'y różne.
- ❌ Pozostawienie #dziennik martwego po 24 h — to sygnał alarmowy; kontakt 1:1 z milczącymi.
