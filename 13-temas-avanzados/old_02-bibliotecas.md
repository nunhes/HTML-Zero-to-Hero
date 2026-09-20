# A cor en CSS

> Todo o que necesitas saber sobre a **cor en CSS**, incluíndo as súas características, tipos e modelos de cor, o seu uso, as implicacións na accesibilidade, a psicoloxía da cor e moito máis.

---

## **1. Características da cor en CSS**

En CSS, a cor pódese aplicar a varios elementos, como o texto, o fondo, os bordos, etc. As principais propiedades relacionadas coa cor son:

- **`color`**: Define a cor do texto.
- **`background-color`**: Define a cor de fondo dun elemento.
- **`border-color`**: Define a cor do bordo dun elemento.
- **`opacity`**: Controla a transparencia dun elemento (de 0 a 1).

Exemplo:
```css
p {
  color: red;
  background-color: yellow;
  border: 2px solid blue;
  opacity: 0.8;
}
```

---

## **2. Tipos e modelos de cor en CSS**

En CSS, podes definir as cores de varias maneiras. Aquí tes os principais tipos e modelos de cor:

#### **Tipos de cor**
1. **Nomes de cores predefinidos**: CSS ten ~140 nomes de cores predefinidos, como `red`, `blue`, `green`, etc.

   ```css
   p {
     color: tomato;
   }
   ```

2. **Cores hexadecimais**: Defínense cun símbolo `#` seguido de 6 díxitos hexadecimais (RRGGBB).

   *Decimal: 0,1,2,3,4,5,6,7,8,9   | Hexadecimal: 0,1,2,3,4,5,6,7,8,9,a,b,c,d,e,f*

   ```css
   p {
     color: #ff5733;
   }
   ```

3. **RGB e RGBA**: Defínense usando valores de vermello, verde e azul (0-255). RGBA inclúe un valor adicional para a transparencia (0-1).
   ```css
   p {
     color: rgb(255, 87, 51);
     background-color: rgba(255, 87, 51, 0.5);
   }
   ```

4. **HSL e HSLA**: Defínense usando matiz (Hue), saturación (Saturation) e luminosidade (Lightness). HSLA inclúe un valor adicional para a transparencia.
   ```css
   p {
     color: hsl(14, 100%, 60%);
     background-color: hsla(14, 100%, 60%, 0.5);
   }
   ```

#### **Modelos de cor**
- **RGB (Red, Green, Blue)**: Baseado na combinación de luz vermella, verde e azul.
- **HSL (Hue, Saturation, Lightness)**: Baseado na matiz, saturación e luminosidade, o que o fai máis intuitivo para axustar cores.
- **Hexadecimal**: Unha representación compacta de RGB.

---

## 3. O **canal alfa**

O **canal alfa** é un concepto moi importante no uso moderno de cores en CSS, xa que permite controlar a **transparencia** dunha cor. Isto é especialmente útil para crear deseños máis dinámicos e visuais atractivos, permitindo que os elementos se superpoñan ou se mesturen de maneira máis fluída.

Vexamos como funciona o canal alfa en CSS e como podes usalo nos diferentes modelos de cor.

---

### **3.1. Que é o canal alfa?**

O **canal alfa** é un valor adicional que se engade a unha cor para controlar a súa **transparencia**. Este valor vai de **0** (completamente transparente) a **1** (completamente opaco). O canal alfa permíteche facer que unha cor sexa parcialmente transparente, o que é moi útil para crear efectos visuais como superposicións, degradados ou fondos semitransparentes.

---

### **3.2. Modelos de cor con canal alfa en CSS**

En CSS, podes usar o canal alfa en varios modelos de cor. Aquí tes os máis comúns:

#### **RGBA (Red, Green, Blue, Alpha)**
O modelo **RGBA** engade un cuarto valor ao modelo RGB tradicional para controlar a transparencia.

- **Sintaxe**: `rgba(red, green, blue, alpha)`
- **Exemplo**:
  ```css
  background-color: rgba(255, 0, 0, 0.5); /* Vermello cun 50% de transparencia */
  ```

#### **HSLA (Hue, Saturation, Lightness, Alpha)**
O modelo **HSLA** funciona de maneira similar a RGBA, pero usa matiz, saturación e luminosidade en lugar de valores RGB.

- **Sintaxe**: `hsla(hue, saturation, lightness, alpha)`
- **Exemplo**:
  ```css
  background-color: hsla(120, 100%, 50%, 0.3); /* Verde cun 30% de transparencia */
  ```

#### **Cores hexadecimais con canal alfa**
A partir de CSS Color Module Level 4, podes engadir un canal alfa ás cores hexadecimais usando 8 díxitos en lugar de 6. Os últimos dous díxitos representan o valor alfa.

- **Sintaxe**: `#RRGGBBAA`
- **Exemplo**:
  ```css
  background-color: #ff000080; /* Vermello cun 50% de transparencia */
  ```

#### **Propiedade `opacity`**
Aínda que non é un modelo de cor, a propiedade `opacity` tamén controla a transparencia dun elemento completo, incluíndo o seu contido e fillos.

- **Sintaxe**: `opacity: value;` (onde `value` vai de 0 a 1).
- **Exemplo**:
  ```css
  div {
    opacity: 0.5; /* O elemento e todo o seu contido serán semitransparentes */
  }
  ```

---

### **3.3. Diferenzas entre `opacity` e o canal alfa**

- **`opacity`**: Afecta a todo o elemento, incluíndo o texto e outros elementos fillos. Se defines `opacity: 0.5`, todo o contido do elemento terá un 50% de transparencia.
- **Canal alfa**: Afecta só á cor específica á que se aplica. Por exemplo, se usas `rgba(255, 0, 0, 0.5)`, só o fondo será semitransparente, pero o texto seguirá sendo completamente opaco.

---

### **3.4. Usos comúns do canal alfa**

O canal alfa é moi útil en moitos escenarios de deseño web:

#### **Superposicións (Overlays)**
Podes crear fondos semitransparentes para superpoñer texto ou imaxes.
```css
.overlay {
  background-color: rgba(0, 0, 0, 0.5); /* Fondo negro cun 50% de transparencia */
}
```

#### **Degradados (Gradients)**
Os degradados poden incluír transparencia para crear efectos visuais interesantes.
```css
background: linear-gradient(to right, rgba(255, 0, 0, 0.5), rgba(0, 0, 255, 0.5));
```

#### **Sombreados (Shadows)**
Podes usar cores con canal alfa en sombreados para crear efectos máis sutís.
```css
box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
```

#### **Botóns e enlaces**
Podes usar cores semitransparentes en botóns ou enlaces para crear efectos de hover ou estados activos.
```css
button {
  background-color: rgba(0, 123, 255, 0.8);
}

button:hover {
  background-color: rgba(0, 123, 255, 1);
}
```

---

### **3.5. Exemplo práctico**

Aquí tes un exemplo completo que mostra como usar o canal alfa en diferentes contextos:

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Canal Alfa en CSS</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    .header {
      background-color: rgba(0, 0, 0, 0.7); /* Fondo negro cun 70% de transparencia */
      color: white;
      padding: 20px;
      text-align: center;
    }

    .overlay {
      background-color: rgba(255, 255, 255, 0.8); /* Fondo branco cun 80% de transparencia */
      padding: 20px;
      margin: 20px;
      border-radius: 10px;
    }

    .gradient-box {
      background: linear-gradient(to right, rgba(255, 0, 0, 0.5), rgba(0, 0, 255, 0.5));
      height: 100px;
      margin: 20px;
    }

    .shadow-box {
      background-color: white;
      padding: 20px;
      margin: 20px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Sombra con transparencia */
    }

    button {
      background-color: rgba(0, 123, 255, 0.8); /* Azul cun 80% de transparencia */
      color: white;
      border: none;
      padding: 10px 20px;
      cursor: pointer;
      border-radius: 5px;
    }

    button:hover {
      background-color: rgba(0, 123, 255, 1); /* Azul completamente opaco ao pasar o rato */
    }
  </style>
</head>
<body>
  <div class="header">
    <h1>Uso do Canal Alfa en CSS</h1>
  </div>

  <div class="overlay">
    <p>Este é un exemplo de fondo semitransparente.</p>
  </div>

  <div class="gradient-box"></div>

  <div class="shadow-box">
    <p>Este é un exemplo de sombreado con transparencia.</p>
  </div>

  <button>Botón con transparencia</button>
</body>
</html>
```

---

### **3.6. Conclusión**

O **canal alfa** é unha ferramenta poderosa en CSS que permite controlar a transparencia das cores. Podes usalo en modelos como **RGBA**, **HSLA** e cores hexadecimais con 8 díxitos para crear efectos visuais avanzados, como superposicións, degradados e sombreados. Ademais, é importante entender a diferenza entre o canal alfa e a propiedade `opacity`, xa que cada un ten usos específicos.

Espero que esta explicación e exemplo che sexan útiles para explorar as posibilidades do canal alfa en CSS! 😊

---

## **4. Uso da cor en CSS**

A cor úsase en CSS para mellorar o deseño e a usabilidade dunha páxina web. Aquí tes algúns usos comúns:

- **Destacar elementos importantes**: Usa cores contrastantes para chamar a atención sobre botóns ou enlaces.
- **Crear xerarquía visual**: Usa cores diferentes para títulos, subtítulos e texto normal.
- **Establecer un tema visual**: Define unha paleta de cores para crear unha identidade visual consistente.

**Exemplo:**

```css
body {
  background-color: #f4f4f4;
  color: #333;
}

h1 {
  color: #ff5733;
}

button {
  background-color: #28a745;
  color: white;
}
```

---

## **5. Implicacións na accesibilidade**

A accesibilidade é crucial cando se usan cores en CSS. Aquí tes algunhas prácticas recomendadas:

- **Contraste suficiente**: Asegúrate de que hai suficiente contraste entre o texto e o fondo. A relación de contraste recomendada é de **4.5:1** para texto normal e **3:1** para texto grande.
- **Non confiar só na cor**: Non uses só a cor para transmitir información. Por exemplo, usa iconas ou texto adicional para indicar erros ou estados.
- **Probar con ferramentas**: Usa ferramentas como [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) para verificar o contraste das cores.

**Exemplo accesible:**

```css
.error {
  color: #d9534f;
  border: 1px solid #d9534f;
  padding: 10px;
}
```

---

## **6. Psicoloxía da cor**

A cor ten un impacto psicolóxico nos usuarios e pode influír na súa percepción e comportamento. Aquí tes algúns puntos clave:

- **Vermello**: Asóciase con enerxía, urxencia e pasión. Úsase para chamar a atención ou indicar erros.
- **Azul**: Transmite confianza, calma e profesionalismo. Común en sitios web corporativos.
- **Verde**: Asóciase con natureza, saúde e éxito. Úsase para indicar accións positivas ou ecoloxía.
- **Amarelo**: Representa optimismo e atención. Úsase para destacar información importante.
- **Negro e branco**: Son cores neutras que se usan para crear contraste e elegancia.

**Exemplo de uso psicolóxico da cor:**

```css
button.primary {
  background-color: #007bff; /* Azul para confianza */
  color: white;
}

button.danger {
  background-color: #dc3545; /* Vermello para urxencia */
  color: white;
}
```

---

## **7. Ferramentas e recursos útiles**

- **Paletas de cores**: Ferramentas como [Coolors](https://coolors.co/) ou [Adobe Color](https://color.adobe.com/) axúdanche a crear paletas de cores harmoniosas.
- **Verificación de contraste**: Usa [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) para asegurarte de que as cores son accesibles.
- **Generadores de gradientes**: Ferramentas como [CSS Gradient](https://cssgradient.io/) axúdanche a crear gradientes complexos.

---

## **Exercicio práctico**

#### **Obxectivo**
Practicar o uso de cores en CSS, crear unha paleta de cores accesible e aplicar a psicoloxía da cor nun deseño web.

#### **Instrucións**
1. **Crea unha paleta de cores**: Usa unha ferramenta como Coolors para xerar unha paleta de 5 cores.
2. **Define estilos CSS**:
   - Usa as cores da paleta para definir estilos para o texto, fondo, botóns e enlaces.
   - Asegúrate de que o contraste entre o texto e o fondo cumpre as normas de accesibilidade.
3. **Aplica a psicoloxía da cor**:
   - Usa cores que transmitan confianza para os botóns principais.
   - Usa cores que indiquen urxencia ou erro para mensaxes de alerta.
4. **Proba o contraste**: Usa unha ferramenta de verificación de contraste para asegurarte de que as cores son accesibles.

#### **Exemplo de solución**

```html
<!DOCTYPE html>
<html lang="gl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Práctica de Cor en CSS</title>
  <style>
    /* Paleta de cores */
    :root {
      --primary: #007bff; /* Azul para confianza */
      --secondary: #6c757d; /* Gris para neutralidade */
      --success: #28a745; /* Verde para éxito */
      --danger: #dc3545; /* Vermello para urxencia */
      --warning: #ffc107; /* Amarelo para advertencia */
    }

    body {
      background-color: #f8f9fa;
      color: #333;
      font-family: Arial, sans-serif;
    }

    h1 {
      color: var(--primary);
    }

    button {
      padding: 10px 20px;
      border: none;
      color: white;
      cursor: pointer;
    }

    button.primary {
      background-color: var(--primary);
    }

    button.danger {
      background-color: var(--danger);
    }

    .alert {
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
    }

    .alert.success {
      background-color: var(--success);
      color: white;
    }

    .alert.warning {
      background-color: var(--warning);
      color: black;
    }
  </style>
</head>
<body>
  <h1>Práctica de Cor en CSS</h1>
  <button class="primary">Botón Primario</button>
  <button class="danger">Botón de Peligro</button>

  <div class="alert success">Operación exitosa!</div>
  <div class="alert warning">Advertencia: Isto é importante.</div>
</body>
</html>
```

---

## **Conclusión**
A cor en CSS é unha ferramenta poderosa para mellorar o deseño e a usabilidade dunha páxina web. Coñecer os tipos de cor, a súa psicoloxía e as implicacións na accesibilidade é esencial para crear experiencias de usuario efectivas e inclusivas. Espero que este resumo e exercicio che sexan útiles! 😊


---

DAW🧊2025

#css
#DAW