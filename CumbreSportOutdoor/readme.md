# Datos — Electiva Libre III (Análisis de Datos, Ingeniería de Sistemas)

Caso: **Cumbre Sport & Outdoor S.A.S.** (mismo caso del Módulo 3 del Diplomado).
Subir esta carpeta completa como subcarpeta nueva dentro de:
`Módulo3_CumbreSportOutdoor_Power_Bi/ElectivaLibreIII_Datos/` en el repo `hmedrano1979/ITC`
(NO sobrescribir los archivos originales del Diplomado — estos son copias/versiones propias de Libre III).

## Archivos

| Archivo | Estado | Uso en el curso |
|---|---|---|
| `Ventas_CumbreSportOutdoor_Sucio.csv` | Sucio a propósito (2,045 filas, muestra real 2023-2024) | Semanas 1-4 de clase (limpieza progresiva en Unidad 1); separador `;`, encoding `latin-1` |
| `Dim_Producto_Sucio.csv` | Sucio a propósito (160 filas) | Talleres 1.1 y 1.2 (aplicar en taller lo aprendido en clase, sobre una tabla no vista) |
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
