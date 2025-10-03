# 📊 Dashboard de Rendimiento de Ventas y Rentabilidad (AdventureWorks)

## 🌟 Resumen del Proyecto

Este proyecto es una solución de **Business Intelligence (BI)** que demuestra el ciclo completo de análisis de datos: desde la conexión a la base de datos **AdventureWorks 2022** (SQL Server) hasta la entrega de un dashboard interactivo en **Power BI**. El objetivo principal es monitorear los indicadores clave de **Ventas**, **Costos** y **Rentabilidad** para informar las decisiones gerenciales.

El enfoque en el repositorio está en la **metodología de análisis** y la **ejecución técnica**.

---

## 🛠️ Flujo de Trabajo (Workflow) del Proyecto

El proyecto se ejecutó siguiendo una metodología estructurada de **7 Fases**:

### Fase 1: Planificación y Comprensión del Negocio
* **Objetivo:** Definir las necesidades del negocio. El dashboard se centró en responder preguntas clave como: *¿Cuál es el margen de beneficio actual?* y *¿Cómo ha evolucionado la tendencia de ventas a lo largo del tiempo?*
* **KPIs Definidos:** Ventas Totales, Coste Total, Beneficio, Margen Bruto (%), y Ventas por Geografía y Categoría.

### Fase 2: Obtención y Conexión de Datos
* **Fuente:** Conexión a la base de datos **AdventureWorks 2022** alojada en **SQL Server**.
* **Tablas Seleccionadas:** Se importaron las tablas necesarias para un modelo de esquema estrella, incluyendo `FactInternetSales` (Hechos) y dimensiones (`DimProduct`, `DimCustomer`, `DimDate`, `DimGeography`).

### Fase 3: Preparación y Transformación de Datos (Power Query)
* **Limpieza:** Se renombraron columnas para mayor claridad y se ajustaron los tipos de datos (ej. Fechas, Moneda) para asegurar la integridad.
* **Creación de Atributos:** Se crearon columnas auxiliares (ej. Año Fiscal) necesarias para la segmentación del informe.

### Fase 4: Modelado de Datos
* **Estructura:** Implementación de un **Esquema Estrella** sólido, estableciendo relaciones **Uno a Varios (1:\*)** entre la tabla de hechos (`FactInternetSales`) y las tablas de dimensión.
* **Optimización:** Se ocultaron las claves primarias/foráneas del panel de campos para facilitar la creación de informes.

### Fase 5: Cálculos y Métricas (DAX)
* Se desarrolló la lógica de negocio creando **Medidas (DAX)** clave, esenciales para el análisis:
    * `Beneficio = [Ventas Totales] - [Coste Total]`
    * `Margen Bruto (%) = DIVIDE([Beneficio], [Ventas Totales])`
    * `Crecimiento Año a Año (YoY)` para el análisis de tendencias.

### Fase 6: Visualización y Diseño del Informe
* **Diseño:** Se implementó un diseño limpio y profesional con una paleta de colores coherente y un uso estratégico de **Tarjetas KPI** en la parte superior.
* **Visualizaciones:** Se eligieron visuales específicos (Gráfico de Línea, Gráficos de Anillo y Mapas) para contar la historia de los datos de forma efectiva.

### Fase 7: Revisión, Documentación y Entrega
* **Validación:** Se verificó que los totales y porcentajes del dashboard coincidieran con los datos fuente.
* **Documentación:** Creación de este `README.md` detallando el proceso, y subida del archivo `.pbix` a GitHub para la reproducibilidad.

---

## 📈 Dashboard y Conclusiones Clave

*(**Instrucción:** Inserta las imágenes aquí)*

| Captura de Pantalla | Conclusión (Ejemplo) |
| :--- | :--- |
| `![Dashboard Principal](Images/image_63bbca.jpg)` | El **Margen Bruto** se mantuvo por encima del 45%, indicando una alta rentabilidad de los productos. |
| `![Análisis Geográfico](Images/image_63be73.jpg)` | Se identificó que **Estados Unidos** y **Reino Unido** generan la mayor parte de las ventas totales, lo que requiere un foco estratégico en estos mercados. |

---

## ⚙️ Tecnologías Utilizadas

* **Power BI Desktop**
* **SQL Server (AdventureWorks 2022)**
* **Lenguaje DAX**
* **Power Query**
