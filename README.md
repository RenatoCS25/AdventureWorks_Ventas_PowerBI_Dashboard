# 🚴‍♂️ Adventure Works - Análisis Integral de Ventas

## 1. Fase Preguntar – Definir el Problema y los Objetivos
### Contexto del Negocio
Adventure Works es una empresa multinacional de fabricación y venta de bicicletas y accesorios deportivos. Este proyecto presenta un análisis exhaustivo de datos de ventas, clientes y productos del período 2022-2024, implementando un modelo dimensional en Power BI para proporcionar insights accionables al equipo directivo.
El análisis se enfoca en identificar patrones de ventas, productos más rentables, segmentación de clientes y tendencias geográficas para optimizar estrategias comerciales y maximizar la rentabilidad.

### Objetivos del Proyecto

1. Analizar el desempeño comercial de Adventure Works durante el período 2022-2024
2. Identificar productos y categorías más rentables para optimizar el inventario
3. Segmentar clientes por características demográficas y comportamiento de compra
4. Detectar tendencias temporales en ventas para planificar estrategias estacionales
5. Visualizar KPIs clave mediante dashboards interactivos para la toma de decisiones


### Preguntas Clave del Análisis

1. ¿Cuál es la tendencia de ventas y rentabilidad en los últimos 3 años?
2. ¿Qué productos y categorías generan mayor margen de utilidad?
3. ¿Cuáles son las características demográficas de los clientes más valiosos?
4. ¿Qué mercados geográficos presentan mayor potencial de crecimiento?
5. ¿Existen patrones estacionales en las ventas que puedan aprovecharse?


## 2. Fase Preparar – Recolección y Comprensión de los Datos

### Fuente de Datos
•	Dataset: AdventureWorks2022 (Microsoft SQL Server Sample Database)
•	Período Analizado: 2022 – 2024
•	Origen: Archivos de base de datos .BAK (AdventureWorks2022.bak)

### Tablas Principales
•	FactInternetSales – 60,000 transacciones
•	DimCustomer – 18,000 clientes únicos
•	DimProduct / DimProductCategory / DimProductSubcategory – Jerarquías de productos
•	DimGeography – Ubicación geográfica de clientes
•	DimDate – Dimensión temporal

### Modelado
Los datos se importaron a Power BI implementando un modelo dimensional tipo estrella (Star Schema) para optimizar consultas y relaciones.

## 3. Fase PROCESS – Limpieza y Transformación
### Exploración Inicial
•	Revisión de estructura, relaciones y llaves primarias/foráneas
•	Detección de duplicados y valores nulos
•	Verificación de tipos de datos y consistencia
### Limpieza de Datos
•	Eliminación de duplicados
•	Estandarización de nombres y formatos
•	Reemplazo de valores nulos en campos críticos
•	Validación de montos y fechas
### Transformaciones
•	Columnas calculadas: Utilidad Bruta, Margen %
•	Jerarquías temporales: Año → Trimestre → Mes
•	Segmentación de clientes por ingreso y ocupación

## 4. Fase ANALYZE – Análisis y Descubrimiento de Insights

### Métricas Principales (DAX)
Ventas Totales = SUM(FactInternetSales[SalesAmount])
Costo Total = SUM(FactInternetSales[TotalProductCost])
Utilidad Bruta = [Ventas Totales] - [Costo Total]
Margen % = DIVIDE([Utilidad Bruta], [Ventas Totales], 0)
Clientes Únicos = DISTINCTCOUNT(FactInternetSales[CustomerKey])

### Tipos de Análisis Realizados
•	Tendencias temporales (YoY, CAGR, estacionalidad)
•	Análisis de Pareto (80/20) por productos
•	Segmentación RFM de clientes
•	Análisis geográfico de ventas
•	Comparación de rentabilidad por categoría

### KPIs Principales
Métrica	Valor	Insight
Ventas Totales	$29.36M	Crecimiento sostenido 2022–2024
Costo Total	$17.28M	Eficiencia operativa del 59%
Utilidad Bruta	$12.08M	Margen saludable del 41.2%
Clientes Únicos	18,000	Base de clientes sólida
Ticket Promedio	$489	Mercado de gama media-alta

## 5. Fase SHARE – Comunicación de Resultados
### Dashboards en Power BI
1.	Resumen Ejecutivo: KPIs principales, tendencia anual, distribución geográfica.
2.	Productos: Rentabilidad por categoría/subcategoría y análisis temporal.
3.	Clientes: Segmentación demográfica, top clientes, y comportamiento de compra.
### Visualización:
•	Filtros interactivos por año, categoría y región.
•	Navegación mediante botones temáticos.
•	Enfoque UX/UI profesional y minimalista.
(Incluye imágenes o enlaces al dashboard)
________________________________________

## 6. Fase ACT – Conclusiones y Recomendaciones

### a). Principales Insights
1. Dominio Absoluto de la Categoría Bikes

Las bicicletas representan el 96.46% del total de ventas ($28.3M), mientras que Accessories y Clothing solo contribuyen con 3.54% combinados. Este hallazgo revela que la empresa depende críticamente de las ventas de bicicletas, lo cual representa tanto una fortaleza como un riesgo de concentración. Existe una oportunidad significativa para incrementar la venta cruzada de accesorios y ropa, que típicamente tienen márgenes más altos y menor costo de inventario. La diversificación del portafolio podría mejorar la estabilidad del negocio y reducir la vulnerabilidad ante cambios en la demanda de bicicletas.

2. Concentración de Valor en Pocos Clientes

El análisis reveló que el top 10 de clientes genera aproximadamente el 40% del revenue total, con el cliente principal, Nichole Nara, habiendo gastado $13,295 y contribuido con un margen de $5,250. Esta concentración de valor implica que la retención de clientes VIP es crítica para la estabilidad del negocio, ya que la pérdida de estos clientes tendría un impacto desproporcionado en los ingresos. Se hace evidente la necesidad de implementar un programa de fidelización robusto que incluya atención personalizada, beneficios exclusivos y comunicación directa con este segmento para asegurar su lealtad a largo plazo.

3. Crecimiento Explosivo en 2024

Las ventas de 2024 ($16M) superan más del doble a las de 2023 ($6M), representando un crecimiento extraordinario del 166% year-over-year. Este patrón indica que el negocio está en una fase de crecimiento acelerado y expansión de mercado. Este momentum presenta el momento óptimo para escalar operaciones, optimizar la cadena de suministro y expandir la capacidad de inventario. Es crucial capitalizar este crecimiento mediante inversiones estratégicas en infraestructura, marketing y expansión geográfica antes de que el mercado alcance su punto de saturación.

4. Segmento Profesional Como Core Customer

Los clientes con ocupación "Profesional" generan $9.9M en ventas (33.7% del total), seguidos por "Obreros especializados" con $6.4M (21.8%). Este hallazgo define claramente que el perfil demográfico ideal es un profesional de ingresos medios-altos con poder adquisitivo y disposición para invertir en productos de calidad. Las campañas de marketing deben enfocarse estratégicamente en este segmento, destacando aspectos como calidad, tecnología, performance y durabilidad que se alinean con sus valores y expectativas. El messaging debe reflejar aspiraciones profesionales y estilo de vida activo.

5. Equilibrio de Género en la Base de Clientes

La distribución de clientes es prácticamente equitativa con 49.7% masculino y 50.3% femenino, lo cual es notable en una industria tradicionalmente sesgada. Este equilibrio valida que los productos de Adventure Works tienen appeal universal y que las estrategias de producto y marketing han sido efectivas en atraer a ambos géneros por igual. Las futuras estrategias de marketing deben mantener cuidadosamente este equilibrio, evitando campañas que segmenten artificialmente por género y en su lugar enfocándose en beneficios universales como salud, aventura y calidad de vida.

6. Correlación Entre Educación y Gasto

Los clientes con educación universitaria completa (30.04%) y postgrado (20.04%) representan el 50% de la base de clientes pero generan proporcionalmente más revenue per capita que otros segmentos educativos. Este patrón sugiere que el nivel educativo es un predictor confiable del valor de vida del cliente (CLV). Las estrategias de adquisición deberían enfocarse geográfica y digitalmente en áreas donde se concentra este perfil demográfico, tales como zonas universitarias, distritos empresariales, y canales como LinkedIn y publicaciones especializadas. El contenido de marketing debe reflejar sofisticación y conocimiento técnico que resuene con este público educado.


### b). Recomendaciones Estratégicas

 1. Optimización del Portafolio de Productos

Actualmente, el 96.46% de las ventas provienen de la categoría Bikes, lo que representa una fuerte dependencia. Se recomienda diversificar promoviendo la línea de Mountain Bikes (la más rentable) y fomentando la venta de accesorios y ropa junto con cada bicicleta. Promociones del tipo “compra una bici y obtén 20% en accesorios” pueden aumentar la venta cruzada. También se sugiere revisar la línea de ropa y eliminar productos con bajo rendimiento para concentrar recursos en categorías más rentables.

 2. Estrategias de Marketing Segmentado

El análisis demográfico muestra que el segmento Profesional (33.7% de ventas) valora el rendimiento, la tecnología y los materiales premium, mientras que el segmento de Gestión responde mejor a la exclusividad y estatus. Se recomienda diseñar campañas específicas por tipo de cliente y crear un programa de fidelización para el 10% de clientes que generan el 40% de los ingresos, con beneficios como descuentos especiales, acceso anticipado y eventos exclusivos.

 3. Expansión Geográfica

EE. UU. sigue siendo el mercado más importante, pero aún tiene espacio para crecer con más puntos de venta y marketing local. Australia destaca como el segundo mercado con mayor potencial; se recomienda establecer un centro de distribución regional y alianzas con minoristas locales. Además, se podrían evaluar nuevos mercados como Canadá, Alemania o España, que tienen clientes con perfiles similares al público objetivo de Adventure Works.

 4. Estrategia Estacional

Las ventas son muy estacionales, por lo que se sugiere una gestión más dinámica del inventario. Antes de la temporada alta (marzo-abril), lanzar campañas de preventa con descuentos. Durante los meses pico (mayo a septiembre), garantizar alta disponibilidad de stock. En los meses bajos, realizar promociones de fin de año (octubre-diciembre) y considerar una línea de productos para invierno que mantenga las ventas activas todo el año.

 5. Retención de Clientes

El 10% de los clientes genera el 40% del revenue, por lo que es clave un programa VIP con niveles (Silver, Gold, Platinum) y beneficios crecientes como descuentos, eventos exclusivos y atención personalizada. Además, usar email marketing personalizado según historial de compra y aplicar un sistema NPS para medir satisfacción y prevenir la pérdida de clientes valiosos.


##  Dashboard
<img width="637" height="357" alt="image" src="https://github.com/user-attachments/assets/6e30011f-4110-4db9-9d95-5706ae5097a0" />
<img width="638" height="359" alt="image" src="https://github.com/user-attachments/assets/16072082-9cb6-497f-a84f-a9d7fa9b3a5e" />
<img width="638" height="361" alt="image" src="https://github.com/user-attachments/assets/f138f845-cae3-4982-a7b2-95605ac7e67e" />



##  Herramientas que Usé

* **Power BI Desktop** 
* **SQL Server** 
* **Lenguaje DAX** 
* **Power Query** 
