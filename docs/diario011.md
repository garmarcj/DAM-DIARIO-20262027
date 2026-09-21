# 🚀 Diario de clase: jueves, 24 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Jueves, 24 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

## 🧭 Sesión 1. PR - Auditoría de calidad y consolidación v0.6

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Es jueves por la tarde. Concluyen las segundas 8 horas de Programación de la semana. Laia Claramunt proyecta la versión `v0.6` del código base en el repositorio.
* *«Fijaos en el avance: nuestro motor matemático ya está operativo. Hemos aprendido a manipular la memoria, utilizar operadores compuestos, diferenciar la división entera del residuo y forzar la conversión de tipos. Hoy no añadiremos características nuevas; dedicaremos la sesión a auditar, asentar y documentar nuestra versión v0.6 antes de sincronizarla definitivamente con GitHub»*.

### 2. Lista de comprobación técnico de calidad del código para la versión v0.6 (10 min)

Laia repasa en pantalla los criterios obligatorios de calidad que todo código en AzaharTech debe superar:
* **Uso correcto de operadores de asignación:** Verificación de que no se duplican variables innecesariamente (ej. utilizar `+=` o `++` para contadores).
* **Precisión en conversiones de tiempo/distancia:** Comprobación de que la separación de unidades (como horas y minutos) emplea correctamente la división entera (`/`) y el operador residuo (`%`).
* **Protección matemática mediante *casting*:** Auditar que las métricas estadísticas utilizan `(double)` protegiendo la operación antes de que se produzca el truncamiento decimal.
* **Autoformateo de código:** Asegurar que todo el archivo pasa por el formateador del IDE (`Ctrl + Alt + L`) manteniendo la indentación a 4 espacios y que el `Scanner` se cierra correctamente (`teclado.close();`).

### 3. La versión v0.6 del proyecto propio del estudiante (35 min)

* Cada estudiante abre su archivo `pr/src/MiProyecto.java` y `pr/pseudocodigo/MiProyecto.psc`.
* Audita minuciosamente su propio código aplicando la lista de comprobación de calidad expuesta.
* Asegura que los cálculos exclusivos de su dominio (Aventura conversacional, Motor de recomendación, Físicas o Contraseñas) compilan y arrojan resultados exactos en consola, mostrando decimales correctos donde se requiere.
* El docente circula por el aula validando visualmente el autoformateo y resolviendo avisos (warnings) del IDE en cada puesto.

## ⚙️ Sesión 2 (50 min). PR - Cierre del ciclo y versionado

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 4. Cierre formal en Git y sincronización con GitHub (45 min)

* Una vez que el código cumple los estándares de calidad, el estudiante realiza el cierre formal de la semana en su repositorio.
* **Paso 1:** Pulsa el atajo `Ctrl + K` (o el icono verde de Commit) para abrir el panel de control de versiones en IntelliJ.
* **Paso 2:** Marca las casillas de los archivos modificados dentro de la carpeta `pr/`.
* **Paso 3:** Redacta un mensaje de confirmación descriptivo utilizando el estándar de *Conventional Commits*:
  `feat(pr): consolidar version v0.6 con motor matematico, casting y operadores compuestos`
* **Paso 4:** Despliega el botón azul inferior y selecciona **«Commit and Push»**.
* **Paso 5:** En la ventana final, pulsa **Push** para enviar todo su trabajo de la semana a su repositorio remoto.
* El docente verifica en el panel web de GitHub que toda la clase ha sincronizado correctamente los cambios atómicos de sus proyectos y el historial está actualizado.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Código v0.6 auditado con la lista de comprobación técnica.         ║
║ [ ] Verificada la indentación y cierre de recursos (Ctrl + Alt + L).   ║
║ [ ] Cálculos del proyecto propio validados y sin pérdida de precisión. ║
║ [ ] Sincronización exitosa con GitHub mediante Commit and Push.        ║
║ [ ] Semana 2 concluida con el motor matemático integrado.              ║
╚════════════════════════════════════════════════════════════════════════╝