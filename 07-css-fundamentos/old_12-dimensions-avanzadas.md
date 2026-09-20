## A etiqueta `<select>`

A etiqueta `<select>` permíte crear **listas despregables** ou **cuadros combinados** para selección múltiple ou única. É ideal para formularios con moitas opcións onde os botóns radio ou checkboxes resultarían pouco prácticos.

### Uso básico

```html
<form method="post" action="/procesar">
  <label for="cursos">Escolle un curso:</label>
  <select id="cursos" name="curso">
    <option value="1">Introdución a HTML</option>
    <option value="2">CSS Avanzado</option>
    <option value="3">JavaScript Moderno</option>
  </select>
</form>
```

#### Atributos clave:
- `multiple`: Permite selección múltiple
- `size`: Número de opcións visíbeis sen despregar
- `required`: Validación de campo obrigatorio

### 🛠️ Funcionalidades avanzadas

#### 1. Agrupación de opcións con `<optgroup>`
```html
<select name="coches">
  <optgroup label="Alemáns">
    <option value="bmw">BMW</option>
    <option value="audi">Audi</option>
  </optgroup>
  <optgroup label="Xaponeses" disabled>
    <option value="toyota">Toyota</option>
    <option value="honda">Honda</option>
  </optgroup>
</select>
```

#### 2. Selección múltiple
```html
<select name="linguas" multiple size="4">
  <option value="gl">Galego</option>
  <option value="es">Castelán</option>
  <option value="en">Inglés</option>
</select>
```

#### 3. Valores predeterminados e desactivados
```html
<select name="tipo_usuario">
  <option selected disabled>-Escolle rol-</option>
  <option value="admin">Administrador</option>
  <option value="editor">Editor</option>
</select>
```

### 🎨 Personalización con CSS

#### Estilización básica:
```css
select {
  width: 100%;
  padding: 12px;
  border: 2px solid #4CAF50;
  border-radius: 8px;
  background: #f8f8f8;
  font-family: 'Open Sans', sans-serif;
  appearance: none; /* Elimina estilos por defecto */
  background-image: url('data:image/svg+xml;utf8,<svg ...></svg>');
  background-repeat: no-repeat;
  background-position: right 1rem center;
}
```

#### Selector moderno con degradado:
```css
.custom-select {
  background: linear-gradient(45deg, #f3f4f6, #e5e7eb);
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
}

.custom-select:hover {
  border-color: #3B82F6;
  box-shadow: 0 4px 8px rgba(59,130,246,0.2);
}
```

### 🔍 Boas prácticas de accesibilidade

1. **Asociar sempre etiquetas:**
   ```html
   <label for="menu-linguas">Idioma preferido:</label>
   <select id="menu-linguas" name="lingua">
     <!-- Opcións -->
   </select>
   ```

2. **Usar atributos ARIA:**
   ```html
   <div role="listbox" aria-label="Lista de países">
     <!-- Opcións -->
   </div>
   ```

3. **Navegación por teclado:**
   - `Tab`: Move entre elementos
   - `↑/↓`: Selecciona opcións
   - `Espazo`: Abre/pecha lista

### 📚 Recursos recomendados

1. [Guía MDN sobre `<select>`](https://developer.mozilla.org/gl/docs/Web/HTML/Element/select)
2. [Patróns de deseño accesíbeis](https://www.w3.org/WAI/ARIA/apg/patterns/listbox/)
3. [Bibliotecas para selects avanzados](https://select2.org/)

---

### 💡 Consellos avanzados

1. **Integración con JavaScript:**
   ```javascript
   const selector = document.querySelector('select');
   
   selector.addEventListener('change', (e) => {
     console.log(`Opción seleccionada: ${e.target.value}`);
   });
   ```

2. **Validación en tempo real:**
   ```html
   <select required oninvalid="this.setCustomValidity('Selecciona unha opción válida')">
     <!-- Opcións -->
   </select>
   ```

3. **Carga dinámica de opcións:**
   ```javascript
   fetch('/api/cursos')
     .then(response => response.json())
     .then(data => {
       const select = document.getElementById('cursos');
       data.forEach(curso => {
         select.innerHTML += `<option value="${curso.id}">${curso.nome}</option>`;
       });
     });
   ```

---

DAW🧊2025

#html
#DAW