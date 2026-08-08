# Datos — Electiva Libre I (Tecnología en Gestión de Calidad)

Caso: **Confecciones Andina S.A.S.** — empresa textil/confección con Sistema de Gestión de Calidad ISO 9001.
Esquema de constelación: 2 tablas de hechos que comparten dimensiones — mismo patrón de esquema estrella que Complementaria (Envases del Caribe) y Libre III (Cumbre Sport & Outdoor).

Ya cargado en `github.com/hmedrano1979/ITC/ConfeccionesAndina_Datos`.

## Datos

| Archivo | Filas | Rol |
|---|---|---|
| `Hechos_NoConformidades.csv` | 6,200 | Tabla de hechos 1 — casos de no conformidad, 2005-01 a 2024-12 (20 años, volumen creciente, igual horizonte temporal que Cumbre Sport & Outdoor) |
| `Hechos_Auditorias.csv` | 420 | Tabla de hechos 2 — auditorías internas/externas, mismo rango 2005-2024 |
| `Metas_Mensuales_Proceso.csv` | 160 | Tabla ANCHA (formato wide, Ene...Dic) — meta de no conformidades por proceso/año. Usada en la Semana 3 para enseñar Anular dinamización de columnas (Unpivot) |
| `Dim_Proceso.csv` | 8 | Dimensión — procesos de la empresa (Diseño, Compras, Corte, Confección, Producto No Conforme, Empaque, Servicio al Cliente, Talento Humano) |
| `Dim_Responsable.csv` | 24 | Dimensión — responsables/auditores con fecha de ingreso (rotación de personal a lo largo de 20 años; nombre, cargo, departamento) |
| `Dim_Tipo_Hallazgo.csv` | 6 | Dimensión — tipos de no conformidad (referenciados a cláusulas ISO 9001) |

Las dos tablas de hechos se relacionan entre sí a través de `Proceso_ID` (comparten la dimensión Proceso) — la relación que se combina explícitamente en la Semana 2 con Power Query (Merge).

Todas las tablas están limpias (sin errores deliberados) — Unidad 1-3 de este curso es Power BI, no limpieza de datos con Python. La tabla de calendario NO se incluye como archivo — se construye dentro de Power BI con DAX (`CALENDAR()`), en la Unidad 2 (recordar anular la Configuración de fecha y hora automática antes de crearla).

## Marca e información general

| Archivo | Rol |
|---|---|
| `00_Perfil_Empresa_y_Diccionario_Datos.docx` / `.pdf` | Perfil de la empresa, objetivos del sistema de reportes, banco de preguntas de negocio (descriptivas/diagnósticas/seguimiento) y diccionario de datos completo de las 6 tablas. Documento único para toda la Unidad 1-2-3, no se repite por semana. |
| `logo_confecciones_andina.png` | Logo horizontal (fondo transparente), paleta navy `#1B3A5C` / terracota `#C1592C` |
| `logo_confecciones_andina_icono.png` | Versión ícono cuadrado (favicon/avatar) |
| `fondo_dashboard_confecciones_1280x720.png` | Fondo de dashboard para Power BI, motivo de tejido sutil |
| `Tema_Confecciones_Andina.json` | Tema visual de Power BI (Ver → Temas → Explorar temas → Examinar), aplica la paleta a todos los visuales automáticamente |

## Trazabilidad pedagógica

Cada sesión del curso debe encadenar: **Objetivo → Pregunta de negocio (banco en §3 del Perfil) → Variables necesarias → Medida DAX → Visualización**. No se introduce una herramienta de Power BI sin conectarla primero a una pregunta real del banco.
