# Unidades de medida

As **unidades de medida** en CSS son fundamentais para controlar o tamaño das fontes, o espazado entre elementos, a organización dos contidos e moito máis. Estas unidades pódense clasificar en dous tipos principais: **unidades absolutas** e **unidades relativas**. Cada tipo ten os seus usos, vantaxes e desvantaxes, e a súa elección pode afectar significativamente ao deseño, a responsividade, a usabilidade e a accesibilidade dun sitio web.

Imos ver as principais unidades de medida, cando usalas e como afectan ao maquetado e á experiencia do usuario.

---

## **1. Unidades absolutas**

As **unidades absolutas** son fixas e non cambian en función do contexto ou do dispositivo. As máis comúns son:

- **`px` (píxeles)**: De lonxe é a unidade máis usada. Un píxel corresponde a un punto na pantalla.
- **`pt` (puntos)**: Usada principalmente en impresión. 1 punto = 1/72 de polgada.
- **`in` (polgadas)**: 1 polgada = 96 píxeles.
- **`cm` (centímetros)** e **`mm` (milímetros)**: Unidades baseadas no sistema métrico.

#### **Cando usar unidades absolutas?**
- **Deseños fixos**: Cando o tamaño dos elementos debe ser exacto e non cambiar en función do contexto.
- **Impresión**: As unidades como `pt`, `in`, `cm` e `mm` son útiles para deseños destinados a impresión.

#### **Desvantaxes**:
- **Falta de flexibilidade**: Non se adaptan ben a diferentes tamaños de pantalla ou dispositivos.
- **Problemas de accesibilidade**: Os usuarios que necesitan ampliar o texto poden ter dificultades se os tamaños están definidos en unidades absolutas.

---

## **2. Unidades relativas**

As **unidades relativas** son flexibles e dependen dun valor de referencia, como o tamaño da fonte do elemento pai ou o tamaño da pantalla. As máis comúns son:

- **`em`**: Basease no tamaño da fonte do elemento pai. Se o elemento pai ten unha fonte de `16px`, `1em = 16px`.
- **`rem`**: Basease no tamaño da fonte do elemento raíz (`<html>`). Se o elemento raíz ten unha fonte de `16px`, `1rem = 16px`.
- **`%` (porcentaxe)**: Basease nunha porcentaxe do valor do elemento pai.
- **`vw` (viewport width)**: 1% do ancho da ventana gráfica (viewport).
- **`vh` (viewport height)**: 1% do alto da ventana gráfica.
- **`vmin` e `vmax`**: O menor ou maior valor entre `vw` e `vh`.

#### **Cando usar unidades relativas?**
- **Deseños responsivos**: As unidades como `em`, `rem`, `%`, `vw` e `vh` son ideais para deseños que deben adaptarse a diferentes tamaños de pantalla.
- **Accesibilidade**: As unidades relativas permiten que os usuarios amplíen ou reduzan o texto sen romper o deseño.
- **Espazado e tamaños flexibles**: Úsanse para definir espazos, anchos, altos e outros tamaños de maneira flexible.

#### **Vantaxes**:
- **Flexibilidade**: Adáptanse a diferentes dispositivos e tamaños de pantalla.
- **Accesibilidade**: Facilitan a lectura e a usabilidade para usuarios con discapacidades visuais.

| Relativas | Absolutas |
| :-------: | :-------: |
|   `em`    |   `px`    |
|   `rem`   |   `pt`    |
|   `vh`    |   `cm`    |
|   `vw`    |   `in`    |
|    `%`    |   `mm`    |
|     …     |           |



---

## **3. Unidades recomendables e contextos**

#### **`rem`**
- **Recomendable**: Para tamaños de fonte, espazado e dimensións que deben ser consistentes en toda a páxina.
- **Contexto**: Ideal para deseños responsivos e accesibles, xa que se basea no tamaño da fonte do elemento raíz.

> *Relativo ao tamaño da fonte do elemento html raíz. Moitas veces é o máis fácil de traballar. Se o tamaño da fonte raíz é 20px, 1 rem sempre é 20px, 2rem sempre é 40px, etc.*

#### **`em`**
- **Recomendable**: Para espazado e tamaños que dependen do contexto do elemento pai.
- **Contexto**: Útil cando se quere que os elementos escalen en función do tamaño da fonte do seu contedor.

> *Ao usar `font-size`, `1em` é igual ao tamaño da fonte do elemento pai. 2em's é o dobre do tamaño da fonte do elemento pai, etc.  Con outras propiedades, `1em` é igual ao tamaño de letra calculado do propio elemento.*

#### **`%`**
- **Recomendable**: Para anchos, altos e espazado que deben ser proporcionais ao tamaño do contedor pai.
- **Contexto**: Ideal para deseños flexibles e layouts baseados en porcentaxes.

#### **`vw` e `vh`**
- **Recomendable**: Para elementos que deben escalar en función do tamaño da ventana gráfica (viewport).
- **Contexto**: Útil para deseños "full-screen" ou elementos que deben cubrir toda a pantalla.

#### **`px`**
- **Recomendable**: Para bordos, sombras e outros detalles que requiren precisión.
- **Contexto**: Útil en deseños fixos ou cando se require un control exacto do tamaño.

> *1px non é necesariamente igual ao ancho exacto dun píxel!
> Non (moi) recomendado para sitios web responsivos.*

---

## **4. Como afectan ao maquetado, responsividade, usabilidade e accesibilidade**

#### **Maquetado**
- **Unidades absolutas**: Poden facer que o deseño sexa ríxido e difícil de adaptar a diferentes dispositivos.
- **Unidades relativas**: Permiten deseños flexibles e adaptables, o que facilita a creación de layouts responsivos.

#### **Responsividade**
- **Unidades absolutas**: Non se adaptan ben a diferentes tamaños de pantalla, o que pode levar a problemas en dispositivos pequenos ou grandes.
- **Unidades relativas**: Adáptanse automaticamente ao tamaño da pantalla, o que facilita a creación de deseños responsivos.

#### **Usabilidade**
- **Unidades absolutas**: Poden dificultar a lectura e a interacción en dispositivos con diferentes densidades de píxeles.
- **Unidades relativas**: Melloran a experiencia do usuario ao permitir que o texto e os elementos escalen de maneira adecuada.

#### **Accesibilidade**
- **Unidades absolutas**: Poden causar problemas para usuarios que necesitan ampliar o texto ou cambiar o tamaño da fonte.
- **Unidades relativas**: Facilitan a accesibilidade ao permitir que os usuarios amplíen ou reduzan o texto sen romper o deseño.

---

## **5. Exemplo práctico**

Aquí tes un exemplo que mostra como usar unidades relativas e absolutas nun deseño responsivo:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Unidades de Medida en CSS</title>
  <style>
    /* Tamaño de fonte base */
    html {
      font-size: 16px;
    }

    /* Usando rem para tamaños de fonte e espazado */
    h1 {
      font-size: 2rem; /* 32px */
      margin-bottom: 1rem; /* 16px */
    }

    p {
      font-size: 1rem; /* 16px */
      line-height: 1.5; /* 24px */
    }

    /* Usando % para anchos */
    .container {
      width: 90%;
      max-width: 1200px;
      margin: 0 auto;
    }

    /* Usando vw e vh para elementos "full-screen" */
    .hero {
      height: 50vh; /* 50% do alto da ventana */
      background-color: #f4f4f4;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    /* Usando em para espazado relativo ao tamaño da fonte */
    .button {
      font-size: 1.2em; /* 19.2px */
      padding: 0.5em 1em; /* 9.6px 19.2px */
      background-color: #007bff;
      color: white;
      border: none;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="hero">
    <h1>Benvido ao noso sitio web</h1>
  </div>
  <div class="container">
    <p>Este é un exemplo de como usar unidades de medida en CSS para crear un deseño responsivo e accesible.</p>
    <button class="button">Clica aquí</button>
  </div>
</body>
</html>
```

---

## **6. Conclusión**

A elección entre **unidades absolutas** e **relativas** en CSS depende do contexto e dos obxectivos do teu deseño. As unidades relativas, como `rem`, `em`, `%`, `vw` e `vh`, son xeralmente máis recomendables para deseños responsivos e accesibles, mentres que as unidades absolutas, como `px`, son útiles para detalles que requiren precisión. Espero que esta explicación e exemplo che sexan útiles para tomar decisións informadas sobre o uso de unidades de medida en CSS! 😊

---

DAW🧊2025

#css
#DAW