---
title: Apache Hive
layout: slide
---

<!-- ajustar tamaños de slides -->

<style>
  .reveal .slides section {
    max-height: 90vh !important;
    overflow: hidden !important;
  }
  .reveal .slides section > * {
    max-height: 85vh;
    overflow-y: auto;
  }
  .reveal ul, .reveal p {
    font-size: 0.9em !important;
    line-height: 1.4 !important;
  }
  .reveal li {
    margin-bottom: 8px !important;
  }
</style>






<!-- ============================================ -->
<!-- SLIDE 1: PORTADA                             -->
<!-- ============================================ -->
<section style="text-align: center; background: linear-gradient(135deg, #1a1a2e, #16213e, #0f3460);">
    <div style="display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100%;">
        <span style="font-size: 4em; display: block; margin-bottom: 20px;">🐝</span>
        <h1 style="font-size: 3.5em; background: linear-gradient(to right, #f7971e, #ffd200); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; margin: 0;">Apache Hive</h1>
        <p style="font-size: 1.8em; color: #e0e0e0; margin: 10px 0 5px 0;"><em>El puente entre SQL y el Big Data</em></p>
        <div style="width: 80px; height: 4px; background: linear-gradient(to right, #f7971e, #ffd200); margin: 15px auto;"></div>
        <p style="font-size: 1.2em; color: #aaa; letter-spacing: 2px;">⚡ Data Warehouse para Hadoop</p>
        <p style="font-size: 0.8em; color: #666; margin-top: 40px;">Presiona → para comenzar</p>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 2: ¿QUÉ ES?                           -->
<!-- ============================================ -->
<section style="background: linear-gradient(135deg, #0d1117, #161b22);">
    <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
        <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 25px;">
            <span style="font-size: 2.5em;">📖</span>
            <h2 style="margin: 0; color: #f7971e; font-size: 2.2em;">¿Qué es Apache Hive?</h2>
        </div>
        <div style="background: rgba(255,255,255,0.03); border-left: 4px solid #f7971e; padding: 25px 30px; border-radius: 8px;">
            <p style="font-size: 1.2em; line-height: 1.6; color: #e6e6e6;">
                Es un <strong style="color: #ffd200;">sistema de almacenamiento de datos (Data Warehouse)</strong> construido sobre Apache Hadoop.
            </p>
            <p style="font-size: 1.1em; line-height: 1.6; color: #ccc; margin-top: 15px;">
                Su propósito es permitir que analistas y desarrolladores realicen consultas sobre grandes conjuntos de datos en HDFS usando un lenguaje similar a SQL, llamado <strong style="color: #f7971e;">HiveQL</strong>.
            </p>
        </div>
        <div style="display: flex; gap: 30px; margin-top: 25px; justify-content: center;">
            <div style="text-align: center; background: rgba(247, 151, 30, 0.1); padding: 15px 25px; border-radius: 10px; border: 1px solid rgba(247, 151, 30, 0.2);">
                <span style="font-size: 1.8em; display: block;">📊</span>
                <span style="color: #aaa; font-size: 0.85em;">Petabytes de datos</span>
            </div>
            <div style="text-align: center; background: rgba(247, 151, 30, 0.1); padding: 15px 25px; border-radius: 10px; border: 1px solid rgba(247, 151, 30, 0.2);">
                <span style="font-size: 1.8em; display: block;">🔄</span>
                <span style="color: #aaa; font-size: 0.85em;">SQL → MapReduce/Spark</span>
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 3: CARACTERÍSTICAS                     -->
<!-- ============================================ -->
<section style="background: linear-gradient(135deg, #0d1117, #161b22);">
    <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
        <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 25px;">
            <span style="font-size: 2.5em;">⚙️</span>
            <h2 style="margin: 0; color: #f7971e; font-size: 2.2em;">Características principales</h2>
        </div>
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
            <div style="background: rgba(255,255,255,0.03); padding: 18px 20px; border-radius: 10px; border-left: 3px solid #f7971e;">
                <strong style="color: #ffd200;">🗄️ Interfaz SQL familiar</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Baja barrera de entrada para quienes ya conocen SQL.</p>
            </div>
            <div style="background: rgba(255,255,255,0.03); padding: 18px 20px; border-radius: 10px; border-left: 3px solid #f7971e;">
                <strong style="color: #ffd200;">☁️ Almacenamiento flexible</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Funciona sobre HDFS, Amazon S3 y otros sistemas.</p>
            </div>
            <div style="background: rgba(255,255,255,0.03); padding: 18px 20px; border-radius: 10px; border-left: 3px solid #f7971e;">
                <strong style="color: #ffd200;">🧩 Extensible</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Soporta funciones personalizadas (UDF) en Java o Python.</p>
            </div>
            <div style="background: rgba(255,255,255,0.03); padding: 18px 20px; border-radius: 10px; border-left: 3px solid #f7971e;">
                <strong style="color: #ffd200;">📁 Metastore centralizado</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Metadatos en base de datos externa (MySQL, PostgreSQL).</p>
            </div>
            <div style="background: rgba(255,255,255,0.03); padding: 18px 20px; border-radius: 10px; border-left: 3px solid #f7971e; grid-column: span 2;">
                <strong style="color: #ffd200;">🚀 Optimización de costes (CBO)</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Mejora el rendimiento de consultas complejas mediante un optimizador basado en costes.</p>
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 4: VENTAJAS (vertical)                 -->
<!-- ============================================ -->
<section>
    <section style="background: linear-gradient(135deg, #0d2818, #1a3a2a);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 20px;">
                <span style="font-size: 2.5em;">✅</span>
                <h2 style="margin: 0; color: #4ade80; font-size: 2.2em;">Ventajas</h2>
            </div>
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                <div style="background: rgba(74, 222, 128, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(74, 222, 128, 0.15);">
                    <strong style="color: #4ade80;">📚 Curva de aprendizaje suave</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Ideal para equipos con experiencia en SQL.</p>
                </div>
                <div style="background: rgba(74, 222, 128, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(74, 222, 128, 0.15);">
                    <strong style="color: #4ade80;">📈 Escalabilidad masiva</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Capacidad para procesar petabytes de datos.</p>
                </div>
            </div>
            <p style="margin-top: 30px; text-align: center; color: #666; font-size: 0.85em;">⬇️ Presiona la flecha hacia abajo para más ventajas</p>
        </div>
    </section>

    <section style="background: linear-gradient(135deg, #0d2818, #1a3a2a);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 20px;">
                <span style="font-size: 2.5em;">✅</span>
                <h2 style="margin: 0; color: #4ade80; font-size: 2.2em;">Ventajas (continuación)</h2>
            </div>
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                <div style="background: rgba(74, 222, 128, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(74, 222, 128, 0.15);">
                    <strong style="color: #4ade80;">🔗 Ecosistema maduro</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Integración con BI (Tableau, PowerBI) y ML (Spark).</p>
                </div>
                <div style="background: rgba(74, 222, 128, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(74, 222, 128, 0.15);">
                    <strong style="color: #4ade80;">💾 Eficiencia en almacenamiento</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Formatos columnar (ORC/Parquet) reducen espacio y mejoran velocidad.</p>
                </div>
            </div>
            <p style="margin-top: 30px; text-align: center; color: #666; font-size: 0.85em;">⬆️ Presiona la flecha hacia arriba para volver</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 5: DESVENTAJAS (vertical)              -->
<!-- ============================================ -->
<section>
    <section style="background: linear-gradient(135deg, #1a0a0a, #2a1515);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 20px;">
                <span style="font-size: 2.5em;">⚠️</span>
                <h2 style="margin: 0; color: #f87171; font-size: 2.2em;">Desventajas y limitaciones</h2>
            </div>
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                <div style="background: rgba(248, 113, 113, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(248, 113, 113, 0.15);">
                    <strong style="color: #f87171;">⏱️ Alta latencia</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">No diseñado para consultas en tiempo real (OLTP).</p>
                </div>
                <div style="background: rgba(248, 113, 113, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(248, 113, 113, 0.15);">
                    <strong style="color: #f87171;">🔄 Actualizaciones complejas</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Las operaciones de actualización y borrado no son su punto fuerte.</p>
                </div>
            </div>
            <p style="margin-top: 30px; text-align: center; color: #666; font-size: 0.85em;">⬇️ Presiona la flecha hacia abajo para más</p>
        </div>
    </section>

    <section style="background: linear-gradient(135deg, #1a0a0a, #2a1515);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 20px;">
                <span style="font-size: 2.5em;">⚠️</span>
                <h2 style="margin: 0; color: #f87171; font-size: 2.2em;">Desventajas (continuación)</h2>
            </div>
            <div style="background: rgba(248, 113, 113, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(248, 113, 113, 0.15); max-width: 70%; margin: 0 auto;">
                <strong style="color: #f87171;">🔧 Requiere configuración y tuning</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.95em; color: #bbb;">Para obtener buen rendimiento, se debe optimizar particiones, formatos de archivo y parámetros de ejecución.</p>
            </div>
            <p style="margin-top: 30px; text-align: center; color: #666; font-size: 0.85em;">⬆️ Presiona la flecha hacia arriba para volver</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 6: USO LABORAL (vertical)             -->
<!-- ============================================ -->
<section>
    <section style="background: linear-gradient(135deg, #0f1a2e, #1a2a45);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 20px;">
                <span style="font-size: 2.5em;">💼</span>
                <h2 style="margin: 0; color: #60a5fa; font-size: 2.2em;">Uso laboral</h2>
            </div>
            <p style="font-size: 1em; color: #aaa; margin-bottom: 15px;">Empresas como CNET, Digg, Last.fm y TaoBao lo utilizan para:</p>
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                <div style="background: rgba(96, 165, 250, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(96, 165, 250, 0.15);">
                    <strong style="color: #60a5fa;">🔍 Minería y análisis de logs</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Comportamiento de usuario, errores y auditorías.</p>
                </div>
                <div style="background: rgba(96, 165, 250, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(96, 165, 250, 0.15);">
                    <strong style="color: #60a5fa;">📊 Data Warehousing</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Almacenamiento histórico para informes y dashboards.</p>
                </div>
            </div>
            <p style="margin-top: 30px; text-align: center; color: #666; font-size: 0.85em;">⬇️ Presiona la flecha hacia abajo para más usos</p>
        </div>
    </section>

    <section style="background: linear-gradient(135deg, #0f1a2e, #1a2a45);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 20px;">
                <span style="font-size: 2.5em;">💼</span>
                <h2 style="margin: 0; color: #60a5fa; font-size: 2.2em;">Uso laboral (continuación)</h2>
            </div>
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px;">
                <div style="background: rgba(96, 165, 250, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(96, 165, 250, 0.15);">
                    <strong style="color: #60a5fa;">⚙️ ETL</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Limpieza, transformación y enriquecimiento de datos.</p>
                </div>
                <div style="background: rgba(96, 165, 250, 0.05); padding: 18px 20px; border-radius: 10px; border: 1px solid rgba(96, 165, 250, 0.15);">
                    <strong style="color: #60a5fa;">🤖 Preparación para ML</strong>
                    <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Transformación de datasets masivos para entrenar modelos.</p>
                </div>
            </div>
            <p style="margin-top: 30px; text-align: center; color: #666; font-size: 0.85em;">⬆️ Presiona la flecha hacia arriba para volver</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 7: EFICACIA                           -->
<!-- ============================================ -->
<section style="background: linear-gradient(135deg, #0d1117, #161b22);">
    <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
        <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 25px;">
            <span style="font-size: 2.5em;">📈</span>
            <h2 style="margin: 0; color: #f7971e; font-size: 2.2em;">¿Es eficaz?</h2>
        </div>
        <p style="font-size: 1.1em; color: #ccc; margin-bottom: 20px;">Sí, y los datos lo demuestran. Su eficacia se basa en la optimización:</p>
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px;">
            <div style="background: rgba(247, 151, 30, 0.08); padding: 25px 20px; border-radius: 12px; border: 1px solid rgba(247, 151, 30, 0.2); text-align: center;">
                <span style="font-size: 2.5em; display: block;">📉</span>
                <strong style="color: #ffd200; font-size: 1.1em;">-90% de espacio</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Con formatos columnar (ORC/Parquet)</p>
            </div>
            <div style="background: rgba(247, 151, 30, 0.08); padding: 25px 20px; border-radius: 12px; border: 1px solid rgba(247, 151, 30, 0.2); text-align: center;">
                <span style="font-size: 2.5em; display: block;">🚀</span>
                <strong style="color: #ffd200; font-size: 1.1em;">3-4x más rápido</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Velocidad de consultas mejorada</p>
            </div>
            <div style="background: rgba(247, 151, 30, 0.08); padding: 25px 20px; border-radius: 12px; border: 1px solid rgba(247, 151, 30, 0.2); text-align: center; grid-column: span 2;">
                <span style="font-size: 2.5em; display: block;">🧠</span>
                <strong style="color: #ffd200; font-size: 1.1em;">-40% de tiempo</strong>
                <p style="margin: 5px 0 0 0; font-size: 0.9em; color: #bbb;">Optimizador de costes (CBO) en consultas complejas</p>
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!-- SLIDE 8: PRÁCTICA (vertical con imágenes)   -->
<!-- ============================================ -->
<section>
    <!-- Sub-diapositiva 1: Imagen principal -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 20px;">
                <span style="font-size: 2.5em;">🛠️</span>
                <h2 style="margin: 0; color: #f7971e; font-size: 2.2em;">Práctica: Configuración de Hive</h2>
            </div>
            
            <!-- 
            📍 IMAGEN 1: Sustituye "practica1.png" por el nombre real de tu imagen
            -->
            <div style="background: rgba(255,255,255,0.02); border-radius: 12px; padding: 15px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica1.png" 
                     alt="Configuración de Hive" 
                     style="max-width: 80%; height: auto; margin: 0 auto; display: block; border-radius: 8px;">
            </div>
            
            <p style="margin-top: 15px; font-size: 0.95em; color: #ccc; text-align: center;">
                <strong style="color: #ffd200;">Descripción:</strong> Configuración inicial de Hive, definiendo el metastore y las rutas de almacenamiento.
            </p>
            
            <p style="margin-top: 20px; text-align: center; color: #666; font-size: 0.85em;">⬇️ Presiona ↓ para ver el siguiente paso</p>
        </div>
    </section>

    <!-- Sub-diapositiva 2: Metastore -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 15px;">
                <span style="font-size: 2em;">📁</span>
                <h2 style="margin: 0; color: #60a5fa; font-size: 1.8em;">Componente 1: Metastore</h2>
            </div>
            
            <!-- 
            📍 IMAGEN 2: Sustituye "practica2.png" por el nombre real de tu imagen
            -->
            <div style="background: rgba(255,255,255,0.02); border-radius: 12px; padding: 15px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica2.png" 
                     alt="Metastore en Hive" 
                     style="max-width: 80%; height: auto; margin: 0 auto; display: block; border-radius: 8px;">
            </div>
            
            <ul style="margin-top: 15px; font-size: 0.95em; color: #ccc;">
                <li><strong style="color: #60a5fa;">Función:</strong> Almacena metadatos de tablas (esquemas, particiones, ubicación en HDFS).</li>
                <li><strong style="color: #60a5fa;">Base de datos:</strong> Usa MySQL, PostgreSQL o Derby para persistencia.</li>
            </ul>
            
            <p style="margin-top: 20px; text-align: center; color: #666; font-size: 0.85em;">⬇️ Presiona ↓ para continuar</p>
        </div>
    </section>

    <!-- Sub-diapositiva 3: Optimizador -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 15px;">
                <span style="font-size: 2em;">🧠</span>
                <h2 style="margin: 0; color: #4ade80; font-size: 1.8em;">Componente 2: Optimizador (CBO)</h2>
            </div>
            
            <!-- 
            📍 IMAGEN 3: Sustituye "practica3.png" por el nombre real de tu imagen
            -->
            <div style="background: rgba(255,255,255,0.02); border-radius: 12px; padding: 15px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica3.png" 
                     alt="Optimizador de costes Hive" 
                     style="max-width: 80%; height: auto; margin: 0 auto; display: block; border-radius: 8px;">
            </div>
            
            <ul style="margin-top: 15px; font-size: 0.95em; color: #ccc;">
                <li><strong style="color: #4ade80;">Función:</strong> Analiza consultas HiveQL y elige el plan más eficiente.</li>
                <li><strong style="color: #4ade80;">Beneficio:</strong> Reduce tiempo de ejecución hasta un <strong style="color: #ffd200;">40%</strong>.</li>
            </ul>
            
            <p style="margin-top: 20px; text-align: center; color: #666; font-size: 0.85em;">⬇️ Presiona ↓ para continuar</p>
        </div>
    </section>

    <!-- Sub-diapositiva 4: Motores -->
    <section style="background: linear-gradient(135deg, #0d1117, #161b22);">
        <div style="display: flex; flex-direction: column; justify-content: center; height: 100%; max-width: 900px; margin: 0 auto; padding: 0 40px;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 15px;">
                <span style="font-size: 2em;">⚡</span>
                <h2 style="margin: 0; color: #f7971e; font-size: 1.8em;">Componente 3: Motores de ejecución</h2>
            </div>
            
            <!-- 
            📍 IMAGEN 4 (opcional): Sustituye "practica4.png" si tienes una cuarta imagen
            -->
            <div style="background: rgba(255,255,255,0.02); border-radius: 12px; padding: 15px; border: 1px solid rgba(255,255,255,0.05);">
                <img src="{{ site.baseurl }}/images/practica4.png" 
                     alt="Motores de ejecución Hive" 
                     style="max-width: 80%; height: auto; margin: 0 auto; display: block; border-radius: 8px;">
            </div>
            
            <ul style="margin-top: 15px; font-size: 0.95em; color: #ccc;">
                <li><strong style="color: #f7971e;">MapReduce:</strong> Estable pero más lento.</li>
                <li><strong style="color: #f7971e;">Apache Tez:</strong> Reduce sobrecarga de E/S.</li>
                <li><strong style="color: #f7971e;">Apache Spark:</strong> Mejor rendimiento para consultas interactivas.</li>
            </ul>
            
            <p style="margin-top: 20px; text-align: center; color: #666; font-size: 0.85em;">⬆️ Presiona ↑ para volver al inicio de la práctica</p>
        </div>
    </section>
</section>

<!-- ============================================ -->
<!-- SLIDE 9: CIERRE                             -->
<!-- ============================================ -->
<section style="text-align: center; background: linear-gradient(135deg, #1a1a2e, #0f3460);">
    <div style="display: flex; flex-direction: column; justify-content: center; align-items: center; height: 100%;">
        <span style="font-size: 4em; display: block; margin-bottom: 20px;">🐝</span>
        <h2 style="font-size: 2.8em; margin: 0; background: linear-gradient(to right, #f7971e, #ffd200); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text;">¡Gracias!</h2>
        <p style="font-size: 1.5em; color: #ccc; margin: 10px 0;">Apache Hive: Big Data al alcance de todos</p>
        <div style="width: 60px; height: 3px; background: linear-gradient(to right, #f7971e, #ffd200); margin: 15px auto;"></div>
        <p style="font-size: 0.9em; color: #666; margin-top: 30px;">¿Preguntas?</p>
    </div>
</section>
