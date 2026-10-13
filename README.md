# Grupo Orión · El valor de nuestro servicio

Presentación interactiva de 21 escenas con tablero de incidencias de asistencia.

## Fuente

Actualización del 13 de octubre de 2026 a partir de `Presentacion_Grupo_Orion (9)(2).html`. `index.html` conserva exactamente el archivo recibido, sin cambios de contenido ni diseño. El dashboard en `public/incidencias/index.html` es una extracción exacta del contenido incrustado en `window.ORION_DASH` para que el enlace relativo funcione en línea.

La versión anterior de 18 escenas permanece en el historial de Git en el commit `a3a68bb36e48046f41b375953ab547ea6a6e8a6c`.

## Render

- Servicio existente: `orion-valor-servicio`
- Tipo: Static Site
- Rama: `main`
- Build: `mkdir -p public && cp index.html public/index.html`
- Directorio publicado: `public`
- Presentación: `/` (escenas `#1` a `#21`)
- Dashboard: `/incidencias/index.html`
- Despliegue manual: los cambios de Git no activan publicación automática

## Controles

Flechas o espacio para navegar; G para índice; N para guía; D para detalle; T para reloj de 20 minutos; F para pantalla completa; M para movimiento reducido; P para pausar el movimiento; B para pantalla negra. El botón de la escena 4 abre el dashboard en otra pestaña.

## Verificación técnica

Los 11 scripts de la presentación y el script del dashboard pasan comprobación de sintaxis. Las 21 escenas coinciden con la configuración de navegación y no hay IDs HTML duplicados. Imágenes y fuente de la presentación están incorporadas; el dashboard utiliza Google Fonts. Los efectos 3D requieren WebGL disponible en el navegador.
