# Elementos de Formulario

Máis alá do básico `<input>`, HTML5 ofrece unha gran variedade de elementos para recoller diferentes tipos de información.

---

## 1. Textos longos (`<textarea>`)

Cando necesitas que o usuario escriba máis dunha liña (como un comentario ou unha bio).
```html
<label for="comentarios">A túa mensaxe:</label>
<textarea id="comentarios" name="mensaxe" rows="4" cols="50"></textarea>
```

---

## 2. Listas de selección (`<select>`)

Permite ao usuario escoller unha ou varias opcións dunha lista despregable.
```html
<label for="pais">País:</label>
<select id="pais" name="pais">
  <option value="gl">Galicia</option>
  <option value="pt">Portugal</option>
  <option value="fr">Francia</option>
</select>
```

---

## 3. Mensaxes de axuda e suxestións (`<datalist>`)

Ofrece unha lista de opcións recomendadas sen impedir que o usuario escriba o que queira.
```html
<input list="navegadores" name="navegador">
<datalist id="navegadores">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Safari">
</datalist>
```

---

## 4. Botóns (`<button>`)

Máis flexibles que o vello `<input type="submit">`, xa que poden conter etiquetas HTML dentro (como iconas).

---

## 5. Organización con `<fieldset>`

Axuda a agrupar campos relacionados visual e semanticamente.
```html
<fieldset>
  <legend>Datos de Envío</legend>
  <!-- Campos aquí -->
</fieldset>
```

---

**Resumo**:
Escoller o elemento correcto mellora a usabilidade. Usa `<select>` para opcións pechadas e `<textarea>` para textos libres longos.

---

DAW🧊2026