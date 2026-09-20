# Propiedades Básicas de CSS

Unha vez entendidos os selectores, o seguinte paso é coñecer as propiedades que nos permiten cambiar o aspecto visual dos elementos.

---

## 1. O contedor básico: `display`

A propiedade `display` é unha das máis importantes de CSS, xa que define como se comporta un elemento na páxina.

- **`block`**: O elemento ocupa todo o ancho dispoñible e salta de liña (ex: `<div>`, `<h1>`).
- **`inline`**: O elemento ocupa só o espazo do seu contido e non salta de liña (ex: `<span>`, `<a>`).
- **`inline-block`**: Comportase como un elemento en liña pero admite dimensións (ancho e alto).
- **`none`**: O elemento desaparece completamente da páxina e non ocupa espazo.

---

## 2. Dimensións: `width` e `height`

Permiten definir o tamaño dun elemento.
- **Valores**: Podes usar píxeles (`px`), porcentaxes (`%`), ou unidades relativas á pantalla (`vw`, `vh`).
- **Límites**: `min-width`, `max-width`, `min-height` e `max-height` son fundamentais para o deseño responsivo.

---

## 3. Visibilidade e Opacidade

- **`visibility: hidden;`**: O elemento faise invisible pero segue ocupando o seu espazo na páxina (a diferenza de `display: none;`).
- **`opacity`**: Define a transparencia (de `0` a `1`). Afecta a todo o elemento e ao seu contido.

---

## 4. O cursor

Podes cambiar o punteiro do rato cando está sobre un elemento:
```css
.boton {
  cursor: pointer;
}
```

---

**Resumo**:
As propiedades básicas controlan a existencia e as dimensións dos elementos. `display` é a clave para entender como se estruturan as caixas na web.

---

DAW🧊2026
