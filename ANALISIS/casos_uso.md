### *Caso de uso: Evaluar a un docente*

*Actor principal:* Estudiante

*Sistema:* Sistema de Información de Evaluación Docente (SIED)

---

#### *Objetivo del caso de uso:*

Permitir al estudiante evaluar el desempeño de sus docentes al finalizar el periodo académico.

---

#### *Escenario principal:*

1. El estudiante accede al sistema de evaluación docente a través del portal académico.
2. El sistema solicita autenticación; el estudiante ingresa su usuario y contraseña.
3. El sistema valida las credenciales y muestra el listado de materias y docentes asignados durante el periodo académico.
4. El estudiante selecciona un curso para evaluar.
5. El sistema muestra un formulario estructurado con preguntas sobre el desempeño del docente (claridad al explicar, puntualidad, dominio del tema, etc.).
6. El estudiante responde el formulario de manera anónima y sincera.
7. El estudiante envía la evaluación.
8. El sistema confirma la recepción y guarda la evaluación en la base de datos.
9. El sistema actualiza el estado del curso como "evaluado" para evitar duplicación.
10. El estudiante puede continuar evaluando otros docentes o cerrar sesión.

---

#### *Condiciones previas:*

* El estudiante debe estar matriculado en el periodo vigente.
* El sistema debe tener habilitado el periodo de evaluación.

---

#### *Resultado exitoso:*

El sistema registra correctamente la evaluación del docente por parte del estudiante y garantiza la confidencialidad.