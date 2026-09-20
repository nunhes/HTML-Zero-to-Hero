# CSS Grid Layout

**CSS Grid Layout** é un sistema de deseño bidimensional (filas e columnas) que permite crear estruturas complexas e responsivas sen necesidade de hacks como o uso de floats ou múltiples contedores anidados.

---

## 1. Conceptos de Grid

A diferenza de Flexbox, Grid traballa en dúas dimensións ao mesmo tempo.

- **Grid Container**: O elemento pai con `display: grid`.
- **Grid Item**: Os fillos directos do contedor.
- **Grid Line**: As liñas divisorias que forman a cuadrícula.
- **Grid Track**: O espazo entre dúas liñas (unha fila ou unha columna).
- **Grid Area**: O espazo rodeado por 4 liñas que pode conter un ou varios elementos.

---

## 2. Propiedades principais do Contedor

### **Definir a cuadrícula**
```css
.container {
  display: grid;
  grid-template-columns: 200px 1fr 1fr; /* 3 columnas */
  grid-template-rows: auto 100px;       /* 2 filas */
  gap: 20px;                            /* Espazo entre celas */
}
```

### **A unidade `fr`**
A unidade de fracción (`fr`) permite distribuír o espazo dispoñible de xeito proporcional, o que o fai ideal para deseños responsivos.

### **`grid-template-areas`**
Permite nomear áreas da páxina e situalas visualmente no código:
```css
.container {
  grid-template-areas: 
    "header header header"
    "nav    main   sidebar"
    "footer footer footer";
}
```

---

## 3. Propiedades dos Elementos

- **`grid-column` / `grid-row`**: Indica onde comeza e onde remata un elemento.
  - Ex: `grid-column: 1 / 3;` (ocupa dende a liña 1 á 3).
- **`grid-area`**: Asocia o elemento a un nome definido en `grid-template-areas`.

---

## 4. Xogo interactivo

- **[Grid Garden](https://cssgridgarden.com/)**: Aprende a crear cuadrículas cultivando cenorias no teu xardín.

---

**Resumo**:
CSS Grid é a ferramenta definitiva para deseñar a estrutura xeral (layout) dunha páxina web. Combinalo con Flexbox para os pequenos detalles de aliñación é a práctica recomendada hoxe en día.

---

DAW🧊2026
