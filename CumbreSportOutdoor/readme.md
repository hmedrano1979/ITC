# Datos — Electiva Libre III (Análisis de Datos, Ingeniería de Sistemas)

Caso: **Cumbre Sport & Outdoor S.A.S.** (mismo caso del Módulo 3 del Diplomado).
Ya cargado en `github.com/hmedrano1979/ITC/CumbreSportOutdoor` (carpeta propia, no se sobrescribió nada del Diplomado).

## Archivos

| Archivo | Estado | Uso en el curso |
|---|---|---|
| `Ventas_CumbreSportOutdoor_Sucio.csv` | Sucio a propósito (2,045 filas, muestra real del rango completo 2005-2024) | Semanas 1-4 de clase (limpieza progresiva en Unidad 1); separador `;`, encoding `latin-1` |
| `Ventas_CumbreSportOutdoor_Completo.csv` | Limpio, tabla de hechos completa (81,109 filas, 2005-2024, mismo archivo fuente `ventas-tienda-LATAM.xlsx` del Módulo 3 del Diplomado) | Unidad 2-3 (Semanas 7 en adelante) — dashboards reales de Power BI; separador `;` |
| `Dim_Producto_Sucio.csv` | Sucio a propósito (160 filas) | Talleres 1.1 y 1.2 (aplicar en taller lo aprendido en clase, sobre una tabla no vista) |
| `Dim_Producto.csv` | Limpio (mismo archivo del Diplomado) | Unidad 2-3 — dimensión producto para el modelo estrella |
| `Dim_Pais.csv` | Limpio, sin cambios | Referencia / Unidad 2 (modelado de relaciones) |
| `Dim_Vendedor.csv` | Limpio, sin cambios | Referencia / Unidad 2 |
| `Dim_Canal.csv` | Limpio, sin cambios | Referencia / Unidad 2 |
| `Metas_Mensuales_Vendedor_2025.csv` | Limpio, sin cambios | Referencia / Unidad 3 (KPIs, DAX) |

## Problemas de calidad introducidos deliberadamente

**`Ventas_CumbreSportOutdoor_Sucio.csv`:**
- Nulos: `CLIENTE` (~3%), `IDENTIFICACION` (~2.5%)
- Tipo mixto: `VENTAS` mezcla números con texto ("N/A", "Sin dato", "Pendiente", "?")
- 40 duplicados exactos
- 12 outliers reales en `VENTAS` (multiplicados x15-30)
- `PAIS` con inconsistencias de mayúsculas/espacios (además de las que ya trae `CANAL`/`FORMA DE PAGO` de forma real: "Punto de venta"/"punto de venta"/"Punto de Venta", "Cheque"/"Cheque  ")

**`Dim_Producto_Sucio.csv`:**
- Nulos: `MARCA` (~5%), `PROVEEDOR` (~4%)
- `CATEGORIA` con inconsistencias de mayúsculas/espacios/símbolos
- Tipo mixto: `PRECIO_LISTA_PROMEDIO` con texto ("N/A", "Sin definir", "?")
- 8 duplicados exactos
- 4 outliers reales en `PRECIO_LISTA_PROMEDIO` (multiplicados x10-20)

Generado con `random_state`/semilla fija (2026) — reproducible si se necesita regenerar.

## Marca e información general

| Archivo | Rol |
|---|---|
| `00_Perfil_Empresa_y_Diccionario_Datos.docx` / `.pdf` | Adaptación propia de Libre III del perfil/diccionario oficiales del Módulo 3: historia, misión/visión, objetivos estratégicos reales (crecimiento 15%/año, digitalización, stock, rentabilidad), banco de preguntas de negocio y diccionario completo de las 6 tablas, incluyendo las diferencias frente al Módulo 3 (muestra sucia, Latin-1, CSV) |
| `logo_cumbre_sport_outdoor.png` / `logo_cumbre_icono.png` | Logo real de la empresa, reutilizado tal cual del Diplomado (Módulo 3) — mismo caso, mismo activo |
| `fondo_dashboard_cumbre_1280x720.png` | Fondo de dashboard real del Diplomado (trae el subtítulo "Sesión 1" grabado en la imagen — se reutiliza igual en todas las semanas, mismo criterio que usó el propio Módulo 3 en sus 7 sesiones) |
| `Tema_Cumbre_Sport_Outdoor.json` | Tema visual de Power BI real del Diplomado (paleta navy/naranja) |

## Trazabilidad pedagógica

Cada sesión debe encadenar: **Objetivo → Pregunta de negocio (banco en §3 del Perfil) → Variables necesarias → Medida DAX → Visualización**, igual que en Electiva Libre I.
