# CSS Flexbox

**Flexbox** (Flexible Box Layout) é un módulo de deseño unidimensional de CSS que permite aliñar e distribuir o espazo entre os elementos dun contedor de xeito moi sinxelo, incluso cando os seus tamaños son dinámicos.

---

## 1. Conceptos Clave

Flexbox funciona cunha estrutura de **Contedor** (pai) e **Elementos** (fillos).

- **Eixe Principal (Main Axis)**: O eixe no que se dispoñen os elementos (por defecto horizontal).
- **Eixe Transversal (Cross Axis)**: O eixe perpendicular ao principal (por defecto vertical).

---

## 2. Propiedades do Contedor (Pai)

Para activar flexbox, usamos `display: flex;` no contedor.

| Propiedade | Descrición | Valores comúns |
| :--- | :--- | :--- |
| **`flex-direction`** | Define a dirección dos elementos. | `row`, `column`, `row-reverse` |
| **`justify-content`** | Aliña no eixe principal. | `center`, `space-between`, `flex-start` |
| **`align-items`** | Aliña no eixe transversal. | `center`, `stretch`, `flex-end` |
| **`flex-wrap`** | Permite que os fillos salten de liña. | `wrap`, `nowrap` |

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

## 3. Propiedades dos Elementos (Fillos)

- **`flex-grow`**: Define canto medra un elemento en relación aos demais.
- **`flex-shrink`**: Define se o elemento pode encollerse.
- **`flex-basis`**: Tamaño inicial do elemento antes de distribuír o espazo.
- **`align-self`**: Permite a un elemento individual sobrescribir a aliñación do pai.

---

## 4. Xogos para aprender Flexbox

A mellor forma de aprender Flexbox é xogando:
- **[Flexbox Froggy](https://flexboxfroggy.com/)**: Axuda a unha ra a chegar á súa folla de lirio usando CSS.
- **[Flexbox Zombies](https://mastery.games/flexboxzombies/)**: Unha aventura narrativa para dominar flexbox.

---

**Resumo**:
Flexbox é ideal para compoñentes pequenos (como un menú de navegación ou unha barra de ferramentas). Para deseños completos de páxinas con filas e columnas simultáneas, recomendase o uso de **CSS Grid**.

---

DAW🧊2026