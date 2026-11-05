# Reporte de folios iCash (ServiceNow)

Página web de un solo archivo que convierte el export de incidentes de ServiceNow
(cajas inteligentes iCash) en un reporte de seguimiento: quién tiene cada folio, por
plaza y plataforma (Glory / Administrativo / ATIS), con días de rezago y semáforo.

## Uso

1. En ServiceNow exporta la lista de incidentes a Excel
   (`incident - AAAA-MM-DDThhmmss.xlsx`).
2. Abre `Reporte Folios iCash.html` en Edge o Chrome (doble clic).
3. Arrastra el `.xlsx` al recuadro o usa **Seleccionar archivo**.

El archivo se procesa solo en el navegador; no se envía a ningún servidor.
No requiere instalación ni internet (sin internet usa la fuente del sistema).

## Cálculos

- **Fecha del reporte:** se toma del nombre del archivo.
- **Días de rezago** = fecha del reporte (00:00) − fecha/hora de apertura, redondeado.
- **Semáforo:** rojo 7+ días, amarillo 3 a 6, verde menos de 3.
- **Plataforma** por grupo de asignación: "Proveedor"/"Glory" → Glory,
  "ATIS" → ATIS, cualquier otro → Administrativo.
- Solo folios activos (excluye Resuelto, Cerrado y Cancelado).

## Secciones

- Campanita de alertas: folios Alto/Crítico con 2 días o más.
- Folios por plaza, asignado y plataforma.
- Distribución por plaza.
- Indicadores por plataforma.
- Top de incidencias.
- Casos activos (folio con enlace a ServiceNow, búsqueda, orden por columna,
  vista cómoda/compacta).

Cada sección se puede copiar o descargar como imagen. Exporta a Excel (CSV) e
imprime a PDF. Más detalle en `LEEME.txt`.
