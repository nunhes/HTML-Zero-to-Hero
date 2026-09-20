# Float e Limpeza en CSS

A propiedade `float` foi durante anos a ferramenta principal para crear layouts, pero hoxe úsase principalmente para envolver texto arredor de imaxes.

---

## 1. Funcionamento de `float`

- **`float: left;`**: Empuxa o elemento á esquerda e permite que o texto suba ao seu carón pola dereita.
- **`float: right;`**: Empuxa o elemento á dereita.

---

## 2. O problema do colapso do pai

Cando todos os fillos dun contedor teñen `float`, o pai "colapsa" e a súa altura pasa a ser 0, xa que os fillos están fora do fluxo normal.

---

## 3. Limpeza (`clear`)

A propiedade `clear` serve para indicar que un elemento non debe estar ao carón doutro que teña float.
- `clear: both;`: O elemento baixará ata debaixo de calquera float anterior.

---

## 4. O truco "Clearfix"

Unha técnica clásica para evitar o colapso do pai:
```css
.contedor::after {
  content: "";
  display: table;
  clear: both;
}
```

---

**Resumo**:
Evita usar `float` para complexos layouts de columnas (usa Flexbox ou Grid). Resérvao para casos simples onde queiras envolver texto arredor de medios.

---

DAW🧊2026
