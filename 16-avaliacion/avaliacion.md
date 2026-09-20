Preguntas de avaliación sobre os temas tratados (HTML5, CSS, formularios, semántica, atributos ARIA, etc.). 

Incluíren diferentes tipos de preguntas, como múltiple selección, verdadeiro/falso, relación de conceptos, completar frases, completado de código, corrección de código, e outras. Tamén proporcionarei as solucións para cada pregunta.

---

### **Preguntas de avaliación**

#### **1. Múltiple selección**

**Pregunta 1**: Cal das seguintes etiquetas HTML5 é semántica?
a) `<div>`  
b) `<span>`  
c) `<article>`  
d) `<bold>`  

**Solución**: c) `<article>`

---

**Pregunta 2**: Cal dos seguintes atributos é válido para a etiqueta `<input>`?
a) `type="text"`  
b) `type="color"`  
c) `type="date"`  
d) Todos os anteriores  

**Solución**: d) Todos os anteriores

---

**Pregunta 3**: Cal dos seguintes atributos ARIA se usa para describir o estado dun elemento?
a) `aria-label`  
b) `aria-expanded`  
c) `aria-hidden`  
d) `aria-describedby`  

**Solución**: b) `aria-expanded`

---

#### **2. Verdadeiro/Falso**

**Pregunta 4**: O atributo `required` en HTML5 só se pode usar en campos de texto.  
**Solución**: Falso (pódese usar en moitos tipos de campos, como `email`, `number`, etc.).

---

**Pregunta 5**: A etiqueta `<footer>` só se pode usar ao final dunha páxina web.  
**Solución**: Falso (pódese usar ao final dunha sección ou artigo).

---

**Pregunta 6**: O modelo de caixa en CSS inclúe o contido, recheo, borde e marxe.  
**Solución**: Verdadeiro.

---

#### **3. Relacionar conceptos e definicións**

**Pregunta 7**: Relaciona cada etiqueta HTML co seu propósito:
1) `<nav>`  
2) `<aside>`  
3) `<figure>`  
4) `<time>`  

a) Contido relacionado pero secundario.  
b) Navegación principal.  
c) Contido multimedia con descrición.  
d) Representa unha data ou hora.  

**Solución**:  
1) b) Navegación principal.  
2) a) Contido relacionado pero secundario.  
3) c) Contido multimedia con descrición.  
4) d) Representa unha data ou hora.

---

#### **4. Selección única**

**Pregunta 8**: Cal das seguintes etiquetas úsase para crear unha lista desordenada?
a) `<ol>`  
b) `<ul>`  
c) `<li>`  
d) `<dl>`  

**Solución**: b) `<ul>`

---

**Pregunta 9**: Cal dos seguintes atributos se usa para asociar unha etiqueta a un campo de formulario?
a) `for`  
b) `id`  
c) `name`  
d) `value`  

**Solución**: a) `for`

---

#### **5. Completar frase**

**Pregunta 10**: O atributo `_____` en HTML5 permíteche almacenar información personalizada nun elemento.  
**Solución**: `data-*`

---

**Pregunta 11**: A propiedade CSS `_____` controla o espazo interior dun elemento.  
**Solución**: `padding`

---

#### **6. Completado de código**

**Pregunta 12**: Completa o código para crear un formulario con un campo de texto e un botón de envío.
```html
<form _____="/procesar-datos" _____="POST">
  <label for="nome">Nome:</label>
  <input type="_____" id="nome" name="nome" _____>
  <button type="_____">Enviar</button>
</form>
```
**Solución**:

```html
<form action="/procesar-datos" method="POST">
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome" required>
  <button type="submit">Enviar</button>
</form>
```

---

#### **7. Corrección de código**

**Pregunta 13**: Corrixe o seguinte código HTML:
```html
<img scr="logo.png" alt="Logo da empresa">
```
**Solución**:
```html
<img src="logo.png" alt="Logo da empresa">
```

---

**Pregunta 14**: Corrixe o seguinte código CSS:
```css
div {
  margin: 10px, 20px;
  padding 15px;
}
```
**Solución**:
```css
div {
  margin: 10px 20px;
  padding: 15px;
}
```

---

#### **8. Preguntas teóricas**

**Pregunta 15**: Que é o modelo de caixa en CSS?  
**Solución**: É un concepto que describe como se compón un elemento HTML, incluíndo o contido, recheo, borde e marxe.

---

**Pregunta 16**: Para que serve o atributo `aria-label`?  
**Solución**: Proporciona unha etiqueta descritiva para un elemento, útil para accesibilidade.

---

#### **9. Preguntas prácticas**

**Pregunta 17**: Escribe o código HTML para crear unha táboa con dúas filas e dúas columnas.  
**Solución**:
```html
<table>
  <tr>
    <td>Celda 1</td>
    <td>Celda 2</td>
  </tr>
  <tr>
    <td>Celda 3</td>
    <td>Celda 4</td>
  </tr>
</table>
```

---

**Pregunta 18**: Escribe o código CSS para aplicar un borde de 2 píxeles sólido e cor negra a todos os elementos `<div>`.  
**Solución**:
```css
div {
  border: 2px solid black;
}
```

---

#### **10. Preguntas avanzadas**

**Pregunta 19**: Como se pode usar JavaScript para acceder a un atributo `data-*`?  
**Solución**:
```javascript
const elemento = document.getElementById('idElemento');
console.log(elemento.dataset.nomeAtributo);
```

---

**Pregunta 20**: Que diferenza hai entre `padding` e `margin` en CSS?  
**Solución**: `padding` é o espazo interior ao redor do contido dun elemento, mentres que `margin` é o espazo exterior ao redor do borde dun elemento.

---

#### **11. Preguntas de relación**

**Pregunta 21**: Relaciona cada tipo de CSS co seu exemplo:
1) CSS interno  
2) CSS externo  
3) CSS en liña  

a) `<style> h1 { color: blue; } </style>`  
b) `<link rel="stylesheet" href="estilos.css">`  
c) `<h1 style="color: blue;">Ola Mundo!</h1>`  

**Solución**:  
1) a) CSS interno  
2) b) CSS externo  
3) c) CSS en liña

---

#### **12. Preguntas de completar código**

**Pregunta 22**: Completa o código para crear un botón con texto "Enviar" e un fondo azul.
```html
<button _____="background-color: blue;">_____</button>
```
**Solución**:
```html
<button style="background-color: blue;">Enviar</button>
```

---

#### **13. Preguntas de corrección de código**

**Pregunta 23**: Corrixe o seguinte código HTML:
```html
<ul>
  <li>Item 1<li>
  <li>Item 2<li>
</ul>
```
**Solución**:
```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
```

---

#### **14. Preguntas de selección múltiple**

**Pregunta 24**: Cal dos seguintes atributos se usa para facer un campo de formulario obrigatorio?
a) `required`  
b) `placeholder`  
c) `disabled`  
d) `readonly`  

**Solución**: a) `required`

---

#### **15. Preguntas de verdadeiro/falso**

**Pregunta 25**: A etiqueta `<header>` só se pode usar unha vez por páxina.  
**Solución**: Falso (pódese usar varias veces, por exemplo, en cada sección).

---

#### **16. Preguntas de relación**

**Pregunta 26**: Relaciona cada atributo ARIA co seu propósito:
1) `aria-label`  
2) `aria-hidden`  
3) `aria-expanded`  

a) Indica se un elemento está despregado ou pechado.  
b) Proporciona unha etiqueta descritiva para un elemento.  
c) Oculta un elemento aos lectores de pantalla.  

**Solución**:  

1) b) Proporciona unha etiqueta descritiva para un elemento.  
2) c) Oculta un elemento aos lectores de pantalla.  
3) a) Indica se un elemento está despregado ou pechado.

---

#### **17. Preguntas de completar frase**

**Pregunta 27**: O atributo `_____` en HTML5 permíteche asociar un campo de formulario cunha etiqueta.  
**Solución**: `for`

---

#### **18. Preguntas de corrección de código**

**Pregunta 28**: Corrixe o seguinte código CSS:
```css
h1 {
  font-size = 24px;
  color: blue
}
```
**Solución**:
```css
h1 {
  font-size: 24px;
  color: blue;
}
```

---

#### **19. Preguntas teóricas**

**Pregunta 29**: Que é o modelo de caixa en CSS?  
**Solución**: É un concepto que describe como se compón un elemento HTML, incluíndo o contido, recheo, borde e marxe.

---

#### **20. Preguntas prácticas**

**Pregunta 30**: Escribe o código HTML para crear unha lista ordenada con tres elementos.  
**Solución**:
```html
<ol>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ol>
```

---

### **Resumo**
Estas preguntas abarcan unha ampla variedade de temas e tipos de preguntas para avaliar os coñecementos sobre HTML5, CSS, formularios, semántica, atributos ARIA, e moito máis. Se necesitas máis preguntas ou axuda adicional, avísame! 😊

-----

# Aplicación de autoavaliación

Claro! Vou axudarte a crear unha pequena aplicación de **autoavaliación** usando HTML, CSS e JavaScript. Esta aplicación presentará as preguntas que xeramos anteriormente e permitirá ao usuario responder e verificar as súas respostas. Vou proporcionar un exemplo básico que podes ampliar ou personalizar segundo as túas necesidades.

---

### **Estrutura da aplicación**

1. **HTML**: Estrutura da páxina e preguntas.
2. **CSS**: Estilos para facer a aplicación visualmente atractiva.
3. **JavaScript**: Lóxica para verificar as respostas e mostrar os resultados.

---

### **1. Código HTML**

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Autoavaliación de HTML5 e CSS</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <h1>Autoavaliación de HTML5 e CSS</h1>
    <form id="quiz-form">
      <!-- Pregunta 1 -->
      <div class="question">
        <p>1. Cal das seguintes etiquetas HTML5 é semántica?</p>
        <label><input type="radio" name="q1" value="a"> a) &lt;div&gt;</label>
        <label><input type="radio" name="q1" value="b"> b) &lt;span&gt;</label>
        <label><input type="radio" name="q1" value="c"> c) &lt;article&gt;</label>
        <label><input type="radio" name="q1" value="d"> d) &lt;bold&gt;</label>
      </div>

      <!-- Pregunta 2 -->
      <div class="question">
        <p>2. Cal dos seguintes atributos é válido para a etiqueta &lt;input&gt;?</p>
        <label><input type="radio" name="q2" value="a"> a) type="text"</label>
        <label><input type="radio" name="q2" value="b"> b) type="color"</label>
        <label><input type="radio" name="q2" value="c"> c) type="date"</label>
        <label><input type="radio" name="q2" value="d"> d) Todos os anteriores</label>
      </div>

      <!-- Pregunta 3 -->
      <div class="question">
        <p>3. Cal dos seguintes atributos ARIA se usa para describir o estado dun elemento?</p>
        <label><input type="radio" name="q3" value="a"> a) aria-label</label>
        <label><input type="radio" name="q3" value="b"> b) aria-expanded</label>
        <label><input type="radio" name="q3" value="c"> c) aria-hidden</label>
        <label><input type="radio" name="q3" value="d"> d) aria-describedby</label>
      </div>

      <!-- Botón de envío -->
      <button type="submit">Enviar respostas</button>
    </form>

    <!-- Resultados -->
    <div id="results" class="hidden">
      <h2>Resultados</h2>
      <p id="score"></p>
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
```

---

### **2. Código CSS (styles.css)**

```css
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 600px;
  margin: 50px auto;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  color: #333;
}

.question {
  margin-bottom: 20px;
}

label {
  display: block;
  margin: 5px 0;
}

button {
  display: block;
  width: 100%;
  padding: 10px;
  background-color: #28a745;
  color: white;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: #218838;
}

.hidden {
  display: none;
}

#results {
  margin-top: 20px;
}
```

---

### **3. Código JavaScript (script.js)**

```javascript
document.getElementById('quiz-form').addEventListener('submit', function(event) {
  event.preventDefault(); // Evita o envío do formulario

  // Respostas correctas
  const respostasCorrectas = {
    q1: 'c', // Pregunta 1
    q2: 'd', // Pregunta 2
    q3: 'b', // Pregunta 3
  };

  // Obter respostas do usuario
  const respostasUsuario = {
    q1: document.querySelector('input[name="q1"]:checked')?.value,
    q2: document.querySelector('input[name="q2"]:checked')?.value,
    q3: document.querySelector('input[name="q3"]:checked')?.value,
  };

  // Calcular puntuación
  let puntuacion = 0;
  for (const pregunta in respostasCorrectas) {
    if (respostasUsuario[pregunta] === respostasCorrectas[pregunta]) {
      puntuacion++;
    }
  }

  // Mostrar resultados
  const resultadosDiv = document.getElementById('results');
  resultadosDiv.classList.remove('hidden');
  document.getElementById('score').textContent = `Puntuación: ${puntuacion} de ${Object.keys(respostasCorrectas).length}`;
});
```

---

### **4. Como funciona a aplicación**

1. **Preguntas**: A aplicación presenta 3 preguntas de múltiple selección.
2. **Respostas**: O usuario selecciona as respostas e fai clic en "Enviar respostas".
3. **Verificación**: JavaScript compara as respostas do usuario coas respostas correctas.
4. **Resultados**: A aplicación mostra a puntuación obtida.

---

### **5. Ampliacións posibles**

- **Máis preguntas**: Engade máis preguntas ao formulario.
- **Explicacións**: Mostra explicacións das respostas correctas.
- **Estilos avanzados**: Mellorar o deseño con animacións ou efectos.
- **Almacenamento**: Gardar os resultados no `localStorage` para facer un seguimento do progreso.

---

### **6. Resumo**

Esta aplicación de autoavaliación é unha forma sinxela e efectiva de probar os coñecementos sobre HTML5 e CSS. Podes ampliala e personalizala segundo as túas necesidades. Se tes máis preguntas ou necesitas máis axuda, avísame! 😊

---

# ``localstorage``

O **`localStorage`** é unha característica dos navegadores web que permite almacenar datos de forma persistente no lado do cliente (é dicir, no navegador do usuario). É moi útil para gardar información que debe persistir entre sesións, como preferencias do usuario, datos de formularios, ou estado da aplicación. Vou explicarche como funciona, o seu nivel de persistencia, e os usos máis comúns.

---

### **1. Que é `localStorage`?**

`localStorage` é un obxecto JavaScript que forma parte da API Web Storage. Permite almacenar datos en forma de pares clave-valor no navegador do usuario. Os datos almacenados en `localStorage` non caducan e permanecen aí mesmo despois de pechar o navegador ou reiniciar o dispositivo.

---

### **2. Características principais**

#### **a) Persistencia**
- Os datos almacenados en `localStorage` **non teñen data de caducidade**. Permanecen no navegador ata que se borran explicitamente (por exemplo, mediante código JavaScript ou borrando o cache do navegador).

#### **b) Capacidade**
- A capacidade máxima de `localStorage` é de **5 MB por dominio** na maioría dos navegadores.

#### **c) Acceso**
- Os datos almacenados en `localStorage` só están dispoñibles para o mesmo dominio que os almacenou. Non se poden acceder desde outros dominios por motivos de seguridade.

#### **d) Sincronización**
- `localStorage` non está sincronizado entre diferentes pestañas ou ventás do navegador. Cada pestaña ten o seu propio almacenamento.

---

### **3. Como usar `localStorage`**

#### **a) Almacenar datos**
Usa o método `setItem()` para gardar datos en `localStorage`.

- **Exemplo**:
  ```javascript
  localStorage.setItem('nome', 'Fulano');
  ```

#### **b) Recuperar datos**
Usa o método `getItem()` para recuperar datos almacenados.

- **Exemplo**:
  ```javascript
  const nome = localStorage.getItem('nome');
  console.log(nome); // "Fulano"
  ```

#### **c) Eliminar datos**
Usa o método `removeItem()` para eliminar un elemento específico.

- **Exemplo**:
  ```javascript
  localStorage.removeItem('nome');
  ```

#### **d) Borrar todos os datos**
Usa o método `clear()` para eliminar todos os datos almacenados.

- **Exemplo**:
  ```javascript
  localStorage.clear();
  ```

#### **e) Comprobar se existe un dato**
Podes comprobar se unha clave existe en `localStorage` usando `getItem()`.

- **Exemplo**:
  ```javascript
  if (localStorage.getItem('nome') === null) {
    console.log('O nome non está almacenado.');
  }
  ```

---

### **4. Nivel de persistencia**

- **Persistente**: Os datos almacenados en `localStorage` non caducan e permanecen no navegador ata que se borren explicitamente.
- **Específico do dominio**: Os datos só están dispoñibles para o mesmo dominio que os almacenou.
- **Non compartido**: Non se comparte entre diferentes navegadores ou dispositivos.

---

### **5. Usos comúns de `localStorage`**

#### **a) Gardar preferencias do usuario**
Podes almacenar preferencias como o tema (claro/escuro), idioma, ou configuracións personalizadas.

- **Exemplo**:
  ```javascript
  localStorage.setItem('tema', 'escuro');
  ```

#### **b) Gardar datos de formularios**
Podes gardar datos de formularios temporalmente para que non se perdan se o usuario recarga a páxina.

- **Exemplo**:
  ```javascript
  const formulario = document.getElementById('meuFormulario');
  formulario.addEventListener('input', () => {
    localStorage.setItem('formularioDatos', JSON.stringify({
      nome: formulario.nome.value,
      email: formulario.email.value,
    }));
  });
  ```

#### **c) Gardar o estado da aplicación**
Podes gardar o estado dunha aplicación (como o contido dun carriño da compra ou o progreso dun xogo).

- **Exemplo**:
  ```javascript
  const estado = {
    carrinho: ['produto1', 'produto2'],
    progreso: 50,
  };
  localStorage.setItem('estadoAplicacion', JSON.stringify(estado));
  ```

#### **d) Autenticación e tokens**
Podes almacenar tokens de autenticación ou información de sesión (aínda que é recomendable usar `sessionStorage` para datos sensibles que deben caducar ao pechar o navegador).

- **Exemplo**:
  ```javascript
  localStorage.setItem('token', 'abc123');
  ```

---

### **6. Limitacións e consideracións**

#### **a) Seguridade**
- **Non almacenar datos sensibles**: `localStorage` non é seguro para gardar información sensible como contrasinais ou datos de tarxetas de crédito, xa que os datos non están cifrados.
- **Ataques XSS**: `localStorage` é vulnerable a ataques de cross-site scripting (XSS). Se un atacante pode executar código JavaScript na páxina, pode acceder a `localStorage`.

#### **b) Capacidade**
- A capacidade máxima é de 5 MB por dominio. Se necesitas máis espazo, considera usar **IndexedDB**.

#### **c) Sincronización**
- `localStorage` non está sincronizado entre pestañas ou dispositivos. Se necesitas sincronización, considera usar **bases de datos no servidor** ou **servizos en la nube**.

---

### **7. Exemplo completo**

Aquí tes un exemplo completo dunha aplicación que usa `localStorage` para gardar e recuperar preferencias do usuario:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo localStorage</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 600px;
      margin: 50px auto;
      padding: 20px;
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    label {
      display: block;
      margin: 10px 0;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Preferencias do usuario</h1>
    <form id="preferenciasForm">
      <label for="tema">Tema:</label>
      <select id="tema" name="tema">
        <option value="claro">Claro</option>
        <option value="escuro">Escuro</option>
      </select>

      <label for="idioma">Idioma:</label>
      <select id="idioma" name="idioma">
        <option value="gl">Galego</option>
        <option value="es">Español</option>
        <option value="en">Inglés</option>
      </select>

      <button type="submit">Gardar preferencias</button>
    </form>
  </div>

  <script>
    // Cargar preferencias gardadas
    const tema = localStorage.getItem('tema') || 'claro';
    const idioma = localStorage.getItem('idioma') || 'gl';

    document.getElementById('tema').value = tema;
    document.getElementById('idioma').value = idioma;

    // Gardar preferencias
    document.getElementById('preferenciasForm').addEventListener('submit', function(event) {
      event.preventDefault();

      const tema = document.getElementById('tema').value;
      const idioma = document.getElementById('idioma').value;

      localStorage.setItem('tema', tema);
      localStorage.setItem('idioma', idioma);

      alert('Preferencias gardadas!');
    });
  </script>
</body>
</html>
```

---

### **8. Resumo**
- **`localStorage`**: Almacena datos de forma persistente no navegador.
- **Persistencia**: Os datos non caducan e permanecen ata que se borren explicitamente.
- **Usos**: Gardar preferencias, datos de formularios, estado da aplicación, etc.
- **Limitacións**: Non é seguro para datos sensibles e ten unha capacidade máxima de 5 MB.

---

## IndexedDB

**IndexedDB** é unha base de datos NoSQL do lado do cliente que permite almacenar grandes cantidades de datos estruturados no navegador do usuario. É máis potente que `localStorage` e `sessionStorage`, xa que permite almacenar datos complexos, realizar consultas avanzadas e traballar con grandes volumes de información. Vou explicarche como usar IndexedDB e outras alternativas dispoñibles.

---

### **1. Introdución a IndexedDB**

IndexedDB é unha API de baixo nivel que permite almacenar datos no navegador de forma asíncrona. É ideal para aplicacións web que necesitan almacenar grandes cantidades de datos ou realizar operacións complexas.

#### **Características principais**:
- **Base de datos NoSQL**: Almacena datos en forma de pares clave-valor.
- **Asíncrona**: As operacións realízanse de forma non bloqueante.
- **Transaccións**: Soporta transaccións para garantir a integridade dos datos.
- **Índices**: Permite crear índices para consultas rápidas.
- **Capacidade**: Non ten un límite estrito de tamaño, pero depende do navegador e do almacenamento dispoñible no dispositivo.

---

### **2. Como usar IndexedDB**

#### **a) Abrir ou crear unha base de datos**
Usa o método `indexedDB.open()` para abrir ou crear unha base de datos.

- **Exemplo**:
  ```javascript
  const request = indexedDB.open('miBaseDeDatos', 1);
  
  request.onupgradeneeded = function(event) {
    const db = event.target.result;
    const store = db.createObjectStore('usuarios', { keyPath: 'id' });
    store.createIndex('nome', 'nome', { unique: false });
  };
  
  request.onsuccess = function(event) {
    const db = event.target.result;
    console.log('Base de datos aberta correctamente.');
  };
  
  request.onerror = function(event) {
    console.error('Erro ao abrir a base de datos:', event.target.error);
  };
  ```

#### **b) Engadir datos**
Usa unha transacción para engadir datos a un almacén de obxectos.

- **Exemplo**:
  ```javascript
  const transaction = db.transaction(['usuarios'], 'readwrite');
  const store = transaction.objectStore('usuarios');
  const usuario = { id: 1, nome: 'Fulano', email: 'fulano@exemplo.com' };
  
  const request = store.add(usuario);
  
  request.onsuccess = function() {
    console.log('Usuario engadido correctamente.');
  };
  
  request.onerror = function(event) {
    console.error('Erro ao engadir o usuario:', event.target.error);
  };
  ```

#### **c) Recuperar datos**
Usa unha transacción para recuperar datos dun almacén de obxectos.

- **Exemplo**:
  ```javascript
  const transaction = db.transaction(['usuarios'], 'readonly');
  const store = transaction.objectStore('usuarios');
  const request = store.get(1); // Obtén o usuario co id 1
  
  request.onsuccess = function(event) {
    const usuario = event.target.result;
    console.log('Usuario:', usuario);
  };
  
  request.onerror = function(event) {
    console.error('Erro ao obter o usuario:', event.target.error);
  };
  ```

#### **d) Actualizar datos**
Usa unha transacción para actualizar datos nun almacén de obxectos.

- **Exemplo**:
  ```javascript
  const transaction = db.transaction(['usuarios'], 'readwrite');
  const store = transaction.objectStore('usuarios');
  const usuario = { id: 1, nome: 'Fulano Actualizado', email: 'fulano@exemplo.com' };
  
  const request = store.put(usuario);
  
  request.onsuccess = function() {
    console.log('Usuario actualizado correctamente.');
  };
  
  request.onerror = function(event) {
    console.error('Erro ao actualizar o usuario:', event.target.error);
  };
  ```

#### **e) Eliminar datos**
Usa unha transacción para eliminar datos dun almacén de obxectos.

- **Exemplo**:
  ```javascript
  const transaction = db.transaction(['usuarios'], 'readwrite');
  const store = transaction.objectStore('usuarios');
  const request = store.delete(1); // Elimina o usuario co id 1
  
  request.onsuccess = function() {
    console.log('Usuario eliminado correctamente.');
  };
  
  request.onerror = function(event) {
    console.error('Erro ao eliminar o usuario:', event.target.error);
  };
  ```

---

### **3. Alternativas a IndexedDB**

#### **a) localStorage**
- **Uso**: Almacenamento sinxelo de pares clave-valor.
- **Capacidade**: 5 MB por dominio.
- **Persistencia**: Os datos non caducan.
- **Limitacións**: Non é axeitado para datos complexos ou grandes volumes de información.

#### **b) sessionStorage**
- **Uso**: Similar a `localStorage`, pero os datos só están dispoñibles durante a sesión do navegador.
- **Capacidade**: 5 MB por dominio.
- **Persistencia**: Os datos bórranse ao pechar a pestaña ou o navegador.

#### **c) Cookies**
- **Uso**: Almacenamento de pequenos datos que se envían ao servidor con cada solicitude.
- **Capacidade**: 4 KB por cookie.
- **Persistencia**: Pódense configurar para caducar nunha data específica.

#### **d) Web SQL (obsoleta)**
- **Uso**: Base de datos SQL do lado do cliente.
- **Capacidade**: Depende do navegador.
- **Persistencia**: Os datos non caducan.
- **Limitacións**: Non é un estándar e está obsoleta en favor de IndexedDB.

#### **e) Cache API**
- **Uso**: Almacenamento de recursos (como imaxes, CSS, JS) para aplicacións web progresivas (PWAs).
- **Capacidade**: Depende do navegador.
- **Persistencia**: Os datos persisten ata que se borren explicitamente.

#### **f) Servizos en la nube**
- **Uso**: Almacenamento de datos en servidores remotos (por exemplo, Firebase, AWS, Google Cloud).
- **Capacidade**: Ilimitada (depende do provedor).
- **Persistencia**: Os datos están dispoñibles en calquera dispositivo con conexión a Internet.

---

### **4. Exemplo completo con IndexedDB**

Aquí tes un exemplo completo dunha aplicación que usa IndexedDB para almacenar e recuperar datos:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo IndexedDB</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 600px;
      margin: 50px auto;
      padding: 20px;
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    label {
      display: block;
      margin: 10px 0;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>IndexedDB: Usuarios</h1>
    <form id="usuarioForm">
      <label for="nome">Nome:</label>
      <input type="text" id="nome" name="nome" required>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required>

      <button type="submit">Gardar usuario</button>
    </form>

    <h2>Usuarios gardados</h2>
    <ul id="usuariosList"></ul>
  </div>

  <script>
    let db;

    // Abrir ou crear a base de datos
    const request = indexedDB.open('miBaseDeDatos', 1);

    request.onupgradeneeded = function(event) {
      db = event.target.result;
      const store = db.createObjectStore('usuarios', { keyPath: 'id', autoIncrement: true });
      store.createIndex('nome', 'nome', { unique: false });
    };

    request.onsuccess = function(event) {
      db = event.target.result;
      cargarUsuarios();
    };

    request.onerror = function(event) {
      console.error('Erro ao abrir a base de datos:', event.target.error);
    };

    // Gardar usuario
    document.getElementById('usuarioForm').addEventListener('submit', function(event) {
      event.preventDefault();

      const nome = document.getElementById('nome').value;
      const email = document.getElementById('email').value;

      const transaction = db.transaction(['usuarios'], 'readwrite');
      const store = transaction.objectStore('usuarios');
      const usuario = { nome, email };

      const request = store.add(usuario);

      request.onsuccess = function() {
        console.log('Usuario gardado correctamente.');
        cargarUsuarios();
      };

      request.onerror = function(event) {
        console.error('Erro ao gardar o usuario:', event.target.error);
      };
    });

    // Cargar usuarios
    function cargarUsuarios() {
      const transaction = db.transaction(['usuarios'], 'readonly');
      const store = transaction.objectStore('usuarios');
      const request = store.getAll();

      request.onsuccess = function(event) {
        const usuarios = event.target.result;
        const lista = document.getElementById('usuariosList');
        lista.innerHTML = '';

        usuarios.forEach(usuario => {
          const li = document.createElement('li');
          li.textContent = `${usuario.nome} (${usuario.email})`;
          lista.appendChild(li);
        });
      };

      request.onerror = function(event) {
        console.error('Erro ao cargar os usuarios:', event.target.error);
      };
    }
  </script>
</body>
</html>
```

---

### **5. Resumo**
- **IndexedDB**: Base de datos NoSQL do lado do cliente para almacenar grandes cantidades de datos.
- **Alternativas**: `localStorage`, `sessionStorage`, cookies, Web SQL (obsoleta), Cache API, servizos en la nube.
- **Uso de IndexedDB**: Abrir/crear base de datos, engadir, recuperar, actualizar e eliminar datos.

😊

----

## Formularios

### **Cuestionario sobre Formularios HTML (Nivel Intermedio-Avanzado)**

#### **Sección 1: Verdadeiro/Falso** (🔵 Marca V ou F)

1. ( ) O atributo `novalidate` no formulario desactiva todas as validacións HTML5. | (V)

2. ( ) `<datalist>` pode usarse con `<input type="email">`. | (V)

3. ( ) `minlength="5"` aplica a un `<input type="number">`. | F (Non, minlength aplica a campos de texto, non numéricos)

4. ( ) `<fieldset>` mellora a semántica pero non a accesibilidade. | F (Mellora accesibilidade ao agrupar elementos relacionados)

5. ( ) `aria-describedby` asóciase a IDs de elementos que describen o campo. | (V)

#### **Sección 2: Selección Múltiple** (🔵 Escolle todas as correctas)

6. Que atributos prevén ataques CSRF?

a) `action="/secure"`

b) `<input type="hidden" name="csrf_token">` ✅

c) `enctype="multipart/form-data"`

d) `method="POST"`

7. Que validacións aplica `pattern="^\+34\d{9}$"`?

a) Número español con +34  ✅

b) 9 díxitos tras +34      ✅ 

c) Comeza con 34 sen +

d) 11 díxitos totais       ✅ (Exemplo: +34612345678 → 11 díxitos totais)

8. Cales son boas prácticas para `<label>`?

a) Usar `for` e `id`  ✅

b) Ocultar labels con `display: none`

c) Agrupar con `<fieldset>`  ✅

d) Usar `placeholder` como substituto

#### **Sección 3: Selección Única** (🔵 Escolle a correcta)

9. Que fai `input.setCustomValidity('Erro')`?

a) Mostra un popup

b) Marca o campo como inválido    ✅

c) Envía o formulario

d) Desactiva o botón

10. Para unha barra de progreso de carga, usarías:

a) `<progress>`     ✅

b) `<meter>`

c) `<input type="range">`

d) `<div class="progress">`

11. Cal é o valor por defecto de `enctype`?

a) `text/plain`

b) `application/json`

c) `multipart/form-data`

d) `application/x-www-form-urlencoded`    ✅

#### **Sección 4: Completar** (🔵 Completa o baleiro)

12. O atributo `__________` en `<input>` activa o teclado numérico en móbiles.   (inputmode="numeric")

13. Para validar un NIF español, o patrón Regex sería `__________`.  (`^[0-9]{8}[A-HJ-NP-TV-Z]$`)

14. O elemento HTML que agrupa varios `<option>` é `__________`.    (`<optgroup>`)

#### **Sección 5: Relacionar** (🔵 Une con liñas)

15. Relaciona concepto-definición: 

1 → b), 2 → c), 3 → d), 4 → e)

```

1. aria-live      a) Describir erros

2. Constraint API b) Actualizacións en tempo real

3. DOMPurify      c) Validacións HTML5

4. Honeypot      d) Sanitización

e) Protección anti-spam

```

#### **Sección 6: Definicións** (🔵 Que concepto é?)

16. "Campo invisible para detectar bots":

a) CSRF

b) Honeypot      ✅

c) CAPTCHA

d) `disabled`

17. "Permite seleccionar múltiples opciones nun `<select>`":

a) `selected`

b) `multiple`      ✅

c) `optgroup`

d) `size`

#### **Sección 7: Casos Prácticos** (🔵 Resolve)

18. Crea un `<input>` que:

- Acepte só datas posteriores a 2024

- Sexa obrigatorio

```html
<input type="______" name="data" ______ ______>
```

```
&rarr;  `<input type="date" name="data" min="2024-01-01" required>`

19. Que código JavaScript valida un campo de teléfono español?

```javascript
const telefonoValido = (t) => /________/.test(t);
```

&rarr;  `const telefonoValido = (t) => /^\+34\d{9}$/.test(t);`

20. Diseña unha Regex para contrasinais que:

- Teña 8+ caracteres

- Inclúa maiúscula e número

```
^__________$
```

&rarr;  `^(?=.*[A-Z])(?=.*\d).{8,}$`

#### **Sección 8: Erros Comúns** (🔵 Detecta o erro)

21. Problema (que falta)
```html
<label>Email:</label>
<input type="text" name="email" required>
```

&rarr;  `Falta id no <input> e for na <label>`


22.
```html
<form method="POST">
<input type="text" name="user">
<button type="button">Enviar</button>
</form>
```

&rarr;  `O botón ten type="button", non envía o formulario. Usar type="submit".`

#### **Sección 9: Avanzadas** (🔵 Desenvolve)

23. Como implementarías unha validación asíncrona de dispoñibilidade de email?

    *Usando fetch para consultar un endpoint ao cambiar o campo:*

    ```javascript
    document.getElementById('email').addEventListener('input', async (e) => {
      const resposta = await fetch(`/check-email?email=${e.target.value}`);
      const dispoñible = await resposta.json();
      if (!dispoñible) e.target.setCustomValidity('Email xa en uso');
    });
    ```

24. Que atributos ARIA usarías para un formulario con validación en tempo real?
    ```js
    <div role="alert" aria-live="polite" id="erro-email"></div>
    <input aria-invalid="false" aria-describedby="erro-email">
    ```

---

**Notas:**

- As respostas requiren coñecementos de HTML5, CSS, JS e accesibilidade

- Inclúen temas como validacións, seguridade, ARIA e boas prácticas

- Algúns ítems teñen varias respostas correctas

**Comentarios Adicionais:**

As preguntas cobreiron validacións, seguridade, accesibilidade e boas prácticas.

Algúns ítems (como preguntas 18-20) teñen múltiples solucións válidas.

Recoméndase probar os exemplos en navegadores actuais e validar con ferramentas como Lighthouse.

## 2 FORM


Aquí tes **30 preguntas formativas** sobre formularios HTML, organizadas por tipo e nivel de dificultade:

---

### **Sección 1: Verdadeiro/Falso**  
1. O atributo `required` funciona en `<input type="hidden">`.  
2. `maxlength="5"` permite escribir exactamente 5 caracteres.  
3. O atributo `minlength` aplícase a campos numéricos como `<input type="number">`.  
4. `<fieldset>` só se usa para agrupar campos visualmente, non semánticamente.  
5. `autocomplete="off"` desactiva o almacenamento de datos no navegador.  

---

### **Sección 2: Selección Múltiple**  
6. Que atributos usarías para validar un código postal galego (5 díxitos)?  
   a) `pattern="\d{5}"`  
   b) `pattern="^15\d{3}$"`  
   c) `min="15001" max="15999"`  
   d) `inputmode="numeric"`  

7. Que tipos de validacións HTML5 se aplican a un teléfono móbil español?  
   a) `<input type="tel">`  
   b) `pattern="\+34\d{9}"`  
   c) `maxlength="13"`  
   d) `required`  

8. Cales son boas prácticas para formularios accesibles?  
   a) Usar `<label for="id">`  
   b) Ocultar etiquetas con `display: none`  
   c) `aria-describedby` para mensaxes de erro  
   d) `tabindex="0"` en todos os campos  

---

### **Sección 3: Selección Única**  
9. Que atributo prevén que un campo se envíe?  
   a) `readonly`  
   b) `disabled`  
   c) `hidden`  

10. Para unha barra de progreso que mostra o 75% completado:  
    a) `<progress value="75" max="100">`  
    b) `<meter value="75" min="0" max="100">`  
    c) `<input type="range" value="75">`  

11. Que tipo de entrada usarías para seleccionar unha cor corporativa?  
    a) `<input type="text">`  
    b) `<input type="select">`  
    c) `<input type="color">`  

---

### **Sección 4: Completar**  
12. Completa o atributo para forzar o teclado numérico en móbiles:  
    `<input type="tel" __________="numeric">`  

13. Expresión regular para validar DNI español:  
    `pattern="__________"`  

14. Etiqueta para agrupar opcións nun `<select>`:  
    `<__________ label="Categoría">`  

---

### **Sección 5: Relacionar**  
15. Relaciona cada concepto coa súa definición:  
    - 1) `novalidate`  
    - 2) `formaction`  
    - 3) `datalist`  
    - 4) `optgroup`  
    a) Lista de opcións predefinidas  
    b) Desactiva validación HTML5  
    c) Agrupa opcións nun select  
    d) URL alternativa para envío  
    
      b, d, a, c

---

### **Sección 6: Definicións**  
16. Que é un **honeypot**?  
    a) Un tipo de validación con JavaScript  
    b) Campo oculto para detectar bots  
    c) Unha técnica de cifrado  

17. Que fai `aria-live="polite"`?  
    a) Anuncia cambios aos lectores de pantalla  
    b) Oculta contido visualmente  
    c) Desactiva navegación por teclado  

---

### **Sección 7: Casos Prácticos**  
18. Corrixe o erro neste formulario:  
    ```html
    <label>Nome:</label>
    <input type="text" name="nome">
    ```

19. Escribe unha función JavaScript que valide que un teléfono español comeza por +34.  

20. Crear unha expresión regular que permita contrasinais con:  
    - Mínimo 8 caracteres  
    - 1 letra maiúscula  
    - 1 número  

---

### **Sección 8: Erros Comúns**  
21. Por que non funciona este código?  
    ```html
    <input type="text" id="usuario">
    <label for="usuario">Usuario:</label>
    ```

22. Que ocorre ao enviar este formulario?  
    ```html
    <form method="post">
      <input type="text" name="email">
      <button type="button">Enviar</button>
    </form>
    ```

---

### **Sección 9: Avanzadas**  
23. Como implementarías unha validación asíncrona de email (comprobando se xa existe)?  

24. Que atributos ARIA usarías para unha mensaxe de erro dinámica?  

---

**Clave de Respostas e Explicacións** 

Aquí están as **respostas detalladas e explicacións formativas**:

---

### **Sección 1: Verdadeiro/Falso**  
1. **Falso**: `<input type="hidden">` non é afectado por `required`, xa que non é interactivo.  
2. **Falso**: `maxlength="5"` permite *ata* 5 caracteres, non exactamente 5.  
3. **Falso**: `minlength` aplica a campos de texto (`text`, `email`, etc.), non numéricos.  
4. **Falso**: `<fieldset>` ten valor semántico para agrupar campos relacionados (mejora accesibilidade).  
5. **Verdadeiro**: `autocomplete="off"` desactiva suxestións do navegador, pero non sempre é respectado.  

---

### **Sección 2: Selección Múltiple**  
6. **b) e d)**:  
   - `pattern="^15\d{3}$"` (códigos galegos comezan con 15)  
   - `inputmode="numeric"` para teclado numérico en móbiles.  
   - ❌ `min/max` non funcionan en campos de texto.  

7. **a, b, c)**:  
   - `type="tel"` optimiza para móbiles.  
   - `pattern="\+34\d{9}"` valida formato +34 seguido de 9 díxitos.  
   - `maxlength="13"` limita a +34 máis 9 díxitos.  

8. **a) e c)**:  
   - `<label for="id">` é esencial para accesibilidade.  
   - `aria-describedby` vincula mensaxes de erro.  
   - ❌ `tabindex="0"` pode romper a orde natural de navegación.  

---

### **Sección 3: Selección Única**  
9. **b) `disabled`**: Os campos desactivados non se envían.  
10. **a) `<progress value="75" max="100">`**: Usase para progreso acumulativo.  
11. **c) `<input type="color">`**: Selector de cor nativo.  

---

### **Sección 4: Completar**  
12. **`inputmode="numeric"`**: Forza teclado numérico en dispositivos móbiles.  
13. **`^[0-9]{8}[A-HJ-NP-TV-Z]$`**: 8 díxitos + letra de control (exclúe I, O, U, etc.).  
14. **`<optgroup>`**: Agrupa opcións en `<select>` (ex: `<optgroup label="Cidades">`).  

---

### **Sección 5: Relacionar**  
15. **1-b, 2-d, 3-a, 4-c**:  
   - `novalidate` → Desactiva validación HTML5.  
   - `formaction` → URL alternativa de envío.  
   - `datalist` → Lista de opcións predefinidas.  
   - `optgroup` → Agrupa opcións en `<select>`.  

---

### **Sección 6: Definicións**  
16. **b)**: Un **honeypot** é un campo oculto para detectar bots (os bots adoitan cubrilos).  
17. **a)**: `aria-live="polite"` anuncia cambios aos lectores de pantalla sen interromper.  

---

### **Sección 7: Casos Prácticos**  
18. **Falta `id` no input e `for` na label**:  
   ```html
   <label for="nome">Nome:</label>
   <input type="text" id="nome" name="nome">
   ```
   - Sen `for` e `id`, a label non se asocia ao campo.  

19. **Función de validación de teléfono**:  
   ```javascript
   const validarTelefono = (telefono) => /^\+34\d{9}$/.test(telefono);
   ```
   - Exemplo válido: `+34612345678`.  

20. **Regex para contrasinal seguro**:  
   ```regex
   ^(?=.*[A-Z])(?=.*\d).{8,}$
   ```
   - `(?=.*[A-Z])`: Polo menos 1 maiúscula.  
   - `(?=.*\d)`: Polo menos 1 número.  
   - `.{8,}`: Mínimo 8 caracteres.  

---

### **Sección 8: Erros Comúns**  
21. **Orde incorrecta**: O `<label>` debe referenciar o `id` do `<input>`.  
22. **O botón non envía**: `type="button"` non envía o formulario. Cambiar a `type="submit"`.  

---

### **Sección 9: Avanzadas**  
23. **Validación asíncrona de email**:  
   ```javascript
   document.getElementById('email').addEventListener('blur', async () => {
     const resposta = await fetch(`/dispoñibilidade?email=${email.value}`);
     if (!resposta.ok) {
       campo.setCustomValidity('Email xa en uso');
     }
   });
   ```
   - Usar `setCustomValidity` para mensaxes personalizadas.  

24. **ARIA para erros dinámicos**:  
   ```html
   <div role="alert" aria-live="assertive" id="erro-email"></div>
   ```
   - `role="alert"` identifica como mensaxe importante.  
   - `aria-live="assertive"` actualiza inmediatamente a usuarios de lectores de pantalla.  

---

### **Conclusión Educativa**  
- **Validacións**: Combinar HTML5 (client-side) con validacións no servidor (obrigatorio para seguridade).  
- **Accesibilidade**: `<label>`, `aria-*`, e semántica correcta son claves para usuarios con discapacidade.  
- **Seguridade**: CSRF tokens e honeypots prevén ataques comúns.  
- **UX**: Mensaxes claras e retroalimentación inmediata melloran a experiencia.  

¿Necesitas máis profundidade en algún tema? 😊


😊  
**Dificultade:** Media-Alta | **Temas Cubertos:** Validacións, Accesibilidade, Seguridade, UX.


### 📚 **Temas Adicionais para Explorar**

1. **Integración con APIs de Autenticación**:  
   - Como usar OAuth2 ou JWT en formularios de login.  
   - Exemplo: Conectar un formulario de rexistro a Firebase ou Auth0.

2. **Formularios Dinámicos con JavaScript**:  
   - Engadir/eliminar campos dinamicamente (ex: listas de elementos).  
   - Uso de `data-*` para personalizar comportamentos.

3. **Validacións Cruzadas entre Campos**:  
   - Exemplo: Confirmación de contrasinal ou validación de rango de datas.

4. **Subida de Arquivos Segura**:  
   - Validación de tipos MIME, tamaño máximo, e scan de malware.  
   - Uso de `FileReader` para previsualizacións.

5. **Formularios Multi-Idioma**:  
   - Como xestionar etiquetas e mensaxes en varios idiomas.  
   - Uso de `lang` e bibliotecas de i18n.

6. **Accesibilidade Avanzada**:  
   - Uso de `aria-invalid` e `aria-errormessage`.  
   - Navegación por teclado en formularios complexos.

7. **Optimización para SEO**:  
   - Estrutura semántica de formularios e impacto no SEO.  
   - Metadatos relevantes para formularios de contacto.

---

### 💡 **Preguntas Reflexivas (Exercicios Prácticos)**

1. **Deseño Responsivo**:  
   - Como adaptar un formulario con 10 campos a unha pantalla de móbil mantendo a usabilidade?

2. **Validacións Complexas**:  
   - ¿Como validar que unha data de nacemento é maior de 18 anos usando `input[type="date"]`?

3. **Seguridade**:  
   - ¿Que pasos seguirías para previr ataques de inxección SQL nun formulario de contacto?

4. **UX/UI**:  
   - ¿Como implementarías unha barra de progreso en tempo real para un contrasinal que require 1 maiúscula, 1 número e 8 caracteres?

5. **Integración con Backend**:  
   - ¿Como manejarías un erro 500 do servidor despois de enviar un formulario?

---

### 🛠️ **Ferramentas Recomendadas**

1. **Validación de Accesibilidade**:  
   - [axe DevTools](https://www.deque.com/axe/devtools/)  
   - [WAVE Evaluation Tool](https://wave.webaim.org/)

2. **Testeo de Formularios**:  
   - [Cypress](https://www.cypress.io/) para probas E2E.  
   - [Jest](https://jestjs.io/) para validacións en JavaScript.

3. **Deseño Responsivo**:  
   - [Chrome DevTools Device Mode](https://developer.chrome.com/docs/devtools/device-mode/).

---

### 📝 **Exercicio Final (Integral)**

**Desafío**: Crea un formulario de rexistro que inclúa:  

- Validacións frontend (HTML5 + JS).  
- Accesibilidade completa (ARIA, navegación por teclado).  
- Subida de avatar (imaxe, máx. 2MB).  
- Confirmación de contrasinal con retroalimentación visual.  
- Conexión a un mock API usando `fetch`.  
- Mensaxes de éxito/erro estilizadas.

**Bonus**:  

- Implementa un CAPTCHA funcional.  
- 

----

----

Aquí tes unha selección de preguntas sobre **táboas** e **formularios HTML**, deseñadas para avaliar o coñecemento teórico e práctico dos teus alumnos. Inclúen solucións detalladas:

---

### **Táboas HTML**
1. **Pregunta**:  
   *Crea unha táboa HTML con 2 filas e 3 columnas, onde a primeira fila sexa de cabeceiras (`<th>`) e a segunda de datos (`<td>`). Inclúe un texto de exemplo.*  
   **Solución**:  
   ```html
   <table border="1">
     <tr>
       <th>Nome</th>
       <th>Idade</th>
       <th>Cidade</th>
     </tr>
     <tr>
       <td>Ana</td>
       <td>25</td>
       <td>Vigo</td>
     </tr>
   </table>
   ```

2. **Pregunta**:  
   *¿Para que serve o atributo `colspan`? Proporciona un exemplo práctico.*  
   **Solución**:  
   ```html
   <table border="1">
     <tr>
       <th colspan="2">Información Persoal</th>
     </tr>
     <tr>
       <td>Nome</td>
       <td>Ana</td>
     </tr>
   </table>
   ```
   **Explicación**: `colspan="2"` fai que a cela ocupe 2 columnas.

3. **Pregunta**:  
   *¿Como se estructura semanticamente unha táboa usando `<thead>`, `<tbody>` e `<tfoot>`?*  
   **Solución**:  
   ```html
   <table border="1">
     <thead>
       <tr>
         <th>Produto</th>
         <th>Prezo</th>
       </tr>
     </thead>
     <tbody>
       <tr>
         <td>Libro</td>
         <td>20€</td>
       </tr>
     </tbody>
     <tfoot>
       <tr>
         <td>Total</td>
         <td>20€</td>
       </tr>
     </tfoot>
   </table>
   ```

4. **Pregunta**:  
   *¿Que diferenza hai entre `<th>` e `<td>`?*  
   **Solución**:  
   - `<th>`: Define **cabeceiras** de columnas/filas (texto en negrita e centrado por defecto).  
   - `<td>`: Define **celas de datos** normais.  

5. **Pregunta**:  
   *¿Como engadir unha descrición a unha táboa para mellorar a accesibilidade?*  
   **Solución**:  
   Usar `<caption>`:  
   ```html
   <table>
     <caption>Lista de alumnos</caption>
     <!-- ... -->
   </table>
   ```

---

### **Formularios HTML**
1. **Pregunta**:  
   *Crea un formulario con un campo de texto para o nome, un para o contrasinal (que non se mostre o texto) e un botón de envío.*  
   **Solución**:  
   ```html
   <form>
     <label>Nome: <input type="text" name="nome"></label><br>
     <label>Contrasinal: <input type="password" name="password"></label><br>
     <button type="submit">Enviar</button>
   </form>
   ```

2. **Pregunta**:  
   *¿Como crear unha lista desplegable (`<select>`) con 3 opcións, onde a segunda esteña desactivada?*  
   **Solución**:  
   ```html
   <select name="cidades">
     <option value="vigo">Vigo</option>
     <option value="coruña" disabled>A Coruña</option>
     <option value="ourense">Ourense</option>
   </select>
   ```

3. **Pregunta**:  
   *¿Que diferencia hai entre `placeholder` e `value` nun campo de texto?*  
   **Solución**:  
   - `placeholder`: Texto temporal que **desaparece** ao escribir no campo.  
   - `value`: Valor **predeterminado** do campo (persiste ao enviar o formulario).  

4. **Pregunta**:  
   *¿Como agrupar opcións nun `<select>` usando `<optgroup>`? Proporciona un exemplo.*  
   **Solución**:  
   ```html
   <select name="frutas">
     <optgroup label="Cítricos">
       <option>Laranxa</option>
       <option>Limón</option>
     </optgroup>
     <optgroup label="Tropicais">
       <option>Plátano</option>
     </optgroup>
   </select>
   ```

5. **Pregunta**:  
   *¿Para que serve o atributo `formaction` nun botón de tipo `submit`?*  
   **Solución**:  
   Permite enviar o formulario a unha **URL diferente** da definida no atributo `action` do `<form>`.  
   Exemplo:  
   ```html
   <form action="/predeterminado">
     <button type="submit" formaction="/alternativo">Enviar a URL alternativa</button>
   </form>
   ```

---

### **Preguntas Avanzadas**
1. **Pregunta**:  
   *¿Como validar un campo de correo electrónico usando só HTML5?*  
   **Solución**:  
   
   ```html
   <input type="email" name="email" required>
   ```
   
2. **Pregunta**:  
   *¿Que é o elemento `<datalist>` e como se vincula a un `<input>`?*  
   **Solución**:  
   ```html
   <input list="cidades">
   <datalist id="cidades">
     <option value="Vigo">
     <option value="Ourense">
   </datalist>
   ```

3. **Pregunta**:  
   *¿Como agrupar campos relacionados nun formulario usando `<fieldset>` e `<legend>`?*  
   **Solución**:  
   ```html
   <fieldset>
     <legend>Información Persoal</legend>
     <input type="text" name="nome">
   </fieldset>
   ```

---

### **Obxectivo das Preguntas**  
- **Teoría**: Comprobar coñecementos de etiquetas, atributos e boas prácticas.  
- **Práctica**: Avaliar a capacidade de escribir código funcional e semántico.  
- **Avanzadas**: Profundizar en características de HTML5 (validacións, elementos semánticos, etc.).  

Se necesitas máis preguntas ou adaptacións, avísame! 😊

---

---

---

Vou deseñar preguntas de tipo test variadas para avaliar o coñecemento de táboas e formularios HTML. Inclúen **solucións destacadas** ao final de cada bloque:

---

### **1. Verdadeiro/Falso**  
1. **O elemento `<td>` úsase para definir cabeceiras de columnas.**  
   - **☐ Verdadeiro**  
   - **☒ Falso** (Solución: `<td>` é para datos normais, `<th>` para cabeceiras).  

2. **O atributo `required` nun campo de entrada forza ao usuario a cubrilo antes de enviar o formulario.**  
   - **☒ Verdadeiro**  
   - **☐ Falso** (Solución: É verdadeiro, pero só se o formulario non ten `novalidate`).  

3. **`<optgroup>` permite agrupar opcións dentro dun `<select>`.**  
   - **☒ Verdadeiro**  
   - **☐ Falso**.

---

### **2. Selección única (escolla a correcta)**  
1. **¿Cal é o atributo que desactiva as validacións HTML5 nun formulario?**  
   - a) `disable-validation`  
   - b) `novalidation`  
   - c) **☑ `novalidate`**  
   - d) `skip-validate`  

2. **¿Que elemento se usa para crear unha lista de suxestións predefinidas vinculada a un `<input>`?**  
   - a) `<select>`  
   - b) **☑ `<datalist>`**  
   - c) `<option>`  
   - d) `<list>`  

3. **¿Cal é a etiqueta correcta para unha cela de cabeceira nunha táboa?**  
   - a) **☑ `<th>`**  
   - b) `<td>`  
   - c) `<header>`  
   - d) `<thead>`  

---

### **3. Selección múltiple (escolla todas as correctas)**  
1. **¿Que elementos se usan para estruturar semanticamente unha táboa?**  
   - ☑ `<thead>`  
   - ☑ `<tbody>`  
   - ☑ `<tfoot>`  
   - ☐ `<tr>`  

2. **¿Cales destes atributos se poden usar nun `<input>` para validacións?**  
   - ☑ `required`  
   - ☑ `pattern`  
   - ☑ `type="email"`  
   - ☐ `novalidate`  

---

### **4. Relacionar conceptos**  
**Relaciona cada elemento coa súa función:**  

- 1) `<fieldset>`  
- 2) `colspan`  
- 3) `<caption>`  
- 4) `formaction`  

a) Especifica unha URL alternativa de envío.  
b) Agrupa campos nun formulario.  
c) Une múltiples columnas nunha cela.  
d) Engade unha descrición á táboa.  

**Solución:**  
1 → a, 2 → c, 3 → d, 4 → b.
1) `<fieldset>` → b) Agrupa campos nun formulario.

2) colspan → c) Une múltiples columnas nunha cela.

3) `<caption>` → d) Engade unha descrición á táboa.

4) formaction → a) Especifica unha URL alternativa de envío.

---

### **5. Completar frases clave**  
1. **O atributo `________` permite que un botón de envío ignore a URL do `<form>` e use outra.**  
   - **Solución:** `formaction`.  

2. **Para que un campo de texto mostre un texto temporal que desaparece ao escribir, úsase o atributo `________`.**  
   - **Solución:** `placeholder`.  

3. **A etiqueta `<________>` úsase para definir un grupo lóxico de opcións dentro dun `<select>`.**  
   - **Solución:** `optgroup`.

---

### **6. Completar código**  
1. **Completa o código para crear unha táboa con 2 filas e 2 columnas (primeira fila como cabeceiras):**  
   ```html  
   <table>
     <tr>
       <th>Nome</th>
       <th>Idade</th>
     </tr>
     <tr>
       <td>Ana</td>
       <td>25</td>
     </tr>
   </table>
   ```

2. **Completa o formulario cun campo obrigatorio de tipo email:**  
   ```html  
   <form>
     <input type="email" name="email" required>
     <button type="submit">Enviar</button>
   </form>
   ```

---

### **Solucións destacadas**  
- **Verdadeiro/Falso**: 1-F, 2-V, 3-V.  
- **Selección única**: 1-c, 2-b, 3-a.  
- **Relacionar**: 1-a, 2-c, 3-d, 4-b.  
- **Completar frases**: `formaction`, `placeholder`, `optgroup`.

---

**Nota:** Estas preguntas poden adaptarse en dificultade ou combinarse con imaxes (ex: mostrar un código e preguntar que fai). Se necesitas máis ou enfoques específicos, dime! 😊

---

---

---

Aquí tes unha pregunta de **relacionar conceptos e definicións** sobre táboas HTML, ideal para avaliar o coñecemento dos teus alumnos:

------

### **Pregunta de relación**

**Relaciona cada elemento/atributo coa súa definición ou función:**

- **1) `<tr>`**
- **2) `<th>`**
- **3) `<td>`**
- **4) `<thead>`**
- **5) `<tbody>`**
- **6) `<tfoot>`**
- **7) `<caption>`**
- **8) `colspan`**
- **9) `rowspan`**

**Definicións:**
a) Define unha fila na táboa.
b) Representa unha cela de cabeceira (texto en negrita e centrado).
c) Representa unha cela de datos normal.
d) Especifica un grupo de cabeceiras na táboa.
e) Indica o corpo principal da táboa.
f) Agrupa filas para o pé da táboa.
g) Proporciona un título ou descrición da táboa.
h) Amplía unha cela en dúas ou máis columnas.
i) Amplía unha cela en dúas ou máis filas.

---

Vou mesturar as opcións para que non esteñan ordenadas e engadir máis desafío. Aquí tes a pregunta **desordenada**:

---

### **Pregunta de relación (non ordenada)**  
**Relaciona cada concepto coa súa definición ou función:**  

**Conceptos:**  
- A) `<td>`  
- B) `<th>`  
- C) `<caption>`  
- D) `rowspan`  
- E) `<tfoot>`  
- F) `<tbody>`  
- G) `colspan`  
- H) `<thead>`  
- I) `<tr>`  

**Definicións:**  
1. Define unha cela de datos normal.  
2. Especifica o pé da táboa (resumo ou total).  
3. Indica o corpo principal de datos da táboa.  
4. Amplía unha cela en múltiples filas.  
5. Define unha fila dentro da táboa.  
6. Engade un título descriptivo á táboa.  
7. Amplía unha cela en múltiples columnas.  
8. Define unha cela de cabeceira (texto destacado).  
9. Agrupa as cabeceiras da táboa.  

---

### **Solución correcta (non ordenada)**

- **A) `<td>`** → **1. Define unha cela de datos normal.**  
- **B) `<th>`** → **8. Define unha cela de cabeceira (texto destacado).**  
- **C) `<caption>`** → **6. Engade un título descriptivo á táboa.**  
- **D) `rowspan`** → **4. Amplía unha cela en múltiples filas.**  
- **E) `<tfoot>`** → **2. Especifica o pé da táboa (resumo ou total).**  
- **F) `<tbody>`** → **3. Indica o corpo principal de datos da táboa.**  
- **G) `colspan`** → **7. Amplía unha cela en múltiples columnas.**  
- **H) `<thead>`** → **9. Agrupa as cabeceiras da táboa.**  
- **I) `<tr>`** → **5. Define unha fila dentro da táboa.**  

---

1c, 2e, 3a, 4b,  5d





### **Dificultade extra (opcional)**

- **Engade elementos distractores**: Incluír opcións falsas como `<div>` ou `border` nas definicións.  
- **Solicitar exemplos de código**: Pedir que escriban unha táboa usando os elementos relacionados.  
- **Preguntas adicionais**: "¿Por que é importante usar `<thead>` e `<tbody>`?" (Solución: Por semántica e accesibilidade).  

**Exemplo de táboa para referencia:**  
```html  
<table>  
  <caption>Alumnos de 1º DAW</caption>  
  <thead>  
    <tr>  
      <th>Nome</th>  
      <th>Nota</th>  
    </tr>  
  </thead>  
  <tbody>  
    <tr>  
      <td>Ana</td>  
      <td>8.5</td>  
    </tr>  
  </tbody>  
  <tfoot>  
    <tr>  
      <td>Media</td>  
      <td>8.5</td>  
    </tr>  
  </tfoot>  
</table>  
```

Se necesitas máis variacións ou enfoques, avísame! 😊

**Resposta:** **Si, aplicase o mesmo principio de flexibilidade semántica**. Vexámolo con detalle:

---

### **1. Etiqueta `<header>`**  
**Verdadeiro ou falso:** *`<header>` só se usa na parte superior da páxina*.  
**Resposta:** **Falso**.  

#### **Explicación:**  
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

### **2. Etiqueta `<aside>`**  
**Verdadeiro ou falso:** *`<aside>` só se usa para barras laterais*.  
**Resposta:** **Falso**.  

#### **Explicación:**  
- **Uso principal**: Contido relacionado **indirectamente** co contido principal (ex: barras laterais, glosarios, publicidade relevante).  
- **Pode usarse en**:  
  - **Calquera sección**: Dentro de `<article>`, `<section>`, ou incluso no `<body>`.  
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
- **Semántica > Posición**: En HTML5, estas etiquetas (**`<header>`, `<footer>`, `<aside>`**) **non están limitadas a unha posición fixa**. O seu uso depende do **contexto semántico** do contido.  
- **Accesibilidade e SEO**: Usalas correctamente mellora a interpretación por lectores de pantalla e motores de busca 🚀.  

**Importante**: Evita usar estas etiquetas só por estética; prioriza o seu significado estrutural. 😊