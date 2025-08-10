# 🔄 Ciclo de Vida del Bug

El **ciclo de vida de un bug** describe las diferentes etapas que atraviesa un error desde que se detecta hasta que se cierra.  
Este proceso asegura trazabilidad, comunicación efectiva y control de calidad en la gestión de incidencias.

---

## 📋 Etapas típicas

1. **Nuevo / Reportado**  
   El bug ha sido detectado y documentado por QA o un usuario.

2. **Asignado**  
   El responsable del proyecto asigna el bug a un desarrollador.

3. **En progreso / En reparación**  
   El desarrollador trabaja en la corrección.

4. **Corregido / Fixed**  
   El cambio ha sido implementado en el código.

5. **En pruebas / Ready for QA**  
   QA verifica si la corrección funciona y no afecta otras partes del sistema.

6. **Reabierto** *(si aplica)*  
   Si el bug persiste o reaparece, se vuelve a abrir.

7. **Cerrado**  
   La corrección es validada y aprobada por QA.

8. **Rechazado / No reproducible** *(si aplica)*  
   El bug no se puede replicar o se considera inválido.

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
