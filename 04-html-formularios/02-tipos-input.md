# Tipos de Input en HTML5

A etiqueta `<input>` é a máis versátil de HTML. Grazas ao seu atributo `type`, pode transformarse en moitos tipos de campos diferentes.

---

## 1. Campos de texto e datos básicos

- **`type="text"`**: Campo de texto simple (unha soa liña).
- **`type="password"`**: Enmascara os caracteres para contrasinais.
- **`type="email"`**: Valida automaticamente que o texto teña formato de correo.
- **`type="number"`**: Só permite números e engade frechas para subir/baixar.
- **`type="url"`**: Valida que o texto sexa un enderezo web.

---

## 2. Electores de opción

- **`type="radio"`**: Permite escoller só UNHA opción entre un grupo (deben compartir o mesmo `name`).
- **`type="checkbox"`**: Permite escoller MÚLTIPLES opcións.

---

## 3. Seletores de data e cor

- **`type="date"`**: Abre un calendario nativo do sistema.
- **`type="color"`**: Abre un seletor de cor.
- **`type="time"`**: Seletor de hora.

---

## 4. Otros tipos útiles

- **`type="range"`**: Unha barra deslizante (slider).
- **`type="file"`**: Permite ao usuario subir un arquivo dende o seu computador.
- **`type="hidden"`**: Campo invisible para gardar datos que o usuario non debe ver nin tocar.

---

## 5. Atributos de validación

Podes engadir atributos para obrigar ao usuario a introducir datos correctos:
- **`required`**: O campo non pode quedar baleiro.
- **`minlength` / `maxlength`**: Lonxitude do texto.
- **`min` / `max`**: Rango para números ou fechas.
- **`pattern`**: Permite usar expresións regulares (regex) para validacións complexas.

---

**Resumo**:
Usa sempre o `type` máis específico para a información que queiras recoller. Isto mellora a experiencia do usuario (especialmente en móbiles) e a validación dos datos.

---

DAW🧊2026
