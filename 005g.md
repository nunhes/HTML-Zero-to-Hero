# **Creación de sitios web con múltiples páxinas**

Agora que xa coñeces como funcionan as **rutas de arquivos**, imos usar ese coñecemento para crear **sitios web con múltiples páxinas**. Este concepto é esencial para construír sitios web máis complexos e organizados.

---

### **Estrutura dun sitio web con múltiples páxinas**

Imaxina que tes un **proxecto web** coa seguinte estrutura:

```
/Proxecto
  /public
    about.html
    contact.html
  /assets
    /images
      gato.png
  index.html
```

- **`index.html`**: A páxina principal (home) do teu sitio web.
- **`about.html`**: Unha páxina que describe quen es ou que fai o teu sitio.
- **`contact.html`**: Unha páxina para que os usuarios poidan contactar contigo.
- **`gato.png`**: Unha imaxe que podes usar no teu sitio.

---

### **Como ligar páxinas entre si**

Para ligar páxinas, usamos o **elemento de ancoraxe** (`<a>`) co atributo `href`. Por exemplo, para ligar a páxina principal (`index.html`) á páxina "Sobre min" (`about.html`), o código sería:

```html
<a href="./public/about.html">Sobre min</a>
```

Aquí, `./` indica que debemos buscar o arquivo `about.html` na carpeta `public`, que está no mesmo nivel que `index.html`.

---

### **Exercicio práctico: Ligando páxinas e imaxes**

Agora é o teu turno. Vamos crear un sitio web con múltiples páxinas e ligar imaxes a outras páxinas.

#### **Pasos para o Exercicio:**
1. **Descarga os arquivos**: Asegúrate de ter a estrutura de carpetas e arquivos proporcionada.
2. **Liga a páxina de contacto**: Na páxina principal (`index.html`), engade un enlace á páxina de contacto (`contact.html`).
3. **Liga unha imaxe á páxina "Sobre min"**: Engade unha imaxe na páxina principal que, ao facer clic, leve á páxina "Sobre min" (`about.html`).

#### **Exemplo de código:**
```html
<!-- Enlace á páxina de contacto -->
<a href="./public/contact.html">Contacto</a>

<!-- Imaxe que liga á páxina "Sobre min" -->
<a href="./public/about.html">
  <img src="./assets/images/gato.png" alt="Gato">
</a>
```

---

### **Desafío adicional: Usa a túa propia imaxe**

Se queres personalizar o teu sitio web, podes engadir a túa propia imaxe. Simplemente:
1. Sube a túa imaxe á carpeta `assets/images`.
2. Cambia o valor do atributo `src` na etiqueta `<img>` para que apunte á túa imaxe.

Por exemplo:
```html
<a href="./public/about.html">
  <img src="./assets/images/tua-imaxe.jpg" alt="A miña foto">
</a>
```

---

### **Recursos adicionais**

- **Documentación oficial de HTML**: [MDN Web Docs - Elemento de Ancoraxe](https://developer.mozilla.org/es/docs/Web/HTML/Element/a)
- **Visual Studio Code**: [Descarga VS Code](https://code.visualstudio.com/)

---

### **Conclusión**

Crear **sitios web con múltiples páxinas** é unha habilidade esencial no desenvolvemento web. Dominar o uso de **rutas relativas** e **elementos de ancoraxe** permitiráche construír sitios web organizados e funcionales. Practica con este exercicio e, se tes dúbidas, non dubides en preguntar. 🚀


---

DAW🧊2026

#html
#DAW