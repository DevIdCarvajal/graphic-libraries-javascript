# Introducción a la manipulación del DOM con jQuery

## Introducción

jQuery es una librería para JavaScript que facilita la codificación de la mayoría de necesidades de una aplicación web frontend en el navegador (sea cual sea este).

Algunas de estas son el acceso y manipulación de elementos del árbol DOM, manejo de eventos, animaciones o peticiones AJAX.

Su lema y por tanto el objetivo que persigue es el de *hacer más escribiendo menos*.

A grandes rasgos, se basa principalmente en un objeto principal que se puede referenciar mediante el símbolo dólar, seguido dependiendo del método a usar de la librería.

El caso general presenta la siguiente estructura:

    $(selector).method(arguments)

Donde `selector` sigue la notación de selectores de CSS, el `method` lo proporciona la librería, del que dependen los `arguments`.

Debido a la extensión y popularidad de la librería en su momento, esta notación ha sido replicada en otros recursos del ecosistema (e.g., cheerio en Node.js).

Ejemplos:

  - Manipulación del DOM

        $("button.continue").html("Siguiente")

  - Manejo de eventos

        const hiddenBox = $("#banner-message")

        $("#button-container button")
          .on("click", (event) => hiddenBox.show())

  - Ajax

        $.ajax({
          url: "/api/getWeather",
          data: {
            zipcode: 97201
          },
          success: (result) => $("#weather-temp")
            .html(`<strong>${result}</strong> degrees`)
        })

[Descarga e instalación](https://jquery.com/download/)

## Manejo de atributos de clase

- addClass
- hasClass
- removeClass
- toggleClass

## Inserción de elementos

### Alrededor

- unwrap
- wrap
- wrapAll
- wrapInner

### Interior

- append
- appendTo
- html
- prepend
- prependTo
- text

### Exterior

- after
- before
- insertAfter
- insertBefore

## Eliminación de elementos

- detach
- empty
- remove
- unwrap

## Sustitución de elementos

- replaceAll
- replaceWith

## Manejo de atributos generales

- attr
- prop
- removeAttr
- removeProp
- val

## Manejo de propiedades de estilo

- css
- height
- innerHeight
- innerWidth
- offset
- outerHeight
- outerWidth
- position
- scrollLeft
- scrollTop
- width

## Manejo de eventos

- blur
- change
- click
- dblclick
- event.pageX
- event.pageY
- event.preventDefault
- event.stopPropagation
- event.target
- focus
- focusin
- focusout
- hover
- keydown
- keypress
- keyup
- mousedown
- mouseenter
- mouseleave
- mousemove
- mouseout
- mouseover
- mouseup
- off
- on
- one
- ready
- resize
- scroll
- select
- submit
- trigger

## Filtrado

- eq
- even
- filter
- first
- has
- is
- last
- map
- not
- odd
- slice

## Efectos

- animate
- clearQueue
- delay
- dequeue
- fadeIn
- fadeOut
- fadeTo
- fadeToggle
- finish
- hide
- queue
- show
- slideDown
- slideToggle
- slideUp
- stop
- toggle

## Ajax

- ajax
- get
- getJSON
- post
- load

## Referencias generales

[Documentación oficial](https://api.jquery.com/)  
[Guía básica de jQuery](https://www.geeksforgeeks.org/jquery-cheat-sheet-a-basic-guide-to-jquery/)  
[Chuleta Online (Selectores)](https://www.jquerycheatsheet.com/)  
[Alternativas a jQuery](https://youmightnotneedjquery.com/)

## Ejercicios

[Selectores CSS](https://flukeout.github.io/)  
[w3schools](https://www.w3schools.com/jquery/jquery_exercises.asp)  
[w3resource](https://www.w3resource.com/jquery-exercises/part1/index.php)