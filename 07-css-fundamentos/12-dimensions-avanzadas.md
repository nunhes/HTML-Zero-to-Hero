# Dimensións Avanzadas

Nesta sección veremos propiedades que nos dan un control máis preciso sobre como se axustan as caixas ao seu contido ou ao seu pai.

---

## 1. Relación de Aspecto (`aspect-ratio`)

Unha propiedade moderna que permite manter a proporción dun elemento (moi útil para vídeos ou imaxes).
```css
.video {
  width: 100%;
  aspect-ratio: 16 / 9;
}
```

---

## 2. Axuste de obxecto (`object-fit`)

Define como se debe redimensionar unha imaxe ou vídeo dentro do seu contedor.
- **`cover`**: A imaxe recórtase para cubrir todo o espazo.
- **`contain`**: A imaxe vese enteira sen ser deformada.

---

## 3. Funcións de cálculo (`calc()`)

Permite facer matemáticas directamente en CSS.
```css
.sidebar {
  width: calc(100% - 300px);
}
```

---

## 4. Funcións de comparación

- **`clamp(min, valor, max)`**: Define un valor que medra pero nunca sae dun rango (ex: para fontes responsivas).
- **`min()`** e **`max()`**: Elixen o valor máis pequeno ou grande de entre unha lista.

---

**Resumo**:
As funcións como `calc()` e `clamp()` son esenciais para o deseño responsivo moderno, permitindo que a web se adapte a calquera pantalla sen esforzo.

---

DAW🧊2026
