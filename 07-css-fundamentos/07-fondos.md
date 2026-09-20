# Fondos en CSS

A propiedade `background` permite controlar o fondo dos elementos, dende cores ata imaxes complexas.

---

## 1. Imaxes de fondo (`background-image`)

Permite cargar unha imaxe como fondo dun elemento.
```css
background-image: url("fondo.jpg");
```

---

## 2. Control da imaxe

Para que a imaxe se vexa correctamente, usamos estas propiedades:

- **`background-size`**: 
  - `cover`: A imaxe cúbreo todo sen deformarse (pode cortarse).
  - `contain`: A imaxe vese enteira (pode quedar espazo baleiro).
- **`background-repeat`**: `no-repeat` evita que a imaxe se repita coma un mosaico.
- **`background-position`**: `center`, `top right`, etc. Define onde se fixa a imaxe.
- **`background-attachment`**: `fixed` crea o efecto **parallax** (a imaxe non se move ao facer scroll).

---

## 3. Múltiples fondos

Podes poñer varias imaxes separadas por comas. A primeira da lista será a que estea máis "arriba".
```css
background: url("capa-arriba.png"), url("fondo-abaixo.jpg");
```

---

**Resumo**:
Usa `background-size: cover` para fondos de pantalla completa e recorda que podes combinar imaxes con degradados para efectos profesionais.

---

DAW🧊2026
