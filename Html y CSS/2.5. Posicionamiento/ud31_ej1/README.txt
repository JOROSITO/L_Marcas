# UD 3.1 — Ejercicio 1: Laboratorio de Position

## Observaciones de los Pasos Experimento a Experimento

### 1. `static` (Añadir `left: 50px` a `.c1`)
* **¿Se mueve?:** No, no se desplaza en absoluto.
* **¿Por qué?:** El posicionamiento `static` es el valor por defecto en HTML. Los elementos fluyen naturalmente según el documento y las propiedades de coordenadas (`top`, `bottom`, `left`, `right`) son ignoradas por completo.

### 2. `relative` (Configurar `c2` con `position: relative; top: 20px; left: 50px;`)
* **Observación:** El cuadro se desplaza 20px hacia abajo y 50px hacia la derecha desde su ubicación original.
* **Hueco dejado:** Deja un espacio vacío de 100x100px en el flujo del documento exactamente donde solía estar. Los demás elementos no ocupan su lugar original.

### 3. `absolute` (Configurar `c3` con `position: absolute; top: 0; right: 0;`)
* **Sin `position: relative` en `.contenedor`:** El cuadro viaja a la esquina superior derecha de la ventana del navegador (`body`), porque busca el primer contenedor padre posicionado y, si no lo hay, toma de referencia la ventana del navegador.
* **Al añadir `position: relative` a `.contenedor`:** El cuadro se coloca en la esquina superior derecha del recuadro `.contenedor`.
* **Hueco de `c3`:** Al ser `absolute`, sale completamente del flujo normal del documento, por lo que su hueco desaparece y no afecta a los elementos circundantes.

### 4. `z-index` (Subir `c2` con `top: -40px` para solapar `c1`)
* **Solapamiento:** Al dar a `.c1` `position: relative` con un `z-index: 2` superior al de `.c2` (`z-index: 1`), `.c1` queda por encima visualmente de `.c2`.
* **Regla clave:** La propiedad `z-index` solo funciona en elementos cuyo posicionamiento sea distinto de `static`.