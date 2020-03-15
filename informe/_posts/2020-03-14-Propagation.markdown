---
layout: post
title:  "Propagation"
date:   2020-03-14 20:58:17 +0000
categories: jekyll update
---
##### Propagation
El método **stopPropagation** usado para evitar que los controladores reciban el evento.

**Target** se trata de unapropiedad para lanzar una red amplia para un tipo específico de evento, se puede usar esta propiedad para asegurarnos que no está manejando accidentalmente algo que se propagó desde un nodo que no desea manejar.


```HTML
<p>A paragraph with a <button>button</button>.</p>
<script>
  let para = document.querySelector("p");
  let button = document.querySelector("button");
  para.addEventListener("mousedown", () => {
    console.log("Handler for paragraph.");
  });
  button.addEventListener("mousedown", event => {
    console.log("Handler for button.");
    if (event.button == 2) event.stopPropagation();
  });
</script>
```