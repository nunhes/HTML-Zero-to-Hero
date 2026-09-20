# Operadores en JavaScript

Os operadores son símbolos que nos permiten realizar operacións sobre os nosos datos (variables e valores). Sen os operadores, os nosos programas non poderían facer máis que mostrar información estática.

---

## 📚 Obxectivos de Aprendizaxe

Ao finalizar este tema, serás capaz de:
- [ ] Usar operadores aritméticos para facer cálculos.
- [ ] Utilizar operadores de asignación para gardar e actualizar valores.
- [ ] Comparar valores con operadores de comparación.
- [ ] Entender a diferenza entre igualdade estrita e igualdade debil.
- [ ] Combinar condicións con operadores lóxicos.

---

## ➕ Operadores Aritméticos

Son os que usamos para realizar operacións matemáticas básicas:

| Operador | Operación | Exemplo | Resultado |
|----------|-----------|---------|-----------|
| `+` | Suma | `5 + 2` | `7` |
| `-` | Resta | `10 - 4` | `6` |
| `*` | Multiplicación | `3 * 4` | `12` |
| `/` | División | `10 / 2` | `5` |
| `%` | Módulo (Resto) | `7 % 3` | `1` |
| `**` | Exponenciación | `2 ** 3` | `8` |
| `++` | Incremento | `let x = 5; x++` | `6` |
| `--` | Decremento | `let y = 5; y--` | `4` |

---

## 💾 Operadores de Asignación

O operador básico de asignación é o signo igual `=`. Permite gardar o valor da dereita na variable da esquerda. Tamén existen formas abreviadas:

- `let x = 10;`
- `x += 5;` (Equivale a `x = x + 5`)
- `x -= 2;` (Equivale a `x = x - 2`)
- `x *= 3;` (Equivale a `x = x * 3`)

---

## ⚖️ Operadores de Comparación

Úsanse para comparar dous valores e sempre devolven un valor booleano (`true` ou `false`).

| Operador | Significado | Exemplo |
|----------|-------------|---------|
| `>` | Maior que | `10 > 5` (true) |
| `<` | Menor que | `3 < 1` (false) |
| `>=` | Maior ou igual | `5 >= 5` (true) |
| `<=` | Menor ou igual | `10 <= 8` (false) |
| `==` | Igualdade (compara só valor) | `5 == "5"` (true) ⚠️ |
| `===` | Igualdade estrita (valor e tipo) | `5 === "5"` (false) ✅ |
| `!=` | Diferente de | `5 != 8` (true) |
| `!==` | Diferencia estrita | `5 !== "5"` (true) |

### 💡 Consello: Igualdade Estrita
En JavaScript, recoméndase usar sempre `===` e `!==` para evitar erros accidentais causados pola conversión automática de tipos.

---

## 🧠 Operadores Lóxicos

Permítennos combinar varias expresións booleanas para formar unha lóxica máis complexa.

### 1. AND (`&&`)
Devolve `true` só se **todas** as condicións son verdadeiras.
```javascript
let idade = 20;
let tenCarné = true;
console.log(idade >= 18 && tenCarné); // true
```

### 2. OR (`||`)
Devolve `true` se **polo menos unha** das condicións é verdadeira.
```javascript
let tenCoche = false;
let tenBici = true;
console.log(tenCoche || tenBici); // true
```

### 3. NOT (`!`)
Inviste o valor booleano. Se é `true`, pasa a ser `false`.
```javascript
let chove = true;
console.log(!chove); // false
```

---

## 📝 Operador Ternario

É unha forma abreviada de escribir unha estrutura `if/else` simple nunha soa liña.

**Sintaxe**: `condición ? valor_se_verdadeiro : valor_se_falso`

```javascript
let idade = 20;
let mensaxe = (idade >= 18) ? "Es maior de idade" : "Es menor de idade";
console.log(mensaxe);
```

---

## ✏️ Exercicios Prácticos

### Exercicio 1: Cálculos básicos
Crea unha variable `base = 10` e `altura = 5`. Calcula a área dun rectángulo (`base * altura`) e móstraa por consola.

### Exercicio 2: Comparacións
Predí o resultado (true/false) antes de probalo na consola:
1. `10 === "10"`
2. `5 > 3 && 2 <= 2`
3. `!(10 < 5)`

### Exercicio 3: Lóxica complexa
Tes unha tenda. Un cliente ten un desconto se:
- É maior de 65 anos **OU**
- Comprou máis de 3 produtos **E** é domingo.

Traduce esta lóxica a código JavaScript usando variables booleanas.

---

## ➡️ Seguinte Paso

Con estes operadores, xa podemos facer cálculos e comparacións. O seguinte paso é aprender a **tomar decisións** no noso código coas **Estruturas de Control**.

---

**Data de actualización**: 12/02/2026
**Estado**: ✅ Completado

---

DAW🧊2026

#javascript #operadores #loxica #mate
