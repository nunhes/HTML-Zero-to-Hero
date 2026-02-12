# Últimos cambios e melloras en CSS

CSS é unha linguxe en constante evolución. Neste artigo farei unha breve **introdución aos últimos cambios e melloras en CSS**. baseándome na información da páxina que mencionas (. Estes cambios están a transformar a forma en que os desenvolvedores traballan con CSS, ofrecendo novas funcionalidades e mellorando a eficiencia do código.

---

### **1. CSS Nesting**

Unha das melloras máis esperadas é a **aniñación de CSS** (CSS Nesting), que permite aniñar selectores dentro doutros, similar a como se fai en preprocesadores como **SASS**.

#### **Exemplo tradicional (sen aniñación)**:
```css
.container {
  background-color: #f0f0f0;
}

.container .title {
  font-size: 2rem;
  color: #333;
}

.container .button {
  background-color: #007bff;
  color: #fff;
}
```

#### **Con aniñación**:
```css
.container {
  background-color: #f0f0f0;

  .title {
    font-size: 2rem;
    color: #333;
  }

  .button {
    background-color: #007bff;
    color: #fff;
  }
}
```

- **Beneficios**: Redúcese a repetición de código e mellórase a lexibilidade.

---

### **2. Container Queries**

As **consultas de contedor** (Container Queries) permiten aplicar estilos baseados no tamaño dun contedor específico, non só no tamaño da pantalla. Isto é especialmente útil para compoñentes reutilizables.

#### **Exemplo**:
```css
.component {
  container-type: inline-size;
}

@container (min-width: 400px) {
  .component {
    background-color: lightblue;
  }
}
```

- **Beneficios**: Permite crear compoñentes máis flexibles e independentes do contexto en que se usan.

---

### **3. Cascade Layers**

As **capas en cascada** (Cascade Layers) permiten organizar os estilos en capas, o que facilita a xestión de estilos complexos e evita conflitos.

#### **Exemplo**:
```css
@layer base, theme, utilities;

@layer base {
  body {
    font-family: Arial, sans-serif;
  }
}

@layer theme {
  .button {
    background-color: #007bff;
    color: #fff;
  }
}

@layer utilities {
  .text-center {
    text-align: center;
  }
}
```

- **Beneficios**: Control máis granular sobre a especificidade e a orde de aplicación dos estilos.

---

### **4. Subgrid**

A propiedade **subgrid** permite que os elementos dunha cuadrícula (grid) herden a estrutura da cuadrícula pai, o que facilita a creación de deseños complexos.

#### **Exemplo**:
```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.grid-item {
  display: grid;
  grid-template-rows: subgrid;
  grid-row: span 2;
}
```

- **Beneficios**: Simplifica a creación de deseños aniñados e mellora a consistencia visual.

---

### **5. Accent Color**

A propiedade **`accent-color`** permite cambiar a cor de elementos de formulario como checkboxes, radios e range inputs de forma sinxela.

#### **Exemplo**:
```css
input[type="checkbox"] {
  accent-color: #007bff;
}
```

- **Beneficios**: Personalización sinxela de elementos de formulario sen necesidade de CSS complexo.

---

### **6. Scroll Snap**

A propiedade **`scroll-snap`** permite crear efectos de desprazamento suave e preciso en contedores con desbordamento (overflow).

#### **Exemplo**:
```css
.container {
  scroll-snap-type: y mandatory;
  overflow-y: scroll;
  height: 300px;
}

.item {
  scroll-snap-align: start;
}
```

- **Beneficios**: Mellor experiencia de usuario en interfaces con desprazamento.

---

### **7. Aspect Ratio**

A propiedade **`aspect-ratio`** permite definir a relación de aspecto dun elemento, o que é útil para imaxes, vídeos e outros elementos multimedia.

#### **Exemplo**:
```css
.video {
  aspect-ratio: 16 / 9;
}
```

- **Beneficios**: Simplifica o mantemento da proporción dos elementos sen necesidade de cálculos manuais.

---

### **8. Logical Properties**

As **propiedades lóxicas** (Logical Properties) permiten definir estilos baseados na dirección do texto (por exemplo, esquerda/dereita ou inicio/fin), o que é útil para sitios multilingües.

#### **Exemplo**:
```css
.text {
  margin-inline-start: 1rem;
  padding-block-end: 2rem;
}
```

- **Beneficios**: Mellor soporte para idiomas con diferentes direccións de texto (por exemplo, árabe ou hebreo).

---

### **9. Color Functions**

CSS está a introducir novas funcións de cor, como **`color-mix()`**, que permiten mesturar cores de forma dinámica.

#### **Exemplo**:
```css
.element {
  background-color: color-mix(in srgb, #007bff, #fff 50%);
}
```

- **Beneficios**: Máis flexibilidade na creación de paletas de cores e efectos de cor.

---

### **10. Viewport Units**

As novas unidades de viewport, como **`svh`**, **`lvh`** e **`dvh**`, permiten un control máis preciso sobre o tamaño dos elementos en relación coa ventana gráfica.

#### **Exemplo**:
```css
.header {
  height: 100dvh;
}
```

- **Beneficios**: Mellor adaptación a dispositivos con barras de navegación dinámicas (como móbiles).

---

### **Conclusión**

Estas novas funcionalidades e melloras en CSS están a transformar a forma en que os desenvolvedores crean deseños web. Desde a aniñación de CSS ata as consultas de contedor, estas ferramentas ofrecen máis flexibilidade, eficiencia e control. 

Se queres profundizar nestes temas, podes consultar a páxina de [Frontend Masters](https://frontendmasters.com/blog/what-you-need-to-know-about-modern-css-spring-2024-edition) ou explorar documentación oficial como [MDN Web Docs](https://developer.mozilla.org/es/docs/Web/CSS).

---

### **Enlaces de interese**

1. **CSS Nesting**: [MDN - CSS Nesting](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting)
2. **Container Queries**: [MDN - Container Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries)
3. **Cascade Layers**: [MDN - Cascade Layers](https://developer.mozilla.org/en-US/docs/Web/CSS/@layer)
4. **Subgrid**: [MDN - Subgrid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Subgrid)
5. **Aspect Ratio**: [MDN - Aspect Ratio](https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio)

---

## Exemplo práctico

Imos crear unha **páxina de exemplo** que poña en práctica as últimas novidades de CSS que mencionamos. Esta páxina incluirá:

1. **CSS Nesting**
2. **Container Queries**
3. **Cascade Layers**
4. **Subgrid**
5. **Accent Color**
6. **Scroll Snap**
7. **Aspect Ratio**
8. **Logical Properties**
9. **Color Functions**
10. **Viewport Units**

---

### **Páxina de Exemplo: Galería de Produtos Interactiva**

#### **Estrutura do Proxecto**
1. **Arquivo HTML**: `index.html`
2. **Arquivo CSS**: `styles.css`

---

### **Código HTML (`index.html`)**

```html
<!DOCTYPE html>
<html lang="gl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Galería de Produtos</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Galería de Produtos</h1>
    </header>

    <main>
        <section class="product-grid">
            <article class="product">
                <img src="https://via.placeholder.com/400" alt="Produto 1">
                <h2>Produto 1</h2>
                <p>Descrición do produto 1.</p>
                <input type="checkbox" id="product1">
                <label for="product1">Seleccionar</label>
            </article>
            <article class="product">
                <img src="https://via.placeholder.com/400" alt="Produto 2">
                <h2>Produto 2</h2>
                <p>Descrición do produto 2.</p>
                <input type="checkbox" id="product2">
                <label for="product2">Seleccionar</label>
            </article>
            <!-- Engadir máis produtos aquí -->
        </section>

        <section class="scroll-section">
            <div class="scroll-item">Item 1</div>
            <div class="scroll-item">Item 2</div>
            <div class="scroll-item">Item 3</div>
            <div class="scroll-item">Item 4</div>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Galería de Produtos</p>
    </footer>
</body>
</html>
```

---

### **Código CSS (`styles.css`)**

```css
/* Capas en cascada */
@layer base, theme, utilities;

@layer base {
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        background-color: #f0f0f0;
    }

    header {
        background-color: #007bff;
        color: white;
        padding: 1rem;
        text-align: center;
    }

    footer {
        background-color: #333;
        color: white;
        text-align: center;
        padding: 1rem;
        margin-block-start: 2rem;
    }
}

@layer theme {
    .product-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 1rem;
        padding: 1rem;
        container-type: inline-size;
    }

    .product {
        background-color: white;
        border-radius: 0.5rem;
        padding: 1rem;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        display: grid;
        grid-template-rows: subgrid;
        grid-row: span 3;
    }

    .product img {
        aspect-ratio: 1 / 1;
        width: 100%;
        border-radius: 0.5rem;
    }

    .product h2 {
        font-size: 1.5rem;
        margin-block-start: 1rem;
    }

    .product p {
        color: #666;
    }

    .product input[type="checkbox"] {
        accent-color: #007bff;
    }

    .scroll-section {
        scroll-snap-type: x mandatory;
        overflow-x: scroll;
        display: flex;
        gap: 1rem;
        padding: 1rem;
        background-color: #e0e0e0;
    }

    .scroll-item {
        scroll-snap-align: start;
        flex: 0 0 200px;
        background-color: #007bff;
        color: white;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 0.5rem;
        height: 100px;
    }
}

@layer utilities {
    .text-center {
        text-align: center;
    }

    .margin-block-start {
        margin-block-start: 1rem;
    }
}

/* Consultas de contedor */
@container (min-width: 400px) {
    .product {
        background-color: #f9f9f9;
    }
}

/* Propiedades lóxicas */
.product h2 {
    margin-inline-start: 0.5rem;
}

/* Funcións de cor */
.product {
    background-color: color-mix(in srgb, white, #f0f0f0 10%);
}

/* Unidades de viewport */
header {
    height: 10dvh;
}

footer {
    height: 5dvh;
}
```

---

### **Explicación do Código**

1. **CSS Nesting**:
   - Usamos anidación para organizar os estilos dos produtos dentro do contedor `.product-grid`.

2. **Container Queries**:
   - Aplicamos un fondo diferente aos produtos cando o ancho do contedor é maior de 400px.

3. **Cascade Layers**:
   - Organizamos os estilos en capas (`base`, `theme`, `utilities`) para un mellor control da especificidade.

4. **Subgrid**:
   - Usamos `subgrid` para que os elementos dos produtos herden a estrutura da cuadrícula pai.

5. **Accent Color**:
   - Cambiamos a cor dos checkboxes usando `accent-color`.

6. **Scroll Snap**:
   - Creamos unha sección con desprazamento horizontal suave usando `scroll-snap-type`.

7. **Aspect Ratio**:
   - Definimos unha relación de aspecto 1:1 para as imaxes dos produtos.

8. **Logical Properties**:
   - Usamos `margin-inline-start` para aplicar marxes baseadas na dirección do texto.

9. **Color Functions**:
   - Usamos `color-mix` para crear un fondo lixeiramente máis escuro para os produtos.

10. **Viewport Units**:
    - Usamos `dvh` (dynamic viewport height) para definir a altura do cabeceiro e do pé de páxina.

---

### **Como Probar o Proxecto**

1. **Descargar o código**:
   - Copia o código HTML e CSS en dous arquivos (`index.html` e `styles.css`).

2. **Abrir no navegador**:
   - Abre o arquivo `index.html` no teu navegador para ver a páxina en acción.

3. **Experimentar**:
   - Modifica o código para ver como cambia o deseño. Por exemplo, cambia as cores, engade máis produtos ou modifica as consultas de contedor.

---

### **Enlaces de Interese**

1. **CSS Nesting**: [MDN - CSS Nesting](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting)
2. **Container Queries**: [MDN - Container Queries](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries)
3. **Cascade Layers**: [MDN - Cascade Layers](https://developer.mozilla.org/en-US/docs/Web/CSS/@layer)
4. **Subgrid**: [MDN - Subgrid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout/Subgrid)
5. **Aspect Ratio**: [MDN - Aspect Ratio](https://developer.mozilla.org/en-US/docs/Web/CSS/aspect-ratio)

---

Esta páxina de exemplo é unha forma práctica e educativa de poñer en práctica as últimas novidades de CSS. Podes adaptala ás necesidades dos teus alumnos e engadir máis funcionalidades segundo o nivel do curso. 😊

__ref:_ [Frontend Masters](https://frontendmasters.com/blog/what-you-need-to-know-about-modern-css-spring-2024-edition)


---

DAW🧊2025

#css
#DAW