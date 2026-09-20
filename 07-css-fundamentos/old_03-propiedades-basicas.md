# A etiqueta `form`

HTML ofrece un conxunto de etiquetas, atributos e conceptos clave para a entrada de datos por parte do usuario e o envío de información a través dunha páxina web. Un dos desafíos principais é eliminar ambigüidades ou garantir que os datos introducidos cumpran restricións específicas para o seu posterior procesamento.

## Que é un formulario?

**Os formularios** (etiqueta `<form>`) son mecanismos que permiten aos usuarios enviar información mediante campos dispostos dun xeito intuitivo. Estes campos determinan o tipo de datos recollidos e como se procesarán no *backend*.

**Obxectivos** ao crear un formulario:

- Simplificar ao máximo a **introdución de datos** para o usuario.
- Ofrecer unha experiencia de usuario **fluída** e **intuitiva**.
- Asegurar que os datos teñan un **formato estandarizado**.
- Minimizar erros durante a entrada de información.
- Comunicar **erros de validación** de forma clara e inmediata.

### A etiqueta `<form>`

A etiqueta `<form>` actúa como contedor principal para todos os campos do formulario:

```html
<form></form>
```

É posible incluír múltiples formularios nunha mesma páxina (ex: formulario de busca, contacto e comentarios). 

> 💡 Aínda que é posible crear formularios sen `<form>` mediante JavaScript, non é recomendable xa que afecta á accesibilidade e boas prácticas.

#### Atributos principais

| Atributo         | Descrición                                                  | Recursos adicionais                                         |
|------------------|-------------------------------------------------------------|-------------------------------------------------------------|
| `action`         | URL de destino para o envío de datos.                       |                                                             |
| `method`         | Método HTTP: `GET` (visíbel na URL) ou `POST` (oculto).     | [Métodos HTTP](https://developer.mozilla.org/es/docs/Web/HTTP/Methods) |
| `name`           | Identificador único para procesamento no backend.           |                                                             |
| `target`         | Define onde abrir a resposta (`_blank` para nova xanela).   |                                                             |
| `enctype`        | Codificación para o envío de arquivos.                      | [Subir arquivos](https://developer.mozilla.org/es/docs/Web/HTML/Element/input/file) |
| `accept-charset` | Codificación de caracteres (ex: `utf-8`).                   |                                                             |
| `autocomplete`   | Activa (`on`) ou desactiva (`off`) suxestións.              |                                                             |
| `novalidate`     | Desactiva validacións HTML5.                                | [Validacións](https://developer.mozilla.org/es/docs/Learn/Forms/Form_validation) |

#### Exemplo I: Formulario básico

```html
<form name="contacto" method="post" action="/procesar-datos/"></form>
```

- **`name`**: Identifica o formulario no código backend.
- **`method="post"**:** Recomendado para datos sensibles (claves, tarxetas).
- **`action`**: Envía os datos á ruta `/procesar-datos/` do servidor.

#### Exemplo II: Formulario de busca con novas características

```html
<form 
  name="pesquisa" 
  method="get" 
  action="/resultados-busca/" 
  target="_blank" 
  accept-charset="utf-8"
>
</form>
```

- **`target="_blank"`**: Abre os resultados nunha nova pestana (considere engadir `rel="noopener"` por seguridade).
- **`accept-charset`**: Garante compatibilidade con caracteres especiais (á, ñ, ç).

#### Exemplo III: Desactivando funcionalidades

```html
<form 
  method="post" 
  action="/gardar-perfil/" 
  autocomplete="off" 
  novalidate
>
</form>
```

- **`autocomplete="off"`**: Evita que o navegador suxira valores previos.
- **`novalidate`**: Ignora validacións HTML5 (útil se se validará con JavaScript).

---

### Información dun formulario

Para que un usuario poida introducir datos nun formulario, debemos fornecer **campos adecuados** ao tipo de información solicitada. É esencial predefinir que **datos requirimos** (texto, números, datas...) para escoller o elemento HTML máis apropiado.

#### Tipos de datos e elementos asociados

| Tipo de dato                                             | Exemplos comúns                              | Elemento HTML recomendado                                  | Recursos adicionais                                                                 |
|----------------------------------------------------------|-----------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Texto curto**                                          | Nome, apelidos, teléfono                      | `<input type="text">`                                      | [Guía completa de `<input>`](https://developer.mozilla.org/gl/docs/Web/HTML/Element/input) |
| **Texto longo**                                          | Comentarios, descricións                      | `<textarea>`                                               | [Uso de `<textarea>`](https://developer.mozilla.org/gl/docs/Web/HTML/Element/textarea)      |
| **Valores numéricos**                                    | Idade, cantidade, prezo                       | `<input type="number">` ou `<input type="range">`          | [Inputs numéricos](https://developer.mozilla.org/gl/docs/Web/HTML/Element/input/number)    |
| **Datas e horas**                                        | Data de nacemento, hora de reserva            | `<input type="date">`, `<input type="time">`               | [Inputs de data](https://developer.mozilla.org/gl/docs/Web/HTML/Element/input/date)        |
| **Selección binaria**                                    | Aceptar termos, activar notificacións         | `<input type="checkbox">`                                  | [Checkboxes e radios](https://developer.mozilla.org/gl/docs/Web/HTML/Element/input/checkbox) |
| **Selección única**                                      | Escoller país ou idioma                       | `<select>` ou `<input type="radio">`                       | [Listas desplegables](https://developer.mozilla.org/gl/docs/Web/HTML/Element/select)       |
| **Selección múltiple**                                   | Escoller intereses ou habilidades             | `<select multiple>` ou varios `<input type="checkbox">`    | [Selección múltiple](https://developer.mozilla.org/gl/docs/Web/HTML/Element/select#attr-multiple) |
| **Combinar opcións fixas e texto libre**                 | "Outro" con campo aberto                      | `<datalist>` con `<input list="id">`                       | [Listas de suxestións](https://developer.mozilla.org/gl/docs/Web/HTML/Element/datalist)     |
| **Selección de cor**                                     | Escoller cor de fondo                         | `<input type="color">`                                     | [Selector de cor](https://developer.mozilla.org/gl/docs/Web/HTML/Element/input/color)       |
| **Subida de arquivos**                                   | Enviar PDF, imaxe ou documento                | `<input type="file">`                                      | [Subir arquivos](https://developer.mozilla.org/gl/docs/Web/HTML/Element/input/file)         |

> 💡 Para casos complexos (ex: selectores de mapa ou editores de texto enriquecido), recoméndase usar bibliotecas como [React Select](https://react-select.com/) ou [Quill](https://quilljs.com/).

---

### Sintaxe básica de formularios

A etiqueta `<form>` actúa como contedor principal, mentres os elementos `<input>`, `<select>`, etc., definen os campos. Exemplo funcional:

```html
<form name="rexistro" method="post" action="/procesar-datos/" aria-label="Rexistro de usuario">
  <!-- Campo de texto con etiqueta accesible -->
  <label for="nome">Nome completo:</label>
  <input type="text" id="nome" name="nome_usuario" required>
  
  <!-- Selector de país con opcións -->
  <label for="pais">País:</label>
  <select id="pais" name="pais_usuario">
    <option value="es">España</option>
    <option value="pt">Portugal</option>
    <option value="fr">Francia</option>
  </select>
  
  <!-- Botón de envío -->
  <button type="submit">Rexistrarse</button>
</form>
```

**Características destacadas:**
- **`<label>`**: Mellora a accesibilidade e permite facer clic no texto para activar o campo.
- **`required`**: Validación HTML5 para campos obrigatorios.
- **`<button>`**: Preferible sobre `<input type="submit">` por permitir estilización CSS.

---

#### Boas prácticas recomendadas
1. **Validacións**: Combinar validacións HTML5 (`pattern`, `min`, `max`) con JavaScript para maior seguridade.
2. **Accesibilidade**: Usar atributos `aria-*` e asociar sempre `<label>` aos campos.
3. **Deseño responsivo**: Organizar campos con CSS Grid/Flexbox. Exemplo:
   ```css
   form {
     display: grid;
     gap: 1rem;
     max-width: 600px;
     margin: 0 auto;
   }
   ```





### Recursos adicionais
1. [Formularios HTML - MDN Web Docs](https://developer.mozilla.org/gl/docs/Learn/Forms) (en galego)
2. [Boas prácticas en formularios - W3C](https://www.w3.org/WAI/tutorials/forms/)
3. [Diseño de formularios accesibles - WebAIM](https://webaim.org/techniques/forms/)
4. [Formularios accesibles - W3C](https://www.w3.org/WAI/tutorials/forms/)
5. [Diseño de formularios modernos - CSS-Tricks](https://css-tricks.com/tips-for-web-form-design/)

---

### Notas importantes
- **`GET` vs `POST`**: Use `GET` para buscas (datos visíbeis na URL) e `POST` para operacións sensíbeis (login, pagos).
- **Validacións**: Combinar validacións HTML5 (`required`, `pattern`) con JavaScript para maior seguridade.
- **Accesibilidade**: Sempre inclúa a etiqueta `<label>` asociada a cada campo e usa atributos `aria-*` cando sexa necesario.

---

DAW🧊2026

#html
#DAW