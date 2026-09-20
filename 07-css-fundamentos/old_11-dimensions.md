## A etiqueta `<select>`

No artigo anterior vimos [caixas de verificación e botóns de opción](https://lenguajehtml.com/html/formularios/etiqueta-html-input-checkbox-radio), que permiten ao usuario escoller unha das varias opcións. Non obstante, se o número de opcións dispoñibles é moi elevado, estes controis poden resultar pouco prácticos. Ademais, poden simplemente non encaixar co deseño visual desexado do formulario.

Se precisamos mostrar unha lista máis longa de opcións, pode ser conveniente utilizar unha **lista de selección**, tamén chamada frecuentemente **lista despregable** ou **combo box**. Estas listas permiten presentar ao usuario varias opcións dispoñibles para que elixa unha.

Hai dous tipos de **listas seleccionables**:

| Tipo de información a obter  | Etiqueta para usar                                           | Exemplo                  |
| ---------------------------- | ------------------------------------------------------------ | ------------------------ |
| Lista despregable de opcións | `<select>`                                                   | Opción 1Opción 2Opción 3 |
| Lista de suxestións          | [`<datalist>`](https://lenguajehtml.com/html/formularios/etiqueta-html-datalist) |                          |

Centrarémonos no primeiro tipo de lista. Máis adiante, no seguinte artigo, veremos o segundo.

### Listas despregables

A forma máis básica de crear unha **lista despregable** está composta por unha etiqueta contedora `<select>` que conterá varias etiquetas `<option>`, unha por cada opción posible que pode escoller o usuario:

```html
<form method="post" action="/enviar/">
  Selecciona a opción desexada:
  <select>
    <option value="1">Opción 1</option>
    <option value="2">Opción 2</option>
    <option value="3">Opción 3</option>
  </select>
</form>
```

Neste fragmento de código, a etiqueta `<select>` contén tres opcións `<option>`. O atributo `value` contén o valor interno da opción, mentres que o contido da etiqueta `<option>` é o que verá o usuario no formulario.

> Alternativamente, podemos definir o texto da opción mediante o atributo `label` en lugar de dentro da etiqueta `<option>`.

#### Opción seleccionada por defecto

Se queremos que unha opción da lista apareza marcada por defecto, incluiremos o atributo `selected`:

```html
<form method="post" action="/enviar/">
  Selecciona a opción desexada:
  <select>
    <option value="1">Opción 1</option>
    <option value="2" selected>Opción 2</option>
    <option value="3">Opción 3</option>
  </select>
</form>
```

Como podes ver, **a Opción 2** aparecerá seleccionada inicialmente. É importante non confundir o atributo `checked` (usado en `checkbox` e `radio`) co atributo `selected`, xa que teñen funcións diferentes.

#### Suxestión visual

Para ofrecer unha suxestión ao usuario sen que esta opción sexa seleccionable, podemos utilizar `disabled`:

```html
<form method="post" action="/enviar/">
  Selecciona a opción desexada:
  <select>
    <option disabled selected>- Escolle unha opción -</option>
    <option value="1">Opción 1</option>
    <option value="2">Opción 2</option>
    <option value="3">Opción 3</option>
  </select>
</form>
```

Isto evita que o usuario seleccione a opción de suxestión, pero permite que apareza inicialmente como guía.

#### Grupos de opcións

Para agrupar opcións dentro dunha lista despregable, utilizamos a etiqueta `<optgroup>`:

```html
<form method="post" action="/enviar/">
  Selecciona a opción desexada:
  <select>
    <optgroup label="Categoría 1">
      <option value="1">Opción 1</option>
      <option value="2">Opción 2</option>
    </optgroup>
    <optgroup label="Categoría 2">
      <option value="3">Opción 3</option>
      <option value="4">Opción 4</option>
    </optgroup>
  </select>
</form>
```

A etiqueta `<optgroup>` permite definir categorías para unha mellor organización das opcións.

### Selección múltiple

Podemos permitir que o usuario seleccione varias opcións utilizando o atributo `multiple`:

```html
<form method="post" action="/enviar/">
  Selecciona as opcións desexadas:
  <select multiple>
    <option value="1">Opción 1</option>
    <option value="2">Opción 2</option>
    <option value="3">Opción 3</option>
  </select>
</form>
```

Para seleccionar varias opcións, o usuario debe manter premida a tecla `Ctrl` (Windows/Linux) ou `Cmd` (Mac) mentres fai clic nas opcións.

### Personalización do estilo

Podemos modificar a aparencia do `<select>` mediante CSS:

```css
select.custom {
  appearance: none;
  padding: 0.5rem 2.5rem 0.5rem 1rem;
  border-radius: 4px;
  font-family: Arial, sans-serif;
  font-size: 1rem;
  color: #4B0082;
  border: 2px solid #4B0082;
  background: url('data:image/svg+xml;base64,...') center right 5px no-repeat;
  background-size: 20px;
}
```

Aquí usamos `appearance: none;` para eliminar os estilos predeterminados do navegador e engadimos unha imaxe SVG codificada en Base64 para personalizar a frecha.

> Para unha personalización máis avanzada, consulta [Personalización avanzada de etiquetas `<select>`](https://lenguajehtml.com/html/formularios/personalizar-etiqueta-select).

### Personalización avanzada (experimental)

Actualmente, os navegadores están traballando en novas capacidades de personalización para `<select>`. En **Chrome Canary 135+**, é posible utilizar:

```css
select,
::picker(select) {
  appearance: base-select;
}
```

Isto permite unha personalización máis profunda do `<select>` e a xanela despregable.

### Conclusión

A etiqueta `<select>` é unha ferramenta moi útil para formularios con múltiples opcións, e podemos mellorar a súa usabilidade utilizando `optgroup`, `multiple`, `disabled` e `selected`. Ademais, aínda que a súa personalización é limitada, podemos modificar algúns aspectos visuais con CSS e, no futuro, contar con opcións máis avanzadas nos navegadores modernos.

Para máis información, consulta:
- [Documentación oficial de Mozilla sobre `<select>`](https://developer.mozilla.org/gl/docs/Web/HTML/Element/select)
- [Guía avanzada sobre formularios HTML](https://lenguajehtml.com/html/formularios/)


---

DAW🧊2025

#html
#DAW