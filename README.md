# Órbita 30 Live

Órbita 30 Live es una página HTML de pantalla completa que recorre automáticamente cámaras y transmisiones en vivo de distintas partes del mundo. Es un proyecto independiente de EarthQuake.

## Funciones

- **Rotación automática:** muestra una cámara durante 60 segundos y luego pasa a la siguiente.
- **Orden aleatorio por recorrido:** al abrir la página crea una lista aleatoria que intenta no repetir el mismo comienzo que en la sesión anterior. Recorre el catálogo antes de volver a mezclarlo.
- **Mezcla de categorías:** alterna cámaras de carreteras y tráfico público, e intercala el resto de categorías procurando variar el contenido.
- **Catálogo integrado:** la versión actual contiene 650 entradas: 599 reproductores HLS y 51 transmisiones incrustadas. Incluye tráfico, costas, ciudades, fauna, naturaleza, volcanes, auroras, espacio, televisión japonesa y sismos en vivo, entre otras categorías.
- **Mapa mundial compacto:** muestra la ubicación aproximada de la cámara activa con un marcador; la tarjeta indica el número de la cámara en el recorrido. Usa una base oscura de ArcGIS y no permite mover ni acercar el mapa.
- **Diseño adaptable:** el mapa se ajusta al tamaño de la ventana, a la orientación del dispositivo y a la pantalla completa.
- **Pantalla completa:** el botón de la interfaz permite entrar y salir de ese modo.
- **Reproducción integrada:** utiliza reproductores HLS o el reproductor incrustado de la fuente, según la cámara.

## Uso

1. Abre `orbita-30-live.html` en un navegador moderno.
2. Mantén conexión a internet: los mapas, las bibliotecas de reproducción y los videos dependen de servicios externos.
3. La rotación comienza automáticamente. Usa el botón de pantalla completa para ampliar la vista.

No requiere instalación, servidor propio ni claves de API. Para una reproducción más compatible, se recomienda abrirlo desde un sitio HTTPS o un servidor local; algunos navegadores o proveedores limitan la reproducción automática o la carga desde archivos locales.

## Tecnologías y servicios

- HTML, CSS y JavaScript en un solo archivo.
- Leaflet para el minimapa.
- Hls.js para transmisiones HLS en navegadores compatibles; se usa HLS nativo cuando el navegador lo ofrece.
- Teselas de mapa **ArcGIS World Dark Gray Canvas**.
- Videos y cámaras servidos por sus respectivos emisores y plataformas externas.

La página guarda en el almacenamiento local del navegador una firma breve del orden de apertura anterior para intentar variar la secuencia al volver a abrirla.

## Disponibilidad de transmisiones

Las cámaras y sus direcciones están integradas en el HTML. La disponibilidad puede cambiar si el emisor modifica o retira una transmisión, y la reproducción depende de la conexión, el navegador y las restricciones del proveedor. El catálogo no garantiza que cada enlace esté emitiendo en todo momento.

El HTML no declara una licencia propia para el proyecto. Los videos, marcas, reproductores y mapas permanecen sujetos a las condiciones de sus respectivos proveedores.
