# Configura e pesoaliza VSCode

### Tema

Podes escoller entre unha morea de temas. Usa preferentementa temas escuros e cun bo uso da cor para resaltar o código que vas a crear ou editar. Eu uso temas como `Monokai` ou `Oceanic Next` coa opción de fondo escurecido. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=naumovs.theme-oceanicnext)

### Extensións que considero útiles en distintos contextos

Le a páxina de descrición das extensións que vaias instalando para aprender como empregala.

- `Auto Close Tag`: Para pechar automaticamente as etiquetas HTML. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
- `Auto Rename Tag`: Para cambiar automaticamente as etiquetas HTML coincidentes. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- `Color Highlight`: Para, como o nome indica, resaltar cores en CSS. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
- `Paste and Indent`: Para indentar automaticamente o código pegado. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=Rubymaniac.vscode-paste-and-indent)
- `Path Intellisense`: Para autocompletar nomes de arquivos. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- `Prettier`: Para formatear automaticamente o código. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

### Outras extensións que uso (actualizarei esta lista)

- `Project Manager`: Para cambiar facilmente entre proxectos. Unha das extensións máis útiles. [Ligazón &rarr;](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)

### Configuración

Se queres persoalizar o teu editor de xeito máis detallado podes copiar esta configuración no teu arquivo de configuración, ou crear a túa persoalización. Simplemente vai a configuración en VSCode e, na parte dereita, pega este código ou crea o teu propio.

```json
{
  "workbench.colorTheme": "Oceanic Next (dimmed bg)",
  "files.autoSave": "onFocusChange",
  "editor.minimap.enabled": true,
  "workbench.statusBar.visible": true,
  "workbench.activityBar.visible": true,
  "editor.formatOnSave": false,

  "workbench.colorCustomizations": {
    "statusBar.background": "#333333",
    "statusBar.noFolderBackground": "#333333",
    "statusBar.debuggingBackground": "#263238"
  },
  "editor.fontSize": 16,

  "css.validate": false,
  "scss.validate": false,
  "less.validate": false,
  "editor.wordWrap": "on"
}
```

---



Aquí tes unha lista de recomendacións para configurar **Visual Studio Code (VS Code)** e optimizalo para o desenvolvemento web con **HTML, CSS e JavaScript**. Estas configuracións e extensións axudarán a mellorar a túa produtividade e a facilitar o teu fluxo de traballo.

---

### **1. Extensións recomendadas**
Aquí tes algunhas extensións esenciais para desenvolvemento web:

#### **HTML**
- **Auto Close Tag**: Pecha automaticamente as etiquetas HTML.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
- **Auto Rename Tag**: Cambia automaticamente a etiqueta de peche cando renomeas a de apertura.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- **HTML CSS Support**: Proporciona autocompletado para clases e IDs de CSS en arquivos HTML.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)

#### **CSS/SCSS**
- **IntelliSense for CSS class names in HTML**: Autocompleta os nomes das clases CSS nos arquivos HTML.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion)
- **CSS Peek**: Permite inspeccionar e ir á definición de clases e IDs de CSS directamente dende o HTML.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=pranaygp.vscode-css-peek)
- **SCSS IntelliSense**: Autocompletado avanzado para SCSS.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-scss)

#### **JavaScript**
- **ESLint**: Integra ESLint para analizar e corrixir erros no teu código JavaScript.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- **JavaScript (ES6) code snippets**: Proporciona atallos para código JavaScript moderno.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets)
- **Prettier**: Formatea automaticamente o teu código JavaScript, CSS e HTML.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

#### **Produtividade xeral**
- **Live Server**: Inicia un servidor local e actualiza automaticamente a páxina cando gardas cambios.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- **Bracket Pair Colorizer**: Colorea os pares de corchetes para facer máis fácil a lectura do código.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)
- **Path Intellisense**: Autocompleta rutas de arquivos.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- **GitLens**: Proporciona información adicional sobre Git directamente no editor.  
  [Ligazón](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

---

### **2. Outra configuración recomendable**
Aquí tes algunhas configuracións que podes engadir ao teu arquivo `settings.json` para optimizar VS Code para desenvolvemento web:

```json
{
  // Configuracións xerais
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "files.autoSave": "onFocusChange",
  "editor.minimap.enabled": true,

  // Formateo automático
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",

  // Configuracións específicas para HTML
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  },

  // Configuracións específicas para CSS/SCSS
  "css.validate": false,
  "scss.validate": false,
  "less.validate": false,

  // Configuracións específicas para JavaScript
  "javascript.updateImportsOnFileMove.enabled": "always",
  "javascript.suggest.autoImports": true,

  // Configuracións de temas e aparencia
  "workbench.colorTheme": "Default Dark+",
  "workbench.iconTheme": "material-icon-theme",

  // Configuracións de depuración
  "debug.console.fontSize": 12,
  "debug.console.wordWrap": "on"
}
```

---

### **3. Temas e iconos**
- **Tema(s) recomendado(s)**: `Default Dark+` (vén por defecto con VS Code) ou `Oceanic Next` (para unha aparencia máis moderna).  
  [:arrow_upper_right:](https://marketplace.visualstudio.com/items?itemName=naumovs.theme-oceanicnext)
- **Icon Pack**: `Material Icon Theme` para unha vista máis visual e organizada dos arquivos.  
  [:arrow_upper_right:](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)

---

### **4. Atallos de teclado útiles**
- **Abrir terminal integrado**: `Ctrl + `` (ou `Cmd + `` en Mac).
- **Embelecer código**: `Shift + Alt + F` (Windows/Linux) ou `Shift + Option + F` (Mac).
- **Comentar/Descomentar liña**: `Ctrl + /` (ou `Cmd + /` en Mac).
- **Buscar en tódolos arquivos**: `Ctrl + Shift + F` (ou `Cmd + Shift + F` en Mac).
- **Ir á definición**: `F12`.
- **Abrir o panel de extensións**: `Ctrl + Shift + X` (ou `Cmd + Shift + X` en Mac).

---

### **5. Fluxo de traballo recomendado**
1. **Escribe código HTML** usando **Emmet** para xerar estruturas rapidamente (por exemplo, escribe `!` e preme `Tab` para xerar un documento HTML básico).
2. **Conecta CSS e JavaScript** usando as rutas correctas nos arquivos HTML.
3. **Usa Live Server** para ver os cambios en tempo real no navegador.
4. **Formata o código** con **Prettier** a vontade ou cada vez que gardes.
5. **Depura o teu JavaScript** usando a consola do navegador ou as [ferramentas de depuración integradas en VS Code](https://learn.microsoft.com/es-es/microsoft-edge/visual-studio-code/microsoft-edge-devtools-extension/debugging-a-webpage).

---

### **6. Enlaces de interese**
- [Documentación oficial de VS Code](https://code.visualstudio.com/docs)
- [Lista de extensións recomendadas](https://code.visualstudio.com/docs/editor/extension-gallery)
- [Guía de Emmet para VS Code](https://code.visualstudio.com/docs/editor/emmet)

---

Con estas recomendacións, terás un entorno de desenvolvemento web altamente eficiente e personalizado en VS Code. Lembra que podes tamén traballar sen tanta axuda, así que incorpora ao teu fluxo de traballo aquilo que mellore a túa experiencia e sexa relevante para o teu proxecto. 😊


---

DAW🧊2026

#html
#DAW