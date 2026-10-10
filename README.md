# Grupo Orión · El valor de nuestro servicio

Presentación interactiva de 18 escenas, preparada como sitio estático independiente a partir del DOM recuperado de la presentación original.

## Publicación en Render

- Tipo de servicio: **Static Site**
- Rama: la que contenga estos archivos
- Build command: `echo "Static site ready"`
- Publish directory: `.`
- Página de entrada: `index.html`

No requiere servidor de aplicaciones, dependencias de compilación, variables de entorno ni credenciales. Publicar solamente `index.html` y este archivo. Los archivos de captura, recuperación y comprobación no forman parte del sitio.

## Uso

Abrir la URL pública en un navegador moderno. La presentación comienza en la primera escena; `#1` a `#18` permiten abrir una escena concreta.

- Flecha derecha, espacio o Av Pág: siguiente escena
- Flecha izquierda o Re Pág: escena anterior
- G: índice
- N: guía del presentador
- D: detalle de la escena
- T: reloj
- F: pantalla completa cuando el navegador lo admite
- M: movimiento reducido
- P: pausar o reanudar el movimiento
- B: pantalla negra

En el celular se puede deslizar a los lados. La propia presentación incluye una vista alternativa cuando WebGL no está disponible.

## Contenido y dependencias

La presentación conserva sus imágenes, fuente incrustada, texto, notas para el presentador, estilos y lógica originales. Las notas están incluidas en el sitio y son accesibles mediante la herramienta Guía.

Los únicos recursos externos son siete scripts públicos de Three.js, fijados a la versión r128 / 0.128.0, servidos desde cdnjs y jsDelivr. El sitio necesita acceso a esos CDN para las escenas 3D. No contiene integraciones de cuenta, formularios, API privadas ni solicitudes de autenticación. No se añadieron rastreadores.

## Procedencia y cambios de preparación

La fuente recuperada fue un DOM completo de la presentación original de Claude, capturado después de la ejecución de JavaScript. No es una exportación literal del archivo fuente previo a su ejecución.

Preparación realizada:

1. Eliminación del bloque de ejecución del visor de Claude: preámbulo, puente con el host y estilo básico del visor.
2. Retirada de los envoltorios de palabras, elementos de navegación y caracteres del tablero generados por JavaScript, para que se construyan una sola vez al abrir el sitio.
3. Restablecimiento de los valores finales de los contadores y del estado inicial de la interfaz, eliminando el estado capturado en la escena 10 y la clase de ausencia de WebGL del entorno de captura.

No se modificaron las cifras, el contenido editorial, los 18 apartados, las imágenes, la hoja de estilos propia de la presentación ni su código JavaScript. Los scripts propios, la hoja de estilos y las imágenes se compararon con la captura para comprobar que se conservaron sin cambios. Los tres scripts en línea pasaron la comprobación de sintaxis `node --check`.

La disponibilidad real de WebGL depende del navegador y del dispositivo. La comprobación visual en un entorno sin WebGL no valida la ejecución de los efectos 3D.
