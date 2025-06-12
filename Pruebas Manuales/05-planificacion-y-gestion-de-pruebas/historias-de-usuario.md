# 🧾 Historias de Usuario

En un entorno ágil, las **Historias de Usuario (US)** representan funcionalidades desde el punto de vista del usuario final. Son el primer paso del flujo de trabajo del QA, ya que definen **lo que debe ser validado** y permiten establecer los **criterios de aceptación**.

---

## 💬 ¿Qué es una Historia de Usuario?

Es una frase breve que expresa **quién necesita qué** y **por qué**. 

⚠️ Anotar que desde mi experiencia he visto las historias de usuario en **formato BDD con Gherkin**, es decir, lo que vamos a ver en estos apuntes como la Estructura típica. Seguramente lo veamos en ingles como **Given**, **When**, **Then**. 

📌 Estructura típica:

- Como [tipo de usuario],
- Quiero [acción o funcionalidad],
- Para [beneficio o necesidad].

Estas historias se definen en conjunto con el Product Owner y sirven de base para diseñar los casos de prueba, documentarlos y verificar si están completos.

---

## 🧠 ¿Qué busca un QA al leer una US?

Un QA debe:

- Validar que la historia es clara y entendible.  
- Solicitar criterios de aceptación si faltan.  
- Diseñar pruebas positivas y negativas basadas en los criterios.  
- Verificar que cubre tanto la lógica funcional como la experiencia de usuario.

---

## ✅ Criterios de Aceptación

Son las condiciones **que deben cumplirse** para que una historia se considere completada y aceptada por el PO o QA.  
Permiten establecer si la funcionalidad cumple su propósito desde la perspectiva del usuario.

---

## 📋 Ejemplos reales en Parabank

### US001 – Inicio de sesión

- Como cliente registrado,
- quiero iniciar sesión en Parabank con mi usuario y contraseña,
- para acceder a mis cuentas de forma segura.


**Criterios de aceptación:**
- El usuario debe poder iniciar sesión con credenciales válidas.
- Si hay error en los datos, se debe mostrar un mensaje claro.
- Tras iniciar sesión correctamente, el usuario es redirigido a su panel personal.

---

### US002 – Transferencias entre cuentas

- Como cliente autenticado,
- quiero transferir dinero entre mis cuentas,
- para mover fondos fácilmente sin necesidad de acudir al banco.


**Criterios de aceptación:**
- Se puede elegir cuenta origen y cuenta destino.
- El importe debe ser mayor a 0 y menor al saldo disponible.
- Al confirmar, debe mostrarse mensaje de éxito.
- El saldo debe actualizarse correctamente tras la transferencia.

---

### US003 – Cierre de sesión

- Como cliente autenticado,
- quiero cerrar sesión desde cualquier punto del sitio,
- para proteger mi información cuando termine de operar.

**Criterios de aceptación:**
- El botón de logout debe estar siempre visible tras iniciar sesión.
- Al hacer clic en logout, debe finalizar la sesión y redirigir al login.
- La sesión no debe estar activa al retroceder en el navegador.

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
