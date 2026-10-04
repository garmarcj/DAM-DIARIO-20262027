# 🚀 Diario de clase: miércoles, 7 de octubre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Miércoles, 7 de octubre de 2026  
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1. PR - Constructores con parámetros y tipos de retorno

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Pau Ferrer quiere realizar simulaciones de estrés en el control de acceso del IES El Caminàs, pero los códigos aleatorios hacen que sus pruebas fallen porque cada ejecución produce números impredecibles. Además, el director solicita que se genere aleatoriamente un "factor de temperatura de error" decimal.
* Alba Torres interviene: *«Hasta ahora hemos invocado clases pidiendo la configuración por defecto y extraído siempre números enteros. Pero los objetos son herramientas flexibles. Podemos inyectarles datos en el momento de nacer mediante **constructores parametrizados** (para obligarlos a comportarse de forma determinista) y podemos utilizar métodos que devuelven todo tipo de datos: reales, booleanos o caracteres. Hoy aprenderemos a leer las firmas de los métodos y a exprimir la clase Random»*.

### 2. Fundamento teórico: constructores, firmas y tipos de retorno (10 min)

* **A. Constructores con parámetros frente a constructores vacíos:**
    * El constructor vacío (`new Random()`) utiliza el reloj interno del sistema operativo en nanosegundos para crear la semilla de entropía.
    * El constructor parametrizado (`new Random(12345L)`) inyecta una semilla explícita (*Seed*) al nacer. Explicación de cómo esto provoca que la secuencia "aleatoria" pase a ser estrictamente repetitiva y predecible (ideal para *testing* y auditorías).
* **B. Tipos de retorno y métodos de la clase Random:**
    * Cómo leer e interpretar la firma de un método en la documentación oficial de Java (`public double nextDouble()`).
    * Implementación de retornos variados: la generación de decimales con `nextDouble()` (que devuelve un valor estrictamente entre `0.0` y `1.0`) y la toma de decisiones binarias aleatorias con `nextBoolean()`.

### 3. Evolución del caso guía a ControlAccesoQR v1.3 (35 min)

Actualización conjunta a `ControlAccesoQR v1.3`. Los estudiantes abren el archivo maestro para implementar constructores parametrizados para la auditoría y añadir ruido térmico decimal:

* **Paso A. Algoritmo en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc — v1.3`)**:
    * Actualización del diagrama incluyendo la simulación de variaciones térmicas (decimales) y las banderas lógicas generadas al azar.

* **Paso B. Implementación en Java (`pr/src/ControlAccesoQR.java — v1.3`)**:
    * Configuración del objeto de simulación inyectando una semilla fija: `Random auditoria = new Random(42L);`.
    * Extracción de ruido térmico mediante el tipo de retorno adecuado: `double errorSensor = auditoria.nextDouble();`.
    * Simulación de un fallo técnico aleatorio en el terminal extrayendo un valor lógico: `boolean sensorBloqueado = auditoria.nextBoolean();`.

## ⚙️ Sesión 2 (50 min). PR - Dojo de entrenamiento y katas de código

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 1. Segunda sesión: dojo de entrenamiento y katas de código (45 min)

Cada estudiante trabaja de forma autónoma sobre la versión `v1.3` de su proyecto elegido, resolviendo las siguientes katas de destreza técnica:

* **Kata 1 (Cinturón blanco / Nivel base). Métodos con retorno `double` y `boolean` en tu proyecto:** 
    * Invocar y guardar el resultado de métodos que devuelven distintos tipos primitivos.
    * En *Aventura*: generar una probabilidad de esquive (`nextBoolean`) y un multiplicador de poción entre 0.0 y 1.0 (`nextDouble`).
    * En *Motor de recomendación*: determinar si un usuario es "VIP" al azar y asignar una desviación decimal en la nota de la película.
    * En *Simulador de físicas*: simular ráfagas de viento decimales y si el cuerpo de prueba colisiona en el aire de forma aleatoria.
    * En *Bóveda de contraseñas*: decidir si se incluye o no un símbolo especial en la contraseña generada (`nextBoolean`).
* **Kata 2 (Cinturón marrón / Nivel avanzado). La fábrica de números reales escalados:** Puesto que `nextDouble()` solo devuelve valores en el rango `[0.0, 1.0)`, el estudiante debe implementar una fórmula matemática utilizando sumas y multiplicaciones para lograr generar números decimales aleatorios dentro de un rango específico distinto (por ejemplo, temperaturas térmicas reales aleatorias estrictamente entre `36.0` y `40.0` ºC).
* **Kata 3 (Cinturón negro / «Hacker AzaharTech»). El determinismo de la semilla en auditoría de software:** Instanciar el objeto principal del proyecto utilizando un constructor parametrizado con la semilla `new Random(1337L)`. El alumno ejecutará el código 5 veces y capturará la salida, documentando por qué el comportamiento del sistema (números y booleanos extraídos) es matemáticamente idéntico en todas las pruebas, demostrando el poder del *testing* con semillas.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendido el uso de constructores con parámetros (semillas).     ║
║ [ ] Asimiladas las firmas de los métodos y sus tipos de retorno.       ║
║ [ ] Implementados métodos nextDouble() y nextBoolean() de Random.      ║
║ [ ] Evolucionada la versión v1.3 del proyecto propio sin errores.      ║
║ [ ] Katas de números escalados y determinismo criptográfico superadas. ║
╚════════════════════════════════════════════════════════════════════════╝
```