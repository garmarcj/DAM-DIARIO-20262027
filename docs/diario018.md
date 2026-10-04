# 🚀 Diario de clase: lunes, 5 de octubre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulos:** Programación (PR) + Entornos de desarrollo (ED)  
**Fecha:** Lunes, 5 de octubre de 2026  
**Duración:** 4 horas lectivas (200 min)  

## 🧭 Sesión 1. PR - Fundamentos de POO, instanciación y memoria (Stack vs. Heap)

**Balance de tiempo:** Docente: 20 min | Estudiante: 30 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del Sprint 2. Alba Torres proyecta el código `v1.0` cerrado la semana pasada: *«Hemos logrado que nuestro software sea un motor secuencial exacto. Pero el director del IES El Caminàs ha detectado una vulnerabilidad: el token QR usa un número correlativo simple (`#1043`, `#1044`...). Cualquiera podría predecir el siguiente código y falsificar su asistencia»*.
* *«Para blindarlo, no reinventaremos la rueda con cálculos complejos; daremos el salto a la **Programación Orientada a Objetos (POO)**. Instanciaremos clases de la biblioteca estándar de Java como `Random` y descubriremos qué ocurre bajo el capó de la memoria RAM al utilizar el operador `new`»*.

### 2. Fundamento teórico: clases, objetos y modelo de memoria física (15 min)

* **Clase (molde) frente a objeto (instancia):** Una clase es el plano que define comportamiento, mientras que un objeto es la entidad viva creada en memoria mediante el operador `new`.
* **Arquitectura de la memoria RAM en Java:**
    * **Stack (Pila):** Memoria rápida y estructurada donde viven las variables primitivas (`int`, `double`) y las referencias (punteros a memoria).
    * **Heap (Montón):** Espacio dinámico donde residen los objetos físicos reales generados con `new`.
* **El valor `null` y el temido `NullPointerException`:** Qué sucede cuando una variable de referencia en el *Stack* se declara, pero no se inicializa apuntando a un objeto real en el *Heap*.

### 3. Evolución del caso guía a ControlAccesoQR v1.1 (30 min)

Actualización conjunta a `ControlAccesoQR v1.1`. Los estudiantes abren el archivo maestro para integrar la clase `Random` e inyectar un código criptográfico de seguridad:

* **Paso A. Algoritmo en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc - v1.1`)**:
    * Se añade a la lógica la variable para almacenar el código de seguridad aleatorio, aunque PSeInt no gestione el Heap como Java.

* **Paso B. Implementación en Java (`pr/src/ControlAccesoQR.java - v1.1`)**:
    * Importación del paquete `java.util.Random`.
    * Instanciación del objeto: `Random generador = new Random();`.
    * Sustitución del identificador predecible por un número pseudoaleatorio seguro capturado con el método `generador.nextInt()`.

## ⚙️ Sesión 2 (50 min). PR - Dojo de entrenamiento y katas de código

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 1. Katas de código: instanciación en el proyecto propio (45 min)

Cada estudiante trabaja de forma autónoma en su proyecto propio `v1.1`, resolviendo las katas según su nivel de destreza:

* **Kata 1 (Cinturón blanco / Nivel base):** Instanciar la clase `Random` en su proyecto.
    * En *Aventura*: generar tiradas de dados para calcular daño.
    * En *Recomendación*: generar IDs de usuarios anónimos aleatorios.
    * En *Físicas*: introducir perturbaciones aleatorias en la velocidad del viento.
    * En *Contraseñas*: generar semillas para claves aleatorias.
* **Kata 2 (Cinturón marrón / Nivel avanzado):** Implementar una fórmula matemática pura para acotar los números generados a un rango estricto `[MIN, MAX]`.
* **Kata 3 (Cinturón negro / Hacker AzaharTech):** Investigación del comportamiento de la semilla (*Seed*). Instanciar el objeto pasando una semilla fija `new Random(12345L)` y explicar por qué la "aleatoriedad" se vuelve completamente determinista.

## 🧭 Sesión 3. ED - La transformación del software y Bytecode universal

**Balance de tiempo:** Docente: 25 min | Estudiante: 25 min

### 1. Caso guía en AzaharTech (5 min)

* Inicia la sesión de Entornos. Laia Claramunt expone una duda del instituto: el IES El Caminàs tiene ordenadores con Windows, servidores con Linux y equipos variados. *«¿Tendremos que programar versiones distintas para cada sistema?»*
* La respuesta es negativa. Hoy entenderemos el viaje del código: cómo un archivo de texto humano se convierte en *Bytecode* y por qué la Máquina Virtual de Java hace que el software sea independiente del *hardware*.

### 2. La cadena de transformación y virtualización (10 min)

* **A. Código fuente (*Source code*):** El archivo `.java` legible para humanos.
* **B. Código objeto intermedio (*Bytecode*):** Archivo `.class` generado tras compilar (`javac`). Son instrucciones binarias para un procesador virtual genérico.
* **C. Código ejecutable (*Machine code*):** Los ceros y unos traducidos en tiempo real por la Máquina Virtual de Java (JVM) específica de cada sistema operativo (Windows, Linux, macOS). Principio *Write Once, Run Anywhere*.

### 3. Laboratorio práctico guiado: Inspección del archivo .class (10 min)

* Utilización de un visor hexadecimal para observar las tripas de `ControlAccesoQR.class` y encontrar la firma mágica `0xCAFEBABE`.
* Uso del desensamblador oficial en la terminal (`javap -c`) para leer el bytecode y observar las instrucciones internas (`iload`, `imul`, `bipush`) en las que se ha convertido el código de la sesión de PR.

## 🛠️ Sesión 4. Laboratorio práctico: Compilación multi-entorno y katas

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 1. Katas de herramientas: la independencia del IDE (45 min)

Los estudiantes abren la terminal nativa y abandonan el confort del IDE para trabajar directamente con el *JDK*:

* **Kata 1 (Cinturón blanco / Nivel base):** Compilación y ejecución multi-entorno de su proyecto. Navegar al directorio fuente y utilizar explícitamente `javac MiProyecto.java` y `java MiProyecto`, verificando que el software funciona perfectamente sin IntelliJ.
* **Kata 2 (Cinturón marrón / Nivel avanzado):** Compilación desacoplada. Crear una carpeta limpia `bin/` y obligar al compilador a depositar allí el `.class` utilizando el parámetro de destino (`javac -d bin ...`). Posteriormente, arrancar la JVM apuntando la ruta mediante el parámetro de Classpath (`java -cp bin ...`).
* **Kata 3 (Cinturón negro / Hacker AzaharTech):** Telemetría de la JVM. Ejecutar el proyecto con la bandera de diagnóstico detallado (`java -verbose:class`) para observar en tiempo real la carga en memoria RAM de cientos de clases núcleo del sistema operativo antes de arrancar el propio código del estudiante.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendida la arquitectura de memoria Stack frente a Heap (PR).   ║
║ [ ] Clase Random instanciada y versión v1.1 evolucionada con éxito.    ║
║ [ ] Asimilado el flujo: Código fuente -> Bytecode -> JVM (ED).         ║
║ [ ] Archivo .class analizado mediante desensamblador javap.            ║
║ [ ] Katas de compilación manual y Classpath superadas en terminal.     ║
╚════════════════════════════════════════════════════════════════════════╝
```
```