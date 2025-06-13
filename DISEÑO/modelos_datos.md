# Modelo de Datos - Sistema e-VALuacion

Este el siguiente documento describe el modelo de datos relacional propuesto para la aplicación e-VALuacion, destinado a la evaluar de manera estructurada a docentes por parte de estudiantes mediante formularios personalizados.

## Descripción General

El sistema del modelo de datos se basa en un enfoque entidad-relación (ER) que garantiza integridad referencial, escalabilidad y trazabilidad en las evaluaciones docentes. Se han definido las siguientes entidades clave:

---

## Entidades y Atributos

### 1. Docente

| Atributo         | Tipo de Dato | Clave | Descripción                       |
|------------------|--------------|-------|-----------------------------------|
| id_docente       | INT          | PK    | Identificador único del docente   |
| nombre           | VARCHAR(50)  |       | Nombre del docente                |
| apellidos        | VARCHAR(50)  |       | Apellidos del docente             |
| identificacion   | VARCHAR(20)  |       | Documento de identidad            |
| area             | VARCHAR(50)  |       | Área o departamento académico     |

---

### 2. Estudiante

| Atributo         | Tipo de Dato | Clave | Descripción                         |
|------------------|--------------|-------|-------------------------------------|
| id_estudiante    | INT          | PK    | Identificador único del estudiante  |
| nombre           | VARCHAR(50)  |       | Nombre del estudiante               |
| curso            | VARCHAR(30)  |       | Curso o grupo académico actual      |

---

### 3. Formulario

| Atributo         | Tipo de Dato | Clave | Descripción                              |
|------------------|--------------|-------|------------------------------------------|
| id_formulario    | INT          | PK    | Identificador único del formulario       |
| nombre_formulario| VARCHAR(100) |       | Título o nombre del formulario           |
| fecha_creacion   | DATE         |       | Fecha de creación del formulario         |

---

### 4. Criterio

| Atributo         | Tipo de Dato | Clave | Descripción                                       |
|------------------|--------------|-------|---------------------------------------------------|
| id_criterio      | INT          | PK    | Identificador del criterio                        |
| descripcion      | TEXT         |       | Descripción detallada del criterio evaluativo     |
| ponderacion      | DECIMAL(5,2) |       | Valor porcentual del criterio                     |
| id_formulario    | INT          | FK    | Relación al formulario correspondiente            |

---

### 5. Evaluación

| Atributo         | Tipo de Dato | Clave | Descripción                                        |
|------------------|--------------|-------|----------------------------------------------------|
| id_evaluacion    | INT          | PK    | Identificador de la evaluación                     |
| id_docente       | INT          | FK    | Docente evaluado                                   |
| id_estudiante    | INT          | FK    | Estudiante que realiza la evaluación               |
| id_formulario    | INT          | FK    | Formulario utilizado para la evaluación            |
| fecha            | DATE         |       | Fecha en la que se realiza la evaluación           |
| puntaje_total    | DECIMAL(5,2) |       | Puntaje agregado obtenido en la evaluación         |
| observaciones    | TEXT         |       | Comentarios adicionales del estudiante             |

---

## Relaciones Entre Entidades

- Un **Docente** puede ser evaluado múltiples veces.
- Un **Estudiante** puede realizar múltiples evaluaciones.
- Un **Formulario** puede tener múltiples **Criterios**.
- Una **Evaluación** está asociada a un **Formulario**, un **Docente** y un **Estudiante**.
- Cada **Criterio** pertenece a un único **Formulario**.

---

## Consideraciones Técnicas

- Las claves primarias (PK) son autoincrementales (`AUTO_INCREMENT` en MySQL).
- Todas las claves foráneas (FK) deben tener restricciones `ON DELETE CASCADE` o `SET NULL` según el caso.
- Se recomienda normalización hasta la 3NF para evitar redundancia de datos.
- Los valores de `ponderacion` deben sumar 100 por formulario para mantener coherencia en la evaluación.

---

## Diagrama Relacional (referencia)

> Para complementar este documento, se adjunta un diagrama ER en el archivo `diagramas.md`.

