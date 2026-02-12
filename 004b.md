# **A Estrutura Básica dun Documento HTML (Boilerplate)**

Agora que xa coñecemos como funcionan os **elementos e etiquetas HTML**, é hora de explorar a **estrutura básica** dun documento HTML, coñecida como **boilerplate**. Esta estrutura é esencial para organizar o noso código e asegurar que os navegadores poidan interpretalo correctamente.

---

### **Analoxía coa Estrutura dunha Carta**

Pensa nunha carta que escribirías a alguén. Normalmente, unha carta ten unha estrutura clara:
1. **Enderezo**: O remitente e o destinatario.
2. **Saludo**: "Querido/a..."
3. **Corpo**: O contido principal da carta.
4. **Despedida**: "Ata pronto" ou "Atentamente".
5. **Firma**: O teu nome.

Do mesmo xeito, un documento HTML ten unha estrutura definida que imos explorar a continuación.

---

### **Estrutura do Boilerplate HTML**

O **boilerplate HTML** é o esqueleto básico que todo documento HTML debe ter. Aquí tes un exemplo:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O Meu Sitio Web</title>
</head>
<body>
    <!-- O teu contido vai aquí -->
</body>
</html>
```

#### **1. Declaración `<!DOCTYPE html>`**
- Indica ao navegador que o documento está escrito en **HTML5**, a última versión de HTML.
- Sempre debe ir na primeira liña do teu documento.

#### **2. Elemento `<html>`**
- É a **raíz** do documento. Todo o contido HTML debe ir dentro deste elemento.
- O atributo `lang="gl"` indica que o idioma do contido é **galego**. Isto é importante para os lectores de pantalla e outras ferramentas de accesibilidade.

#### **3. Elemento `<head>`**
- Contén **metadatos** sobre o documento, como o conxunto de caracteres (`charset`), a configuración da vista (`viewport`) e o título da páxina.
- **Metadatos importantes**:
  - `<meta charset="UTF-8">`: Define o conxunto de caracteres como **UTF-8**, que soporta emojis, símbolos e caracteres especiais.
  - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Axusta a visualización da páxina en dispositivos móbiles.
  - `<title>`: Define o título da páxina, que aparece na lapela do navegador.

#### **4. Elemento `<body>`**
- É onde vai o **contido visible** da páxina: texto, imaxes, enlaces, etc.
- Todo o que queiras que os usuarios vexan debe ir dentro deste elemento.

---

### **Anidación e Indentación**

A **anidación** refírese a como os elementos HTML están contidos dentro doutros. Por exemplo, o elemento `<head>` e o elemento `<body>` están anidados dentro do elemento `<html>`.

A **indentación** (sangría) é crucial para manter o código organizado e lexible. Por exemplo:

```html
<html>
  <head>
    <title>O Meu Sitio Web</title>
  </head>
  <body>
    <h1>Benvido ao meu sitio web</h1>
    <p>Este é un exemplo de estrutura HTML.</p>
  </body>
</html>
```

- Cada nivel de anidación debe estar indentado con **dous espazos** ou unha **tabulación**.
- Isto axuda a visualizar a estrutura do código e facilita a súa lectura e depuración.

---

### **Atallo en VS Code: Xerar o Boilerplate Automaticamente**

Se estás usando **Visual Studio Code**, podes xerar o boilerplate HTML automaticamente seguindo estes pasos:
1. Crea un novo arquivo e gárdao con extensión `.html` (por exemplo, `index.html`).
2. Escribe `!` e preme `Tab` ou `Enter`.
3. VS Code xerará automaticamente o seguinte código:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

Cambia `lang="en"` por `lang="gl"` e modifica o título e o contido segundo as túas necesidades.

---

### **Exercicio Práctico: Crea o Teu Propio Boilerplate**

Agora é o teu turno. Sigue estes pasos:
1. Abre **VS Code** e crea un novo arquivo chamado `index.html`.
2. Usa o atallo `!` para xerar o boilerplate HTML.
3. Modifica o título e engade algún contido no `<body>`, como un encabezado (`<h1>`) e un parágrafo (`<p>`).
4. Asegúrate de que o código estea ben indentado e organizado.

#### **Exemplo de Código:**
```html
<!DOCTYPE html>
<html lang="gl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>O Meu Primeiro Sitio Web</title>
</head>
<body>
    <h1>Benvido ao meu sitio web</h1>
    <p>Este é un exemplo de estrutura HTML.</p>
</body>
</html>
```

---

### **Conclusión**

O **boilerplate HTML** é a base de calquera sitio web. Dominar esta estrutura permitiráche crear páxinas web ben organizadas e compatibles con todos os navegadores. Practica creando o teu propio boilerplate e experimenta con diferentes elementos HTML. Se tes dúbidas, non dubides en preguntar.  🚀

_\_ref:_ 
- [Basic HTML5 template boilerplate](https://www.freecodecamp.org/news/basic-html5-template-boilerplate-code-example/)
- [html5boilerplate.com](https://html5boilerplate.com/)

---

DAW🧊2026

#html
#DAW