# Media, vídeo e son

O uso de **media** en HTML5 (*audio*, vídeo, incrustación de vídeos de YouTube, etc.) revolucionou a forma en que se incorporan elementos multimedia nas páxinas web. HTML5 introduciu etiquetas específicas para manexar audio e vídeo de forma nativa, sen necesidade de plugins externos como Flash. Vou explicarche todo sobre o uso de media en HTML5.

---

## **1. Audio en HTML5**
A etiqueta `<audio>` permíteche incorporar arquivos de audio nunha páxina web.

### **Etiqueta básica**:
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  O teu navegador non soporta o elemento de audio.
</audio>
```

### **Atributos importantes**:
- **`controls`**: Mostra os controis de reprodución (play, pause, volume).
- **`autoplay`**: Reproduce o audio automaticamente (non recomendado por cuestións de usabilidade).
- **`loop`**: Reproduce o audio en bucle.
- **`muted`**: Silencia o audio.
- **`preload`**: Especifica como se carga o audio (`auto`, `metadata`, `none`).

### **Formatos soportados**:
- **MP3**: `audio/mpeg`
- **WAV**: `audio/wav`
- **OGG**: `audio/ogg`

### **Exemplo con múltiples fontes**:
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
  O teu navegador non soporta o elemento de audio.
</audio>
```

---

## **2. Vídeo en HTML5**
A etiqueta `<video>` permíteche incorporar arquivos de vídeo nunha páxina web.

### **Etiqueta básica**:
```html
<video controls width="600">
  <source src="video.mp4" type="video/mp4">
  O teu navegador non soporta o elemento de vídeo.
</video>
```

### **Atributos importantes**:
- **`controls`**: Mostra os controis de reprodución.
- **`autoplay`**: Reproduce o vídeo automaticamente (non recomendado).
- **`loop`**: Reproduce o vídeo en bucle.
- **`muted`**: Silencia o vídeo.
- **`poster`**: Especifica unha imaxe de portada para o vídeo.
- **`width` e `height`**: Define o tamaño do vídeo.

### **Formatos soportados**:
- **MP4**: `video/mp4`
- **WebM**: `video/webm`
- **OGG**: `video/ogg`

### **Exemplo con múltiples fontes**:
```html
<video controls width="600" poster="poster.jpg">
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  O teu navegador non soporta o elemento de vídeo.
</video>
```

---

## **3. Incrustación de vídeos de YouTube**
Para incrustar vídeos de YouTube, podes usar o código de incorporación que proporciona YouTube.

### **Pasos**:
1. Ve ao vídeo de YouTube que queres incrustar.
2. Fai clic en **Compartir** e logo en **Incorporar**.
3. Copia o código iframe proporcionado.

### **Exemplo**:
```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

### **Personalización**:
- Cambia o `width` e `height` para axustar o tamaño.
- Engade `autoplay=1` ao URL para reproducir automaticamente (non recomendado).

---

## **4. Outros elementos multimedia**

### **a) `<iframe>`**
Úsase para incrustar contido externo, como mapas de Google, presentacións de SlideShare, etc.

- **Exemplo**:
  ```html
  <iframe src="https://www.google.com/maps/embed?pb=..." width="600" height="450" frameborder="0" style="border:0;" allowfullscreen></iframe>
  ```

### **b) `<object>` e `<embed>`**
Úsanse para incrustar contido multimedia, como arquivos PDF, Flash (obsoleto), etc.

- **Exemplo**:
  ```html
  <object data="documento.pdf" type="application/pdf" width="600" height="400">
    <p>O teu navegador non soporta PDFs. <a href="documento.pdf">Descarga o arquivo</a>.</p>
  </object>
  ```

---

## **5. Boas prácticas**
- **Accesibilidade**: Proporciona textos alternativos e subtítulos para audio e vídeo.
- **Optimización**: Usa formatos modernos como WebM para vídeo e OGG para audio.
- **Responsividade**: Asegúrate de que os elementos multimedia sexan responsivos (usa CSS ou atributos como `max-width`).
- **Autoplay**: Evita o autoplay, xa que pode ser molesto para os usuarios.

---

## **6. Exemplo completo**
Aquí tes un exemplo completo que inclúe audio, vídeo e un vídeo de YouTube:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Multimedia en HTML5</title>
</head>
<body>
  <h1>Audio en HTML5</h1>
  <audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    O teu navegador non soporta o elemento de audio.
  </audio>

  <h1>Vídeo en HTML5</h1>
  <video controls width="600" poster="poster.jpg">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    O teu navegador non soporta o elemento de vídeo.
  </video>

  <h1>Vídeo de YouTube</h1>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</body>
</html>
```

---

## **7. Resumo**
- **Audio**: `<audio>` con `<source>` para múltiples formatos.
- **Vídeo**: `<video>` con `<source>` para múltiples formatos.
- **YouTube**: Usa o código de incorporación de YouTube.
- **Outros**: `<iframe>`, `<object>`, `<embed>` para contido externo.

Se tes máis preguntas ou necesitas máis exemplos, avísame! 😊


---

DAW🧊2026

#html
#DAW