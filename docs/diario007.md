---
title: "Viernes 18 de septiembre de 2026 - Repositorio en GitHub y análisis del reto"
date: 2026-09-18
modules: "Entornos de desarrollo (ED) · Proyecto intermodular (PI)"
duration: "2 horas lectivas (100 minutos)"
layout: page
---

# 🚀 Diario de clase: viernes, 18 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027
**Módulos del día:** Entornos de desarrollo (ED) · Proyecto intermodular (PI)  
**Fecha:** Viernes, 18 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

---

## 🧭 Sesión 1. Metodología Scrum, estructura corporativa y primer repositorio en GitHub (ED)
*Balance de tiempo:* **Docente: 15 min | Estudiante: 35 min**

### 1. Contexto profesional en AzaharTech (5 min)
* Los estudiantes tienen abierto en IntelliJ IDEA el código del caso guía `ControlAccesoQR.java` y su proyecto propio compilados el jueves, junto a la captura `entorno.png` guardada en su carpeta de trabajo.
* Laia Claramunt explica que el código en un ordenador local no tiene validez profesional si no está versionado, protegido y compartido de forma transparente con el cliente y el equipo.
* Presenta el marco de trabajo ágil: en AzaharTech no se usa el modelo en cascada tradicional; se trabaja con Scrum en sprints de 3 semanas, entregando software funcional al final de cada ciclo y utilizando GitHub como canal oficial de entregas.

### 2. Micro-exposición docente: El marco ágil y el repositorio digital (10 min)
* **El marco de trabajo Scrum:**
  * *Sprint:* Ciclo de desarrollo de duración fija (3 semanas en nuestro curso).
  * *Product Backlog:* Lista priorizada con todos los requisitos del cliente.
  * *Sprint Backlog:* Subconjunto de tareas comprometidas para las 3 semanas actuales.
  * *Roles:* Product Owner (representa al cliente), Scrum Master (Laia Claramunt, guía metodológica) y Developers (el equipo de desarrollo).
* **Control de versiones y repositorio remoto:**
  * *Repositorio local:* Base de datos de Git en el disco duro del alumno (`.git/`).
  * *Repositorio remoto en GitHub:* Repositorio en la nube que actúa como buzón oficial de entregas y garantiza la autoría de cada cambio.
* **El archivo `.gitignore`:**
  * Regla de higiene técnica: en Git solo se sube código fuente (`.java`, `.psc`) y documentación (`.md`, `.png`).
  * Los archivos compilados (`.class`), carpetas de salida (`out/`, `target/`) y configuraciones privadas del IDE (`.idea/`) deben quedar estrictamente excluidos.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        EL FLUJO DE TRABAJO EN SCRUM                    │
├──────────────────────────┬─────────────────────────────┬───────────────┤
│ 1. Product Backlog       │ 2. Sprint Backlog           │ 3. Incremento │
├──────────────────────────┼─────────────────────────────┼───────────────┤
│ Lista global de          │ Tareas seleccionadas para   │ Software 100% │
│ requisitos del cliente.  │ las 3 semanas del sprint.   │ funcional.    │
└──────────────────────────┴─────────────────────────────┴───────────────┘
```

### 3. Taller guiado: Creación de carpetas y primer commit visual en IntelliJ (30 min)
*Los estudiantes configuran la estructura corporativa y publican su repositorio sin usar comandos de consola:*

1. **Creación de la jerarquía oficial de carpetas:**
    * En el explorador de archivos o en IntelliJ, crean la estructura universal dentro de su espacio de trabajo:
      ```text
      azahartech/
      └── equipo-alfa/                        <-- Nombre del equipo asignado
          └── apellidos-nombre/               <-- Espacio personal (sin espacios ni acentos)
              ├── README.md                   <-- Portada oficial
              ├── .gitignore                 <-- Archivo de exclusiones
              ├── ed/
              │   └── docs/
              │       └── entorno.png         <-- Mueven aquí la captura del lunes
              ├── pr/
              │   ├── pseudocodigo/
              │   └── src/
              └── pi/
                  └── docs/
      ```
2. **Configuración del archivo `.gitignore`:**
    * Crean el archivo `.gitignore` en la raíz de su espacio personal con las siguientes reglas:
      ```text
      .idea/
      *.iml
      out/
      target/
      *.class
      .DS_Store
      ```
3. **Vinculación con GitHub y primer commit visual:**
    * En IntelliJ, vinculan su cuenta de GitHub desde *Settings -> Version Control -> GitHub*.
    * Inicializan el repositorio local desde el menú superior: *Git -> Create Git Repository...*, seleccionando su carpeta personal.
    * Abren el panel visual de confirmación con **`Ctrl + K`** (o icono verde *Commit* en la barra lateral izquierda).
    * Marcan las casillas de los archivos preparados y escriben el mensaje convencional:  
      `feat: inicializar estructura corporativa oficial y verificar entorno con OpenJDK 21`
    * Publican el proyecto en GitHub desde el menú: *Git -> GitHub -> Share Project on GitHub*, nombrándolo `DAM-AzaharTech-Proyecto-TuNombre` y marcándolo como público.

### 4. Cierre y comprobación en GitHub (5 min)
* Comprobación en el navegador de que el repositorio es accesible, que la imagen `ed/docs/entorno.png` se visualiza correctamente y que el historial muestra el commit con prefijo `feat:`.

---

## ⚙️ Sesión 2. De la idea al reto técnico: Análisis de necesidades, ODS y Sprint Backlog 1 (PI)
*Balance de tiempo:* **Docente: 10 min | Estudiante: 40 min**

### 1. Contexto profesional en AzaharTech (5 min)
* Laia Claramunt reúne al equipo para la sesión de Proyecto intermodular: el espacio para conectar el código con el cliente real y planificar las entregas.
* Mientras en clase se toma como referencia el control de acceso del IES El Caminàs, cada estudiante debe aterrizar los requisitos para **su proyecto elegido de la bolsa de proyectos**.

### 2. Micro-exposición docente: Requisitos, actores, ODS e inteligencia artificial (10 min)
* **Definición del reto:** Delimitar el problema operativo del cliente y justificar por qué la digitalización aporta valor.
* **Mapa de actores:** Identificar usuarios primarios (operarios/alumnos), administradores (gestores) y sistemas externos (pantallas, terminales).
* **Alineación con los ODS:** Conectar la solución con al menos un Objetivo de Desarrollo Sostenible (ej. ODS 9: *Industria, innovación e infraestructura* u ODS 12: *Producción y consumo responsables*).
* **Uso ético y transparente de la IA (Prompt Log):**
    * La IA se utiliza como asistente de análisis y redacción, nunca como sustituto del criterio técnico.
    * Es obligatorio documentar en una tabla las herramientas empleadas, los prompts introducidos y la revisión crítica aplicada por el estudiante.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        EL CAMINO DEL RETO TÉCNICO                      │
├───────────────────┬───────────────────┬────────────────────────────────┤
│ 1. Problema real  │ 2. Mapa actores   │ 3. ODS e IA ética              │
├───────────────────┼───────────────────┼────────────────────────────────┤
│ Necesidad clara   │ Quién interactúa  │ Impacto sostenible y registro  │
│ del cliente.      │ con el software.  │ transparente de prompts.       │
└───────────────────┴───────────────────┴────────────────────────────────┘
```

### 3. Taller guiado: Documento de análisis y creación del Sprint Backlog 1 (20 min)
*Cada estudiante trabaja en su puesto individual en su proyecto elegido:*

1. **Creación de carpetas de documentación y gestión:**
    * Dentro de `pi/`, crean las carpetas `pi/docs/` y `pi/backlog/`.
2. **Redacción del documento de análisis (`pi/docs/analisis-reto.md`):**
    * Crean el archivo con los siguientes apartados:
        * *Contexto y justificación:* Problema del cliente y solución propuesta.
        * *Alineación ODS:* Objetivo seleccionado y justificación en dos líneas.
        * *Mapa de actores:* Tabla con perfiles de usuario y permisos en el sistema.
        * *Prompt Log:* Tabla con la herramienta de IA consultada, prompt utilizado y ajuste personal aplicado.
3. **Creación del cuadro de tareas inicial (`pi/backlog/sprint1-backlog.md`):**
    * Crean el archivo con las tareas del Sprint 1 (14 sep – 2 oct) en estado pendiente (`- [ ]`):
      ```markdown
      # Sprint Backlog 1 — [Nombre de Tu Proyecto Propio]
      **Periodo:** 14 de septiembre – 2 de octubre de 2026  
      **Responsable:** [Tu Nombre]  
 
      ## 📋 Cuadro de mando de tareas
 
      ### Módulo: Proyecto intermodular (PI)
      - [x] T-PI-01: Redactar análisis de necesidades y mapa de actores (`pi/docs/analisis-reto.md`)
      - [x] T-PI-02: Registrar el uso ético de IA (*Prompt Log*)
      - [x] T-PI-03: Crear el Sprint Backlog 1 inicial
      - [ ] T-PI-04: Elaborar diagrama de bloques funcional y viabilidad técnica
      - [ ] T-PI-05: Consolidar dossier técnico y guion de demo v0.1
 
      ### Módulo: Entornos de desarrollo (ED)
      - [x] T-ED-01: Instalar y verificar OpenJDK 21 e IntelliJ IDEA (`ed/docs/entorno.png`)
      - [x] T-ED-02: Crear estructura corporativa oficial y repositorio en GitHub
      - [ ] T-ED-03: Elaborar memoria técnica de marco Scrum (`ed/docs/marco-scrum.md`)
      - [ ] T-ED-04: Auditar limpieza de repositorio y publicar tag `v0.1.0-sprint1`
 
      ### Módulo: Programación (PR)
      - [x] T-PR-01: Declarar variables primitivas y lectura con Scanner (`pr/src/MiProyecto.java`)
      - [ ] T-PR-02: Implementar operadores aritméticos, módulo y casting
      - [ ] T-PR-03: Integrar constantes `final` y salida formateada con `printf`
      ```

### 4. Guardado y sincronización visual en IntelliJ (5 min)
* Abren el panel de Commit con **`Ctrl + K`**, seleccionan la carpeta `pi/`, escriben el mensaje:  
  `docs(pi): definir analisis del reto del proyecto propio y sprint backlog 1`  
  y pulsan **«Commit and Push»**.

---

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendido el funcionamiento de Scrum y el ciclo de sprint.       ║
║ [ ] Creada la jerarquía corporativa azahartech/equipo-XX/alumno/.      ║
║ [ ] Configurado el archivo .gitignore con exclusiones de binarios.     ║
║ [ ] Repositorio público publicado en GitHub con la captura de entorno. ║
║ [ ] Redactado el análisis del reto y el mapa de actores en pi/docs/.   ║
║ [ ] Registrado el uso ético de IA en la tabla de Prompt Log.           ║
║ [ ] Inicializado el Sprint Backlog 1 con las tareas de los 3 módulos.  ║
╚════════════════════════════════════════════════════════════════════════╝
```