# 🚀 Dashboard de Ventas y Rentabilidad para AdventureWorks (Mi Proyecto de BI)

## 🌟 Introduccion

Este es mi proyecto de Business Intelligence. Mi objetivo principal fue tomar la popular base de datos AdventureWorks 2022 (que está en SQL Server) y transformarla en un Dashboard de Power BI útil y dinámico.

Decidí enfocarme en lo más importante para cualquier empresa: Saber dónde está ganando o perdiendo dinero. Así que, el informe está diseñado para que los gerentes puedan monitorear la Rentabilidad, el Margen Bruto y las tendencias de ventas de forma instantánea.

Lo mejor de este proyecto es que pude demostrar todo el proceso, desde la limpieza del dato hasta el insight final.

## Titulo del Proyecto
“Análisis de Ventas Adventure Works (2022–2024): Rentabilidad, Clientes y Oportunidades de Crecimiento”
Desarrollo de un dashboard ejecutivo en Power BI para el análisis integral del desempeño comercial de Adventure Works, abarcando ventas, costos, utilidad, clientes y productos entre 2022 y 2024.

## Objetivo del Proyecto:
Analizar la evolución de las ventas, costos y rentabilidad de Adventure Works entre 2022 y 2024, identificando los productos, países y segmentos de clientes más rentables para apoyar la toma de decisiones comerciales.

Objetivos específicos:

-Evaluar la rentabilidad por categoría y subcategoría de producto.
-Analizar el comportamiento temporal de ventas y costos.
-Identificar el perfil de los clientes más valiosos.
-Detectar oportunidades de crecimiento en países y ciudades clave.

## Descripción del Proyecto y Metodología

Para estructurar el trabajo, seguí estas 7 fases clave:

Planificación: Definí que los KPIs principales serían el Ventas Totales, Costo Total, Utilidad Bruta, Número de Pedidos y Clientes Únicos.

Obtención de Datos: Me conecté a la base de datos de AdventureWorks en SQL Server, seleccionando las tablas de hechos y dimensiones necesarias.

Preparación de Datos (Power Query): Limpié y renombré columnas, asegurando que los tipos de datos fueran correctos (fechas, moneda, etc.).

Modelado de Datos: Construí un Esquema Estrella, estableciendo relaciones Uno a Varios (1:*) entre las tablas para garantizar la estabilidad del informe.

Cálculos (DAX): Desarrollé la lógica de negocio. Las métricas esenciales incluyen el Beneficio, el Margen Bruto y el cálculo del Crecimiento Año a Año (YoY).

Visualización y Diseño: Creé el diseño del informe, usando tarjetas para los KPIs y gráficos (línea, dona, mapa) que responden a preguntas específicas de negocio.

Documentación y Entrega: Verifiqué que los números fueran precisos y preparé el archivo .pbix y esta documentación para compartir.

## Resultados Clave 
-Las ventas totales alcanzan $29,36M, con una utilidad bruta de $12,08M.
-Crecimiento sostenido entre 2022 y 2024, con tendencia positiva en ingresos y márgenes.
-La categoría Bikes representa el 96 % del total de ventas.
-Road Bikes y Mountain Bikes son los productos más vendidos y rentables.
-Algunas líneas de accesorios tienen ventas moderadas pero bajo margen.
-Se observa estacionalidad por trimestres, con picos de ventas en ciertos periodos
-Los Top 10 clientes generan una parte significativa de los ingresos totales.
-La mayoría de los clientes pertenecen a ocupaciones profesionales.
-El género masculino predomina ligeramente.

## Conclusiones
1. Adventure Works muestra un crecimiento sostenido en ventas y utilidad entre 2022 y 2024.
2. 2.La categoría Bikes domina el negocio, pero genera dependencia de un solo producto principal.
3. EE. UU. concentra la mayor parte de las ventas, representando riesgo si el mercado se contrae.
4. lgunos productos con alto volumen presentan bajos márgenes, por lo que requieren ajustes de precio o costo.
5. El perfil de cliente más rentable son los profesionales recurrentes, pero la empresa puede expandirse a otros segmentos.

## Insights 
La empresa tiene un desempeño sólido, pero una fuerte dependencia de la categoría “Bikes” y del mercado estadounidense.
Se puede mejorar la rentabilidad optimizando precios o costos en subcategorías con bajo margen y aprovechando la estacionalidad con campañas dirigidas.
Existe potencial para diversificar la cartera de clientes y captar nuevos segmentos, especialmente en ocupaciones o regiones con menor participación.

## Recomendaciones

Diversificación: desarrollar líneas de accesorios o ropa con mayor margen para reducir la dependencia de “Bikes”.

Expansión geográfica: fortalecer presencia en Australia y Francia con campañas regionales.

Gestión de precios: revisar márgenes en subcategorías menos rentables.

Fidelización: crear programas de puntos o beneficios para clientes frecuentes.

Optimización estacional: lanzar promociones en trimestres de menor demanda.

Monitoreo continuo: mantener actualizado el dashboard para decisiones en tiempo real.



## 📊 Dashboard
<img width="637" height="357" alt="image" src="https://github.com/user-attachments/assets/6e30011f-4110-4db9-9d95-5706ae5097a0" />
<img width="638" height="359" alt="image" src="https://github.com/user-attachments/assets/16072082-9cb6-497f-a84f-a9d7fa9b3a5e" />
<img width="638" height="361" alt="image" src="https://github.com/user-attachments/assets/f138f845-cae3-4982-a7b2-95605ac7e67e" />



## 💻 Herramientas que Usé

* **Power BI Desktop** 
* **SQL Server** 
* **Lenguaje DAX** 
* **Power Query** 
