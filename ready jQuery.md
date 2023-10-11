El evento que se utiliza comúnmente en jQuery para detectar cuando el contenido del DOM de una página ha terminado de cargar (sin esperar a que todos los recursos, como imágenes, estén completamente cargados) es el evento `ready`. Este evento es esencial cuando quieres asegurarte de que el DOM esté disponible antes de ejecutar código que lo manipule.

**Ejemplo usando `$(document).ready()`:**

```javascript
$(document).ready(function() {
    // Tu código aquí se ejecutará una vez que el DOM esté listo.
    alert("¡El DOM está listo!");
});
```

Una forma abreviada de escribir lo mismo es:

```javascript
$(function() {
    // Tu código aquí se ejecutará una vez que el DOM esté listo.
    alert("¡El DOM está listo!");
});
```

Si también quieres esperar a que todos los recursos (incluidas las imágenes) estén cargados, puedes usar el evento `load` en el objeto `window`:

```javascript
$(window).on("load", function() {
    // Tu código aquí se ejecutará una vez que todos los recursos estén completamente cargados.
    alert("¡Todo el contenido de la página está cargado!");
});
```

Es importante distinguir entre estos eventos: 

- `$(document).ready()`: Se dispara cuando el DOM está listo.
- `$(window).on("load", ... )`: Se dispara cuando todos los recursos de la página (incluidas imágenes, scripts, estilos, etc.) están completamente cargados.

La mayoría de las veces, especialmente cuando solo necesitas manipular el DOM, `$(document).ready()` es el evento que utilizarás.
