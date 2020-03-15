---
layout: post
title:  "Keys events"
date:   2020-03-14 20:58:07 +0000
categories: jekyll update
---
**Key events**

Los eventos por clave se trata de leer las teclas del teclado una vez se pulsa o mantiente se siguen enviado repetidamente hasta que dejamos de pulsar la tecla, por lo que habrá que tener cuidado cuando se use un botón DOM ya que cuando se presiona una tecla y lo elimina nuevamente cuando se suelta la tecla, puede agregar accidentalmente cientos de botones.

El siguiente codigo de ejemplo, funciona cuando pulsamos la tecla **V** pondrá el fondo de la página en "violeta".

```HTML
<p>This page turns violet when you hold the V key.</p>
<script>
  window.addEventListener("keydown", event => {
    if (event.key == "v") {
      document.body.style.background = "violet";
    }
  });
  window.addEventListener("keyup", event => {
    if (event.key == "v") {
      document.body.style.background = "";
    }
  });
</script>
```