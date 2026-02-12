# Elementos baleiros

Vexamos agora os **elementos baleiros** (void elements), como a **regra horizontal** (`<hr>`) e o **elemento de salto de liña** (`<br>`).

Pero, **que son exactamente os elementos baleiros?**

Xa vimos elementos non baleiros, como o elemento **parágrafo** (`<p>`) ou os **encabezados** (`<h1>`, `<h2>`, etc.), que non son baleiros xa que teñen contido entre a etiqueta de apertura e a de peche.

Un **elemento baleiro** é un elemento no que non está permitido incluír ningún contido dentro da etiqueta. De feito, a propia etiqueta ten un aspecto diferente.

Por exemplo, este é un elemento de **regra horizontal** (`<hr>`). Podes ver que comeza cun corchete angular (`<`) e remata cun corchete angular de peche (`>`), pero antes do peche hai unha **barra diagonal** (`/`).

Isto pode parecerse un pouco á etiqueta de peche dun elemento HTML normal, pero é sutilmente diferente. Nas etiquetas de peche, a barra diagonal está xusto despois do corchete angular de apertura (`</`), mentres que nos elementos baleiros, a barra diagonal está xusto antes do peche da etiqueta (`/>`). Ademais, por convención, adoita haber un espazo entre o nome da etiqueta e a barra diagonal, como en `<hr />` ou `<br />`.

É importante ter coidado ao escribir estes elementos baleiros. Asegúrate de que a barra diagonal (`/`) vaia na dirección correcta (`/`).

---

### **Exemplos prácticos**

Vexamos como se ve isto nun documento HTML. Aquí temos dous parágrafos e, no medio, engadimos unha **regra horizontal** (`<hr />`) para separar o contido.

```html
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque vitae leo vitae diam rhoncus condimentum. Mauris vestibulum odio eget mi fringilla pulvinar. Duis pretium sollicitudin nulla, quis feugiat enim venenatis ut.</p>
<hr />
<p>Curabitur et consequat dui, varius vestibulum sem. Quisque vel massa ultrices, pharetra odio et, porta ante. Sed et iaculis arcu. Suspendisse at libero tincidunt, ultricies turpis sed, mollis nisl.</p>
```

Cando executamos este código no navegador, veremos o primeiro parágrafo, unha liña horizontal e logo o segundo parágrafo.

A regra horizontal non é o único elemento baleiro que atoparemos en HTML. Outro elemento baleiro común é o **elemento de salto de liña** (`<br />`), que se usa para separar liñas dentro dun mesmo parágrafo. Por exemplo, se temos un poema, cada verso debe estar nunha liña separada, pero todos deben formar parte do mesmo parágrafo. Aquí é onde o `<br />` é útil.

Vexamos un exemplo co poema *"Negra sombra"* de Rosalía de Castro:

```html
<p>
  Cando penso que te fuches<br />
  negra sombra que me asombras,<br />
  ó pe dos meus cabezales<br />
  tornas facéndome mofa.
</p>
```

Cando este código se renderiza no navegador, cada verso aparece nunha liña separada, grazas ao uso do `<br />`.

---

### **Exercicio práctico**

Agora é o teu turno.

Aquí tes un exercicio práctico para practicar o uso do elemento `<br />` cun poema dun autor galego. Usaremos un fragmento do poema **"Adiós ríos, adiós fontes"** de **Rosalía de Castro**, unha das figuras máis importantes da literatura galega.

------

#### Formatando un poema con `<br />`

#### **Instrucións:**

1. Crea un arquivo HTML chamado `poema.html`.
2. O título do poema será un **encabezado** (`<h1>`).
3. O nome do poeta será un **encabezado** (``<h4>``).
4. Engade unha **regra horizontal** (`<hr />`) entre o titulo e o nome do autor e outra entre o autor e o poema.
5. Usa a etiqueta `<p>` para envolver o poema.
6. Usa a etiqueta `<br />` para separar cada verso do poema.
7. Asegúrate de que o poema se renderice correctamente no navegador, con cada verso nunha liña separada.

#### Poema:

```
Adiós ríos, adiós fontes,
adiós, regatos pequenos;
adiós, vista dos meus ollos,
non sei cando nos veremos.
```

#### **Estrutura HTML agardada:**

```html
<!DOCTYPE html>
<html lang="gl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Poema de Rosalía de Castro</title>
</head>
<body>
	<h1><em>Adiós ríos, adiós fontes</em></h1>
	<hr />
    <h4>Rosalía de Castro</h4>
    <hr />
    <p>
        Adiós ríos, adiós fontes,<br />
        adiós, regatos pequenos;<br />
        adiós, vista dos meus ollos,<br />
        non sei cando nos veremos.
    </p>
</body>
</html>
```

------

### **Pasos adicionais:**

1. **Proba o código**: Abre o arquivo `poema.html` no teu navegador para asegurarte de que cada verso aparece nunha liña separada.
2. **Experimenta**: Intenta engadir máis versos do poema ou outro poema de Rosalía de Castro, como **"Cantares Galegos"**.
3. **Accesibilidade**: Pensa en como este formato afecta á accesibilidade. Sería mellor usar varias etiquetas `<p>` en vez de `<br />`? Discute as vantaxes e desvantaxes.

------

### **Boas Prácticas con elementos baleiros**

- **Non abuses do `<br />`**: Úsao só cando é necesario, como en poemas ou enderezos. Para separar parágrafos, usa sempre a etiqueta `<p>`.
- **Accesibilidade**: Os lectores de pantalla para persoas con discapacidade visual funcionan mellor cando se usan elementos semánticos correctamente.
- **Formato de etiquetas**: Aínda que en HTML5 a barra diagonal final (`/>`) é opcional, recoméndase usala para facer o código máis lexible.

---

### **Recursos adicionais**

- **Documentación oficial de HTML**: [MDN Web Docs - Elementos baleiros](https://developer.mozilla.org/es/docs/Glossary/Void_element)
- **Ferramentas de comparación de código**: [Diffchecker](https://www.diffchecker.com)
- **Titorias de HTML**: [W3Schools - HTML Elements](https://www.w3schools.com/html/html_elements.asp)
- **Documentación sobre `<br />`**: [MDN Web Docs -](https://developer.mozilla.org/es/docs/Web/HTML/Element/br)
- **Poesía completa de Rosalía de Castro**: [Biblioteca Virtual Galega](http://www.bvg.udc.es/)

---

### **Conclusión**

Os elementos baleiros, como `<hr />` e `<br />`, son ferramentas útiles para formatar contido en HTML. Aprender a usalos correctamente é esencial para crear páxinas web ben estruturadas e accesibles. Se tes dúbidas ou precisas máis información, non dubides en consultar os recursos anteriores ou preguntar. 🚀


---

DAW🧊2026

#html
#DAW