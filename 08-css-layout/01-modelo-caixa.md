# O Modelo de Caixa (Box Model)

O **Modelo de Caixa** é o concepto máis importante de CSS. Define como se calcula o espazo que ocupa cada elemento na páxina.

---

## 1. As capas da caixa

Cada elemento en HTML é visto polo navegador como unha caixa rectangular composta por:

1.  **Contido (Content)**: O texto, imaxe ou fillos do elemento.
2.  **Recheo (Padding)**: O espazo interior entre o contido e o borde.
3.  **Borde (Border)**: A liña que rodea o recheo e o contido.
4.  **Marxe (Margin)**: O espazo exterior que separa a caixa doutros elementos.

Visualmente:
```
+---------------------------+
|          Margin           |
|  +---------------------+  |
|  |       Border        |  |
|  |  +--------------+   |  |
|  |  |   Padding    |   |  |
|  |  |  +--------+  |   |  |
|  |  |  | Content|  |   |  |
|  |  |  +--------+  |   |  |
|  |  +--------------+   |  |
|  +---------------------+  |
+---------------------------+
```

---

## 2. Cálculo do tamaño total

Por defecto, se defines `width: 300px`, estás definindo só o ancho do **contido**. O tamaño real será:
`Ancho Total = width + padding-left + padding-right + border-left + border-right`

---

## 3. A propiedade `box-sizing`

Para evitar cálculos complexos, o estándar moderno é usar:
```css
* {
  box-sizing: border-box;
}
```
Con **`border-box`**, o `width` inclúe o padding e o borde, o que fai moito máis fácil deseñar layouts precisos.

---

**Resumo**:
Entender o modelo de caixa é a diferenza entre un deseño que encaixa e un que "rompe". Lembra: `padding` é interior, `margin` é exterior.

---

DAW🧊2026
