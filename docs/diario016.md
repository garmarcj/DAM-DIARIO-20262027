# 🚀 Diario de clase: jueves, 1 de octubre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Jueves, 1 de octubre de 2026  
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1. PR - Documentación técnica y versión 1.0

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Es jueves por la tarde. Concluyen las sesiones de programación del Sprint 1. Laia Claramunt y Alba Torres proyectan el código final en pantalla.
* *«Hemos llegado al final de nuestra primera iteración. Nuestro sistema de control de acceso por QR ya no es un prototipo, sino una aplicación de consola sólida. Pero antes de dar por cerrada esta versión (v1.0), necesitamos auditar el código. Un buen ingeniero no solo escribe código que la máquina compila, sino código estructurado y documentado que otros humanos pueden leer y mantener. Hoy finalizaremos nuestra obra»*.

### 2. Fundamento teórico: documentación técnica y autoformateo (10 min)

* **Documentación técnica con Javadoc:** Explicación de cómo utilizar los comentarios de bloque estructurados `/** ... */` justo encima de la cabecera de la clase y del método principal (`main`). Uso de etiquetas clave como `@author`, `@version` y la descripción del dominio.
* **Comentarios de línea:** Uso prudente de `//` para explicar "el porqué" (reglas de negocio) y no "el qué" (que debería ser evidente si las variables tienen nombres descriptivos).
* **Autoformateo del IDE:** Recordatorio de la regla de oro en AzaharTech: pulsar `Ctrl + Alt + L` en IntelliJ IDEA para garantizar que la indentación a 4 espacios y los saltos de línea sean homogéneos en todo el archivo.

### 3. El código definitivo del Sprint 1: ControlAccesoQR v1.0 (35 min)

Actualización conjunta a `ControlAccesoQR v1.0`. Los estudiantes abren el archivo maestro por última vez en este sprint:

* **Paso A. Revisión en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v1.0`)**:
    * Se insertan comentarios algorítmicos (`//`) al inicio del archivo resumiendo el flujo secuencial y asegurando la limpieza visual de las definiciones.

* **Paso B. Versión final en Java (`pr/src/ControlAccesoQR.java - v1.0`)**:
    * Inserción de la cabecera oficial Javadoc documentando el proyecto del IES El Caminàs.
    * Ejecución del atajo de formateo automático.
    * Revisión general del flujo completo: desde las constantes, captura con limpieza de buffer, aritmética, hasta la inyección de salida con `printf` y secuencias de escape.

## ⚙️ Sesión 2 (50 min). PR - Auditoría final del proyecto propio

**Balance de tiempo:** Docente: 10 min | Estudiante: 40 min

### 1. Trabajo del estudiante: la versión v1.0 de su proyecto propio (40 min)

* Cada estudiante abre los archivos `.psc` y `.java` correspondientes a su proyecto y prepara la *Release Candidate* `v1.0`.
* Aplica obligatoriamente la **lista de comprobación de calidad del código**:
    * **Cabecera Javadoc:** Incluir la descripción (Aventura, Motor de recomendación, Físicas o Contraseñas), el autor (nombre del alumno) y fijar `@version 1.0`.
    * **Autoformateo:** Pulsar `Ctrl + Alt + L` para eliminar tabulaciones irregulares o espacios en blanco innecesarios.
    * **Constantes e inmutabilidad:** Verificar que todos los "números mágicos" han sido transformados a `final` en formato *SNAKE_CASE*.
    * **Cierre de recursos:** Comprobar que `teclado.close()` está presente al final del programa sin lanzar advertencias de fuga de memoria (*resource leaks*).
* El docente circula auditando personalmente el monitor de cada estudiante para conceder el "visto bueno" técnico y aprobar su versión 1.0.

### 2. Cierre de la sesión y del Sprint de Programación (10 min)

* Comprobación definitiva ejecutando el proyecto propio en consola (`Ctrl + Shift + F10`) e introduciendo datos críticos reales.
* Mensaje final de cierre: el código fundacional de los cuatro proyectos ya es robusto y se encuentra listo para el inminente Sprint 2, donde la aplicación dejará de ser estrictamente secuencial y aprenderá a "tomar decisiones".

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendida la importancia de documentar cabeceras con Javadoc.    ║
║ [ ] Dominado el atajo de autoformateo de IntelliJ (Ctrl + Alt + L).    ║
║ [ ] Finalizado el código fuente de ControlAccesoQR en su versión v1.0. ║
║ [ ] Auditada y documentada la versión v1.0 del proyecto propio.        ║
║ [ ] Cierre técnico superado: el software secuencial está terminado.    ║
╚════════════════════════════════════════════════════════════════════════╝
```
```