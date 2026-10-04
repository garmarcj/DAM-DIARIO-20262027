# 🚀 Diario de clase: viernes, 9 de octubre de 2026 (festivo, pero sirve para otros grupos)
## 1.º DAM — Curso académico 2026/2027

**Módulos:** Entornos de desarrollo (ED) + Proyecto Intermodular (PI)  
**Fecha:** Viernes, 9 de octubre de 2026 (festivo, pero sirve para otros grupos) 
**Duración:** 2 horas lectivas (100 min)  

## 🧭 Sesión 1 (50 min). ED - Comparación de entornos de desarrollo

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: Es viernes por la tarde en la sede de AzaharTech. Laia Claramunt proyecta una consulta técnica remitida por el equipo de soporte del IES El Caminàs: *«En las aulas de informática disponen de equipos con IntelliJ IDEA, pero en los ordenadores portátiles prefieren utilizar Visual Studio Code. Nos preguntan si abrir el proyecto con otro entorno diferente puede corromper el software»*.
* *«Hoy comprobaremos de forma práctica que un código bien estructurado no pertenece a un fabricante de software concreto. El núcleo de Java debe comportarse con absoluta fidelidad tanto si lo editamos en un entorno libre como en un entorno propietario»*.

### 2. El ecosistema de herramientas de desarrollo (10 min)

* **El IDE completo frente al editor modular extensible:** 
    * *IntelliJ IDEA Community:* Entorno integrado (IDE) completo, libre (Apache 2.0) y diseñado específicamente para la JVM. Incluye compilador, depurador y analizador de serie.
    * *Visual Studio Code (VS Code):* Editor de texto modular y ligero. Utiliza extensiones (como el *Extension Pack for Java*) para comunicarse con el JDK mediante el protocolo LSP. Su instalador oficial incluye telemetría bajo licencia privativa.
* **Independencia del código fuente:** Ambos entornos utilizan bajo el capó el mismo compilador (`javac`) y máquina virtual (`java`). El código no cambia; lo que varía es la ergonomía y el consumo de recursos de la máquina.

### 3. Dojo de entrenamiento y katas de herramientas (35 min)

Cada estudiante trabaja de forma autónoma con su proyecto propio para certificar su independencia del IDE:

* **Kata 1 (Cinturón blanco / Nivel base). Ejecución en un segundo entorno:** Abrir, compilar y ejecutar el archivo maestro del proyecto propio en *Visual Studio Code*, demostrando que los resultados en consola (capturas de datos, cálculos y formateos) coinciden al céntimo con los obtenidos en IntelliJ.
* **Kata 2 (Cinturón marrón / Nivel avanzado). Auditoría de consumo en RAM:** Abrir el monitor del sistema operativo (Administrador de Tareas / `htop`) y comparar la memoria consumida por IntelliJ en reposo (ej. 800 MB - 1,5 GB) frente a VS Code (ej. 300 MB - 600 MB). Anotar en la libreta técnica en qué escenarios (equipos antiguos vs. estaciones de trabajo) sería más viable cada uno.
* **Kata 3 (Cinturón negro / «Hacker AzaharTech»). Diagnóstico de `UnsupportedClassVersionError`:** Utilizar el desensamblador `javap -v` para rastrear la versión interna del archivo compilado (`major version: 65`, que corresponde a Java 21) y documentar qué excepción crítica saltará si el cliente intenta ejecutar el binario en un servidor desfasado con Java 17.

## ⚙️ Sesión 2 (50 min). PI - De la necesidad al catálogo de requisitos del sistema

**Balance de tiempo:** Docente: 15 min | Estudiante: 35 min

### 1. Caso guía en AzaharTech (5 min)

* Arranque del caso guía: El equipo arranca el módulo de Proyecto Intermodular para abrir el Sprint 2. Laia toma la palabra: *«En el Sprint 1 demostramos que la lógica base era viable. Pero un cliente no firma contratos sobre intenciones generales; necesita saber con exactitud matemática qué hará y qué no hará el software»*.
* *«Si el cliente pide que el sistema sea 'rápido y seguro', eso no le sirve a un programador. Hoy aprenderemos a transformar necesidades en un Catálogo Formal de Requisitos del Sistema y abriremos nuestro Sprint Backlog 2»*.

### 2. La ingeniería de requisitos en el desarrollo de software (10 min)

* **Requisitos Funcionales (RF) frente a No Funcionales (RNF):**
    * **RF:** Describen *qué hace* el sistema (ej. capturar identificador, calcular estancia).
    * **RNF:** Describen *bajo qué restricciones técnicas o de calidad* lo hace (ej. usar OpenJDK 21, estructurarse mediante Apache Maven).
* **Reglas de redacción profesional (SMART):** Todo requisito debe tener un identificador unívoco (`RF-01`), evitar adjetivos subjetivos ("fácil", "moderno") y ser 100 % verificable mediante una prueba objetiva.
* **Fuentes técnicas y registro de IA (*Prompt Log*):** Obligatoriedad de contrastar información en fuentes primarias (Oracle, Apache) y documentar de forma ética cualquier consulta realizada a Inteligencia Artificial para depurar requisitos.

### 3. Laboratorio práctico guiado: Catálogo de requisitos y Sprint Backlog 2 (35 min)

* **Paso 1. Creación del catálogo de requisitos:** El estudiante crea el archivo `pi/docs/requisitos-sistema.md`. Redacta al menos 4 Requisitos Funcionales y 2 Requisitos No Funcionales aplicados estrictamente a su proyecto de la bolsa de proyectos (Aventura, Recomendador, Físicas o Contraseñas).
* **Paso 2. Apertura del Sprint Backlog 2:** Creación del archivo `pi/backlog/sprint2-backlog.md` listando las nuevas metas del Sprint 2 para los tres módulos técnicos.
* **Paso 3. Sincronización en GitHub:** Empleo del panel de control de versiones para realizar un commit atómico (ej. `docs(pi): definir catalogo de requisitos del sistema y abrir sprint backlog 2`) y subir la documentación técnica al repositorio remoto.

## 📊 Estado al cierre de la jornada

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DEL DÍA                         ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Verificada la independencia del código fuente ejecutando VS Code.  ║
║ [ ] Analizado el consumo de RAM de los diferentes IDEs del mercado.    ║
║ [ ] Comprendida la diferencia entre un RF y un RNF verificable.        ║
║ [ ] Creado el catálogo de requisitos del sistema (requisitos-sistema.md)║
║ [ ] Abierto y sincronizado en GitHub el Sprint Backlog 2.              ║
║ [ ] ¡SEMANA 4 COMPLETADA CON ÉXITO!                                    ║
╚════════════════════════════════════════════════════════════════════════╝
```