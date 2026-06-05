---
title: Virtualización en TIC
layout: slide
---

# Solución estratificada de problemas en TIC

## 1.1.a Virtualización por interpretación pura

**Descripción:** El software emula completamente el hardware del sistema invitado.

**Características:**
- Emulación completa de CPU, memoria y periféricos
- Aislamiento total del hardware anfitrión
- Rendimiento más bajo

**Casos de uso:**
- Emulación de sistemas antiguos
- Depuración y análisis de malware

**Ejemplos:** QEMU, Bochs

---

## 1.1.b Virtualización por recompilación dinámica

**Descripción:** Traduce bloques de código a código nativo en tiempo real.

**Características:**
- Traducción de bloques básicos
- Caché de código traducido
- Rendimiento medio

**Casos de uso:**
- Máquinas virtuales JVM/.NET
- Emulación de arquitecturas diferentes

**Ejemplos:** VirtualBox, DynamoRIO, QEMU

---

## 1.1.c Virtualización por hipervisión (bare metal)

**Descripción:** Hipervisor Tipo 1 que se ejecuta directamente sobre el hardware.

**Características:**
- Acceso directo al hardware
- Mínima sobrecarga
- Máximo rendimiento y seguridad

**Casos de uso:**
- Centros de datos y servidores
- Infraestructura en la nube (IaaS)

**Ejemplos:** VMware ESXi, Hyper-V, KVM

---

## 📊 Comparativa rápida

| Método | Rendimiento | Aislamiento |
|--------|-------------|-------------|
| Interpretación pura | Bajo | Alto |
| Recompilación dinámica | Medio | Medio |
| Hipervisión bare metal | Alto | Muy alto |
