## A etiqueta `<input>` con caixas de verificación

Se queremos definir opcións onde o usuario debe escoller ou seleccionar, en moitos casos o máis axeitado é utilizar un dos dous tipos de campos seguintes:

- **Casiñas de verificación**, tamén chamadas campos `checkbox` (*verdadeiro ou falso*).
- **Botóns de opción**, tamén chamados botóns de opción `radio` (*unha opción entre varias dispoñibles*).

Para configuralos nunha páxina teriamos que usar as seguintes etiquetas:

| Tipo de campo                                | Etiqueta para usar        | Exemplo |
|--------------------------------------------|-------------------------|---------|
| Casiña de verificación (activada/desactivada) | `<input type="checkbox">` |         |
| Botón de opción (unha só opción)            | `<input type="radio">`    |         |

Vexamos as súa diferenzas e profundicemos en cada tipo de control para comprender as súa capacidades.

### Casiñas de verificación

As **casiñas de verificación** indícanse mediante o atributo `type="checkbox"` nun campo de entrada `<input>`. Este tipo de control permite mostrar unha casiña de verificación ao usuario, dándolle a opción de activala ou desactivala.

```html
<form method="post" action="/enviar/">
  <input type="checkbox" name="nome_real">
  Mostrar nome real do usuario
</form>
```

Este tipo de controis son útiles para definir estados que teñen valores booleanos, como verdadeiro/falso, activado/desactivado ou positivo/negativo.

#### O atributo `checked`

Se engadimos o atributo `checked`, a casiña de verificación aparecerá activada por defecto ao cargar a páxina:

```html
<form method="post" action="/enviar/">
  <input type="checkbox" name="nome_real" checked>
  Mostrar nome real do usuario
  <input type="checkbox" name="alcume">
  Mostrar alcume do usuario
</form>
```

Para obter o estado actual dun campo `<input type="checkbox">` en JavaScript, debemos acceder á propiedade `checked`:

```javascript
const checkbox = document.querySelector("input[name='nome_real']");
console.log(checkbox.checked); // true se está marcada, false se non
```

> **NOTA**: O atributo `checked` define o **estado inicial** da casiña, mentres que a propiedade `checked` indica o **estado actual**. Lembra que un atributo e unha propiedade non son o mesmo.

#### Estado indeterminado

Aínda que non se pode definir en HTML, é posible establecer un **estado indeterminado** desde JavaScript. Isto adoita mostrarse visualmente cunha aparencia gris e cunha liña.

```html
<form method="post" action="/enviar/">
  <input type="checkbox" id="indeterminado"> Mostrar nome real do usuario
</form>

<script>
  const input = document.querySelector("#indeterminado");
  input.indeterminate = true;
</script>
```

> O **estado indeterminado** é só un cambio visual e non se envía co formulario. O valor enviado seguirá dependendo da propiedade `checked`.

#### Personalización con CSS

A aparencia das casiñas de verificación pode modificarse mediante a propiedade CSS `accent-color`, que cambia a cor de acento da maioría dos campos de formulario.

```html
<form method="post" action="/enviar/">
  <input type="checkbox" checked> Mostrar nome real do usuario
</form>

<style>
  input[type="checkbox"] {
    accent-color: red;
  }
</style>
```

#### Recursos adicionais

- 📖 [MDN: `input type="checkbox"`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox)
- 📖 [HTML Living Standard - `input`](https://html.spec.whatwg.org/multipage/input.html)

😊

---

DAW🧊2025

#html
#DAW