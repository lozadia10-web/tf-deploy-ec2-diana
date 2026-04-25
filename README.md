# 🚀 Despliegue de Infraestructura AWS con Terraform & CI/CD

Este proyecto automatiza la creación de una instancia **EC2**, un **Security Group** y un **IAM Role** en AWS utilizando **Terraform**. Además, cuenta con un flujo de integración y despliegue continuo (CI/CD) mediante **GitHub Actions**.

## 🏗️ Arquitectura de la Solución
La infraestructura está organizada mediante módulos para asegurar la escalabilidad y el orden:
- **IAM Module:** Configura el rol con políticas de AmazonSSM y CloudWatch.
- **Security Group Module:** Define reglas de acceso (RDP puerto 3389).
- **EC2 Module:** Gestiona la instancia, el par de llaves (.pem) y el disco de almacenamiento gp3.



## 🛠️ Tecnologías Utilizadas
- **Terraform:** Infraestructura como Código (IaC).
- **AWS:** Proveedor de servicios en la nube.
- **GitHub Actions:** Automatización de despliegue (CI/CD).
- **S3 Backend:** Para el almacenamiento remoto del estado de Terraform.

## 🤖 Automatización CI/CD
El proyecto incluye un pipeline que se dispara automáticamente en cada `push` a la rama `main`:
1. **Terraform Init:** Inicializa el entorno y el backend.
2. **Terraform Format & Validate:** Asegura que el código sea correcto y profesional.
3. **Terraform Plan:** Muestra los cambios antes de aplicarlos.
4. **Terraform Apply:** Despliega los recursos en AWS de forma automática.



## 📋 Requisitos Previos
Para replicar este proyecto localmente, necesitas:
- Terraform instalado.
- AWS CLI configurado con credenciales válidas.
- Un bucket S3 para el `backend.tf`.

## 🚀 Cómo usar este repositorio
1. Clonar el repositorio.
2. Configurar los secretos en GitHub: `AWS_ACCESS_KEY_ID` y `AWS_SECRET_ACCESS_KEY`.
3. Realizar un cambio y hacer `push` para ver la magia en la pestaña **Actions**.

---
*Proyecto desarrollado por Diana Marcela Lozano Zárate - Analyst Cloud*
