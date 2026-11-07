# Historial de versiones

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
