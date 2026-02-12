# Elementos bloque e elementos en liña

En HTML, os elementos divídense en dous tipos principais segundo o seu comportamento no fluxo do documento: **nivel bloque** e **nivel inline**. Cada tipo ten características específicas e úsase para diferentes propósitos. Vou explicarche en detalle ambos conceptos e as etiquetas HTML máis comúns asociadas a cada un.

---

### **1. Elementos de nivel bloque (Block-level elements)**

#### **Características**:
- Ocupan todo o ancho do seu contedor pai.
- Comezan nunha nova liña.
- Poden conter outros elementos de nivel bloque e inline.
- Admiten propiedades CSS como `width`, `height`, `margin`, `padding`, etc.

#### **Etiquetas HTML comúns de nivel bloque**:
- **`<div>`**: Contedor xenérico para agrupar contido.
- **`<p>`**: Define un parágrafo.
- **`<h1>` a `<h6>`**: Cabeceiras ou títulos.
- **`<header>`**, **`<footer>`**, **`<section>`**, **`<article>`**, **`<nav>`**, **`<aside>`**: Elementos semánticos de HTML5.
- **`<ul>`**, **`<ol>`**, **`<li>`**: Listas non ordenadas, ordenadas e elementos de lista.
- **`<table>`**: Táboas.
- **`<form>`**: Formularios.
- **`<hr>`**: Liña horizontal.
- **`<blockquote>`**: Cita longa.

#### **Exemplo**:
```html
<div>
  <h1>Título principal</h1>
  <p>Este é un parágrafo dentro dun contedor.</p>
</div>
```

---

### **2. Elementos de nivel inline (Inline elements)**

#### **Características**:
- Ocupan só o espazo necesario para o seu contido.
- Non comezan nunha nova liña.
- Só poden conter outros elementos inline ou texto.
- Non admiten propiedades CSS como `width` ou `height` (a menos que se cambie o seu comportamento con `display: block` ou `display: inline-block`).

#### **Etiquetas HTML comúns de nivel inline**:
- **`<span>`**: Contedor xenérico para texto ou elementos inline.
- **`<a>`**: Ligazóns ou hipervínculos.
- **`<strong>`**, **`<em>`**: Texto importante ou con énfase.
- **`<img>`**: Imaxes.
- **`<br>`**: Salto de liña.
- **`<input>`**: Campos de formulario.
- **`<label>`**: Etiquetas para formularios.
- **`<code>`**: Código.
- **`<q>`**: Cita curta.
- **`<sub>`**, **`<sup>`**: Subíndices e superíndices.

#### **Exemplo**:
```html
<p>Este é un parágrafo con un <a href="#">ligazón</a> e unha <strong>palabra importante</strong>.</p>
```

---

### **3. Diferenzas clave entre nivel bloque e inline**

| Característica        | Nivel Bloque                    | Nivel Inline                    |
| --------------------- | ------------------------------- | ------------------------------- |
| **Ancho**             | Ocupa todo o ancho do contedor. | Ocupa só o espazo necesario.    |
| **Nova liña**         | Comeza nunha nova liña.         | Non comeza nunha nova liña.     |
| **Contido permitido** | Pode conter bloques e inline.   | Só pode conter inline ou texto. |
| **Propiedades CSS**   | Admite `width`, `height`, etc.  | Non admite `width`, `height`.   |

---

### **4. Elementos `inline-block`**
Hai un terceiro tipo de comportamento chamado **`inline-block`**, que combina características de ambos:
- Ocupa só o espazo necesario (como inline).
- Admite propiedades CSS como `width` e `height` (como bloque).

#### **Exemplo**:
```html
<span style="display: inline-block; width: 100px; height: 50px; background-color: lightblue;">
  Este é un elemento inline-block.
</span>
```

---

### **5. Etiquetas semánticas de HTML5**
HTML5 introduciu varias etiquetas semánticas que son de nivel bloque e axudan a estruturar mellor o contido:

- **`<header>`**: Cabeceira da páxina ou sección.
- **`<footer>`**: Pé de páxina ou sección.
- **`<section>`**: Sección temática do contido.
- **`<article>`**: Contido independente (como un artigo).
- **`<nav>`**: Menú de navegación.
- **`<aside>`**: Contido relacionado pero secundario (como unha barra lateral).
- **`<main>`**: Contido principal da páxina.

#### **Exemplo**:
```html
<header>
  <h1>Benvido ao meu sitio web</h1>
  <nav>
    <a href="#">Inicio</a> |
    <a href="#">Sobre</a> |
    <a href="#">Contacto</a>
  </nav>
</header>
<main>
  <section>
    <h2>Sobre nós</h2>
    <p>Información sobre a nosa empresa.</p>
  </section>
</main>
<footer>
  <p>&copy; 2023 O meu sitio web.</p>
</footer>
```

---

### **6. Resumo**
- **Nivel bloque**: Ocupan todo o ancho, comezan nunha nova liña e poden conter outros bloques e inline. Exemplos: `<div>`, `<p>`, `<h1>`-`<h6>`.
- **Nivel inline**: Ocupan só o espazo necesario, non comezan nunha nova liña e só poden conter inline ou texto. Exemplos: `<span>`, `<a>`, `<strong>`.
- **Inline-block**: Combina características de ambos. Exemplo: `<span style="display: inline-block;">`.

### 7. Lembra

As etiquetas `<footer>`, `<header>`, `<aside>` en HTML5 **non están limitadas a ser usadas ao final da páxina web, a cabeceira da paxina ou un lateral da mesma respectivamente**. Poden usarse en calquera sección ou elemento estrutural (como `<article>`, `<section>`, ou `<body>`) para proporcionar información adicional relevante para esa área específica.

#### Etiqueta `<footer>`

1. **Ao final da páxina**: O máis común, con información de contacto, enlaces legais ou copyright.
2. **Dentro dun `<article>`**: Para detalles do autor, datas de publicación ou taxonomías.
3. **Nunha `<section>`**: Por exemplo, nunha sección de comentarios, para enlaces relacionados.

**Código de exemplo:

```html
<article>
  <h2>Artigo sobre accesibilidade web</h2>
  <p>Contido do artigo...</p>
  <footer>  
    <p>Publicado por: Ana Pérez | Data: 25/10/2023</p>  
  </footer>  
</article>  
```

##### **Importancia semántica:**

O uso correcto de `<footer>` mellora a **accesibilidade** (lectores de pantalla interpretan mellor a estrutura) e o **SEO** (os buscadores entenden mellor o contido).

**Conclusión:** A etiqueta `<footer>` é flexible e semántica, e non está restrinxida só ao pé de páxina 😊.

#### Etiqueta `<header>`

- **Uso principal**: Contido introdutorio (títulos, logos, menús de navegación).  
- **Pode usarse en**:  
  - **Páxina completa**: O cabeceiro principal (ex: logo + menú global).  
  - **Seccións ou artigos**: Para introducir contido específico (ex: título dun artigo dentro de `<article>`).  

**Exemplo:**  

```html  
<article>  
  <header>  
    <h2>Guía de accesibilidade web</h2>  
    <p>Por: María López | Data: 01/11/2023</p>  
  </header>  
  <p>Contido do artigo...</p>  
</article>  
```

---

#### Etiqueta `<aside>`

- **Uso principal**: Contido relacionado **indirectamente** co contido principal (ex: barras laterais, glosarios, publicidade relevante).  
- **Pode usarse en**:  
  - **Calquera sección**: Dentro de `<article>`, `<section>`, e por suposto tamén no `<body>`.  
  - **Notas ou explicacións**: Comentarios adicionais que complementan o contido principal.  

**Exemplo:**  

```html  
<article>  
  <h2>Cambio climático</h2>  
  <p>Os efectos do quecemento global...</p>  
  <aside>  
    <h3>Dato curioso</h3>  
    <p>En 2023, a temperatura media aumentou 1.5°C respecto a 1900.</p>  
  </aside>  
</article>  
```

---

### **Conclusión:**  

- **Semántica > Posición**: En HTML5, as etiquetas (**`<header>`, `<footer>`, `<aside>`**) **non están limitadas a unha posición fixa**. O seu uso depende do **contexto semántico** do contido.  
- **Accesibilidade e SEO**: Usalas correctamente mellora a interpretación por lectores de pantalla e motores de busca 🚀.  

**Importante**: Evita usar estas etiquetas só por estética; prioriza o seu significado estrutural. 😊

---

### :tada:

DAW🧊2026

#html
#DAW