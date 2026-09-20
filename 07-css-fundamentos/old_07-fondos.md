## A etiqueta `<input>` e as datas

Se queremos que o usuario introduza unha data concreta, en vez de utilizar un campo de texto xenérico (`<input type="text">`), o máis axeitado é empregar un campo específico para datas. Estes mostran un control frecuentemente chamado **selector de datas**, que permite seleccionar día, mes e ano dun calendario personalizado, evitando a necesidade de escribir a data manualmente e garantindo un formato uniforme.

Existen varios valores para o atributo `type` do campo `<input>` que permiten obter datas ou horas do usuario:

| Tipo de información a obter | Etiqueta para usar              |
| --------------------------- | ------------------------------- |
| Data                        | `<input type="date">`          |
| Mes                         | `<input type="month">`         |
| Semana                      | `<input type="week">`          |
| Hora                        | `<input type="time">`          |
| Data e hora local           | `<input type="datetime-local">` |

É importante ter en conta que estes controis poden variar visualmente dependendo do sistema operativo e do navegador empregado. Vexamos algúns exemplos.

### O atributo `type="date"`

Usando `<input type="date">` podemos obter datas e incluso indicar unha data predeterminada co atributo `value`. O formato no código sempre debe ser **AAAA-MM-DD**, e o navegador encargarase de formatalo segundo a configuración rexional do usuario:

```html
<form method="post" action="/enviar">
  <label for="data">Selecciona a data:</label>
  <input type="date" id="data" name="data" value="2024-02-25">
</form>
```

Os atributos `min` e `max` permiten definir un intervalo de datas válidas. As datas fóra deste rango aparecerán desactivadas:

```html
<input type="date" min="2025-03-25" max="2025-12-25">
```

Tamén podemos usar o atributo `step` para definir un incremento entre datas. No seguinte exemplo, só se poderán seleccionar datas cada dous días:

```html
<input type="date" min="2024-02-25" max="2024-12-25" step="2">
```

### Campos de data relacionados

Ademais de `<input type="date">`, existen outros tipos relacionados:

#### O atributo `type="month"`

Se só nos interesa que o usuario seleccione un mes sen indicar o día, podemos empregar `<input type="month">`:

```html
<input type="month" value="2024-11" min="2024-02" max="2024-12" step="2">
```

Neste caso, os valores de `min` e `max` só inclúen ano e mes.

#### O atributo `type="week"`

O atributo `type="week"` permite seleccionar unha semana específica do ano:

```html
<input type="week" value="2024-W19" min="2024-W13" max="2024-W36" step="2">
```

O formato de semana usa o ano seguido de `-W` e o número da semana, por exemplo, `2024-W15`.

#### O atributo `type="time"`

Se queremos que o usuario seleccione unha hora concreta, podemos empregar `<input type="time">`. Podemos limitar as opcións con `min`, `max` e `step`:

```html
<input type="time" value="11:00" min="09:00" max="22:00" step="1800">
```

O valor de `step` está en segundos (`1800` = 30 minutos).

#### O atributo `type="datetime-local"`

Para pedir unha data e hora local, utilizamos `<input type="datetime-local">`:

```html
<input type="datetime-local" value="2024-07-23T11:00" min="2024-03-23T11:00" max="2024-11-23T11:00" step="3600">
```

O formato combina data (`AAAA-MM-DD`) e hora (`HH:MM`) separadas por `T`.

### Personalización con CSS

Podemos modificar a aparencia dos controis de data mediante CSS:

```css
input[type="date"] {
  border: 2px solid indigo;
  font-size: 1.1rem;
  background: #000d;
  color: #fff;
  padding: 6px;
  border-radius: 6px;
}

input[type="date"]::-webkit-calendar-picker-indicator {
  filter: invert(1);
}
```

Tamén podemos modificar partes específicas do control de data:

| Selector CSS                      | Descrición                                    |
|-----------------------------------|--------------------------------------------|
| `::datetime-edit`                | Contedor xeral do campo de data.           |
| `::datetime-edit-fields-wrapper` | Contedor dos campos de data.               |
| `::datetime-edit-day-field`      | Campo do día.                              |
| `::datetime-edit-month-field`    | Campo do mes.                              |
| `::datetime-edit-year-field`     | Campo do ano.                              |
| `::calendar-picker-indicator`    | Icona do selector de datas.                |

### Recursos adicionais

- 📖 [MDN: `input type="date"`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/date)
- 📖 [MDN: `input type="time"`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/time)
- 📖 [HTML Living Standard - `input`](https://html.spec.whatwg.org/multipage/input.html)

Esta breve guía ofrece unha visión completa sobre os tipos de entrada para datas en HTML e como empregalos correctamente. Se necesitas máis exemplos ou aclaracións, avísame! 😊

---

DAW🧊2025

#html
#DAW