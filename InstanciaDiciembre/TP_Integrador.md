### **Trabajo Práctico: Bases de Datos y SQL**

#### **Objetivo**
Desarrollar una base de datos relacional mediante comandos DDL y realizar consultas utilizando comandos DML con un enfoque en relaciones entre tablas y consultas avanzadas.

---

### **Parte 1: Creación de la Base de Datos**
1. **Crea una base de datos llamada `Universidad`.**
   - Comando: `CREATE DATABASE Universidad;`

2. **Dentro de la base de datos, crea las siguientes tablas utilizando DDL:**

   **Tabla `Estudiantes`:**
   - `id_estudiante` (INT, PRIMARY KEY, AUTOINCREMENT)
   - `nombre` (VARCHAR(50), NOT NULL)
   - `apellido` (VARCHAR(50), NOT NULL)
   - `edad` (INT, NOT NULL)
   - `carrera` (VARCHAR(50))

   **Tabla `Cursos`:**
   - `id_curso` (INT, PRIMARY KEY, AUTOINCREMENT)
   - `nombre_curso` (VARCHAR(100), NOT NULL)
   - `creditos` (INT, NOT NULL)

   **Tabla `Inscripciones`:**
   - `id_inscripcion` (INT, PRIMARY KEY, AUTOINCREMENT)
   - `id_estudiante` (INT, FOREIGN KEY que referencia a `Estudiantes.id_estudiante`)
   - `id_curso` (INT, FOREIGN KEY que referencia a `Cursos.id_curso`)
   - `fecha_inscripcion` (DATE, NOT NULL)

3. **Inserta datos en cada tabla:**
   Proporciona al menos 5 registros para las tablas `Estudiantes` y `Cursos`, y al menos 8 registros para `Inscripciones`.

---

### **Parte 2: Consultas SQL**

#### **Consultas de DML:**

1. **Inserta un nuevo estudiante en la tabla `Estudiantes`.**
   - Datos: `nombre = 'Juan', apellido = 'Pérez', edad = 22, carrera = 'Ingeniería en Sistemas'`.

2. **Actualiza el nombre del curso con `id_curso = 2` a `'Matemáticas Avanzadas'`.**

3. **Elimina la inscripción del estudiante con `id_estudiante = 3` en el curso con `id_curso = 1`.**

---

#### **Consultas Básicas con SELECT:**

4. **Obtén una lista de todos los estudiantes inscritos en el curso `'Programación Avanzada'`.**

5. **Consulta los nombres y apellidos de los estudiantes cuya edad sea mayor o igual a 20.**

6. **Muestra todos los cursos con más de 3 créditos, ordenados alfabéticamente.**

---

#### **Consultas con JOINS:**

7. **Realiza una consulta que muestre el nombre y apellido de cada estudiante junto con el nombre de los cursos en los que está inscrito.**
   - Utiliza un **INNER JOIN**.

8. **Haz una consulta para listar los estudiantes que no tienen inscripciones.**
   - Utiliza un **LEFT JOIN**.

---

#### **Consultas Multitabla:**

9. **Encuentra el nombre de los estudiantes que están inscritos en más de un curso.**
   - Utiliza **GROUP BY** y **HAVING**.

10. **Genera un reporte que muestre por cada curso el número total de estudiantes inscritos.**
    - Muestra `nombre_curso` y `cantidad_estudiantes`.

---

#### **Entrega**
- Código SQL utilizado para crear las tablas y para las consultas.
- Capturas de pantalla de las consultas realizadas en el workbench de MySql.
---
