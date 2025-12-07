# Dokumentacja Projektu (MkDocs)

Poniżej znajduje się instrukcja konfiguracji środowiska deweloperskiego oraz inicjalizacji projektu dokumentacji.

## Wymagania wstępne
- Zainstalowany Python (wersja 3.x).

## Instrukcja instalacji i konfiguracji

Wykonaj poniższe kroki w terminalu w głównym katalogu projektu:

### Krok 1: Utworzenie środowiska wirtualnego
Należy utworzyć izolowane środowisko o nazwie `.venv`.

```bash
python -m venv .venv
```

### Krok 2: Utworzenie pliku .gitignore (jeśli nie istnieje)
Aby nie wysyłać śmieci do repozytorium, utwórz plik `.gitignore` z odpowiednią zawartością:

```bash
echo .venv/ >> .gitignore
echo site/ >> .gitignore
echo __pycache__/ >> .gitignore
```

### Krok 3: Aktywacja środowiska

**Windows (PowerShell/CMD):**
```bash
.venv\Scripts\activate
```

**macOS / Linux:**
```bash
source .venv/bin/activate
```

### Krok 4: Instalacja MkDocs
Instalujemy MkDocs wraz z popularnym motywem "Material".

```bash
pip install mkdocs mkdocs-material
```

### Krok 5: Inicjalizacja szkieletu projektu
Tworzymy nową strukturę plików konfiguracyjnych w obecnym folderze.

```bash
mkdocs new .
```

### Krok 6: Zapisanie zależności
Generujemy plik `requirements.txt` dla przyszłych instalacji.

```bash
pip freeze > requirements.txt
```

## Dalsze kroki

Potem: mkdocs gh-deploy  - Wykonaj polecenie, aby opublikować dokumentację na GitHub Pages.

Potem: mkdocs serve  - Uruchom lokalny serwer do podglądu dokumentacji.

## Uwagi końcowe

Pamiętaj, aby regularnie aktualizować plik `requirements.txt` po dodaniu nowych zależności do projektu.

## Dodanie htmla do MkDocs

Aby dodać pliki HTML do dokumentacji MkDocs, umieść je w katalogu `docs` i odwołaj się do nich w pliku `mkdocs.yml` lub bezpośrednio w nawigacji. Możesz również użyć wtyczek MkDocs do lepszej integracji HTML z resztą dokumentacji.

Przykład dodania pliku HTML do nawigacji w `mkdocs.yml`:

```yamlnav:
  - Home: index.md
  - Custom Page: custom_page.html
```

nav:
  - Home: index.md
  - Ekstremum Funkcji: extremum.md
  - Styczna: styczna.html