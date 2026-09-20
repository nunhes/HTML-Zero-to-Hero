# Animacións e Keyframes

A diferenza das transicións, as animacións non necesitan un cambio de estado para ocorrer e poden ter múltiples pasos.

---

## 1. Fotogramas clave (`@keyframes`)

Aquí definimos os pasos da animación:
```css
@keyframes mover-y-xirar {
  0% { transform: translateX(0); }
  50% { transform: translateX(100px) rotate(180deg); }
  100% { transform: translateX(0) rotate(360deg); }
}
```

---

## 2. Aplicar a animación

Usamos a propiedade `animation` co nome que definimos nos keyframes:
```css
.caixa {
  animation: mover-y-xirar 2s infinite alternate;
}
```

---

## 3. Propiedades de control

- **`animation-iteration-count`**: Cantas veces se repite (ex: `3`, `infinite`).
- **`animation-direction`**: `normal`, `reverse`, `alternate` (vai e volve).
- **`animation-fill-mode`**: `forwards` (queda no estado final ao rematar).

---

## 4. Rendemento

Anima sempre propiedades que non forcen o recálculo do layout (usa `transform` e `opacity` en vez de `width` ou `top`).

---

**Resumo**:
As animacións dan vida á web. Úsaas con moderación para non marear ao usuario nin afectar ao rendemento.

---

DAW🧊2026
