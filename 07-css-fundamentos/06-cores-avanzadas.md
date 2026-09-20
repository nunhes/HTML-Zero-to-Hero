# Cores Avanzadas en CSS

Máis alá das cores sólidas, CSS permite crear efectos visuais complexos mediante degradados e transparencias.

---

## 1. Degradados Lineais (`linear-gradient`)

Crea unha transición suave entre dúas ou máis cores nunha dirección determinada.
```css
background: linear-gradient(to right, #ff7e5f, #feb47b);
```
Podes especificar a dirección (`to bottom`, `to top left`, `45deg`) e múltiples puntos de cor.

---

## 2. Degradados Radiais (`radial-gradient`)

A transición nace dende un punto central e esténdese cara fóra.
```css
background: radial-gradient(circle, #00c6ff, #0072ff);
```

---

## 3. Transparencias e Mesturas

- **Canal Alfa**: Usar `rgba()` ou `hsla()` permite que a cor teña transparencia sen afectar ao resto do elemento.
- **`background-clip: text`**: Un efecto moderno que permite aplicar un degradado só ao texto (facendo o fondo invisible).

---

## 4. Filtros de cor (`filter`)

Podes aplicar efectos de post-procesado como:
- `grayscale(100%)`: Converte o elemento a branco e negro.
- `blur(5px)`: Desenfoca o elemento.
- `sepia(50%)`: Aplica un ton sepia.

---

**Resumo**:
Os degradados e filtros son ferramentas poderosas para dar profundidade e dinamismo ao teu deseño sen necesidade de cargar imaxes pesadas.

---

DAW🧊2026
