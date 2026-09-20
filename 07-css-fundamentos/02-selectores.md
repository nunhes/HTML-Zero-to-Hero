# Selectores CSS

Os **selectores de CSS** son o xeito que temos de indicarlle ao navegador a que elementos HTML debe aplicar un estilo determinado. Dominar os selectores é clave para escribir un código limpo, eficiente e fácil de manter.

---

## 1. Selectores Básicos

Estes son os que máis usarás no día a día:

| Selector | Exemplo | Descrición |
| :--- | :--- | :--- |
| **Tipo** | `p { ... }` | Selecciona todas as etiquetas dese tipo. |
| **Clase** | `.botón { ... }` | Selecciona elementos co atributo `class="botón"`. |
| **ID** | `#cabezallo { ... }` | Selecciona o único elemento co atributo `id="cabezallo"`. |
| **Universal** | `* { ... }` | Selecciona absolutamente todos os elementos da páxina. |

```css
/* Exemplo de uso de clase */
.aviso {
  color: orange;
  font-weight: bold;
}
```

---

## 2. Selectores Combinados

Permiten seleccionar elementos baseándose na súa relación con outros:

- **Descendente (`div p`)**: Selecciona todos os `<p>` que estean dentro dun `<div>`.
- **Fillo directo (`ul > li`)**: Selecciona os `<li>` que son fillos imediatos do `<ul>`.
- **Irmán adxacente (`h1 + p`)**: Selecciona o `<p>` que vai xusto despois dun `<h1>`.

---

## 3. Pseudo-clases e Pseudo-elementos

Engaden estilos baseándose en estados ou partes específicas dun elemento:

### **Pseudo-clases (Estados)**
- **`:hover`**: Cando o usuario pasa o rato por riba.
- **`:focus`**: Cando un elemento (como un input) está seleccionado.
- **`:nth-child(n)`**: Selecciona o elemento na posición `n`.

### **Pseudo-elementos (Partes)**
- **`::before` / `::after`**: Permiten inserir contido antes ou despois dun elemento.
- **`::first-letter`**: Para dar estilo á primeira letra dun parágrafo.

```css
/* Engade unha estrela antes dos títulos */
h2::before {
  content: "★ ";
  color: gold;
}
```

---

## 4. Selectores de Atributo

Seleccionan elementos que teñen un atributo específico:
```css
/* Selecciona só os enlaces que se abren en nova pestana */
a[target="_blank"] {
  text-decoration: none;
}
```

---

**Resumo**:
Usa clases para estilos reutilizables e reserva os IDs para elementos únicos. Evita selectores demasiado complexos para manter a túa folla de estilos lexible e rápida.

---

DAW🧊2026
