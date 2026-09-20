# HTML Semántico

O **HTML semántico** é a práctica de usar etiquetas que describen o significado do contido, non só a súa aparencia. 

---

## 1. Por que usar semántica?

- **Accesibilidade**: Os lectores de pantalla poden navegar mellor pola páxina.
- **SEO**: Os buscadores (como Google) entenden mellor de que trata o teu sitio.
- **Mantemento**: O código é máis fácil de ler para outros desenvolvedores.

---

## 2. Etiquetas Estruturais

HTML5 introduciu etiquetas para as partes comúns dunha web:

- **`<header>`**: Cabeceira do sitio ou dunha sección.
- **`<nav>`**: Bloque de navegación (enlaces principais).
- **`<main>`**: O contido principal e único do documento.
- **`<article>`**: Contido independente e reutilizable (ex: un post do blog).
- **`<section>`**: Agrupa contido relacionado tematicamente.
- **`<aside>`**: Contido indirectamente relacionado (ex: barra lateral).
- **`<footer>`**: Pé de páxina.

---

## 3. Semántica vs Presentación

Evita usar `<div>` para todo. Se algo é un menú, usa `<nav>`. Se algo é un pé de páxina, usa `<footer>`. 

| Mal (Sen semántica) | Ben (Semántico) |
| :--- | :--- |
| `<div id="menu">` | `<nav>` |
| `<div class="rodape">` | `<footer>` |
| `<div class="artigo">` | `<article>` |

---

## 4. Atributos ARIA e Data-*

Cando as etiquetas estándar non chegan, podemos usar:
- **ARIA (Accessible Rich Internet Applications)**: Atributos como `aria-label` ou `role` para dar máis contexto ás ferramentas de asistencia.
- **`data-*`**: Atributos personalizados para gardar información que logo usaremos con JavaScript.

---

**Resumo**:
O HTML semántico dálle sentido á web. Unha boa estrutura separa claramente as seccións e axuda tanto a humanos como a máquinas a entender o teu contido.

---

DAW🧊2026
