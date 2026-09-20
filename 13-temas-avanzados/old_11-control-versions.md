# Fontes tipográficas

O uso de **fontes tipográficas** en CSS é fundamental para controlar a aparencia do texto nunha páxina web. CSS ofrece varias propiedades para definir o tipo de letra, o tamaño, o grosor, o estilo e moito máis. Ademais, podes usar fontes personalizadas que non están instaladas no sistema do usuario, o que permite un maior control sobre o deseño tipográfico.

Vou explicarche as principais propiedades relacionadas coas fontes en CSS, como usar fontes personalizadas e algunhas boas prácticas para o uso de tipografías na web.

---

### **1.1. Propiedades básicas de fontes en CSS**

#### **`font-family`**
Define o tipo de letra que se usa no texto. Podes especificar varias fontes como fallback en caso de que a primeira non estea dispoñible.

- **Sintaxe**:
  ```css
  font-family: "Nome da fonte", fallback, sans-serif;
  ```
- **Exemplo**:
  ```css
  body {
    font-family: "Arial", "Helvetica", sans-serif;
  }
  ```
  - Se "Arial" non está dispoñible, úsase "Helvetica". Se ningunha das dúas está dispoñible, úsase unha fonte sans-serif xenérica.

#### **`font-size`**
Controla o tamaño do texto. Pódese definir en píxeles (`px`), ems (`em`), rems (`rem`), porcentaxes (`%`), etc.

- **Sintaxe**:
  ```css
  font-size: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    font-size: 2rem;
  }
  ```

#### **`font-weight`**
Define o grosor da fonte. Pódese usar valores como `normal`, `bold`, ou números como `100`, `200`, ..., `900`.

- **Sintaxe**:
  ```css
  font-weight: valor;
  ```
- **Exemplo**:
  ```css
  strong {
    font-weight: bold;
  }
  ```

#### **`font-style`**
Controla o estilo da fonte, como `normal`, `italic` (cursiva) ou `oblique`.

- **Sintaxe**:
  ```css
  font-style: valor;
  ```
- **Exemplo**:
  ```css
  em {
    font-style: italic;
  }
  ```

#### **`font-variant`**
Controla variantes tipográficas, como `small-caps` (versalitas).

- **Sintaxe**:
  ```css
  font-variant: valor;
  ```
- **Exemplo**:
  ```css
  .small-caps {
    font-variant: small-caps;
  }
  ```

#### **`line-height`**
Define a altura da liña de texto. Pódese usar valores sen unidades (multiplicadores) ou con unidades como `px` ou `em`.

- **Sintaxe**:
  ```css
  line-height: valor;
  ```
- **Exemplo**:
  ```css
  p {
    line-height: 1.6;
  }
  ```

---

### **1.2. Uso de fontes personalizadas**

Para usar fontes personalizadas que non están instaladas no sistema do usuario, podes usar a regra **`@font-face`**. Isto permíteche cargar fontes desde un servidor ou un servizo externo como Google Fonts.

#### **`@font-face`**
Define unha fonte personalizada para usala no teu CSS.

- **Sintaxe**:
  ```css
  @font-face {
    font-family: "Nome da fonte";
    src: url("ruta-da-fonte.woff2") format("woff2"),
         url("ruta-da-fonte.woff") format("woff");
  }
  ```
- **Exemplo**:
  ```css
  @font-face {
    font-family: "MiFont";
    src: url("mifont.woff2") format("woff2"),
         url("mifont.woff") format("woff");
  }
  
  body {
    font-family: "MiFont", sans-serif;
  }
  ```

#### **Google Fonts**
Google Fonts é un servizo gratuíto que ofrece unha gran variedade de fontes que podes usar directamente no teu sitio web.

- **Exemplo**:
  ```html
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  ```
  ```css
  body {
    font-family: 'Roboto', sans-serif;
  }
  ```

---

### **1.3. Boas prácticas para o uso de fontes na web**

1. **Usa fontes web seguras**: As fontes web seguras son aquelas que están dispoñibles na maioría dos sistemas operativos. Exemplos inclúen Arial, Helvetica, Times New Roman, etc.
2. **Define fallbacks**: Sempre especifica fontes de fallback no `font-family` para garantir que o texto sexa lexible incluso se a fonte principal non está dispoñible.
3. **Optimiza o rendemento**: Usa formatos de fontes modernos como WOFF2, que ofrecen unha mellor compresión e rendemento.
4. **Limita o número de fontes**: Usar moitas fontes diferentes pode ralentizar a carga da páxina e facer que o deseño sexa menos consistente.
5. **Usa `font-display`**: A propiedade `font-display` controla como se mostra unha fonte mentres se carga. O valor `swap` é útil para evitar que o texto sexa invisible durante a carga.
   ```css
   @font-face {
     font-family: "MiFont";
     src: url("mifont.woff2") format("woff2");
     font-display: swap;
   }
   ```

---

### **1.4. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar fontes personalizadas e propiedades de fonte en CSS:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Uso de Fontes en CSS</title>
  <style>
    @font-face {
      font-family: "MiFont";
      src: url("mifont.woff2") format("woff2"),
           url("mifont.woff") format("woff");
      font-display: swap;
    }

    body {
      font-family: "MiFont", Arial, sans-serif;
      font-size: 1rem;
      line-height: 1.6;
      color: #333;
    }

    h1 {
      font-size: 2.5rem;
      font-weight: bold;
      font-variant: small-caps;
    }

    p {
      font-size: 1.2rem;
      font-style: italic;
    }

    .highlight {
      font-weight: bold;
      color: #ff5733;
    }
  </style>
</head>
<body>
  <h1>Benvido ao noso sitio web</h1>
  <p>Este é un exemplo de como usar fontes personalizadas e propiedades de fonte en CSS.</p>
  <p class="highlight">Este texto está destacado.</p>
</body>
</html>
```

#### **Explicación**:
1. **`@font-face`**: Define unha fonte personalizada chamada "MiFont".
2. **`body`**: Usa "MiFont" como fonte principal, con Arial e sans-serif como fallbacks.
3. **`h1`**: Define un tamaño de fonte grande, en negrita e en versalitas.
4. **`p`**: Define un tamaño de fonte lixeiramente maior e en cursiva.
5. **`.highlight`**: Aplica unha cor destacada e un peso de fonte en negrita.

---

### **1.5. Conclusión**

O uso de **fontes tipográficas** en CSS é esencial para controlar a aparencia do texto nunha páxina web. Coñecer as propiedades básicas (`font-family`, `font-size`, `font-weight`, etc.) e como usar fontes personalizadas permíteche crear deseños tipográficos atractivos e consistentes. Ademais, seguir boas prácticas como o uso de fontes web seguras, a optimización do rendemento e a limitación do número de fontes asegura que o teu sitio web sexa lexible e eficiente. Espero que esta explicación e exemplo che sexan útiles para dominar o uso de fontes en CSS! 😊

## Propiedades CSS para o tratamento de fontes tipográficas

Aquí tes unha lista completa das **propiedades CSS** relacionadas co tratamento de **fontes tipográficas**. Estas propiedades permítenche controlar a aparencia do texto nunha páxina web, desde o tipo de letra ata o espazado entre caracteres e liñas.

---

### **2.1. Propiedades básicas de fontes**

#### **`font-family`**
Define o tipo de letra que se usa no texto. Podes especificar varias fontes como fallback.

- **Sintaxe**:
  ```css
  font-family: "Nome da fonte", fallback, sans-serif;
  ```
  
  > *fallback é a colección de fontes que se inclúen por se algunha falla.*
- **Exemplo**:
  ```css
  body {
    font-family: "Arial", "Helvetica", sans-serif;
  }
  ```

#### **`font-size`**
Controla o tamaño do texto. Pódese definir en píxeles (`px`), ems (`em`), rems (`rem`), porcentaxes (`%`), etc.

- **Sintaxe**:
  ```css
  font-size: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    font-size: 2rem;
  }
  ```

#### **`font-weight`**
Define o grosor da fonte. Pódese usar valores como `normal`, `bold`, ou números como `100`, `200`, ..., `900`.

- **Sintaxe**:
  ```css
  font-weight: valor;
  ```
- **Exemplo**:
  ```css
  strong {
    font-weight: bold;
  }
  ```

#### **`font-style`**
Controla o estilo da fonte, como `normal`, `italic` (cursiva) ou `oblique`.

- **Sintaxe**:
  ```css
  font-style: valor;
  ```
- **Exemplo**:
  ```css
  em {
    font-style: italic;
  }
  ```

#### **`font-variant`**
Controla variantes tipográficas, como `small-caps` (versalitas).

- **Sintaxe**:
  ```css
  font-variant: valor;
  ```
- **Exemplo**:
  ```css
  .small-caps {
    font-variant: small-caps;
  }
  ```

---

### **2.2. Propiedades de espazado e aliñación**

#### **`line-height`**
Define a altura da liña de texto. Pódese usar valores sen unidades (multiplicadores) ou con unidades como `px` ou `em`.

- **Sintaxe**:
  ```css
  line-height: valor;
  ```
- **Exemplo**:
  ```css
  p {
    line-height: 1.6;
  }
  ```

#### **`letter-spacing`**
Controla o espazado entre caracteres.

- **Sintaxe**:
  ```css
  letter-spacing: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    letter-spacing: 2px;
  }
  ```

#### **`word-spacing`**
Controla o espazado entre palabras.

- **Sintaxe**:
  ```css
  word-spacing: valor;
  ```
- **Exemplo**:
  ```css
  p {
    word-spacing: 5px;
  }
  ```

#### **`text-align`**
Controla a aliñación horizontal do texto. Os valores máis comúns son `left`, `right`, `center` e `justify`.

- **Sintaxe**:
  ```css
  text-align: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    text-align: center;
  }
  ```

---

### **2.3. Propiedades avanzadas de fontes**

#### **`@font-face`**
Permite cargar fontes personalizadas que non están instaladas no sistema do usuario.

- **Sintaxe**:
  ```css
  @font-face {
    font-family: "Nome da fonte";
    src: url("ruta-da-fonte.woff2") format("woff2"),
         url("ruta-da-fonte.woff") format("woff");
  }
  ```
- **Exemplo**:
  ```css
  @font-face {
    font-family: "MiFont";
    src: url("mifont.woff2") format("woff2"),
         url("mifont.woff") format("woff");
  }
  
  body {
    font-family: "MiFont", sans-serif;
  }
  ```

#### **`font-display`**
Controla como se mostra unha fonte mentres se carga. Os valores máis comúns son `auto`, `block`, `swap`, `fallback` e `optional`.

- **Sintaxe**:
  ```css
  font-display: valor;
  ```
- **Exemplo**:
  ```css
  @font-face {
    font-family: "MiFont";
    src: url("mifont.woff2") format("woff2");
    font-display: swap;
  }
  ```

#### **`font-stretch`**
Controla o ancho da fonte, como `condensed` (condensada) ou `expanded` (expandida).

- **Sintaxe**:
  ```css
  font-stretch: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    font-stretch: condensed;
  }
  ```

#### **`font-kerning`**
Controla o espazado entre pares de caracteres (kerning). Os valores son `auto`, `normal` e `none`.

- **Sintaxe**:
  ```css
  font-kerning: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    font-kerning: normal;
  }
  ```

#### **`font-variant-ligatures`**
Controla o uso de ligaduras (combinacións de caracteres). Os valores son `normal`, `none`, `common-ligatures`, etc.

- **Sintaxe**:
  ```css
  font-variant-ligatures: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    font-variant-ligatures: common-ligatures;
  }
  ```

#### **`font-variant-caps`**
Controla o uso de versalitas (small caps). Os valores son `normal`, `small-caps`, `all-small-caps`, etc.

- **Sintaxe**:
  ```css
  font-variant-caps: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    font-variant-caps: small-caps;
  }
  ```

---

### **2.4. Propiedades de decoración de texto**

#### **`text-decoration`**
Engade decoracións ao texto, como subliñado (`underline`), tachado (`line-through`) ou liña superior (`overline`).

- **Sintaxe**:
  ```css
  text-decoration: valor;
  ```
- **Exemplo**:
  ```css
  a {
    text-decoration: underline;
  }
  ```

#### **`text-transform`**
Transforma o texto en maiúsculas (`uppercase`), minúsculas (`lowercase`) ou capitaliza a primeira letra de cada palabra (`capitalize`).

- **Sintaxe**:
  ```css
  text-transform: valor;
  ```
- **Exemplo**:
  ```css
  h1 {
    text-transform: uppercase;
  }
  ```

#### **`text-shadow`**
Engade unha sombra ao texto. Pódese definir a posición horizontal, vertical, o desenfoque e a cor da sombra.

- **Sintaxe**:
  ```css
  text-shadow: h-shadow v-shadow blur color;
  ```
- **Exemplo**:
  ```css
  h1 {
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  }
  ```

---

### **2.5. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar varias propiedades de fontes:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Propiedades de Fontes en CSS</title>
  <style>
    @font-face {
      font-family: "MiFont";
      src: url("mifont.woff2") format("woff2"),
           url("mifont.woff") format("woff");
      font-display: swap;
    }

    body {
      font-family: "MiFont", Arial, sans-serif;
      font-size: 1rem;
      line-height: 1.6;
      color: #333;
    }

    h1 {
      font-size: 2.5rem;
      font-weight: bold;
      font-variant: small-caps;
      text-align: center;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
    }

    p {
      font-size: 1.2rem;
      font-style: italic;
      letter-spacing: 1px;
      word-spacing: 2px;
    }

    .highlight {
      font-weight: bold;
      color: #ff5733;
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <h1>Benvido ao noso sitio web</h1>
  <p>Este é un exemplo de como usar propiedades de fontes en CSS.</p>
  <p class="highlight">Este texto está destacado.</p>
</body>
</html>
```

#### **Explicación**:
1. **`@font-face`**: Define unha fonte personalizada chamada "MiFont".
2. **`body`**: Usa "MiFont" como fonte principal, con Arial e sans-serif como fallbacks.
3. **`h1`**: Define un tamaño de fonte grande, en negrita, en versalitas, centrado e con sombra.
4. **`p`**: Define un tamaño de fonte lixeiramente maior, en cursiva, con espazado entre caracteres e palabras.
5. **`.highlight`**: Aplica unha cor destacada, un peso de fonte en negrita e un subliñado.

---

### **2.6. Conclusión**

As **propiedades de fontes en CSS** permítenche controlar a aparencia do texto dunha páxina web de maneira precisa e flexible. Coñecer e usar estas propiedades é esencial para crear deseños tipográficos atractivos e consistentes. Espero que esta lista e exemplo che sexan útiles para dominar o uso de fontes en CSS! 😊


---

DAW🧊2025

#css
#DAW