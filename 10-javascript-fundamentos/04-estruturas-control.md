# Estruturas de Control en JavaScript

As estruturas de control permítennos romper a execución lineal dun programa. Grazas a elas, o noso código pode decidir que facer segundo certas condicións ou repetir unha acción tantas veces como sexa necesario.

---

## 📚 Obxectivos de Aprendizaxe

Ao finalizar este tema, serás capaz de:
- [ ] Tomar decisións no código usando `if`, `else if` e `else`.
- [ ] Manexar múltiples opcións coa estrutura `switch`.
- [ ] Repetir tarefas usando os bucles `for` e `while`.
- [ ] Diferenciar cando usar cada tipo de bucle.

---

## 🚦 Estruturas Condicionais

### 1. `if / else`
É a estrutura básica para tomar decisións. O código dentro do `if` só se executa se a condición entre parénteses é `true`.

```javascript
let idade = 20;

if (idade >= 18) {
  console.log("Podes entrar!");
} else {
  console.log("Es menor de idade.");
}
```

### 2. `else if`
Para comprobar múltiples condicións en cadea.

```javascript
let hora = 14;

if (hora < 12) {
  console.log("Bos días");
} else if (hora < 20) {
  console.log("Boas tardes");
} else {
  console.log("Boas noites");
}
```

### 3. `switch`
Moi útil cando temos moitas opcións posibles para unha mesma variable. É máis limpo que moitos `if/else` xuntos.

```javascript
let dia = "Luns";

switch (dia) {
  case "Sábado":
  case "Domingo":
    console.log("É fin de semana! 🎉");
    break; // Moi importante para non seguir executando os seguintes casos
  case "Luns":
    console.log("A empezar a semana...");
    break;
  default:
    console.log("Un día calquera.");
}
```

---

## 🔄 Bucles (Iteracións)

Os bucles serven para repetir un bloque de código.

### 1. Bucle `for`
Úsase cando sabemos **exactamente cantas veces** queremos repetir algo. Ten tres partes: inicio, condición e incremento.

```javascript
// Imprimir os números do 1 ao 5
for (let i = 1; i <= 5; i++) {
  console.log("Número: " + i);
}
```

### 2. Bucle `while`
Repítese mentres unha condición sexa verdadeira. Úsase cando **non sabemos cantas veces** se vai repetir (depende de algo externo).

```javascript
let contador = 1;
while (contador <= 5) {
  console.log("Contador: " + contador);
  contador++; // Coidado! Se non incrementas, terás un bucle infinito
}
```

### 3. Bucle `do...while`
Similar ao `while`, pero garante que o código se execute **polo menos unha vez**, xa que a condición se comproba ao final.

---

## 🛑 Control de Bucles: `break` e `continue`

- **`break`**: Sae do bucle inmediatamente.
- **`continue`**: Salta a iteración actual e pasa á seguinte.

```javascript
for (let i = 1; i <= 10; i++) {
  if (i === 5) continue; // Salta o número 5
  if (i === 8) break;    // Detén o bucle ao chegar ao 8
  console.log(i);
}
```

---

## ✏️ Exercicios Prácticos

### Exercicio 1: Calificador
Crea unha variable `nota = 7`. Usando `if/else`, amosa por consola se está aprobado (>= 5) ou suspenso (< 5). Engade un `else if` para as notas superiores a 9 que diga "Sobresalinte!".

### Exercicio 2: Táboa de multiplicar
Escribe un bucle `for` que amose a táboa de multiplicar do número 7 por consola (do 7x1 ao 7x10).

### Exercicio 3: FizzBuzz (Un clásico)
Escribe un bucle do 1 ao 20.
- Se o número é divisible por 3, imprime "Fizz".
- Se é divisible por 5, imprime "Buzz".
- Se é divisible por ambos, imprime "FizzBuzz".
- Se non, imprime o número.

---

## ➡️ Seguinte Paso

Xa sabemos como controlar o fluxo do programa. Agora imos aprender a **organizar o noso código** para que fose reutilizable usando as **Funcións**.

---

**Data de actualización**: 12/02/2026
**Estado**: ✅ Completado

---

DAW🧊2026

#javascript #condicionais #bucles #if #for #while
