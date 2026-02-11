# ☸️ Kubernetes: De Junior a Cloud Engineer en 120min

¡Hola, Clan! Hoy vamos a dejar de ser "dueños de código" para convertirnos en "arquitectos de sistemas". 

## ⏱️ Agenda de la Sesión
* **00:00 - 00:20:** Introducción del Team Leader + "The Magic Trick" (Demo en vivo).
* **00:20 - 01:40:** Entrenamiento Autónomo (Investigación y Laboratorio).
* **01:40 - 02:00:** Checkpoint de Objetivos y Cierre.

---

## ⚡ La Probadita: El sistema que no duerme
En producción, si un servidor falla a las 2:00 AM, no queremos que nadie se despierte. **Kubernetes (K8s)** es el sistema de auto-curación que gestiona tus contenedores por ti.

> **DEMO DEL TL:** Observen la pantalla. Voy a "matar" el proceso principal de mi aplicación.
> *¿Qué pasó?* Kubernetes detectó que la realidad no coincide con mi deseo y levantó un reemplazo en milisegundos.

---

## 🎯 Objetivos de Hoy (Resultados Esperados)
Para considerar este entrenamiento exitoso, al final de las 2 horas debes haber logrado:
1.  **Levantar un Cluster Local:** Tener Minikube o Kind corriendo en tu máquina.
2.  **Desplegar Resiliencia:** Crear un Deployment con **3 réplicas** de una app.
3.  **Simular un desastre:** Borrar un Pod manualmente y verificar la auto-recuperación.
4.  **Acceso Externo:** Ver tu aplicación corriendo en el navegador a través de un Service.

---

## 🛠️ Guía de Trabajo Autónomo (70% del tiempo)

### Paso 1: El Entorno
K8s no corre directo en Windows/Mac/Linux como un .exe. Necesitas un orquestador local.
* **Misión:** Instala `kubectl` (el control remoto) y `minikube` (el cluster).
* **Comando clave para investigar:** `minikube start`.

### Paso 2: Tu primer manifiesto (.yaml)
En K8s no usamos comandos largos, usamos archivos de configuración. Crea un archivo `riwi-app.yaml` e investiga cómo estructurarlo para que contenga:
1.  Un **Deployment** que use la imagen `nginx`.
2.  Una especificación de `replicas: 3`.

### Paso 3: El desafío de la auto-curación
Una vez desplegado tu archivo (`kubectl apply -f riwi-app.yaml`):
1.  Lista tus pods: `kubectl get pods`.
2.  Borra uno: `kubectl delete pod [nombre-de-un-pod]`.
3.  **Investiga:** ¿Por qué aparece un pod nuevo con un nombre diferente de inmediato?

### Paso 4: Abrir las puertas
Los pods son efímeros y sus IPs cambian. Para entrar desde Chrome, necesitas un **Service**.
* **Misión:** Investiga cómo exponer tu deployment usando `kubectl expose` o un archivo YAML de tipo `NodePort`.

---

## 🔍 Recursos de Investigación Sugeridos
1.  **Kubernetes Docs (Get Started):** La fuente oficial.
2.  **Interactive Browser Tutorial:** [Killercoda](https://killercoda.com/playgrounds/scenario/kubernetes) (Si tu PC no soporta Minikube, úsalo aquí).
3.  **Cheat Sheet:** Busca "Kubectl Cheat Sheet" para los comandos de supervivencia.

---

## 🚩 Checklist de Entrega
Muestra a tu Team Leader o monitor:
- [ ] El comando `kubectl get deployments` mostrando 3/3 réplicas listas.
- [ ] La aplicación cargando en tu navegador local.
- [ ] Explicación de 30 segundos: ¿Qué es un `Control Plane`?