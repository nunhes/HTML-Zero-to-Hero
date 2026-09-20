# HTML semántico

O **HTML semántico** é unha práctica esencial no desenvolvemento web que consiste en usar etiquetas HTML que describan correctamente o significado e a estrutura do contido. Isto non só mellora a accesibilidade e a SEO (optimización para motores de busca), senón que tamén fai o código máis lexible e mantible. Vou explicarche o seu cometido, as etiquetas que favorecen o marcado semántico, recomendacións de uso e como mellorar o marcado semántico cando non hai etiquetas axeitadas. Tamén falaremos da influencia de CSS no marcado semántico.


### **1. Cometido do HTML semántico**

#### **a) Accesibilidade**
As etiquetas semánticas axudan aos lectores de pantalla e outras ferramentas de accesibilidade a entender mellor a estrutura e o contido dunha páxina web.

#### **b) SEO**
Os motores de busca usan as etiquetas semánticas para indexar e clasificar o contido dunha páxina de forma máis eficiente.

#### **c) Mantibilidade**
O código semántico é máis fácil de entender e manter, xa que a estrutura e o significado do contido están claramente definidos.

#### **d) Compatibilidade**
O HTML semántico é compatible con todos os navegadores modernos e dispositivos.

### **2. Etiquetas que favorecen o marcado semántico**

HTML5 introduciu varias etiquetas semánticas para describir mellor a estrutura dunha páxina web. Aquí tes as máis importantes:

#### **a) Etiquetas estruturais**
- **`<header>`**: Define a cabeceira dunha páxina ou sección.
- **`<footer>`**: Define o pé dunha páxina ou sección.
- **`<main>`**: Define o contido principal dunha páxina.
- **`<section>`**: Define unha sección temática do contido.
- **`<article>`**: Define un contido independente (como un artigo ou entrada de blog).
- **`<aside>`**: Define contido relacionado pero secundario (como unha barra lateral).
- **`<nav>`**: Define unha sección de navegación (como un menú).

#### **b) Etiquetas de texto**
- **`<h1>` a `<h6>`**: Cabeceiras ou títulos.
- **`<p>`**: Define un parágrafo.
- **`<blockquote>`**: Define unha cita longa.
- **`<q>`**: Define unha cita curta.
- **`<cite>`**: Define o título dunha obra ou referencia.
- **`<time>`**: Define unha data ou hora.

#### **c) Etiquetas multimedia**
- **`<figure>`**: Define contido multimedia (como imaxes, vídeos, gráficos).
- **`<figcaption>`**: Define unha descrición para o contido de `<figure>`.

#### **d) Etiquetas de formulario**
- **`<form>`**: Define un formulario.
- **`<label>`**: Asocia unha etiqueta a un campo de formulario.
- **`<fieldset>`**: Agrupa elementos relacionados nun formulario.
- **`<legend>`**: Define un título para un `<fieldset>`.

---

### **3. Recomendacións de emprego**

#### **a) Usa as etiquetas axeitadas**
- Usa `<header>` para a cabeceira, `<footer>` para o pé, `<main>` para o contido principal, etc.
- Evita usar `<div>` para todo. En vez diso, usa etiquetas semánticas como `<section>`, `<article>`, `<aside>`, etc.

#### **b) Xerarquía de cabeceiras**
- Usa `<h1>` para o título principal e `<h2>` a `<h6>` para subtítulos, mantendo unha xerarquía lóxica.

#### **c) Accesibilidade**
- Usa atributos como `alt` en imaxes e `aria-*` para mellorar a accesibilidade.
- Asocia `<label>` con campos de formulario usando o atributo `for`.

#### **d) Contido independente**
- Usa `<article>` para contido que pode ser distribuído independentemente (como artigos, entradas de blog, etc.).

#### **e) Contido relacionado**
- Usa `<aside>` para contido relacionado pero secundario (como barras laterais, ligazóns relacionadas, etc.).

### **4. Como mellorar o marcado semántico na ausencia de etiquetas axeitadas**

Ás veces, non hai unha etiqueta semántica específica para un tipo de contido. Neses casos, podes mellorar o marcado semántico das seguintes formas:

#### **a) Usa `<div>` con atributos ARIA**
Os atributos ARIA (Accessible Rich Internet Applications) poden engadir semántica adicional a elementos non semánticos como `<div>`.

- **Exemplo**:
  ```html
  <div role="navigation" aria-label="Menú principal">
    <ul>
      <li><a href="#">Inicio</a></li>
      <li><a href="#">Sobre</a></li>
    </ul>
  </div>
  ```

#### **b) Usa clases semánticas**
Podes usar clases CSS con nomes semánticos para describir o propósito dun elemento.

- **Exemplo**:
  ```html
  <div class="card">
    <h2 class="card-title">Título da tarxeta</h2>
    <p class="card-content">Contido da tarxeta.</p>
  </div>
  ```

#### **c) Usa microdatos ou JSON-LD**
Os microdatos e JSON-LD son formas de engadir semántica adicional ao teu contido para mellorar a SEO e a accesibilidade.

- **Exemplo con microdatos**:
  ```html
  <div itemscope itemtype="http://schema.org/Person">
    <span itemprop="name">Fulano de Tal</span>
    <span itemprop="jobTitle">Desenvolvedor web</span>
  </div>
  ```

---

### **5. Influencia de CSS no marcado semántico**

O CSS non ten influencia directa no marcado semántico, xa que a semántica está definida polo HTML. Non obstante, o CSS pode axudar a reforzar a semántica visualmente:

#### **a) Estilos semánticos**
- Usa estilos CSS que reflictan a estrutura semántica do contido. Por exemplo, aplica estilos diferentes a `<header>`, `<footer>`, `<section>`, etc.

#### **b) Accesibilidade visual**
- Asegúrate de que os estilos CSS non dificulten a accesibilidade. Por exemplo, non uses cores que dificulten a lectura para persoas con daltonismo.

#### **c) Responsividade**
- Usa CSS para asegurarte de que o contido semántico se amose correctamente en todos os dispositivos.

---
- **Exemplo**:
  ```html
  <div data-id="123" data-user="fulano" data-role="admin"></div>
  ```

#### **b) Acceso desde JavaScript**
Podes acceder aos atributos `data-*` usando a propiedade `dataset` en JavaScript.

- **Exemplo**:
  ```html
  <div id="user" data-id="123" data-user="fulano" data-role="admin"></div>
  
  <script>
    const userDiv = document.getElementById('user');
    console.log(userDiv.dataset.id);    // "123"
    console.log(userDiv.dataset.user);  // "fulano"
    console.log(userDiv.dataset.role);  // "admin"
  </script>
  ```

#### **c) Uso con CSS**
Podes usar os atributos `data-*` como selectores en CSS para aplicar estilos específicos.

- **Exemplo**:
  ```html
  <div data-status="active">Usuario activo</div>
  <div data-status="inactive">Usuario inactivo</div>
  
  <style>
    div[data-status="active"] {
      color: green;
    }
    div[data-status="inactive"] {
      color: red;
    }
  </style>
---

### **6. Exemplo completo de HTML semántico**

Aquí tes un exemplo completo dunha páxina web con marcado semántico:

<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo ARIA</title>
</head>
<body>
  <nav aria-label="Menú principal">
    <ul>
      <li><a href="#">Inicio</a></li>
      <li><a href="#">Sobre</a></li>
      <li><a href="#">Contacto</a></li>
    </ul>
  </nav>

  <button aria-expanded="false" aria-controls="menu">
    Menú
  </button>
  <ul id="menu" aria-hidden="true">
    <li><a href="#">Inicio</a></li>
    <li><a href="#">Sobre</a></li>
  </ul>

  <div role="alert" aria-live="assertive">
    Erro: O campo é obrigatorio.
  </div>

  <div role="tablist">
    <button role="tab" aria-selected="true" aria-controls="pestana1">
      Pestana 1
    </button>
    <button role="tab" aria-selected="false" aria-controls="pestana2">
      Pestana 2
    </button>
  </div>
  <div role="tabpanel" id="pestana1">
    Contido da pestana 1.
  </div>
  <div role="tabpanel" id="pestana2" aria-hidden="true">
    Contido da pestana 2.
  </div>
</body>
</html>
```

Aquí, `data-id`, `data-user` e `data-role` son atributos personalizados.

---

### **2. Cometido do atributo `data-*`**

O principal cometido dos atributos `data-*` é almacenar información adicional nun elemento HTML que non é relevante para a presentación visual, pero que pode ser útil para JavaScript, CSS ou outras tecnoloxías.

#### **Usos comúns**:
- **Almacenar datos**: Gardar información específica dun elemento, como IDs, configuracións ou metadatos.
- **Comunicación entre HTML e JavaScript**: Facilitar o acceso a datos desde JavaScript sen necesidade de usar variables globais ou estruturas de datos complexas.
- **Personalización con CSS**: Usar os datos almacenados para aplicar estilos específicos mediante CSS.

---

### **3. Como se usa o atributo `data-*`?**

#### **a) Definición no HTML**
Podes engadir atributos `data-*` a calquera elemento HTML.

```html
<div id="usuario" data-id="123" data-user="fulano" data-role="admin">
  Contido do usuario
</div>
```

#### **b) Acceso desde JavaScript**
Podes acceder aos atributos `data-*` desde JavaScript usando a propiedade `dataset`.

```javascript
const usuario = document.getElementById('usuario');
const id = usuario.dataset.id;       // "123"
const nome = usuario.dataset.user;   // "fulano"
const rol = usuario.dataset.role;    // "admin"
```

#### **c) Uso con CSS**
Podes usar os atributos `data-*` para aplicar estilos específicos mediante CSS.

```css
[data-role="admin"] {
  background-color: #f0f0f0;
}

[data-id="123"] {
  border: 2px solid blue;
}
```

---

### **4. Mellores prácticas para o uso de atributos `data-*`**

#### **a) Non usar para presentación**
Os atributos `data-*` non deben usarse para propósitos de presentación. Para iso, usa CSS.

#### **b) Non usar para datos sensibles**
Evita almacenar información sensible nos atributos `data-*`, xa que son visibles no código fonte da páxina.

#### **c) Nomes de atributos**
- Os nomes dos atributos `data-*` deben estar en minúsculas.
- Podes usar guións para separar palabras (camelCase non é necesario).

#### **d) Cantidade de datos**
Non almacenes grandes cantidades de datos nos atributos `data-*`. Para datos complexos, considera usar JSON ou outras estruturas de datos.

---

### **5. Exemplo completo de uso de atributos `data-*`**

Aquí tes un exemplo completo de como usar atributos `data-*` nunha páxina web:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo de atributos data-*</title>
  <style>
    .produto {
      border: 1px solid #ccc;
      padding: 10px;
      margin: 10px;
    }
    
    .produto[data-categoria="electronica"] {
      border-color: blue;
    }
    
    .produto[data-stock="baixo"] {
      background-color: #ffcccc;
    }
  </style>
</head>
<body>
  <h1>Lista de produtos</h1>
  
  <div class="produto" data-id="101" data-categoria="electronica" data-stock="alto">
    <h2>Smartphone</h2>
    <p>Un smartphone moderno con cámara de alta resolución.</p>
    <p>Prezo: 599€</p>
  </div>
  
  <div class="produto" data-id="102" data-categoria="libros" data-stock="baixo">
    <h2>Novela de misterio</h2>
    <p>Unha emocionante novela de misterio.</p>
    <p>Prezo: 15€</p>
  </div>
  
  <div class="produto" data-id="103" data-categoria="electronica" data-stock="medio">
    <h2>Auriculares sen fíos</h2>
    <p>Auriculares de alta calidade con cancelación de ruído.</p>
    <p>Prezo: 129€</p>
  </div>
  
  <script>
    // Acceso aos atributos data-*
    const produtos = document.querySelectorAll('.produto');
    
    produtos.forEach(produto => {
      const id = produto.dataset.id;
      const categoria = produto.dataset.categoria;
      const stock = produto.dataset.stock;
      
      console.log(`Produto ID: ${id}, Categoría: ${categoria}, Stock: ${stock}`);
    });
  </script>
</body>
</html>
```

---

### **6. Diferenza entre atributos `data-*` e IDs/Clases**

#### **Atributos `data-*`**
- **Propósito**: Almacenar datos personalizados para JavaScript, CSS ou outras tecnoloxías.
- **Flexibilidade**: Podes ter múltiples atributos `data-*` no mesmo elemento.
- **Uso**: Ideal para datos que non son nin estrutura nin presentación.

#### **IDs**
- **Propósito**: Identificar un elemento único na páxina.
- **Restricións**: Só pode haber un elemento co mesmo ID nunha páxina.
- **Uso**: Para selección precisa con JavaScript ou CSS.

#### **Clases**
- **Propósito**: Clasificar elementos e aplicar estilos ou comportamento.
- **Flexibilidade**: Un elemento pode ter múltiples clases.
- **Uso**: Para reutilización de estilos e comportamento.

---

### **7. Resumo**

Os atributos `data-*` son unha ferramenta poderosa para engadir datos personalizados aos elementos HTML. Permiten unha mellor comunicación entre HTML e JavaScript, facilitan a personalización con CSS e melloran a accesibilidade. Ao usalos correctamente, podes crear páxinas web máis dinámicas e interactivas.

---

**Data de actualización**: 12/02/2026
**Estado**: ✅ Completado

---

DAW🧊2026

#html #atributos #datadata #webdev #galego











