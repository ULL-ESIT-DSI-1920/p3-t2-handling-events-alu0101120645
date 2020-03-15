---
layout: post
title:  "Default actions"
date:   2020-03-14 20:55:07 +0000
categories: jekyll update
---
**Default actions**

El metodo **preventDefault** permite al usuario a configurar el comportamiento de la pagina evitando que funcione de manera normal, por lo con este método podremos crear atajos en nuestra pagina mediante teclado o menú, aunque existen algunas limitaciones dependiendo del navegador en el que nos encontremos.


```HTML
<a href="https://developer.mozilla.org/">MDN</a>
<script>
  let link = document.querySelector("a");
  link.addEventListener("click", event => {
    console.log("Nope.");
    event.preventDefault();
  });
</script>
```