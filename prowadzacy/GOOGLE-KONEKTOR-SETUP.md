# Konnektor Google (Drive + Dokumenty) dla Hermesa — setup krok po kroku

> **Cel:** Hermes (ja) dostaje bezpośredni dostęp do Twojego Google Drive i Dokumentów przez MCP — wtedy sam tworzę strukturę folderów, wgrywam materiały kursu, aktualizuję Dokumenty. Zero ręcznego klikania.
>
> **Wybrany serwer:** `taylorwilsdon/google_workspace_mcp` (3 106★, najpopularniejszy Google MCP; obsługuje Drive, Docs, Gmail, Calendar, Sheets; tryb `--read-only` dostępny; licencja MIT).
> **Czas:** ~15 minut (głównie Google Cloud Console). **Płatność:** 0 zł — Google Cloud free tier wystarcza, to nie jest płatne API w rozumieniu Konstytucji #1 (używasz własnego, darmowego konta Google).

---

## KROK 1 — Google Cloud Console (10 min, jednorazowo)

1. Wejdź: https://console.cloud.google.com/ → zaloguj się kontem Google, na którym masz Drive z materiałami kursu
2. Górny pasek → **wybierz/zrób projekt**: nazwa `osnowa-edu` (Create Project)
3. Menu ☰ → **APIs & Services → Library** → znajdź i **Enable**:
   - **Google Drive API**
   - **Google Docs API** (dokumenty kursu)
4. Menu ☰ → **APIs & Services → OAuth consent screen**:
   - User Type: **External** → Create
   - App name: `OSNOWA EDU` · User support email: Twój mail · Developer contact: Twój mail
   - **Scopes:** Add or Remove Scopes → dodaj:
     - `https://www.googleapis.com/auth/drive`
     - `https://www.googleapis.com/auth/documents`
   - **Test users:** Add Users → dodaj SWÓJ adres Gmail (bez tego OAuth nie przepuści)
   - Save
5. **APIs & Services → Credentials → Create Credentials → OAuth client ID**:
   - Application type: **Desktop app** → Create
   - **Download JSON** → zapisz jako `client_secret.json` (np. do `~/Documents/`)
   - Z Copy weź też: **Client ID** i **Client Secret** (przydadzą się w Kroku 3)

## KROK 2 — dodaj serwer do Hermesa (2 min)

Wklej w terminal (podmień `...` na swoje wartości z Kroku 1):

```bash
hermes mcp add gws \
  --command uvx \
  --args workspace-mcp --tools drive docs --read-only \
  --env GOOGLE_OAUTH_CLIENT_ID=... \
  --env GOOGLE_OAUTH_CLIENT_SECRET=... \
  --env GOOGLE_CLIENT_SECRET_PATH=/Users/marcinoldak/Documents/client_secret.json
```

*(Używam `--read-only` na start — bezpieczniej; po weryfikacji, że wszystko działa, przełączamy na tryb z zapisem. `uvx` masz z uv — Hermes go wymaga, więc jest zainstalowany.)*

Restart Hermesa (desktop app → restart / `hermes desktop` ponownie) — na starcie zarejestruje narzędzia `mcp_gws_*`.

## KROK 3 — pierwsza autoryzacja (2 min)

1. Zapytaj mnie w nowej rozmowie: **„pokaż pliki z Drive"**
2. Pierwsze wywołanie zwróci **link OAuth** → otwórz w przeglądarce → zaloguj się → „OSNOWA EDU wants access" → **Allow** (zaznacz wszystkie scopes)
3. Token zapisze się lokalnie — kolejne wywołania bez logowania

## KROK 4 — weryfikacja (1 min)

Powiedz mi: „pokaż strukturę folderu OSNOWA EDU" — jeśli widzi drzewo z GDRIVE-SETUP, jest zrobione.

## KROK 5 — tryb pełny (zapis) — po weryfikacji

```bash
hermes mcp remove gws
hermes mcp add gws \
  --command uvx \
  --args workspace-mcp --tools drive docs \
  --env GOOGLE_OAUTH_CLIENT_ID=... \
  --env GOOGLE_OAUTH_CLIENT_SECRET=... \
  --env GOOGLE_CLIENT_SECRET_PATH=/Users/marcinoldak/Documents/client_secret.json
```

Bez `--read-only` — wtedy ja tworzę foldery, wgrywam materiały i aktualizuję Dokumenty na żywo (PIPELINE z INFRA: repo → Drive → Discord).

---

## Co osiągniesz (po KROKU 5)

| Zadanie | Kto robi |
|---|---|
| Struktura folderów Drive wg GDRIVE-SETUP | **ja, jednym poleceniem** |
| Wgranie ściągawki, instrukcji asystenta, planów | **ja** (konwersja MD→Docs w locie) |
| Linki do pinów #start-tutaj | **ja** podam po utworzeniu |
| Aktualizacja materiałów po każdej sesji | **ja** (commit w repo → sync do Drive) |
| Kolektor feedbacku (arkusz) | **ja** + Apps Script |
| Newsletter #1 → Dokument Google | **ja** |

## Uwagi bezpieczeństwa

- `client_secret.json` zostaje na Twoim dysku (`~/Documents/`) — nie idzie do repo, nie idzie do gita (jest w .gitignore wzorcu; sprawdzę przed commitem)
- Token OAuth: lokalny cache serwera (`~/.credentials/` u serwera) — odwołujesz w Google Account → Security → Third-party access
- Start z `--read-only`: nawet jeśli coś pójdzie nie tak, ja nie mogę nic zepsuć w Twoim Drive
- Później mogę zawęzić do konkretnego folderu (scope folder-level) — Drive API pozwala na folder-specific access

## Alternatywa (jeśli nie chcesz Google Cloud Console)

**Gemini w przeglądarce** (workspace.google.pl → Gemini): otwierasz folder Drive → „Gemini: utwórz strukturę folderów wg tej listy" — zadziała dla folderów, ale NIE wgrywa plików z dysku, NIE tworzy Dokumentów z treścią 1:1 i nie aktualizuje się z repo. To rozwiązanie „na dziś", nie systemowe. Rekomendacja: **krok przez Cloud Console — 15 min raz i masz automatyzację na cały kurs.**
