# Introdución a Formularios

Os **formularios** son a ferramenta principal para que o usuario interactúe cun sitio web e envíe información ao servidor (como rexistros, buscas ou contactos).

---

## 1. O Contedor `<form>`

Para crear un formulario, todo debe ir envolto na etiqueta `<form>`. Os seus atributos máis importantes son:

- **`action`**: A URL a onde se enviarán os datos (ex: `/procesar-datos`).
- **`method`**: O xeito de enviar os datos.
  - **`GET`**: Os datos viaxan na URL como parámetros (ex: `?id=123`). Úsase para buscas e navegación onde os datos non son sensibles e a URL pode compartirse.
  - **`POST`**: Os datos viaxan no corpo da petición HTTP. É moito máis seguro para datos sensibles (contrasinais, tarxetas) e permite enviar arquivos grandes.

| Característica | GET | POST |
| :--- | :--- | :--- |
| **Visibilidade** | Visible na URL | Oculto |
| **Seguridade** | Baixa (queda no historial) | Alta (con HTTPS) |
| **Límite** | ~2000 caracteres | Sen límite práctico |
| **Uso** | Buscas, filtros | Rexistros, pagos, arquivos |

```html
<form action="/login" method="POST">
  <!-- Aquí van os elementos do formulario -->
</form>
```

---

## 2. Etiquetas e Asociación (`<label>`)

É fundamental que cada campo teña a súa etiqueta asociada para a accesibilidade.
```html
<label for="nome_usuario">Nome de usuario:</label>
<input type="text" id="nome_usuario" name="usuario">
```
O atributo **`for`** da etiqueta debe coincidir co **`id`** do input.

---

## 3. Envío e Limpeza

- **`<button type="submit">`**: Envía o formulario ao servidor.
- **`<button type="reset">`**: Limpa todos os campos do formulario.

---

## 4. Agrupación Semántica

- **`<fieldset>`**: Agrupa elementos relacionados dentro do formulario.
- **`<legend>`**: Proporciona un título para o grupo definido no fieldset.

---

**Resumo**:
Un formulario ben estruturado usa o método de envío correcto, asocia sempre as etiquetas cos seus campos e organiza a información semanticamente.

---

DAW🧊2026
