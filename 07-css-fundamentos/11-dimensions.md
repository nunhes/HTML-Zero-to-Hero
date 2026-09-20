# Dimensións en CSS

Controlar o tamaño dos elementos é fundamental para crear layouts equilibrados e adaptables.

---

## 1. Unidades de Medida

### **Absolutas**
- **`px` (píxel)**: Tamaño fixo que non cambia.

### **Relativas**
- **`%`**: Relativo ao tamaño do contedor pai.
- **`em`**: Relativo ao tamaño de fonte do elemento actual.
- **`rem`**: Relativo ao tamaño de fonte da raíz (`html`). Moi recomendado por accesibilidade.
- **`vw` / `vh`**: Porcentaxe do ancho ou alto da pantalla (viewport).

---

## 2. Ancho e Alto (`width` / `height`)

- **`auto`**: O valor por defecto. O navegador calcula o tamaño.
- **`100%`**: Ocupa todo o espazo dispoñible no pai.

---

## 3. Límites de tamaño

- **`max-width`**: Evita que un elemento medre de máis (vital para imaxes en móbiles).
- **`min-height`**: Asegura un mínimo de altura aínda que haxa pouco contido.

---

## 4. Desbordamento (`overflow`)

Que pasa se o contido é máis grande que a caixa?
- **`visible`**: O contido sae fóra.
- **`hidden`**: O que sobra córtase e non se ve.
- **`scroll`**: Engade barras de desprazamento.
- **`auto`**: Só engade barras se son necesarias.

---

**Resumo**:
Usa unidades relativas como `rem` e `%` para deseños flexibles. Controla o desbordamento para evitar que o contido "rompa" o layout.

---

DAW🧊2026
