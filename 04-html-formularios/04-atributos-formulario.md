# Atributos de Formulario

Existen atributos que se aplican a case calquera campo (`input`, `select`, `textarea`) para controlar como se comportan e como viaxan os datos.

---

## 1. Atributos de Identificación

- **`name`**: O máis importante para o servidor. É a "clave" coa que o backend recibirá o dato.
- **`id`**: Usado para asociar a `<label>` e para aplicar estilos CSS ou manipular con JavaScript.
- **`value`**: Define o valor inicial do campo.

---

## 2. Atributos de Estado

- **`disabled`**: O usuario non pode interactuar co campo e o seu valor NO se envía ao servidor.
- **`readonly`**: O usuario pode ver e copiar o texto, pero non cambialo. O valor SI se envía ao servidor.
- **`autofocus`**: O campo selecciónase automaticamente ao cargar a páxina.

---

## 3. Atributos de Axuda

- **`placeholder`**: Texto temporal que aparece dentro do campo mentres está baleiro.
- **`autocomplete`**: Podes poñelo en `on` ou `off` para controlar se o navegador debe axudar ao usuario a rechear o campo con datos gardados.

---

## 4. Atributos de Estrutura

- **`multiple`**: Usado en `<select>` ou `<input type="file">` para permitir elixir máis dunha opción.
- **`size`**: Define cantas filas se ven nun select ou o ancho visual dun texto.

---

**Resumo**:
Usa `name` para o servidor, `id` para o deseño e a accesibilidade, e `placeholder` para guiar ao usuario sen substituír a etiqueta (`label`).

---

DAW🧊2026
