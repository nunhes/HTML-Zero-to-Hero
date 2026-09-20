# Media Queries e Responsividade

As **Media Queries** permiten aplicar estilos diferentes segundo as características do dispositivo (ancho da pantalla, orientación, resolución).

---

## 1. Sintaxe básica

```css
/* Estilos xerais */
.sidebar { display: block; }

/* Só se aplican se a pantalla ten menos de 768px */
@media (max-width: 768px) {
  .sidebar { display: none; }
}
```

---

## 2. Móbil Primeiro (Mobile First)

A estratexia recomendada: escribe os estilos para móbil primeiro (sen media queries) e vai engadindo capas para pantallas máis grandes:
```css
/* Móbil */
.grid { grid-template-columns: 1fr; }

/* Escritorio */
@media (min-width: 1024px) {
  .grid { grid-template-columns: 1fr 1fr 1fr; }
}
```

---

## 3. Puntos de corte (Breakpoints)

Os máis comúns son:
- **`576px`**: Móbiles grandes.
- **`768px`**: Tablets.
- **`992px`**: Desktops.
- **`1200px`**: Pantallas grandes.

---

## 4. O Meta Viewport

Para que as media queries funcionen en móbiles reais, debes ter esta liña no teu `<head>`:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

**Resumo**:
As media queries son o motor do **Responsive Design**. Permiten que o teu sitio web se vexa perfecto tanto nun iPhone como nunha pantalla ultra-panorámica.

---

DAW🧊2026
