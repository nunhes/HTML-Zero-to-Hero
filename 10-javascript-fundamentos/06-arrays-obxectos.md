# Arrays e Obxectos en JavaScript

En aplicacións reais, non adoitamos traballar con variables soltas. Necesitamos formas de agrupar información relacionada. JavaScript ofrécenos dúas ferramentas principais para isto: os **Arrays** (listas) e os **Obxectos** (estruturas clave-valor).

---

## 📚 Obxectivos de Aprendizaxe

Ao finalizar este tema, serás capaz de:
- [ ] Crear e manipular listas de datos con Arrays.
- [ ] Acceder, engadir e eliminar elementos dun Array.
- [ ] Usar métodos modernos de Arrays como `map`, `filter` e `forEach`.
- [ ] Definir obxectos para representar entidades complexas.
- [ ] Acceder ás propiedades e métodos dun obxecto.

---

## 📦 Arrays (Listas)

Un Array é unha lista ordenada de valores. Podes gardar calquera tipo de dato dentro.

### 1. Crear un Array
```javascript
const froitas = ["Mazá", "Plátano", "Pera"];
```

### 2. Acceso por índice
Os elementos dun array están numerados empezando desde o **0**.
```javascript
console.log(froitas[0]); // "Mazá"
console.log(froitas[2]); // "Pera"
```

### 3. Operacións básicas
```javascript
froitas.push("Laranxa");     // Engade ao final
froitas.unshift("Limón");   // Engade ao inicio
froitas.pop();               // Elimina o último
console.log(froitas.length); // Tamaño do array (4)
```

### 4. Métodos Modernos (ES6+)
Son formas máis potentes de traballar con arrays:

- **`forEach`**: Percorre o array.
  ```javascript
  froitas.forEach(f => console.log("Gústame a " + f));
  ```
- **`filter`**: Crea un novo array con elementos que cumpren unha condición.
  ```javascript
  const prezos = [10, 50, 80, 20];
  const caros = prezos.filter(p => p > 30); // [50, 80]
  ```
- **`map`**: Crea un novo array transformando cada elemento.
  ```javascript
  const dobres = prezos.map(p => p * 2); // [20, 100, 160, 40]
  ```

---

## 🏠 Obxectivos (Estruturas clave-valor)

Un obxecto permite agrupar propiedades (características) e métodos (accións) baixo un mesmo nome. É ideal para representar cousas do mundo real.

### 1. Crear un Obxecto
```javascript
const usuario = {
  nome: "Brais",
  idade: 30,
  estudante: true,
  materias: ["HTML", "CSS", "JS"],
  
  // Isto é un método (función dentro dun obxecto)
  saudar: function() {
    console.log("Ola, son " + this.nome);
  }
};
```

### 2. Acceder ás propiedades
Podes usar a notación de punto (a máis común) ou de corchetes.
```javascript
console.log(usuario.nome);        // "Brais"
console.log(usuario["idade"]);    // 30
usuario.saudar();                 // "Ola, son Brais"
```

### 3. Modificar e engadir
```javascript
usuario.idade = 31;            // Modificar
usuario.cidade = "Vigo";      // Engadir nova propiedade
delete usuario.estudante;     // Eliminar
```

---

## 🤝 Arrays de Obxectos

É a forma máis común de manexar datos que veñen dunha base de datos ou dunha API.

```javascript
const alumnos = [
  { nome: "Ana", nota: 8 },
  { nome: "Pedro", nota: 4 },
  { nome: "Sabela", nota: 9 }
];

// Obter só os nomes dos aprobados
const aprobados = alumnos
  .filter(a => a.nota >= 5)
  .map(a => a.nome);

console.log(aprobados); // ["Ana", "Sabela"]
```

---

## ✏️ Exercicios Prácticos

### Exercicio 1: Miña Lista
Crea un array cos teus 5 libros ou películas favoritas.
1. Engade un novo ao final.
2. Elimina o primeiro da lista.
3. Imprime por consola cantos elementos ten a lista agora.

### Exercicio 2: O Coche
Crea un obxecto `coche` con propiedades como `marca`, `modelo`, `ano` e `cor`.
1. Crea un método llamado `mostrarResumo` que imprima: "Este é un [marca] [modelo] do ano [ano]".
2. Cambia a cor do coche.

### Exercicio 3: Inventario
Tes este array: `const produtos = [{nome: "Pan", prezo: 1}, {nome: "Leite", prezo: 2}, {nome: "Auga", prezo: 0.5}]`.
Usa `forEach` para imprimir o nome e prezo de cada produto.

---

## ➡️ Seguinte Paso

Con isto rematamos os fundamentos da linguaxe! Agora estamos preparados para saír da consola e interactuar coas páxinas web reais usando o **DOM (Document Object Model)**.

---

**Data de actualización**: 12/02/2026
**Estado**: ✅ Completado

---

DAW🧊2026

#javascript #arrays #obxectos #json #webdev #estructurasdedatos
