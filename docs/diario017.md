# 🚀 Diario de clase: viernes, 2 de octubre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulos:** Entornos de desarrollo (ED) + Proyecto Intermodular (PI)  
**Fecha:** Viernes, 2 de octubre de 2026  
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1 (50 min). ED - Versionado semántico y etiquetas (TAGS)

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Es viernes por la mañana en AzaharTech. Laia Claramunt y Alba Torres se reúnen con el equipo. El código del sistema de control de acceso para el IES El Caminàs (`v1.0`) ya está purgado, autoformateado y documentado con Javadoc en la rama principal.
* *«Tener el código terminado no basta. En un proyecto profesional con cientos de *commits*, el cliente no sabe qué momento exacto del historial corresponde a la versión final entregable. Hoy aprenderemos a "congelar" y firmar el historial mediante **Etiquetas (Git Tags)** y aplicaremos el estándar mundial de Versionado Semántico para empaquetar nuestra primera gran entrega»*.

### 2. Fundamentos del versionado semántico y las etiquetas en Git (10 min)

* **¿Qué es un Git Tag y en qué se diferencia de una rama?** Mientras que una rama es móvil y avanza con cada nuevo *commit*, un *Tag* es una fotografía inmutable de un *commit* concreto. Es el equivalente a precintar una caja de software.
* **El estándar de versionado semántico (SemVer 2.0.0):** Cómo interpretar y asignar versiones siguiendo el formato `Mayor.Menor.Parche` (ej. `v1.0.0` o `v0.1.0`). Explicación de los sufijos de prelanzamiento (ej. `-sprint1`).

### 3. Laboratorio práctico guiado: Firma de la Release y entrega oficial (35 min)

* **Paso 1. Cierre del panel README.md:** Cada estudiante edita la portada de su proyecto en la raíz del repositorio indicando que el Sprint 1 ha finalizado con éxito.
* **Paso 2. Creación de la etiqueta de versión formal:** Utilizando el panel Git de IntelliJ IDEA (`Log`), el estudiante localiza el último *commit* válido de la semana y crea una nueva etiqueta (*New Tag*) con el nombre corporativo obligatorio: `v0.1.0-sprint1`.
* **Paso 3. Publicación del Tag en el servidor remoto (Push Tags):** A diferencia de un push normal, los *tags* no viajan por defecto a GitHub. El alumno ejecuta un Push especial marcando la casilla *Push Tags* en el IDE.
* **Paso 4. Verificación final en GitHub:** Comprobación en la interfaz web de GitHub de que la sección *Releases/Tags* muestra el código empaquetado, dejando la evidencia oficial (RA4.h) lista para la calificación.

## ⚙️ Sesión 2 (50 min). PI - Aspectos formales y técnica de comunicación oral

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Laia Claramunt proyecta la etiqueta de GitHub recién creada. *«Equipo, el software está firmado. Pero en la vida profesional, el código no se defiende solo. El cliente del IES El Caminàs no va a leerse doscientas líneas de Java; va a valorar nuestra capacidad para documentar el producto y comunicar su valor en una demostración en vivo de tres minutos. Hoy redactaremos el Dossier Técnico y prepararemos la **Sprint Review**»*.

### 2. Calidad documental y comunicación técnica (10 min)

* **Aspectos formales del dossier técnico:** La documentación final debe tener estructura lógica, normas de estilo impersonales (*«se implementa»*, *«el sistema calcula»*), ausencia de faltas y un registro de IA (*Prompt Log*) transparente.
* **Técnicas de comunicación oral y defensa ante el cliente:**
    * *The 3-Minute Demo*: Estructura de impacto.
        * **Minuto 1:** Presentar al cliente y el problema.
        * **Minuto 2:** Demostración en vivo en la consola de IntelliJ ejecutando datos reales.
        * **Minuto 3:** Muestra del código fuente, arquitectura (diagrama IPO) y validación del Tag en GitHub.

### 3. Laboratorio práctico guiado: Consolidación documental y ensayo (35 min)

* **Paso 1. Creación del dossier técnico:** El estudiante crea `pi/docs/dossier-tecnico-sprint1.md` agrupando el análisis de actores, el diagrama de bloques, la viabilidad técnica y el registro de IA.
* **Paso 2. Cierre definitivo del Sprint Backlog:** Acceso a `pi/backlog/sprint1-backlog.md` para marcar el 100% de las tareas de PR, ED y PI con el check de completado `[x]`.
* **Paso 3. Preparación del guion de la demo técnica:** Redacción final de una escaleta de 3 minutos (Minutaje de la demostración) al final del dossier.
* **Paso 4. Commit final y sincronización en GitHub:** Mensaje convencional (ej. `docs(pi): consolidar dossier tecnico final del sprint 1 y cerrar backlog al 100%`) y Push final.

## 📊 Estado al cierre de la jornada y del Sprint 1

```text
╔════════════════════════════════════════════════════════════════════════╗
║                   ESTADO AL CIERRE DEL SPRINT 1                        ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendido el Versionado Semántico (SemVer) y los Git Tags (ED).  ║
║ [ ] Repositorio firmado en GitHub con la etiqueta v0.1.0-sprint1.      ║
║ [ ] Dossier técnico PI consolidado: actores, bloques y viabilidad.     ║
║ [ ] Sprint Backlog 1 auditado y marcado al 100 % de finalización.      ║
║ [ ] Guion estructurado (3 minutos) preparado para la Sprint Review.    ║
║ [ ] ¡HITOS DEL SPRINT 1 ALCANZADOS! Fin de la programación secuencial. ║
╚════════════════════════════════════════════════════════════════════════╝
```