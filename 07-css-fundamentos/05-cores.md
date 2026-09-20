# A cor en CSS

A cor é un dos elementos máis poderosos do deseño web. En CSS, podemos aplicar cor ao texto, aos fondos, aos bordos e incluso crear efectos de transparencia.

---

## 1. Como definir cores en CSS

Existen varias formas de indicar unha cor:

### **a) Nomes de cores**
CSS recoñece uns 140 nomes estándar (ex: `red`, `blue`, `tomato`, `steelblue`).
```css
h1 { color: tomato; }
```

### **b) Código Hexadecimal**
É o sistema máis usado. Usa 6 díxitos (RRGGBB) precedidos de `#`.
```css
p { color: #ff5733; }
```

### **c) RGB e RGBA**
Define a mestura de Vermello (Red), Verde (Green) e Azul (Blue) de 0 a 255.
- **`rgb(255, 0, 0)`**: Vermello puro.
- **`rgba(255, 0, 0, 0.5)`**: Vermello con un 50% de transparencia (Alpha).

### **d) HSL e HSLA**
Máis intuitivo para humanos: Matiz (Hue), Saturación (Saturation) e Luminosidade (Lightness).
```css
div { background-color: hsl(120, 100%, 50%); } /* Verde brillante */
```

---

## 2. Propiedades principais

- **`color`**: Cor do texto.
- **`background-color`**: Cor de fondo.
- **`border-color`**: Cor do bordo.
- **`opacity`**: Opacidade de todo o elemento (afecta tamén ao contido).

---

## 3. O Canal Alfa vs Opacity

É importante distinguir entre ambos:
- A propiedade **`opacity: 0.5;`** fai que todo o elemento (incluíndo o seu texto) sexa semitransparente.
- O uso de **`rgba`** ou **`hsla`** permite que, por exemplo, o fondo sexa transparente pero o texto permaneza 100% opaco e lexible.

---

## 4. Accesibilidade e Contraste

Ao deseñar, debemos garantir que o texto sexa lexible para todos.
- **Contraste**: Debe haber unha diferenza clara entre o texto e o fondo.
- **Non usar só a cor**: Non indiques un erro só poñendo o texto en vermello; engade unha icona ou un texto explicativo para persoas con daltonismo.

---

**Resumo**:
A cor non é só estética, é comunicación. Usa sistemas como HSL para axustes finos e asegúrate sempre de que o teu deseño sexa accesible.

---

DAW🧊2026