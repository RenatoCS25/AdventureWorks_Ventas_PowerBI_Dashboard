### 🚴‍♂️ Adventure Works - Análisis Integral de Ventas

## Descripción del Proyecto
Adventure Works es una empresa multinacional de fabricación y venta de bicicletas y accesorios deportivos. Este proyecto presenta un análisis exhaustivo de datos de ventas, clientes y productos del período 2022-2024, implementando un modelo dimensional en Power BI para proporcionar insights accionables al equipo directivo.
El análisis se enfoca en identificar patrones de ventas, productos más rentables, segmentación de clientes y tendencias geográficas para optimizar estrategias comerciales y maximizar la rentabilidad.

## Objetivos del Proyecto

Analizar el desempeño comercial de Adventure Works durante el período 2022-2024

Identificar productos y categorías más rentables para optimizar el inventario

Segmentar clientes por características demográficas y comportamiento de compra

Detectar tendencias temporales en ventas para planificar estrategias estacionales

Visualizar KPIs clave mediante dashboards interactivos para la toma de decisiones


## Preguntas Clave del Análisis

1. ¿Cuál es la tendencia de ventas y rentabilidad en los últimos 3 años?
2. ¿Qué productos y categorías generan mayor margen de utilidad?
3. ¿Cuáles son las características demográficas de los clientes más valiosos?
4. ¿Qué mercados geográficos presentan mayor potencial de crecimiento?
5. ¿Existen patrones estacionales en las ventas que puedan aprovecharse?


## Metodología
# a. Preparación de Datos

Fuente de Datos: Base de datos AdventureWorks2022 (Microsoft SQL Server)

-Tablas Principales:

FactInternetSales: ~60,000 registros de transacciones

DimCustomer: 18,000 clientes únicos

DimProduct: Catálogo completo de productos

DimProductCategory y DimProductSubcategory: Jerarquías de productos

DimGeography: Datos geográficos (países, estados, ciudades)

DimDate: Tabla calendario para análisis temporal

Integración: Los datos fueron importados a Power BI y se estableció un modelo relacional tipo Star Schema para optimizar el rendimiento de las consultas.

# b. Procesamiento de Datos

-Exploración Inicial:
Análisis de estructura de tablas y relaciones
Identificación de claves primarias y foráneas
Evaluación de calidad de datos

-Limpieza de Datos:
Gestión de valores nulos en campos críticos
Validación de tipos de datos (fechas, montos, categorías)
Eliminación de registros duplicados
Normalización de nombres y categorías

-Transformación:
Creación de columnas calculadas (Utilidad Bruta, Margen %)
Generación de jerarquías temporales (Año > Trimestre > Mes)
Categorización de clientes por rangos de ingreso

# c. Análisis de Datos

- Métricas Clave Calculadas (DAX):
Ventas Totales = SUM(FactInternetSales[SalesAmount])
Costo Total = SUM(FactInternetSales[TotalProductCost])
Utilidad Bruta = [Ventas Totales] - [Costo Total]
Margen % = DIVIDE([Utilidad Bruta], [Ventas Totales], 0)
Clientes Únicos = DISTINCTCOUNT(FactInternetSales[CustomerKey])

-Análisis Realizados:
Análisis de tendencias temporales (series de tiempo)
Análisis de Pareto (80/20) para productos
Segmentación RFM básica de clientes
Análisis geográfico de ventas por país/ciudad
Comparación año contra año (YoY)

-Visualización:
Se desarrollaron 3 dashboards interactivos en Power BI con filtros dinámicos por fecha y categoría.

## Resultados
a. KPIs Principales del Negocio
MétricaValorInsightVentas Totales$29.36MCrecimiento sostenido 2022-2024Costo Total$17.28MEficiencia operativa del 59%Utilidad Bruta$12.08MMargen saludable del 41.2%Total Pedidos60,000Alto volumen de transaccionesClientes Únicos18,000Base de clientes sólidaTicket Promedio$489Valor alto por transacción

b. Análisis de Productos
Desempeño por Categoría: Bikes - $28.3M (96.46% de ventas)
Mountain Bikes: Categoría líder en ventas
Road Bikes: Segunda categoría más rentable
Touring Bikes: Menor participación pero alto margen
Accessories - $700K (2.38%)
Tires and Tubes: Mayor volumen
Alto potencial de venta cruzada
Clothing - $339K (1.15%)
Complemento de línea de productos

Top 5 Productos por Ventas:
Los 5 productos principales concentran aproximadamente el 35% del revenue total, evidenciando oportunidades de diversificación.

c. Análisis de Clientes
- Perfil del Cliente Top:

Nombre: Nichole Nara
Ventas Generadas: $13,295
Unidades Compradas: 13
Margen Contribuido: $5,250

- Segmentación Demográfica:
Profesionales $9.9M con 33.7% del total
Gestión $5.5 M con 18.7% del total
Obreros especializados $6.4M con 21.8% del total
Administrativos $4.7M con 16.0% del total
Otros $2.9M con 9.8% del total

-  Distribución por Género:

Masculino: 49.7% (30,000 clientes)
Femenino: 50.3% (30,000 clientes)
Distribución equilibrada sin sesgo de género

- Nivel Educativo:

Licenciatura completa: 30.04%
Universidad parcial: 27.52%
Postgrado: 20.04%
Mayor nivel educativo correlaciona con mayor gasto

- Ingresos por Cliente:

Rango $20K-$40K: Mayor volumen de ventas
Rango $60K-$80K: Clientes de mayor valor individual

d. Análisis Geográfico
- Distribución de Ventas por País:

United States: Mayor mercado (~45%)
United Kingdom: Segundo mercado importante
Australia: Mercado en crecimiento
France: Menor participación pero estable

- Ciudades Top por Ventas:

London, Paris, Wollongong, Warrnambool, Bendigo
Concentración en áreas metropolitanas

e. Patrones Temporales
- Tendencia Anual:

2022: $7M (fase inicial)
2023: $6M (consolidación)
2024: $16M (crecimiento acelerado)
CAGR aproximado: 51% anual

- Estacionalidad:

Picos de ventas consistentes en segundo semestre
Posible influencia de temporada deportiva y clima

- Patrones Semanales:
Los datos sugieren uso consistente a lo largo de la semana por clientes miembros.

## Principales Insights del Análisis

Insight 1: Dominio Absoluto de la Categoría Bikes
Hallazgo: Las bicicletas representan el 96.46% del total de ventas ($28.3M), mientras que Accessories y Clothing solo contribuyen con 3.54% combinados.
Implicación: La empresa depende críticamente de las ventas de bicicletas. Existe una oportunidad significativa para incrementar la venta cruzada de accesorios y ropa, que típicamente tienen márgenes más altos y menor costo de inventario.


Insight 2: Concentración de Valor en Pocos Clientes
Hallazgo: El top 10 de clientes genera aproximadamente el 40% del revenue total. El cliente principal, Nichole Nara, ha gastado $13,295 con un margen de contribución de $5,250.
Implicación: La retención de clientes VIP es crítica para la estabilidad del negocio. La pérdida de estos clientes tendría un impacto desproporcionado en los ingresos. Se requiere un programa de fidelización robusto.


Insight 3: Crecimiento Explosivo en 2024
Hallazgo: Las ventas de 2024 ($16M) superan más del doble a las de 2023 ($6M), representando un crecimiento del 166% year-over-year.
Implicación: El negocio está en una fase de crecimiento acelerado. Es el momento óptimo para escalar operaciones, optimizar la cadena de suministro y expandir la capacidad de inventario para sostener este momentum.

Insight 4: Segmento Profesional Como Core Customer
Hallazgo: Los clientes con ocupación "Profesional" generan $9.9M en ventas (33.7% del total), seguidos por "Obreros especializados" con $6.4M (21.8%).
Implicación: El perfil demográfico ideal es un profesional de ingresos medios-altos. Las campañas de marketing deben enfocarse en este segmento, destacando aspectos como calidad, tecnología y performance para alinearse con sus valores.


Insight 5: Equilibrio de Género en la Base de Clientes
Hallazgo: La distribución de clientes es prácticamente equitativa: 49.7% masculino y 50.3% femenino.
Implicación: No existe sesgo de género en la base de clientes, lo que valida que los productos de Adventure Works tienen appeal universal. Las estrategias de marketing deben mantener este equilibrio, evitando campañas que segmenten artificialmente por género.


Insight 6: Correlación Entre Educación y Gasto
Hallazgo: Clientes con educación universitaria completa (30.04%) y postgrado (20.04%) representan el 50% de la base de clientes pero generan proporcionalmente más revenue per capita.
Implicación: El nivel educativo es un predictor de valor de cliente. Las estrategias de adquisición deberían enfocarse en áreas geográficas y canales digitales donde se concentra este perfil demográfico (zonas universitarias, LinkedIn, publicaciones especializadas).


Insight 7: Mercados Geográficos con Potencial Diferenciado
Hallazgo: Estados Unidos domina las ventas (~45%), pero Australia muestra un crecimiento acelerado a pesar de ser un mercado más pequeño. Reino Unido mantiene un desempeño estable.
Implicación: Australia representa una oportunidad de expansión de alto potencial con menor competencia. Se recomienda aumentar inversión en marketing y distribución en este mercado antes de que se sature. UK requiere estrategias de revitalización.


Insight 8: Estacionalidad Pronunciada en Segundo Semestre
Hallazgo: Se observa un incremento significativo de ventas entre los meses de abril a septiembre, con picos máximos en verano. El cuarto trimestre muestra caída.
Implicación: La gestión de inventario debe anticipar la demanda estacional. Se recomienda implementar campañas pre-temporada (marzo-abril) para capturar early adopters y promociones de fin de año (noviembre-diciembre) para reducir inventario obsoleto.


Insight 9: Mountain Bikes y Road Bikes Impulsan la Rentabilidad
Hallazgo: Dentro de la categoría Bikes, Mountain Bikes y Road Bikes son las subcategorías más rentables, generando los mayores márgenes de utilidad bruta.
Implicación: El portafolio debe optimizarse hacia estas dos subcategorías. Touring Bikes, aunque genera ventas, tiene menor margen y podría considerarse para descontinuación parcial o reposicionamiento premium.


Insight 10: Alto Ticket Promedio Indica Mercado Premium
Hallazgo: El ticket promedio de $489 por transacción es significativamente alto, indicando que los clientes están comprando productos de gama media-alta.
Implicación: Adventure Works está bien posicionada en el segmento premium. Las estrategias de precio pueden mantenerse o incluso incrementarse ligeramente sin riesgo de pérdida significativa de clientes. El valor percibido es alto.


## Recomendaciones Estratégicas
1. Optimización de Portfolio de Productos

Expandir línea Mountain Bikes: Es la categoría más rentable
Impulsar venta cruzada de Accessories: Alto margen, bajo penetración
Revisar línea Clothing: Evaluar discontinuar productos de bajo rendimiento

2. Estrategias de Marketing Segmentado

Segmento Profesional: Campañas enfocadas en performance y tecnología
Segmento Gestión: Énfasis en exclusividad y estatus
Programas de fidelización: Para retener top 10% de clientes (generan 40% del revenue)

3. Expansión Geográfica

Priorizar mercado US: Mayor potencial, optimizar distribución
Desarrollar Australia: Mercado emergente con buen desempeño
Evaluar nuevos mercados: Considerar expansión a Canadá o Alemania

4. Optimización Estacional

Campañas pre-temporada: Marzo-Abril para capturar demanda de verano
Promociones de fin de año: Octubre-Diciembre para liquidar inventario
Lanzamientos de productos: Alinear con picos estacionales

5. Mejora en Retención de Clientes

Programa VIP: Para clientes con gasto >$10K anual
Email marketing personalizado: Basado en historial de compra
Encuestas de satisfacción: Implementar NPS para medir lealtad



##  Dashboard
<img width="637" height="357" alt="image" src="https://github.com/user-attachments/assets/6e30011f-4110-4db9-9d95-5706ae5097a0" />
<img width="638" height="359" alt="image" src="https://github.com/user-attachments/assets/16072082-9cb6-497f-a84f-a9d7fa9b3a5e" />
<img width="638" height="361" alt="image" src="https://github.com/user-attachments/assets/f138f845-cae3-4982-a7b2-95605ac7e67e" />



##  Herramientas que Usé

* **Power BI Desktop** 
* **SQL Server** 
* **Lenguaje DAX** 
* **Power Query** 
