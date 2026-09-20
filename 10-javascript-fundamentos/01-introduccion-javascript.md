# Introdución a JavaScript

JavaScript é unha linguaxe de programación potente, lixeira e interpretada, coñecida principalmente por ser a linguaxe de programación das páxinas web. É o que fai que a web sexa interactiva: desde galerías de imaxes que se desprazan ata mapas interactivos e animacións complexas.

---

## 📚 Obxectivos de Aprendizaxe

Ao finalizar este tema, serás capaz de:
- [ ] Comprender que é JavaScript e para que se utiliza.
- [ ] Coñecer a historia e evolución da linguaxe (ECMAScript).
- [ ] Entender a diferenza entre HTML, CSS e JavaScript.
- [ ] Saber como incluír JavaScript nun ficheiro HTML.
- [ ] Executar o teu primeiro "Ola Mundo" na consola do navegador.

---

## 📖 Que é JavaScript?

JavaScript (JS) é unha linguaxe de programación de **alto nivel**, **dinámica** e **multiparadigma**. Aínda que comezou como unha linguaxe para facer as páxinas web máis "vivas", hoxe en día úsase en case calquera lugar: servidores (Node.js), aplicacións móbiles, robots e mesmo intelixencia artificial.

### O Tríptico do Desenvolvemento Web

Para construír unha páxina web moderna, necesitamos tres tecnoloxías fundamentais:
1. **HTML (Estrutura)**: O esqueleto da páxina (títulos, parágrafos, imaxes).
2. **CSS (Presentación)**: A roupa e a maquillaxe (cores, fontes, deseño).
3. **JavaScript (Comportamento)**: O cerebro e os músculos (interactividade, validacións, comunicación con servidores).

---

## 📜 Un pouco de historia

- **1995**: Brendan Eich crea JavaScript en só 10 días para o navegador Netscape Navigator.
- **1997**: Publácase o estándar **ECMAScript (ES)** para garantir que JS funcione igual en todos os navegadores.
- **2009**: Nace **Node.js**, permitindo usar JS fóra do navegador (no servidor).
- **2015**: Publácase **ES6 (ES2015)**, a maior actualización da historia da linguaxe, que introduciu clases, promesas e moitas melloras sintácticas.

---

## 💻 Como incluír JavaScript en HTML

Existen tres xeitos de engadir código JavaScript a un documento HTML:

### 1. JavaScript en liña (Inline)
O código escríbese directamente dentro dun atributo HTML. **Non se recomenda** para aplicacións grandes porque mestura a estrutura coa lóxica.

```html
<button onclick="alert('Ola Mundo!')">Fai clic aquí</button>
```

### 2. JavaScript interno
O código escríbese dentro dunha etiqueta `<script>` no propio ficheiro HTML. É útil para exemplos rápidos ou scripts moi específicos de unha soa páxina.

```html
<script>
  console.log("Este é código JavaScript interno");
</script>
```

### 3. JavaScript externo (O máis recomendado)
O código gárdase nun ficheiro separado con extensión `.js`. Isto permite que o código fose reutilizable e máis fácil de manter.

```html
<!-- No ficheiro HTML -->
<script src="script.js"></script>
```

---

## 🛠️ Onde se executa JavaScript?

JavaScript execútase normalmente no **navegador** (Chrome, Firefox, Safari, Edge). Todos os navegadores teñen un "motor de JavaScript" (como o V8 en Chrome) que interpreta e executa o código.

### A Consola do Navegador
A ferramenta máis importante para un programador de JS é a **Consola**. Podes abrila premendo `F12` ou `Ctrl + Shift + J` no teu navegador. Nela podes escribir código JS e ver os resultados ou erros instantaneamente.

---

## ✏️ O teu primeiro código: Ola Mundo

1. Abre a consola do teu navegador.
2. Escribe o seguinte e preme Enter:

```javascript
console.log("Ola Mundo desde a consola!");
```

Tamén podes probar cunha ventá emerxente:

```javascript
alert("Benvido ao curso de JavaScript!");
```

---

## ➡️ Seguinte Paso

Agora que xa sabes que é e como incluír JavaScript, imos aprender o fundamental de calquera linguaxe: as **Variables e os Tipos de Datos**.

---

**Data de actualización**: 12/02/2026
**Estado**: ✅ Completado

---

DAW🧊2026

#javascript #introducion #webdev #galego