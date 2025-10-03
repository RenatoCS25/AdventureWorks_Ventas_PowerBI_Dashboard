# 🚀 Dashboard de Ventas y Rentabilidad para AdventureWorks (Mi Proyecto de BI)

## 🌟 Un Resumen Rápido

Este es mi proyecto de Business Intelligence. Mi objetivo principal fue tomar la popular base de datos AdventureWorks 2022 (que está en SQL Server) y transformarla en un Dashboard de Power BI útil y dinámico.

Decidí enfocarme en lo más importante para cualquier empresa: **saber dónde está ganando o perdiendo dinero**. Así que, el informe está diseñado para que los gerentes puedan monitorear la **Rentabilidad**, el **Margen Bruto** y las tendencias de ventas de forma instantánea.

Lo mejor de este proyecto es que pude demostrar todo el proceso, desde la limpieza del dato hasta el *insight* final.

---

## 🛠️ El Workflow: Cómo construí el proyecto (7 Fases)

Para asegurarme de que el proyecto fuera robusto, seguí esta metodología paso a paso:

### Fase 1: Entender qué Necesitaba el Negocio
Antes de tocar un dato, definí las **preguntas clave**. Sabía que tenía que responder: *¿Cuánto estamos vendiendo?, ¿Cuánto estamos ganando?, ¿Quiénes son nuestros mejores clientes?* Esto me llevó a definir los KPIs esenciales como **Beneficio**, **Margen Bruto** y **Ventas Totales**.

### Fase 2: Conexión con la Fuente
Me conecté directamente a la base de datos **AdventureWorks 2022 en SQL Server**. Fue clave identificar las tablas que realmente necesitaba, principalmente `FactInternetSales` (mis hechos) y todas las tablas de dimensión (`DimProduct`, `DimDate`, etc.).

### Fase 3: ¡A Limpiar y Transformar! (Power Query)
Aquí pasé tiempo en **Power Query** (el editor de Power BI). Hice las tareas necesarias para dejar los datos listos:
* **Limpié** los nombres de las columnas para que fueran amigables (de `SalesAmount` a `Ventas Totales`).
* **Aseguré** los tipos de datos correctos (fechas, monedas, etc.).

### Fase 4: La Arquitectura del Modelo
Para que los filtros funcionaran correctamente y el rendimiento fuera rápido, organicé todo en un **Esquema Estrella**. Conecté mi tabla de hechos a todas mis tablas de dimensión con relaciones **Uno a Varios (1:\*)**. Esto es crucial para la estabilidad del informe.

### Fase 5: La Magia de DAX
Esta fue una de mis partes favoritas. Usé **DAX** para crear la lógica de negocio, no solo para sumar. Las medidas más importantes que creé fueron:
* **`Beneficio`**: La resta simple entre mis ventas y costes.
* **`Margen Bruto (%)`**: La fórmula que indica la rentabilidad real.
* **`Crecimiento Año a Año (YoY)`**: Para medir si estamos mejorando o empeorando respecto al periodo pasado.

### Fase 6: El Diseño (Hacerlo Útil y Bonito)
Aquí convertí los números en la interfaz que vieron. Puse los **KPIs clave** en tarjetas grandes en la parte superior para que fueran lo primero que viera el usuario. Elegí un diseño limpio y gráficos apropiados (como el de línea para la tendencia y el mapa para el impacto geográfico).

### Fase 7: Documentación y Entrega
Finalmente, verifiqué que mis números fueran correctos (validación) y preparé la entrega. Eso incluye este `README.md` y el archivo `.pbix`, listos para ser compartidos y revisados.

---

## 📊 Vistazo Rápido a Mi Dashboard

*(**Instrucción:** Inserta aquí tus capturas de pantalla)*

| Captura de Pantalla | Lo que me pareció más interesante (Conclusión) |
| :--- | :--- |
| `![Dashboard Principal](Images/image_63bbca.jpg)` | Me di cuenta de que, aunque las ventas crecen, el **Margen Bruto** debe ser monitoreado de cerca para asegurar que el crecimiento sea rentable. |
| `![Análisis Geográfico](Images/image_63be73.jpg)` | La mayor parte del negocio se concentra en dos o tres países clave. Es el momento de evaluar si es mejor invertir en esos mercados o explorar nuevas geografías. |

---

## 💻 Herramientas que Usé

* **Power BI Desktop** (El motor principal del análisis y la visualización)
* **SQL Server** (La fuente de todos los datos)
* **Lenguaje DAX** (Para toda la lógica de negocio y las métricas)
* **Power Query** (Para la limpieza inicial de los datos)
