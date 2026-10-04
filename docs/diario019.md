# 🚀 Diario de clase: martes, 6 de octubre de 2026
## 1.º DAM — Curso académico 2026/2027

**Módulo:** Programación (PR)  
**Fecha:** Martes, 6 de octubre de 2026  
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1. PR - Variables primitivas frente a variables de referencia

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Pau Ferrer intenta crear un segundo generador aleatorio para la asignación de códigos promocionales en el vestíbulo. Escribe en el código `Random generadorPromocion = generadorAcceso;` esperando tener dos máquinas distintas. Sin embargo, al probarlo, descubre que ambos generan exactamente la misma secuencia de números, afectándose mutuamente.
* Alba Torres interviene: *«Ese es el error más común al dar el salto a los objetos. Al utilizar el operador igual (`=`) con variables primitivas, copias el dato real en una nueva celda de la memoria. Pero con los objetos, solo estás copiando el 'mando a distancia' (la referencia), creando un **alias** que apunta a la misma máquina física en el Heap. Hoy entenderemos cómo gestionar estas referencias y qué ocurre cuando un objeto se queda huérfano y actúa el Recolector de Basura»*.

### 2. Fundamento teórico: variables primitivas frente a variables de referencia (10 min)

* **A. El mecanismo de copia en memoria: valor frente a referencia (alias):** 
    * En tipos primitivos (`int a = b;`): se clona el valor físico en dos celdas independientes del Stack.
    * En tipos de referencia (`Random a = b;`): se copia la dirección de memoria. Ambas variables se convierten en *alias* que apuntan a la misma entidad viva en el montón (Heap).
* **B. Objetos huérfanos y el recolector de basura (Garbage Collector):** Si reasignamos la única variable que apunta a un objeto hacia otro lugar, el objeto original queda "huérfano" en el Heap. La JVM detecta que nadie puede comunicarse con él y el *Garbage Collector* actúa en segundo plano para limpiar esa memoria y evitar fugas (*memory leaks*).
* **C. El valor `null` y la seguridad de referencias:** Cómo forzar que una variable de referencia suelte su objeto apuntándola conscientemente a la nada (`null`), garantizando que no modifiquemos objetos por accidente.

### 3. Evolución del caso guía a ControlAccesoQR v1.2 (35 min)

Actualización conjunta a `ControlAccesoQR v1.2`. Los estudiantes abren el archivo maestro para corregir el error del alias y crear una segunda instancia real y separada en memoria:

* **Paso A. Algoritmo en PSeInt (`pr/pseudocodigo/ControlAccesoQR.psc — v1.2`)**:
    * Actualización del diagrama introduciendo conceptualmente la lógica de los dos generadores independientes.

* **Paso B. Implementación en Java (`pr/src/ControlAccesoQR.java — v1.2`)**:
    * Creación correcta del segundo objeto utilizando nuevamente el operador de instanciación: `Random generadorPromocion = new Random();`.
    * Sustitución de la asignación defectuosa que provocaba la trampa del alias.
    * Impresión por consola de ambos resultados para verificar visualmente que las secuencias criptográficas ahora discurren de forma totalmente independiente.

## ⚙️ Sesión 2 (50 min). PR - Dojo de entrenamiento y katas de código

**Balance de tiempo:** Docente: 5 min | Estudiante: 45 min

### 1. Segunda sesión: dojo de entrenamiento y katas de código (45 min)

Cada estudiante trabaja de forma autónoma sobre la versión `v1.2` de su proyecto elegido, resolviendo los siguientes retos de asimilación técnica:

* **Kata 1 (Cinturón blanco / Nivel base). Dos generadores independientes en tu proyecto:** 
    * Instanciar explícitamente con el operador `new` dos objetos `Random` en la misma clase.
    * En *Aventura*: un generador para el daño crítico y otro para la aparición del botín.
    * En *Motor de recomendación*: un generador de identificadores de visualización y otro para inyectar ruido estadístico en las reseñas.
    * En *Simulador de físicas*: viento horizontal por un lado y turbulencias verticales por otro.
    * En *Bóveda de contraseñas*: un generador para las letras minúsculas y otro distinto para caracteres numéricos.
* **Kata 2 (Cinturón marrón / Nivel avanzado). La trampa del alias de memoria:** Forzar intencionadamente un alias (`Random copia = original;`) en el proyecto propio. Extraer valores utilizando el "original" y luego la "copia", demostrando mediante `System.out.println` cómo ambos mandos a distancia agotan la misma secuencia del objeto compartido.
* **Kata 3 (Cinturón negro / «Hacker AzaharTech»). Telemetría de objetos huérfanos y Garbage Collector:** Ensuciar intencionadamente la memoria RAM creando objetos anónimos en bucle continuo o reasignando incesantemente la misma variable de referencia. Utilizar las herramientas de la máquina virtual (como invocar `System.gc()` y medir con `Runtime.getRuntime().freeMemory()`) para documentar en la consola el momento exacto en el que el recolector de basura interviene.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Comprendida la copia por referencia (alias) frente a por valor.    ║
║ [ ] Solucionada la trampa del alias al instanciar objetos en Java.     ║
║ [ ] Asimilado el rol del Garbage Collector limpiando el Heap.          ║
║ [ ] Evolucionada la versión v1.2 del proyecto propio sin errores.      ║
║ [ ] Katas de instanciación múltiple y memoria residual superadas.      ║
╚════════════════════════════════════════════════════════════════════════╝
```