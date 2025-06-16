# 🧾 Historias de Usuario

En un entorno ágil, las **Historias de Usuario (US)** representan funcionalidades desde el punto de vista del usuario final. Son el primer paso del flujo de trabajo del QA, ya que definen **lo que debe ser validado** y permiten establecer los **criterios de aceptación**. En estA página veremos como enfocarlo desde un punto de vista más teórico y como a lo largo de mi carrera lo he encontrado en distintos equipos de trabajo en el día a día.

⚠️ Anotar que 


---
# **DESDE LA TEORÍA**
## 💬 ¿Qué es una Historia de Usuario?

Es una frase breve que expresa **quién necesita qué** y **por qué**. 

📌 Estructura típica:

- Como [tipo de usuario],
- Quiero [acción o funcionalidad],
- Para [beneficio o necesidad].

Estas historias se definen en conjunto con el Product Owner y sirven de base para diseñar los casos de prueba, documentarlos y verificar si están completos.

## ✅ Criterios de Aceptación

Son las condiciones **que deben cumplirse** para que una historia se considere completada y aceptada por el PO o QA.  
Permiten establecer si la funcionalidad cumple su propósito desde la perspectiva del usuario.

---
# **DESDE MI EXPERIENCIA**
## 💬 ¿Qué es una Historia de Usuario?

Es un documento o página que define las funcionalidades a desarrollar.

🆘**Ej.** Como cliente de Para Bank, quiero poder ver el saldo actual de mi cuenta desde el panel principal después de iniciar sesión, para tener claridad inmediata sobre mis finanzas.

## ✅ Criterios de Aceptación

Desde mi experiencia he visto los criterios de aceptación en **formato BDD con Gherkin**, es decir, los veremos como "**Como** +  rol de usuario", "**Cuando** + flujo a probar" y "**Entonces** + resultado esperado". O como seguramente lo encontremos **Given**, **When**, **Then**, básicamente en Ingles.

🆘**Ej.** 

Scenario: Mostrar el saldo de la cuenta en el panel principal

&nbsp;&nbsp; Given que el cliente ha iniciado sesión correctamente
  
&nbsp;&nbsp; When el cliente accede al panel principal
  
&nbsp;&nbsp; Then el sistema debe mostrar el saldo actual de la cuenta en una sección visible

---

## 🧠 ¿Qué busca un QA al leer una US?

Un QA debe:

- Validar que la historia es clara y entendible.  
- Solicitar criterios de aceptación si faltan.  
- Diseñar pruebas positivas y negativas basadas en los criterios.  
- Verificar que cubre tanto la lógica funcional como la experiencia de usuario.

---

## 📋 Ejemplos reales en Parabank
```
Desde la teoría = 📚
Desde mi experiencia = 👨🏽‍🔬
```

### 📚 US001 – Inicio de sesión

- Como cliente registrado,
- quiero iniciar sesión en Parabank con mi usuario y contraseña,
- para acceder a mis cuentas de forma segura.


**Criterios de aceptación:**
- El usuario debe poder iniciar sesión con credenciales válidas.
- Si hay error en los datos, se debe mostrar un mensaje claro.
- Tras iniciar sesión correctamente, el usuario es redirigido a su panel personal.

### 👨🏽‍🔬 US001 – Inicio de sesión

**Descripción:**  
Como cliente registrado, quiero iniciar sesión en Para Bank con mi usuario y contraseña, para acceder a mis cuentas de forma segura.

**Criterios de Aceptación:**

```gherkin
Scenario: Inicio de sesión exitoso con credenciales válidas
  Given que el cliente está en la página de inicio de sesión
  And introduce un usuario y contraseña válidos
  When hace clic en el botón de iniciar sesión
  Then debe ser redirigido a su panel personal

Scenario: Error al ingresar credenciales incorrectas
  Given que el cliente está en la página de inicio de sesión
  And introduce un usuario o contraseña incorrectos
  When hace clic en el botón de iniciar sesión
  Then el sistema debe mostrar un mensaje de error claro indicando que las credenciales no son válidas
```
---

### 📚 US002 – Transferencias entre cuentas

- Como cliente autenticado,
- quiero transferir dinero entre mis cuentas,
- para mover fondos fácilmente sin necesidad de acudir al banco.


**Criterios de aceptación:**
- Se puede elegir cuenta origen y cuenta destino.
- El importe debe ser mayor a 0 y menor al saldo disponible.
- Al confirmar, debe mostrarse mensaje de éxito.
- El saldo debe actualizarse correctamente tras la transferencia.

### 👨🏽‍🔬US002 – Transferencias entre cuentas

**Descripción:**
Como cliente autenticado, quiero transferir dinero entre mis cuentas, para mover fondos fácilmente sin necesidad de acudir al banco.

**Criterios de Aceptación:**

```gherkin
Scenario: Transferencia exitosa entre cuentas
  Given que el cliente ha iniciado sesión
  And selecciona una cuenta de origen y una de destino distintas
  And introduce un importe mayor a 0 y menor al saldo disponible
  When confirma la transferencia
  Then el sistema debe mostrar un mensaje de éxito
  And debe actualizarse el saldo de ambas cuentas correctamente

Scenario: Error al ingresar importe inválido
  Given que el cliente ha iniciado sesión
  And introduce un importe menor o igual a 0, o mayor al saldo disponible
  When intenta confirmar la transferencia
  Then el sistema debe mostrar un mensaje indicando que el importe no es válido
```

---

### 📚 US003 – Cierre de sesión

- Como cliente autenticado,
- quiero cerrar sesión desde cualquier punto del sitio,
- para proteger mi información cuando termine de operar.

**Criterios de aceptación:**
- El botón de logout debe estar siempre visible tras iniciar sesión.
- Al hacer clic en logout, debe finalizar la sesión y redirigir al login.
- La sesión no debe estar activa al retroceder en el navegador.

### 👨🏽‍🔬 US003 – Cierre de sesión

**Descripción:**
Como cliente autenticado, quiero cerrar sesión desde cualquier punto del sitio, para proteger mi información cuando termine de operar.

**Criterios de Aceptación:**

```gherkin
Scenario: Cierre de sesión desde el botón de logout
  Given que el cliente ha iniciado sesión
  And el botón de logout está visible
  When hace clic en el botón de logout
  Then debe finalizar la sesión
  And debe ser redirigido a la página de inicio de sesión

Scenario: Impedir acceso tras cerrar sesión
  Given que el cliente ha cerrado sesión
  When intenta retroceder en el navegador
  Then el sistema no debe mostrar el panel personal
  And debe permanecer en la página de inicio de sesión
```

---

## 📌 Buenas prácticas al usar historias de usuario

- No asumir información que no esté explícita.  
- Pedir criterios claros cuando falten.  
- Asegurar que cada US tenga trazabilidad con sus pruebas.  
- No diseñar pruebas sin validar antes la historia.

---

> 💡 Como QA, tu trabajo empieza desde aquí. Una buena historia de usuario da lugar a un buen plan de pruebas.

---

📌 Documento elaborado por **Francis Paneque** – QA Specialist  
✉️ francisco.j.paneque@gmail.com | 🌐 [LinkedIn](https://www.linkedin.com/in/francis-paneque-21092a252)
