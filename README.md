# 📱 Pruebas de Aplicaciones Móviles (Android): Urban.Lunch

![Project](https://img.shields.io/badge/Project-Mobile_Testing-blue) ![OS](https://img.shields.io/badge/OS-Android-green) ![Tool](https://img.shields.io/badge/Tool-Android_Studio-orange) ![Tracking](https://img.shields.io/badge/Tracking-Jira-blue)

## 📌 Resumen del Proyecto 

*   **Situación:** El equipo de desarrollo lanzó la primera versión para Android de **Urban.Lunch**, una aplicación móvil para pedir comida a diferentes restaurantes y enviarla a puntos de recogida. Era indispensable garantizar la usabilidad, la lógica de los contadores del carrito de compras y la correcta gestión de permisos del dispositivo (como la geolocalización) antes de su lanzamiento .
*   **Tarea:** Diseñar y ejecutar listas de comprobación exhaustivas probando la aplicación directamente en un entorno móvil (emulador de Android Studio / dispositivo Android) y reportar cualquier anomalía de UI/UX o funcional en Jira.
*   **Acción:** 
    * Ejecuté pruebas funcionales navegando por el mapa de puntos de recogida, pantallas de detalles de platillos y seguimiento de temporizadores de pedidos.
    * Estresé la interfaz de usuario comprobando superposiciones de texto y cambios dinámicos de estado (ej. colores de selección en platillos y botones).
    * Validé la integración de hardware/software denegando el acceso a la ubicación para verificar el manejo de excepciones (Notificaciones de error).
*   **Resultado:** Se aislaron más de 10 defectos, incluyendo fallos críticos donde el contador de unidades no aumentaba al presionar el botón '+' , superposición de nombres de restaurantes en la interfaz y vulnerabilidades en la gestión de permisos (la app no mostraba el error al denegar la geolocalización). 

---

## 🛠️ Stack Tecnológico y Herramientas

*   **Plataforma:** Android.
*   **Entorno de Pruebas:** Emulador de Android Studio / Dispositivo físico.
*   **Documentación y Seguimiento:** Listas de comprobación (Checklists), Jira (Bug Tracking).
*   **Tipos de Prueba:** Mobile Testing, UI/UX Testing, Functional Testing, Pruebas de Permisos del SO.

---

## 📸 Evidencias de Ejecución (Mobile Testing)

*(Nota: Demostración de la interfaz de Urban.Lunch ejecutándose en entorno de pruebas).*

<!-- 📸 ESPACIO PARA EVIDENCIA 1: Sube aquí una captura de pantalla de la app corriendo en tu emulador de Android o una de tus evidencias de Jira -->
![Evidencia de Pruebas Móviles] (assets/Emulador de la app Urban.Lunch.png)

---
*🧑‍💻 Perfil Técnico: María Auxiliadora Vélez Mendoza - QA Engineer*