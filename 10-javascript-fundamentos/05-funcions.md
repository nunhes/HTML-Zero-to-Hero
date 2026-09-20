# Funcións en JavaScript

As funcións son un dos piares fundamentais de JavaScript. Unha función é un bloque de código deseñado para realizar unha tarefa específica. A súa gran vantaxe é que permite escribir o código unha vez e **reutilizalo** moitas veces, o que nos aforra traballo e fai que o programa sexa máis fácil de manter.

---

## 📚 Obxectivos de Aprendizaxe

Ao finalizar este tema, serás capaz de:
- [ ] Declarar e invocar funcións básicas.
- [ ] Usar parámetros para pasar información ás funcións.
- [ ] Entender a importancia da instrución `return`.
- [ ] Coñecer as diferenzas entre funcións tradicionais e funcións de frecha (*Arrow Functions*).
- [ ] Comprender que é o "scope" ou alcance das variables.

---

## 🛠️ Declaración e Invocación

Para usar unha función necesítanse dous pasos: definila e chamala (invocala).

### 1. Definir a función
```javascript
function saudar() {
  console.log("Ola! Benvido ao curso.");
}
```

### 2. Chamar á función
```javascript
saudar(); // Amosa: "Ola! Benvido ao curso."
```

---

## 📥 Parámetros e Argumentos

As funcións poden recibir información para traballar con ela. Esa información pásase a través dos **parámetros**.

```javascript
function saudarUsuario(nome) {
  console.log("Ola, " + nome + "!");
}

saudarUsuario("Brais"); // Ola, Brais!
saudarUsuario("Sabela"); // Ola, Sabela!
```

Podes pasar máis dun parámetro separándoos por comas:
```javascript
function sumar(a, b) {
  console.log(a + b);
}
sumar(5, 3); // 8
```

---

## 📤 O valor de retorno (`return`)

A maioría das funcións non só fan algo, senón que **devolven** un resultado para que poidamos gardalo ou usalo despois. Para iso usamos a palabra reservada `return`.

```javascript
function calcularAreaRectangulo(base, altura) {
  return base * altura;
}

let area = calcularAreaRectangulo(10, 5);
console.log("A área é: " + area); // A área é: 50
```

> ⚠️ **Nota importante**: Unha función detense inmediatamente cando chega a un `return`. O código que haxa despois non se executará.

---

## 🏹 Funcións de Frecha (*Arrow Functions*)

En JavaScript moderno, existe unha forma máis curta e elegante de escribir funcións. Son moi comúns hoxe en día.

```javascript
// Función tradicional
function sumar(a, b) {
  return a + b;
}

// Arrow function (equivalente)
const sumar = (a, b) => a + b;

console.log(sumar(10, 20)); // 30
```

---

## 🌐 O Alcance das Variables (Scope)

As variables non son visibles desde calquera parte do código.

- **Variables Globais**: Declaradas fóra de calquera función. Son visibles desde todo o programa.
- **Variables Locais**: Declaradas dentro dunha función. Só se poden usar dentro desa función.

```javascript
let global = "Sóc global";

function probarScope() {
  let local = "Sóc local";
  console.log(global); // Funciona
  console.log(local);  // Funciona
}

probarScope();
console.log(local); // ERROR! local non está definida fóra
```

---

## ✏️ Exercicios Prácticos

### Exercicio 1: Saúdo personalizado
Crea unha función chamada `presentarse` que reciba un `nome` e unha `cidade`. Debe imprimir: "Ola, son [nome] e vivo en [cidade]".

### Exercicio 2: Conversor de temperatura
Crea unha función (pode ser de frecha) que converta graos Celsius a Fahrenheit.
Fórmula: `(Celsius * 1.8) + 32`.

### Exercicio 3: Par ou Impar
Crea unha función chamada `ePar` que reciba un número e devolva `true` se é par e `false` se é impar. (Pista: usa o operador módulo `%`).

---

## ➡️ Seguinte Paso

Agora que sabemos como organizar a lóxica en funcións, o seguinte paso é aprender a manexar grandes cantidades de información coas ferramentas máis potentes de JS: os **Arrays e Obxectos**.

---

**Data de actualización**: 12/02/2026
**Estado**: ✅ Completado

---

DAW🧊2026

#javascript #funcions #programacion #webdev #reutilizacion
