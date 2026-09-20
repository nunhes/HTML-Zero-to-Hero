# Variables CSS (Custom Properties)

As variables permiten gardar valores (cores, tamaños, fontes) e reutilizalos en todo o documento.

---

## 1. Declaración e Uso

Decláranse no selector `:root` para que estean dispoñibles en todo o sitio. Deber comezar por dous guións (`--`).

```css
:root {
  --cor-principal: #3498db;
  --espazado: 20px;
}

.boton {
  background-color: var(--cor-principal);
  padding: var(--espazado);
}
```

---

## 2. Vantaxes sobre SASS

A diferenza das variables en preprocesadores como SASS:
- Son **vivas**: Podes cambialas con JavaScript e o navegador actualiza todo ao instante.
- Heredanse: Un elemento fillo pode ter un valor diferente para a mesma variable.

---

## 3. Modo Escuro instantáneo

Podes crear temas facilmente cambiando só os valores das variables en función dunha clase ou media query:
```css
:root { --fondo: white; }
body.dark { --fondo: black; }

body { background: var(--fondo); }
```

---

**Resumo**:
As variables CSS fan que o teu código sexa máis limpo, fácil de manter e escalable. Son imprescindibles en proxectos modernos.

---

DAW🧊2026
