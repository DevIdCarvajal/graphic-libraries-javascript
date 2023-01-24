# Elementos gráficos con jQuery-UI

## Introducción

jQuery UI (*user interface*) es una selección de recursos de interfaz de usuario (interacciones, efectos, widgets y temas) implementados a partir de la librería jQuery.

Ofrece un amplio catálogo de elementos totalmente personalizables que permiten desarrollar aplicaciones de frontend rápidamente, compatibles con cualquier navegador.

Aunque cada recurso tiene su propia sintaxis, lo más habitual es que cumplan la estructura propia de jQuery de selector-método-argumentos.

Esta notación suele complementarse además con la construcción en HTML de las etiquetas necesarias para y que dependen también de cada recurso.

Ejemplo ( `dragabble` ):

  - HTML
  
    ```
    <div id="draggable" class="ui-widget-content">
      <p>Objeto arrastrable</p>
    </div>
    ```

  - JavaScript
  
    ```
    $(() => $("#draggable").draggable())
    ```

[Descarga e instalación](https://jqueryui.com/download/)

## Paneles en acordeón

  - HTML
  
    ```
    <div id="accordion">
      <h3>Sección 1</h3>
      <div>
        <p>Mauris mauris ante, blandit et, ultrices a, suscipit eget, quam.</p>
      </div>
      
      <h3>Sección 2</h3>
      <div>
        <p>Sed non urna. Donec et ante. Phasellus eu ligula. Vestibulum sit amet purus.</p>
      </div>
    </div>
    ```

  - JavaScript
  
    ```
    $(() => $("#accordion").accordion())
    ```

## Inputs autocompletados

  - HTML
  
    ```
    <div class="ui-widget">
      <label for="tags">Etiquetas: </label>
      <input id="tags">
    </div>
    ```

  - JavaScript
  
    ```
    $(() => {
      const availableTags = [
        "HTML",
        "CSS",
        "JavaScript"
      ]

      $("#tags").autocomplete({source: availableTags})
    })
    ```

## Botones

  - HTML
  
    ```
    <div class="widget">
      <button>Botón 1</button>
      <input type="submit" value="Botón 2">
      <a href="#">Botón 3</a>
    </div>
    ```

  - JavaScript
  
    ```
    $(() => {
      $(".widget input[type=submit], .widget a, .widget button").button()
    })
    ```

## Checkboxes y radio buttons

  - HTML
  
    ```
    <div class="widget">
      <h2>Checkbox</h2>
      <fieldset>
        <legend>Puntuación:</legend>

        <label for="checkbox-1">Mal</label>
        <input type="checkbox" name="checkbox-1" id="checkbox-1">
        <label for="checkbox-2">Regular</label>
        <input type="checkbox" name="checkbox-2" id="checkbox-2">
        <label for="checkbox-3">Bien</label>
        <input type="checkbox" name="checkbox-3" id="checkbox-3">
      </fieldset>

      <h2>Radio</h2>
      <fieldset>
        <legend>Seleccione una ciudad:</legend>

        <label for="radio-1">Nueva York</label>
        <input type="radio" name="radio-1" id="radio-1">
        <label for="radio-2">París</label>
        <input type="radio" name="radio-1" id="radio-2">
        <label for="radio-3">Londres</label>
        <input type="radio" name="radio-1" id="radio-3">
      </fieldset>
    </div>
    ```

  - JavaScript
  
    ```
    $(() => $("input[type=checkbox], input[type=radio]").checkboxradio())
    ```

## Grupos

  - HTML
  
    ```
    <div class="widget">
      <fieldset>
        <legend>Alquiler de coches</legend>

        <div class="controlgroup">
          <select id="car-type">
            <option>Pequeño</option>
            <option>Grande</option>
            <option>Furgoneta</option>
          </select>

          <label for="transmission-standard">Normal</label>
          <input type="radio" name="transmission" id="transmission-standard">
          <label for="transmission-automatic">Automático</label>
          <input type="radio" name="transmission" id="transmission-automatic">

          <label for="insurance">Seguro</label>
          <input type="checkbox" name="insurance" id="insurance">

          <button>Reservar</button>
        </div>
      </fieldset>
    </div>
    ```

  - JavaScript
  
    ```
    $(() => $(".controlgroup").controlgroup())
    ```

## Selectores de fechas

  - HTML
  
    ```
    <p>Fecha: <input type="text" id="datepicker"></p>
    ```

  - JavaScript
  
    ```
    $(() => $("#datepicker").datepicker())
    ```

## Diálogos

  - HTML
  
    ```
    <div id="dialog" title="Basic dialog">
      <p>Lorem ipsum dolor</p>
    </div>
    ```

  - JavaScript
  
    ```
    $(() => $("#dialog").dialog())
    ```

## Menús

  - HTML
  
    ```
    <ul id="menu">
      <li class="ui-state-disabled"><div>Juguetes (n/a)</div></li>
      <li><div>Libros</div></li>
      <li><div>Electrónica</div>
        <ul>
          <li><div>Motor</div></li>
          <li><div>Varios</div></li>
        </ul>
      </li>
    </ul>
    ```

  - JavaScript
  
    ```
    $(() => $("#menu").menu())
    ```

## Barras de progreso

  - HTML
  
    ```
    <div id="progressbar"></div>
    ```

  - JavaScript
  
    ```
    $(() => $("#progressbar").progressbar({value: 50}))
    ```

## Listas desplegables

  - HTML
  
    ```
    <fieldset>
      <label for="selectmenu">Seleccione velocidad:</label>

      <select name="selectmenu" id="selectmenu">
        <option>Lento</option>
        <option selected="selected">Normal</option>
        <option>Rápido</option>
      </select>
    </fieldset>
    ```

  - JavaScript
  
    ```
    $(() => $("#selectmenu").selectmenu())
    ```

## Sliders

  - HTML
  
    ```
    <div id="slider"></div>
    ```

  - JavaScript
  
    ```
    $(() => $("#slider").slider())
    ```

## Pestañas (tabs)

  - HTML
  
    ```
    <div id="tabs">
      <ul>
        <li><a href="#tabs-1">Opción 1</a></li>
        <li><a href="#tabs-2">Opción 2</a></li>
        <li><a href="#tabs-3">Opción 3</a></li>
      </ul>
      <div id="tabs-1">
        <p>Proin elit arcu, rutrum commodo, vehicula tempus, commodo a, risus.</p>
      </div>
      <div id="tabs-2">
        <p>Morbi tincidunt, dui sit amet facilisis feugiat, odio metus gravida ante, ut pharetra massa metus id nunc.</p>
      </div>
      <div id="tabs-3">
        <p>Mauris eleifend est et turpis. Duis id erat. Suspendisse potenti.</p>
      </div>
    </div>
    ```

  - JavaScript
  
    ```
    $(() => $("#tabs").tabs())
    ```

## Tooltips

  - HTML
  
    ```
    <p><a href="#" title="Soy un tooltip">Cualquier cosa</a> puede ser un tooltip.</p>
    <p><label for="age">Nombre:</label><input id="age" title="Adelante, pasa"></p>
    ```

  - JavaScript
  
    ```
    $(() => $(document).tooltip())
    ```

## Referencias generales

[Documentación oficial](https://jqueryui.com/)  
[Primeros pasos](https://learn.jquery.com/jquery-ui/getting-started/)  
[Chuleta](https://simplecheatsheet.com/tag/jquery-ui-cheat-sheet/)  

## Ejercicios

[w3resource](https://www.w3resource.com/jquery-ui-exercises/1/index.php)