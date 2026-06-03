# 🚀 Laboratorio de Observabilidad y Persistencia Microservicios

Este repositorio contiene un entorno completo de infraestructura como código (IaC) diseñado para desplegar, persistir y monitorizar una aplicación web en contenedores utilizando buenas prácticas de DevOps.

## 🛠️ Tecnologías Utilizadas

* **Orquestación:** Docker & Docker Compose
* **Aplicación Frontend/Backend:** Node.js (Express)
* **Base de Datos:** MySQL 8.0 con volúmenes persistentes
* **Monitorización y Métricas:** Prometheus & Node Exporter
* **Visualización de Datos:** Grafana

## 🏗️ Arquitectura del Sistema

El entorno levanta de forma aislada una red interna de Docker donde conviven los siguientes servicios:
1. `mi-web`: Aplicación Node.js expuesta en el puerto `3000`.
2. `mysql`: Base de datos conectada a la app web con datos inmortalizados en un volumen local.
3. `node-exporter`: Extractor de métricas de hardware de la máquina host.
4. `prometheus`: Servidor encargado de hacer scraping al job de métricas de infraestructura.
5. `grafana`: Panel visualizador para la toma de decisiones críticas de sistemas.

## 🚀 Cómo Desplegar el Entorno

Para levantar este laboratorio en un servidor limpio, solo es necesario clonar el repositorio y ejecutar:

```bash
docker compose up -d
