# Táboas Avanzadas

Máis alá da estrutura básica, HTML permite ter un control moito máis fino sobre as columnas e a accesibilidade das táboas.

---

## 1. Control de Columnas (`<colgroup>` e `<col>`)

Se queres aplicar estilos a unha columna enteira sen ter que facelo cela por cela, usa `<colgroup>`.

```html
<table>
  <colgroup>
    <col style="background-color: #f2f2f2;"> <!-- Primeira columna -->
    <col span="2" style="background-color: #ffffff;"> <!-- Seguintes 2 columnas -->
  </colgroup>
  ...
</table>
```

---

## 2. Atributos de cabeceira complexos (`headers`)

En táboas moi complexas con múltiples niveis de cabeceiras, o atributo `scope` pode non ser suficiente. Nestes casos, usamos:
- **`id`** nas etiquetas `<th>`.
- **`headers`** nas etiquetas `<td>`, apuntando ao ID da súa cabeceira.

```html
<tr>
  <th id="id1">Data</th>
  <th id="id2">Evento</th>
</tr>
<tr>
  <td headers="id1">20/05</td>
  <td headers="id2">Concerto</td>
</tr>
```

---

## 3. Resumo para lectores de pantalla

Aínda que hoxe se prefire o uso de `<caption>`, algúns sistemas antigos usan o atributo `summary` (obsoleto en HTML5 pero moi común en código vello) para dar unha descrición técnica da táboa.

---

## 4. Estilos recomendados con CSS

Para que unha táboa sexa Lexible:
- **`border-collapse: collapse;`**: Elimina o espazo dobre entre bordos.
- **`padding`**: Dá "aire" ao texto dentro das celas.
- **`nth-child(even)`**: Crea o efecto de "cebra" (fondos alternos) para que sexa máis fácil seguir a fila coa vista.

---

**Resumo**:
As táboas avanzadas melloran a experiencia de usuario e a accesibilidade en conxuntos de datos grandes e complexos.

---

DAW🧊2026
