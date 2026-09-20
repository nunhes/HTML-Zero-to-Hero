# CSS Grid Layout

**CSS Grid Layout** (ou simplemente **Grid**) é un sistema de deseño bidimensional que permite crear layouts complexos e responsivos de maneira eficiente. A diferenza de Flexbox, que é unidimensional (traballa nun só eixe), Grid permíteche controlar tanto as filas como as columnas dun contedor, o que o fai ideal para deseños máis avanzados.

Vexamos os conceptos básicos de Grid, as súas propiedades principais e como usalas para crear deseños complexos. Ademais, ao final, proporcionareiche algúns enlaces útiles para seguir aprendendo e practicando.

---

## **1. Conceptos básicos de Grid**

Grid funciona baseándose en **filas** e **columnas**, que forman unha cuadrícula (grid). Podes definir o tamaño das filas e columnas, así como a posición dos elementos dentro da cuadrícula.

- **Contedor grid (grid container)**: O elemento que contén os elementos da cuadrícula. Defínese usando `display: grid` ou `display: inline-grid`.
- **Elementos grid (grid items)**: Os fillos directos do contedor grid.
- **Liñas grid (grid lines)**: As liñas que dividen as filas e columnas.
- **Celas grid (grid cells)**: As interseccións entre filas e columnas.
- **Áreas grid (grid areas)**: Grupos de celas que forman áreas rectangulares.

---

## **2. Propiedades do contedor grid**

### **`display`**
Define o contedor como un contedor grid.

- **Sintaxe**:
  ```css
  display: grid; /* Bloque grid */
  display: inline-grid; /* Inline grid */
  ```

### **`grid-template-columns` e `grid-template-rows`**
Define o tamaño das columnas e filas da cuadrícula.

- **Sintaxe**:
  ```css
  grid-template-columns: tamaño1 tamaño2 ...;
  grid-template-rows: tamaño1 tamaño2 ...;
  ```
- **Exemplo**:
  ```css
  .container {
    display: grid;
    grid-template-columns: 100px 200px auto;
    grid-template-rows: 50px 100px;
  }
  ```

### **`grid-template-areas`**
Define áreas nomeadas na cuadrícula.

- **Sintaxe**:
  ```css
  grid-template-areas: 
    "área1 área2"
    "área3 área4";
  ```
- **Exemplo**:
  ```css
  .container {
    display: grid;
    grid-template-areas: 
      "header header"
      "sidebar main"
      "footer footer";
  }
  ```

### **`gap`**
Define o espazo entre as filas e columnas.

- **Sintaxe**:
  ```css
  gap: row-gap column-gap;
  ```
- **Exemplo**:
  ```css
  .container {
    gap: 10px 20px;
  }
  ```

### **`justify-items` e `align-items`**
Aliña os elementos dentro das celas ao longo do eixe horizontal e vertical.

- **Valores**: `start`, `end`, `center`, `stretch`.
- **Exemplo**:
  ```css
  .container {
    justify-items: center;
    align-items: center;
  }
  ```

### **`justify-content` e `align-content`**
Aliña a cuadrícula completa dentro do contedor ao longo do eixe horizontal e vertical.

- **Valores**: `start`, `end`, `center`, `stretch`, `space-between`, `space-around`, `space-evenly`.
- **Exemplo**:
  ```css
  .container {
    justify-content: space-between;
    align-content: center;
  }
  ```

---

## **3. Propiedades dos elementos grid**

### **`grid-column` e `grid-row`**
Define a posición dun elemento dentro da cuadrícula.

- **Sintaxe**:
  ```css
  grid-column: inicio / fin;
  grid-row: inicio / fin;
  ```
- **Exemplo**:
  ```css
  .item {
    grid-column: 1 / 3;
    grid-row: 1 / 2;
  }
  ```

### **`grid-area`**
Define a área dun elemento dentro da cuadrícula.

- **Sintaxe**:
  ```css
  grid-area: nome-da-área;
  ```
- **Exemplo**:
  ```css
  .item {
    grid-area: header;
  }
  ```

### **`justify-self` e `align-self`**
Aliña un elemento individual dentro da súa cela ao longo do eixe horizontal e vertical.

- **Valores**: `start`, `end`, `center`, `stretch`.
- **Exemplo**:
  ```css
  .item {
    justify-self: end;
    align-self: start;
  }
  ```

---

## **4. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar Grid para crear un layout simple:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Grid en CSS</title>
  <style>
    .container {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
      grid-template-rows: 100px 200px 100px;
      gap: 10px;
      background-color: #f4f4f4;
      padding: 10px;
    }

    .item {
      background-color: #007bff;
      color: white;
      padding: 20px;
      text-align: center;
    }

    .header {
      grid-column: 1 / 4;
      grid-row: 1 / 2;
    }

    .sidebar {
      grid-column: 1 / 2;
      grid-row: 2 / 3;
    }

    .main {
      grid-column: 2 / 4;
      grid-row: 2 / 3;
    }

    .footer {
      grid-column: 1 / 4;
      grid-row: 3 / 4;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="item header">Cabeceira</div>
    <div class="item sidebar">Barra lateral</div>
    <div class="item main">Contido principal</div>
    <div class="item footer">Pé de páxina</div>
  </div>
</body>
</html>
```

### **Explicación**:
1. **`.container`**:
   - Usa Grid para crear un layout con 3 columnas e 3 filas.
   - Define o tamaño das columnas con `grid-template-columns: 1fr 2fr 1fr`.
   - Define o tamaño das filas con `grid-template-rows: 100px 200px 100px`.
   - Engade un espazo entre as celas con `gap: 10px`.
2. **`.item`**:
   - Define un estilo básico para os elementos da cuadrícula.
3. **`.header`**, **`.sidebar`**, **`.main`**, **`.footer`**:
   - Usa `grid-column` e `grid-row` para posicionar os elementos dentro da cuadrícula.

---

## **5. Recursos para seguir aprendendo e practicando**

Aquí tes algúns enlaces útiles para profundizar en Grid e practicar:

1. **Guía completa de Grid en CSS-Tricks**:
   - [A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/): Unha guía moi detallada con exemplos e diagramas.
   
2. **Grid Garden (Xogo interactivo)**:
   - [Grid Garden](https://cssgridgarden.com/): Un xogo divertido para aprender Grid resolvendo puzzles.
   
3. **MDN Web Docs: Grid**:
   - [Grid en MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout): Documentación oficial de Mozilla sobre Grid.
   
4. **Grid by Example**:
   - [Grid by Example](https://gridbyexample.com/): Un sitio con exemplos prácticos e recursos para aprender Grid.
   
5. **CSS Grid Generator**:
   - [CSS Grid Generator](https://cssgrid-generator.netlify.app/): Unha ferramenta interactiva para xerar código Grid de maneira visual.

---

## **6. Conclusión**

**CSS Grid** é unha ferramenta poderosa e flexible para crear deseños CSS bidimensionais e responsivos. Coñecer as súas propiedades e como combinarlas permíteche crear layouts complexos de maneira eficiente. Espero que esta introdución e os recursos proporcionados che sexan útiles para seguir aprendendo e practicando Grid! 😊


---

DAW🧊2025

#css
#DAW