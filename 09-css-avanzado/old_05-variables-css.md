# **Lista ampliada de consideracións e recursos**:

---

### 1. **Accesibilidade Avanzada**
   - **Etiquetas semánticas**: 
     ```html
     <!-- Boa práctica -->
     <label for="email">Email:</label>
     <input type="email" id="email" aria-describedby="email-help">
     <small id="email-help">Formato: usuario@dominio.gal</small>
     ```
   - **ARIA Roles**: 
     ```html
     <div role="alert" id="erro-mensaxe"></div>
     ```
   - **Navegación por teclado**: Garantir que `tabindex` está configurado correctamente.
   - **Recursos**:
     - [WAI-ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/)
     - [WebAIM: Formularios Accesibles](https://webaim.org/techniques/forms/)

---

### 2. **Seguridade**
   - **CSRF (Cross-Site Request Forgery)**:
     ```html
     <!-- Incluír token en formularios -->
     <input type="hidden" name="csrf_token" value="token_valor">
     ```
   - **Sanitización de datos**: Limpar entradas no backend (ex: [DOMPurify](https://github.com/cure53/DOMPurify)).
   - **HTTPS**: Envío de datos cifrados.

---

### 3. **Deseño Responsivo**
   - **Touch targets**:
     ```css
     input, button {
       min-height: 44px; /* Tamaño mínimo para toque */
     }
     ```
   - **Media queries**:
     ```css
     @media (max-width: 768px) {
       form { padding: 1rem; }
     }
     ```

---

### 4. **Melloras con JavaScript**
   - **Validación en tempo real**:
     ```javascript
     document.querySelector('input[name="usuario"]').addEventListener('input', function(e) {
       // Validación dinámica
     });
     ```
   - **Subida de arquivos con AJAX**:
     ```javascript
     const formData = new FormData(formulario);
     fetch('/upload', { method: 'POST', body: formData });
     ```

---

### 5. **Validacións Adicionais**
   - **Server-Side Validation** (exemplo en PHP):
     ```php
     if (!filter_var($_POST['email'], FILTER_VALIDATE_EMAIL)) {
       die("Email inválido");
     }
     ```
   - **Librarías de validación**:
     - [Validator.js](https://github.com/validatorjs/validator.js)
     - [Yup](https://github.com/jquense/yup)

---

### 6. **UX (Experiencia de Usuario)**
   - **Mensaxes de erro/success**:
     ```html
     <div class="feedback feedback--exito">Rexistro exitoso!</div>
     <div class="feedback feedback--erro" role="alert">Erro no email.</div>
     ```
   - **Carga e retroalimentación**:
     ```javascript
     formulario.addEventListener('submit', () => {
       botonSubmit.textContent = 'Enviando...';
     });
     ```

---

### 7. **Técnicas Modernas**
   - **Web Components para formularios**:
     ```html
     <custom-input label="Nome" type="text"></custom-input>
     ```
   - **APIs nativas**:
     - [FormData API](https://developer.mozilla.org/gl/docs/Web/API/FormData)
     - [Constraint Validation API](https://developer.mozilla.org/gl/docs/Web/API/Constraint_validation)

---

### 8. **Protección contra Spam**
   - **CAPTCHAs**:
     ```html
     <div class="g-recaptcha" data-sitekey="chave_publica"></div>
     ```
   - **Honeypot**:
     ```html
     <input type="text" name="url" style="display: none;">
     ```

---

### 9. **Ferramentas de Depuración**
   - **Consola do navegador**:
     ```javascript
     console.log(formulario.checkValidity()); // Verificar validación
     ```
   - **Ferramentas**:
     - [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview/) (accesibilidade/performance)
     - [axe DevTools](https://www.deque.com/axe/devtools/) (test de accesibilidade)

---

### 10. **Recursos de Referencia**
   - **Documentación**:
     - [MDN Web Docs - Formularios](https://developer.mozilla.org/gl/docs/Web/HTML/Element/form)
     - [HTML5 Pattern Examples](https://htmlpattern.com/)
   - **Cursos**:
     - [FreeCodeCamp - Formularios Accesibles](https://www.freecodecamp.org/news/learn-accessible-html/)
     - [Frontend Masters - Formularios Profesionais](https://frontendmasters.com/courses/forms/)

---

### Conclusión
Un formulario ben implementado combina:  
✅ **Semántica HTML** + 🛡️ **Seguridade** + ♿ **Accesibilidade** + 📱 **Responsividade** + 🛠️ **Validacións robustas**.  
Invertir tempo en estes aspectos asegura formularios eficientes, seguros e inclusivos.

### Exemplos

Vou proporcionar exemplos prácticos que integran múltiples conceptos avanzados. Cada exemplo inclúe comentarios sobre as características clave:

---

### 1. **Formulario de Rexistro con Validacións e Accesibilidade**
```html
<form id="rexistro" novalidate aria-labelledby="titulo-rexistro">
  <h2 id="titulo-rexistro">Rexistro de Usuario</h2>
  
  <!-- Campo: Nome -->
  <div class="campo">
    <label for="nome">Nome completo*</label>
    <input type="text" 
           id="nome" 
           name="nome"
           required
           minlength="3"
           aria-describedby="axuda-nome">
    <small id="axuda-nome" class="axuda">Mínimo 3 caracteres</small>
  </div>

  <!-- Campo: Email -->
  <div class="campo">
    <label for="email">Email*</label>
    <input type="email" 
           id="email" 
           name="email"
           required
           pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$"
           aria-describedby="axuda-email">
    <small id="axuda-email" class="axuda">Formato válido: usuario@dominio.gal</small>
  </div>

  <!-- Campo: Contrasinal -->
  <div class="campo">
    <label for="contrasinal">Contrasinal*</label>
    <input type="password" 
           id="contrasinal" 
           name="contrasinal"
           required
           minlength="8"
           aria-describedby="axuda-contrasinal">
    <div id="axuda-contrasinal" class="axuda">
      <progress id="forza-contrasinal" max="4"></progress>
      <span>Mínimo 8 caracteres</span>
    </div>
  </div>

  <!-- Protección anti-spam (Honeypot) -->
  <div class="hp" style="position: absolute; left: -9999px;">
    <label for="url">Deixe isto en branco</label>
    <input type="text" id="url" name="url">
  </div>

  <!-- CSRF Token (Exemplo con PHP) -->
  <input type="hidden" name="csrf_token" value="<?= $_SESSION['token'] ?>">

  <button type="submit" aria-busy="false">Rexistrarse</button>
</form>

<script>
// Validación en tempo real
document.getElementById('contrasinal').addEventListener('input', function(e) {
  const strength = Math.min(e.target.value.length / 2, 4);
  document.getElementById('forza-contrasinal').value = strength;
});

// Envío con Fetch API
document.getElementById('rexistro').addEventListener('submit', async (e) => {
  e.preventDefault();
  const boton = e.target.querySelector('button[type="submit"]');
  boton.setAttribute('aria-busy', 'true');
  
  try {
    const response = await fetch('/rexistro', {
      method: 'POST',
      body: new FormData(e.target)
    });
    
    if (!response.ok) throw new Error();
    mostrarMensaxe('Éxito! Revisa o teu email.');
  } catch {
    mostrarMensaxe('Erro! Inténtao de novo.', 'erro');
  } finally {
    boton.removeAttribute('aria-busy');
  }
});
</script>

<style>
/* Estilos Responsivos */
@media (max-width: 768px) {
  .campo { grid-template-columns: 1fr; }
}

/* Accesibilidade */
[aria-invalid="true"] { border-color: #c00; }
.axuda { font-size: 0.875rem; }

/* UX */
[aria-busy="true"]::after {
  content: '';
  display: inline-block;
  width: 1em;
  height: 1em;
  border: 2px solid currentColor;
  border-radius: 50%;
  border-right-color: transparent;
  animation: spin 1s linear infinite;
}

@keyframes spin { to { transform: rotate(360deg); } }
</style>
```

**Características destacadas:**  
✅ Validación HTML5 + JavaScript  
✅ Accesibilidade (ARIA, etiquetas)  
✅ Protección (CSRF, Honeypot)  
✅ UX (Loading state, mensaxes)  
✅ Responsividade  
✅ Sanitización no backend (non mostrado)

---

### 2. **Formulario de Contacto con Subida de Arquivos**
```html
<form id="contacto" enctype="multipart/form-data">
  <!-- Campo: arquivos -->
  <div class="campo">
    <label for="arquivo">Anexar documento (PDF, máx. 5MB)</label>
    <input type="file" 
           id="arquivo" 
           name="arquivo"
           accept=".pdf"
           data-max-size="5242880">
    <div class="axuda-validacion"></div>
  </div>

  <!-- Validación en JavaScript -->
  <script>
document.getElementById('arquivo').addEventListener('change', function(e) {
  const maxSize = parseInt(e.target.dataset.maxSize);
  if (e.target.files[0].size > maxSize) {
    e.target.setCustomValidity('O arquivo é demasiado grande');
    e.target.reportValidity();
  } else {
    e.target.setCustomValidity('');
  }
});
  </script>
</form>
```

**Características:**  
✅ Límite de tamaño de arquivo  
✅ Tipo específico (PDF)  
✅ Mensaxes personalizadas

---

### 3. **Formulario de Pagamento con Web Components**
```html
<credit-card-form>
  <div class="tarxeta">
    <card-number 
      label="Número da tarxeta" 
      required 
      pattern="\d{16}"
    ></card-number>
    <card-expiry 
      label="Caducidade (MM/AA)" 
      required 
      pattern="(0[1-9]|1[0-2])\/\d{2}"
    ></card-expiry>
  </div>
</credit-card-form>

<script>
// Exemplo de Web Component
class CardNumber extends HTMLElement {
  connectedCallback() {
    this.innerHTML = `
      <input type="text" 
             inputmode="numeric" 
             placeholder="0000 0000 0000 0000"
             maxlength="19"
             pattern="${this.getAttribute('pattern')}">
    `;
  }
}
customElements.define('card-number', CardNumber);
</script>
```

**Características:**  
✅ Web Components reutilizables  
✅ Inputmode para teclado numérico  
✅ Patróns específicos

---

### 4. **Formulario de Enquisa con Validacións Complexas**
```html
<form id="enquisa">
  <div class="campo">
    <label>Valora o noso servizo (1-5)</label>
    <input type="range" 
           name="valoracion" 
           min="1" 
           max="5" 
           step="1"
           data-list="mala regular boa moi_boa excelente">
    <datalist id="valoracion-labels">
      <option value="1" label="Mala"></option>
      <option value="2" label="Regular"></option>
      <option value="3" label="Boas"></option>
      <option value="4" label="Moi boas"></option>
      <option value="5" label="Excelente"></option>
    </datalist>
  </div>

  <script>
// Validación personalizada
document.querySelector('input[type="range"]').addEventListener('input', (e) => {
  if (e.target.value < 3) {
    e.target.setCustomValidity('Por favor, deixa un comentario');
  } else {
    e.target.setCustomValidity('');
  }
});
  </script>
</form>
```

**Características:**  
✅ Range con etiquetas semánticas  
✅ Validación condicional  
✅ Integración con `<datalist>`

---

### 5. **Formulario de Login con Autocompletado Seguro**
```html
<form id="login" method="post" action="/login">
  <div class="campo">
    <label for="email-login">Email</label>
    <input type="email" 
           id="email-login" 
           name="email"
           autocomplete="username"
           required>
  </div>

  <div class="campo">
    <label for="contrasinal-login">Contrasinal</label>
    <input type="password" 
           id="contrasinal-login" 
           name="contrasinal"
           autocomplete="current-password"
           required>
  </div>

  <security-check 
    difficulty="medium" 
    sitekey="tu_clave_publica"
  ></security-check>
</form>
```

**Características:**  
✅ Autocompletado de navegador seguro  
✅ Componente de seguridade reutilizable  
✅ Validación en 2 pasos

---

**Notas finais:**  
- Todos os exemplos deben combinarse con validacións no servidor  
- Usar ferramentas como Lighthouse para probar accesibilidade  
- Considerar sempre o RGPD en formularios con datos persoais  
- Adaptar estes patróns ás necesidades específicas do proxecto

:eye: Estes exemplos serven como punto de partida para formularios profesionais e seguros. Cada caso de uso pode requerir adaptacións adicionais.

:tada:

---

DAW🧊2025

#html
#DAW