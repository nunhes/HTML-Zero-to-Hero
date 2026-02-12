# **Rutas de arquivos en HTML: absolutas e relativas**

Un concepto fundamental tanto para a informática como para o desenvolvemento web son as **rutas de arquivos**. Especificamente, imos aprender sobre as **rutas absolutas** e **rutas relativas**, que son esenciais para localizar arquivos e carpetas no teu ordenador ou nun servidor web.

---

### **Que é unha ruta de arquivo?**

Unha **ruta de arquivo** é unha dirección única que indica a localización dun arquivo ou carpeta no teu ordenador. Podes pensar nela como unha dirección postal que guía a alguén a un lugar específico. Por exemplo:

- **Ruta no mundo real**: Galicia → Vigo → Calvario → Rúa Urzáiz → Cafetería.
- **Ruta no ordenador**: Disco duro (C:) → Carpeta de proxectos → Carpeta de imaxes → `gato.png`.

---

### **Rutas absolutas**

Unha **ruta absoluta** é unha ruta completa que comeza desde a **raíz do sistema de arquivos** (por exemplo, `C:` en Windows ou `Macintosh HD` en Mac). Esta ruta é útil porque sempre apunta ao mesmo arquivo, independentemente de onde esteas no sistema de arquivos.

#### **Exemplo de Ruta Absoluta:**
- **Windows**: `C:\proxectos\imaxes\gato.png`
- **Mac**: `/Usuarios/TeuUsuario/proxectos/imaxes/gato.png`

---

### **Rutas relativas**

Unha **ruta relativa** é unha ruta que comeza desde a **localización actual** do arquivo no que estás a traballar. Esta ruta é máis común no desenvolvemento web porque é máis flexible e non depende da estrutura completa do sistema de arquivos.

#### **Exemplo de ruta relativa:**
Se estás a traballar nun arquivo `index.html` dentro da carpeta `proxectos`, a ruta relativa para acceder a `gato.png` sería:

```html
./imaxes/gato.png
```

---

### **Caracteres especiais en rutas relativas**

- **`./`**: Indica a **carpeta actual**. Por exemplo, `./gato.png` busca o arquivo `gato.png` na mesma carpeta onde está o arquivo actual.
- **`../`**: Indica **subir un nivel** na estrutura de carpetas. Por exemplo, `../imaxes/gato.png` busca o arquivo `gato.png` nunha carpeta irmá chamada `imaxes`.

---

### **Exercicio práctico: rutas relativas**

Agora é o teu turno. Vamos crear unha páxina web que mostre imaxes de animais usando **rutas relativas**. O obxectivo é que cada imaxe se mostre correctamente baixo o seu título correspondente.

#### **Estrutura de carpetas:**
```
/Proxectos
  /carpeta0
    index.html
    /carpeta1
      /carpeta2
        paxaro.png
      peixe.png
    /carpeta3
      gato.png
    coello.png
  cans.png
```

#### **Pasos para o exercicio:**
1. Abre o arquivo `index.html` no teu editor de código.
2. Engade as etiquetas `<img>` para cada animal, usando rutas relativas para acceder ás imaxes.
3. Asegúrate de que cada imaxe se mostre correctamente baixo o seu título.

#### **Exemplo de Código:**
```html
<h2>Coello</h2>
<img src="./coello.png" alt="Coello">

<h2>Gato</h2>
<img src="./carpeta3/gato.png" alt="Gato">

<h2>Can</h2>
<img src="../cans.png" alt="Can">

<h2>Peixe</h2>
<img src="./carpeta1/peixe.png" alt="Peixe">

<h2>Paxaro</h2>
<img src="./carpeta1/carpeta2/paxaro.png" alt="Paxaro">
```

---

### **Consellos adicionais**

- **Uso de `./` e `../`**: Asegúrate de usar correctamente `./` para acceder a arquivos na mesma carpeta e `../` para subir un nivel na estrutura de carpetas.
- **Alt Text**: Sempre engade un texto alternativo (`alt`) ás imaxes para mellorar a accesibilidade.
- **Depuración**: Se unha imaxe non se mostra, revisa a ruta e asegúrate de que o arquivo existe na localización indicada.

---

### **Recursos adicionais**

- **Documentación oficial de HTML**: [MDN Web Docs - Rutas de Arquivos](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/Dealing_with_files)
- **Visual Studio Code**: [Descarga VS Code](https://code.visualstudio.com/)

---

### **Conclusión**

As **rutas de arquivos** son unha parte esencial do desenvolvemento web. Dominar as rutas **absolutas** e **relativas** permitiráche acceder a recursos como imaxes, arquivos CSS e outros documentos de forma eficiente. Practica con este exercicio e, se tes dúbidas, non dubides en preguntar.  🚀


---

DAW🧊2026

#html
#DAW