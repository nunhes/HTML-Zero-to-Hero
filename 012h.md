# Posición

A propiedade **`position`** en CSS é unha das máis importantes para controlar o deseño e o layout dunha páxina web. Permíteche definir como se posiciona un elemento na páxina, o que é esencial para crear deseños complexos e responsivos.

Vou explicarche os diferentes valores da propiedade `position`, como funcionan e cando usalos, xunto con exemplos prácticos.

---

### **1. Valores da propiedade `position`**

A propiedade `position` pode ter os seguintes valores:

1. **`static`** (valor predeterminado)
2. **`relative`**
3. **`absolute`**
4. **`fixed`**
5. **`sticky`**

---

### **2. `position: static;`**

- **Comportamento**: O elemento segue o fluxo normal do documento. Non se ve afectado polas propiedades `top`, `right`, `bottom` ou `left`.
- **Uso**: Este é o valor predeterminado. **Non se usa para posicionamento especial**.

#### **Exemplo**:
```css
div {
  position: static;
}
```

---

### **3. `position: relative;`**

- **Comportamento**: O elemento posicionase en relación coa súa posición normal no fluxo do documento. Podes mover o elemento usando `top`, `right`, `bottom` ou `left`.
- **Uso**: Útil **para pequenos axustes de posición sen alterar o fluxo do documento**.

#### **Exemplo**:
```css
div {
  position: relative;
  top: 10px;
  left: 20px;
}
```
- O elemento móvese **10px** cara a abaixo e **20px** cara a dereita desde a súa posición orixinal.

---

### **4. `position: absolute;`**

- **Comportamento**: O elemento posicionase en relación co seu antepasado posicionado máis próximo (un antepasado con `position` diferente de `static`). Se non hai ningún antepasado posicionado, úsase o contedor inicial (normalmente o `<body>`).
- **Uso**: Útil para crear elementos que deben estar fóra do fluxo normal do documento, como menús despregables ou capas superpostas.

#### **Exemplo**:
```css
div {
  position: absolute;
  top: 50px;
  left: 100px;
}
```
- O elemento colócase **50px** desde o bordo superior e **100px** desde o bordo esquerdo do seu antepasado posicionado.

---

### **5. `position: fixed;`**

- **Comportamento**: O elemento posicionase en relación coa ventana gráfica (viewport). Non se move cando se fai scroll na páxina.
- **Uso**: Útil para elementos que deben permanecer visibles en todo momento, como menús de navegación fixos ou botóns de "subir arriba".

#### **Exemplo**:
```css
div {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```
- O elemento colócase **20px** desde o bordo inferior e **20px** desde o bordo dereito da ventana gráfica.

---

### **6. `position: sticky;`**

- **Comportamento**: O elemento actúa como `relative` ata que alcanza un punto de desprazamento (definido por `top`, `right`, `bottom` ou `left`), momento no cal se converte en `fixed`.
- **Uso**: Útil para crear elementos que deben "pegarse" á parte superior ou inferior da pantalla cando se fai scroll.

#### **Exemplo**:
```css
div {
  position: sticky;
  top: 0;
}
```
- O elemento permanece no fluxo normal ata que se despraza ata o bordo superior da ventana gráfica, momento no cal se fixa nesa posición.

---

### **7. Propiedades relacionadas**

Cando usas `position` con valores diferentes de `static`, podes usar as seguintes propiedades para controlar a posición exacta do elemento:

- **`top`**: Distancia desde o bordo superior.
- **`right`**: Distancia desde o bordo dereito.
- **`bottom`**: Distancia desde o bordo inferior.
- **`left`**: Distancia desde o bordo esquerdo.

---

### **8. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar os diferentes valores de `position`:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Posición en CSS</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      height: 2000px; /* Para permitir o desprazamento */
    }

    .box {
      width: 100px;
      height: 100px;
      background-color: lightblue;
      margin: 10px;
      text-align: center;
      line-height: 100px;
    }

    .relative {
      position: relative;
      top: 20px;
      left: 50px;
    }

    .absolute {
      position: absolute;
      top: 50px;
      left: 200px;
    }

    .fixed {
      position: fixed;
      bottom: 20px;
      right: 20px;
    }

    .sticky {
      position: sticky;
      top: 0;
      background-color: lightcoral;
    }
  </style>
</head>
<body>
  <div class="box">Static</div>
  <div class="box relative">Relative</div>
  <div class="box absolute">Absolute</div>
  <div class="box fixed">Fixed</div>
  <div class="box sticky">Sticky</div>
</body>
</html>
```

#### **Resultado esperado**:
1. **Static**: O primeiro cuadro permanece no fluxo normal.
2. **Relative**: O segundo cuadro móvese **20px** cara a abaixo e **50px** cara a dereita desde a súa posición orixinal.
3. **Absolute**: O terceiro cuadro colócase **50px** desde o bordo superior e **200px** desde o bordo esquerdo do contedor inicial.
4. **Fixed**: O cuarto cuadro permanece fixo na parte inferior dereita da ventana gráfica.
5. **Sticky**: O quinto cuadro "pégase" ao bordo superior da ventana gráfica cando se fai scroll.

---

### **9. Conclusión**

A propiedade **`position`** en CSS é esencial para controlar o posicionamento dos elementos nunha páxina web. Coñecer os diferentes valores (`static`, `relative`, `absolute`, `fixed` e `sticky`) e como usalos permíteche crear deseños complexos e responsivos. Espero que esta explicación e exemplo che sexan útiles para dominar o uso de `position` en CSS! 😊


---

DAW🧊2025

#css
#DAW