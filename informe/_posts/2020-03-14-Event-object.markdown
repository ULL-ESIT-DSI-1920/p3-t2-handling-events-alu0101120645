---
layout: post
title:  "Event objects"
date:   2020-03-14 20:55:07 +0000
categories: jekyll update
---
**Event objects**

El Event Object se pasa a la funcion controladora como un argumento, conteniendo información sobre el evento que puede tener unas propiedades determinadas, en el siguiente codigo se ve como obtenemos que tipo de click estamos haciendo con el raton sobre el botón.

```HTML

  <button>Click me any way you want</button>
    <script>
      let button = document.querySelector("button");
      button.addEventListener("mousedown", event => {
        if (event.button == 0) {
          console.log("Left button");
        } else if (event.button == 1) {
          console.log("Middle button");
        } else if (event.button == 2) {
          console.log("Right button");
        }
      });
    </script>
```