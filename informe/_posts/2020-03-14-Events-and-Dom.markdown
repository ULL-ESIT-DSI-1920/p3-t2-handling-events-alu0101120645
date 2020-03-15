---
layout: post
title:  "Events and DOM nodes"
date:   2020-03-14 20:59:06 +0000
categories: jekyll update
---
**Events and DOM nodes**

Los controladores de eventos se registra en un determinado contexto, se pueden usar objetos contenidos en DOM. Estos objetos son invocados cuando ocurre el evento, en el ejemplo siguiente funciona cuando pulsamos el botón.

El método **addListener** permite añadir cualquier tipo de controlodores, en cambio el metodo **removeEventListener** elimina el controlador del elemento que tiene asignado,en el siguiente codigo se puede ver como una vez que se pulse el botón este dejara de funcionar.


```HTML
<button>Act-once button</button>
<script>
  let button = document.querySelector("button");
  function once() {
    console.log("Done.");
    button.removeEventListener("click", once);
  }
  button.addEventListener("click", once);
</script>
```

