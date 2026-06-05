---
layout: reveal
title: Virtualización en TIC
---



<section data-markdown>
  <textarea data-template>

    # Solución estratificada de problemas en TIC

    *Una visión general*

    ---

    ## 1.1.a Virtualización por interpretación pura

    **Descripción:** El software emula completamente el hardware.

    ### Características:
    - Emulación completa de CPU, memoria y periféricos
    - Aislamiento total del hardware anfitrión
    - Rendimiento más bajo

    **Ejemplos:** QEMU, Bochs

    ---

    ## 1.1.b Virtualización por recompilación dinámica

    **Descripción:** Traduce bloques de código a código nativo en tiempo real.

    ### Características:
    - Traducción de bloques básicos
    - Caché de código traducido
    - Rendimiento medio

    **Ejemplos:** VirtualBox, DynamoRIO, QEMU

    ---

    ## 1.1.c Virtualización por hipervisión (bare metal)

    **Descripción:** Hipervisor Tipo 1 que se ejecuta directamente sobre el hardware.

    ### Características:
    - Acceso directo al hardware
    - Mínima sobrecarga
    - Máximo rendimiento y seguridad

    **Ejemplos:** VMware ESXi, Hyper-V, KVM

  </textarea>
</section>
