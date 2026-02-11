# 🚀 Kubernetes: El Director de Orquesta de tus Aplicaciones

¡Bienvenidos, Coders! Hoy vamos a dar el salto de "correr código en mi PC" a "gestionar infraestructuras resilientes". En el mundo laboral, no basta con que el código funcione; debe estar disponible 24/7. **Kubernetes (K8s)** es la herramienta que hace eso posible.

---

## 🎯 Objetivos de la Sesión
Al finalizar estas 2 horas, serás capaz de:
1. **Comprender** la diferencia entre un contenedor solitario y una infraestructura orquestada.
2. **Identificar** los componentes básicos: Pods, Deployments y Services.
3. **Desplegar** tu primera aplicación con auto-curación (Self-healing).

---

## 🔥 La Probadita: ¿Por qué K8s?

Imagina que tu aplicación de Node.js o Python se hace viral. De repente, tienes 10,000 usuarios. 
* **Sin K8s:** Tienes que levantar servidores manualmente, configurar balanceadores y rezar para que nada falle a las 3 AM.
* **Con K8s:** Si un contenedor muere, K8s lo revive. Si hay mucho tráfico, K8s crea clones automáticamente.



> **Reto Visual:** Observa cómo Kubernetes actúa como un "capitán de barco". Él no rema, él se asegura de que todos los remeros (contenedores) estén en su puesto y trabajando.

---

## 🛠️ Conceptos Clave (El 30% Guiado)

Para nuestra práctica, necesitamos entender tres piezas del rompecabezas:

1.  **Pod:** La unidad más pequeña. Es donde vive tu contenedor.
2.  **Deployment:** El cerebro. Aquí le dices a K8s: "Quiero que siempre existan 3 réplicas de mi app".
3.  **Service:** La puerta de entrada. Permite que el mundo exterior acceda a tus Pods.

---

## 🏗️ Entrenamiento Autónomo (El 70% Tu Turno)

Basado en la metodología Riwi, el éxito depende de tu investigación. Tienes **60 minutos** para completar el siguiente laboratorio.

### Fase 1: Instalación de Herramientas
Investiga y configura en tu entorno local:
* **Minikube** o **Kind** (Para tener un cluster de K8s en tu PC).
* **kubectl** (La herramienta de línea de comandos para hablarle a K8s).

### Fase 2: El Despliegue "Inmortal"
Crea un archivo llamado `clase-riwi.yaml` con una imagen sencilla (como `nginx`) y sigue estos pasos:
1.  Despliega 3 réplicas de la imagen.
2.  **El Experimento:** Elimina manualmente uno de los Pods usando `kubectl delete pod [nombre]`.
3.  **Observación:** Mira qué sucede inmediatamente después. ¿K8s se quedó de brazos cruzados?

### Fase 3: Exponer al Mundo
Investiga cómo crear un **Service** de tipo `LoadBalancer` o `NodePort` para ver tu aplicación en el navegador.

---

## 🚩 Entregable de la Sesión
Para validar tu entrenamiento, debes mostrar al Team Leader:
1. El comando para ver tus **Pods** activos.
2. El log de cómo Kubernetes recreó un Pod que tú eliminaste.
3. La URL local donde se ve tu app funcionando.

---

## 📚 Recursos para Investigar
* [Kubernetes Interactive Tutorials](https://kubernetes.io/docs/tutorials/kubernetes-basics/)
* [Killer.sh - Kubernetes Simulator](https://killer.sh/)
* [Documentación oficial de kubectl cheat sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

---
**"En Riwi no formamos programadores, formamos dueños de la tecnología. ¡A darle!"**