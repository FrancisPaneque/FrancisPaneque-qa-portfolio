# 🌀 Metodologías de Desarrollo

En el contexto del aseguramiento de la calidad, entender las metodologías de desarrollo es esencial para alinear las pruebas al ciclo de vida del software. Las dos metodologías más comunes son el modelo en cascada y los enfoques ágiles, como Scrum, siendo este el que me llevo encontrando en todos los proyectos que he trabajado hasta ahora.

---

## 📚 Tipos de Metodologías

### 🏛️ Metodologías Tradicionales

- **Modelo en Cascada (Waterfall):**  
  Un enfoque lineal donde las etapas (análisis, diseño, implementación, pruebas, etc.) se completan secuencialmente.*(Desarrollado en detalle más abajo, ya que no tanto como la Scrum, pero si he visto en algún proyecto)*

- **Prototipado:**  
  Se crea un prototipo para validar requisitos y diseño antes de la implementación completa.

- **Modelo Incremental:**  
  Se desarrolla el software en incrementos, añadiendo nuevas funcionalidades en cada iteración.

- **Desarrollo Rápido de Aplicaciones (RAD):**  
  Se enfoca en la creación rápida de prototipos y la entrega temprana de software.

- **Desarrollo en Espiral:**  
  Un modelo iterativo que incluye análisis de riesgos en cada ciclo.

### ⚙️ Metodologías Ágiles

- **Scrum:**  
  Un marco de trabajo iterativo e incremental que utiliza sprints para entregar software funcional. *(Desarrollado en detalle más abajo, ya que durante mi carrera es sin duda la que mas he visto en distintos equipos)*

- **Kanban:**  
  Un sistema visual que ayuda a gestionar el flujo de trabajo y a optimizar la entrega.

- **Programación Extrema (XP):**  
  Se centra en la colaboración, la simplicidad, las pruebas y la retroalimentación.

- **Lean Software Development:**  
  Un enfoque que busca eliminar el desperdicio y maximizar el valor para el cliente.

- **Desarrollo Basado en Características (FDD):**  
  Se enfoca en el desarrollo por características, entregando pequeñas funcionalidades de forma iterativa.

---

## 🌊 1. Modelo en Cascada

El modelo en cascada es una metodología **secuencial**, donde cada fase del desarrollo debe completarse antes de avanzar a la siguiente. Las fases típicas incluyen:

- Recolección de requisitos
- Diseño del sistema
- Implementación (desarrollo)
- Pruebas
- Despliegue
- Mantenimiento

### 🧪 Implicaciones para QA:

- Las pruebas se realizan **después del desarrollo**, lo que puede retrasar la detección de errores.
- No hay iteración entre fases.
- Buena para proyectos con requisitos estables y bien definidos.

---

## 🧭 2. Scrum (Metodología Ágil)

Scrum es un enfoque ágil que trabaja en ciclos iterativos llamados **sprints**. Cada sprint tiene una duración fija (por ejemplo, 2 semanas) y busca entregar una versión funcional del producto.

### 🧑‍🤝‍🧑 Roles en Scrum:
- **Product Owner (PO):** Define y prioriza el backlog, comunmente vamos a ver que este rol está asociado algo más a la parte de negocio, por lo que como QAs es a la persona del equipo que deberemos preguntar todas las dudas relacionadas con "negocio".
- **Scrum Master:** Facilita el proceso Scrum y elimina obstáculos, desde mi experiencia es quien organiza las tareas y tiempos de esta dentro de cada sprint.
- **Equipo de desarrollo o IT:** Incluye desarrolladores y testers. Dentro de este sector estaremos nosotros trabajando codo con codo al equipo de devs, equipo al cual preguntaremos todas nuestras dudas sobre implementación de funcionalidades y cambios.

### 📅 Eventos clave:
- **Sprint Planning:** Planificación de tareas del sprint.
- **Daily Standup:** Reunión diaria de seguimiento.
- **Sprint Review:** Presentación del trabajo realizado.
- **Sprint Retrospective:** Mejora continua del proceso a nivel técnico y como equipo.

### 🧪 Implicaciones para QA:
- Las pruebas se realizan **durante el desarrollo**, no al final.
- Permite feedback rápido y ajuste constante.
- QA participa desde la definición de historias de usuario hasta el final del desarrollo.
- Favorece la automatización y la integración continua.

---

## 📌 Comparación rápida

| Aspecto            | Cascada                           | Scrum (Ágil)                    |
|--------------------|------------------------------------|----------------------------------|
| Flujo              | Lineal                             | Iterativo e incremental         |
| Cambios            | Difíciles de aplicar               | Se adaptan entre sprints        |
| Rol del QA         | Al final del proceso               | Durante todo el proceso         |
| Feedback           | Lento                              | Rápido y frecuente              |
| Entregas           | Al final                           | Parciales en cada sprint        |

---

> 💡 Como QA, es fundamental adaptar nuestras estrategias de pruebas según la metodología del equipo para maximizar el valor del testing en cada fase del desarrollo.
