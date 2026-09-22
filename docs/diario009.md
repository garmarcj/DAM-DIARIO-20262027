# 🚀 Diario de clase: martes, 22 de septiembre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Martes, 22 de septiembre de 2026  
**Duración:** 2 horas lectivas (100 min)

## 🧭 Sesión 1. PR - La división entera frente al operador residuo (%)

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Laia Claramunt revisa el cálculo de tiempos implementado en la semana anterior. *«Actualmente el terminal calcula la estancia en minutos totales, por ejemplo, 135 minutos. Sin embargo, el equipo directivo del IES El Caminàs prefiere que los informes de acceso muestren un formato más natural y legible: horas y minutos (2 horas y 15 minutos).»*
* Pau Ferrer sugiere dividir los minutos entre 60. Alba Torres interviene para aclarar un comportamiento clave de Java: al dividir dos números enteros se pierden los decimales. Esto, que parece un error, es la herramienta perfecta para obtener las horas. Para extraer los minutos sobrantes, utilizaremos el operador residuo (`%`).

### 2. La división entera frente al operador residuo (%) (10 min)

* **División entera (`/`)**: Explicación de cómo funciona el motor matemático de Java cuando ambos operandos son enteros (`int`). La operación `135 / 60` no devuelve `2.25`, sino `2`. El compilador trunca la parte decimal.
* **Operador módulo o residuo (`%`)**: Explicación de su funcionamiento al devolver el resto de una división entera. Así, `135 % 60` devuelve `15`.
* Este tándem matemático (`/` y `%`) es el estándar en la industria del software para realizar conversiones de unidades de tiempo, distancias y divisas.

### 3. Evolución a ControlAccesoQR v0.5 (35 min)

Actualización conjunta a `ControlAccesoQR v0.5`. Los estudiantes abren el archivo maestro y añaden la descomposición matemática del tiempo de estancia:

* **Paso A. Evolución en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v0.5`)**:
    * Se declaran las nuevas variables `horasEstancia` y `minutosEstancia` como Entero.
    * Se integran las operaciones utilizando la división truncada (`trunc(minutosEstanciaTotal / 60)`) y el operador `MOD` para el resto.

* **Paso B. Evolución en Java (`pr/src/ControlAccesoQR.java - v0.5`)**:
    * Integración de las operaciones directamente en el código Java:
      ```java
      int horasEstancia = minutosEstanciaTotal / 60;
      int minutosEstancia = minutosEstanciaTotal % 60;
      ```
    * Actualización del bloque final de salida por pantalla (`System.out.println`) para formatear el mensaje: `"Permanencia total en centro: " + horasEstancia + " horas y " + minutosEstancia + " minutos."`

## ⚙️ Sesión 2 (50 min). PR - Aplicación al proyecto propio

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 1. Trabajo del estudiante: evolución de su proyecto propio (40 min)

* Cada estudiante abre los archivos `.psc` y `.java` correspondientes a la versión `v0.4` de su proyecto elegido de la bolsa de proyectos y la evoluciona a `v0.5`.
* Debe aplicar la división entera (`/`) y el operador residuo (`%`) para resolver alguna conversión en el contexto de su dominio particular:
    * En **Aventura conversacional**: convertir el botín total de la partida en monedas de plata enteras y monedas de cobre restantes (`monedas / 100` y `monedas % 100`).
    * En **Motor de recomendación**: distribuir el total de minutos de visualización continua (*binge-watching*) de un usuario en horas y minutos sobrantes.
    * En **Simulador de físicas 2D**: convertir una distancia total recorrida en metros a un formato de kilómetros enteros y metros restantes.
    * En **Bóveda de contraseñas**: transformar los días restantes para la caducidad obligatoria de la clave en semanas y días sueltos (`dias / 7` y `dias % 7`).
* El docente circula por los puestos de trabajo comprobando que no se declaren como `double` aquellas variables que por lógica de negocio deban procesarse estrictamente con división entera.

### 2. Cierre de la sesión de programación (10 min)

* Comprobación en la consola integrada de IntelliJ (`Ctrl + Shift + F10`) de que la lógica matemática del módulo funciona sin errores de compilación ni anomalías en los resultados impresos por pantalla.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendida la diferencia entre la división entera y el residuo.   ║
║ [ ] Dominio práctico del operador módulo (%) para conversiones.        ║
║ [ ] Evolucionada la versión v0.5 del proyecto propio sin errores.      ║
║ [ ] Lógica matemática actualizada en los diagramas de PSeInt.          ║
╚════════════════════════════════════════════════════════════════════════╝
```