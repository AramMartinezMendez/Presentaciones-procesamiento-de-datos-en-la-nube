---
title: Apache Hive
layout: slide
---

<section>
    <h1>🐝 Apache Hive</h1>
    <p><em>El puente entre SQL y el Big Data</em></p>
    <p><small>Un data warehouse para Hadoop</small></p>
</section>


<!-- DIApositiva 2: ¿QUÉ ES? -->
<section>
    <h2>📖 ¿Qué es Apache Hive?</h2>
    <p>Es un <strong>sistema de almacenamiento de datos (Data Warehouse)</strong> construido sobre Apache Hadoop .</p>
    <p>Su propósito es permitir que los analistas y desarrolladores realicen consultas sobre grandes conjuntos de datos en HDFS usando un lenguaje similar a SQL, llamado <strong>HiveQL</strong> .</p>
    <p>Traduce el código SQL a trabajos de MapReduce, Tez o Spark, eliminando la necesidad de programar en lenguajes de bajo nivel .</p>
</section>

<!-- DIApositiva 3: CARACTERÍSTICAS PRINCIPALES -->
<section>
    <h2>⚙️ Características principales</h2>
    <ul>
        <li><strong>Interfaz SQL familiar:</strong> Baja barrera de entrada para quienes ya conocen SQL.</li>
        <li><strong>Almacenamiento flexible:</strong> Funciona sobre sistemas de archivos como HDFS y Amazon S3 .</li>
        <li><strong>Extensible:</strong> Soporta funciones personalizadas (UDF) para necesidades específicas .</li>
        <li><strong>Metastore centralizado:</strong> Almacena los metadatos (esquemas de tablas) en una base de datos externa (ej. MySQL, PostgreSQL) .</li>
        <li><strong>Optimización de costes (CBO):</strong> Mejora el rendimiento de las consultas complejas.</li>
    </ul>
</section>

<!-- DIApositiva 4: VENTAJAS (con desplazamiento vertical) -->
<section>
    <!-- Sub-diapositiva superior: Título y primeros puntos -->
    <section>
        <h2>✅ Ventajas</h2>
        <ul>
            <li><strong>Curva de aprendizaje suave:</strong> Ideal para equipos con experiencia en SQL. No se requiere programación compleja para análisis básicos .</li>
            <li><strong>Escalabilidad masiva:</strong> Capacidad para procesar y analizar datos de petabytes, aprovechando el poder de un clúster Hadoop .</li>
        </ul>
        <p style="margin-top: 30px;"><small>Presiona la flecha hacia abajo (↓) para ver más ventajas</small></p>
    </section>

    <!-- Sub-diapositiva inferior: Resto de ventajas -->
    <section>
        <h2 style="margin-top: 0;">✅ Ventajas (continuación)</h2>
        <ul>
            <li><strong>Ecosistema maduro:</strong> Se integra con herramientas de BI (Tableau, PowerBI) y Machine Learning (Spark, Mahout) .</li>
            <li><strong>Eficiencia en almacenamiento:</strong> Los formatos de archivo columnar (ORC, Parquet) reducen significativamente el espacio y mejoran la velocidad de lectura .</li>
        </ul>
        <p style="margin-top: 30px;"><small>Presiona la flecha hacia arriba (↑) para volver</small></p>
    </section>
</section>

<!-- DIApositiva 5: DESVENTAJAS (con desplazamiento vertical) -->
<section>
    <!-- Sub-diapositiva superior: Título y primeras desventajas -->
    <section>
        <h2>⚠️ Desventajas y limitaciones</h2>
        <ul>
            <li><strong>Alta latencia:</strong> No está diseñado para consultas en tiempo real (OLTP). Cada consulta tiene una sobrecarga de inicio significativa .</li>
            <li><strong>Actualizaciones complejas:</strong> Aunque versiones recientes (3.x) mejoran esto, históricamente las operaciones de actualización y borrado no son su punto fuerte. Está pensado para lecturas intensivas .</li>
        </ul>
        <p style="margin-top: 30px;"><small>Presiona la flecha hacia abajo (↓) para ver más</small></p>
    </section>

    <!-- Sub-diapositiva inferior: Resto de desventajas -->
    <section>
        <h2 style="margin-top: 0;">⚠️ Desventajas (continuación)</h2>
        <ul>
            <li><strong>Requiere configuración y tuning:</strong> Para obtener un buen rendimiento, es necesario optimizar las consultas y la configuración del clúster (particiones, formatos de archivo, etc.) .</li>
        </ul>
        <p style="margin-top: 30px;"><small>Presiona la flecha hacia arriba (↑) para volver</small></p>
    </section>
</section>

<!-- DIApositiva 6: USO LABORAL (con desplazamiento vertical) -->
<section>
    <!-- Sub-diapositiva superior: Título y primeros usos -->
    <section>
        <h2>💼 Uso laboral: ¿Para qué sirve en la industria?</h2>
        <p>Grandes empresas como CNET, Digg, Last.fm y TaoBao lo utilizan para :</p>
        <ul>
            <li><strong>🔍 Minería y análisis de logs:</strong> Para entender el comportamiento del usuario, detectar errores y auditar sistemas .</li>
            <li><strong>📊 Data Warehousing:</strong> Almacenar datos históricos para generar informes de negocio y dashboards, que luego se visualizan en herramientas de BI .</li>
        </ul>
        <p style="margin-top: 30px;"><small>Presiona la flecha hacia abajo (↓) para ver más casos de uso</small></p>
    </section>

    <!-- Sub-diapositiva inferior: Resto de usos -->
    <section>
        <h2 style="margin-top: 0;">💼 Uso laboral (continuación)</h2>
        <ul>
            <li><strong>⚙️ ETL (Extracción, Transformación y Carga):</strong> Como motor central para limpiar, transformar y enriquecer grandes volúmenes de datos antes de cargarlos a otros sistemas .</li>
            <li><strong>🤖 Preparación de datos para Machine Learning:</strong> Ayudar a preparar y transformar conjuntos de datos masivos para entrenar modelos con herramientas como Spark .</li>
        </ul>
        <p style="margin-top: 30px;"><small>Presiona la flecha hacia arriba (↑) para volver</small></p>
    </section>
</section>

<!-- DIApositiva 7: EFICACIA -->
<section>
    <h2>📈 ¿Es eficaz?</h2>
    <p>Sí, y los datos lo demuestran. Su eficacia se basa en la optimización:</p>
    <ul>
        <li><strong>Uso de formatos columnar (ORC/Parquet):</strong> Puede <strong>reducir el espacio de almacenamiento hasta en un 90%</strong> y <strong>acelerar las consultas entre 3 y 4 veces</strong> más rápido que los formatos de texto plano .</li>
        <li><strong>Optimizador de costes (CBO):</strong> Puede <strong>reducir el tiempo de ejecución de consultas complejas en casi un 40%</strong> .</li>
        <li><strong>Procesamiento de 10 mil millones de registros:</strong> Es común encontrar casos donde se procesan 10 mil millones de registros, y con una buena estrategia de particionado, las consultas que tardaban horas pueden pasar a segundos.</li>
    </ul>
</section>
