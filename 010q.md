# Os modos de envío

**Os botóns de envío de formularios** son elementos cruciais na creación de formularios. Aínda que un formulario pode funcionar sen eles (usando a tecla Enter), é recomendable incluír botóns explícitos para unha experiencia de usuario clara.

### Tipos de botóns

| Tipo de botón              | Etiqueta                       | Uso recomendado               |
|----------------------------|--------------------------------|--------------------------------|
| Envío estándar             | `<input type="submit">`        | Envío principal                |
| Envío con imaxe            | `<input type="image">`         | Botóns gráficos personalizados |
| Restablecer formulario     | `<input type="reset">`         | Limpar campos                  |
| Botón xenérico             | `<button>` ou `<input type="button">` | Accións personalizadas |

### 1. Botón de envío estándar

```html
<form method="post" action="/procesar">
  <label>
    Nome de usuario:
    <input name="usuario">
  </label>
  <input type="submit" value="Gardar datos">
</form>
```

**Características:**  
- Texto personalizable co atributo `value`  
- Activa validacións HTML5 automáticas  
- Envía todos os datos do formulario  

### 2. Botón de envío con imaxe

```html
<form method="post" action="/upload">
  <input type="file" name="arquivo">
  
  <input 
    type="image" 
    src="enviar-icono.svg" 
    alt="Enviar arquivo"
    width="40"
    height="40"
  >
</form>
```

**Consellos:**  
- Usar formatos vectoriais (SVG) para mellor escalabilidade  
- Proporcionar texto alternativo accesible  
- Definir tamaño explícito para evitar saltos no deseño  

### 3. Botón de restablecemento

```html
<form id="formulario-rexistro">
  <label>
    Correo electrónico:
    <input type="email" required>
  </label>
  
  <div class="grupo-botons">
    <input type="submit" value="Rexistrarse">
    <input type="reset" value="Limpar campos">
  </div>
</form>
```

**Boas prácticas:**  
- Separar visualmente do botón de envío  
- Usar etiquetas descritivas  
- Considerar confirmación JavaScript para datos importantes  

### 4. Botóns personalizados

#### Con `<button>`
```html
<button type="button" class="btn-especial">
  <img src="icono-favorito.svg" alt="">
  Gardar como favorito
</button>

<script>
document.querySelector('.btn-especial').addEventListener('click', () => {
  // Lóxica personalizada aquí
});
</script>
```

**Vantaxes:**  
- Permite contido HTML interno (texto, imaxes, íconos)  
- Máis flexible para estilización CSS  
- Ideal para accións non relacionadas con envíos  

### Métodos de envío

**Métodos de envío de formularios HTML: `GET` vs `POST`**

Os formularios HTML utilizan dous métodos principais para enviar datos: **`GET`** e **`POST`**. Cada un ten características específicas e úsase en función do tipo de datos e a seguridade requirida. Aquí tes unha comparativa clara:

---

### **1. Método `GET`**
- **Como funciona**:  
  Os datos **engádense á URL** como parámetros (ex: `?usuario=Ana&idade=30`).  
- **Características**:  
  - **Visibilidade**: Os datos son públicos e quedan no historial do navegador.  
  - **Límite de tamaño**: Aproximadamente **2048 caracteres** (depende do navegador).  
  - **Uso típico**: Buscas, filtros, ou cando queres que a URL sexa compartible.  
  - **Non modificador**: Ideal para operacións que **non alteran datos** no servidor.  

**Exemplo**:  
```html  
<form method="GET" action="/busca">  
  <input type="text" name="termo">  
  <button>Buscar</button>  
</form>  
```
URL resultante: `/busca?termo=accesibilidade`.

---

### **2. Método `POST`**
- **Como funciona**:  
  Os datos **envíanse no corpo da solicitude HTTP**, non na URL.  
- **Características**:  
  - **Seguridade**: Máis seguro para datos sensibles (ex: contrasinais).  
  - **Sen límite de tamaño**: Adecuado para enviar arquivos ou textos longos.  
  - **Uso típico**: Rexistros, logins, envío de arquivos, ou calquera operación que **modifique datos** no servidor.  

**Exemplo**:  
```html  
<form method="POST" action="/rexistro">  
  <input type="text" name="nome">  
  <input type="password" name="contrasinal">  
  <button>Rexistrarse</button>  
</form>  
```

---

### **Diferenzas clave**  
| **Característica**      | **`GET`**                              | **`POST`**                                    |
| ----------------------- | -------------------------------------- | --------------------------------------------- |
| **Visibilidade**        | Datos na URL (públicos).               | Datos ocultos (corpo HTTP).                   |
| **Seguridade**          | Non seguro para datos sensibles.       | Máis seguro (se usa con HTTPS).               |
| **Tamaño máximo**       | Limitado (~2048 caracteres).           | Sen límite práctico.                          |
| **Uso recomendado**     | Consultas, filtros, URLs compartibles. | Datos privados, modificacións en BD.          |
| **Efectos secundarios** | Non debe cambiar datos no servidor.    | Pode cambiar datos (ex: gardar unha entrada). |

---

### **Boas prácticas**  
1. **Usa `POST` para**:  
   - Datos sensibles (contrasinais, información persoal).  
   - Operacións que modifican datos (ex: enviar un comentario).  
   - Subir arquivos (usa `enctype="multipart/form-data"`).  

2. **Usa `GET` para**:  
   - Compartir URLs con parámetros (ex: resultados de busca).  
   - Recuperar datos sen modificar o servidor.  

3. **HTTPS sempre**: Garante a seguridade dos datos, especialmente con `POST`.  

---

### **Outros métodos (non soportados en formularios HTML estándar)**  
- **`PUT`**, **`DELETE`**, **`PATCH`**: Usados en APIs RESTful, pero requiren JavaScript (ex: `fetch` ou `XMLHttpRequest`).  

---

**Resumo final**:  
- **`GET`**: Visible, limitado, ideal para consultas.  
- **`POST`**: Oculto, seguro, ideal para datos críticos.  

Escolle o método segundo a natureza dos datos e a operación que realizas 😊.

## Envíos avanzados

### Múltiples destinos de envío

```html
<form method="POST" action="/base">
  <label>
    Comentario:
    <textarea name="comentario"></textarea>
  </label>
  
  <button 
    type="submit"
    formaction="/backup"
    formmethod="get"
    formtarget="_blank"
  >
    Gardar borrador
  </button>
  
  <button 
    type="submit"
    formaction="/publicar"
  >
    Publicar agora
  </button>
</form>
```

**Atributos clave:**  
- `formaction`: URL alternativa para o envío  
- `formmethod`: Cambiar método HTTP (GET/POST)  
- `formtarget`: Controlar onde abrir a resposta  

### Estilización con CSS Moderno

```css
.btn-galego {
  --cor-primaria: #005792;
  --cor-secundaria: #003459;
  
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  background: linear-gradient(var(--cor-primaria), var(--cor-secundaria));
  color: white;
  font-family: 'Open Sans', sans-serif;
  cursor: pointer;
  transition: transform 0.2s, box-shadow 0.2s;
  
  &:hover {
    box-shadow: 0 4px 12px rgba(0,87,146,0.3);
    transform: translateY(-2px);
  }
  
  &:active {
    transform: translateY(1px);
  }
  
  &[disabled] {
    opacity: 0.6;
    cursor: not-allowed;
  }
}
```

```html
<button class="btn-galego" type="submit">
  Enviar enquisa
</button>
```

---

## Recursos adicionais

1. [Guía MDN sobre formularios](https://developer.mozilla.org/gl/docs/Learn/Forms)  
2. [Patróns ARIA para botóns](https://www.w3.org/WAI/ARIA/apg/patterns/button/)  
3. [Deseño responsivo de botóns](https://css-tricks.com/a-complete-guide-to-links-and-buttons/)  

---

**Consellos clave:**  
- Validar sempre datos no servidor ademais do cliente  
- Usar `aria-label` para botóns só con íconos  
- Probar en múltiples dispositivos e navegadores  
- Considerar efectos de transición para feedback visual  

---

DAW🧊2026

#html
#DAW