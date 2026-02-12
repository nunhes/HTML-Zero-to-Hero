## A etiqueta `<input>`

A etiqueta `<input>` é o elemento máis versátil para recoller datos en formularios HTML. Adapta o seu comportamento mediante o atributo `type`, permitindo recoller desde textos simples ata arquivos binarios.

### Atributos principais

| Atributo          | Descrición                                                                 | Documentación                                                                 |
|-------------------|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| `name`            | Identificador único para procesamento backend                              |                                                                               |
| `type`            | Define o tipo de dato esperado (texto, email, número...)                   | [Tipos de input](https://developer.mozilla.org/gl/docs/Web/HTML/Element/input) |
| `value`           | Valor predeterminado do campo                                              |                                                                               |
| `placeholder`     | Texto guía que desaparece ao escribir                                      |                                                                               |
| `autocomplete`    | Controla suxestións de autocompletado (`on`/`off`)                         |                                                                               |
| `spellcheck`      | Activa/desactiva corrección ortográfica (`true`/`false`)                   | [Atributo spellcheck](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/spellcheck) |
| `pattern`         | Valida o formato mediante expresión regular                                | [Validación con regex](https://developer.mozilla.org/gl/docs/Web/HTML/Attributes/pattern) |

#### Exemplo básico
```html
<form method="post" action="/procesar-datos/" novalidate>
  <label for="usuario">Nome de usuario:</label>
  <input 
    type="text" 
    id="usuario" 
    name="usuario" 
    placeholder="Ex: marinero21"
    required
    minlength="4"
  >
</form>
```

---

### Tipos específicos de `<input>`

#### 1. Campos de texto especializados
```html
<!-- Email con validación integrada -->
<input type="email" name="correo" placeholder="exemplo@dominio.gal">

<!-- URL con teclado adaptativo en móbiles -->
<input type="url" name="web" placeholder="https://galiza.gal">

<!-- Busca con limpeza rápida -->
<input type="search" name="busqueda" results="5">
```

#### 2. Campos sensibles
```html
<!-- Contrasinal enmascarado -->
<input type="password" name="contrasinal" autocomplete="new-password">

<!-- Campo oculto para datos técnicos -->
<input type="hidden" name="token" value="a3f8d-b2e91">
```

#### 3. Campos numéricos avanzados
```html
<!-- Selector de rango con valores mínimo/máximo -->
<input type="range" name="volume" min="0" max="100" step="5">

<!-- Número con restricións -->
<input type="number" name="idade" min="18" max="99">
```

---

### Boas prácticas de deseño

#### Accesibilidade
```html
<!-- Etiqueta asociada correctamente -->
<label for="telefono">Teléfono de contacto:</label>
<input 
  type="tel" 
  id="telefono" 
  name="telefono" 
  aria-describedby="telHelp"
>
<small id="telHelp">Formato: +34 600 000 000</small>
```

#### Estilización moderna con CSS
```css
/* Estilo responsivo para todos os inputs */
input {
  padding: 0.8rem;
  border: 2px solid #ccc;
  border-radius: 8px;
  width: 100%;
  transition: border-color 0.3s;
}

input:focus {
  border-color: #0066cc;
  outline: none;
  box-shadow: 0 0 8px rgba(0,102,204,0.3);
}

/* Estilo específico para busca */
input[type="search"]::-webkit-search-cancel-button {
  -webkit-appearance: none;
  height: 1.2em;
  width: 1.2em;
  background: url(icon-cancel.svg) no-repeat;
}
```

---

### Recursos adicionais
1. [Guía completa de formularios HTML - MDN](https://developer.mozilla.org/gl/docs/Learn/Forms)
2. [Validación de formularios con JavaScript](https://developer.mozilla.org/gl/docs/Learn/Forms/Form_validation)
3. [Deseño de formularios accesibles - W3C](https://www.w3.org/WAI/tutorials/forms/)
4. [Técnicas avanzadas de CSS para formularios](https://css-tricks.com/tag/forms/)

---

### Notas clave
- **Accesibilidade**: Sempre usar `<label>` + `for`/`id` para asociar textos descriptivos.
- **Seguridade**: Para contrasinais, usar `autocomplete="new-password"` e validación backend.
- **Responsividade**: Usar unidades relativas (`rem`, `%`) e media queries para dispositivos móbiles.
- **Compatibilidade**: Verificar soporte de tipos avanzados en [Can I Use](https://caniuse.com).


---

DAW🧊2025

#html
#DAW