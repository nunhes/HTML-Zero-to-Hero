# Especificidade

Xa falamos, brevemente, desta característica de CSS. Imos a analizala máis en detalle. 

Cando **estilos conflitivos** apuntan ao mesmo elemento en CSS, o navegador debe decidir cales estilos aplicar. Este proceso chámase **resolución de conflitos** e baséase en tres conceptos principais: **especificidade**, **orde de aparición** e **importancia**. Vou explicarche como funciona cada un destes conceptos e como o navegador resolve os conflitos.

---

### **1. Especificidade**

A **especificidade** é o mecanismo que determina que regra CSS se aplica cando hai conflitos entre selectores. Calcúlase baseándose no tipo de selector:

- **Inline styles** (estilos en liña): `1000` puntos.
- **IDs**: `100` puntos por cada ID.
- **Clases, pseudo-clases e atributos**: `10` puntos por cada un.
- **Elementos e pseudo-elementos**: `1` punto por cada un.

#### **Exemplo de especificidade**
```css
p {
  color: red; /* Especificidade: 1 */
}

.destacado {
  color: blue; /* Especificidade: 10 */
}

#cabezallo {
  color: green; /* Especificidade: 100 */
}

p.destacado {
  color: purple; /* Especificidade: 11 (1 + 10) */
}
```
- Se un elemento `<p>` ten a clase `destacado` e o ID `cabezallo`, aplicarase a cor **verde** porque o selector de ID ten a maior especificidade.

---

### **2. Orde de aparición**

Se dúas regras teñen a **mesma especificidade**, a regra que aparece **última** no CSS é a que se aplica. Isto coñécese como **cascada** en CSS.

#### **Exemplo de orde de aparición**
```css
p {
  color: red;
}

p {
  color: blue; /* Aplicarase esta cor */
}
```
- A cor do texto será **azul** porque é a última regra definida.

---

### **3. Importancia**

A propiedade `!important` pódese engadir a un valor CSS para darlle a máxima prioridade, independentemente da especificidade ou a orde de aparición.

#### **Exemplo de `!important`**
```css
p {
  color: red !important;
}

p {
  color: blue; /* Non se aplica debido a !important */
}
```
- A cor do texto será **vermella** porque `!important` anula outras regras.

---

### **4. Como se resolve un conflito?**

O navegador segue estes pasos para resolver conflitos:

1. **Especificidade**: A regra con maior especificidade aplícase primeiro.
2. **Orde de aparición**: Se a especificidade é a mesma, a última regra definida aplícase.
3. **Importancia**: Se unha regra ten `!important`, aplícase independentemente da especificidade ou a orde.

---

### **5. Exemplo práctico**

Aquí tes un exemplo que mostra como se resolve un conflito:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Resolución de Conflitos en CSS</title>
  <style>
    /* Especificidade: 1 */
    p {
      color: red;
    }

    /* Especificidade: 10 */
    .destacado {
      color: blue;
    }

    /* Especificidade: 100 */
    #cabezallo {
      color: green;
    }

    /* Especificidade: 11 (1 + 10) */
    p.destacado {
      color: purple;
    }

    /* !important anula a especificidade */
    p {
      color: orange !important;
    }
  </style>
</head>
<body>
  <p>Este é un parágrafo normal.</p>
  <p class="destacado">Este parágrafo ten unha clase destacado.</p>
  <p id="cabezallo">Este parágrafo ten un ID cabezallo.</p>
  <p class="destacado" id="cabezallo">Este parágrafo ten unha clase e un ID.</p>
</body>
</html>
```

#### **Resultado esperado**:
1. O primeiro `<p>` será **laranxa** debido a `!important`.
2. O segundo `<p>` será **laranxa** debido a `!important`.
3. O terceiro `<p>` será **laranxa** debido a `!important`.
4. O cuarto `<p>` será **laranxa** debido a `!important`.

---

### **6. Boas prácticas para evitar conflitos**

1. **Evita o uso excesivo de `!important`**: O abuso de `!important` pode facer que o código sexa difícil de manter.
2. **Usa clases en lugar de IDs**: As clases son máis reutilizables e teñen menor especificidade que os IDs.
3. **Mantén a especificidade baixa**: Canto menor sexa a especificidade, máis fácil será sobrescribir estilos se é necesario.
4. **Organiza o CSS**: Escribe as regras nunha orde lóxica e evita duplicacións.

---

### **7. Conclusión**

Cando estilos conflitivos apuntan ao mesmo elemento, o navegador resolve o conflito baseándose na **especificidade**, a **orde de aparición** e a **importancia**. Coñecer estes conceptos é esencial para escribir CSS eficiente e mantible. Espero que esta explicación e exemplo che sexan útiles para entender como se resolven os conflitos en CSS! 😊

> #### **Lembra:** o uso de `!important` está totalmente desaconsellado. Evítao sempre!


---

DAW🧊2025

#css
#DAW