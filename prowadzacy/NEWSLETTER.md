# Newsletter — „Tygodnik AI po polsku" (design + pipeline)

> Decyzja 02.09: strona www dostaje newsletter — **te same newsy co #newsy-ai, mailem**. Dla osób, które nie chcą Discorda (kluczowe dla 40+ i części 36–50: mail = ich naturalne środowisko, Discord = bariera). Newsletter = dystrybucja równoległa, NIE osobny content.

---

## 1. Rola w ekosystemie

```
          ┌─ Discord #newsy-ai  ← aktywni (komentują, pytają)
NEWSY ────┤
          └─ Newsletter mail    ← cisi (40+, 50+, „nie chcę nic instalować")
                 ↓
          strona www (archiwum wydań — SEO + dowód żywej aktywności)
```

- **Jedno źródło treści:** Ty piszesz wydanie RAZ (3–5 newsów × 1 zdanie „co to znaczy dla Ciebie"), pipeline roznosi.
- **Newsletter = onboarding мягкий:** subskrypcja ma niższy próg niż Discord — łapie tych, którzy „jeszcze nie są gotowi na grupę", i ogrzewa ich do kohorty #2.
- **Newsy ≠ kurs:** to utrzymanie kontaktu i budowanie zaufania („ten człowiek tłumaczy bez straszenia"), nie lekcje.

## 2. Format wydania (stały, 1 ekran maila)

```
TYGODNIK AI — wydanie #N (data)

3 newsy tygodnia, po ludzku:

1. [NAGŁÓWEK newsa po polsku]
   Co się stało: 1 zdanie.
   Co to znaczy dla Ciebie: 1 zdanie. [M##]

2. …

3. …

ZADANIE TYGODNIA (opcjonalne, 5 min): jedno mikro-zadanie z kursu
LINKI: Discord grupy · Materiały · Nauka od zera (strona)
Odpowiedz na tego maila — czytam każdy.
```

Zasady: maks. 3 newsy · zero clickbaitu i paniki (kontrast z „AI zabierze pracę") · każdy news z oznaczeniem źródła · maks. 3 minuty czytania.

## 3. Stack (decyzja: composed before build)

| Wariant | Narzędzie | Koszt | Kiedy |
|---|---|---|---|
| **A — START (rekomendowany)** | MailerLite / MailerSend free tier: formularz na stronie + automatyka + archiwum wydań | 0 zł do ~1k subskrybentów | od dziś |
| B — Niezależny | własny skrypt + Resend/Brevo API, strony z Jekyll/Hugo na GitHub Pages (repo już jest) | 0 zł + robota | gdy A przestanie wystarczać |
| C — n8n pipeline | n8n: RSS/curated → LLM draft → Ty redakcja → mail + Discord webhook + Drive archiwum | 0 zł self-host | kohorta #2+ |

**Rekomendacja:** A na start (60 min setupu, zgodne z RODO out-of-the-box, double opt-in), migracja na B/C gdy lista żyje. Zasada #2: nie budujemy pipeline'u przed pierwszym subskrybentem.

## 4. RODO (honesty gate — obowiązkowe na formularzu)

> „Zapisuję się na Tygodnik AI (max 3 minuty czytania, raz w tygodniu). Zero spamu, wypisujesz jednym klikiem. Administrator: MJ.OLDAK. Szczegóły w polityce prywatności."

- **Double opt-in** (potwierdzenie mailem) — standard narzędzi A, wymóg dobrej praktyki.
- Newsletter ≠ Discord: osobne listy, wspólne treści. Kto jest w obu — dostaje to samo raz (dedupe w narzędziu).

## 5. Miejsce na stronie onboardingowej

`twoj-pierwszy-tydzien.html` dostaje sekcję **„Bądź na bieżąco — bez Discorda"**:

```
Nie chcesz (jeszcze) wchodzić na grupę? Rozumiemy.
Tygodnik AI po polsku — 3 newsy tygodnia, każde z jednozdaniowym
„co to znaczy dla Ciebie". Zero paniki, zero żargonu, 3 minuty czytania.

[FORMULARZ: e-mail → Zapisz mnie]
```

Umiejscowienie: pod kartami narzędzi, przed sekcją „Dlaczego tak uczymy" — łapie tych, którzy skończyli czytać i nie skończyli decydować.

## 6. Pipeline tygodniowy (Twoje 30 min/tydz)

1. **Pon/czw (10 min):** wybierasz 3 newsy z tygodnia (źródła: twoje czytanie; Discord #newsy-ai ma te same) — krótka lista do mnie
2. **Ja (5 min):** draft wydania wg formatu §2 (+ znaczniki [M##] gdy dotyczy kursu)
3. **Ty (10 min):** redakcja — zatwierdzasz lub zmieniasz akcenty „co to znaczy dla Ciebie"
4. **Ja (5 min):** wysyłka przez narzędzie + mirror do #newsy-ai + archiwum na Drive `/04-Feedback/Raporty` (nie — do nowego `/05-Newsletter`)
5. **Raz w miesiącu:** liczby (otwarcia, kliki, wypisy) wchodzą do cotygodniowego raportu feedbacku

## 7. Do zrobienia (kolejka)

| # | Zadanie | Status |
|---|---|---|
| 1 | Wybór narzędzia (MailerLite vs MailerSend) + konto | ⬜ Marcin (wymaga Twojego maila) |
| 2 | Sekcja newsletter na stronie onboardingowej + formularz | ⬜ Hermes (po 1) |
| 3 | Format wydania #1 (szablon) | ✅ ten dokument §2 |
| 4 | Wydanie #1 (3 newsy z tego tygodnia — mam materiał z researchów) | ⬜ Hermes → Ty redakcja |
| 5 | Archiwum wydań na stronie (później) | ⬜ |

---

*Powiązane: DISCORD-SETUP.md (#newsy-ai i kanały głosowe) · INFRA-DISCORD-GOOGLE.md (ekosystem) · KONCEPT §funnel (strona-hub bez CTA „kup" — newsletter jako pierwszy kontakt zgodny z tą zasadą)*
