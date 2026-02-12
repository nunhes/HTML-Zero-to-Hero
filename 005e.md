# **Elementos de ancoraxe e atributos en HTML**

Nesta lección, imos profundizar noutro aspecto importante de HTML: os **atributos**. Especificamente, imos aprender sobre o **elemento de ancoraxe** (`<a>`), que nos permite crear **hiperligazóns** (links) nas nosas páxinas web.

---

### **O Elemento de ancoraxe (`<a>`)**

O elemento de ancoraxe ten unha estrutura similar a outros elementos HTML, cunha **etiqueta de apertura** e unha **etiqueta de peche**. Por exemplo:

```html
<a>Este é un enlace</a>
```

Porén, se escribimos o código así, o enlace non será funcional. Para que funcione, necesitamos engadir un **atributo** chamado `href` (hypertext reference), que especifica a URL á que debe dirixirse o enlace.

#### **Estrutura dun atributo**
Os atributos engádense na **etiqueta de apertura** do elemento, despois do nome da etiqueta e antes do corchete angular de peche (`>`). A estrutura básica é:

```html
<nome-da-etiqueta nome-do-atributo="valor-do-atributo">
```

Por exemplo, para crear un enlace a Google:

```html
<a href="https://www.google.com">Visita Google</a>
```

Neste caso, `href` é o nome do atributo, e `"https://www.google.com"` é o seu valor.

---

### **Atributos específicos e globais**

- **Atributos específicos**: Algúns atributos, como `href`, son específicos de certos elementos. Por exemplo, o atributo `href` só se usa en elementos de ancoraxe (`<a>`).
- **Atributos globais**: Outros atributos, como `draggable`, poden usarse en calquera elemento HTML. Por exemplo:

```html
<a href="https://www.google.com" draggable="true">Arrastra este enlace</a>
```

Neste caso, o atributo `draggable="true"` permite que o enlace sexa arrastrado pola páxina.

---

### **Exercicio práctico: Lista de sitios web favoritos**

Agora é o teu turno. Vamos crear unha páxina web que mostre os teus **cinco sitios web favoritos**. O obxectivo é usar unha **lista ordenada** (`<ol>`) e engadir **enlaces** a cada sitio web.

#### **Pasos para o Exercicio:**
1. Crea unha lista ordenada (`<ol>`) con cinco elementos.
2. Dentro de cada elemento da lista (`<li>`), engade un **elemento de ancoraxe** (`<a>`) que apunte ao sitio web correspondente.
3. Asegúrate de que cada enlace teña o atributo `href` coa URL correcta.

#### **Exemplo de código:**
```html
<h1>Os meus cinco sitios web favoritos</h1>
<ol>
  <li><a href="https://www.producthunt.com">Product Hunt</a></li>
  <li><a href="https://www.example.com">Exemplo 2</a></li>
  <li><a href="https://www.example.com">Exemplo 3</a></li>
  <li><a href="https://www.example.com">Exemplo 4</a></li>
  <li><a href="https://www.example.com">Exemplo 5</a></li>
</ol>
```

---

### **Desafío adicional: Cambiar o inicio da lista ordenada**

Como desafío adicional, podes modificar o atributo `start` da lista ordenada para que a numeración comece desde **5** en vez de **1**. Para iso, engade o atributo `start="5"` á etiqueta `<ol>`:

```html
<ol start="5">
  <li><a href="https://www.producthunt.com">Product Hunt</a></li>
  <li><a href="https://www.example.com">Exemplo 2</a></li>
  <li><a href="https://www.example.com">Exemplo 3</a></li>
  <li><a href="https://www.example.com">Exemplo 4</a></li>
  <li><a href="https://www.example.com">Exemplo 5</a></li>
</ol>
```

Neste caso, a lista comezará a numerarse desde **5** ata **9**.

---

### **Recursos adicionais**

- **Documentación oficial de HTML**: [MDN Web Docs - Elemento de Ancoraxe](https://developer.mozilla.org/es/docs/Web/HTML/Element/a)
- **Lista de Atributos Globais**: [MDN Web Docs - Atributos Globais](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes)
- **Visual Studio Code**: [Descarga VS Code](https://code.visualstudio.com/)

---

### **Conclusión**

Os **elementos de ancoraxe** e os **atributos** son fundamentais para crear enlaces e personalizar o comportamento dos elementos HTML. Dominar estes conceptos permitiráche crear páxinas web máis interactivas e funcionales. Practica con este exercicio e, se tes dúbidas, non dubides en preguntar. 🚀


---

DAW🧊2026

#html
#DAW