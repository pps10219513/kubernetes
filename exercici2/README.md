# 📡 Práctica 5.3: Prometheus y Grafana

Este repositorio contiene los **dos ejercicios** correspondientes a la práctica **RA5.3 - Sistema de monitorización**, dentro del módulo de *Ciberseguridad en entornos de las tecnologías de la información*. El objetivo es implementar y validar un sistema de monitorización utilizando las herramientas **Prometheus**, **Grafana**, **Node Exporter** y **cAdvisor**.

---

## 📁 Ejercicio 1 - Validación del Stack

✅ En este primer ejercicio se ha desplegado correctamente el stack de monitorización. Las evidencias incluyen:

- 📦 **Prometheus** recolectando métricas del sistema
- 🖥️ **Node Exporter** instalado en el servidor
- 📊 **Grafana** configurado en el cliente con dashboards funcionales
- 🧮 **cAdvisor** monitorizando contenedores
- 🔍 Visualización de métricas en tiempo real

📸 Capturas de pantalla:
- `cad.png` ➝ Interfaz de cAdvisor
- `graphana.png` ➝ Dashboard de Grafana
- `logs.png` ➝ Logs de funcionamiento del stack
- `prometheus.png` ➝ Targets de Prometheus

---

## 🧪 Ejercicio 2 - Monitorización Remota

En el segundo ejercicio se ha configurado un entorno distribuido:

- 🖥️ **Ubuntu Server**: Instalación de Prometheus y Node Exporter
- 💻 **Ubuntu Desktop 24.10**: Instalación de Grafana y configuración del dashboard
- 🌐 Exposición de métricas del servidor para ingesta remota
- 📡 Visualización de métricas del servidor en el cliente mediante Grafana

---

## 🎯 Objetivo de Aprendizaje

Esta práctica permite trabajar el resultado de aprendizaje **RA5**:

> "Analiza incidentes de ciberseguridad utilizando herramientas, mecanismos de detección y alertas de seguridad" 

---

## 📚 Referencias

- 🧠 [Introducción Prometheus & Grafana - Dinesh Murali](https://medium.com/@dineshmurali/introduction-to-monitoring-with-prometheus-grafana-ea338d93b2d9)
- 🔗 [Prometheus](https://prometheus.io/)
- 📊 [Grafana](https://grafana.com/)
- 💾 [Node Exporter GitHub](https://github.com/prometheus/node_exporter)

---

# 🐳 Práctica 5.2: Despliegue de clúster K3s en HA y servicio NGINX

Este repositorio contiene las evidencias correspondientes a la **Práctica RA5.2** del módulo de *Ciberseguridad en entornos de las tecnologías de la información*. El objetivo es realizar la instalación y validación de un clúster **K3s en modo HA**, así como desplegar un servicio **NGINX** con **2 réplicas**, y validar su funcionamiento con **K9s**.

---

## ⚙️ Instalación de K3s en modo HA

Se ha desplegado un clúster K3s en alta disponibilidad utilizando dos nodos:

- `notabot` (Master + etcd)
- `debian` (Master + etcd)

### 📸 Evidencias:

- `images/instalacio.png` ➝ Instalación del nodo `notabot` con parámetro `--cluster-init`.
- `images/instalacio_slave.png` ➝ Unión del nodo `debian` al clúster utilizando `K3S_URL` y `K3S_TOKEN`.

---

## 📦 Despliegue de NGINX con 2 réplicas

Se ha creado un `Deployment` de NGINX con 2 réplicas y un `Service` tipo LoadBalancer para exponerlo.

```bash
kubectl apply -f nginx.yaml
```

### 📸 Evidencias:

- `images/2 replicas funcionando.png` ➝ Comprobación de que las 2 réplicas están ejecutándose correctamente.
- `images/svc.png` ➝ Verificación del servicio `nginx-service` y su asignación de puerto externo (pending si no hay LoadBalancer real).

---

## 🖥️ Validación con K9s

Se ha utilizado la herramienta **K9s** para comprobar visualmente el estado de los pods y su despliegue.

### 📸 Evidencias:

- `images/k9s.png` ➝ Visualización en K9s del estado de los pods en ejecución.
- `images/exportar_config.png` ➝ Exportación de la configuración desde K9s para facilitar el acceso futuro.
- `images/funcionament.png` ➝ Visualización del servicio corriendo correctamente a nivel de interfaz.

---

## 🎯 Objetivo de Aprendizaje

Esta práctica trabaja el resultado de aprendizaje **RA5**:

> "Analiza incidentes de ciberseguridad utilizando herramientas, mecanismos de detección y alertas de seguridad"

---

## 🧰 Herramientas utilizadas

- 📦 **K3s** (v1.32.5+k3s1)
- 🔧 **kubectl**
- 📈 **K9s** (v0.50.6)
- 🐧 **Debian GNU/Linux 12** y **Arch Linux**

---

## 📚 Referencias

- 🌐 [K3s - Lightweight Kubernetes](https://k3s.io/)
- 🔎 [K9s - Kubernetes CLI To Manage Your Clusters](https://k9scli.io/)