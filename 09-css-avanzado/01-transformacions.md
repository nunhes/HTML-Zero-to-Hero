# Transformacións en CSS

As divisións e movementos de elementos permiten crear efectos 2D e 3D sen necesidade de JavaScript.

---

## 1. A propiedade `transform`

Esta propiedade permite aplicar as seguintes transformacións:

- **`translate(x, y)`**: Move o elemento dende a súa posición actual.
- **`scale(sx, sy)`**: Cambia o tamaño (ex: `1.2` para un 20% máis grande).
- **`rotate(angle)`**: Xira o elemento (ex: `45deg`, `1turn`).
- **`skew(ax, ay)`**: Inclina o elemento.

---

## 2. Puntos de orixe (`transform-origin`)

Podes elixir dende que punto se aplica a transformación (por defecto é o centro).
```css
transform-origin: top left;
```

---

## 3. Transformacións 3D

Se o pai ten `perspective`, podes mover elementos no eixe Z:
- `rotateX()`, `rotateY()`, `rotateZ()`
- `translateZ()`

---

**Resumo**:
As transformacións son puramente visuais e non afectan ao espazo que ocupa o elemento no layout. Son ideais para efectos de hover ou animacións complexas.

---

DAW🧊2026
