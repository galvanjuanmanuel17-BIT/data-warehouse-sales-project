Data Warehouse Project – Online Retail Analytics
📌 Descripción del proyecto

Este proyecto tiene como objetivo transformar un dataset transaccional (OLTP) en un modelo analítico (Data Warehouse) orientado a la generación de insights mediante herramientas de Business Intelligence.

El trabajo surge inicialmente como un trabajo práctico universitario y fue reconvertido en un proyecto de portfolio profesional enfocado en Data Analytics / BI.

🎯 Objetivo

Construir un proceso end-to-end que permita:

Limpiar y transformar datos transaccionales
Diseñar un modelo dimensional (modelo estrella)
Analizar la información con herramientas de BI
Generar insights de negocio a partir de los datos
🗂 Dataset
Nombre: Online Retail Dataset
Cantidad de registros: ~500.000
Tipo de datos: Transaccional (ventas)
Fuente: Kaggle

El dataset contiene información sobre transacciones de una tienda online, incluyendo productos, clientes, cantidades, precios y fechas.

⚙️ Proceso ETL

El proceso ETL fue desarrollado en Python utilizando Pandas en Google Colab.

🔹 1. Extracción
Carga del dataset original en formato Excel
🔹 2. Transformación

Se realizaron las siguientes transformaciones:

🧹 Limpieza de datos
Eliminación de registros con CustomerID nulo
Eliminación de precios inválidos (UnitPrice <= 0)
Identificación y separación de devoluciones (Quantity < 0)
🧮 Creación de métricas
Revenue = Quantity * UnitPrice
🧠 Enriquecimiento de datos
Creación de la variable Region a partir de Country
Creación de la variable Categoria a partir de Description
📅 Variables temporales
Año (Year)
Mes (Month)
Trimestre (Quarter)
🏷 Estandarización
Renombrado de columnas para facilitar el modelado en BI:
InvoiceNo → Invoice_ID
StockCode → Product_ID
CustomerID → Customer_ID
🔹 3. Carga
Exportación del dataset limpio a formato .csv
Generación de una muestra reducida (~50.000 registros) para GitHub
Almacenamiento del dataset completo en entorno externo (Google Drive)
🏗 Modelo de datos (próximamente)

Se implementará un modelo dimensional tipo estrella (Star Schema) compuesto por:

⭐ Tabla de hechos
fact_sales
Revenue
Quantity
Claves hacia dimensiones
🧩 Dimensiones
dim_product
Producto, descripción, categoría
dim_customer
Cliente, país, región
dim_time
Fecha, año, mes, trimestre
📊 Jerarquías
Tiempo: Año → Mes → Día
Producto: Categoría → Producto
Región: Región → País
📊 Análisis y visualización (próximamente)

El modelo será implementado en Power BI para el desarrollo de dashboards interactivos.

KPIs a desarrollar:
Revenue total
Cantidad de ventas
Ticket promedio
Ventas por categoría
Ventas por región
Evolución temporal de ventas
💡 Insights esperados

El proyecto busca responder preguntas de negocio como:

¿Qué categorías generan mayor revenue?
¿Qué regiones concentran las ventas?
¿Existe estacionalidad en las ventas?
¿Quiénes son los clientes más relevantes?
🛠 Herramientas utilizadas
Python (Pandas, NumPy)
Google Colab
GitHub
Power BI (en desarrollo)

🚀 Estado del proyecto
✅ ETL completo
🔄 Modelado dimensional (en progreso)
🔄 Dashboard en Power BI (pendiente)
🔄 Generación de insights (pendiente)

💼 Enfoque profesional

Este proyecto fue desarrollado con un enfoque orientado a simular un caso real de negocio, aplicando buenas prácticas de:

Limpieza y calidad de datos
Diseño de modelos analíticos
Pensamiento orientado a negocio
Preparación de datos para BI


📌 Próximos pasos
Construcción del modelo estrella
Desarrollo del dashboard en Power BI
Generación de insights y storytelling
Publicación de avances en LinkedIn
