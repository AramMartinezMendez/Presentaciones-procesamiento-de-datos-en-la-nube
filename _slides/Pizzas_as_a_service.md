---
title: Pizza as a Service 2.0
layout: slide
---

<section>
    <h1> Pizza as a Service 2.0</h1>
    <p><em>Una analogía para entender los modelos de servicio en la nube</em></p>
    <p><small>esta basado en el concepto de Albert Barron y Paul Kerrison]</small></p>
</section>

<section>
    <h2>¿Qué es "Pizza as a Service"?</h2>
    <p>Es una <strong>analogía didáctica</strong> que compara los diferentes modelos de despliegue en la nube (IaaS, PaaS, SaaS, etc.) con las distintas formas de preparar y consumir pizza.</p>
    <p>El objetivo es entender fácilmente el <strong>nivel de responsabilidad</strong> que asume el proveedor cloud y cuánto debe gestionar el usuario.</p>
</section>

<section>
    <h2> Opción 1: Modelo de hacer pizza en casa (On-Premise)</h2>
    <p><strong>Descripción:</strong> Compras todos los ingredientes, preparas la masa, horneas y sirves.</p>
    <p><strong>Ventajas:</strong> Control total sobre cada componente.</p>
    <p><strong>Desventajas:</strong> Debes gestionar absolutamente todo.</p>
    <p><strong>Analogía cloud:</strong> Infraestructura local tradicional. Tú administras el edificio, servidores, redes, SO y aplicaciones.</p>
</section>

<section>
    <h2> Opción 2: Modelo pizza congelada (IaaS)</h2>
    <p><strong>Descripción:</strong> Compras la pizza ya hecha, solo la calientas en tu horno.</p>
    <p><strong>Ventajas:</strong> No hiciste la masa ni picaste los ingredientes.</p>
    <p><strong>Desventajas:</strong> Aún necesitas el horno (servidores) y la electricidad (redes).</p>
    <p><strong>Analogía cloud:</strong> Infrastructure as a Service. El proveedor da la infraestructura (servidores, almacenamiento). Tú instalas el SO y las apps.</p>
    <p><strong>Ejemplos AWS:</strong> EC2 (máquinas virtuales), S3 (almacenamiento).</p>
</section>

<section>
    <h2> Opción 3: modelo pizza Delivery (PaaS)</h2>
    <p><strong>Descripción:</strong> Pides la pizza por teléfono y te llega a casa lista para comer.</p>
    <p><strong>Ventajas:</strong> No necesitas horno ni utensilios. Llega caliente.</p>
    <p><strong>Desventajas:</strong> No eliges la marca del queso o la harina.</p>
    <p><strong>Analogía cloud:</strong> Platform as a Service. El proveedor gestiona todo (hardware, SO, runtime). Tú solo despliegas tu aplicación.</p>
    <p><strong>Ejemplos:</strong> AWS Elastic Beanstalk, Google App Engine.</p>
</section>

<section>
    <h2> Opción 4: Modelo Jantar fuera (SaaS)</h2>
    <p><strong>Descripción:</strong> Vas al restaurante, comes la pizza preparada por chefs y solo pagas la cuenta.</p>
    <p><strong>Ventajas:</strong> Experiencia completa sin ninguna preocupación.</p>
    <p><strong>Desventajas:</strong> Cero control sobre la receta o preparación.</p>
    <p><strong>Analogía cloud:</strong> Software as a Service. Usas el software listo y funcionando.</p>
    <p><strong>Ejemplos:</strong> Gmail, Netflix, Salesforce, Office 365.</p>
</section>

<section>
    <h2> Novedades del modelo 2.0</h2>
    <p>Paul Kerrison amplió el concepto agregando:</p>
    <ul>
        <li><strong>CaaS (Containers as a Service):</strong> Como tener una "pizzeria virtual" con contenedores listos para desplegar.</li>
        <li><strong>FaaS (Functions as a Service):</strong> Serverless. Solo pagas por cada "porción de pizza" que consumes.</li>
    </ul>
</section>

<section>
    <h2> Tabla improvisada comparativa de modelos</h2>
    <table>
        <tr><th>Modelo</th><th>Analogía Pizza</th><th>Responsabilidad del usuario</th></tr>
        <tr><td>On-Premise</td><td>Pizza casera desde cero</td><td>Todo (ingredientes, horneado, servicio)</td></tr>
        <tr><td>IaaS</td><td>Pizza congelada</td><td>Sistema Operativo + Apps</td></tr>
        <tr><td>PaaS</td><td>Delivery</td><td>Solo la aplicación</td></tr>
        <tr><td>SaaS</td><td>Restaurante</td><td>Solo usar el software</td></tr>
        <tr><td>CaaS/FaaS</td><td>Pizza en porciones bajo demanda</td><td>El código o contenedor</td></tr>
    </table>
</section>

<section>
    <h2>conclusiones finales</h2>
    <p>La analogía <strong>Pizza as a Service 2.0</strong> muestra cómo los servicios cloud permiten delegar responsabilidades:</p>
    <ul>
        <li><strong>Más control</strong> = más trabajo operativo (On-Premise/IaaS)</li>
        <li><strong>Menos control</strong> = más enfoque en el negocio (PaaS/SaaS)</li>
    </ul>
    <p>El modelo adecuado depende del balance que necesites entre <strong>flexibilidad</strong> y <strong>comodidad</strong>.</p>
</section>


<section>
    <h2>🗺️ Mapa conceptual: Pizza as a Service 2.0</h2>
    <img src="{{ site.baseurl }}/images/pizza-service.png" alt="Mapa de Pizza as a Service 2.0" style="max-width: 80%; height: auto; margin: 0 auto; display: block;">
    <p><small>Fuente: Paul Kerrison - http://www.paulkerrison.co.uk</small></p>
</section>

<section>
    <h2>📖 Explicación del mapa</h2>
    <p>Este mapa muestra cómo <strong>delegar responsabilidades</strong> cambia según el modelo de servicio:</p>
    
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 20px; text-align: left;">
        <div>
            <h3>🏠 Tradición → On-Premise</h3>
            <p><strong>Tú gestionas TODO:</strong> desde la masa (hardware) hasta el horneado (aplicaciones).</p>
            <p><em>Ejemplo: Servidor físico en tu oficina.</em></p>
        </div>
        <div>
            <h3>📦 IaaS</h3>
            <p><strong>Tú gestionas:</strong> Sistema Operativo y aplicaciones.</p>
            <p><strong>Proveedor gestiona:</strong> Hardware y virtualización.</p>
            <p><em>Ejemplo: AWS EC2, Google Compute Engine.</em></p>
        </div>
        <div>
            <h3>📦 CaaS</h3>
            <p><strong>Tú gestionas:</strong> Contenedores y código.</p>
            <p><strong>Proveedor gestiona:</strong> Infraestructura y orquestación.</p>
            <p><em>Ejemplo: AWS ECS, Google Kubernetes Engine.</em></p>
        </div>
        <div>
            <h3>🚚 PaaS</h3>
            <p><strong>Tú gestionas:</strong> Solo tu aplicación y datos.</p>
            <p><strong>Proveedor gestiona:</strong> Todo lo demás.</p>
            <p><em>Ejemplo: Heroku, Google App Engine.</em></p>
        </div>
        <div>
            <h3>🍽️ FaaS (Serverless)</h3>
            <p><strong>Tú gestionas:</strong> Solo el código de las funciones.</p>
            <p><strong>Proveedor gestiona:</strong> Escalado y ejecución bajo demanda.</p>
            <p><em>Ejemplo: AWS Lambda, Google Cloud Functions.</em></p>
        </div>
        <div>
            <h3>🍕 SaaS</h3>
            <p><strong>Tú gestionas:</strong> Solo usar el software.</p>
            <p><strong>Proveedor gestiona:</strong> Todo (infraestructura, datos, seguridad).</p>
            <p><em>Ejemplo: Gmail, Netflix, Office 365.</em></p>
        </div>
    </div>
</section>

<section>
    <h2>🎯 Conclusión del mapa</h2>
    <p>La línea vertical en el mapa separa:</p>
    <ul>
        <li><strong>🔵 Lado izquierdo (Tú gestionas):</strong> Mayor control, mayor responsabilidad.</li>
        <li><strong>🔴 Lado derecho (Proveedor gestiona):</strong> Menos control, menos trabajo operativo.</li>
    </ul>
    <p>💡 <strong>Elección estratégica:</strong> El modelo correcto depende de tu negocio. Si tu ventaja es el software, usa PaaS/FaaS. Si necesitas control total del hardware, usa IaaS u On-Premise.</p>
</section>
