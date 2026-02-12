## A etiqueta `<datalist>`

A etiqueta `<datalist>` permite crear **listas de suxestións personalizadas** para campos de formulario, combinando a flexibilidade dun `<input>` de texto coas opcións predefinidas dun `<select>`. É ideal para:

- Búsquedas con autocompletado  
- Seleccións con opcións personalizábeis  
- Mostrar valores suxeridos mantendo a liberdade de entrada  

### Uso básico

```html
<label for="buscador">Buscar tutoriales:</label>
<input 
  type="text" 
  id="buscador" 
  list="suxestions"
  placeholder="Escribe un tema..."
>
<datalist id="suxestions">
  <option value="HTML">
  <option value="CSS Grid">
  <option value="Flexbox">
  <option value="JavaScript Moderno">
</datalist>
```

**Características principais:**  
- Conéctase ao campo mediante o atributo `list`  
- Filtra opcións segundo o texto introducido  
- Compatible con múltiples tipos de `<input>`

### 🔧 Exemplos avanzados

#### 1. Selector numérico con marcas
```html
<label for="valoracion">Valoración (1-5 estrelas):</label>
<input 
  type="range" 
  id="valoracion" 
  list="marcas"
  min="1" 
  max="5" 
  step="1"
>
<datalist id="marcas">
  <option value="1" label="😞"></option>
  <option value="2" label="😐"></option>
  <option value="3" label="😊"></option>
  <option value="4" label="😃"></option>
  <option value="5" label="🤩"></option>
</datalist>
```

#### 2. Datas destacadas
```html
<label for="evento">Data do evento:</label>
<input 
  type="date" 
  id="evento" 
  list="datas-destacadas"
>
<datalist id="datas-destacadas">
  <option value="2024-07-25" label="Día Nacional de Galicia"></option>
  <option value="2024-09-23" label="Equinoccio de outono"></option>
</datalist>
```

#### 3. Paleta de cores corporativas
```html
<label for="cor-fondo">Escolle unha cor de fondo:</label>
<input 
  type="color" 
  id="cor-fondo" 
  list="cores-galegas"
>
<datalist id="cores-galegas">
  <option value="#6B8E23" label="Verde Galego"></option>
  <option value="#4169E1" label="Azul Atlántico"></option>
  <option value="#F4A460" label="Ouro Vieiro"></option>
</datalist>
```

### 🛠️ Integración con JavaScript

Amplía funcionalidades con interacción dinámica:

```html
<input type="text" id="cidade" list="cidades-galegas">
<datalist id="cidades-galegas"></datalist>

<script>
// Carga dinámica de opcións
const cidades = ['A Coruña', 'Santiago', 'Vigo', 'Ourense', 'Lugo'];
const datalist = document.getElementById('cidades-galegas');

cidades.forEach(cidade => {
  const option = document.createElement('option');
  option.value = cidade;
  datalist.appendChild(option);
});
</script>
```

### 📌 Boas prácticas

1. **Accesibilidade:**
   ```html
   <input 
     aria-describedby="axuda-datalist" 
     aria-label="Busca de contidos"
   >
   <div id="axuda-datalist" hidden>
     Preme para ver suxestións de búsqueda
   </div>
   ```

2. **Validación:**
   ```html
   <input 
     type="text" 
     list="opcions-validas" 
     pattern="Opción 1|Opción 2|Opción 3"
     required
   >
   ```

3. **Estilización CSS:**
   ```css
   input[list] {
     padding: 0.8rem;
     border: 2px solid #4CAF50;
     border-radius: 8px;
     transition: border-color 0.3s ease;
   }

   input[list]:focus {
     border-color: #2196F3;
     box-shadow: 0 0 8px rgba(33,150,243,0.2);
   }
   ```

### 📚 Recursos adicionais
- [Documentación MDN sobre `<datalist>`](https://developer.mozilla.org/gl/docs/Web/HTML/Element/datalist)  
- [Guía de formularios accesíbeis](https://www.w3.org/WAI/tutorials/forms/)  
- [Patróns de deseño para búsquedas](https://www.smashingmagazine.com/2021/11/modern-javascript-datalist-element/)  

---

**Notas clave:**  
- Funciona con: `text`, `search`, `url`, `email`, `number`, `date`, `color`  
- Non compatible con: `password`, `file`, `hidden`  
- Para navegadores antigos, considerar [polyfills](https://github.com/mfranzke/datalist-polyfill)  

---

DAW🧊2025

#html
#DAW