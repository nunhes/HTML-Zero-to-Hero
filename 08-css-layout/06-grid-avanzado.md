# CSS Grid Avanzado

> 🚧 **Contido en construción**
>
> Este tema está sendo desenvolvido. Volve pronto!

## O que aprenderás

- Áreas de grid con `grid-template-areas`
- Colocación explícita: `grid-column`, `grid-row`
- `minmax()`, `repeat()`, `auto-fill` e `auto-fit`
- Grid implícito vs explícito
- Superposición e z-index en Grid
- Combinación de Grid e Flexbox

```css
/* Exemplo: layout con named areas */
.container {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
  grid-template-columns: 250px 1fr;
  grid-template-rows: auto 1fr auto;
}
```

---

← [Grid básico](05-grid.md)
