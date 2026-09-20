# Marxes en CSS (Margin)

A marxe é o espazo **exterior** dun elemento, o que o separa dos seus veciños.

---

## 1. Definición

- **`margin-top`**
- **`margin-right`**
- **`margin-bottom`**
- **`margin-left`**

Sintaxe abreviada (orde das agullas do reloxo):
```css
margin: 10px 20px 30px 40px; /* Arriba, Dereita, Abaixo, Esquerda */
margin: 10px 20px;           /* Arriba/Abaixo: 10px, Dereita/Esquerda: 20px */
```

---

## 2. Centrado automático

Para centrar un elemento de bloque con ancho definido:
```css
div {
  width: 50%;
  margin: 0 auto;
}
```

---

## 3. Colapso de marxes

Un fenómeno curioso en CSS: cando dúas marxes verticais se tocan, non se suman, senón que se "colapsan" e só se aplica a maior delas.

---

## 4. Marxes negativas

A diferenza do padding, as marxes poden ser **negativas**. Isto permite mover elementos "encima" doutros ou sacalos fóra do seu contedor.

---

**Resumo**:
Usa `margin` para crear espazo entre elementos. Lembra que o centrado horizontal conséguese co valor `auto`.

---

DAW🧊2026
