# Introdución a CSS Flexbox
**Flexbox** (ou **Flexible Box Layout**) é un módulo de CSS deseñado para facilitar a creación de deseños flexibles e responsivos. Permíteche distribuir o espazo entre os elementos dun contedor e aliñalos de maneira eficiente, incluso cando o tamaño dos elementos é descoñecido ou dinámico.

Vou explicarche os conceptos básicos de Flexbox, as súas propiedades principais e como usalas para crear deseños complexos. Ademais, ao final, proporcionareiche algúns enlaces útiles para seguir aprendendo e practicando.

---

### **1. Conceptos básicos de Flexbox**

Flexbox funciona baseándose en dous eixes principais: o **eixe principal** (main axis) e o **eixe transversal** (cross axis). A dirección do eixe principal defínese pola propiedade `flex-direction`, mentres que o eixe transversal é perpendicular ao eixe principal.

- **Contedor flex (flex container)**: O elemento que contén os elementos flexibles. Defínese usando `display: flex` ou `display: inline-flex`.
- **Elementos flexibles (flex items)**: Os fillos directos do contedor flex.

---

### **2. Propiedades do contedor flex**

#### **`display`**
Define o contedor como un contedor flex.

- **Sintaxe**:
  ```css
  display: flex; /* Bloque flex */
  display: inline-flex; /* Inline flex */
  ```

#### **`flex-direction`**
Define a dirección do eixe principal.

- **Valores**:
  - `row` (predeterminado): Os elementos dispóñense en fila (de esquerda a dereita).
  - `row-reverse`: Os elementos dispóñense en fila (de dereita a esquerda).
  - `column`: Os elementos dispóñense en columna (de arriba a abaixo).
  - `column-reverse`: Os elementos dispóñense en columna (de abaixo a arriba).

- **Exemplo**:
  ```css
  .container {
    display: flex;
    flex-direction: row;
  }
  ```

#### **`justify-content`**
Aliña os elementos ao longo do eixe principal.

- **Valores**:
  - `flex-start` (predeterminado): Aliña os elementos ao inicio do eixe principal.
  - `flex-end`: Aliña os elementos ao final do eixe principal.
  - `center`: Aliña os elementos ao centro do eixe principal.
  - `space-between`: Distribúe o espazo entre os elementos.
  - `space-around`: Distribúe o espazo ao redor dos elementos.
  - `space-evenly`: Distribúe o espazo uniformemente entre e ao redor dos elementos.

- **Exemplo**:
  ```css
  .container {
    justify-content: space-between;
  }
  ```

#### **`align-items`**
Aliña os elementos ao longo do eixe transversal.

- **Valores**:
  - `stretch` (predeterminado): Estira os elementos para cubrir o contedor.
  - `flex-start`: Aliña os elementos ao inicio do eixe transversal.
  - `flex-end`: Aliña os elementos ao final do eixe transversal.
  - `center`: Aliña os elementos ao centro do eixe transversal.
  - `baseline`: Aliña os elementos pola súa liña base.

- **Exemplo**:
  ```css
  .container {
    align-items: center;
  }
  ```

#### **`align-content`**
Aliña as liñas de elementos cando hai espazo extra no eixe transversal (útil cando hai varias liñas de elementos).

- **Valores**:
  - `stretch` (predeterminado): Estira as liñas para cubrir o contedor.
  - `flex-start`: Aliña as liñas ao inicio do eixe transversal.
  - `flex-end`: Aliña as liñas ao final do eixe transversal.
  - `center`: Aliña as liñas ao centro do eixe transversal.
  - `space-between`: Distribúe o espazo entre as liñas.
  - `space-around`: Distribúe o espazo ao redor das liñas.

- **Exemplo**:
  ```css
  .container {
    align-content: space-around;
  }
  ```

#### **`flex-wrap`**
Controla se os elementos deben envolverse (wrap) ou non cando non caben nunha soa liña.

- **Valores**:
  - `nowrap` (predeterminado): Todos os elementos están nunha soa liña.
  - `wrap`: Os elementos envolven en varias liñas.
  - `wrap-reverse`: Os elementos envolven en varias liñas en orde inversa.

- **Exemplo**:
  ```css
  .container {
    flex-wrap: wrap;
  }
  ```

---

### **3. Propiedades dos elementos flexibles**

#### **`flex-grow`**
Define a proporción na que un elemento debe crecer se hai espazo dispoñible.

- **Valor**: Un número (0 ou positivo).
- **Exemplo**:
  ```css
  .item {
    flex-grow: 1;
  }
  ```

#### **`flex-shrink`**
Define a proporción na que un elemento debe reducirse se non hai espazo dispoñible.

- **Valor**: Un número (0 ou positivo).
- **Exemplo**:
  ```css
  .item {
    flex-shrink: 1;
  }
  ```

#### **`flex-basis`**
Define o tamaño inicial dun elemento antes de que se distribúa o espazo restante.

- **Valor**: Un tamaño (por exemplo, `auto`, `100px`, `50%`).
- **Exemplo**:
  ```css
  .item {
    flex-basis: 100px;
  }
  ```

#### **`flex`**
Abreviatura para `flex-grow`, `flex-shrink` e `flex-basis`.

- **Sintaxe**:
  ```css
  flex: flex-grow flex-shrink flex-basis;
  ```
- **Exemplo**:
  ```css
  .item {
    flex: 1 1 auto;
  }
  ```

#### **`align-self`**
Aliña un elemento individual ao longo do eixe transversal, sobrescribindo `align-items`.

- **Valores**: `auto`, `flex-start`, `flex-end`, `center`, `baseline`, `stretch`.
- **Exemplo**:
  ```css
  .item {
    align-self: flex-end;
  }
  ```

---

### **4. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar Flexbox para crear un layout simple:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flexbox en CSS</title>
  <style>
    .container {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      background-color: #f4f4f4;
      padding: 10px;
    }

    .item {
      background-color: #007bff;
      color: white;
      padding: 20px;
      margin: 10px;
      flex: 1 1 200px;
      text-align: center;
    }

    .item.special {
      flex-grow: 2;
      align-self: flex-end;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item special">Item 3 (Especial)</div>
    <div class="item">Item 4</div>
  </div>
</body>
</html>
```

#### **Explicación**:
1. **`.container`**:
   - Usa Flexbox para aliñar os elementos.
   - Distribúe o espazo entre os elementos con `justify-content: space-between`.
   - Aliña os elementos ao centro do eixe transversal con `align-items: center`.
   - Permite que os elementos se envolvan con `flex-wrap: wrap`.
2. **`.item`**:
   - Define un tamaño inicial de `200px` con `flex-basis: 200px`.
   - Permite que os elementos crezan e se reduzan con `flex: 1 1 200px`.
3. **`.item.special`**:
   - Crece máis que os outros elementos con `flex-grow: 2`.
   - Aliña este elemento ao final do eixe transversal con `align-self: flex-end`.

---

### **5. Recursos para seguir aprendendo e practicando**

Aquí tes algúns enlaces útiles para profundizar en Flexbox e practicar:

1. **Guía completa de Flexbox en CSS-Tricks**:
   - [A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/): Unha guía moi detallada con exemplos e diagramas.
   
2. **Flexbox Froggy (Xogo interactivo)**:
   - [Flexbox Froggy](https://flexboxfroggy.com/): Un xogo divertido para aprender Flexbox resolvendo puzzles.
   
3. **Flexbox Zombies (Xogo interactivo)**:
   - [Flexbox Zombies](https://mastery.games/flexboxzombies/): Outro xogo interactivo para aprender Flexbox de maneira lúdica.
   
4. **MDN Web Docs: Flexbox**:
   - [Flexbox en MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox): Documentación oficial de Mozilla sobre Flexbox.
   
5. **Flexbox Playground**:
   - [Flexbox Playground](https://demos.scotch.io/visual-guide-to-css3-flexbox-flexbox-playground/demos/): Unha ferramenta interactiva para experimentar con Flexbox.

---

### **6. Conclusión**

**Flexbox** é unha ferramenta poderosa e flexible para crear deseños CSS modernos e responsivos. Coñecer as súas propiedades e como combinalas permíteche crear layouts complexos de maneira eficiente. Espero que esta introdución e os recursos proporcionados che sexan útiles para seguir aprendendo e practicando Flexbox! 😊


---

DAW🧊2025

#css
#DAW