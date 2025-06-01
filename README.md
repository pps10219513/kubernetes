# 🐳 Prácticas de Kubernetes

Este repositorio contiene las evidencias correspondientes a diversas prácticas del módulo de *Ciberseguridad en entornos de las tecnologías de la información*. Cada práctica se encuentra organizada en su propia carpeta y documenta el proceso de instalación, configuración y validación de servicios en un clúster de Kubernetes.

---

## 📁 Estructura del Repositorio

- `ejercicio 1/`: Despliegue de un servicio NGINX en un clúster de Kubernetes.
- `exercici2/`: Configuración de un servicio con balanceo de carga utilizando NGINX.
- `ejercicio_3/`: Implementación de una aplicación de ejemplo con múltiples réplicas y validación mediante K9s.

---

## 📸 Evidencias

### 🗂️ Ejercicio 1

![Despliegue de NGINX](images/ejercicio1/nginx_deploy.png)  
> Aplicación del manifiesto de despliegue de NGINX y verificación del pod en ejecución.

### 🗂️ Exercici 2

![Balanceo de carga](images/exercici2/load_balancer.png)  
> Configuración de NGINX como balanceador de carga y prueba de distribución de tráfico entre réplicas.

### 🗂️ Ejercicio 3

![Validación con K9s](images/ejercicio_3/k9s_validation.png)  
> Visualización del estado de los pods y servicios desplegados utilizando la herramienta K9s.

---

## 🧰 Herramientas Utilizadas

- 📦 **Kubernetes** (v1.23+)
- 🔧 **kubectl**
- 📈 **K9s** (v0.25+)
- 🐧 **GNU/Linux** (Distribuciones varias)

---

## 📚 Referencias

- 🌐 [Documentación oficial de Kubernetes](https://kubernetes.io/docs/)
- 🔎 [K9s - Kubernetes CLI To Manage Your Clusters](https://k9scli.io/)

---

> **Nota:** Asegúrate de que la carpeta `images/` contenga las capturas de pantalla correspondientes a cada ejercicio, organizadas en subcarpetas según el nombre de cada práctica.
