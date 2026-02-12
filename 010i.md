## A etiqueta `<textarea>`

A etiqueta `<textarea>` é o elemento HTML óptimo para recoller **textos longos** como comentarios, descricións ou mensaxes extensas. A diferenza de `<input type="text">`, permite múltiples liñas e ofrece maior flexibilidade ao usuario.

### ✨ Atributos clave

| Atributo | Función                                                                 | Boas prácticas                                                                 |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| `rows`   | Define o número inicial de liñas visíbeis                               | Usar en combinación con `min-height` en CSS para responsividade               |
| `cols`   | Establece o ancho en caracteres                                        | **Obsoleto** - Preferir `width: 100%` en CSS                                  |
| `wrap`   | Controla o axuste de texto (`soft`/`hard`)                              | Usar `soft` para textos libres, `hard` para formatos estruturados             |
| `placeholder` | Proporciona unha guía contextual                                     | Mantéñao conciso (< 50 caracteres)                                            |

#### 📝 Exemplo básico
```html
<form method="post" action="/procesar-datos/">
  <label for="mensaxe">Mensaxe:</label>
  <textarea 
    id="mensaxe" 
    name="mensaxe_usuario" 
    rows="4"
    placeholder="Escribe aquí o teu comentario..."
    spellcheck="true"
  ></textarea>
</form>
```

---

### 🎨 Personalización avanzada

#### 1. Adaptación dinámica ao contido
```html
<textarea class="autoajustable"></textarea>

<style>
.autoajustable {
  resize: vertical;
  min-height: 100px;
  max-height: 300px;
  width: 100%;
  padding: 1rem;
  transition: height 0.2s ease;
}
</style>
```

#### 2. Estilo moderno con CSS variables
```css
:root {
  --color-borde: #ccc;
  --color-foco: #4a90e2;
}

textarea {
  font-family: system-ui, sans-serif;
  padding: 1rem;
  border: 2px solid var(--color-borde);
  border-radius: 8px;
  width: 100%;
  line-height: 1.5;

  &:focus {
    border-color: var(--color-foco);
    box-shadow: 0 0 0 3px rgba(74, 144, 226, 0.25);
  }

  &::placeholder {
    color: #666;
    opacity: 0.8;
  }
}
```

---

### 🛠️ Editores WYSIWYG recomendados

Para necesidades avanzadas de edición (formato, imaxes, táboas), considere estas bibliotecas:

| Biblioteca                      | Puntos fortes                                   | Enlace                                      |
|---------------------------------|-------------------------------------------------|---------------------------------------------|
| **TinyMCE**                     | Integración con CMS, soporte Markdown          | [tiny.cloud](https://www.tiny.cloud/)       |
| **CKEditor 5**                  | Accesibilidade AAA, colaborativo               | [ckeditor.com](https://ckeditor.com/)       |
| **TipTap**                      | Baseado en ProseMirror, extensible             | [tiptap.dev](https://tiptap.dev/)           |
| **Quill**                       | Lixeiro (< 50KB), temas personalizables        | [quilljs.com](https://quilljs.com/)         |

#### 💡 Exemplo con TipTap
```html
<div id="editor"></div>

<script type="module">
import { Editor } from 'https://esm.sh/@tiptap/core'
import StarterKit from 'https://esm.sh/@tiptap/starter-kit'

new Editor({
  element: document.querySelector('#editor'),
  extensions: [StarterKit],
  content: '<p>Comeza a escribir aquí...</p>',
})
</script>
```

---

### ✅ Boas prácticas esenciales

1. **Accesibilidade**:
   ```html
   <div class="form-group">
     <label for="comentario">Comentario:</label>
     <textarea 
       id="comentario" 
       aria-describedby="ayuda-comentario"
     ></textarea>
     <small id="ayuda-comentario">Máximo 500 caracteres</small>
   </div>
   ```

2. **Validación integrada**:
   ```html
   <textarea 
     required 
     minlength="50" 
     maxlength="500"
     data-validation="Debe ter entre 50 e 500 caracteres"
   ></textarea>
   ```

3. **Seguridade**:
   - Sanitice sempre o contido con librarías como [DOMPurify](https://github.com/cure53/DOMPurify)
   ```javascript
   import DOMPurify from 'dompurify';
   const cleanHTML = DOMPurify.sanitize(userContent);
   ```

---

### 📚 Recursos adicionais
- [Guía MDN sobre textarea](https://developer.mozilla.org/gl/docs/Web/HTML/Element/textarea)
- [Patróns de deseño para formularios](https://www.smashingmagazine.com/guides/form-design/)
- [Validación avanzada con JavaScript](https://web.dev/learn/forms/validation)


---

DAW🧊2025

#html
#DAW