# Lab 04: Carrito de Compras en Jetpack Compose

Estudiante: Alexis Prieto

## Descripción
App en Jetpack Compose para administrar un carrito de compras. Permite ingresar productos con su precio y cantidad, mostrarlos en una lista, borrarlos uno a uno y calcular de forma automática el subtotal, IGV y total.

## Capturas de Pantalla

**Captura de la interfaz vacia (sin productos)**

<img width="297" height="685" alt="image" src="https://github.com/user-attachments/assets/7175a538-198e-453e-be4a-9231655d958e" />

**Captura de la interfaz con productos añadidos**

<img width="337" height="742" alt="image" src="https://github.com/user-attachments/assets/e1b0dd10-a03f-4441-bfb4-cec5af50e6ce" />

## Cuestionario / Respuestas Conceptuales

### (a) ¿Por qué mutableStateListOf y no una MutableList normal?
Porque mutableStateListOf le avisa a Compose cada vez que agregamos o quitamos un producto para que refresque la pantalla al instante. Con una MutableList normal los datos cambian en memoria, pero la interfaz se queda congelada y no muestra los cambios.

### (b) ¿Por qué la lista es val?
Porque la variable siempre apunta a la misma lista en memoria. Lo que va cambiando son los productos que tiene dentro, pero la lista como tal no se reemplaza por otra.

### (c) ¿Qué hace weight(1f) en la LazyColumn?
Hace que la lista ocupe todo el espacio libre que queda al centro. Así logra que el panel de totales se quede siempre pegado abajo sin importar cuántos productos agregues.
