# Formularios Avanzados e UX

Recoller datos complexos de xeito sinxelo para o usuario require o uso de tipos de input específicos e técnicas de UX.

---

## 1. Datas e Horas

HTML5 ofrece calendarios nativos:
- **`type="date"`**: Selección de día, mes e ano.
- **`type="time"`**: Selección de hora e minutos.
- **`type="datetime-local"`**: Ambos á vez.

---

## 2. Selección Numérica

- **`type="number"`**: Campo de texto que só admite díxitos.
- **`type="range"`**: Unha barra deslizante (slider) ideal para valores aproximados ou niveis.

---

## 3. Seletores Visuales

- **`type="color"`**: Abre a paleta de cores do sistema operativo.
- **`type="file"`**: Permite subir arquivos. Podes usar o atributo `accept=".pdf,.jpg"` para limitar o tipo de ficheiro.

---

## 4. Ocultar Datos técnicas

O **`type="hidden"`** úsase para enviar información ao servidor que o usuario non necesita ver, como tokens de seguridade ou IDs de sesión.

---

**Resumo**:
Canto máis específico sexa o `type` do input, mellor será o teclado que o móbil lle amose ao usuario e menos erros haberá no envío.

---

DAW🧊2026
