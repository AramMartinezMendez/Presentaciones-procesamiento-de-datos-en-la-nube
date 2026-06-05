---
title: Pizza as a Service 2.0
layout: slide
---

<section>
    <h1>🍕 Pizza as a Service 2.0</h1>
    <p><em>Una analogía para entender los modelos de servicio en la nube</em></p>
    <p><small>Basado en el concepto de Albert Barron y Paul Kerrison[citation:1]</small></p>
</section>

<section>
    <h2>📖 ¿Qué es "Pizza as a Service"?</h2>
    <p>Es una <strong>analogía didáctica</strong> que compara los diferentes modelos de despliegue en la nube (IaaS, PaaS, SaaS, etc.) con las distintas formas de preparar y consumir pizza.</p>
    <p>El objetivo es entender fácilmente el <strong>nivel de responsabilidad</strong> que asume el proveedor cloud y cuánto debe gestionar el usuario.</p>
</section>

<section>
    <h2>🏠 Opción 1: Hacer pizza en casa (On-Premise)</h2>
    <p><strong>Descripción:</strong> Compras todos los ingredientes, preparas la masa, horneas y sirves.</p>
    <p><strong>Ventajas:</strong> Control total sobre cada componente.</p>
    <p><strong>Desventajas:</strong> Debes gestionar absolutamente todo.</p>
    <p><strong>Analogía cloud:</strong> Infraestructura local tradicional. Tú administras el edificio, servidores, redes, SO y aplicaciones[citation:4].</p>
</section>

<section>
    <h2>📦 Opción 2: Pizza congelada (IaaS)</h2>
    <p><strong>Descripción:</strong> Compras la pizza ya hecha, solo la calientas en tu horno.</p>
    <p><strong>Ventajas:</strong> No hiciste la masa ni picaste los ingredientes.</p>
    <p><strong>Desventajas:</strong> Aún necesitas el horno (servidores) y la electricidad (redes).</p>
    <p><strong>Analogía cloud:</strong> Infrastructure as a Service. El proveedor da la infraestructura (servidores, almacenamiento). Tú instalas el SO y las apps[citation:5].</p>
    <p><strong>Ejemplos AWS:</strong> EC2 (máquinas virtuales), S3 (almacenamiento)[citation:5].</p>
</section>

<section>
    <h2>🚚 Opción 3: Pizza Delivery (PaaS)</h2>
    <p><strong>Descripción:</strong> Pides la pizza por teléfono y te llega a casa lista para comer.</p>
    <p><strong>Ventajas:</strong> No necesitas horno ni utensilios. Llega caliente.</p>
    <p><strong>Desventajas:</strong> No eliges la marca del queso o la harina.</p>
    <p><strong>Analogía cloud:</strong> Platform as a Service. El proveedor gestiona todo (hardware, SO, runtime). Tú solo despliegas tu aplicación[citation:6].</p>
    <p><strong>Ejemplos:</strong> AWS Elastic Beanstalk, Google App Engine[citation:5].</p>
</section>

<section>
    <h2>🍽️ Opción 4: Jantar fuera (SaaS)</h2>
    <p><strong>Descripción:</strong> Vas al restaurante, comes la pizza preparada por chefs y solo pagas la cuenta.</p>
    <p><strong>Ventajas:</strong> Experiencia completa sin ninguna preocupación.</p>
    <p><strong>Desventajas:</strong> Cero control sobre la receta o preparación.</p>
    <p><strong>Analogía cloud:</strong> Software as a Service. Usas el software listo y funcionando[citation:4].</p>
    <p><strong>Ejemplos:</strong> Gmail, Netflix, Salesforce, Office 365[citation:6].</p>
</section>

<section>
    <h2>⚙️ Novedades del modelo 2.0</h2>
    <p>Paul Kerrison amplió el concepto agregando:</p>
    <ul>
        <li><strong>CaaS (Containers as a Service):</strong> Como tener una "pizzeria virtual" con contenedores listos para desplegar[citation:1].</li>
        <li><strong>FaaS (Functions as a Service):</strong> Serverless. Solo pagas por cada "porción de pizza" que consumes[citation:1].</li>
    </ul>
</section>

<section>
    <h2>📊 Tabla comparativa de modelos</h2>
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
    <h2>✅ Resumen final</h2>
    <p>La analogía <strong>Pizza as a Service 2.0</strong> muestra cómo los servicios cloud permiten delegar responsabilidades:</p>
    <ul>
        <li><strong>Más control</strong> = más trabajo operativo (On-Premise/IaaS)</li>
        <li><strong>Menos control</strong> = más enfoque en el negocio (PaaS/SaaS)</li>
    </ul>
    <p>El modelo adecuado depende del balance que necesites entre <strong>flexibilidad</strong> y <strong>comodidad</strong>.</p>
</section>
