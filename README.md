# Reporte de folios iCash (ServiceNow)

Página web de un solo archivo que convierte el export de incidentes de ServiceNow
(cajas inteligentes iCash) en un reporte de seguimiento: quién tiene cada folio, por
plaza y plataforma (Glory / Administrativo / ATIS), con días de rezago y semáforo.

**Página para probarlo:** https://danstook.github.io/FOLIOS-ICASH/

## Uso

En la página de arriba, o descargando `Reporte Folios iCash.html` (también viene
adjunto en cada [Release](https://github.com/DANSTOOK/FOLIOS-ICASH/releases)):

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
  "ATIS" → ATIS, "OPV-Cajas Inteligentes" (sin "Proveedor"), "L2"/"N2" o
  "Soporte" → L2 Soporte, "OPV-Cajas Inteligentes Admin" → Administrativo,
  cualquier otro → Administrativo.
- **Personas con etiqueta fija:** los asesores de TI van como **ATI (Asesor TI)** y el
  prestador de servicio de TI (Jaime Daniel Bustos Mendez) como **PFS TI**, sin importar
  el grupo. La lista está en `PERSONAS` dentro del HTML.
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

## Versiones y rollback

La página publicada **solo cambia cuando se crea una release**. Los ajustes
pequeños se guardan en `main` sin tocar la página; los cambios grandes se
publican como una versión nueva.

| Paso | Qué pasa |
|---|---|
| Se sube una etiqueta `vX.Y.Z` | El workflow **Release y publicación** crea la Release (con el HTML adjunto) y publica esa versión en la página. |
| Algo salió mal | Pestaña **Actions → Rollback a una versión → Run workflow**, escribir la versión anterior (ej. `v0.1.0`). La página vuelve a esa versión en ~1 minuto. |

- Numeración: empieza en `v0.1.0`. Cambio grande → `v0.2.0`, `v0.3.0`…
  Corrección dentro de una versión → `v0.2.1`.
- La versión publicada se ve en el encabezado del reporte, junto al subtítulo.
- El historial de cambios está en [CHANGELOG.md](CHANGELOG.md).

**Configuración única:** en el repositorio, Settings → Pages → Build and
deployment → Source: **GitHub Actions**.
