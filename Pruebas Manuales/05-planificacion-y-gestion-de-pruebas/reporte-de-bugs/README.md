# 🐞 Plantilla de Reporte de Bugs

Un **reporte de bug** es un documento que describe un comportamiento no deseado del software. Su objetivo es que el equipo de desarrollo pueda entender, reproducir y corregir el error de la forma más eficiente posible.

---

## 🎯 ¿Por qué es importante reportar bien los bugs?

- Ahorra tiempo al equipo de desarrollo  
- Evita ambigüedades sobre lo que falla  
- Mejora la trazabilidad de los errores  
- Ayuda a priorizar la corrección según impacto  
- Profesionaliza el trabajo de QA en cualquier entorno

---

## 🧩 Elementos clave de un bug report

| Campo                 | Descripción |
|----------------------|-------------|
| **ID del bug**        | Identificador único (ej. BUG-001) |
| **Título**            | Breve descripción del problema |
| **Descripción**       | Qué ocurre, cuándo y cómo |
| **Pasos para reproducir** | Detalle paso a paso |
| **Resultado actual**  | Qué está sucediendo |
| **Resultado esperado**| Qué debería suceder |
| **Severidad**         | Crítica / Alta / Media / Baja |
| **Prioridad**         | Alta / Media / Baja |
| **Entorno**           | Navegador, versión, sistema |
| **Evidencias**        | Capturas, vídeos o logs |
| **Estado**            | Abierto, En progreso, Cerrado |

---

## 🧪 Ejemplo práctico – Parabank

**ID del bug:** `BUG-005`  
**Título:** No se muestra mensaje de error al intentar transferir 0€  
**Descripción:** Al intentar realizar una transferencia con importe 0€, el sistema no bloquea la operación ni muestra mensaje de advertencia.

**Pasos para reproducir:**
1. Iniciar sesión en [Parabank](https://parabank.parasoft.com)
2. Ir a la sección "Transfer Funds"
3. Seleccionar cuenta origen y destino válidas
4. Introducir `0` como importe
5. Hacer clic en “Transfer”

**Resultado actual:**  
No ocurre nada, no hay mensaje de error y el sistema queda aparentemente bloqueado.

**Resultado esperado:**  
El sistema debería impedir la operación y mostrar un mensaje tipo: “El importe debe ser mayor a 0€”.

**Severidad:** Media  
**Prioridad:** Alta  
**Entorno:** Chrome 125 / macOS Sonoma  
**Evidencias:** [captura_bug005.png]  
**Estado:** Abierto

---

## ✅ Buenas prácticas

- Usa títulos concretos y descriptivos  
- Detalla bien los pasos para que se pueda reproducir el error fácilmente  
- Acompaña siempre con evidencias visuales o logs  
- No combines varios errores en un mismo reporte  
- Usa etiquetas o campos de prioridad según el impacto

---

📥 También puedes usar la plantilla en Excel que acompaña este punto, ideal para equipos pequeños o proyectos sin Jira:  
🧾 `plantilla-reporte-de-bugs.xlsx` (ver carpeta del repositorio)

---

📌 Documento elaborado por **Francis Paneque – QA Specialist**  
✉️ francisco.j.paneque@gmail.com | 🌐 [LinkedIn](https://www.linkedin.com/in/francis-paneque-21092a252)
