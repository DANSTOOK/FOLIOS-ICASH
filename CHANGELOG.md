# Historial de versiones

## Sin publicar

- Imágenes (copiar / descargar) completas: ya no se cortan abajo ni a la derecha (se miden y dibujan con la misma letra), Casos activos con muchos folios sale entera, el Top incluye todas las incidencias, los números y barras salen en su valor final aunque se acabe de filtrar, y el pie indica los filtros aplicados. El botón gira mientras se genera la imagen.
- Modo oscuro: los días en amarillo y la prioridad Alto/Crítico ya se leen bien.
- Casos activos cabe completa en pantalla amplia (la columna Días rezago ya no queda cortada).
- Rayado de Casos activos estable al abrir un detalle; Esc cierra el detalle abierto.
- Modo presentación: escribir en el buscador ya no cambia de diapositiva.
- Distribución por plaza: 12 colores distintos (ya no se repiten con 9 plazas o más).
- Animaciones más tranquilas: la entrada completa (contar desde 0, barras que crecen, dona que se dibuja, anillo que se llena) solo al cargar el archivo; al filtrar los valores cambian sin volver a empezar. El brillo del total pasa una sola vez, la línea verde ya no se mueve sin parar y las tarjetas con tablas grandes no se elevan al pasar el mouse.
- Detalle al pasar el mouse con el mismo estilo en todo el reporte (tabla por plaza y plazas involucradas incluidas) y onda al hacer clic también en plazas, botones del encabezado y "Ver todas".

## v0.1.0 — primera versión publicada

- Carga del export de incidentes de ServiceNow (.xlsx / .csv) en el navegador, sin servidor.
- Días de rezago = fecha del reporte (tomada del nombre del archivo) − fecha de apertura, redondeado.
- Folios por plaza, asignado y plataforma (Glory / Administrativo / ATIS), con semáforo en la columna de días.
- Distribución por plaza (gráfica de pastel con detalle al pasar el mouse).
- Indicadores por plataforma y Top de incidencias.
- Casos activos: enlace del folio a ServiceNow, búsqueda, orden por columna, mini barra de rezago y vista cómoda/compacta.
- Campanita de alertas: folios Alto/Crítico con 2 días o más.
- Copiar / descargar cada sección como imagen, exportar a Excel (CSV) e imprimir a PDF.
- Pantalla de carga con animaciones: borde punteado en movimiento, icono flotante con ondas, archivo de ejemplo que cae al recuadro, estado al arrastrar y al procesar, pasos con iconos.
- Tarjeta resumen: Región, Plazas (filtra todo el reporte) y total de CI sin resolver con las plazas involucradas.
- Animaciones y UX: transición al filtrar, pulso del semáforo rojo al cargar, campanita animada, fila resaltada y detalle desplegable en Casos activos, esqueleto de carga, avisos con icono y centro dinámico en la gráfica de pastel.
- Efectos visuales: números que cuentan, anillo de % en rojo y brillo en el total, dona que se dibuja, secciones que aparecen al bajar, filas que se deslizan al ordenar, mini barras que crecen, tarjetas que se elevan y onda al hacer clic.
- Plataforma: los folios del grupo OPV-Cajas Inteligentes (sin Proveedor) ahora cuentan como L2 Soporte, no como Administrativo.
- Total con fecha del reporte, más grande. Pie de página (pantalla, imágenes y PDF), PDF con portada, modo presentación, selector de plataforma deslizante, encabezado que se compacta, modo oscuro y optimización (código sin uso eliminado, cálculo en caché, búsqueda con pausa).
- Etiquetas nuevas: ATI (Asesor TI) para los asesores de TI y PFS TI para el prestador de servicio de TI. El grupo OPV-Cajas Inteligentes Admin cuenta como Administrativo.
- Pestañas de plataforma: la activa se resalta con una línea verde líquida (efecto mercurio) que se estira al cambiar de pestaña, y cada pestaña muestra su conteo en una pastilla.
- Tarjeta resumen más compacta: filtros de Región y Plaza en una sola línea y plazas involucradas con barra proporcional (parte en rojo) alineada.
- Pestañas de plataforma: ya no se encogen ni cortan el número; si no caben pasan a una segunda fila.
- Tarjeta resumen a menos de la mitad de alto: total, fecha y anillo en una franja, y copiar/descargar como iconos junto a los filtros.
- Pestañas de plataforma con más espacio: más altas, más separadas y con la línea verde despegada del texto.
- Pestañas de plataforma en una sola fila: la tarjeta de plazas es más ancha y la pestaña de asesores se muestra como ATI (nombre completo al pasar el mouse y en la tabla).
- Tarjeta resumen: las plazas se reparten en filas parejas según cuántas haya (4 plazas = 2 y 2), en cualquier ancho de pantalla.
- Responsive: encabezado, tarjeta resumen, pestañas, tablas y botones se acomodan en ventanas de 320 a 1920 px sin desbordar la página; Casos activos fija la columna Folio al desplazarse.
- Casos activos: un solo detalle abierto a la vez (se cierra al abrir otro o con clic afuera) y unido visualmente a su folio; botón discreto para copiar el número de folio; la barra roja de alerta se reemplaza por una campanita junto al folio.
- Etiquetas de plataforma con tono suave e icono (Glory billetes, Administrativo maletín, ATIS edificio, L2 Soporte audífonos, ATI laptop, PFS TI llave) en la tabla por plaza, Casos activos e Indicadores.
- Se mantiene la corrección de filtros de Casos activos (sin filtros pegados al cambiar plaza o plataforma; clic en una persona muestra solo los folios de su fila; pestañas e Indicadores cuentan la plaza elegida).
