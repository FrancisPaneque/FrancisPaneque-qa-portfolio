# 📑 Plan de Pruebas

El **Plan de Pruebas** es un documento que define el enfoque, el alcance y los criterios con los que se realizarán las pruebas en un proyecto o funcionalidad concreta.

En este portafolio, cada plan estará basado en una o más historias de usuario reales para mostrar cómo se diseña y organiza el trabajo de QA en un entorno funcional.

---

## 🧠 ¿Por qué es importante?

- Alinea al equipo sobre lo que se va a probar y cómo.  
- Permite priorizar riesgos y funcionalidades críticas.  
- Sirve como guía para documentar y auditar el proceso.  
- Facilita la trazabilidad entre requisitos y pruebas.

---

## 🏗️ Estructura típica de un Plan de Pruebas

1. **Objetivo del plan**
2. **Alcance funcional** (qué se prueba y qué no)
3. **Estrategia de pruebas**
4. **Tipos de pruebas**
5. **Entorno y datos de prueba**
6. **Riesgos identificados**
7. **Responsables del proceso**
8. **Steps de prueba**

---

## 🧾 Caso aplicado – Parabank

Plan de Pruebas basado en estas historias:

- ✅ US001: Login
- ✅ US002: Transferencias entre cuentas

**Objetivo:**  
Validar que el usuario pueda autenticarse y realizar transferencias sin errores funcionales.

**Alcance:**  
✔️ Login, logout, selección de cuentas, validación de importes  
❌ Registro, solicitud de préstamos, edición de perfil

**Estrategia:**  
- Pruebas manuales funcionales en entorno demo  
- Exploración básica de errores inesperados

**Tipos de prueba:**  
- Positivas y negativas  
- Regresión puntual  
- Validación visual ligera

**Entorno:**  
[https://parabank.parasoft.com](https://parabank.parasoft.com)  
Usuario: `john` / `demo`

## ✅ Criterios de Aceptación (Formato Gherkin)

### US001 – Login exitoso
```
Given el usuario está en la pantalla de login,

When introduce credenciales válidas,

Then debe acceder a su panel de cuentas.
```

### US002 – Transferencia entre cuentas
```
Given el usuario está logueado y en la sección de transferencias,

When selecciona cuentas válidas e introduce un importe positivo,

Then la transferencia debe ejecutarse y actualizarse el saldo.
```

---

## 🧭 Steps de prueba – Ejecución detallada

### 🔐 Login

| Paso | Acción | Resultado esperado |
|------|--------|---------------------|
| 1    | Acceder a la página de login | Se carga correctamente la vista |
| 2    | Introducir usuario y contraseña válidos | Campos aceptan input |
| 3    | Hacer clic en "Log In" | Redirección al panel principal del usuario |

---

### 💸 Transferencias

| Paso | Acción | Resultado esperado |
|------|--------|---------------------|
| 1    | Ir a "Transfer Funds" | Se muestra el formulario de transferencia |
| 2    | Seleccionar cuenta origen y destino | Las cuentas aparecen disponibles |
| 3    | Introducir un importe válido | Input aceptado, sin errores |
| 4    | Hacer clic en "Transfer" | Confirmación de transferencia exitosa |
| 5    | Verificar el historial de transacciones | Movimiento reflejado correctamente |

---

📥 También puedes consultar este plan en Excel como plantilla de documentación o auditoría:  
🧾 `plan-de-pruebas-parabank.xlsx` (ver carpeta del repositorio)

---

> 💬 La clave no es tener muchas pruebas, sino las pruebas correctas, bien documentadas y alineadas al valor de usuario.

---

📌 Documento elaborado por **Francis Paneque** – QA Specialist  
✉️ francisco.j.paneque@gmail.com | 🌐 [LinkedIn](https://www.linkedin.com/in/francis-paneque-21092a252)
