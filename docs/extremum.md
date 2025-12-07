# Ekstremum Funkcji

## Definicja

Ekstremum funkcji to punkt, w którym funkcja osiąga wartość maksymalną (maksimum) lub minimalną (minimum). Wyróżniamy ekstremum lokalne i globalne.

## Warunki Ekstremum

### Warunek konieczny (I pochodna)

Jeśli funkcja $f(x)$ ma ekstremum w punkcie $x_0$, to:

$$f'(x_0) = 0$$

Punkt $x_0$, w którym pochodna się zeruje, nazywamy **punktem krytycznym**.

### Warunek wystarczający (II pochodna)

Dla punktu krytycznego $x_0$ (gdzie $f'(x_0) = 0$):

- **Jeśli** $f''(x_0) > 0$ **to** w punkcie $x_0$ znajduje się **minimum lokalne**
- **Jeśli** $f''(x_0) < 0$ **to** w punkcie $x_0$ znajduje się **maksimum lokalne**
- **Jeśli** $f''(x_0) = 0$ **to** test nie rozstrzyga (wymaga dalszej analizy)

## Algorytm Szukania Ekstremum

1. Obliczyć pierwszą pochodną: $f'(x)$
2. Rozwiązać równanie: $f'(x) = 0$ → znaleźć punkty krytyczne
3. Obliczyć drugą pochodną: $f''(x)$
4. Zbadać znak drugiej pochodnej w punktach krytycznych
5. Określić typ ekstremum (max/min)

## Przykład

Niech $f(x) = x^3 - 3x^2 + 2$

**Krok 1:** Pierwsza pochodna
$$f'(x) = 3x^2 - 6x$$

**Krok 2:** Rozwiązanie $f'(x) = 0$
$$3x^2 - 6x = 0$$
$$3x(x - 2) = 0$$
$$x_1 = 0, \quad x_2 = 2$$

**Krok 3:** Druga pochodna
$$f''(x) = 6x - 6$$

**Krok 4 & 5:** Badanie ekstremum

- W punkcie $x_1 = 0$: $f''(0) = -6 < 0$ → **maksimum lokalne**
- W punkcie $x_2 = 2$: $f''(2) = 6 > 0$ → **minimum lokalne**

Wartości ekstremów:
- $f(0) = 2$ (maksimum)
- $f(2) = 8 - 12 + 2 = -2$ (minimum)

## Przypadki Szczególne

### Punkt przegięcia
Jeśli $f'(x_0) = 0$ i $f''(x_0) = 0$, punkt $x_0$ może być **punktem przegięcia**, a nie ekstremum.

### Ekstremum na brzegu
Funkcja może osiągać ekstremum globalne również na kraińcach przedziału dziedziny.

### Test trzeciej pochodnej
Jeśli $f''(x_0) = 0$, możemy użyć trzeciej pochodnej:
- **Jeśli** $f'''(x_0) \neq 0$ **to** $x_0$ jest **punktem przegięcia**
