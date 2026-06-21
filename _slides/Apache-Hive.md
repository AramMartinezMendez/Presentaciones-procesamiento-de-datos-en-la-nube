---
title: Apache Hive
layout: slide
---

<!-- ============================================ -->
<!-- ESTILOS GLOBALES PARA EVITAR DESBORDES       -->
<!-- ============================================ -->
<style>
  .reveal .slides section {
    max-height: 92vh !important;
    height: 92vh !important;
    padding: 10px 30px !important;
    box-sizing: border-box !important;
    overflow: hidden !important;
  }
  .reveal .slides section > div {
    max-height: 85vh;
    overflow-y: auto;
    padding-right: 5px;
  }
  .reveal ul, .reveal p {
    font-size: 0.85em !important;
    line-height: 1.4 !important;
  }
  .reveal li {
    margin-bottom: 6px !important;
  }
  .reveal h2 {
    font-size: 1.8em !important;
    margin-bottom: 15px !important;
  }
  .reveal h3 {
    font-size: 1.2em !important;
    margin-bottom: 10px !important;
  }
  .reveal .grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }
  .reveal .card {
    background: rgba(255,255,255,0.03);
    padding: 12px 16px;
    border-radius: 8px;
    border-left: 3px solid #f7971e;
  }
  .reveal .card-green {
    border-left-color: #4ade80;
  }
  .reveal .card-red {
    border-left-color: #f87171;
  }
  .reveal .card-blue {
    border-left-color: #60a5fa;
  }
  .reveal .img-container {
    max-height: 280px;
    overflow: hidden;
    border-radius: 8px;
    margin: 8px 0;
  }
  .reveal .img-container img {
    max-height: 260px;
    width: auto;
    display: block;
    margin: 0 auto;
  }
  .reveal .badge {
    display: inline-block;
    padding: 4px 14px;
    border-radius: 20px;
    font-size: 0.7em;
    font-weight: bold;
  }
  .reveal .badge-orange {
    background: rgba(247, 151, 30, 0.2);
    color: #ffd200;
  }
  .reveal .badge-green {
    background: rgba(74, 222, 128, 0.2);
    color: #4ade80;
  }
  .reveal .badge-red {
    background: rgba(248, 113, 113, 0.2);
    color: #f87171;
  }
  .reveal .badge-blue {
    background: rgba(96, 165, 250, 0.2);
    color: #60a5fa;
  }
  /* Scroll suave para el contenido */
  .reveal .scroll-content::-webkit-scrollbar {
    width: 4px;
  }
  .reveal .scroll-content::-webkit-scrollbar-thumb {
    background: #f7971e;
    border-radius: 4px;
  }
  .reveal .scroll-content::-webkit-scrollbar-track {
    background: transparent;
  }
</style>

<!-- ============================================ -->
<!-- SLIDE 1: PORTADA                             -->
<!-- ============================================ -->
<section style="text-align: center; background: linear-gradient(135deg, #1a1a2e, #16213e, #0f3460);">
    <div style="display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100%;">
        <span style="font-size: 3.5em; display: block; margin-bottom: 10px;">🐝</span>
        <h1 style="font-size: 3em; background: linear-gradient(to right, #f7971e, #ffd200); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; margin: 0;">Apache Hive</h1>
        <p style="font-size: 1.5em; color: #e0e0e0; margin: 8px 0 5px 0;"><em>El puente entre SQL y el Big Data</em></p>
        <div style="width: 60px; height: 3px; background: linear-gradient(to right, #f7971e, #ffd200); margin: 10px auto;"></div>
        <p style="font-size: 1em; color: #aaa; letter-spacing: 2px;">⚡ Data Warehouse para Hadoop</p>
        <p style="font-size: 0.7em; color: #666; margin-top: 25px;">Presiona → para comenzar</p>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 2: ¿QUÉ ES?                           -->
<!-- ============================================ -->
<section style="background: linear-gradient(135deg, #0d1117, #161b22);">
    <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
        <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 15px;">
            <span style="font-size: 2em;">📖</span>
            <h2 style="margin: 0; color: #f7971e; font-size: 1.8em;">¿Qué es Apache Hive?</h2>
        </div>
        <div style="background: rgba(255,255,255,0.03); border-left: 4px solid #f7971e; padding: 18px 22px; border-radius: 8px;">
            <p style="font-size: 1em; line-height: 1.5; color: #e6e6e6; margin: 0;">
                <strong style="color: #ffd200;">Data Warehouse</strong> sobre Hadoop para consultas SQL en grandes volúmenes de datos.
            </p>
            <p style="font-size: 0.9em; line-height: 1.5; color: #ccc; margin: 10px 0 0 0;">
                Usa <strong style="color: #f7971e;">HiveQL</strong> → traduce a MapReduce, Tez o Spark.
            </p>
        </div>
        <div style="display: flex; gap: 15px; margin-top: 15px; justify-content: center;">
            <div style="text-align: center; background: rgba(247, 151, 30, 0.08); padding: 10px 18px; border-radius: 8px; border: 1px solid rgba(247, 151, 30, 0.15);">
                <span style="font-size: 1.4em; display: block;">📊</span>
                <span style="color: #aaa; font-size: 0.75em;">Petabytes de datos</span>
            </div>
            <div style="text-align: center; background: rgba(247, 151, 30, 0.08); padding: 10px 18px; border-radius: 8px; border: 1px solid rgba(247, 151, 30, 0.15);">
                <span style="font-size: 1.4em; display: block;">🔄</span>
                <span style="color: #aaa; font-size: 0.75em;">SQL → MapReduce/Spark</span>
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 3: CARACTERÍSTICAS                     -->
<!-- ============================================ -->
<section style="background: linear-gradient(135deg, #0d1117, #161b22);">
    <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
        <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
            <span style="font-size: 2em;">⚙️</span>
            <h2 style="margin: 0; color: #f7971e; font-size: 1.8em;">Características</h2>
        </div>
        <div class="grid-2">
            <div class="card">
                <strong style="color: #ffd200;">🗄️ Interfaz SQL</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Baja barrera de entrada para equipos con SQL.</p>
            </div>
            <div class="card">
                <strong style="color: #ffd200;">☁️ Almacenamiento flexible</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">HDFS, Amazon S3 y otros sistemas.</p>
            </div>
            <div class="card">
                <strong style="color: #ffd200;">🧩 Extensible</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Funciones personalizadas (UDF) en Java/Python.</p>
            </div>
            <div class="card">
                <strong style="color: #ffd200;">📁 Metastore centralizado</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Metadatos en MySQL, PostgreSQL, etc.</p>
            </div>
            <div class="card" style="grid-column: span 2;">
                <strong style="color: #ffd200;">🚀 Optimizador de costes (CBO)</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Mejora el rendimiento de consultas complejas.</p>
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 4: VENTAJAS (vertical)                 -->
<!-- ============================================ -->
<section>
    <!-- Sub 1 -->
    <section style="background: linear-gradient(135deg, #0d2818, #1a3a2a);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
                <span style="font-size: 2em;">✅</span>
                <h2 style="margin: 0; color: #4ade80; font-size: 1.8em;">Ventajas</h2>
            </div>
            <div class="grid-2">
                <div class="card card-green">
                    <strong style="color: #4ade80;">📚 Curva suave</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Ideal para equipos con SQL.</p>
                </div>
                <div class="card card-green">
                    <strong style="color: #4ade80;">📈 Escalabilidad</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Procesa petabytes de datos.</p>
                </div>
            </div>
            <p style="margin-top: 15px; text-align: center; color: #666; font-size: 0.75em;">⬇️ Más ventajas</p>
        </div>
    </section>

    <!-- Sub 2 -->
    <section style="background: linear-gradient(135deg, #0d2818, #1a3a2a);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
                <span style="font-size: 2em;">✅</span>
                <h2 style="margin: 0; color: #4ade80; font-size: 1.8em;">Ventajas (2)</h2>
            </div>
            <div class="grid-2">
                <div class="card card-green">
                    <strong style="color: #4ade80;">🔗 Ecosistema maduro</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Integración con Tableau, PowerBI, Spark.</p>
                </div>
                <div class="card card-green">
                    <strong style="color: #4ade80;">💾 Almacenamiento eficiente</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Formatos ORC/Parquet reducen espacio y mejoran velocidad.</p>
                </div>
            </div>
            <p style="margin-top: 15px; text-align: center; color: #666; font-size: 0.75em;">⬆️ Volver</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 5: DESVENTAJAS (vertical)              -->
<!-- ============================================ -->
<section>
    <!-- Sub 1 -->
    <section style="background: linear-gradient(135deg, #1a0a0a, #2a1515);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
                <span style="font-size: 2em;">⚠️</span>
                <h2 style="margin: 0; color: #f87171; font-size: 1.8em;">Desventajas</h2>
            </div>
            <div class="grid-2">
                <div class="card card-red">
                    <strong style="color: #f87171;">⏱️ Alta latencia</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">No para consultas en tiempo real (OLTP).</p>
                </div>
                <div class="card card-red">
                    <strong style="color: #f87171;">🔄 Actualizaciones complejas</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">UPDATE/DELETE no son su punto fuerte.</p>
                </div>
            </div>
            <p style="margin-top: 15px; text-align: center; color: #666; font-size: 0.75em;">⬇️ Más</p>
        </div>
    </section>

    <!-- Sub 2 -->
    <section style="background: linear-gradient(135deg, #1a0a0a, #2a1515);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
                <span style="font-size: 2em;">⚠️</span>
                <h2 style="margin: 0; color: #f87171; font-size: 1.8em;">Desventajas (2)</h2>
            </div>
            <div class="card card-red" style="max-width: 70%; margin: 0 auto;">
                <strong style="color: #f87171;">🔧 Requiere tuning</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.85em; color: #bbb;">Optimización de particiones, formatos y parámetros.</p>
            </div>
            <p style="margin-top: 15px; text-align: center; color: #666; font-size: 0.75em;">⬆️ Volver</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 6: USO LABORAL (vertical)             -->
<!-- ============================================ -->
<section>
    <!-- Sub 1 -->
    <section style="background: linear-gradient(135deg, #0f1a2e, #1a2a45);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
                <span style="font-size: 2em;">💼</span>
                <h2 style="margin: 0; color: #60a5fa; font-size: 1.8em;">Uso laboral</h2>
            </div>
            <p style="font-size: 0.8em; color: #aaa; margin-bottom: 10px;">Usado por CNET, Digg, Last.fm, TaoBao:</p>
            <div class="grid-2">
                <div class="card card-blue">
                    <strong style="color: #60a5fa;">🔍 Minería de logs</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Análisis de comportamiento y errores.</p>
                </div>
                <div class="card card-blue">
                    <strong style="color: #60a5fa;">📊 Data Warehousing</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Informes y dashboards históricos.</p>
                </div>
            </div>
            <p style="margin-top: 15px; text-align: center; color: #666; font-size: 0.75em;">⬇️ Más usos</p>
        </div>
    </section>

    <!-- Sub 2 -->
    <section style="background: linear-gradient(135deg, #0f1a2e, #1a2a45);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
                <span style="font-size: 2em;">💼</span>
                <h2 style="margin: 0; color: #60a5fa; font-size: 1.8em;">Uso laboral (2)</h2>
            </div>
            <div class="grid-2">
                <div class="card card-blue">
                    <strong style="color: #60a5fa;">⚙️ ETL</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Limpieza y transformación de datos.</p>
                </div>
                <div class="card card-blue">
                    <strong style="color: #60a5fa;">🤖 Preparación para ML</strong>
                    <p style="margin: 2px 0 0 0; font-size: 0.75em; color: #bbb;">Transformación para modelos con Spark.</p>
                </div>
            </div>
            <p style="margin-top: 15px; text-align: center; color: #666; font-size: 0.75em;">⬆️ Volver</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 7: EFICACIA                           -->
<!-- ============================================ -->
<section style="background: linear-gradient(135deg, #0d1117, #161b22);">
    <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
        <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 12px;">
            <span style="font-size: 2em;">📈</span>
            <h2 style="margin: 0; color: #f7971e; font-size: 1.8em;">¿Es eficaz?</h2>
        </div>
        <p style="font-size: 0.85em; color: #ccc; margin-bottom: 12px;">Sí, con optimizaciones:</p>
        <div class="grid-2">
            <div style="background: rgba(247, 151, 30, 0.08); padding: 15px; border-radius: 10px; border: 1px solid rgba(247, 151, 30, 0.15); text-align: center;">
                <span style="font-size: 2em; display: block;">📉</span>
                <strong style="color: #ffd200; font-size: 1em;">-90% espacio</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.7em; color: #bbb;">Con ORC/Parquet</p>
            </div>
            <div style="background: rgba(247, 151, 30, 0.08); padding: 15px; border-radius: 10px; border: 1px solid rgba(247, 151, 30, 0.15); text-align: center;">
                <span style="font-size: 2em; display: block;">🚀</span>
                <strong style="color: #ffd200; font-size: 1em;">3-4x más rápido</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.7em; color: #bbb;">Velocidad de consultas</p>
            </div>
            <div style="background: rgba(247, 151, 30, 0.08); padding: 15px; border-radius: 10px; border: 1px solid rgba(247, 151, 30, 0.15); text-align: center; grid-column: span 2;">
                <span style="font-size: 2em; display: block;">🧠</span>
                <strong style="color: #ffd200; font-size: 1em;">-40% tiempo</strong>
                <p style="margin: 2px 0 0 0; font-size: 0.7em; color: #bbb;">Optimizador de costes (CBO)</p>
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 8: PRÁCTICA (vertical con imágenes)   -->
<!-- ============================================ -->
<section>
    <!-- Sub 1: Imagen principal -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 10px;">
                <span style="font-size: 1.8em;">🛠️</span>
                <h2 style="margin: 0; color: #f7971e; font-size: 1.6em;">Práctica: Configuración</h2>
            </div>
            <div style="background: rgba(255,255,255,0.02); border-radius: 10px; padding: 10px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica1.png" 
                     alt="Configuración de Hive" 
                     style="max-height: 280px; width: auto; display: block; margin: 0 auto; border-radius: 6px;">
            </div>
            <p style="margin-top: 10px; font-size: 0.8em; color: #ccc; text-align: center;">
                <strong style="color: #ffd200;">Configuración inicial:</strong> Metastore y rutas de almacenamiento.
            </p>
            <p style="margin-top: 10px; text-align: center; color: #666; font-size: 0.7em;">⬇️ Siguiente paso</p>
        </div>
    </section>

    <!-- Sub 2: Metastore -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 10px;">
                <span style="font-size: 1.6em;">📁</span>
                <h2 style="margin: 0; color: #60a5fa; font-size: 1.5em;">Metastore</h2>
            </div>
            <div style="background: rgba(255,255,255,0.02); border-radius: 10px; padding: 10px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica2.png" 
                     alt="Metastore en Hive" 
                     style="max-height: 250px; width: auto; display: block; margin: 0 auto; border-radius: 6px;">
            </div>
            <ul style="margin-top: 10px; font-size: 0.8em; color: #ccc;">
                <li><strong style="color: #60a5fa;">Función:</strong> Almacena metadatos (esquemas, particiones).</li>
                <li><strong style="color: #60a5fa;">DB:</strong> MySQL, PostgreSQL o Derby.</li>
            </ul>
            <p style="margin-top: 10px; text-align: center; color: #666; font-size: 0.7em;">⬇️ Continuar</p>
        </div>
    </section>

    <!-- Sub 3: Optimizador -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 10px;">
                <span style="font-size: 1.6em;">🧠</span>
                <h2 style="margin: 0; color: #4ade80; font-size: 1.5em;">Optimizador (CBO)</h2>
            </div>
            <div style="background: rgba(255,255,255,0.02); border-radius: 10px; padding: 10px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica3.png" 
                     alt="Optimizador de costes" 
                     style="max-height: 250px; width: auto; display: block; margin: 0 auto; border-radius: 6px;">
            </div>
            <ul style="margin-top: 10px; font-size: 0.8em; color: #ccc;">
                <li><strong style="color: #4ade80;">Función:</strong> Elige el plan de ejecución más eficiente.</li>
                <li><strong style="color: #4ade80;">Beneficio:</strong> Reduce tiempo hasta <strong style="color: #ffd200;">40%</strong>.</li>
            </ul>
            <p style="margin-top: 10px; text-align: center; color: #666; font-size: 0.7em;">⬇️ Continuar</p>
        </div>
    </section>

    <!-- Sub 4: Motores -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 20px;">
            <div style="display: flex; align-items: center; gap: 12px; margin-bottom: 10px;">
                <span style="font-size: 1.6em;">⚡</span>
                <h2 style="margin: 0; color: #f7971e; font-size: 1.5em;">Motores de ejecución</h2>
            </div>
            <div style="background: rgba(255,255,255,0.02); border-radius: 10px; padding: 10px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica4.png" 
                     alt="Motores de ejecución" 
                     style="max-height: 250px; width: auto; display: block; margin: 0 auto; border-radius: 6px;">
            </div>
            <ul style="margin-top: 10px; font-size: 0.8em; color: #ccc;">
                <li><strong style="color: #f7971e;">MapReduce:</strong> Estable pero más lento.</li>
                <li><strong style="color: #f7971e;">Tez:</strong> Menor sobrecarga de E/S.</li>
                <li><strong style="color: #f7971e;">Spark:</strong> Mejor para consultas interactivas.</li>
            </ul>
            <p style="margin-top: 10px; text-align: center; color: #666; font-size: 0.7em;">⬆️ Volver al inicio</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 9: CIERRE                             -->
<!-- ============================================ -->
<section style="text-align: center; background: linear-gradient(135deg, #1a1a2e, #0f3460);">
    <div style="display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100%;">
        <span style="font-size: 3.5em; display: block; margin-bottom: 10px;">🐝</span>
        <h2 style="font-size: 2.5em; margin: 0; background: linear-gradient(to right, #f7971e, #ffd200); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">¡Gracias!</h2>
        <p style="font-size: 1.2em; color: #ccc; margin: 8px 0;">Big Data al alcance de todos</p>
        <div style="width: 50px; height: 3px; background: linear-gradient(to right, #f7971e, #ffd200); margin: 10px auto;"></div>
        <p style="font-size: 0.8em; color: #666; margin-top: 20px;">¿Preguntas?</p>
    </div>
</section>
