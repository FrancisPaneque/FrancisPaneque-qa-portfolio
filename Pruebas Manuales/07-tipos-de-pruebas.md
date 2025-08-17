# 🧪 Tipos de Pruebas Funcionales y No Funcionales

En QA, las pruebas se dividen principalmente en **funcionales** y **no funcionales**.  
Ambas son esenciales para garantizar que el software no solo cumpla con lo que debe hacer, sino que también lo haga de forma eficiente, segura y fiable.

---

## ⚙️ Pruebas Funcionales
Evalúan **qué hace** el sistema y si cumple los requisitos definidos.  
Se basan en entradas, salidas y comportamiento esperado.

**Ejemplos comunes:**

- **Smoke Testing**  
  Pruebas rápidas para verificar que las funciones críticas están operativas.  
  *Ejemplo:* Probar login, registro y acceso al dashboard tras una nueva release.

- **Sanity Testing**  
  Verifica una funcionalidad o bug fix específico antes de hacer pruebas más extensas.  
  *Ejemplo:* Validar que un bug corregido en transferencias se haya solucionado.

- **Pruebas de Regresión**  
  Confirma que cambios o correcciones no afectan funcionalidades existentes.  
  *Ejemplo:* Revisar pagos y transferencias después de modificar el login.

- **Pruebas de Integración**  
  Comprueban que los módulos o componentes funcionan correctamente juntos.  
  *Ejemplo:* Validar que el módulo de login se comunica bien con la base de datos y el dashboard.

- **Pruebas de Sistema**  
  Evalúan el sistema completo como un todo, incluyendo hardware y software.  
  *Ejemplo:* Probar todo el flujo de operaciones bancarias en entorno staging.

- **Pruebas de Caja Negra**  
  Se centran en la funcionalidad sin conocer el código interno.  
  *Ejemplo:* Validar que introducir un importe negativo muestra el error esperado.

- **Pruebas de Caja Blanca**  
  Se centran en la lógica interna del código.  
  *Ejemplo:* Verificar la cobertura de código en las funciones de validación.

- **UAT (User Acceptance Testing)**  
  Validación hecha por el cliente o usuario final antes de ir a producción.  
  *Ejemplo:* Cliente del banco prueba la nueva función de pagos recurrentes.

- **Pruebas de Compatibilidad**  
  Confirman que la app funciona en distintos dispositivos, navegadores o sistemas operativos.  
  *Ejemplo:* Validar que Parabank funciona igual en Chrome, Firefox y Safari.

---

## 🛡️ Pruebas No Funcionales
Evalúan **cómo funciona** el sistema: rendimiento, seguridad, experiencia de usuario, entre otros.

**Ejemplos comunes:**

- **Pruebas de Performance**  
  Miden tiempo de respuesta, estabilidad y uso de recursos.  
  *Ejemplo:* Verificar que 500 usuarios simultáneos pueden hacer login en menos de 2 segundos.

- **Pruebas de Carga (Load Testing)**  
  Evalúan rendimiento bajo una carga esperada.  
  *Ejemplo:* Simular operaciones de pago de 1000 clientes en hora punta.

- **Pruebas de Estrés (Stress Testing)**  
  Evalúan el comportamiento bajo cargas extremas o por encima de lo esperado.  
  *Ejemplo:* Forzar 10.000 transacciones simultáneas para medir el límite del sistema.

- **Pruebas de Seguridad**  
  Detectan vulnerabilidades, accesos no autorizados y fallos de cifrado.  
  *Ejemplo:* Intentar acceder a cuentas sin autenticación.

- **Pruebas de Usabilidad**  
  Miden la facilidad de uso y experiencia del usuario.  
  *Ejemplo:* Comprobar si un cliente puede realizar una transferencia en menos de 3 pasos.

- **Pruebas de Recuperación (Recovery Testing)**  
  Validan la capacidad del sistema para recuperarse tras fallos.  
  *Ejemplo:* Simular una caída de servidor y comprobar que la base de datos no se corrompe.

- **Pruebas de Escalabilidad**  
  Evalúan si el sistema puede crecer en usuarios, datos o transacciones sin perder rendimiento.  
  *Ejemplo:* Medir si el sistema sigue respondiendo bien al duplicar el número de usuarios.

- **Pruebas de Mantenibilidad**  
  Evalúan la facilidad para actualizar y corregir el sistema.  
  *Ejemplo:* Validar que aplicar un cambio en la interfaz no rompe la arquitectura.

---

## 💡 Buenas prácticas
- Combinar pruebas funcionales y no funcionales para una cobertura completa.  
- Documentar objetivo, alcance, datos y resultados para cada tipo de prueba.  
- Priorizar en función de riesgos, criticidad y plazos de entrega.  
- Usar entornos representativos para obtener resultados realistas.

---

📌 Documento elaborado por **Francis Paneque – QA Specialist**  
✉️ francisco.j.paneque@gmail.com | 🌐 [LinkedIn](https://www.linkedin.com/in/francis-paneque-21092a252)
