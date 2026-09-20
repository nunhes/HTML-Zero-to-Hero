# Formularios HTML: exercicio práctico

---

## 1. O papel do elemento `form`

O elemento `<form>` en HTML é o contedor principal para todos os controis dun formulario. Permite aos usuarios introducir datos que poden ser enviados a un servidor para procesamento. O formulario é esencial para interactuar co usuario, como en rexistros, inicios de sesión, enquisas, etc.

- **Atributos importantes**:
  - **`action`**: Especifica a URL onde se enviarán os datos do formulario.
  - **`method`**: Define o método HTTP para enviar os datos (xeralmente `GET` ou `POST`).
  - **`enctype`**: Especifica como se codifican os datos ao enviar o formulario (útil para subidas de arquivos).

Exemplo básico:
```html
<form action="/enviar-datos" method="POST">
  <!-- os elementos do formulario van aquí -->
</form>
```

---

## **2. Usar unha variedade de controis de formulario**

Os formularios HTML inclúen varios tipos de controis para recoller datos do usuario. Aquí tes algúns dos máis comúns:

- **`<input>`**: O control máis común. Pode ter diferentes tipos:
  - `type="text"`: Para texto.
  - `type="password"`: Para contrasinais.
  - `type="email"`: Para correos electrónicos.
  - `type="number"`: Para números.
  - `type="date"`: Para datas.
  - `type="checkbox"`: Para seleccións múltiples.
  - `type="radio"`: Para seleccións únicas.
  - `type="file"`: Para subir arquivos.

- **`<textarea>`**: Para entradas de texto longo.
- **`<select>` e `<option>`**: Para menús despregables.
- **`<button>`**: Para botóns de envío ou accións.

Exemplo:
```html
<form action="/enviar-datos" method="POST">
  <label for="nome">Nome:</label>
  <input type="text" id="nome" name="nome" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="contra">Contrasinal:</label>
  <input type="password" id="contra" name="contra" required>

  <label for="mensaxe">Mensaxe:</label>
  <textarea id="mensaxe" name="mensaxe"></textarea>

  <button type="submit">Enviar</button>
</form>
```

---

## **3. Definir formularios HTML complexos**

Un formulario complexo pode incluír múltiples seccións, agrupacións de campos, e diferentes tipos de controis. Aquí tes algunhas técnicas para crear formularios complexos:

- **`<fieldset>` e `<legend>`**: Agrupa campos relacionados e engade unha lenda descritiva.
- **`<label>`**: Asocia unha etiqueta a un control do formulario para mellorar a accesibilidade.
- **`<datalist>`**: Proporciona suxestións para un campo de entrada.

Exemplo de formulario complexo:
```html
<form action="/enviar-datos" method="POST">
  <fieldset>
    <legend>Información persoal</legend>
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" required>

    <label for="idade">Idade:</label>
    <input type="number" id="idade" name="idade" min="0" max="120">
  </fieldset>

  <fieldset>
    <legend>Preferencias</legend>
    <label for="cor">Cor favorita:</label>
    <input type="color" id="cor" name="cor">

    <label for="comida">Comida favorita:</label>
    <input list="comidas" id="comida" name="comida">
    <datalist id="comidas">
      <option value="Pizza">
      <option value="Sushi">
      <option value="Tacos">
    </datalist>
  </fieldset>

  <button type="submit">Enviar</button>
</form>
```

---

## **4. Engadir validacións de formulario HTML5**

HTML5 introduciu validacións integradas para formularios, o que reduce a necesidade de JavaScript para validacións básicas. Aquí tes algúns exemplos:

- **`required`**: O campo é obrigatorio.
- **`min` e `max`**: Define valores mínimos e máximos para números ou datas.
- **`pattern`**: Valida o campo contra unha expresión regular.
- **`type="email"` ou `type="url"`**: Valida que o campo sexa un correo electrónico ou URL válidos.

Exemplo:
```html
<form action="/enviar-datos" method="POST">
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>

  <label for="telefono">Teléfono:</label>
  <input type="tel" id="telefono" name="telefono" pattern="[0-9]{9}" required>

  <button type="submit">Enviar</button>
</form>
```

---

## **5. Garantir a accesibilidade dos nosos formularios**

A accesibilidade é crucial para que todos os usuarios, incluídos os que usan lectores de pantalla, poidan interactuar cos formularios. Aquí tes algunhas prácticas:

- **Usa `<label>`**: Asocia etiquetas a cada control do formulario.
- **`aria-*`**: Usa atributos ARIA para mellorar a accesibilidade.
- **`tabindex`**: Controla a orde de tabulación para usuarios que navegan con teclado.
- **Mensaxes de erro claras**: Proporciona mensaxes de erro accesibles para validacións.

Exemplo accesible:
```html
<form action="/enviar-datos" method="POST">
  <label for="usuario">Usuario:</label>
  <input type="text" id="usuario" name="usuario" required aria-describedby="usuario-error">
  <span id="usuario-error" style="color: red;" aria-live="assertive"></span>

  <button type="submit">Enviar</button>
</form>
```

---

## **Exercicio práctico**

#### **Obxectivo**
Crear un formulario HTML complexo que inclúa varios tipos de controis, validacións HTML5 e sexa accesible.

#### **Instrucións**
1. **Crea un formulario** para rexistrar usuarios nunha web. Debe incluír:
   - Nome completo (obrigatorio).
   - Correo electrónico (obrigatorio e validado).
   - Contrasinal (obrigatorio, mínimo 8 caracteres).
   - Data de nacemento (obrigatoria, formato de data).
   - Xénero (selección única con radio buttons).
   - Intereses (selección múltiple con checkboxes).
   - Comentarios (área de texto).

2. **Engade validacións HTML5**:
   - Todos os campos obrigatorios deben estar marcados.
   - O correo electrónico debe ser válido.
   - O contrasinal debe ter un mínimo de 8 caracteres.

3. **Garante a accesibilidade**:
   - Usa `<label>` para todos os controis.
   - Engade mensaxes de erro accesibles para validacións.

4. **Proba o formulario**:
   - Asegúrate de que funciona correctamente e que as validacións se aplican.

#### **Exemplo de solución**

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Formulario de Rexistro</title>
</head>
<body>
  <h1>Rexistro de Usuario</h1>
  <form action="/rexistro" method="POST">
    <fieldset>
      <legend>Información persoal</legend>
      <label for="nome">Nome completo:</label>
      <input type="text" id="nome" name="nome" required aria-describedby="nome-error">
      <span id="nome-error" style="color: red;" aria-live="assertive"></span>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required aria-describedby="email-error">
      <span id="email-error" style="color: red;" aria-live="assertive"></span>

      <label for="contra">Contrasinal:</label>
      <input type="password" id="contra" name="contra" minlength="8" required aria-describedby="contra-error">
      <span id="contra-error" style="color: red;" aria-live="assertive"></span>

      <label for="data">Data de nacemento:</label>
      <input type="date" id="data" name="data" required aria-describedby="data-error">
      <span id="data-error" style="color: red;" aria-live="assertive"></span>
    </fieldset>

    <fieldset>
      <legend>Xénero</legend>
      <label>
        <input type="radio" name="xenero" value="home" required> Home
      </label>
      <label>
        <input type="radio" name="xenero" value="muller"> Muller
      </label>
      <label>
        <input type="radio" name="xenero" value="outro"> Outro
      </label>
    </fieldset>

    <fieldset>
      <legend>Intereses</legend>
      <label>
        <input type="checkbox" name="intereses" value="deportes"> Deportes
      </label>
      <label>
        <input type="checkbox" name="intereses" value="musica"> Música
      </label>
      <label>
        <input type="checkbox" name="intereses" value="viaxes"> Viaxes
      </label>
    </fieldset>

    <label for="comentarios">Comentarios:</label>
    <textarea id="comentarios" name="comentarios"></textarea>

    <button type="submit">Rexistrarse</button>
  </form>
</body>
</html>
```

---

### **Conclusión**
Este exercicio axúdache a practicar a creación de formularios HTML complexos, validacións e accesibilidade. Espero que che sexa útil! 😊

---

DAW🧊2025

#html
#DAW