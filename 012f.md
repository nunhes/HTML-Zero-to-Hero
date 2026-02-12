# Cascada e herdanza

> Os conceptos de **cascada** e **herdanza** en CSS, que son fundamentais para entender como se aplican os estilos nunha páxina web.

---

## **1. Cascada en CSS**

A **cascada** é o proceso polo cal o navegador decide que estilos aplicar cando hai múltiples regras que afectan ao mesmo elemento. O nome "cascada" vén da idea de que os estilos "caen" dun nivel a outro, aplicándose de maneira xerárquica.

#### **Como funciona a cascada?**
O navegador segue esta orde de prioridade para aplicar os estilos:

1. **Orde de aparición**: Se dúas regras teñen a mesma especificidade, a última regra declarada no CSS é a que se aplica.
2. **Especificidade**: As regras máis específicas teñen prioridade sobre as menos específicas.
3. **Importancia**: As regras con `!important` teñen a máxima prioridade (aínda que non é recomendable abusar deste mecanismo).

#### **Exemplo de cascada**
```css
p {
  color: red; /* Aplicarase se non hai regras máis específicas */
}

.destacado {
  color: blue; /* Aplicarase porque é máis específico */
}

#cabezallo {
  color: green; /* Aplicarase porque é aínda máis específico */
}
```

- Se un elemento `<p>` ten a clase `destacado` e o ID `cabezallo`, aplicarase a cor **verde** porque o selector de ID ten a maior especificidade.

---

## **2. Herdanza en CSS**

A **herdanza** é o proceso polo cal os elementos fillos herdan estilos dos seus elementos pais. Non todas as propiedades CSS son herdables, pero algunhas como `color`, `font-family`, e `font-size` sí que o son.

#### **Como funciona a herdanza?**
- Se defines un estilo nun elemento pai, os elementos fillos herdan ese estilo a menos que se sobrescriba explicitamente.
- Non todas as propiedades son herdables. Por exemplo, `margin`, `padding`, e `border` non se herdan.

#### **Exemplo de herdanza**
```html
<div style="color: blue;">
  <p>Este texto será azul porque herda o estilo do div.</p>
</div>
```

- O texto dentro do `<p>` será **azul** porque herda a propiedade `color` do seu elemento pai `<div>`.

#### **Propiedades non herdables**
Algunhas propiedades, como `margin`, `padding`, e `border`, non se herdan. Para aplicar estes estilos a elementos fillos, debes especificalos directamente.

---

## **3. Diferenzas entre cascada e herdanza**

- **Cascada**: Decide que estilos se aplican cando hai conflitos entre regras CSS.
- **Herdanza**: Determina como os estilos se transmiten dos elementos pais aos fillos.

---

## **4. Exemplo práctico**

Aquí tes un exemplo que mostra como funcionan a cascada e a herdanza:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cascada e Herdanza en CSS</title>
  <style>
    /* Estilo base */
    body {
      font-family: Arial, sans-serif;
      color: black;
    }

    /* Cascada: Especificidade */
    p {
      color: red;
    }

    .destacado {
      color: blue;
    }

    #cabezallo {
      color: green;
    }

    /* Herdanza */
    div {
      color: purple;
      padding: 10px;
      border: 1px solid black;
    }

    /* Propiedade non herdable */
    div p {
      padding: 5px; /* Non se herda do div, debe especificarse */
    }
  </style>
</head>
<body>
  <p>Este é un parágrafo normal.</p>
  <p class="destacado">Este parágrafo ten unha clase destacado.</p>
  <p id="cabezallo">Este parágrafo ten un ID cabezallo.</p>

  <div>
    <p>Este parágrafo está dentro dun div e herda a cor púrpura.</p>
  </div>
</body>
</html>
```

#### **Resultado esperado**:
1. O primeiro `<p>` será **vermello**.
2. O segundo `<p>` será **azul**.
3. O terceiro `<p>` será **verde**.
4. O cuarto `<p>` dentro do `<div>` será **púrpura** (herdanza) e terá un recheo de `5px` (non herdado).

---

## **5. Boas prácticas**

1. **Evita o uso excesivo de `!important`**: O abuso de `!important` pode facer que o código sexa difícil de manter.
2. **Usa clases en lugar de IDs**: As clases son máis reutilizables e teñen menor especificidade que os IDs.
3. **Mantén a especificidade baixa**: Canto menor sexa a especificidade, máis fácil será sobrescribir estilos se é necesario.
4. **Organiza o CSS**: Escribe as regras nunha orde lóxica e evita duplicacións.

---

## **6. Conclusión**

A **cascada** e a **herdanza** son conceptos fundamentais en CSS que determinan como se aplican os estilos aos elementos dunha páxina web. A cascada resolve conflitos baseándose na especificidade, a orde de aparición e a importancia, mentres que a herdanza permite que os elementos fillos herden estilos dos seus elementos pais. Coñecer e entender estes conceptos é esencial para escribir CSS eficiente e mantible. Espero que esta explicación e exemplo che sexan útiles! 😊


---

DAW🧊2025

#css
#DAW