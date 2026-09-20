# **Aniñado e Indentación en HTML**

Na lección anterior, aprendemos sobre as **listas ordenadas** e **desordenadas**. Nesta lección, imos profundizar nese concepto e aprender como **aniñar listas** dentro doutras listas.

---

### **Aniñado de Listas**

Xa vimos que podemos aniñar **elementos de lista** (`<li>`) dentro dunha lista desordenada (`<ul>`) ou ordenada (`<ol>`). Pero, ¿que pasa se queremos aniñar unha lista completa dentro doutra lista? Vexamos un exemplo:

#### **Exemplo de Lista Anidada**
```html
<ul>
  <li>A</li>
  <li>B
    <ol>
      <li>B1</li>
      <li>B2</li>
      <li>B3</li>
    </ol>
  </li>
  <li>C</li>
</ul>
```

Neste exemplo, a lista ordenada (`<ol>`) está anidada dentro do segundo elemento da lista desordenada (`<ul>`). Cando se renderiza no navegador, verás algo así:

- A
- B
  1. B1
  2. B2
  3. B3
- C

---

### **Importancia da Indentación**

A **indentación** é crucial cando traballamos con listas anidadas. Axuda a visualizar a estrutura do código e facilita a lectura. Por exemplo:

```html
<ul>
  <li>A</li>
  <li>B
    <ol>
      <li>B1</li>
      <li>B2
        <ul>
          <li>B2A</li>
          <li>B2B</li>
        </ul>
      </li>
      <li>B3</li>
    </ol>
  </li>
  <li>C</li>
</ul>
```

Neste caso, a indentación permite ver claramente como as listas están anidadas unhas dentro doutras. Sen indentación, o código sería moito máis difícil de ler e depurar.

---

### **Exercicio Práctico: Listas Anidadas Complexas**

Agora é o teu turno. Descarga os arquivos de inicio para este exercicio e crea unha lista anidada complexa. O obxectivo é replicar a seguinte estrutura:

1. **Lista Desordenada**:
   - A
   - B
     1. B1
     2. B2
        - B2A
        - B2B
     3. B3
        - B31
        - B32
   - C

#### **Pasos para o Exercicio:**
1. Crea unha lista desordenada (`<ul>`) con tres elementos: A, B e C.
2. Dentro do elemento B, anida unha lista ordenada (`<ol>`) con tres elementos: B1, B2 e B3.
3. Dentro de B2, anida unha lista desordenada (`<ul>`) con dous elementos: B2A e B2B.
4. Dentro de B3, anida unha lista ordenada (`<ol>`) con dous elementos: B31 e B32.

#### **Código de Exemplo:**
```html
<ul>
  <li>A</li>
  <li>B
    <ol>
      <li>B1</li>
      <li>B2
        <ul>
          <li>B2A</li>
          <li>B2B</li>
        </ul>
      </li>
      <li>B3
        <ol>
          <li>B31</li>
          <li>B32</li>
        </ol>
      </li>
    </ol>
  </li>
  <li>C</li>
</ul>
```

---

### **Consellos Adicionais**

- **Indentación Automática**: Ferramentas como **Visual Studio Code** indentan automaticamente o código cando gardas o arquivo (`Ctrl + S` en Windows ou `Cmd + S` en Mac). Aproveita esta funcionalidade para manter o teu código organizado.
- **Depuración**: Se algo non funciona como esperabas, usa a indentación para identificar erros. Por exemplo, se unha lista non se pecha correctamente, a indentación axudarache a detectar onde está o problema.
- **Lectura do Código**: A indentación non só é útil para ti, senón tamén para outras persoas que poidan ler o teu código no futuro.

---

### **Recursos Adicionais**

- **Documentación oficial de HTML**: [MDN Web Docs - Listas](https://developer.mozilla.org/es/docs/Web/HTML/Element/ul)
- **Visual Studio Code**: [Descarga VS Code](https://code.visualstudio.com/)
- **Guía de indentación en HTML**: [W3Schools - HTML Formatting](https://www.w3schools.com/html/html_formatting.asp)

---

### **Conclusión**

A anidación e a indentación son conceptos fundamentais para crear estruturas complexas en HTML. Dominar estas técnicas non só mellora a túa eficiencia como desenvolvedor, senón que tamén fai o teu código máis lexible e fácil de manter. Practica con este exercicio e, se tes dúbidas, non dubides en preguntar. 😊

---

**Nota**: Na próxima lección, imos aprender sobre **elementos de ancoraxe** (`<a>`) e como crear **hiperligazóns** en páxinas web. ¡Ata pronto! 🚀


---

DAW🧊2026

#html
#DAW