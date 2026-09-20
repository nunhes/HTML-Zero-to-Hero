# Variables e Tipos de Datos

As variables son os contedores onde almacenamos información na memoria do ordenador para poder usala máis tarde no noso programa. Imaxina que as variables son "caixas" con etiquetas (nomes) nas que podes gardar diferentes tipos de obxectos (datos).

---

## 📚 Obxectivos de Aprendizaxe

Ao finalizar este tema, serás capaz de:
- [ ] Declarar variables usando `let` e `const`.
- [ ] Comprender por que xa non se recomenda usar `var`.
- [ ] Seguir as regras de nomenclatura de variables.
- [ ] Identificar os diferentes tipos de datos primitivos en JavaScript.
- [ ] Entender a diferenza entre tipos de datos simples e obxectos.

---

## 📖 Declaración de Variables

En JavaScript moderno (desde ES6), temos dúas formas principais de declarar variables:

### 1. `let`
Úsase para variables cuxo valor **pode cambiar** ao longo do programa.

```javascript
let puntuacion = 10;
puntuacion = 15; // É posible cambiar o valor
```

### 2. `const`
Úsase para variables cuxo valor **non vai cambiar**. Unha vez que lle dás un valor, non podes reasinalo. É a opción recomendada por defecto.

```javascript
const pi = 3.1416;
// pi = 3.14; // Isto daría un erro!
```

### ⚠️ Por que non usar `var`?
Antes de 2015, só existía `var`. O problema de `var` é que ten un comportamento confuso co "scope" (alcance) e permite declarar a mesma variable varias veces sen erro, o que provoca moitos fallos ocultos. **Evita o seu uso sempre que poidas.**

---

## 🏷️ Regras de Nomenclatura

Para dar nome ás túas variables en JavaScript, debes seguir estas regras:
1. **Case-sensitive**: `nome` e `Nome` son variables diferentes.
2. **Caracteres permitidos**: Letras, números, o signo do dólar `$` e o guión baixo `_`.
3. **Non poden empezar por número**: `let 1usuario` é incorrecto.
4. **Non usar palabras reservadas**: Non podes chamar a unha variable `let`, `const`, `if`, etc.
5. **Estilo CamelCase**: É a convención máis común en JS (ex: `nomeUsuario`, `calcularPrezoTotal`).

---

## 💎 Tipos de Datos Primitivos

JavaScript é unha linguaxe de **tipado dinámico**, o que significa que non tes que dicir que tipo de dato ten unha variable, JS descúbreo por ti. Existen 7 tipos de datos primitivos:

### 1. Number (Números)
Representa tanto números enteiros como decimais.
```javascript
let idade = 25;
let prezo = 19.99;
```

### 2. String (Cadeas de texto)
Texto entre comiñas simples `'`, dobres `"` ou backticks `` ` ``.
```javascript
let nome = "Brais";
let saudo = 'Ola, que tal?';
```

### 3. Boolean (Booleanos)
Só poden ter dous valores: `true` (verdadeiro) ou `false` (falso). Úsanse para a lóxica.
```javascript
let estaLogueado = true;
let tenPermiso = false;
```

### 4. Undefined
O valor que ten unha variable que foi declarada pero á que aínda non se lle asignou ningún valor.
```javascript
let caixaBaleira;
console.log(caixaBaleira); // undefined
```

### 5. Null
Representa a ausencia intencionada dun valor. É como dicir: "esta caixa está baleira a propósito".
```javascript
let resultadoSorteo = null;
```

### 6. Symbol e 7. BigInt
Tipos máis avanzados para casos moi específicos (BigInt úsase para números extremadamente grandes).

---

## 🧪 Como saber o tipo de dato?

Podes usar o operador `typeof` para ver o tipo de calquera variable:

```javascript
console.log(typeof 42);       // "number"
console.log(typeof "Ola");    // "string"
console.log(typeof true);     // "boolean"
```

---

## ✏️ Exercicios Prácticos

### Exercicio 1: Crea as túas variables
Crea un ficheiro ou usa a consola para:
1. Declarar unha variable `nome` co teu nome usando `const`.
2. Declarar unha variable `idade` coa túa idade usando `let`.
3. Incrementa a variable `idade` nun ano.
4. Amosa por consola: "Ola, son [nome] e teño [idade] anos".

### Exercicio 2: Tipos de datos
Que devolve `typeof` para as seguintes variables?
```javascript
let a = 100;
let b = "100";
let c = (a == b);
```

---

## ➡️ Seguinte Paso

Agora que sabemos como gardar datos, o seguinte paso é aprender a **manipular eses datos** usando os **Operadores**.

---

**Data de actualización**: 12/02/2026
**Estado**: ✅ Completado

---

DAW🧊2026

#javascript #variables #let #const #tiposdedatos
