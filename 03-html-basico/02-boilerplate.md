# A Estrutura Boilerplate

Todo documento HTML debe comezar cunha estrutura base chamada **boilerplate**. Este "esqueleto" contén a información mínima necesaria para que o navegador entenda o documento.

---

## 1. O código base

```html
<!DOCTYPE html>
<html lang="gl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O meu primeiro sitio web</title>
    <link rel="icon" href="favicon.ico">
</head>
<body>
    <!-- O contido visible vai aquí -->
</body>
</html>
```

---

## 2. Explicación das partes

- **`<!DOCTYPE html>`**: Indica que o documento usa a versión moderna de HTML5.
- **`<html lang="gl">`**: A raíz do documento. O atributo `lang` é vital para a accesibilidade e o SEO.
- **`<head>`**: Contén metadatos (información non visible directamente para o usuario).
  - **`charset="UTF-8"`**: Permite mostrar correctamente caracteres como a "ñ", acentos ou emojis.
  - **`viewport`**: Asegura que a páxina se vexa ben en móbiles.
  - **`<title>`**: O nome que aparece na lapela do navegador.
- **`<body>`**: Contén todo o que o usuario ve na pantalla.

---

## 3. Favicon

O **favicon** é a pequena icona que se mostra na lapela do navegador. Descríbese no `<head>`:
```html
<link rel="icon" type="image/x-icon" href="favicon.ico">
```

---

## 4. Atallo en VS Code

Podes xerar esta estrutura en segundos escribindo `!` e premendo `Tab`. Lembra cambiar sempre o `lang="en"` por `lang="gl"`!

---

**Resumo**:
O boilerplate organiza a información técnica no `<head>` e o contido visual no `<body>`. É o punto de partida de todo proxecto web.

---

DAW🧊2026
