# 📂 Documentación Técnica: Mobile Testing en Urban.Lunch (Android)

Este documento detalla la estrategia de pruebas móviles, el diseño de listas de comprobación y la gestión de defectos descubiertos en la primera versión de la aplicación Android **Urban.Lunch** .

## 🧠 Contexto y Entorno de Pruebas
El alcance del testing se centró en la validación funcional e interfaz de usuario (UI) de los flujos de "Selección del punto de recogida", "Elección de platillos", "Confirmación" y "Seguimiento de pedidos". 
*   **Entorno configurado:** Pruebas ejecutadas mediante el emulador de **Android Studio** (y/o dispositivo Android físico).
*   **Gestión de Defectos:** Jira.

---

## 📋 Muestra Técnica: Diseño de Listas de Comprobación (Checklists)

Para las pruebas móviles, estructuré listas de comprobación atómicas para validar cada interacción táctil en la pantalla. A continuación, un extracto evaluando la lógica de los contadores de platillos:

| ID | Descripción de la Verificación (Elección de Platillos) | Estado | ID Defecto |
| :--- | :--- | :--- | :--- |
| **EP-5** | Confirmar que al tocar el área del platillo (excepto el '+') se abre la pantalla de detalles. | ✅ PASSED | N/A |
| **EP-7** | Verificar la funcionalidad del contador al hacer clic repetido en '+' aumenta el contador. | ❌ FAILED | S5MAVM-3 |
| **EP-9** | Confirmar que el contador no baja de 0. | ✅ PASSED | N/A |

> *Nota de QA: El fallo en el caso EP-7 representaba un bloqueador crítico para las ventas, ya que impedía a los usuarios agregar múltiples unidades de un mismo producto al carrito.*

---

## 🐛 Evidencia Técnica: Reporte de Errores Críticos (Jira)

Durante la regresión móvil, identifiqué fallos que afectaban la experiencia del usuario y la integración con el sistema operativo Android.

### 1. Defecto de Integración con el SO (Permisos de Ubicación)
*   **Descripción del Defecto (NE-1):** Al denegar el acceso a la geolocalización del dispositivo, la aplicación no muestra el mensaje de error informando que se necesita la ubicación para funcionar correctamente .
*   **Impacto:** El usuario queda en un estado de confusión ("Dead end") sin saber por qué la app no carga los puntos de recogida.


<img width="337" height="562" alt="SPR-1 - Error al cargar el mapa, al abrir la app de Urban Lunch" src="https://github.com/user-attachments/assets/83d97eb8-cb20-429c-b2cd-2f7b26a12285" />


### 2. Defecto de Usabilidad y Renderizado de UI
*   **Descripción del Defecto (DP-18):** En la pantalla de detalles del platillo, el nombre del restaurante se visualiza superpuesto con otros elementos de la interfaz, dificultando la lectura.
*   **Impacto:** Degrada la calidad visual de la aplicación móvil, causando una pobre experiencia de usuario (UX).


<img width="357" height="669" alt="CAPTURA PARA COD 4 DE DETAllES DEL PLATILLO" src="https://github.com/user-attachments/assets/9dd6dff0-c540-4e83-982e-57419331ce56" />


---
*Documentación estructurada por María Auxiliadora Vélez Mendoza - QA Engineer.*
