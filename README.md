# RetailPro — Análisis SQL y Documentación

Repositorio del proyecto **RetailPro**, enfocado en la modelación y consulta SQL de clientes, productos, categorías y ventas para apoyar el análisis comercial de forma clara y reproducible.

## Estructura del proyecto
- `RetailPro.sql`: Script inicial de creación de la base de datos `RetailPro`.
- `sql/vista_base_ventas.sql`: Consulta base con unión de `ventas`, `clientes`, `productos` y `categorias`.
- `sql/consultas_comerciales.sql`: Consultas de resumen mensual, ranking de productos por facturación y recurrencia de clientes.
- `docs/`: Documentación del proyecto, validación de métricas y hallazgos para el equipo comercial.

## Herramientas utilizadas
- **Base de datos:** SQL (compatible con MySQL: `CREATE DATABASE`, `MONTH()`, `SUM()`, `COUNT()`, `AVG()`, `INNER JOIN`).
- **Control de versiones:** Git y GitHub.
- **Documentación y apoyo:** Google Docs y herramientas de IA gratuitas utilizadas como co-piloto con revisión humana.

## Cómo ejecutar los scripts SQL
1. Creá la base de datos ejecutando `CREATE DATABASE RetailPro;` y seleccionála (`USE RetailPro;`).
2. Creá y cargá las tablas `clientes`, `categorias`, `productos` y `ventas`.
3. Ejecutá la consulta base (`INNER JOIN` entre las tablas) para verificar la integridad de los registros.
4. Ejecutá las consultas de análisis: resumen mensual, top 5 de productos por facturación y clientes recurrentes.

## Notas de validación analítica
- Revisar el rango de fechas (`YEAR` y `MONTH`) antes de interpretar estacionalidad.
- Cruzar `id_producto` y `id_cliente` con sus respectivas tablas maestras para dar contexto de negocio a los resultados.