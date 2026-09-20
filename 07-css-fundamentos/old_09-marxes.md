## A etiqueta `<input>` e as cores

HTML5 introduciu un novo campo de entrada `<input>` que permite ao usuario seleccionar unha cor específica. Este campo proporciona unha interface de usuario coñecida como **selector de cores**, é dicir, un cadro de diálogo que permite escoller unha cor específica dunha roda de cores ou un sistema alternativo, normalmente dentro dun dos diferentes [modelos de cores CSS](https://lenguajecss.com/css/colores/codigos-color/).

### O atributo `type="color"`

A etiqueta que usaremos para mostrar esta interface será `<input>`, utilizando o atributo `type` co valor `color`. Ten en conta que a interface **do selector de cores** pode variar dependendo do sistema operativo. Mentres que en Windows aparece dun xeito, nos dispositivos Apple ou Android pode verse de forma diferente:

| Tipo de información a obter | Etiqueta para usar     | Exemplo |
| --------------------------- | ---------------------- | ------- |
| Campo de selección de cor   | `<input type="color">` |         |

O usuario pode escoller unha cor na súa interface de selección e esta cor gárdase no atributo `value` en [formato hexadecimal](https://lenguajecss.com/css/colores/formato-hexadecimal/).

```html
<form method="post" action="/send/">
  Selecciona a cor desexada:
  <input type="color">
</form>
```

### Cor predeterminada

Tamén é posible especificar un atributo `value` para establecer unha cor predeterminada. Este valor debe estar en formato hexadecimal, con ou sen `#`. Outros esquemas de cores como palabras clave (*`red`, `tomato`, `green`*), `RGB`, `HSL`, `HWB`, `OKLCH` ou outros non son válidos:

```html
<form method="post" action="/send/">
  Selecciona a cor desexada:
  <input type="color" value="#1BF44A">
</form>
```

> 📌 Este campo pódese mellorar combinándoo coa etiqueta HTML `<datalist>`. Verémolo nun artigo futuro onde explicaremos como funciona.

### Personalización do aspecto

Vexamos como personalizar este campo de entrada con CSS e algúns pseudoelementos especiais para modificar a súa aparencia.

| Selector                 | Descrición                                        |
| ------------------------ | ------------------------------------------------- |
| `input[type="color"]`    | Elemento de entrada para escoller a cor.         |
| `::color-swatch-wrapper` | Recipiente exterior da cor escollida.             |
| `::color-swatch`         | Recipiente interior da cor escollida.             |

A continuación, modificamos os estilos para converter o **selector** `<input>` de cores nun elemento circular. Para iso, eliminamos a cor de fondo predeterminada co atributo `background: none`, arredondamos as esquinas e engadimos un bordo:

```css
input[type="color"].custom {
  --size: 45px;

  width: var(--size);
  height: var(--size);
  background: none;
  padding: 0;
  border: 0;

  &::-webkit-color-swatch-wrapper {
    width: var(--size);
    height: var(--size);
    padding: 0;
  }

  &::-webkit-color-swatch {
    border: 3px solid #333;
    border-radius: 50%;
  }
}
```

```html
<fieldset>
  <legend>Sen estilo</legend>
  <input type="color" value="#732FB6">
</fieldset>

<fieldset>
  <legend>Con estilo personalizado</legend>
  <input class="custom" type="color" value="#732FB6">
</fieldset>
```

📢 **Importante**: O diálogo **Selector de cores** non se pode modificar con CSS, xa que é proporcionado polo sistema operativo. Cada plataforma (Windows, macOS/iOS, Linux, Android) ten o seu propio selector de cores.

> ⚠️ Esta API aínda non é estable en todos os navegadores. Para garantir compatibilidade, usa o prefixo `-webkit-` para navegadores baseados en Chromium e `-moz-` para Firefox. Cando a API sexa estable, poderemos prescindir dos prefixos.

> ⚠️ Non podes combinar selectores con prefixos diferentes como `::-webkit-` e `::-moz-` dentro do mesmo bloque CSS. Se o navegador non recoñece un deles, ignorará todo o selector.


---

DAW🧊2025

#html
#DAW