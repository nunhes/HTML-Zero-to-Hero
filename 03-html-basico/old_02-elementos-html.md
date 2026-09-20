# Elementos básicos de HTML

Nesta sección veremos os elementos fundamentais que compoñen a estrutura de calquera documento HTML: titulares, parágrafos e a distinción entre elementos de bloque e en liña.

---

## 1. Titulares (*headings*: `h1`-`h6`)

Os **headings** (cabeceiras ou encabezados) úsanse para definir títulos e subtítulos. Son fundamentais para estruturar o contido e mellorar o SEO.

- **`<h1>`**: Título principal da páxina (só debe haber un).
- **`<h2>` a `<h6>`**: Subtítulos e seccións secundarias.

```html
<h1>Benvido á miña páxina web</h1>
<h2>Sobre min</h2>
<p>Aquí tes algunha información sobre min.</p>
```

---

## 2. Parágrafos (`<p>`)

A etiqueta `<p>` define un bloque de texto. É un elemento de bloque, o que significa que sempre comeza nunha nova liña.

```html
<p>Este é un parágrafo de exemplo. Podes escribir aquí o teu texto.</p>
```

### Elementos comúns dentro de parágrafos:
- **`<strong>`**: Para texto en **negrita** (importancia semántica).
- **`<em>`**: Para texto en *cursiva* (énfase).
- **`<a>`**: Para engadir ligazóns.
- **`<br>`**: Para un salto de liña manual.

---

## 3. Elementos de bloque vs Elementos en liña

En HTML, os elementos divídense en dous tipos segundo o seu comportamento no fluxo do documento:

### **a) Elementos de nivel bloque (Block-level)**
- Ocupan todo o ancho do seu contedor.
- Comezan nunha nova liña.
- Exemplos: `<div>`, `<p>`, `<h1>`-`<h6>`, `<ul>`, `<table>`, `<form>`, `<header>`, `<footer>`.

### **b) Elementos de nivel inline (Inline)**
- Ocupan só o espazo necesario para o seu contido.
- Non comezan nunha nova liña.
- Exemplos: `<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<code>`.

| Característica | Nivel Bloque | Nivel Inline |
| :--- | :--- | :--- |
| **Ancho** | Todo o ancho do contedor | Só o necesario |
| **Nova liña** | Sempre comeza unha | Mantense na mesma liña |
| **Contido** | Pode conter outros bloques e inline | Só inline ou texto |

---

## 4. Etiquetas de formatado semántico

HTML5 ofrece etiquetas para dar significado ao texto alén da súa aparencia:

- **`<strong>` vs `<b>`**: Ambos locen en negrita, pero `<strong>` indica importancia.
- **`<em>` vs `<i>`**: Ambos locen en cursiva, pero `<em>` indica énfase.
- **`<mark>`**: Texto resaltado (como cun marcador).
- **`<small>`**: Texto secundario (letra pequena).
- **`<del>`**: Texto eliminado (tachado).
- **`<ins>`**: Texto engadido (subliñado).
- **`<sub>` e `<sup>`**: Subíndices e superíndices.

---

**Resumo**:
Usa os titulares (`h1`-`h6`) para a xerarquía, os parágrafos (`p`) para o texto, e comprende a diferenza entre bloque e en liña para controlar o deseño da túa páxina.

---

DAW🧊2026