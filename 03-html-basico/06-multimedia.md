# Multimedia en HTML5

HTML5 facilita a inclusión de imaxes, audio e vídeo sen necesidade de programas externos.

---

## 1. Imaxes (`<img>`)

Ficheiros de imaxe (`jpg`, `png`, `svg`, `webp`).
- **`src`**: Ruta do ficheiro.
- **`alt`**: Descrición textual (fundamental para a accesibilidade).

```html
<img src="foto.jpg" alt="Unha paisaxe galega ao amencer">
```

---

## 2. Audio e Vídeo (`<audio>`, `<video>`)

Permiten reprodutores nativos no navegador.

```html
<video controls width="400">
  <source src="video.mp4" type="video/mp4">
  O teu navegador non soporta vídeo.
</video>
```
O atributo **`controls`** é necesario para que o usuario poida darlle ao play, pausar ou axustar o volume.

---

## 3. Figuras e lendas

Usa **`<figure>`** para envolver a multimedia e **`<figcaption>`** para engadir unha descrición que apareza xunto á imaxe ou vídeo.

---

**Resumo**:
Usa sempre o atributo `alt` e elixe formatos modernos (como WebP) para que a túa web cargue máis rápido.

---

DAW🧊2026
