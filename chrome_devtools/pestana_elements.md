# Pestaña elements

La pestaña "**Elements**" representa lo que llamaremos el "**[DOM](https://es.wikipedia.org/wiki/Document_Object_Model)**"<sup>1</sup> (*Document Object Model*), que no es más que lo que representa la página que estamos viendo.

El DOM lo construye el navegador a partir del código HTML que recibe tras hacer la petición HTTP inicial. Además, el navegador intenta arreglar cualquier error que se encuentre en el código, por ejemplo: si se nos olvida cerrar una etiqueta, si anidamos etiquetas que no son anidables, etc. Por ese motivo y porque el DOM se puede modificar<sup>2</sup>, este se parece pero no suele ser exactamente igual al código HTML recibido en la petición HTTP.

Además de poder ver el DOM, podemos editarlo, buscar texto en él y hasta reordenar las etiquetas arrastrándolas con el ratón.

En la siguiente imagen vemos las diferentes partes de esta pestaña:

[![](../images/pestana_elements_2.png)](../images/pestana_elements_2.png)

* **Emulador**: esta opción nos permitirá simular que estamos usando un móvil o tablet y hacer *throttling* (simular otro tipo de conexión) al igual que hemos visto en la pestaña "**Network**".
* **Inspeccionar elementos**: activando esta opción podrás hacer clic sobre cualquier parte de la página y el inspector señalará en el DOM el código que representa el elemento seleccionado.
* **Menú contextual**: pulsando el botón derecho sobre el código veremos varias opciones:
    * **Add attribute**: permite añadir un atributo, por ejemplo: *charset="UTF-8*" (atajo de teclado: *Enter*).
    * **Edit as HTML**: nos permite añadir, editar o quitar cualquier cosa (atajo de teclado: F2 tanto en Windows como en Mac)
    * **Copy**: nos permite copiar el código (*outerHTML*), el selector (ya veremos lo que significa cuando veamos CSS), el [XPath](https://es.wikipedia.org/wiki/XPath)<sup>3</sup> (es un lenguaje que nos permite buscar y seleccionar elementos teniendo en cuenta la estructura jerárquica del código), cotar y copiar el elemento.
    * **Ocultar elemento**: cambia la visibilidad a "no visible" usando CSS.
    * **Delete element**: permite eliminar el elemento (atajo de teclado: *Suprimir* o *Borrar*).
    * **:active, :hover, :focus, :visited**: nos permite cambiar el estado del elemento (esto lo usaremos en el apartado de CSS)
    * **Scroll into View...**: en caso de ser necesario se hace scroll hasta que se muestre el elemento.
    * **Break on...**: nos permite establecer puntos de parada indicando que se debe detener la ejecución de cualquier código JavaScript si:
        * Se modifica alguno de sus hijos.
        * Se modifica algún atributo. 
        * O si se elimina el código.
* **Buscar**: Nos permite buscar cualquier palabra dentro del DOM (atajo de teclado: *Ctrl + F* en Windows ó *Cmd + F* en Mac).
* **Jerarquía**: nos muestra todos los ancestros del elemento y nos permite seleccionarlos.

Los cambios que hagas sobre esta pestaña no se guardarán ya que no estamos modificando el fichero de código<sup>4</sup> sino el DOM (y ya hemos visto la diferencia), por tanto al refrescar la página todos los cambios desaparecerán.

Para mejorar tu productividad te recomiendo que de vez en cuando consultes [los atajos de teclado del panel Elements](https://developers.google.com/web/tools/chrome-devtools/iterate/inspect-styles/shortcuts#elements-1), como por ejemplo:

Windows/Linux   | Mac           | Función
----------------|---------------|---
Ctrl + Z        | Cmd+Z         | Deshacer los cambios realizados
Ctrl + Shift + C| Cmd + Shift  + C | Abrir DevTools con la herramienta para "**Inspeccionar elementos**" activada por defecto
&larr;, &rarr;, &uarr;, &darr; | &larr;, &rarr;, &uarr;, &darr; | Navegar por los elementos del DOM

El panel que sale a la derecha es el del código CSS que se le ha aplicado al elemento seleccionado, pero esto ya lo veremos más adelante.

<small>Aclaraciones:</small><br>
<small>1. Puedes encontrar la definición formal del DOM en la [página del W3C](https://www.w3.org/DOM/).</small><br>
<small>2. Usando JavaScript, o mediante una extensión del navegador por ejemplo</small><br>
<small>3. Puedes encontrar la definición formal de XPATH en la [página del W3C](https://www.w3.org/TR/xpath/)
</small><br>
<small>4. A veces escucharás "[código fuente](https://es.wikipedia.org/wiki/C%C3%B3digo_fuente)" en lugar de código, son sinónimos.
</small><br>