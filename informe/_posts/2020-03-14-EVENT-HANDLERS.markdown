---
layout: post
title:  "Event handlers"
date:   2020-03-14 20:55:06 +0000
categories: jekyll update
---
**Event handlers**

Los controladores de eventos se tratan de aquellas funciones que nos permite hacer una función cuando pulsamos en esta.

Con el codigo siguiente lo que haremos sera leer cuando el usuario hace click en cualquier lado de la ventana del navegador ya que el enlace "window" permite resgistrar los click en toda la pagina.

```HTML
<p>Click this document to activate the handler.</p>
<script>
  window.addEventListener("click", () => {
    console.log("You knocked?");
  });
</script>
```