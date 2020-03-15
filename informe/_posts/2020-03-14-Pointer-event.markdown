---
layout: post
title:  "Pointer events"
date:   2020-03-14 20:55:07 +0000
categories: jekyll update
---
**Pointer events**

Existen dos formas para señalar por pantalla, que se trata del ratón y las pantallas táctiles

##### Mouse clicks:
 Existen metodos parecidos a los de teclado pero en este caso son **"mousedown"** y **"mouseup"** , funcionan en los nodos DOM que en los que se encuentra el puntero del ratón.

Cuando queremos obtener la informacion del lugar del suceso, existe la propiedad **clientX** y **clientY**  que obtiene las coordenadas delevento en pixeles 

El siguiente [codigo](/ejemplos/Mouse_clicks.html) su función es poner un punto de clolor justo debajo del puntero cunado hacemos click. 

##### Mouse motion: 

Siempre que se mueve el ratón un evento "mousemove", es util  para rastrear la posición del ratón.

En el código de ejemplo que se nos da podemos ver que su objetivos es alargar o estrecha de izquiera a derecha según necesitemos una barra, al tener "window" si nos salimos de la barra continuara moviendo la barra hasta que soltemos el click.

##### Touch Event :

Cuando se comienza a tocar la pantalla se obtiene un evento **touchstart**, cuando nos movemos mientras mantenemos seran los eventos **touchmove** y cuando dejemos de precionar será el evento **touchend**. 

##### Scroll events :

Cada vez que usamos el scroll de ratón este activara un evento. Los principales usos de este tipo de evento es ver que parte de la pagina está mirando el usuario asi como realizar acciones cada a la vez que baja con el scroll.

##### Focus Event: 


A medida que el usuario navega por una pagina, es inevitable que tenga que interactuar con alguno de los elementos dispuestos dentro
del contenido de dicha pagina. Se le llama `focus` a aquel elemento que esta actualmente en interaccion directa con el usuario, de 
modo que si el usuario selecciona un `textbox` dicho elemento sera el que tenga el focus actual de la ventana, lo que le permitira al
usuario al momento de escribir, que el contenido sea enviado a dicha `textbox`.

Podemos encontrar un ejemplo de esto, en donde tendremos dos campos para introducir informacion, y vemos que
al principio los marcos son de color negro, y al seleccionarlos, obtienen el focus y cambian a un gris.
```HTML
    <p>Name: <input type="text" data-help="Your full name"></p>
    <p>Age: <input type="text" data-help="Your age in years"></p>
    <p id="help"></p>

    <script>
    let help = document.querySelector("#help");
    let fields = document.querySelectorAll("input");
    for (let field of Array.from(fields)) {
        field.addEventListener("focus", event => {
        let text = event.target.getAttribute("data-help");
        help.textContent = text;
        });
        field.addEventListener("blur", event => {
        help.textContent = "";
        });
    }
    </script>

  ```
