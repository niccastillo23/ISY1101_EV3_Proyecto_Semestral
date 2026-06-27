# 🚀 Innovatech - Cloud Orchestration & CI/CD Pipeline (AWS EKS)

Este repositorio contiene la arquitectura de microservicios contenerizada y la configuración de infraestructura como código (YAML) para el despliegue elástico en **Amazon EKS (Elastic Kubernetes Service)** del sistema central de **Innovatech**, cumpliendo rigurosamente con los lineamientos de la evaluación **ISY1101_EV3**.

---

## 🛠️ Arquitectura de la Solución

La solución está distribuida bajo un enfoque nativo en la nube en el espacio de nombres corporativo `innovatech`:

* **`front-despacho`**: Aplicación frontend construida en **React**, expuesta al tráfico de internet público por medio de un balanceador de carga aprovisionado automáticamente por AWS.
* **`back-despachos`**: Microservicio REST desarrollado en **Spring Boot** (Java 17) ejecutándose internamente bajo el puerto `8081`.
* **`back-ventas`**: Microservicio REST desarrollado en **Spring Boot** (Java 17) ejecutándose internamente bajo el puerto `8080`.

---

## 📂 Estructura del Repositorio

```text
├── back-Despachos_SpringBoot/  # Código fuente del microservicio de Despachos
├── back-Ventas_SpringBoot/     # Código fuente del microservicio de Ventas
├── front_despacho/             # Código fuente de la interfaz de usuario (React)
├── k8s/                        # Manifiestos de Kubernetes declarativos
│   ├── despachos-deployment.yaml
│   ├── ventas-deployment.yaml
│   └── front-deployment.yaml
├── pipeline-actions.txt        # Especificación técnica del Pipeline CI/CD (GitHub Actions)
└── README.md                   # Documentación del proyecto
