# Datos — Electiva Complementaria (Ingeniería Industrial)

Caso: **Envases del Caribe S.A.S.** — manufactura de envases plásticos, 3 plantas (Cartagena, Barranquilla, Soledad), esquema estrella completo.

Subir esta carpeta como `EnvasesDelCaribe_Datos/` en el repo `hmedrano1979/ITC`.

## Datos

| Archivo | Filas | Rol |
|---|---|---|
| `hechos_produccion.csv` | 117,684 | Tabla de hechos — grano diario por línea/turno/proceso, 2016-2024. Incluye OEE ya calculado (Disponibilidad × Rendimiento × Calidad) |
| `dim_planta.csv` | 3 | Cartagena (matriz, 2014), Barranquilla (2016), Soledad (2019) |
| `dim_linea.csv` | 12 | 4 líneas por planta (Inyectora, Sopladora, Ensambladora, Empacadora) |
| `dim_proceso.csv` | 4 | Corte, Ensamble, Empaque, Despacho |
| `dim_turno.csv` | 3 | Mañana, Tarde, Noche |
| `dim_causa_parada.csv` | 9 | Categorías: Mecánica, Eléctrica, Logística, Calidad |
| `dim_calendario.csv` | 3,865 | Tabla de fechas completa (a diferencia de Cumbre Sport & Outdoor, aquí SÍ viene como archivo, no se construye en DAX) |

Todas las tablas están limpias — este curso es Power BI (no limpieza de datos con Python). Separador `;`, encoding `latin-1`.

## Marca e información general

| Archivo | Rol |
|---|---|
| `00_Perfil_Empresa_y_Diccionario_Datos.docx` / `.pdf` | Perfil de la empresa, objetivos estratégicos (OEE, paradas, calidad, estandarización entre plantas), banco de preguntas de negocio y diccionario de datos completo |
| `logo_envases_caribe.png` / `logo_envases_caribe_icono.png` | Logo propio, paleta teal `#0F6E7A` / ámbar `#E8A33D` |
| `fondo_dashboard_envases_1280x720.png` | Fondo de dashboard, motivo de círculos concéntricos sutil |
| `Tema_Envases_Caribe.json` | Tema visual de Power BI |

## Trazabilidad pedagógica

Cada sesión debe encadenar: **Objetivo → Pregunta de negocio (banco en §3 del Perfil) → Variables necesarias → Medida DAX → Visualización**, mismo estándar que Libre I y Libre III.

## Pendiente

Todavía no se ha construido ninguna semana de clase — este curso empieza el viernes 14 de agosto (Semana 1).
