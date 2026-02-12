# Como crear táboas HTML ben formadas

## Estrutura básica dunha táboa HTML
Unha táboa HTML créase usando as etiquetas `<table>`, `<tr>`, `<th>`, e `<td>` (e outras etiquetas opcionais como `<thead>` , `<tbody>` e `<tfoot>`). Aquí tes un exemplo básico:

```html
<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Idade</th>
      <th>Cidade</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ana</td>
      <td>25</td>
      <td>Vigo</td>
    </tr>
    <tr>
      <td>Pedro</td>
      <td>30</td>
      <td>A Coruña</td>
    </tr>
  </tbody>
</table>
```

- **`<table>`**: Define a táboa.
- **`<thead>`**: Contén a cabeceira da táboa (opcional, pero recomendable para semántica e accesibilidade).
- **`<tr>`**: Define unha fila na táboa.
- **`<th>`**: Define unha celda de cabeceira (normalmente en negrita e centrada).
- **`<td>`**: Define unha celda de datos.

#### **Boas prácticas**
1. **Usar `<thead>`, `<tbody>` e `<tfoot>`**: Isto mellora a semántica e a accesibilidade da táboa.
2. **Evita aniñar táboas**: Aniñar táboas dentro doutras táboas pode facer o código difícil de manter e non é recomendable.
3. **Usa atributos de accesibilidade**: Como `scope` en `<th>` para indicar se a cabeceira corresponde a unha fila ou columna.
   ```html
   <th scope="col">Nome</th>
   ```
4. **Evita usar táboas para deseñar páxinas**: As táboas deben usarse para datos tabulares, non para o deseño da páxina. Para deseño, usa CSS e técnicas como Flexbox ou Grid.

---

### **Cando usar e cando non usar táboas**

#### **Cando usar táboas**
- **Datos tabulares**: Cando precisas mostrar datos organizados en filas e columnas, como táboas de prezos, horarios, ou listas de produtos.
- **Información estruturada**: Se a información ten unha relación clara entre filas e columnas, como unha lista de empregados con nome, idade e departamento.

#### **Cando NON usar táboas**
- **Deseño de páxinas**: As táboas non deben usarse para crear o deseño dunha páxina web (por exemplo, para colocar menús, cabeceiras, ou imaxes). Isto é unha mala práctica e dificulta a accesibilidade e o mantemento.
- **Listas sinxelas**: Se só estás mostrando unha lista de elementos sen relacións complexas, é mellor usar listas HTML (`<ul>` ou `<ol>`).
- **Contido non tabular**: Evita usar táboas para contido que non sexa tabular, como bloques de texto ou imaxes.

---

### **Exercicio práctico**

#### **Obxectivo**
Crear unha táboa HTML ben formada que mostre información sobre libros, e despois reflexionar sobre cando sería ou non apropiado usar táboas.

#### **Instrucións**
1. **Crea unha táboa HTML** que mostre información sobre libros. A táboa debe ter as seguintes columnas:
   - Título do libro
   - Autor
   - Ano de publicación
   - Xénero

2. **Engade datos**: Inclúe polo menos 3 libros na táboa.

3. **Aplica boas prácticas**:
   - Usa `<thead>` e `<tbody>`.
   - Engade unha cabeceira clara usando `<th>`.
   - Asegúrate de que a táboa sexa accesible usando o atributo `scope`.

4. **Reflexión**:
   - Explica cando sería apropiado usar unha táboa para mostrar esta información.
   - Pensa nun exemplo onde non sería apropiado usar unha táboa e explica por qué.

#### **Exemplo de solución**

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Táboa de Libros</title>
</head>
<body>
  <h1>Lista de Libros</h1>
  <table>
    <thead>
      <tr>
        <th scope="col">Título</th>
        <th scope="col">Autor</th>
        <th scope="col">Ano</th>
        <th scope="col">Xénero</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>O Señor dos Aneis</td>
        <td>J.R.R. Tolkien</td>
        <td>1954</td>
        <td>Fantasia</td>
      </tr>
      <tr>
        <td>1984</td>
        <td>George Orwell</td>
        <td>1949</td>
        <td>Distopía</td>
      </tr>
      <tr>
        <td>Cien Años de Soledad</td>
        <td>Gabriel García Márquez</td>
        <td>1967</td>
        <td>Realismo Máxico</td>
      </tr>
    </tbody>
  </table>

  <h2>Reflexión</h2>
  <p>
    <strong>Cando é apropiado usar táboas:</strong> 
    Neste caso, a táboa é apropiada porque estamos mostrando datos tabulares (libros con información relacionada en filas e columnas). Cada fila representa un libro e cada columna un atributo específico (título, autor, etc.).
  </p>
  <p>
    <strong>Cando non é apropiado usar táboas:</strong> 
    Non sería apropiado usar unha táboa para mostrar unha lista de imaxes ou un menú de navegación. Para iso, é mellor usar listas HTML ou técnicas de deseño CSS como Flexbox ou Grid.
  </p>
</body>
</html>
```

---

### **Conclusión**
Este exercicio axúdache a practicar a creación de táboas HTML ben formadas e a entender cando é apropiado usalas. Recorda que as táboas deben reservarse para datos tabulares e non para o deseño xeral da páxina. 😊

---

*_ref:*  [The Table element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table)

---

DAW🧊2026

#html
#DAW