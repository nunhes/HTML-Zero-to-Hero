# Introdución a CSS

Como colofón a esta introdución a HTML facemos unha introdución breve a **CSS** (Cascading Style Sheets), que é a linguaxe usada para para describir como os documentos son presentados visualmente, e como se aplican e organizan os estilos. 

CSS é relativamente fácil de entender, pero pode ser intimidante pola cantidade de propiedades que podemos chegar a manipular.

Despois, profundaremos en conceptos clave como os tipos de CSS, marxes, recheos, bordes e o modelo de caixa.

---

## 1. Que é CSS?

CSS é unha linguaxe que se usa para definir a presentación e o deseño dun documento HTML. Permite controlar aspectos como cores, fontes, espazado, tamaño, posición e moito máis. CSS funciona en conxunto con HTML para crear páxinas web visualmente atractivas e ben estruturadas.

### Exemplo básico:
```html
<style>
  body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
  }
  h1 {
    color: #0066cc;
    text-align: center;
  }
</style>
```

---

## 2. Formas de aplicar CSS

Existen tres xeitos de aplicar estilos a un HTML:

### **a) CSS externo (Recomendado)**
O CSS defínese nun arquivo `.css` independente e vincúlase mediante a etiqueta `<link>`.
```html
<link rel="stylesheet" href="estilos.css">
```

### **b) CSS interno**
Defínese dentro da etiqueta `<style>` no `<head>` do documento. Útil para estilos específicos dunha soa páxina.

### **c) CSS en liña**
Aplícase directamente nun elemento usando o atributo `style`. **Debe evitarse** xa que dificulta o mantemento.
```html
<h1 style="color: blue;">Ola Mundo!</h1>
```

---

## 3. Estrutura dunha Regra CSS

Unha regra CSS consta dun **selector** e un **bloque de declaración**.

```css
p {
  color: red;
  font-size: 16px;
}
```
- **Selector**: `p` (o elemento ao que queremos dar estilo).
- **Declaración**: `color: red;` (propiedade e valor).

---

## 4. Conceptos Fundamentais

Para dominar CSS, é vital entender estes tres piares:

### **A Cascada**
Se dúas regras afectan ao mesmo elemento, o navegador decide cal aplicar segundo a súa importancia, especificidade e orde de aparición (a última regra declarada adoita gañar).

### **A Herdanza**
Algunhas propiedades (como o tipo de letra ou a cor) pásanse dos pais aos fillos. Outras (como as marxes ou bordes) non se herdan.

### **A Especificidade**
É a puntuación que determina que regra é máis "poderosa". Un ID (`#`) é máis específico que unha clase (`.`), e unha clase máis que unha etiqueta.

---

**Resumo**:
CSS separa o contido (HTML) do deseño. Usar arquivos externos e manter unha xerarquía clara de selectores é a base dun bo desenvolvemento web.

---

DAW🧊2026
