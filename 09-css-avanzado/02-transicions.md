# Transicións en CSS

As transicións permiten que os cambios de estilo ocorran de xeito suave e progresivo no tempo.

---

## 1. Propiedades básicas

Para que unha transición funcione, necesitas polo menos dúas cousas:
1.  **`transition-property`**: Que propiedade vai cambiar (ex: `background-color`, `transform`).
2.  **`transition-duration`**: Canto tempo vai tardar (ex: `0.3s`, `500ms`).

---

## 2. Control de tempo e atrasos

- **`transition-timing-function`**: Define a "curva" de velocidade.
  - `ease` (lento-rápido-lento).
  - `linear` (velocidade constante).
  - `ease-in` / `ease-out`.
- **`transition-delay`**: Tempo de espera antes de que comece a transición.

---

## 3. Atallo (Shorthand)

```css
button {
  transition: all 0.3s ease-in-out;
}
```

---

## 4. Cando usar transicións

Son ideais para cambios simples de estado:
- Cambiar a cor dun botón ao pasar o rato (`:hover`).
- Despregar un menú ao premer (`:active` ou clase JS).

---

**Resumo**:
As transicións fan que o sitio web se sinta máis Orgánico e menos brusco. Lembra: sen `duration`, o cambio será instantáneo.

---

DAW🧊2026
