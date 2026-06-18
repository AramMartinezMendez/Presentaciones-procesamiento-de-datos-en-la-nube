---
title: Apache Hive
layout: slide
---

<section>
    <h1>🐝 Apache Hive</h1>
    <p><em>El puente entre SQL y el Big Data</em></p>
    <p><small>Un data warehouse para Hadoop</small></p>
</section>

<section>
    <h2>📖 ¿Qué es Apache Hive?</h2>
    <p>Es un <strong>sistema de almacenamiento de datos (Data Warehouse)</strong> construido sobre Apache Hadoop [citation:2][citation:5].</p>
    <p>Su propósito es permitir que los analistas y desarrolladores realicen consultas sobre grandes conjuntos de datos en HDFS usando un lenguaje similar a SQL, llamado <strong>HiveQL</strong> [citation:2][citation:8].</p>
    <p>Traduce el código SQL a trabajos de MapReduce, Tez o Spark, eliminando la necesidad de programar en lenguajes de bajo nivel [citation:2].</p>
</section>

<section>
    <h2>⚙️ Características principales</h2>
    <ul>
        <li><strong>Interfaz SQL familiar:</strong> Baja barrera de entrada para quienes ya conocen SQL.</li>
        <li><strong>Almacenamiento flexible:</strong> Funciona sobre sistemas de archivos como HDFS y Amazon S3 [citation:3][citation:9].</li>
        <li><strong>Extensible:</strong> Soporta funciones personalizadas (UDF) para necesidades específicas [citation:5][citation:9].</li>
        <li><strong>Metastore centralizado:</strong> Almacena los metadatos (esquemas de tablas) en una base de datos externa (ej. MySQL, PostgreSQL) [citation:2][citation:9].</li>
        <li><strong>Optimización de costes (CBO):</strong> Mejora el rendimiento de las consultas complejas.</li>
    </ul>
</section>

<section>
    <h2>✅ Ventajas</h2>
    <ul>
        <li><strong>Curva de aprendizaje suave:</strong> Ideal para equipos con experiencia en SQL. No se requiere programación compleja para análisis básicos [citation:2][citation:6][citation:9].</li>
        <li><strong>Escalabilidad masiva:</strong> Capacidad para procesar y analizar datos de petabytes, aprovechando el poder de un clúster Hadoop [citation:9].</li>
        <li><strong>Ecosistema maduro:</strong> Se integra con herramientas de BI (Tableau, PowerBI) y Machine Learning (Spark, Mahout) [citation:1][citation:4][citation:7].</li>
        <li><strong>Eficiencia en almacenamiento:</strong> Los formatos de archivo columnar (ORC, Parquet) reducen significativamente el espacio y mejoran la velocidad de lectura [citation:2][citation:5][citation:9].</li>
    </ul>
</section>

<section>
    <h2>⚠️ Desventajas y limitaciones</h2>
    <ul>
        <li><strong>Alta latencia:</strong> No está diseñado para consultas en tiempo real (OLTP). Cada consulta tiene una sobrecarga de inicio significativa [citation:2][citation:7].</li>
        <li><strong>Actualizaciones complejas:</strong> Aunque versiones recientes (3.x) mejoran esto, históricamente las operaciones de actualización y borrado no son su punto fuerte. Está pensado para lecturas intensivas [citation:9].</li>
        <li><strong>Requiere configuración y tuning:</strong> Para obtener un buen rendimiento, es necesario optimizar las consultas y la configuración del clúster (particiones, formatos de archivo, etc.) [citation:8][citation:9].</li>
    </ul>
</section>

<section>
    <h2>💼 Uso laboral: ¿Para qué sirve en la industria?</h2>
    <p>Grandes empresas como CNET, Digg, Last.fm y TaoBao lo utilizan para [citation:1][citation:10]:</p>
    <ul>
        <li><strong>🔍 Minería y análisis de logs:</strong> Para entender el comportamiento del usuario, detectar errores y auditar sistemas [citation:1][citation:5][citation:10].</li>
        <li><strong>📊 Data Warehousing:</strong> Almacenar datos históricos para generar informes de negocio y dashboards, que luego se visualizan en herramientas de BI [citation:1][citation:7][citation:9].</li>
        <li><strong>⚙️ ETL (Extracción, Transformación y Carga):</strong> Como motor central para limpiar, transformar y enriquecer grandes volúmenes de datos antes de cargarlos a otros sistemas [citation:5][citation:9].</li>
        <li><strong>🤖 Preparación de datos para Machine Learning:</strong> Ayudar a preparar y transformar conjuntos de datos masivos para entrenar modelos con herramientas como Spark [citation:1][citation:4][citation:10].</li>
    </ul>
</section>

<section>
    <h2>📈 ¿Es eficaz?</h2>
    <p>Sí, y los datos lo demuestran. Su eficacia se basa en la optimización:</p>
    <ul>
        <li><strong>Uso de formatos columnar (ORC/Parquet):</strong> Puede <strong>reducir el espacio de almacenamiento hasta en un 90%</strong> y <strong>acelerar las consultas entre 3 y 4 veces</strong> más rápido que los formatos de texto plano [citation:2][citation:5].</li>
        <li><strong>Optimizador de costes (CBO):</strong> Puede <strong>reducir el tiempo de ejecución de consultas complejas en casi un 40%</strong> [citation:2].</li>
        <li><strong>Procesamiento de 10 mil millones de registros:</strong> Es común encontrar casos donde se procesan 10 mil millones de registros, y con una buena estrategia de particionado, las consultas que tardaban horas pueden pasar a segundos.</li>
    </ul>
</section>
