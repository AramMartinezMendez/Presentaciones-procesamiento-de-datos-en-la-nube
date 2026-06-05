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

<!-- explicacion del esquema -->

<!-- DIApositiva PADRE (contiene el mapa y la explicación como slides verticales) -->
<section>
    <!-- DIApositiva VERTICAL 1: El mapa -->
    <section>
        <h2>🗺️ Mapa conceptual: Pizza as a Service 2.0</h2>
        <img src="{{ site.baseurl }}/images/pizza-service" alt="Mapa" style="max-width: 70%; margin: 0 auto; display: block;">
        <p><small>Fuente: Paul Kerrison</small></p>
    </section>
    
    <!-- DIApositiva VERTICAL 2: La explicación (se accede con ↓) -->
    <section>
        <h3>📖 Explicación del mapa</h3>
        <p>Este mapa muestra cómo <strong>delegar responsabilidades</strong> cambia según el modelo de servicio.</p>
        
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; text-align: left; font-size: 0.7em;">
            <div><h4> On-Premise</h4><p>Tú gestionas TODO</p></div>
            <div><h4> IaaS</h4><p>Tú: SO y apps | Proveedor: Hardware</p></div>
            <div><h4> CaaS</h4><p>Tú: Contenedores | Proveedor: Infraestructura</p></div>
            <div><h4>PaaS</h4><p>Tú: Solo tu app | Proveedor: Lo demás</p></div>
            <div><h4> FaaS</h4><p>Tú: Solo funciones | Proveedor: Escalado</p></div>
            <div><h4> SaaS</h4><p>Tú: Solo usar | Proveedor: Todo</p></div>
        </div>
        
        <p style="margin-top: 20px; font-style: italic;">💡 La línea vertical separa responsabilidades</p>
    </section>
</section>

<section>
    <h2> Conclusión del mapa</h2>
    <p>La línea vertical en el mapa separa:</p>
    <ul>
        <li><strong>🔵 Lado izquierdo (Tú gestionas):</strong> Mayor control, mayor responsabilidad.</li>
        <li><strong>🔴 Lado derecho (Proveedor gestiona):</strong> Menos control, menos trabajo operativo.</li>
    </ul>
    <p> <strong>Elección estratégica:</strong> El modelo correcto depende de tu negocio. Si tu ventaja es el software, usa PaaS/FaaS. Si necesitas control total del hardware, usa IaaS u On-Premise.</p>
</section>
