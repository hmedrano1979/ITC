# Datos — Electiva Libre I (Tecnología en Gestión de Calidad)

Caso: **Confecciones Andina S.A.S.** — empresa textil/confección con Sistema de Gestión de Calidad ISO 9001.
Esquema de constelación: 2 tablas de hechos que comparten dimensiones — mismo patrón de esquema estrella que Complementaria (Envases del Caribe) y Libre III (Cumbre Sport & Outdoor).

Subir esta carpeta como `ElectivaLibreI_ConfeccionesAndina/` en el repo `hmedrano1979/ITC` (o donde indiques).

## Archivos

| Archivo | Filas | Rol |
|---|---|---|
| `Hechos_NoConformidades.csv` | 6,200 | Tabla de hechos 1 — casos de no conformidad, 2005-01 a 2024-12 (20 años, volumen creciente, igual horizonte temporal que Cumbre Sport & Outdoor) |
| `Hechos_Auditorias.csv` | 420 | Tabla de hechos 2 — auditorías internas/externas, mismo rango 2005-2024 |
| `Dim_Proceso.csv` | 8 | Dimensión — procesos de la empresa (Diseño, Compras, Corte, Confección, Producto No Conforme, Empaque, Servicio al Cliente, Talento Humano) |
| `Dim_Responsable.csv` | 24 | Dimensión — responsables/auditores con fecha de ingreso (rotación de personal a lo largo de 20 años; nombre, cargo, departamento) |
| `Dim_Tipo_Hallazgo.csv` | 6 | Dimensión — tipos de no conformidad (referenciados a cláusulas ISO 9001) |

Las dos tablas de hechos se relacionan entre sí a través de `Proceso_ID` (comparten la dimensión Proceso) — la relación que se combina explícitamente en la Semana 2 con Power Query (Merge).

Todas las tablas están limpias (sin errores deliberados) — Unidad 1 de este curso es introducción a Power BI, no limpieza de datos con Python.
