# Selectores CSS

Os **selectores de CSS** son unha parte fundamental do deseño web, xa que permiten seleccionar e aplicar estilos a elementos específicos dun documento HTML. Coñecer os diferentes tipos de selectores e como usalos é esencial para crear deseños eficientes, organizados e mantibles.

Vexamos os conceptos básicos e avanzados dos selectores de CSS, incluíndo exemplos prácticos para que poidas entender como funcionan e cando usalos.

---

### **1. Que son os selectores de CSS?**

Os **selectores de CSS** son patróns que se usan para seleccionar os elementos HTML aos que se quere aplicar estilos. Un selector pode ser tan sinxelo como o nome dun elemento (por exemplo, `p` para seleccionar todos os parágrafos) ou tan complexo como unha combinación de clases, IDs, atributos e pseudo-clases.

---

### **2. Tipos de selectores de CSS**

#### **Selectores básicos**
1. **Selector de tipo**: Usa os nomes das etiquetas HTML e selecciona todos os elementos dun tipo específico. 
   
   ```css
   p {
     color: blue;
   }
   ```
   - Selecciona todos os elementos `<p>` e cambia a cor do texto a azul.
   
2. **Selector de clase**: Selecciona elementos cunha clase específica. As clases pódense reutilizar en varios elementos.
   ```css
   .destacado {
     background-color: yellow;
   }
   ```
   - Selecciona todos os elementos coa clase `destacado` e aplica un fondo amarelo.

3. **Selector de ID**: Selecciona un elemento cun ID específico. Os IDs deben ser únicos nun documento.
   ```css
   #cabezallo {
     font-size: 24px;
   }
   ```
   - Selecciona o elemento co ID `cabezallo` e cambia o tamaño da fonte a 24px.

4. **Selector universal**: Selecciona todos os elementos da páxina.
   ```css
   * {
     margin: 0;
     padding: 0;
   }
   ```
   - Elimina todos os márxenes e recheos de todos os elementos.

---

#### **Selectores avanzados**
1. **Selector descendente**: Selecciona elementos que están dentro doutros elementos.
   ```css
   div p {
     color: green;
   }
   ```
   - Selecciona todos os elementos `<p>` que están dentro dun `<div>`.

2. **Selector de fillo directo**: Selecciona elementos que son fillos directos doutro elemento.
   ```css
   ul > li {
     list-style: none;
   }
   ```
   - Selecciona todos os elementos `<li>` que son fillos directos dun `<ul>`.

3. **Selector de irmán adxacente**: Selecciona un elemento que está inmediatamente despois doutro elemento.
   ```css
   h1 + p {
     font-size: 18px;
   }
   ```
   - Selecciona o primeiro `<p>` que está inmediatamente despois dun `<h1>`.

4. **Selector de irmán xeral**: Selecciona todos os elementos que están despois doutro elemento.
   ```css
   h1 ~ p {
     color: red;
   }
   ```
   - Selecciona todos os elementos `<p>` que están despois dun `<h1>`.

5. **Selector de atributo**: Selecciona elementos baseados nun atributo ou valor de atributo.
   ```css
   a[target="_blank"] {
     color: purple;
   }
   ```
   - Selecciona todos os elementos `<a>` que teñen o atributo `target="_blank"`.

---

#### **Pseudo-clases e pseudo-elementos**
1. **Pseudo-clases**: Seleccionan elementos en estados específicos.
   ```css
   a:hover {
     color: orange;
   }
   ```
   - Cambia a cor dos enlaces a laranxa cando se pasa o rato por riba.

2. **Pseudo-elementos**: Seleccionan partes específicas dun elemento.
   ```css
   p::first-line {
     font-weight: bold;
   }
   ```
   - Fai que a primeira liña de cada `<p>` sexa en negrita.

---

### **3. Combinación de selectores**

Podes combinar selectores para crear regras máis específicas. Aquí tes algúns exemplos:

1. **Selector múltiple**: Aplica o mesmo estilo a varios selectores.
   ```css
   h1, h2, h3 {
     color: blue;
   }
   ```
   - Aplica a cor azul a todos os elementos `<h1>`, `<h2>` e `<h3>`.

2. **Selector descendente con clase**:
   ```css
   .container p {
     font-size: 16px;
   }
   ```
   - Selecciona todos os elementos `<p>` dentro dun elemento coa clase `container`.

3. **Selector de fillo directo con clase**:
   ```css
   .menu > li {
     padding: 10px;
   }
   ```
   - Selecciona todos os elementos `<li>` que son fillos directos dun elemento coa clase `menu`.

---

### **4. Especificidade dos selectores**

A **especificidade** é o mecanismo que determina que regra CSS se aplica cando hai conflitos entre selectores. A especificidade calcúlase baseándose no tipo de selector:

- **Inline styles** (estilos en liña): `1000` puntos.
- **IDs**: `100` puntos por cada ID.
- **Clases, pseudo-clases e atributos**: `10` puntos por cada un.
- **Elementos e pseudo-elementos**: `1` punto por cada un.

Exemplo:
```css
p {
  color: red; /* Especificidade: 1 */
}

.destacado {
  color: blue; /* Especificidade: 10 */
}

#cabezallo {
  color: green; /* Especificidade: 100 */
}

p.destacado {
  color: purple; /* Especificidade: 11 (1 + 10) */
}
```

---

### 5. Pseudo-clases e pseudo-elementos

Claro! As **pseudo-clases** e **pseudo-elementos** son características avanzadas de CSS que permiten seleccionar e aplicar estilos a elementos en estados específicos ou a partes específicas dun elemento. Estas ferramentas son moi útiles para crear efectos dinámicos e deseños máis complexos sen necesidade de JavaScript ou HTML adicional.

Vou explicarche con detalle que son as pseudo-clases e pseudo-elementos, como funcionan e como usalos con exemplos prácticos.

---

#### **5.1. Pseudo-clases**

As **pseudo-clases** permítenche seleccionar elementos baseados no seu estado ou posición nun documento. Non se refiren a un elemento específico, senón a un estado ou condición que se aplica a ese elemento.

##### **Pseudo-clases máis comúns**

1. **`:hover`**: Selecciona un elemento cando o usuario pasa o rato por riba.
   ```css
   a:hover {
     color: orange;
   }
   ```
   - Cambia a cor dos enlaces a laranxa cando se pasa o rato por riba.

2. **`:active`**: Selecciona un elemento cando está sendo activado (por exemplo, cando se fai clic nun botón).
   ```css
   button:active {
     background-color: red;
   }
   ```
   - Cambia o fondo do botón a vermello cando se fai clic nel.

3. **`:focus`**: Selecciona un elemento cando recibe o foco (por exemplo, cando se fai clic nun campo de formulario).
   ```css
   input:focus {
     border-color: blue;
   }
   ```
   - Cambia a cor do bordo do campo de entrada a azul cando recibe o foco.

4. **`:nth-child()`**: Selecciona elementos baseados na súa posición nun grupo de irmáns.
   ```css
   li:nth-child(odd) {
     background-color: #f4f4f4;
   }
   ```
   - Aplica un fondo gris claro a todos os elementos `<li>` impares.

5. **`:first-child` e `:last-child`**: Seleccionan o primeiro ou o último elemento nun grupo de irmáns.
   ```css
   p:first-child {
     font-weight: bold;
   }
   ```
   - Fai que o primeiro `<p>` dun contedor sexa en negrita.

6. **`:not()`**: Selecciona elementos que non coinciden cun selector específico.
   ```css
   p:not(.destacado) {
     color: gray;
   }
   ```
   - Aplica a cor gris a todos os elementos `<p>` que non teñen a clase `destacado`.

---

#### **5.2. Pseudo-elementos**

Os **pseudo-elementos** permítenche seleccionar e aplicar estilos a partes específicas dun elemento, como a primeira liña ou a primeira letra dun texto.

##### **Pseudo-elementos máis comúns**

1. **`::before` e `::after`**: Insiren contido antes ou despois do contido dun elemento.
   ```css
   p::before {
     content: "★ ";
     color: gold;
   }
   ```
   - Engade unha estrela dourada antes de cada `<p>`.

2. **`::first-line`**: Selecciona a primeira liña dun bloque de texto.
   ```css
   p::first-line {
     font-weight: bold;
   }
   ```
   - Fai que a primeira liña de cada `<p>` sexa en negrita.

3. **`::first-letter`**: Selecciona a primeira letra dun bloque de texto.
   ```css
   p::first-letter {
     font-size: 2em;
     color: red;
   }
   ```
   - Fai que a primeira letra de cada `<p>` sexa máis grande e de cor vermella.

4. **`::selection`**: Selecciona o texto que o usuario selecciona co rato.
   ```css
   ::selection {
     background-color: yellow;
     color: black;
   }
   ```
   - Cambia o fondo do texto seleccionado a amarelo e a cor do texto a negro.

---

#### **5.3. Diferenzas entre pseudo-clases e pseudo-elementos**

- **Pseudo-clases**: Seleccionan elementos baseados no seu estado ou posición (por exemplo, `:hover`, `:nth-child`).
- **Pseudo-elementos**: Seleccionan partes específicas dun elemento (por exemplo, `::first-line`, `::before`).

---

#### **5.4. Exemplos prácticos**

Aquí tes un exemplo completo que mostra como usar pseudo-clases e pseudo-elementos:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pseudo-clases e Pseudo-elementos</title>
  <style>
    /* Pseudo-clase :hover */
    a:hover {
      color: orange;
    }

    /* Pseudo-clase :nth-child */
    li:nth-child(odd) {
      background-color: #f4f4f4;
    }

    /* Pseudo-clase :first-child */
    p:first-child {
      font-weight: bold;
    }

    /* Pseudo-elemento ::before */
    p::before {
      content: "★ ";
      color: gold;
    }

    /* Pseudo-elemento ::first-line */
    p::first-line {
      font-weight: bold;
    }

    /* Pseudo-elemento ::selection */
    ::selection {
      background-color: yellow;
      color: black;
    }
  </style>
</head>
<body>
  <h1>Pseudo-clases e Pseudo-elementos</h1>
  <p>Este é o primeiro parágrafo.</p>
  <p>Este é o segundo parágrafo.</p>
  <ul>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
    <li>Elemento 3</li>
    <li>Elemento 4</li>
  </ul>
  <a href="#">Enlace de exemplo</a>
</body>
</html>
```

---

Hai moitas pseudo-clases e pseudo-elementos  dispoñibles en CSS. Ata aquí só mencionei as máis comúns e útiles para a maioría dos casos de uso. Se queres unha lista máis completa, aquí tes un resumo máis exhaustivo das **pseudo-clases** e **pseudo-elementos** en CSS:

---

#### **Pseudo-clases**

As pseudo-clases permítenche seleccionar elementos baseados no seu estado, posición ou outras condicións. Aquí tes unha lista máis completa:

##### **Pseudo-clases de estado**
1. **`:hover`**: Selecciona un elemento cando o usuario pasa o rato por riba.
2. **`:active`**: Selecciona un elemento cando está sendo activado (por exemplo, cando se fai clic nun botón).
3. **`:focus`**: Selecciona un elemento cando recibe o foco (por exemplo, cando se fai clic nun campo de formulario).
4. **`:visited`**: Selecciona enlaces que xa foron visitados.
5. **`:link`**: Selecciona enlaces que aínda non foron visitados.
6. **`:checked`**: Selecciona elementos de formulario que están marcados (como checkboxes ou radio buttons).
7. **`:disabled`**: Selecciona elementos de formulario que están desactivados.
8. **`:enabled`**: Selecciona elementos de formulario que están activados.
9. **`:required`**: Selecciona elementos de formulario que son obrigatorios.
10. **`:optional`**: Selecciona elementos de formulario que son opcionais.
11. **`:valid`**: Selecciona elementos de formulario cun valor válido.
12. **`:invalid`**: Selecciona elementos de formulario cun valor inválido.
13. **`:in-range`**: Selecciona elementos de formulario cun valor dentro dun rango específico.
14. **`:out-of-range`**: Selecciona elementos de formulario cun valor fóra dun rango específico.
15. **`:read-only`**: Selecciona elementos de formulario que son de só lectura.
16. **`:read-write`**: Selecciona elementos de formulario que son editables.

##### **Pseudo-clases de posición**
1. **`:first-child`**: Selecciona o primeiro elemento fillo do seu pai.
2. **`:last-child`**: Selecciona o último elemento fillo do seu pai.
3. **`:nth-child(n)`**: Selecciona o n-ésimo elemento fillo do seu pai.
4. **`:nth-last-child(n)`**: Selecciona o n-ésimo elemento fillo do seu pai, contando desde o final.
5. **`:first-of-type`**: Selecciona o primeiro elemento do seu tipo entre os seus irmáns.
6. **`:last-of-type`**: Selecciona o último elemento do seu tipo entre os seus irmáns.
7. **`:nth-of-type(n)`**: Selecciona o n-ésimo elemento do seu tipo entre os seus irmáns.
8. **`:nth-last-of-type(n)`**: Selecciona o n-ésimo elemento do seu tipo entre os seus irmáns, contando desde o final.
9. **`:only-child`**: Selecciona elementos que son o único fillo do seu pai.
10. **`:only-of-type`**: Selecciona elementos que son o único do seu tipo entre os seus irmáns.

##### **Outras pseudo-clases**
1. **`:not(selector)`**: Selecciona elementos que non coinciden co selector especificado.
2. **`:target`**: Selecciona o elemento ao que se lle fixo referencia nunha URL con un identificador (por exemplo, `#section1`).
3. **`:root`**: Selecciona o elemento raíz do documento (normalmente `<html>`).
4. **`:empty`**: Selecciona elementos que non teñen fillos (nin texto nin elementos).
5. **`:lang()`**: Selecciona elementos baseados no idioma especificado (por exemplo, `:lang(gl)` para galego).

---

#### **Pseudo-elementos**

Os pseudo-elementos permítenche seleccionar e aplicar estilos a partes específicas dun elemento. Aquí tes unha lista completa:

1. **`::before`**: Insire contido antes do contido dun elemento.
   ```css
   p::before {
     content: "★ ";
     color: gold;
   }
   ```

2. **`::after`**: Insire contido despois do contido dun elemento.
   ```css
   p::after {
     content: " ★";
     color: gold;
   }
   ```

3. **`::first-line`**: Selecciona a primeira liña dun bloque de texto.
   ```css
   p::first-line {
     font-weight: bold;
   }
   ```

4. **`::first-letter`**: Selecciona a primeira letra dun bloque de texto.
   ```css
   p::first-letter {
     font-size: 2em;
     color: red;
   }
   ```

5. **`::selection`**: Selecciona o texto que o usuario selecciona co rato.
   ```css
   ::selection {
     background-color: yellow;
     color: black;
   }
   ```

6. **`::placeholder`**: Selecciona o texto de marcador de posición (placeholder) nun campo de formulario.
   ```css
   input::placeholder {
     color: gray;
   }
   ```

7. **`::marker`**: Selecciona os marcadores de elementos de lista (como os puntos ou números).
   ```css
   li::marker {
     color: red;
   }
   ```

8. **`::backdrop`**: Selecciona o fondo dun elemento en modo de pantalla completa (como un vídeo ou imaxe).
   ```css
   video::backdrop {
     background-color: black;
   }
   ```

---

#### **Exemplo completo**

Aquí tes un exemplo que usa varias pseudo-clases e pseudo-elementos:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Pseudo-clases e Pseudo-elementos</title>
  <style>
    /* Pseudo-clase :hover */
    a:hover {
      color: orange;
    }

    /* Pseudo-clase :nth-child */
    li:nth-child(odd) {
      background-color: #f4f4f4;
    }

    /* Pseudo-clase :first-child */
    p:first-child {
      font-weight: bold;
    }

    /* Pseudo-elemento ::before */
    p::before {
      content: "★ ";
      color: gold;
    }

    /* Pseudo-elemento ::first-line */
    p::first-line {
      font-weight: bold;
    }

    /* Pseudo-elemento ::selection */
    ::selection {
      background-color: yellow;
      color: black;
    }

    /* Pseudo-clase :checked */
    input[type="checkbox"]:checked + label {
      color: green;
    }

    /* Pseudo-elemento ::placeholder */
    input::placeholder {
      color: gray;
    }
  </style>
</head>
<body>
  <h1>Pseudo-clases e Pseudo-elementos</h1>
  <p>Este é o primeiro parágrafo.</p>
  <p>Este é o segundo parágrafo.</p>
  <ul>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
    <li>Elemento 3</li>
    <li>Elemento 4</li>
  </ul>
  <a href="#">Enlace de exemplo</a>

  <form>
    <input type="checkbox" id="check">
    <label for="check">Marcar</label>
    <input type="text" placeholder="Escribe algo...">
  </form>
</body>
</html>
```

---

#### **5.5. Conclusión**

As **pseudo-clases** e **pseudo-elementos** son ferramentas moi poderosas en CSS que permiten seleccionar e aplicar estilos a elementos en estados específicos ou a partes específicas dun elemento. Ademais permiten crear efectos dinámicos e deseños máis complexos. 

As pseudo-clases permítenche seleccionar elementos baseados no seu estado ou posición, mentres que os pseudo-elementos permítenche aplicar estilos a partes específicas dun elemento.

Coñecer e usar estas características pode mellorar significativamente a túa capacidade para crear deseños web dinámicos, atractivos e funcionais. Espero que esta lista completa e o exemplo che sexan útiles! 😊

---

### **6. Boas prácticas no uso de selectores**

1. **Evita o uso excesivo de IDs**: Os IDs son moi específicos e poden dificultar a reutilización de estilos. Prefire o uso de clases.
2. **Usa selectores descritivos**: Nomea as clases e IDs de maneira descritiva para que o código sexa máis lexible.
3. **Mantén a especificidade baixa**: Canto menor sexa a especificidade, máis fácil será sobrescribir estilos se é necesario.
4. **Evita o uso de `!important`**: O uso excesivo de `!important` pode facer que o código sexa difícil de manter.

---

### **7. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar diferentes tipos de selectores:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Selectores de CSS</title>
  <style>
    /* Selector de tipo */
    h1 {
      color: blue;
    }

    /* Selector de clase */
    .destacado {
      background-color: yellow;
    }

    /* Selector de ID */
    #cabezallo {
      font-size: 24px;
    }

    /* Selector descendente */
    div p {
      color: green;
    }

    /* Selector de fillo directo */
    ul > li {
      list-style: none;
    }

    /* Selector de irmán adxacente */
    h1 + p {
      font-size: 18px;
    }

    /* Selector de atributo */
    a[target="_blank"] {
      color: purple;
    }

    /* Pseudo-clase */
    a:hover {
      color: orange;
    }

    /* Pseudo-elemento */
    p::first-line {
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Selectores de CSS</h1>
  <p>Este é un exemplo de selector de tipo.</p>
  <p class="destacado">Este parágrafo ten unha clase destacado.</p>
  <div>
    <p>Este parágrafo está dentro dun div.</p>
  </div>
  <ul>
    <li>Elemento 1</li>
    <li>Elemento 2</li>
  </ul>
  <a href="#" target="_blank">Enlace con target _blank</a>
</body>
</html>
```

---

### **8. Conclusión**

Os **selectores de CSS** son unha ferramenta poderosa para aplicar estilos a elementos HTML de maneira precisa e eficiente. Coñecer os diferentes tipos de selectores, como combinálos e como xestionar a especificidade é esencial para crear deseños web organizados e mantibles. Espero que esta explicación e exemplo che sexan útiles para dominar o uso de selectores en CSS! 😊


---

DAW🧊2025

#css
#DAW