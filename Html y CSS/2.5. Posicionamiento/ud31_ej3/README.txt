# UD 3.1 — Ejercicio 3: Tarjeta de Producto y Caja con Scroll

## Parte A — Etiqueta Absoluta y Overflow

1. **¿Qué elemento necesita `position: relative`?**
   * La tarjeta `.tarjeta-producto` necesita obligatoriamente `position: relative`. De lo contrario, la etiqueta con `position: absolute` tomaría como referencia la ventana del navegador (`body`) en lugar del recuadro de la tarjeta.

2. **¿Qué le ocurre a la etiqueta si añadimos `overflow: hidden` a la tarjeta?**
   * Las esquinas sobresalientes de la etiqueta (`top: -10px; right: -10px`) son recortadas por completo y desaparecen. 
   * **Por qué ocurre:** `overflow: hidden` recorta cualquier elemento contenido que exceda los límites geométricos de la caja.
   * **Cómo arreglarlo:** Quitar la regla `overflow: hidden` de la tarjeta contenedora o reubicar la etiqueta para que quede completamente dentro del margen interior (`padding`) de la tarjeta.

## Parte B — Opciones de Overflow y Comparativa de Ocultación

### Comportamientos de la propiedad `overflow`:
* **`visible` (Predeterminado):** El texto sobrante desborda la caja y se dibuja por fuera sobre los elementos inferiores.
* **`hidden`:** El contenido sobrante se recorta y se vuelve invisible. No aparece ninguna barra de desplazamiento.
* **`scroll`:** Añade siempre barras de desplazamiento (vertical y horizontal) independientemente de si el texto cabe o no.
* **`auto` (Recomendado):** Añade la barra de desplazamiento únicamente cuando el contenido supera las dimensiones de la caja.

### Diferencia entre `visibility: hidden` y `display: none`:
* **`visibility: hidden`:** Oculta la tarjeta a la vista, pero la caja sigue ocupando su espacio físico intacto de 300px en el diseño.
* **`display: none`:** Oculta la tarjeta y elimina por completo el espacio que ocupaba en el layout, provocando que los elementos vecinos se muevan para ocupar su hueco.