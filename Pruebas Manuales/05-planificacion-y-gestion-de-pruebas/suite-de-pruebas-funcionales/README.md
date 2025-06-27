# 📦 Suite de Pruebas Funcionales

Una **suite de pruebas funcionales** es un conjunto organizado de casos de prueba que validan el correcto funcionamiento de un sistema de acuerdo con los requisitos definidos.

Esta suite se deriva directamente del **plan de pruebas** y los **criterios de aceptación** definidos en las historias de usuario, de mala manera lo veremos en el futuro simplemente como una carpeta en la que se encuentran los PDP.

---

## 🎯 Objetivo

- Validar funcionalidades desde la perspectiva del usuario.  
- Confirmar que los flujos clave funcionan según lo esperado.  
- Cubrir tanto escenarios positivos como negativos.  
- Proveer trazabilidad entre requisitos y resultados de prueba.

---

## 🧩 Cobertura de esta suite

| Historia | Funcionalidad | Casos cubiertos                        |
|----------|----------------|----------------------------------------|
| US001    | Login           | Acceso válido, error por credenciales |
| US002    | Transferencia   | Transferencia válida e inválida       |

---
## 📌 Ejemplos de test suite
### ✅ Casos de Prueba – Login

| ID       | Descripción                           | Datos entrada             | Resultado esperado                          | Estado |
|----------|----------------------------------------|---------------------------|----------------------------------------------|--------|
| TC001    | Login exitoso                          | user: john, pass: demo    | Redirección al panel de usuario              | ☐      |
| TC002    | Login con credenciales inválidas       | user: john, pass: xyz     | Mensaje de error                             | ☐      |
| TC003    | Login con campos vacíos                | user: "", pass: ""        | Validación de campos obligatorios            | ☐      |

---

### ✅ Casos de Prueba – Transferencias

| ID       | Descripción                                    | Datos entrada                             | Resultado esperado                          | Estado |
|----------|------------------------------------------------|--------------------------------------------|----------------------------------------------|--------|
| TC004    | Transferencia válida entre cuentas             | cuenta origen, cuenta destino, 100€        | Confirmación de transferencia, saldo ok      | ☐      |
| TC005    | Transferencia con importe 0                    | cuenta origen, cuenta destino, 0€          | Mensaje de error por importe no válido       | ☐      |
| TC006    | Transferencia con saldo insuficiente           | cuenta origen, cuenta destino, 999999€     | Error por saldo insuficiente                 | ☐      |

---

📌 *Puedes marcar el estado como: ✅ Aprobado / ❌ Fallado / ☐ No ejecutado*

---

## 🧪 Buenas prácticas al diseñar suites

- Asegúrate de cubrir al menos un caso positivo y uno negativo por funcionalidad.  
- Agrupa los casos por módulo o historia.  
- Usa IDs únicos y consistentes (TC001, TC002...).  

---

> 💬 Una suite de pruebas clara es clave para mantener la calidad del producto en cada sprint.

---

📥 Te dejo esta suite en formato Excel, que es de la manera en que normalmente la encontraremos en nuestro día a día:  
🧾 `suite-de-pruebas-parabank.xlsx` (ver carpeta del repositorio)

---

📌 Documento elaborado por **Francis Paneque** – QA Specialist  
✉️ francisco.j.paneque@gmail.com | 🌐 [LinkedIn](https://www.linkedin.com/in/francis-paneque-21092a252)
