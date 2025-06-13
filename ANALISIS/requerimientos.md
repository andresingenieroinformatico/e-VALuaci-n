Requerimientos para el Sistema de Evaluación Docente e-Valuacion.

Requerimientos Funcionales

🔧1. Gestión de Usuarios
📌 Registro de Usuarios

Descripción: Los administradores podrán registrar usuarios (docentes, evaluadores, directivos) con roles específicos.

Campos: Nombre, correo electrónico, identificación, rol, contraseña.

Criterios de Aceptación: Todos los campos deben ser completados. El correo debe ser único y válido.

Observaciones: Se generará una contraseña temporal enviada por correo.

📌 Inicio de Sesión

Descripción: Los usuarios podrán acceder al sistema con su correo y contraseña.

Criterios de Aceptación: Autenticación exitosa solo con credenciales válidas. Bloqueo tras 5 intentos fallidos.

Observaciones: Opción de recuperación de contraseña vía correo.

📌 Gestión de Roles

Descripción: El administrador podrá asignar, modificar o eliminar roles de usuario.

Criterios de Aceptación: Los cambios deben reflejarse inmediatamente en el sistema.

🔧2. Gestión de Evaluaciones
📌 Creación de Evaluaciones

Descripción: Los evaluadores podrán crear evaluaciones basadas en plantillas predefinidas.

Campos: Nombre de la evaluación, período, criterios (planeación, intervención, evaluación), ponderación.

Criterios de Aceptación: Todos los criterios deben sumar 100% en ponderación.

📌 Autoevaluación Docente

Descripción: Los docentes podrán completar un cuestionario de autoevaluación.

Criterios de Aceptación: Respuestas guardadas solo tras completar todos los ítems obligatorios.

📌 Evaluación por Pares

Descripción: Los evaluadores (pares, directivos o inspectores) podrán calificar al docente según rúbricas.

Criterios de Aceptación: Las rúbricas deben estar completadas antes de enviar.

📌 Observación de Aula

Descripción: Los evaluadores podrán registrar observaciones de clases mediante un formulario digital.

Campos: Fecha, duración, descripción, evidencias (fotos, videos, documentos, si aplica).

Criterios de Aceptación: Las evidencias deben cumplir con formatos permitidos (PDF, JPG, MP4).

🔧3. Generación de Informes
📌 Informe Individual

Descripción: El sistema generará un informe por docente con resultados de autoevaluación, evaluación de pares y observaciones.

Criterios de Aceptación: El informe debe incluir gráficos comparativos y comentarios cualitativos.

📌 Informe Institucional

Descripción: Los administradores podrán generar informes consolidados por departamento o institución.

Criterios de Aceptación: Los datos deben ser anonimizados para proteger la privacidad.

🔧4. Retroalimentación y Planes de Mejora
📌 Retroalimentación

Descripción: Los evaluadores podrán enviar comentarios al docente tras la evaluación.

Criterios de Aceptación: Los comentarios deben ser obligatorios para cerrar la evaluación.

