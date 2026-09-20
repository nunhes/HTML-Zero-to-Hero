# Listas e Enlaces

As listas e os enlaces son dous dos elementos máis importantes para a organización e a navegación en calquera sitio web.

---

## 1. Listas en HTML

As listas permiten agrupar elementos relacionados. Existen tres tipos principais:

### **a) Listas non ordenadas (`<ul>`)**
Úsanse para elementos onde a orde non é importante. Cada elemento da lista defínese con `<li>`.

```html
<ul>
  <li>Mazá</li>
  <li>Pera</li>
  <li>Plátano</li>
</ul>
```

### **b) Listas ordenadas (`<ol>`)**
Úsanse para elementos que seguen unha secuencia específica (ex: pasos dunha receita).

```html
<ol>
  <li>Pelar a froita</li>
  <li>Cortala en anacos</li>
  <li>Servir</li>
</ol>
```

### **c) Listas de descrición (`<dl>`)**
Úsanse para pares de termos (`<dt>`) e descricións (`<dd>`).

```html
<dl>
  <dt>HTML</dt>
  <dd>Linguaxe de marcado para a web.</dd>
  <dt>CSS</dt>
  <dd>Linguaxe de estilos para a web.</dd>
</dl>
```

---

## 2. Hiperenlaces (`<a>`)

Os enlaces créanse coa etiqueta `<a>` e o atributo `href`.

### **Tipos de enlaces**:
- **Externos**: `href="https://google.com"`
- **Internos**: `href="sobre-nos.html"`
- **Correo**: `href="mailto:exemplo@correo.com"`
- **Teléfono**: `href="tel:+34900000000"`

### **Atributos importantes**:
- **`target="_blank"`**: Abre o enlace nunha nova pestana.
- **`title`**: Mostra un texto ao pasar o rato.
- **`id` (Ancoras)**: Permite saltar a unha sección da mesma páxina.

```html
<a href="#contacto">Ir ao formulario de contacto</a>
...
<h2 id="contacto">Contacto</h2>
```

---

## 3. O modelo 'One-page-site'

Un **One-page-site** é aquel onde todo o contido vive nunha única páxina. A navegación realízase mediante ancoras (`#id`) que desprazan ao usuario ás diferentes seccións.

### **Vantaxes**:
- Navegación fluída e intuitiva.
- Carga rápida de toda a información.
- Ideal para móbiles.

---

## 4. Imaxes con enlaces e Mapas

As imaxes tamén poden actuar como enlaces:
```html
<a href="https://exemplo.com">
  <img src="logo.png" alt="Ir ao inicio">
</a>
```

Os **mapas de imaxe** (`<map>`) permiten definir múltiples áreas clicables nunha soa imaxe usando coordenadas.

---

**Resumo**:
As listas axudan a estruturar os datos, e os enlaces conectan o teu contido co resto do mundo dixital.

---

DAW🧊2026
