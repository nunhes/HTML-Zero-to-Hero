# Posicionamento en CSS

A propiedade `position` permite sacar elementos do fluxo normal do documento e situalos en lugares específicos da pantalla.

---

## 1. Posición Estática (`static`)

É o valor por defecto. O elemento segue o fluxo natural da páxina (un detrás doutro). Non admite as propiedades `top`, `right`, `bottom`, `left`.

---

## 2. Posición Relativa (`relative`)

O elemento segue no fluxo, pero podes movelo respecto á súa posición orixinal sen afectar ao espazo que ocupaba.
```css
.caixa {
  position: relative;
  top: 10px; /* Móvese 10px cara abaixo dende onde estaba */
}
```

---

## 3. Posición Absoluta (`absolute`)

O elemento sae do fluxo (as outras caixas compórtanse coma se non existise). Posiciónase respecto ao seu **contedor pai máis próximo que teña `position: relative;`** (ou o `<body>` se non hai ningún).

---

## 4. Posición Fixa (`fixed`)

O elemento queda "pegado" á pantalla (viewport). Non se move aínda que fagas scroll. Úsase moito para menús de navegación superiores ou botóns de "volver arriba".

---

## 5. Posición Pegaxenta (`sticky`)

Unha mestura entre `relative` e `fixed`. O elemento móvese co scroll ata que chega a un punto definido (ex: `top: 0`) e nese momento queda fixo no seu contedor.

---

## 6. O índice Z (`z-index`)

Cando os elementos se solapan, `z-index` decide quen vai enriba de quen. Só funciona en elementos posicionados (non `static`).

---

**Resumo**:
Usa `relative` como referencia para os teus `absolute`. Usa `fixed` ou `sticky` para elementos que deban acompañar ao usuario durante a navegación.

---

DAW🧊2026
