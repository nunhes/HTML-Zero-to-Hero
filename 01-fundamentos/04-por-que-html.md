# I. Por que os humanos inventaron HTML - Aprender frontend a fondo

> **O que pasou, pasou.  Agora o entendo.  Pero é máis difícil crer nas cousas de quen di medias verdades.** Tenet, de C.Dollan

## Por que deberías ler isto?

Se algunha vez viches a película de Kubrick de **2001: A odisea no espazo**, deberás ter visto a súa popular escena, na que un home-mono lanza un óso ao ceo e cando o óso alcanza o seu clímax, corta a escena para mostrar outra na que unha nave espacial está acelerando no espazo.

Contén unha mensaxe indirecta e heroica: "O mesmo home-mono que lanzou un óso ao ceo, por alegría e curiosidade, tamén foi o mesmo home que enviou naves ao espazo exterior".

É a idea da evolución. Como os humanos aprenderon a desenvolver mellores solucións e ferramentas, baseándose nos seus descubrimentos e coñecementos pasados.

Pero como se poden relacionar todas estas cousas co HTML? Estamos vivindo nunha era na que a web está a marcar tendencia! Hai aplicacións web, sitios web, blogs, tendas de comercio electrónico, redes sociais, xogos web e moito máis. Como se podería relacionar tal cousa cun home-mono e o seu óso? A resposta reside en como e con que propósito e en base a que conceptos, desenvolvidos anteriormente por humanos, se introduciu HTML.

E isto é o que imos aprender neste artigo. Abróchache o cinto de seguridade mentres imos facer unha viaxe fulgurante pola historia de HTML e a fundación da World Wide Web.

**❓ Como che pode ser útil este artigo?**  
       Este artigo non é un titorial ou non intenta ensinarche a escribir HTML. Só mostrar unha imaxe profunda do HTML e o seu propósito e fundamento. Se acabas de comezar a aprender desenvolvemento web, pode ser unha boa axuda para ti. E se es un desenvolvedor de frontend experimentado, pode ampliar a túa visión sobre o ambiente de desenvolvemento web.

**❓ Por que estou publicando esta serie?**  
       Porque despois de ter éxito nunha entrevista pero perder o traballo nunha semana, estaba motivado a aprender todo o relacionado co frontend, profundamente e pouco a pouco. Nesta serie compartirei con vós a experiencia e os coñecementos que reunín ao longo desta viaxe. Tamén podes ler máis neste artigo: [Por que tiven éxito na entrevista pero perdín o traballo!](https://dev.to/alimobasheri/why-i-succeeded-in-the-interview-but-lost-the-job-gej)

### Antes de Comezar...

**Pregunta**: Como todo o feito polos humanos, HTML tamén se desenvolveu para superar un desafío. Pero cal era o reto e como podería HTML, específicamente, axudar a resolvelo?

A resposta curta é que: HTML é a solución humana para compartir documentos. É unha linguaxe de marcado que simplifica o proceso de estruturación de documentos que se poden compartir no contexto da World Wide Web.

Pero a resposta longa é algo máis complexa. Primeiro debemos aprender como se desenvolveu HTML...

## 👨‍🔬 Nacido nun laboratorio de física❕

Non. HTML non estaba destinado a crear páxinas web usando a enerxía liberada pola excitación do átomo. Pero foi ideada por Sir Tim Berners-Lee, que ocupaba un posto na sección de servizos informáticos do CERN (o Laboratorio Europeo de Física de Partículas en Xenebra, Suíza) co fin de facilitar o proceso de transporte de documentos.

**❓ Que fixo que Tim Berners-Lee sentise o desexo de crear HTML?**

- O CERN é un centro para as reunións dos principais físicos onde se discutían e intercambiaban ideas revolucionarias sobre cousas que poden evolucionar e revolucionar a vida na terra.
  Así podemos concluír que os documentos oficiais, ou artigos ou manuscritos, etc. tiveron un gran uso nas súas reunións.

- Pero e se puidesen desfacerse de toda a molestia da accesibilidade a estes documentos e gardar o seu valioso tempo para pensar en teorías que poderían acabar coa vida humana na Terra cun fácil paso de partículas, en lugar de esperar tempo e tempo ata chegar a Xenebra e discutir durante horas con outros científicos, para que ao fin nunca se aceptaran as súas teorías?


De aí que Tim Berners-Lee tivo a idea de crear unha especie de hipertexto que puidera comportarse como un documento en papel e permitir ao lector navegar polas páxinas e os contidos facendo clic no que se coñecería como hipervínculos. E que todos estes documentos puideran ser transferidos a través das redes informáticas cun protocolo que axudara aos interesados a acceder a eles en todo o mundo tendo unha conexión a Internet. Así nacerían HTML(Hypertext Markup Language) e  HTTP (HyperText Transfer Protocol).

Seguramente, a Internet da que estamos a falar era diferente do que parece hoxe e os navegadores web e páxinas web iniciais tiñan moitas diferenzas coas de agora. A idea de Berners-Lee para a definición do tipo de documento HTML foi unha mestura de SGML e hipertexto. Pero que son estes dous? 

### 🦸‍♂️ Hipertexto: textos que só Superman pode ler

Ao definir 'hipertexto' debemos ter en conta que a palabra "hiper" non se usa no sentido dun texto moi longo ou de algo que ten millóns de palabras. Por suposto que Internet e o hipertexto son ferramentas útiles que facilitan o acceso a miles de millóns de páxinas de documentos, pero hipertexto significa especificamente: "Documentos que conteñen áncoras especiais a outros documentos. Pódese acceder a estas áncoras mediante o clic do rato ou a tecla, ou as pantallas táctiles. Activar estas áncoras faría que o navegador salte a outro documento".

- **A etiqueta de áncora ⚓**
  - ``<a href="http://example.com">Link text</a>``: A etiqueta ``<a>`` é unha das principais etiquetas HTML. A palabra 'a' é a primeira letra de "áncora"- *anchor*-. E acepta un atributo chamado ``href`` que significa *Hypertext Reference* e o seu valor é o destino ao que debe ir o navegador, tras a activación da áncora. Esta etiqueta mostrará unha ligazón no documento de hipertexto, cuxo enderezo é o valor do ``href``.

A terminoloxía do hipertexto era coñecida entre os académicos desde os anos corenta. Pero non foi ata que os primeiros PC gráficos cobraron vida, que os hipertextos puideron facerse realidade.
O desenvolvemento de hipertextos en PC incluía arquivos de documentos que consistían en botóns non que ao facer clic sobre eles, o sistema decidía que contido había que mostrar. Eran botóns como `paxina seguinte` e `paxina anterior` ou `Títulos dos capítulos` nunha táboa de contidos.

Non obstante, estes hipertextos só funcionaban nun ordenador e non podían acceder a documentos noutros ordenadores do outro lado do mundo. Para iso, Tim Berners-Lee decidiu implementar **HTTP**.

Explicar o que é HTTP e como funciona está fóra do ámbito deste artigo. <!--Coñecerémolo nalgúns artigos futuros desta serie onde leremos sobre Ajax.-->

Así que vexamos logo que é unha linguaxe de marcas e como SGML inspirou a sir Tim Berners-Lee.

### 🧾 Linguaxe de marcado: como definir elementos nun documento

Moitas veces atopeime con persoas en Internet que debatían se HTML é unha linguaxe de programación ou non. Para min a resposta pódese atopar tan facilmente como buscar o seu nome.
HTML significa **Hypertext Markup Language**. Ben, o nome en si non afirma que sexa unha linguaxe de programación, senón que é unha linguaxe de marcado. **Unha linguaxe de marcas é un texto lexible por humanos que usa etiquetas para definir elementos dentro dun documento.**

Para unha mellor comprensión podes botar unha ollada á publicación actual. Hai un título que di "Por que os humanos inventaron HTML". Supoñamos agora que necesitamos imprimir unha copia desta publicación e queremos que o título se imprima na esquina superior esquerda da páxina. A posición establécese previamente na impresora, pero a impresora debe saber cal é o título. En lugar de pasar o título á impresora por separado, definímolo no propio documento. Pero como?
Aí é onde a linguaxe de marcas vén ao noso rescate.
No texto que contén a linguaxe de marcas definimos unha etiqueta de título e pasámoslle o título que desexamos. A impresora, mentres analiza o texto, almacenará o valor do título e imprimirao na posición correcta.
Aquí tes un exemplo:

```html
<title>Por que os humanos inventaron HTML</title>
```

O exemplo anterior usa etiquetas HTML. Pero como hai diferentes linguaxes de marcado, poderiamos empregar calquera deles no seu propio entorno.
O seguinte é un exemplo da linguaxe de marcado Scribe:

```scribe
@Title(Por que os humanos inventaron HTML)
```

Entón, agora que temos unha boa idea de como unha linguaxe de marcas define os elementos nun documento, imos descubrir o que é SGML.

### 📋 SGML: como deberían definirse as linguaxes de marcado

SGML significa **'Standard Generalized Markup Language'** . Non é unha linguaxe de marcado en si, senón que é un estándar rexistrado pola ISO (International Standard Organization) que define os estándares para unha linguaxe de marcado.

- **Como pode ser útil SGML?**
  - Se estiveses a piques de desenvolver novas linguaxes de marcado, este estándar pode aplicarse a elas para que a linguaxe de marcado sexa compatible con diferentes plataformas. Dado que as linguaxes de marcado baseadas neste estándar compórtanse preto entre si e obedecen ás mesmas regras, pódense transferir facilmente a diferentes formatos e imprimirse facilmente. Así é como HTML pódese transformar facilmente en PDF, EPUB, XML, etc.


O propio SGML foi desenvolvido baseándose en GML **(Linguaxe de marcado xeralizado)** , desenvolvido anteriormente por IBM para os seus dispositivos de impresión. A estrutura dun documento en GML pode verse así:

```gml
:h1.O título vai aquí!
:p.Un parágrafo sobre o contido.
:h2.Un título para unha lista.
:ol.
:li.Elemento 1 da lista.
:li.Elemento 2 da lista.
:eol.
```

- **Que é o marcado '``:ol``'?**
  - ❗ Observa como `:ol` se usa para comezar unha lista ordenada e `eol` (fin de lista ordenada) se usa para declarar que o elemento lista remata alí.


O marcado imprimiría o seguinte documento:

------

#### O título vai aquí!

Un parágrafo sobre o contido.

##### Un título para unha lista.

1. Elemento 1 da lista.
2. Elemento 2 da lista.

------

En SGML substituíuse `:tagname. :etagname.` por `<tagname></tagname>`, que tamén se implementou en HTML.

Agora aparece unha nova pregunta. Como HTML implementou SGML?

### ✅ HTML cobra vida.

Cando Sir Burners-Lee comezou a dar a coñecer a súa idea de compartir hipertextos a través de Internet, fíxose ben coñecido entre os investigadores que o aprenderon que se convertería, no futuro, na principal ferramenta de comunicación.

- **Que pensaron as empresas sobre o HTTP nun principio?** 
  - As grandes empresas como HP ou IBM vírono útil só para os investigadores que querían compartir os seus documentos e simplificar a referencia. Para eles, o futuro da comunicación dependía en gran medida das compañías de telefonía e das solucións que puidesen atopar para o seu desenvolvemento.
  - Pois parece que estaban equivocados. Agora mesmo, a WWW é o fogar de miles de millóns de sitios web, que hoxe en día son algo máis que a investigación e os documentos oficiais.

Pero aínda así, Tim estaba só ao principio. Tivo que usar as súas propias habilidades informáticas para facer realidade os seus conceptos. Mesturou outros conceptos como hipertexto, SGML, etc. e tamén desenvolveu o seu propio protocolo de uso compartido que é **HTTP**. Despois puido reunir pequenos equipos e desenvolver o mundo da comunicación!

Pero como era o HTML ao principio?

#### HTML: A primeira versión.

Para un exemplo real podes visitar esta páxina: [The World Wide Web Project](http://info.cern.ch/hypertext/WWW/TheProject.html)
A ligazón anterior redirixirache á primeira páxina escrita en HTML. Se queres ver como se marcou a páxina, podes facelo facendo clic co botón dereito na páxina no navegador e seleccionar "Ver a fonte da páxina", ”Inspeccionar” ou outras opcións como estas.

Podemos ver de cerca a súa fonte:

```html
<HEADER>
  ...
</HEADER>
<BODY>
  ...
</BODY>
```

A fonte, como podes observar, consiste en etiquetas lexibles por humanos. Hai dúas etiquetas principais: `<HEADER>` e `<BODY>`.

Agora que decatámonos de que unha linguaxe de marcado tenta estimular un documento en papel, podemos entender facilmente de que tratan estas dúas etiquetas. Definen as dúas partes principais dun documento: 'Detalles' e 'Contidos'. É como moitos cartafoles de documentos que podes atopar en oficinas, escolas e noutros lugares. É probable que ti mesmo xa escribiras un documento deste tipo.

:mag: **Que fai realmente  "HEADER"? **


- Os detalles dá a etiqueta `<HEADER>` son diferentes dos que necesitamos saber sobre un documento en papel. A parte `<HEADER>` en realidade non está destinada a ser lida por humanos. Contén información que pode resultar útil a un navegador - ou tamén aos buscadores e indexadores de contidos-. Como que? Como un "título" ou un "conxunto de caracteres".


Imos ampliar a etiqueta `<HEADER>`:

```html
<HEADER>
  <TITLE>The World Wide Web project</TITLE>
  <NEXTID N="55">
</HEADER>
```

Dado que esta é unha versión moi elemental de HTML, só se definiron dúas etiquetas dentro de `<HEADER>`.

Unha delas é o título, que é simplemente un título ou un nome que se lle dá ao documento actual. Xa que os navegadores teñen que informar ao usuario sobre o que está mirando; o título é o que o navegador mostra na posición máis alta.

- O título é un dos elementos máis importantes dun documento HTML, baseado no feito de que se non se define ningún título, o usuario debe confiar no URL do enderezo HTTP para identificar que documento está mirando.

A etiqueta `<NEXTID>` se utilizaba exclusivamente como unha **axuda interna para editores de HTML automáticos**, e non estaba destinada a ser escrita a man polos desenvovledores, foi utilizada nas versións HTML elementais e producida polo editor **Next HTML** para xerar atributos `name` para as etiquetas `Anchor`, ou dito doutro xeito: levar a conta do seguinte identificador único que se debía asignar aos enlaces. Sinceramente, non sei moi ben como se utilizou. 😅 Ademais é unha etiqueta obsoleta dende fai moito tempo e xa non se usa.

##### Como pode axudarche unha comprensión profunda do desenvolvemento de HTML no desenvolvemento da web moderna?

- Podo adiviñar o que podes estar pensando agora: todo o que aprendemos ata agora é como se desenvolveron as linguaxes de marcado e como resultado a creación de HTML. Pero os feitos sobre os documentos e as súas estruturas de papel poden parecer irrelevantes para o funcionamento e o aspecto do contorno web na actualidade.
- Pero ese é o truco. Nada cambiou realmente. Todo o que ves na web, desde os xogos HTML5 ata as aplicacións web progresivas ata as animacións e gráficos SVG ben mantidos; todo isto, e moito máis, baséase sobre o concepto de estrutura do documento. Este concepto coñécese como **Document Object Model** ou **DOM**, sobre o que falaremos na segunda parte.
- Sei que ler isto pode parecer aburrido, longo e lento, pero podo apostar que reunindo estes coñecementos podes mergullar máis nas etiquetas semánticas HTML5, as mellores prácticas de deseño de CSS, o SEO e como un motor de busca tratará e analizará os `<head>` e `<body>` das túas aplicacións web, o *pipeline* de datos de JSX e como un DOM virtual pode facerse real e moitas cousas máis.
- Créeme, todos eles están baseados na simple idea de hipertexto 😊.

Agora que estás de novo cheo de enerxía e estás motivado para buscar as raíces profundas do HTML, vexamos que é `BODY` nun documento HTML.

Así é como a parte `<BODY>` está escrita no exemplo anterior:

```html
<BODY>
  <H1>World Wide Web</H1>The WorldWideWeb (W3) is a wide-area<A NAME=0 HREF="WhatIs.html"> 
hypermedia</A>
  ...
  <DL>
    <DT><A NAME=44 HREF="../DataSources/Top.html">What's out there?</A>
    <DD> Pointers to the
    world's online information,<A NAME=45 HREF="../DataSources/bySubject/Overview.html"> 
    subjects</A>
    , <A NAME=z54 HREF="../DataSources/WWW/Servers.html">W3 servers</A>, etc.
    <DT><A NAME=46 HREF="Help.html">Help</A>
    <DD> on the browser you are using
    ...
  </DL>
</BODY>
```

O que o corpo representa é un conxunto de elementos. Cada elemento é identificado mediante etiquetas. O texto que queda dentro dunha etiqueta chámase texto interno - `inner text`- e as etiquetas que aniñas dentro doutra etiqueta chámanse seus fillos - `children`-. A etiqueta principal chámase pai -`parent`-.
O texto interno é a parte que se imprime na páxina do navegador.

Pregunta: Pero por que debemos usar termos como irmáns, fillos e pais nunha estrutura HTML?
Resposta: porque a estrutura do documento HTML compórtase de xeito herdado.

O concepto herdanza - `inheritance`- vólvese máis importante cando tes que manexar unha disposición - `layout`-,  un posicionamento -`positioning`- e  unha visualización -`display`-. Hai un bo exemplo no marcado HTML anterior que demostra como `inheritance` axuda no deseño ou `layout`.

A etiqueta `<DL>` define unha `Description List`. O que mostra unha Lista de descricións é unha lista con  `items`, cada un deles cunha `description` propia.

- Un bo exemplo para unha Lista de descricións sería un dicionario.
  - Un documento de dicionario contén unha lista de palabras. E cada unha das palabras ten unha definición de si mesma.
  - As palabras son os `items` e as definicións son as `description`.

O exemplo anterior usa `<DL>` para mostrar unha lista de hipervínculos. Pódese dicir que cada hipervínculo está escrito como un **termo**  para indicarlle ao usuario a onde o leva, que á súa vez defínese cunha **descrición**. Este é o propósito obvio para a implementación desta `DL`. Pero tamén ten outro uso...

É `layout`. Se xa estás familiarizado co deseño web e CSS, saberás como as propiedades CSS como Flexbox ou Grid axudan co deseño.
Pero o proxecto inicial de hipertexto non definía ningunha forma de estilizar os contidos. E isto foi por unha boa razón. Porque Berners-Lee anticipou o feito de que HTML só tiña que conter estrutura e marcado do documento, concluíndo que a lóxica de estilo non debería implementarse no propio HTML. Isto fixo que HTML fose máis flexible. Ademais, unha estrutura de documento pode ser estilizada de diferentes xeitos, xa sexa polo usuario, polo autor ou polo navegador.

- **Que raios é CSS e que é Flexbox ou Grid?**
- CSS significa **Follas de estilo en cascada**. Unha folla de estilo é un conxunto de regras que aplican estilos a un documento. E a cascada significa que estas regras actúan como fervenzas de auga que anulan todo o que está debaixo de si mesmas.
  
  - Así, certas regras de estilo pódense cambiar ou anular en determinadas partes dun documento. Esta propiedade é diferente do comportamento de herdanza de HTML e tratarase en partes futuras.
  
  - Flexbox e Grid son algunhas propiedades de CSS usadas para o deseño HTML. Aliñan os contidos de forma a `list-like` e `table-like` respectivamente.

O que isto significa é que o elemento `description list` úsase para darlle ao contido impreso (ou renderizado) algún **deseño** e **estrutura** visual .
A estrutura realízase mostrando só un hipervínculo en cada liña e a súa descrición na seguinte liña. Esta estrutura facilita ao lector a lectura do documento.

Espero que este exemplo demostrara como se estruturaron inicialmente os documentos HTML. Incluso as versións HTML máis recentes seguen moitas destas regras. Así podes observar como e para que fins se desenvolveu HTML.

### E iso é todo por agora...!

Percorremos un longo camiño, describindo moitas cousas, que quizais xa coñecías.

- Pero o que intentaba conseguir escribindo este longo artigo era darche unha idea fundamental de como se definiron as tecnoloxías frontend.
- Na miña opinión, todo baséase na estrutura do documento, xa se trate de video reunións en liña ou de aplicacións sociais, ou de animacións gráficas.
- Ter un coñecemento firme da linguaxe de marcas e da metodoloxía de herdanza seguramente nos axudará durante toda a nosa viaxe para aprender frontend a fondo.
- Unha cousa importante sobre o DOM é o uso das etiquetas semánticas. Viches diferentes tipos destas etiquetas neste artigo. Inclúen `title`, `h1`, `list`, etc. Estas etiquetas son semánticas no sentido de que permiten ao navegador saber o papel que ten o seu contido no documento.
- Por exemplo, unha etiqueta `h1` significa que o seu texto interno é o título máis importante do documento actual e seguramente o seu texto interno contén información importante e descritiva sobre a sección actual.
- Aprender etiquetas semánticas é importante para o SEO, o deseño e mesmo para dominar a programación declarativa e baseada en compoñentes. E nas últimas definicións de HTML, introducíronse etiquetas semánticas máis novas que xogan un papel fundamental no desenvolvemento de mellores aplicacións frontend.
- Nas próximas partes imos utilizar o coñecemento recollido nesta primeira parte para mergullarnos máis no mar da programación frontend.

<!-- ### ~~Comentarios por favor!~~

~~Esta é unha publicación longa e tardei en anotala. E xa que estou pensando amplialo nunha serie gustaríame coñecer as vosas opinións e ideas ao respecto.~~

~~E o máis importante que todo: moitas cousas escritas neste post pódense clasificar como explicacións pensadas. Polo tanto, poderían existir explicacións e teorizacións opostas ou mellores. Se tes tales ideas, comentádeas.~~

~~Na seguinte parte volveremos co DOM.~~ -->

----

# II. Por que debería preocuparme polo DOM e a [entalpía](https://gl.wikipedia.org/wiki/Entalp%C3%ADa) negativa?

Na primeira parte deste artigo, decatámonos de que `HTML` é unha linguaxe de marcado - `Markup Language` - destinada a crear documentos. Agora sabemos que este documento é moi parecido a un documento en papel. Podemos usar diferentes elementos e sistemas de deseño en HTML para dar forma ao noso deseño ideal do documento.
Pero aínda así, hai unha pregunta. Se só se trata de documentos, entón os humanos puideron crealos hai miles de anos. Os documentos poden ser tallados na pedra, pintados en papiros e escritos en papel.
Polo tanto, aínda que `HTTP` facilita poder compartir o documento en todo o mundo, hai unha cousa importante que unha páxina web debe ser capaz de facer para, finalmente, ser superior a un documento simple.

E é a posibilidade de **actualizar os datos en tempo real, en resposta ás interaccións dos usuarios e a diferentes eventos**. Esta característica fai que os documentos sexan interactivos e empurra o límite dos documentos tradicionais que nunca se poderían editar nin actualizar. E especialmente esta é unha das habilidades principais que todo desenvolvedor frontend debe adquirir.

Ao longo deste artigo, imos aprender sobre o `Document Object Model`, abreviado como `DOM`. Na última parte, aprendemos sobre o **Documento**, agora intentaremos descubrir que é un **Obxecto** e como `DOM` implementa o **Modelo** .

Pero non imos por un camiño directo. Imos coñecer algunhas teorías básicas da programación informática. Isto inclúe variables, obxectos, coleccións, compiladores, etc. Isto é porque quero amosarche como ao final todas estas teorías configuran as funcionalidades internas dunha aplicación web frontend.
Así é como se nos presenta '*Tenet*' de Christopher Nolan. Mostrarache algunhas teorías e, ao final, enfrontarás todo na acción real. Entón imos mergullar máis a fondo!

Primeiras preguntas primeiro...

## 🏍️ Que é un obxecto?

Mentres unha motocicleta ten dúas rodas, un coche ten catro. Ambos son **obxectos**. Cada un coas súas características. Estes trazos poden variar de moitas maneiras.

A comparación que fixemos identifica a diferenza no reconto da propiedade común en dous obxectos distintos.

Un caso contrastado é a observación dunha galiña e unha motocicleta. Ambos poden moverse. E mentres a galiña utiliza as súas patas para este fin, a outra usa as súas rodas. A **acción** de movemento é posible para ambos, pero fano usando **ferramentas** bastante diferentes .

> ❗ En canto á programación, podemos expresar as accións como **Métodos** e as ferramentas como **Propiedades** .

Así, o elemento principal na Definición de obxectos é que **un conxunto de trazas dan forma ao obxecto** .

Coñecendo o que é unha definición de obxecto, pasemos a como se define un documento por ela.

## 🌴 Que é un modelo de obxectos?

C é unha linguaxe de programación. Tamén o é C++. Ambas as dúas coñécense como linguas de baixo nivel. Isto significa que terás que escribir miles de liñas de código para que un programa sinxelo funcione. Pero a cambio, os seus programas corren a velocidades máis altas. Porque ao escribir código nunha linguaxe de baixo nivel, o sistema necesita menos tradución do teu código para entender o que estás tentando montar.

Pero hai unha gran diferenza entre as dúas linguas das que falamos anteriormente. C++ é unha versión orientada a obxectos de C. Que significa isto?
Isto significa que podemos definir obxectos en programas C++ que posúan as súas propias características e accións.

Imos definir a orientación do obxecto en anacos máis pequenos. Isto facilitarache comprender a idea se aínda non a coñeces.

En primeiro lugar, imos comezar cunha cousa sinxela: valor. Iso é o que trata cada programa!

### 2️⃣ Ola PC, toma este 2!

Nun programa, cada valor gárdase nunha parte da memoria. Este valor identifícase mediante unha referencia. Unha referencia é un número específico que se dirixe a unha localización na memoria que contén un valor específico.

Esta referencia pode ser axeitada para realizar accións como o cálculo. Por exemplo, se queres calcular a suma de 2 e 3, tes que almacenar estes valores no sistema e, a continuación, darlle ao sistema o programa polo que debe sumar estes dous números.
Unha referencia ao valor 2 pode ser un número como 2452123 e unha referencia ao valor 3 pode ser outro número como 7892392.

O sistema pode xestionar estas referencias facilmente. Pero sería difícil para un humano traballar con eles. Esqueceriamos facilmente que puntos de referencia apuntan a que valor.

### 🤙 Chama ao meu 2, Ey!

Unha variable é simplemente un nome que lle damos a referencia a un valor. No último parágrafo, dixemos que nun sistema exemplar unha referencia ao número 2 é 2452123.
Agora, e se lle dixemos ao sistema que queremos que esta referencia se chame `a`; de xeito que cada vez que teñamos que sinalar este número simplemente deramos o seu nome e o sistema recuperara o valor por nós?

- Como as variables se asemellan á memoria dos humanos. 
  - Este comportamento está próximo a como os humanos almacenamos diferentes datos na nosa mente. Por exemplo, cando queremos referirnos a unha froita longa con tapa amarela, dicimos plátano. O valor foi recuperado!

### 🎙️ Hey PC, Repeat After Me: Ey equals 2!

Afortunadamente, a maioría das linguaxes de programación xestionan isto por nós.
Así é como definimos unha variable en JavaScript:

```javascript
let a = 2;
let b = 3;
```

No bloque de código anterior, declaramos dous valores, almacenámolos na memoria e dámoslles un nome personalizado para as súas referencias. Así, se queriamos sumar estes números simplemente dicimos ao sistema: `suma a e b`.
En JavaScript está escrito así:

```
let c = a + b;
```

- **Que pasou neste bloque de código?**
  - Aquí, nunha soa liña, realizamos tres accións. En primeiro lugar, recuperamos os dous valores 2 e 3 da memoria, chamando os seus nomes. Despois, engadimos estes dous números que dan como resultado un novo valor, 5. A continuación, o novo valor gárdase na memoria e dáselle un nome á súa referencia: `c`.

Ben, puxemos un nome ás referencias. Pero que ten que ver coa orientación a obxectos?

### ⛏️ A cousa ou o obxecto?

Ata agora, só definimos variables simples. Estes poden ser os fundamentos da programación, pero son insuficientes para un programa máis avanzado.

> O metal é un dos materiais máis útiles na construción, pero ao dar unha ollada xusta ao mundo que te rodea, é fácil concluír que os edificios non só están feitos de metais. Están ensamblados de cristales, metais, formigón, etc.

A mesma observación se aplica a un programa. Nunca está feito de valores únicos. Senón máis ben dunha colección deles.

### 👨‍👩‍👧‍👦 [Persoa 1, Persoa 2, Persoa 3]

Coñeces a xente polo seu nome, número de teléfono, aspecto, traballo e moito máis. Quizais coñezas a moita xente. Centos de nomes poden resultarche coñecidos.

De feito, tes unha colección de información na túa memoria. Unha colección de nomes, ou unha colección de diferentes marcas. Con todo, as coleccións son a principal forma de almacenamento de información.

> O que fai que as coleccións sexan axeitadas para este fin é a súa flexibilidade e sinxeleza na integración. Pode buscar, ordenar, filtrar ou manipular unha colección facilmente.

### 📊 Estruturas de datos

Probablemente, os algoritmos che sexan familiares. Se non, podes pensar no seguinte texto como un algoritmo:

> Vai á cociña. Busca nos armarios a lata de pementa vermella. Se a atopas, traga todo o contido da lata. Se non, vai ao conxelador. Saca todos os xeos que hai e trágaos un por un.

Como podes ver, un algoritmo é un conxunto de comandos paso a paso. Os programas informáticos instrúense utilizando estes algoritmos.

Pensemos no programa suma que escribimos anteriormente usando as variables. O seu algoritmo é sinxelo. Colle o primeiro número e engádeo ao segundo. Garda o resultado nunha nova localización de memoria.

Pero tamén hai colección?

### 🔢 Arrays

Ás veces cómpre almacenar diferentes valores como un grupo. Como unha lista de diferentes versións dunha frase. Podes almacenar cada valor nunha variable separada, pero esa non é a forma ideal. Porque, por exemplo, se tes que iterar pola lista e atopar unha versión específica, terás que comprobar cada valor manualmente para saber se é o valor desexado ou non.

As matrices veñen axudar.
Unha matriz é unha lista de enderezos de memoria. Por suposto, estes enderezos de memoria fan referencia a valores. Pero a súa diferenza cunha referencia normal é que se pode indexar.

- ***Que é a indexación? E como funciona unha matriz?***

  - Simplemente é como cando estás mirando unha lista de diferentes versións dunha frase e lle preguntas ao teu compañeiro sobre que versión lle gusta máis e el responde: "¡A **terceira** !"
  - Entón, a palabra clave aquí é `terceira`.
    Agora, se queriamos representar a lista do historial de versións nunha matriz JavaScript, quedaría así:

  ```javascript
  let versions = [
    'Unha sentenza.', 
    'Unha frase ben escrita.', 
    'Unha frase chusca!'
  ]
  ```

  - Para acceder á segunda frase e almacenala nunha nova variable abonda coa seguinte liña de JavaScript:

  ```javascript
  let aFraseDesexada = versions[1]
  ```
  
  - En JavaScript, as matrices están indexadas a partir de 0, o que significa que o índice do primeiro elemento é 0 e o índice do enésimo elemento é `n-1`.


A matriz é unha colección moi sinxela. Pero lembra cando falamos do programa de cálculo. Non constaba de ningunha matriz. Quizais poderiamos usar unha matriz de números e escribir un programa para calcular a suma de todos os números da matriz. Pero iso non é o que estamos tentando facer agora mesmo.

A cuestión era se, nese sinxelo programa, existía ou non unha colección. Agora, ningún dos valores eran coleccións, pero en realidade, todo o programa é unha colección.

Por que é iso?🧐

### 🔁 Recopilación de programas

Todo programa escrito nunha linguaxe ten que ser compilado en linguaxe máquina para actuar o máis rápido posible. A linguaxe máquina é a máis directa, pero ao ter o nivel máis baixo entre as linguaxes de programación, non é posible que os programadores interactúen con ela facilmente.
A solución dos *nerds* a este problema foi o desenvolvemento de linguaxes de programación de nivel superior. Si, incluso C++ ten un nivel superior en comparación co de Assembly.

Aínda así, hai un asunto sobre o que reflexionar. Se a comunicación coas máquinas é difícil, como é que os compiladores o fan e converten grandes anacos de código en lexibles por máquinas?

Para comprender o mecanismo que podes pensar en ti mesmo intentando falar unha lingua estranxeira, como o xestionarás?
En primeiro lugar, crearás modelos mentais.

Cal é o modelo mental? É o **concepto** ou o **significado** do que estás a traducir.

Como se concibe un modelo mental? Supón que queres dicirlle a un estranxeiro que lle arde a cara. Cal é o concepto detrás desta frase? Un rostro que pertence a esa persoa estase a derreter polo contacto coa calor?
Pero cal é o contexto? Quizais ti e a outra persoa esteades atrapados dentro dunha casa en chamas e estás a berrarlle para avisarlle de que lle arde a cara. Ou quizais estás empurrando o seu rostro na auga fervendo e gritando alegremente: "Ha! Ja! Ja! A túa cara arde!"

Ves? Diferentes contextos. Diferentes tons. Diferentes estruturas oracionais.

Agora como están relacionados coa tarefa dun compilador? Pois, en primeiro lugar, reúne todos os valores do teu programa. Estes valores son como o significado de cada palabra. A continuación, tenta dar forma a un modelo dos teus valores. Este modelo está configurado a partir dos diferentes ámbitos dentro dun código de programa.
Os ámbitos son diferentes bloques de código dentro dun programa. Estes bloques conteñen lóxicas autónomas, que poden funcionar independentemente doutras partes do código. Seguro que a maioría das veces os bloques usarán variables definidas noutros ámbitos ou pasadas como argumentos.

O compilador buscará os distintos bloques presentes nun código para dar forma ao seu modelo. Estes bloques axudarán a manter os niveis do modelo. Anteriormente aprendemos sobre as matrices que son as formas máis comúns de coleccións, pero das que falamos eran só unidimensionales. Non obstante, nos casos nos que precisamos especificar unha colección de grupos de valores, podemos simplemente aniñar matrices unhas dentro das outras.

En JavaScript, unha matriz aniñada pode verse así:

```javascript
let listaAninhada = [
  [1, 2, 3],
  [4, 5, 6]
]
```

No exemplo de código anterior, a variable `listaAninhada` podería ser un modelo de varios valores organizados en diferentes bloques. Gústame `block 0` e `block 1` así por diante. Deste xeito, o compilador saberá a que bloque pertence cada valor. Entón, se nalgún lugar do teu código intentas chamar a un valor que non está dispoñible no bloque correspondente, o compilador lanzará un erro.

Unha matriz aniñada pode ser un bo exemplo para ilustrar un modelo de colección, pero non é perfecto para un caso como o modelo dun compilador. Porque as matrices son só un grupo de valores nunha orde específica.

Así, os programadores deseñaron varios tipos de estruturas de datos que se poden utilizar para implementar coleccións de forma útil. Exemplos destas estruturas de datos inclúen listas vinculadas, filas, pilas, gráficos e táboas hash.

### Que estrutura de datos usa un compilador?

Os compiladores usan principalmente `Symbol Tables` como estrutura de datos primaria.
A `Symbol Table` é unha colección simbolizada de datos. Non te asustes se isto non ten sentido para ti, imos velo con máis detalle.

#### ⚛️ Que significa simbolizado?

Lembras cando falabamos de variables?
Gardamos un valor na memoria e despois puxémoslle un nome. Polo tanto, cada variable dun programa está formada por un grupo de información que inclúe: `memory reference`, `name`, `type` e `attribute`.
Usando estas propiedades, o compilador pode almacenar a información que precisa sobre unha variable particular nun único símbolo e despois implementar estes símbolos nun modelo máis grande que representa os bloques de código e os ámbitos, utilizando unha estrutura de datos.

Unha representación de `Symbol Tables` podería verse así:

```
<symbol name, type, attribute>
```

- ***Cales son o tipo e o atributo?***
  - JavaScript é unha linguaxe de tipo dinámico, o que significa que non tes que definir estrictamente o tipo dunha variable. Pero baixo o capó, cada valor posúe un tipo. Hai varios tipos incorporados como obxectos, cadeas, números, etc.
  - Estes tipos declaran o comportamento intrínseco das variables. Polo tanto, nun `Symbol Table`, cada valor contén unha declaración de tipo. O atributo é outro termo impopular en JS. En linguaxes como Java, existen palabras clave como `public` e `private` que se poden usar nunha declaración de variables para indicar en que contexto se pode usar a variable.
  - Os `let` e `const` son os dous atributos que se poden usar en JS. Por exemplo, usar o atributo  `const` aclara para o compilador que non se lle pode asignar un valor novo á variable despois da súa declaración inicial.


A estrutura de datos que utiliza un compilador para dar forma aos bloques de código pode variar entre `Linear Lists`, `Binary Search Tree`, e `Hash Tables`en función do arquitecto do compilador.

#### 💼 É suficiente unha estrutura de datos para que un compilador faga o seu traballo?

A resposta curta é **non**.
A resposta longa é que **unha estrutura de datos é só un modelo que pon os datos dispoñibles para ti**. Non expón métodos para traballar cos datos. Apenas é un esqueleto de datos.
Un esqueleto non se move por si só. Non pode tomar ningunha medida. Un corpo necesita músculos para poder manexar o seu esqueleto para un bo uso.
Polo tanto, o compilador utiliza os seus propios métodos integrados para traballar cos datos que se expón a el a través dos símbolos.


- Como é que esta estrutura de datos é semellante a unha base de datos? 

  - Cada símbolo é un `entry` e cada bloque de código chámase `block`. Poderías pensar nunha táboa de símbolos como unha base de datos. <!-- De feito, podo relacionarme persoalmente con isto, xa que actualmente estou traballando no desenvolvemento dunha aplicación de xestión de bases de datos baseada na web para o lugar no que traballo.-->
  - Cada cela dunha táboa de base de datos é como un `entry`. Unha cela pode ser un texto, un número, unha data e moitos máis campos. Cada un destes campos ten o seu propio tipo e atributos. Cada táboa tamén se pode dividir en diferentes fases e cada fase ten as súas propias filas de entradas.
  - Pero unha aplicación de xestión de bases de datos non está formada só por entradas e fases. Tamén se trata da ordenación dos datos, da súa agregación, edición, inserción, eliminación, validación, etc.
  - Cada unha destas funcionalidades tamén se pode xeneralizar a como se comporta habitualmente un compilador cunha táboa de símbolos.

### ⁉️ E agora?

Esta foi unha lectura longa, pero non inútil. Aprendemos sobre o progreso da compilación do programa e chegamos a recoñecer o que é unha estrutura de datos e como se define un obxecto.
Agora, é hora de volver ao bo camiño e aprender como se implementa o modelo de obxectos dun documento.

Pero primeiro, dediquemos uns segundos a pensar na resposta a unha pregunta fundamental da área de frontend.

#### 🤷‍♂️ HTML é unha estrutura de datos ou é un obxecto?

É tentador dicir que HTML é un `object` xa que posúe trazas como a `body` ou a `head` ou a `title`. Estas poden parecer trazas definidas para un obxecto.
Pero non o son e HTML definitivamente non é un `Object`. É un `Data Structure`. Todo o que fai HTML é expor datos.

> De feito, o programador que escribe o HTML estás expoñendo estes datos ao navegador. Usando a estrutura do documento da que falamos na última parte, estabas facendo o traballo do compilador.
> Ah, si! Quizais teñas escrito varios documentos HTML, ou quizais esteas experimentado, e usar o marcado HTML foi un traballo diario para ti. Pero nunca pensaches que estabas escribindo un arquivo de precompilación. Que estabas facendo o proceso de programación cunha entalpía negativa!

Parece tolo e parece o que Christopher Nolan presentou na súa película de 2020; Principio.

Percorreches un longo camiño para chegar a este punto, e quizais esteas canso ou pensas que este artigo foi inútil. Xa sei! Esta idea está a darche voltas á cabeza: estoume burlando de ti todo o tempo. Que os compiladores e estruturas de datos e a Orientación a Obxectos non teñen nada que ver cun HTML simple.
Pero ten paciencia. A partir de agora as cousas só melloraran.

![!](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sv5tsk8fdz7dc6vxh75w.gif)
Despois de todo, que esperas dunha idea Nolanish?😎

> **SPOILER FREE** : Non vou facer spoiler de nada do argumento da película. A teoría da entalpía negativa é algo que aprendes moi cedo na película. Así que desfruta!

### 🔀 Pero como está a suceder a entalpía negativa?

> Unha reacción química cunha entalpía negativa é aquela que perde enerxía ao longo do proceso.

Isto pode parecer demasiado teórico, pero podemos interpretalo na nosa materia como tal:

> Cando codificamos un programa e o compilador convérteo nun arquivo executable, mantemos enerxía facendo menos traballo por nós mesmos. O compilador é o que se encarga da molestia de traducir o noso código a programas lexibles pola máquina. Agora, cando escribimos HTML, estamos perdendo enerxía. Porque estamos a facer unha parte do traballo do compilador que é crear unha estrutura de datos - `data structure` -. Estamos facendo máis traballo para modelar a estrutura fina do documento para o noso propósito.

Pero `Data Structure` non é o único que crea o compilador. En realidade, fan falta diferentes métodos para poder traballar con estes datos.
Aquí é onde `Document Object Model` entra en xogo. E para nada, esta vez imos traballar con `objects`.

### 🗜️ Onde están os meus métodos?

Entón, dáslle ao navegador todos os datos necesarios no teu documento, organizados en estruturas aniñadas, segundo o teu deseño desexado, e esperas que a maxia ocorra.
Pero iso non é do que se trata cada aplicación. É? Hoxe en día as aplicacións web son algo máis que documentos científicos. Son os interfaces interactivos - `Interactive Interfaces` - que responden á interacción do usuario.

Os documentos actualízanse, cámbianse, inspeccionan, animan, estilizan e manipulan en tempo real. Se pensas en `HTML Document` como a `Symbol Table` que utiliza `DOM Methods`para traballar con esta estrutura de datos e cambiala, estás facendo o traballo do compilador.
Porque está a xestionar as estruturas e métodos de datos dispoñibles para producir o programa desexado.

Pero hai unha diferenza importante. O compilador compila unha vez, ti faralo moitas veces.

## Que segue?

<!--Orixinalmente, esta publicación pretendía--> … ter unha cobertura completa de todos os métodos cos que `DOM` nos serve. <!-- Pero esta noite decidín que escribir un artigo tan longo podería non ser un movemento sabio e que podería provocar a perda de atención dos queridos lectores.-->

<!-- Así que a nosa longa viaxe chega a unha pausa co coñecemento de --> [entender] que a xestión dunha aplicación frontend é como unha compilación en tempo real. <!-- Na seguinte parte, --> aprender<!--emos--> sobre os métodos do `DOM` e comparar<!--emos--> cada un deles co que fai un compilador.

<!--A seguinte parte é máis como--> un paseo de acción a través de como actualizar as diferentes partes dun documento, [como lidar cos posibles] <!--resulta en--> diferentes estados, e quizais [comprender certos] Principios!

[![Tenet gif. Pattinson: Que diaños pasou aquí? Washington: Aínda non pasou.](https://img.wattpad.com/bf019605b887fd08e749a36a1a216d27121d6a5a/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f776174747061642d6d656469612d736572766963652f53746f7279496d6167652f6546673544774f51744e706d58413d3d2d313037383235363037312e313638343036666665383038386539383336313735393735323638352e676966)

<!-- E espero que a seguinte parte saia máis rápido que esta. Xa que a maior parte xa está escrito!😁-->

<!-- ### O Fin! -->

<!-- E non esquezas darme comentarios. Estou tentando traer novas ideas a esta serie e, como todos os demais, as miñas ideas tamén teñen os seus propios defectos. Entón, encantaríame saber o que pensas!😅-->

[Learning Frontend Deeply (serie de 2 partes)](https://dev.to/alimobasheri/series/10573)

---

_.ref: _
-  https://dev.to/alimobasheri/why-humans-invented-html-learning-frontend-deeply-part-1-h1l_

- https://dev.to/alimobasheri/why-the-dom-causes-negative-enthalpy-learning-frontend-deeply-part-2-1k8n