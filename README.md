#  Adventure Works - Análisis Integral de Ventas

## 1. Definicion del Problema y los Objetivos
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


## 2. Metodologia

La metodología se estructuró en tres fases: **preparación**, **transformación** y **análisis** de los datos.

### 1. Preparación de los Datos
Se utilizó el dataset AdventureWorks2022 (Microsoft SQL Server, 2022–2024), empleando las tablas **FactInternetSales**, **DimCustomer**, **DimProduct**, **DimGeography** y **DimDate**.  
El modelo se diseñó bajo un **esquema estrella (Star Schema)** e importó a **Power BI** para optimizar relaciones y consultas.

### 2. Limpieza y Transformación
Se validó la estructura y calidad de los datos mediante:
- **Limpieza:** eliminación de duplicados, corrección de formatos y manejo de valores nulos.  
- **Transformación:** creación de columnas calculadas (*Utilidad Bruta*, *Margen %*), jerarquías temporales (*Año → Trimestre → Mes*) y segmentación de clientes por nivel de ingreso y ocupación.

### 3. Análisis e Insights
Se desarrollaron medidas **DAX** clave como:  
Ventas Totales, Costo Total, Utilidad Bruta, Margen % y Clientes Únicos.  

El análisis incluyó:
- Tendencias temporales (YoY, CAGR)  
- Análisis Pareto (80/20)  
- Segmentación RFM de clientes  
- Análisis geográfico de ventas  
- Rentabilidad por categoría  

### KPIs Principales

| Métrica | Valor | Insight |
|----------|--------|----------|
| Ventas Totales | $29.36M | Crecimiento sostenido |
| Costo Total | $17.28M | Eficiencia operativa del 59% |
| Utilidad Bruta | $12.08M | Margen saludable del 41.2% |
| Clientes Únicos | 18,000 | Base de clientes sólida |
| Ticket Promedio | $489 | Mercado de gama media-alta |


## 3. Comunicación de Resultados
### Dashboards en Power BI
1.	Resumen Ejecutivo: KPIs principales, tendencia anual, distribución geográfica.
2.	Productos: Rentabilidad por categoría/subcategoría y análisis temporal.
3.	Clientes: Segmentación demográfica, top clientes, y comportamiento de compra.
### Visualización:
<img width="691" height="388" alt="image" src="https://github.com/user-attachments/assets/d01f7f90-deb8-4388-852a-055a66c8b6bc" />
<img width="691" height="388" alt="image" src="https://github.com/user-attachments/assets/58483a18-d399-4e52-8a27-98f36ce7ff9e" />
<img width="692" height="388" alt="image" src="https://github.com/user-attachments/assets/2f96c045-60c3-41a7-a832-426f4af73aba" />


## 4. Principales Insights
1. Dominio Absoluto de la Categoría Bikes

Las bicicletas representan el 96.46% del total de ventas ($28.3M), mientras que Accessories y Clothing solo contribuyen con 3.54% combinados. Este revela que la empresa depende críticamente de las ventas de bicicletas, lo cual representa tanto una fortaleza como un riesgo de concentración. Existe una oportunidad significativa para incrementar la venta cruzada de accesorios y ropa, que típicamente tienen márgenes más altos y menor costo de inventario. La diversificación del portafolio podría mejorar la estabilidad del negocio y reducir la vulnerabilidad ante cambios en la demanda de bicicletas.

2. Mayor margen de la bicicletas de montaña 
Las bicicletas de montaña destacan por tener el mayor margen de rentabilidad, pero su volumen de ventas es 38% menor que el de las bicicletas de carretera, lo que sugiere una oportunidad de crecimiento enfocada en aumentar unidades sin sacrificar margen.

3. Crecimiento Explosivo en 2024

En 2024, las ventas crecieron 166% interanual, impulsadas principalmente por el aumento en la venta de bicicletas y la incorporación de accesorios y ropa, lo que indica una fase de expansión acelerada del negocio.

4. Segmento Profesional como cliente principal

Los clientes con ocupación profesional generan el 33.7% de las ventas, consolidándose como el segmento más relevante y definiendo un perfil de cliente con alto poder adquisitivo y enfoque en calidad y performance.

5. Equilibrio de Género en la Base de Clientes

La base de clientes muestra una distribución de género equilibrada (49.7% masculino, 50.3% femenino), lo que amplía el mercado objetivo y valida una estrategia de producto y comunicación inclusiva.

6. Correlación Entre Educación y Gasto

Los clientes con educación universitaria y postgrado representan el 50% de la base, pero generan un mayor ingreso per cápita, lo que posiciona el nivel educativo como un fuerte predictor del valor del cliente.

## 5. Recomendaciones Estratégicas

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


##  Herramientas que Usé

* **Power BI Desktop** 
* **SQL Server** 
* **Lenguaje DAX** 
* **Power Query** 
