---
title: Virtualización en TIC
layout: slide
---

<section>
    <h1>Solución estratificada de problemas en TIC</h1>
    <p><em>Una visión general</em></p>
</section>

<section>
    <h2>1.1.a Virtualización por interpretación pura</h2>
    <p><strong>Descripción:</strong> El software emula completamente el hardware.</p>
    <h3>Características:</h3>
    <ul>
        <li>Emulación completa de CPU, memoria y periféricos</li>
        <li>Aislamiento total del hardware anfitrión</li>
        <li>Rendimiento más bajo</li>
    </ul>
    <p><strong>Ejemplos:</strong> QEMU, Bochs</p>
</section>

<section>
    <h2>1.1.b Virtualización por recompilación dinámica</h2>
    <p><strong>Descripción:</strong> Traduce bloques de código a código nativo en tiempo real.</p>
    <h3>Características:</h3>
    <ul>
        <li>Traducción de bloques básicos</li>
        <li>Caché de código traducido</li>
        <li>Rendimiento medio</li>
    </ul>
    <p><strong>Ejemplos:</strong> VirtualBox, DynamoRIO, QEMU</p>
</section>

<section>
    <h2>1.1.c Virtualización por hipervisión (bare metal)</h2>
    <p><strong>Descripción:</strong> Hipervisor Tipo 1 que se ejecuta directamente sobre el hardware.</p>
    <h3>Características:</h3>
    <ul>
        <li>Acceso directo al hardware</li>
        <li>Mínima sobrecarga</li>
        <li>Máximo rendimiento y seguridad</li>
    </ul>
    <p><strong>Ejemplos:</strong> VMware ESXi, Hyper-V, KVM</p>
</section>

<section>
    <h2>📊 Comparativa</h2>
    <table>
        <tr><th>Método</th><th>Rendimiento</th><th>Aislamiento</th></tr>
        <tr><td>Interpretación pura</td><td>Bajo</td><td>Alto</td></tr>
        <tr><td>Recompilación dinámica</td><td>Medio</td><td>Medio</td></tr>
        <tr><td>Hipervisión bare metal</td><td>Alto</td><td>Muy alto</td></tr>
    </table>
</section>
