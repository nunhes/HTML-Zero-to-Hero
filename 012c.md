# CSS Text properties

En CSS hai unha gran variedade de propiedades deseñadas especificamente para o **tratamento de texto**. Estas propiedades permiten controlar aspectos como o tipo de letra, o tamaño, o espazado, a aliñación, a decoración e moito máis. Vou explicarche as principais propiedades e os efectos que teñen no texto.

---

## **1. Propiedades básicas de texto**

#### **`font-family`**
Define o tipo de letra (font) que se usa no texto. Podes especificar varias fontes como fallback en caso de que a primeira non estea dispoñible.

- **Sintaxe**:
  ```css
  font-family: "Arial", sans-serif;
  ```
- **Efecto**: Cambia o estilo da fonte do texto.

#### **`font-size`**
Controla o tamaño do texto. Pódese definir en píxeles (`px`), ems (`em`), rems (`rem`), porcentaxes (`%`), etc.

- **Sintaxe**:
  ```css
  font-size: 16px;
  ```
- **Efecto**: Cambia o tamaño do texto.

#### **`font-weight`**
Define o grosor da fonte. Pódese usar valores como `normal`, `bold`, ou números como `100`, `200`, ..., `900`.

- **Sintaxe**:
  ```css
  font-weight: bold;
  ```
- **Efecto**: Cambia o grosor do texto (por exemplo, para facelo negrita).

#### **`font-style`**
Controla o estilo da fonte, como `normal`, `italic` (cursiva) ou `oblique`.

- **Sintaxe**:
  ```css
  font-style: italic;
  ```
- **Efecto**: Cambia o estilo do texto (por exemplo, para facelo cursiva).

#### **`color`**
Define a cor do texto.

- **Sintaxe**:
  ```css
  color: #333;
  ```
- **Efecto**: Cambia a cor do texto.

---

## **2. Propiedades de espazado e aliñación**

#### **`text-align`**
Controla a aliñación horizontal do texto. Os valores máis comúns son `left`, `right`, `center` e `justify`.

- **Sintaxe**:
  ```css
  text-align: center;
  ```
- **Efecto**: Aliña o texto horizontalmente.

#### **`line-height`**
Define a altura da liña de texto. Pódese usar valores sen unidades (multiplicadores) ou con unidades como `px` ou `em`.

- **Sintaxe**:
  ```css
  line-height: 1.5;
  ```
- **Efecto**: Controla o espazado entre liñas de texto.

#### **`letter-spacing`**
Controla o espazado entre caracteres.

- **Sintaxe**:
  ```css
  letter-spacing: 2px;
  ```
- **Efecto**: Aumenta ou diminúe o espazado entre letras.

#### **`word-spacing`**
Controla o espazado entre palabras.

- **Sintaxe**:
  ```css
  word-spacing: 5px;
  ```
- **Efecto**: Aumenta ou diminúe o espazado entre palabras.

---

## **3. Propiedades de decoración e transformación**

#### **`text-decoration`**
Engade decoracións ao texto, como subliñado (`underline`), tachado (`line-through`) ou liña superior (`overline`).

- **Sintaxe**:
  ```css
  text-decoration: underline;
  ```
- **Efecto**: Engade decoracións ao texto.

#### **`text-transform`**
Transforma o texto en maiúsculas (`uppercase`), minúsculas (`lowercase`) ou capitaliza a primeira letra de cada palabra (`capitalize`).

- **Sintaxe**:
  ```css
  text-transform: uppercase;
  ```
- **Efecto**: Cambia a capitalización do texto.

#### **`text-shadow`**
Engade unha sombra ao texto. Pódese definir a posición horizontal, vertical, o desenfoque e a cor da sombra.

- **Sintaxe**:
  ```css
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  ```
- **Efecto**: Engade unha sombra ao texto.

---

## **4. Propiedades avanzadas de texto**

#### **`white-space`**
Controla como se manexan os espazos en branco e os saltos de liña no texto. Valores comúns inclúen `normal`, `nowrap` (non permite saltos de liña) e `pre` (conserva os espazos e saltos de liña).

- **Sintaxe**:
  ```css
  white-space: nowrap;
  ```
- **Efecto**: Controla o comportamento dos espazos e saltos de liña.

#### **`text-overflow`**
Controla como se mostra o texto cando desborda o contedor. Úsase xunto con `white-space: nowrap` e `overflow: hidden`.

- **Sintaxe**:
  ```css
  text-overflow: ellipsis;
  ```
- **Efecto**: Mostra puntos suspensivos (`...`) cando o texto desborda.

#### **`direction`**
Define a dirección do texto, como `ltr` (esquerda a dereita) ou `rtl` (dereita a esquerda).

- **Sintaxe**:
  ```css
  direction: rtl;
  ```
- **Efecto**: Cambia a dirección do texto.

---

## **5. Propiedades de tipografía avanzada**

#### **`font-variant`**
Controla variantes tipográficas, como `small-caps` (versalitas).

- **Sintaxe**:
  ```css
  font-variant: small-caps;
  ```
- **Efecto**: Converte o texto en versalitas.

#### **`font-stretch`**
Controla o ancho da fonte, como `condensed` (condensada) ou `expanded` (expandida).

- **Sintaxe**:
  ```css
  font-stretch: condensed;
  ```
- **Efecto**: Cambia o ancho da fonte.

#### **`@font-face`**
Permite cargar fontes personalizadas que non están instaladas no sistema do usuario.

- **Sintaxe**:
  ```css
  @font-face {
    font-family: 'MiFont';
    src: url('mifont.woff2') format('woff2');
  }
  ```
- **Efecto**: Carga unha fonte personalizada para usala no texto.

---

## **6. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar varias propiedades de texto en CSS:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Propiedades de Texto en CSS</title>
  <style>
    body {
      font-family: "Arial", sans-serif;
      line-height: 1.6;
      color: #333;
    }

    h1 {
      font-size: 2.5rem;
      font-weight: bold;
      text-align: center;
      text-transform: uppercase;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
    }

    p {
      font-size: 1.2rem;
      text-align: justify;
      letter-spacing: 1px;
      word-spacing: 2px;
    }

    .highlight {
      font-style: italic;
      color: #ff5733;
      text-decoration: underline;
    }

    .small-caps {
      font-variant: small-caps;
    }

    .overflow-example {
      white-space: nowrap;
      overflow: hidden;
      text-overflow: ellipsis;
      width: 200px;
      border: 1px solid #ccc;
      padding: 10px;
    }
  </style>
</head>
<body>
  <h1>Propiedades de Texto en CSS</h1>
  <p>
    Este é un exemplo de texto con varias propiedades CSS aplicadas. O texto está xustificado, con espazado entre letras e palabras. 
    <span class="highlight">Este texto está destacado</span> e ten un subliñado.
  </p>
  <p class="small-caps">
    Este texto está en versalitas grazas á propiedade <code>font-variant</code>.
  </p>
  <div class="overflow-example">
    Este texto é demasiado longo e desbordará o contedor, mostrando puntos suspensivos.
  </div>
</body>
</html>
```

---

## **7. Conclusión**

As propiedades de texto en CSS son fundamentais para controlar a aparencia e o comportamento do texto nunha páxina web. Desde a elección da fonte e o tamaño ata o espazado, a aliñación e a decoración, estas propiedades permiten crear deseños de texto atractivos e funcionais. Espero que esta explicación e exemplo che sexan útiles para dominar o tratamento de texto en CSS! 😊

---

DAW🧊2025

#css
#DAW