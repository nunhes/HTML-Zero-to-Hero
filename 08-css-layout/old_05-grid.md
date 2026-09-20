## A etiqueta `<meter>`

A etiqueta `<meter>` permite representar visualmente **valores nun rango coñecido**, ideal para mostrar medidas como:
- Nivel de carga dunha batería  
- Uso de almacenamento nun disco  
- Forza dun contrasinal  
- Resultados de enquisas  

### Atributos principais

| Atributo   | Descrición                                  | Valor predeterminado |
|------------|--------------------------------------------|----------------------|
| `value`    | Valor actual (obrigatorio)                 | -                    |
| `min`      | Valor mínimo do rango                      | 0                    |
| `max`      | Valor máximo do rango                      | 1                    |
| `low`      | Límite inferior para valores "baixos"      | -                    |
| `high`     | Límite superior para valores "altos"       | -                    |
| `optimum`  | Valor ideal dentro do rango                | -                    |

### Exemplos básicos

#### 1. Uso de disco (escala 0-100)
```html
<meter 
  min="0" 
  max="100" 
  value="75"
  aria-label="Uso de disco">
  75 GB usados de 100 GB
</meter>
```

#### 2. Forza do contrasinal
```html
<meter 
  min="0" 
  max="5" 
  value="3"
  low="2" 
  high="4"
  optimum="5"
  aria-label="Forza do contrasinal">
  Forza media (3/5)
</meter>
```

### Zonas de valoración

Os atributos `low`, `high` e `optimum` permiten crear zonas visuais:

```html
<!-- Exemplo: Nivel de almacenamento -->
<meter
  min="0"
  max="500"
  value="420"
  low="100"
  high="400"
  optimum="300"
  aria-label="Almacenamento en nube">
  420 MB usados (Límite: 500 MB)
</meter>
```

**Comportamento por zonas**:
- **Valor < low**: Alerta visual (vermello/naranxa)  
- **low < Valor < high**: Zona normal (verde)  
- **Valor > high**: Alerta visual (vermello)  

### Boas prácticas

1. **Accesibilidade**:
   ```html
   <meter 
     aria-labelledby="disk-label"
     role="meter"
     aria-valuetext="75% de capacidade">
   </meter>
   <span id="disk-label" hidden>Uso do disco duro</span>
   ```

2. **Fallback para navegadores antigos**:
   ```html
   <meter value="0.7">
     <div class="meter-fallback">
       <div style="width:70%"></div>
       <span>70% completo</span>
     </div>
   </meter>
   ```

3. **Estilización CSS**:
   ```css
   meter {
     width: 300px;
     height: 25px;
   }

   /* Estilos para WebKit */
   meter::-webkit-meter-bar {
     background: #eee;
     border-radius: 10px;
   }

   meter::-webkit-meter-optimum-value {
     background: #4CAF50;
   }

   meter::-webkit-meter-suboptimum-value {
     background: #FFC107;
   }

   meter::-webkit-meter-even-less-good-value {
     background: #F44336;
   }
   ```

### 📚 Recursos adicionais
1. [Documentación MDN sobre `<meter>`](https://developer.mozilla.org/gl/docs/Web/HTML/Element/meter)  
2. [Diferenzas entre `<meter>` e `<progress>`](https://css-tricks.com/html5-meter-element/)  
3. [Patróns ARIA para medidores](https://www.w3.org/WAI/ARIA/apg/patterns/meter/)  

---

**Notas importantes**:  
- Non usar para datos temporais (utiliza `<progress>`)  
- O aspecto visual varía entre navegadores  
- Combinar sempre con texto descriptivo para accesibilidade  
- Valores deben estar sempre entre `min` e `max`


---

DAW🧊2025

#html
#DAW