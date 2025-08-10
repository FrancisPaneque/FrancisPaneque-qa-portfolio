# 🔄 Ciclo de Vida del Bug

El **ciclo de vida de un bug** describe las diferentes etapas que atraviesa un error desde que se detecta hasta que se cierra.  
Este proceso asegura trazabilidad, comunicación efectiva y control de calidad en la gestión de incidencias.

---

## 📋 Etapas típicas

1. **Nuevo / Reportado**  
   - El bug ha sido detectado por QA, un usuario final o cualquier miembro del equipo y se documenta en la herramienta de seguimiento (por ejemplo: Jira, Azure DevOps).  
   - Se incluye información como: descripción, pasos para reproducir, entorno afectado y evidencias (capturas de pantalla, logs, vídeos).  
   - *Ejemplo:* QA detecta que al intentar transferir fondos con importe negativo, la aplicación no muestra el mensaje de error esperado.

2. **Asignado**  
   - El líder técnico, Project Manager o Scrum Master asigna el bug a un desarrollador responsable de corregirlo.  
   - Se prioriza en función de la severidad y el impacto en el negocio.  
   - *Ejemplo:* El bug detectado en transferencias es asignado al desarrollador de backend que gestiona la lógica de validación de importes.

3. **Open**  
   - El desarrollador comienza a trabajar en la incidencia y confirma que puede reproducir el error.  
   - En esta etapa, el bug puede recibir alguno de estos estados derivados:  
     - **Duplicado:** ya existe un reporte previo idéntico.  
     - **Rechazado:** el bug no es válido o el comportamiento es esperado según el diseño.  
     - **Aplazado:** se reconoce el problema, pero se pospone su corrección para una futura iteración.  
   - *Ejemplo:* El desarrollador confirma que el bug es válido y pasa a implementar la solución.

4. **Fixed**  
   - El desarrollador implementa la corrección en el código y la sube al repositorio de desarrollo.  
   - Se documentan los cambios realizados y se enlazan con el bug en la herramienta de seguimiento.  
   - *Ejemplo:* Se añade una validación en el backend para que importe negativo muestre un mensaje de error.

5. **Testing**  
   - El equipo de QA recibe la nueva versión con el fix y ejecuta las pruebas de validación.  
   - Se revisan no solo los pasos del bug, sino también casos relacionados para evitar regresiones.  
   - *Ejemplo:* QA prueba transferencias con importe negativo y positivo para confirmar que todo funciona correctamente.

6. **Reopen** *(si aplica)*  
   - Si durante la fase de testing el bug persiste o se detectan errores colaterales, el bug se reabre.  
   - Se devuelve al estado **Open** y se notifica al desarrollador para nueva corrección.  
   - *Ejemplo:* El mensaje de error aparece, pero con un texto incorrecto, por lo que se reabre.

7. **Verificado**  
   - QA confirma que la corrección funciona como se esperaba y que no hay efectos adversos.  
   - *Ejemplo:* Tras el fix final, el sistema muestra el mensaje correcto y no afecta otras funciones.

8. **Closed**  
   - El bug se da por resuelto y se cierra definitivamente en la herramienta de gestión.  
   - No requiere más acciones y se considera parte del historial del proyecto.  
   - *Ejemplo:* El bug queda cerrado y marcado como resuelto en la release correspondiente.

---

## Diagrama del ciclo de Vida del Bug
![Image_Alt](https://github.com/FrancisPaneque/FrancisPaneque-qa-portfolio/blob/561e6bc74007852a6ff65cffe62432d3c997d1c9/Pruebas%20Manuales/diagramaCVB-ByFP.png)

---

## 🧪 Ejemplo práctico – Parabank

**Bug:** Transferencia con importe 0 no muestra mensaje de error.  
1. Reportado en Jira como *BUG-005*.  
2. Asignado a un desarrollador backend.  
3. Corregido añadiendo validación en el campo importe.  
4. Pasó a QA para pruebas en staging.  
5. QA verifica y detecta que el mensaje sí aparece ahora.  
6. Bug cerrado.

---

## 💡 Buenas prácticas + tips

- Documentar cada cambio de estado en la herramienta de seguimiento (Jira, Azure DevOps, etc.), durante mi experiencia siempre he usado una muletilla que me ha ayudado (varía dependiendio de la herramienta): "Fecha de la modificación + Nombre del tester/equipo + estado al que pasa + motivo".
- Usar evidencias visuales y logs en cada transición importante.
- Evitar cerrar un bug sin validación previa de QA.

---

📌 Documento elaborado por **Francis Paneque – QA Specialist**  
✉️ francisco.j.paneque@gmail.com | 🌐 [LinkedIn](www.linkedin.com/in/francisco-paneque-jurado-21092a252)
