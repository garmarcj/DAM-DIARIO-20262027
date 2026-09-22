# 🚀 Diario de clase: viernes, 25 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulos:** Entornos de desarrollo (ED) + Proyecto Intermodular (PI)  
**Fecha:** Viernes, 25 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

## 🧭 Sesión 1 (50 min). ED - El estándar Markdown en la ingeniería del software

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Es viernes. El código del motor matemático de la semana está validado, pero el repositorio de GitHub carece de portadas o explicaciones legibles. Alba Torres muestra un archivo `.txt` con los requisitos del IES El Caminàs que resulta confuso, y luego intenta subir un documento binario de Microsoft Word que Git no es capaz de versionar ni comparar línea a línea.
* Laia Claramunt interviene: *«Los ingenieros de software no utilizamos procesadores de texto pesados y opacos para documentar los repositorios. Utilizamos **Markdown**, un estándar de texto plano que permite aplicar formato semántico y estructural, y que además es renderizado de forma nativa y espectacular por GitHub. Hoy redactaremos nuestra primera memoria técnica y el panel de control del proyecto utilizando esta sintaxis»*.

### 2. Sintaxis esencial de Markdown para documentación de software (10 min)

* **Elementos básicos:** Uso del símbolo `#` para estructurar la jerarquía de encabezados, `**` para **negritas**, y el guion `-` para crear listas de control (*checklists*).
* **Tablas en Markdown:** Cómo construir cuadrículas combinando *pipes* (`|`) y guiones (`-`) para documentar perfiles de usuario, casos de prueba o diccionarios de variables.
* **Bloques de código estructurado:** El uso de la triple comilla invertida junto al nombre del lenguaje (ej. `java`, `text`) para insertar fragmentos de código fuente formateados y legibles.

### 3. Laboratorio práctico guiado: Redacción de ED-2 y panel README (35 min)

* **Paso 1. Redacción de la memoria técnica Scrum:** Cada estudiante crea el archivo `ed/docs/marco-scrum.md` (Entregable ED-2). En él redacta y documenta los conceptos básicos de la metodología ágil y cómo los está aplicando a su proyecto.
* **Paso 2. Transformación del README.md en panel de control:** Modificación del archivo raíz del repositorio (`README.md`) para incluir la portada del proyecto, el escudo de AzaharTech y una tabla descriptiva con la estructura de las carpetas.
* **Paso 3. Confirmación atómica y sincronización con GitHub:** El estudiante abre el panel de control de versiones (`Ctrl + K`), redacta un mensaje bajo el estándar *Conventional Commits* (ej. `docs(ed): redactar memoria tecnica scrum y actualizar panel readme`) y sube los cambios mediante *Commit and Push*.

## ⚙️ Sesión 2 (50 min). PI - Arquitectura de bloques y viabilidad

**Balance de tiempo:** Docente: 20 min | Estudiante: 30 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: El equipo inicia la sesión de Proyecto Intermodular. Laia proyecta en la pantalla táctil el esquema técnico del caso del IES El Caminàs, compuesto exclusivamente por tres grandes bloques conectados por flechas: captura (cámara), procesamiento (algoritmo Java) y salida (pantalla del vestíbulo).
* *«La semana pasada analizamos el problema y los actores. Pero un cliente no puede financiar una idea en el aire: necesita ver el **plano arquitectónico de la solución y tener la certeza de que es técnicamente viable**. Hoy diseñaréis el Diagrama de Bloques Funcional de vuestro proyecto propio, evaluaréis su viabilidad contrastando fuentes oficiales de información y actualizaréis el Sprint Backlog para afrontar la recta final»*.

### 2. Fundamento metodológico: arquitectura funcional y contraste de fuentes (15 min)

* **A. El diagrama de bloques funcional (Modelo IPO):** Representación visual de muy alto nivel. Permite entender el flujo sin leer código:
    * **Entradas:** Qué datos brutos se capturan por consola.
    * **Procesamiento:** Qué cálculos o lógica de negocio en Java los transforman.
    * **Salidas:** Qué información útil entrega el sistema por pantalla.
* **B. Estudio de viabilidad técnica:** Certificar que la solución es realizable. Evaluación del entorno de software exigido (Java OpenJDK 21 LTS e IntelliJ), requisitos mínimos de hardware del cliente (ej. mínimo 2 GB de RAM) y gestión de las restricciones operativas del Sprint 1 (procesamiento en memoria sin bases de datos relacionales).
* **C. Búsqueda y contraste de fuentes técnicas oficiales:** La regla de descartar foros anónimos o tutoriales obsoletos y acudir a fuentes primarias fiables (documentación oficial de Oracle Java SE 21).

### 3. Laboratorio práctico: Modelado de bloques y viabilidad técnica (30 min)

* **Paso 1. Redacción del documento de viabilidad y arquitectura:** El estudiante navega a `pi/docs/` y crea el archivo `viabilidad-tecnica.md`. Utilizando la sintaxis Markdown aprendida en la sesión anterior, dibuja un diagrama funcional mediante bloques de texto e incorpora su estudio de viabilidad.
* **Paso 2. Actualización y seguimiento del Sprint Backlog 1:** Modificación de la lista de tareas `pi/backlog/sprint1-backlog.md` para marcar con una `[x]` los hitos de programación y entornos de desarrollo conquistados a lo largo de esta segunda semana.
* **Paso 3. Confirmación y sincronización en GitHub:** Commit final empleando un prefijo convencional (ej. `docs(pi): elaborar estudio de viabilidad tecnica y actualizar sprint backlog 1`) y envío mediante *Push*.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Dominada la sintaxis básica y creación de tablas en Markdown.      ║
║ [ ] Memoria Scrum (ED-2) y archivo README redactados y subidos (ED).   ║
║ [ ] Diagrama funcional (IPO) y viabilidad técnica completados (PI).    ║
║ [ ] Actualizado el Sprint Backlog 1 con el progreso de la Semana 2.    ║
║ [ ] Semana 2 cerrada con sincronización exitosa de toda la doc técnica.║
╚════════════════════════════════════════════════════════════════════════╝
```