# 📊 Modelo de Datos: e-VALuacion

Sistema de evaluación docente que permite registrar, gestionar y analizar evaluaciones de docentes en diferentes modalidades.

---

## 🧑‍🏫 Entidad: Docentes

| Campo         | Tipo de Dato | Descripción                     |
|---------------|--------------|---------------------------------|
| IdDocente     | Entero (PK)  | Identificador único del docente |
| Nombres       | Texto        | Nombres del docente             |
| Apellidos     | Texto        | Apellidos del docente           |
| Correo        | Texto        | Correo institucional            |
| Área          | Texto        | Área académica                  |
| Facultad      | Texto        | Facultad a la que pertenece     |
| FechaIngreso  | Fecha        | Fecha en que ingresó            |

---

## 📝 Entidad: Evaluaciones

| Campo          | Tipo de Dato | Descripción                                  |
|----------------|--------------|----------------------------------------------|
| IdEvaluacion   | Entero (PK)  | Identificador único de la evaluación         |
| IdDocente      | Entero (FK)  | Relación con el docente evaluado             |
| Fecha          | Fecha        | Fecha de realización de la evaluación        |
| Periodo        | Texto        | Periodo académico (ej. 2025-1)               |
| TipoEvaluacion | Texto        | Tipo (Autoevaluación, Pares, Estudiantes)    |

---

## 🎯 Entidad: Criterios

| Campo        | Tipo de Dato | Descripción                           |
|--------------|--------------|---------------------------------------|
| IdCriterio   | Entero (PK)  | Identificador del criterio            |
| NombreCriterio | Texto      | Nombre del criterio evaluado          |
| Descripción  | Texto        | Detalles del criterio                 |

---

## 📈 Entidad: Resultados

| Campo         | Tipo de Dato | Descripción                                     |
|---------------|--------------|-------------------------------------------------|
| IdResultado   | Entero (PK)  | Identificador del resultado                     |
| IdEvaluacion  | Entero (FK)  | Relación con la evaluación                      |
| IdCriterio    | Entero (FK)  | Relación con el criterio evaluado              |
| Calificación  | Decimal (1-5)| Nota obtenida                                   |
| Observaciones | Texto        | Comentarios o retroalimentación del evaluador  |

---

## 🔐 Entidad: Usuarios

| Campo      | Tipo de Dato | Descripción                            |
|------------|--------------|----------------------------------------|
| IdUsuario  | Entero (PK)  | Identificador del usuario              |
| Usuario    | Texto        | Nombre de usuario                      |
| Contraseña | Texto        | Clave encriptada                       |
| Rol        | Texto        | Tipo de usuario (Admin, Coordinador)  |

---

## 🔗 Relaciones Entre Entidades

- Un *Docente* puede tener muchas *Evaluaciones*
- Cada *Evaluación* evalúa múltiples *Criterios* mediante *Resultados*
- Un *Resultado* relaciona una *Evaluación* y un *Criterio*
- *Usuarios* administran el sistema y gestionan datos

---

## 🧾 Ejemplo de Evaluación Registrada

*Docente:* María López  
*Área:* Ciencias Naturales  
*Correo:* maria.lopez@universidad.edu.co  
*Tipo Evaluación:* Estudiantes  
*Fecha:* 01/06/2025  
*Criterio Evaluado:* Planeación  
*Calificación:* 4.5  
*Observaciones:* Excelente organización de los contenidos.

---

✅ Este modelo puede implementarse en sistemas como *MySQL, **Access* o frameworks backend como *Django* o *Laravel*.