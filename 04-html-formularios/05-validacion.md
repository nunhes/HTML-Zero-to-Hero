# Validación de Formularios

A validación asegura que o usuario introduza datos no formato correcto antes de que estes cheguen ao servidor.

---

## 1. Validación Básica (Obrigatoriedade)

O atributo **`required`** pide ao navegador que non deixe enviar o formulario se o campo está baleiro.

---

## 2. Validación de Lonxitude e Rango

- **`minlength` / `maxlength`**: Para controlar o número de caracteres en textos.
- **`min` / `max`**: Para controlar os valores mínimos e máximos en números (`type="number"`) ou datas.

---

## 3. Validación de Formato (Regex)

O atributo **`pattern`** permite definir unha **expresión regular** que o dato debe cumprir.
```html
<!-- Só permite números de 9 cifras (teléfono) -->
<input type="text" pattern="[0-9]{9}" title="Introduce un teléfono de 9 díxitos">
```
O atributo **`title`** amosará unha mensaxe de erro ao usuario se non cumpre o patrón.

---

## 4. Estilización da Validación (CSS)

Podes usar pseudo-clases para dar feedback visual inmediato:
- **`:required`**: Campos que son obrigatorios.
- **`:valid`**: O campo cumpre todas as regras.
- **`:invalid`**: O campo ten erros.

```css
input:invalid {
  border-color: red;
}
```

---

**Resumo**:
A validación en HTML5 é a primeira liña de defensa. Mellora a experiencia do usuario ao avisar dos erros antes de recargar a páxina.

---

DAW🧊2026
