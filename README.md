# RappiPlus

Performance evaluation of the RappiPlus subscription service, to support data-based business decisions.

## Datasets
- `rappiplus_orders_raw.csv` — orders, prices, discounts, revenue
- `rappiplus_catalog.csv` — product costs, categories, suppliers
- `rappiplus_marketing_spend.csv` — marketing spend by channel and country
- `events`, `users`, `user_activity` via SQL — user behaviour on the platform
- `experiment_checkout_ui.csv` — checkout A/B experiment

Merged orders after joining with catalog: 24,996 rows × 17 columns.

## Tools
Python, Pandas, SQL (SQLAlchemy, PostgreSQL), Statsmodels, Tableau, Jupyter Notebook.

## What I did
1. Data-quality validation in Python: load, explore and clean orders, catalog and marketing data.
2. Profitability: revenue, costs, profit, average ticket, product volume, marketing-spend distribution.
3. Conversion funnel: unique users per event, ordered by user flow, conversion rate between steps, and the stage with the largest drop.
4. Cohort retention: users after registration and permanence over time.
5. Statistical test: checkout-UI experiment, metric conversion (1 = completed purchase, 0 = not). H0: control conversion equals treatment conversion. H1: treatment conversion differs from control. Proportions Z-test, alpha = 0.05.
6. Dashboard in Tableau: executive KPIs (total revenue, total profit, total marketing spend, average ticket, average products per order), monthly revenue/profit and year-to-date line charts, revenue/profit by product and category bar charts, and a detail view with order, product, quantity, revenue, cost and profit, with negative profit in red and positive profit in green, filtered by date and product category.

## Key findings — outputs shown
- Total orders: 24,996
- Average ticket: 2,079.88
- Cost: 43,132,326.49
- Marketing spend: 2,871,843.53
- Profit (revenue − cost − marketing spend): 5,984,439.54
- Average quantity per order: 7.11
- Top product by quantity: Laptop-Gaming-16GB, 144,206
- Marketing spend by channel: social 918,043.21; organic 913,533.01; paid_search 863,088.21; unknown 177,179.10
- Checkout A/B test: z = 0.81, p = 0.42. H0 is not rejected: no evidence of a significant impact on conversion in this test at alpha = 0.05.

## How to run
Open the `.ipynb` in Jupyter or Colab and run all cells. The Tableau workbook is in this repo as `RappiPlus - Business Analytics Dashboard -AV.twbx`.

---

## Versión en español

# RappiPlus

Evaluación del rendimiento del servicio de suscripción RappiPlus, para apoyar decisiones empresariales basadas en datos.

## Conjuntos de datos
- `rappiplus_orders_raw.csv` — pedidos, precios, descuentos, ingresos
- `rappiplus_catalog.csv` — costos de productos, categorías, proveedores
- `rappiplus_marketing_spend.csv` — gasto en marketing por canal y país
- `events`, `users`, `user_activity` mediante SQL — comportamiento de los usuarios en la plataforma
- `experiment_checkout_ui.csv` — experimento A/B de checkout

Pedidos fusionados tras unir con el catálogo: 24,996 filas × 17 columnas.

## Herramientas
Python, Pandas, SQL (SQLAlchemy, PostgreSQL), Statsmodels, Tableau, Jupyter Notebook.

## Qué hice
1. Validación de calidad de datos en Python: cargar, explorar y limpiar datos de pedidos, catálogo y marketing.
2. Rentabilidad: ingresos, costos, ganancias, ticket promedio, volumen de productos, distribución del gasto en marketing.
3. Embudo de conversión: usuarios únicos por evento, ordenados según el flujo de usuario, tasa de conversión entre pasos y la etapa con la mayor caída.
4. Retención por cohortes: usuarios después del registro y permanencia en el tiempo.
5. Prueba estadística: experimento de interfaz de checkout, métrica conversión (1 = compra completada, 0 = no). H0: la conversión del control es igual a la conversión del tratamiento. H1: la conversión del tratamiento difiere de la del control. Prueba Z de proporciones, alfa = 0.05.
6. Panel en Tableau: KPI ejecutivos (ingreso total, ganancia total, gasto total en marketing, ticket promedio, productos promedio por pedido), gráficos de líneas de ingreso/ganancia mensual y acumulado en el año, gráficos de barras de ingreso/ganancia por producto y categoría, y una vista de detalle con pedido, producto, cantidad, ingreso, costo y ganancia, con la ganancia negativa en rojo y la positiva en verde, filtrada por fecha y categoría de producto.

## Hallazgos clave — resultados mostrados
- Total de pedidos: 24,996
- Ticket promedio: 2,079.88
- Costo: 43,132,326.49
- Gasto en marketing: 2,871,843.53
- Ganancia (ingreso − costo − gasto en marketing): 5,984,439.54
- Cantidad promedio por pedido: 7.11
- Producto principal por cantidad: Laptop-Gaming-16GB, 144,206
- Gasto en marketing por canal: social 918,043.21; organic 913,533.01; paid_search 863,088.21; unknown 177,179.10
- Prueba A/B de checkout: z = 0.81, p = 0.42. No se rechaza H0: no hay evidencia de un impacto significativo en la conversión en esta prueba con alfa = 0.05.

## Cómo ejecutar
Abrir el `.ipynb` en Jupyter o Colab y ejecutar todas las celdas. El libro de trabajo de Tableau está en este repositorio como `RappiPlus - Business Analytics Dashboard -AV.twbx`.
