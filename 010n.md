# A etiqueta `<input>` e os arquivos

A etiqueta `<input type="file">` permite aos usuarios **cargar arquivos** a través dun formulario. Esta funcionalidade é esencial para:

- Subida de imaxes de perfil  
- Envío de documentos en formularios de contacto  
- Carga de arquivos en ferramentas de administración  

### Configuración básica

```html
<form method="post" action="/procesar" enctype="multipart/form-data">
  <label for="arquivo">Selecciona un arquivo:</label>
  <input type="file" id="arquivo" name="arquivo_usuario">
</form>
```

**Atributos clave do formulario:**  
| Atributo    | Valor                   | Descrición                          |
|-------------|-------------------------|--------------------------------------|
| `enctype`   | `multipart/form-data`   | Permite envío de arquivos (obrigatorio) |
| `method`    | `post`                  | Único método compatible con arquivos |

### 🔒 Restrinxir tipos de arquivos

Use o atributo `accept` para suxerir formatos específicos:

```html
<input type="file" accept=".pdf,.docx,image/*">
```

**Exemplos de tipos MIME comúns:**  
| Categoría   | Tipo MIME               | Extensións              |
|-------------|-------------------------|-------------------------|
| Imaxes      | `image/jpeg`            | .jpeg, .jpg             |
| Documentos  | `application/pdf`       | .pdf                    |
| Vídeos      | `video/mp4`             | .mp4                    |
| Comprimidos | `application/zip`       | .zip                    |

> 💡 Consulte a [lista completa de tipos MIME](https://developer.mozilla.org/gl/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types) en MDN.

### Carga múltiple de arquivos

Permita selección múltiple co atributo `multiple`:

```html
<input type="file" multiple accept="image/*">
```

**Boas prácticas:**  
- Limite o número máximo de arquivos con JavaScript  
- Indique restricións de tamaño no texto de axuda  
- Valide sempre os arquivos no servidor

---

## Organización de campos no formulario

### Agrupación con `<fieldset>` e `<legend>`

Estrutura visual e semántica para seccións relacionadas:

```html
<form method="post" action="/rexistro">
  <fieldset>
    <legend>Datos persoais</legend>
    
    <div class="campo">
      <label for="nome">Nome completo:</label>
      <input type="text" id="nome" required>
    </div>

    <div class="campo">
      <label for="nacemento">Data de nacemento:</label>
      <input type="date" id="nacemento">
    </div>
  </fieldset>

  <fieldset>
    <legend>Preferencias</legend>
    
    <div class="campo">
      <label>
        <input type="checkbox" name="notificacions"> Recibir notificacións
      </label>
    </div>
  </fieldset>
</form>
```

**Estilización CSS recomendada:**  
```css
fieldset {
  border: 2px solid #4CAF50;
  border-radius: 8px;
  margin: 1rem 0;
  padding: 1rem;
}

legend {
  color: #2E7D32;
  font-weight: bold;
  padding: 0 0.5rem;
}
```

### Accesibilidade e navegación

**Orde de tabulación:**  
```html
<input type="text" tabindex="1"> <!-- Primeiro en focus -->
<input type="email" tabindex="2">
<button type="submit" tabindex="3">Enviar</button>
```

**Consellos:**  
- Use `tabindex="0"` para elementos non interactivos que deban ser enfocados  
- Evite valores negativos de `tabindex`  
- Valide a orde con [ferramentas de accesibilidade](https://wave.webaim.org/)

### 🏿 Etiquetas accesibles

Mellor práctica para asociar etiquetas:

```html
<div class="campo">
  <label for="correo">Correo electrónico:</label>
  <input type="email" id="correo" aria-describedby="axuda-correo">
  <small id="axuda-correo">Exemplo: usuario@dominio.gal</small>
</div>
```

---

## Recursos adicionais

1. [Guía completa de formularios HTML - MDN](https://developer.mozilla.org/gl/docs/Learn/Forms)  
2. [Patróns de deseño accesíbeis - W3C](https://www.w3.org/WAI/ARIA/apg/patterns/)  
3. [Validación de arquivos con JavaScript](https://web.dev/learn/forms/file-upload/)

---

**Notas finais:**  
- Sempre valide os arquivos no servidor, incluso con restricións no cliente  
- Considere usar [FilePond](https://pqina.nl/filepond/) para UX mellorado  
- Limite tamaños de arquivo con `max-file-size` en combinación co servidor


---

DAW🧊2025

#html
#DAW