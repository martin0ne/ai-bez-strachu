# OSNOWA EDU — biblioteka kursów AI

> System edukacji AI zbudowany na badaniach: poziomy = **kompetencje** (triage wykonaniowy), wiek = **opakowanie** (tempo, przykłady, wsparcie). Trzy poziomy: **START → HORIZON → FLOW**.

**Start:** wypełnij [TRIAGE-v2](./TRIAGE-v2.md) (10–15 min, zadania wykonawcze) → dostaniesz rekomendację poziomu → wejdź w swój folder i skopiuj instrukcję swojego asystenta.

## Poziomy

| Poziom | Dla kogo | Co osiągniesz | Instrukcja asystenta |
|---|---|---|---|
| **[START](./start/)** | AI = zero lub jedna próba | pierwsze bezpieczne użycie: konto, pytanie, mail, nawyk | [asystent-start](./start/asystent-start.md) |
| **[HORIZON](./horizon/)** | używam AI, ale powierzchownie | świadome użycie: formuła, weryfikacja, granice | [asystent-horizon](./horizon/asystent-horizon.md) |
| **[FLOW](./flow/)** | projektuję własne workflow | powtarzalne procesy + transfer na firmę/pracę | [asystent-flow](./flow/asystent-flow.md) |

## Instrukcja asystenta — jak działa

Każdy poziom ma **własny wariant** instrukcji (MD do skopiowania w czat). Warianty budowane są ze **wspólnej bazy** ([asystent-szablon-baza](./asystent-szablon-baza.md)): rdzeń (język, uczciwość, 3-check, czerwona lista, jakość, JEŚLI→TO) + warstwa poziomu (tryb współpracy, typ zadań, feedback) + opcjonalna warstwa grupy (ton i przykłady per kohorta). Zmiana zasad trafia do bazy → wszystkie warianty spójne.

## Struktura

```
TRIAGE-v2.md               ← zacznij tutaj: 3 pytania + 2 zadania → poziom
FILOZOFIA-EDUKACJI.md      ← 5 zasad + progresja (dlaczego tak uczymy)
SYSTEM-EDU.md              ← architektura: macierz grup × poziomy, pula modułów
asystent-szablon-baza.md   ← wspólne DNA wariantów asystenta
start/                     ← START: scenariusze, plan, ściąga-A4, asystent-start
horizon/                   ← HORIZON: sylabus, audyt T0, asystent-horizon
flow/                      ← FLOW: asystent-flow (workflow, dokumentacja)
wspolne/                   ← 3-check · czerwona lista · JEŚLI-TO (dla wszystkich)
strona/                    ← strona onboardingowa + kreator
```

## Narzędzia wspólne (każdy poziom)

- **[3-check](./wspolne/3-check-weryfikacja.md)** — źródła / liczby / logika; P0 (prawo/zdrowie/pieniądze) = 100% weryfikacji
- **[Czerwona lista](./wspolne/czerwona-lista.md)** — „wkleiłbym to obcej osobie w mailu?" + protokół przerwania
- **[JEŚLI→TO](./wspolne/jesli-to-plan.md)** — plan nawyku (implementation intentions)

## Zasady

- **Poziom dobiera triage wykonaniowy** (zadania, nie deklaracje) — wiek tylko opakowuje.
- Każdy moduł kończy się **artefaktem** (prompt/checklista/workflow) — nie „wiedzą w głowie".
- **Transfer po 7 dniach** na nowym przykładzie — miara sukcesu, nie quiz.
- Zero liczb bez źródła; pełna rozpiska w materiałach merytorycznych (faza 5).
- Feedback: Issues (anonimizowany) — zasilają cotygodniowy raport ulepszeń.

## Licencja

Użycie osobiste — tak. Komercyjne — kontakt.

---

*Prowadzący: [MJ.OLDAK](https://mjoldak.pl) · system potwierdzony badaniami (DR 02.09: H1 prior knowledge > wiek) · 2026*
