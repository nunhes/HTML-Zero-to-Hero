# Táboas Básicas en HTML

As **táboas** son a forma estándar de presentar datos estruturados en filas e columnas (como follas de cálculo ou horarios).

---

## 1. Estrutura básica

Unha táboa constrúese con catro etiquetas fundamentais:

- **`<table>`**: O contedor principal.
- **`<tr>`**: Unha fila (Table Row).
- **`<th>`**: Unha cela de encabezado (Table Header). Adoita ir en negrita e centrada por defecto.
- **`<td>`**: Unha cela de datos (Table Data).

```html
<table>
  <tr>
    <th>Produto</th>
    <th>Prezo</th>
  </tr>
  <tr>
    <td>Mazás</td>
    <td>1.50€</td>
  </tr>
</table>
```

---

## 2. Etiquetas de organización

Para táboas longas, é recomendable usar estas seccións:
- **`<thead>`**: Agrupa os titulares.
- **`<tbody>`**: Contén os datos.
- **`<tfoot>`**: Úsase para totais ou resumos ao final.
- **`<caption>`**: Título ou descrición da táboa que aparece fóra dela.

---

## 3. Combinar celas (`colspan` e `rowspan`)

- **`colspan="n"`**: Permite que unha cela se estenda horizontalmente por `n` columnas.
- **`rowspan="n"`**: Permite que unha cela se estenda verticalmente por `n` filas.

---

## 4. Accesibilidade

Para que os lectores de pantalla entendan a relación entre os datos, usamos o atributo **`scope`** nas etiquetas `<th>`:
- `scope="col"`: A cabeceira é dunha columna.
- `scope="row"`: A cabeceira é dunha fila.

---

**Resumo**:
As táboas só deben usarse para **datos**, nunca para facer o deseño visual da páxina (para iso temos CSS Grid e Flexbox). Unha táboa ben feita inclúe `<caption>`, `<thead>` e usa correctamente `scope`.

---

DAW🧊2026
