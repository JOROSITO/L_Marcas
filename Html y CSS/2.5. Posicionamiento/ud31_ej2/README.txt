# UD 3.1 — Ejercicio 2: Menú Sticky y Fixed

## Diferencia entre `position: sticky` y `position: fixed`

1. **`position: sticky` (Pegajoso):**
   * El elemento mantiene su lugar natural en el flujo de la página como si fuera `relative` hasta que el usuario hace scroll y alcanza la distancia marcada en la propiedad `top: 0`.
   * Al llegar a ese punto, se detiene y queda pegado arriba mientras hacemos scroll dentro de su contenedor padre.
   * **Ventaja:** No colapsa ni pisa el contenido que viene debajo antes de hacer scroll.

2. **`position: fixed` (Fijo):**
   * El elemento sale por completo del flujo normal del documento desde el primer momento y se posiciona relativo a la ventana del navegador (`viewport`).
   * **Comportamiento si cambiamos el menú a `fixed`:** Al quitarlo del flujo normal, las secciones del contenido principal suben inmediatamente y quedan ocultas por detrás del menú desde el momento en que carga la página.