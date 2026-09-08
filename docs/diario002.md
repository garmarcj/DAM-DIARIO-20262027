---
title: "Viernes 11 de septiembre de 2026 - Presentación de ED y PI"
date: 2026-09-11
modules: "Entornos de desarrollo (ED) + Proyecto intermodular (PI)"
duration: "2 sesiones lectivas (100 minutos)"
layout: page
---

# 🛠️ Jornada de equipos y bolsa de proyectos
## 1.º DAM — Curso académico 2026/2027
**Módulos:** Entornos de desarrollo (ED) + Proyecto intermodular (PI)  
**Fecha:** Viernes, 11 de septiembre de 2026  
**Duración:** 2 sesiones lectivas (100 min)

---

# Entornos de desarrollo (ED) — 50 minutos
### La puesta a punto del taller digital de AzaharTech

---

## 🧭 Sesión 1. El control de calidad y las herramientas

### 1. El papel de entornos de desarrollo en AzaharTech (5 min)
* En programación construimos la lógica del software.
* En **entornos de desarrollo** aseguramos la **calidad de ingeniería**:
  * Manejo del compilador y del IDE profesional (**IntelliJ IDEA**).
  * Uso de sistemas de control de versiones y trazabilidad con **Git** y **GitHub**.
  * Higiene del repositorio y entrega formal con etiquetas de versión (**Git tags**).

---

### 2. Publicación oficial de los equipos de AzaharTech (10 min)
*Equipos equilibrados y heterogéneos confeccionados a partir del cuestionario de diagnóstico de ayer.*

| Equipo de trabajo | Integrantes asignados | Identificador Git oficial |
| :--- | :--- | :---: |
| **Equipo 01** | [Estudiante 1] · [Estudiante 2] · [Estudiante 3] | `equipo-01` |
| **Equipo 02** | [Estudiante 4] · [Estudiante 5] · [Estudiante 6] | `equipo-02` |
| **Equipo 03** | [Estudiante 7] · [Estudiante 8] · [Estudiante 9] | `equipo-03` |
| **Equipo 04** | [Estudiante 10] · [Estudiante 11] · [Estudiante 12] | `equipo-04` |

> 🎙️ **Nota.** Al proyectar la lista de equipos, resolveremos incidencias puntuales y confirmaremos que todo el grupo conoce su identificador.

---

### 3. Actividad 1. Comprobación del taller digital (20 min)
*Comprobación práctica en los puestos de trabajo para no perder tiempo el lunes.*

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   CHECKLIST TÉCNICO EN EL PUESTO                       │
├────────────────────────────────────────────────────────────────────────┤
│ 1. Abrir la terminal (cmd, PowerShell o bash) y ejecutar:              │
│    java -version                                                       │
│    (Comprobar si el equipo del aula tiene Java instalado)              │
│                                                                        │
│ 2. Acceder a https://github.com:                                       │
│    Crear cuenta personal de estudiante o verificar credenciales.       │
│                                                                        │
│ 3. Si no está instalado, descargar instaladores:                       │
│    • OpenJDK 21 (LTS)                                                  │
│    • IntelliJ IDEA Community Edition                                   │
└────────────────────────────────────────────────────────────────────────┘
```

> 🎙️ **Nota.** El profesor irá por el aula resolviendo dudas de cuentas de GitHub, comprobando versiones de Java y ayudando en las descargas.

---

### 4. Simulación de la jerarquía de carpetas oficial (10 min)

Apunta en tu libreta la ruta exacta que crearás el lunes en la primera sesión práctica de Git:

```text
azahartech/
└── equipo-01/                        <-- El identificador que te ha tocado hoy
    └── apellidos-nombre/             <-- Tus apellidos y nombre (sin espacios)
        ├── ed/                       <-- Entornos de desarrollo
        ├── pr/                       <-- Programación
        └── pi/                       <-- Proyecto intermodular
```

* **Regla de estilo.** Todo en minúsculas, sin espacios, sin acentos y sin caracteres especiales.

---

### 5. Dudas técnicas y cierre del bloque de ED (5 min)
* Comprobación de que todo el alumnado tiene cuenta de GitHub operativa y conoce su identificador de equipo.

---

# Proyecto intermodular (PI) — 50 minutos
### Elección del proyecto

---

## 🧭 Sesión 2. La bolsa de proyectos

### 1. ¿Qué es el proyecto intermodular? (10 min)
* Es el módulo que conecta la técnica con el mundo laboral real.
* **El nexo entre los módulos:**
  * En **PR** programáis los algoritmos y la lógica.
  * En **ED** gestionáis el repositorio, el versionado y la calidad.
  * En **PI** analizáis al cliente, gestionáis el backlog y defendéis el software ante el público.
* **Las sesiones de los viernes:** Espacio reservado para tutorización, uso ético de la IA (*prompt log*), arquitectura y preparación de la *sprint review*.

---

### 2. Catálogo de proyectos (15 min)

#### Área 1: Ciberseguridad
* **P1. Simulador de phishing:** Juego interactivo de detección de mensajes fraudulentos; clasificación por tipología (email, SMS, red social) con pistas, usuarios, estadísticas e historial.
* **P2. Bóveda de contraseñas:** Gestor de credenciales con evaluación de fortaleza mediante políticas de seguridad (básica, estricta, corporativa), caducidad y almacén seguro.

#### Área 2: Python
* **P3. Calculadora paso a paso:** Evaluador de expresiones matemáticas con desglose paso a paso, tokenización, precedencia, visor del proceso e histórico.
* **P4. Generador de datos de prueba:** Herramienta de síntesis de datasets sintéticos a partir de plantillas con campos polimórficos y exportación a ficheros CSV.

#### Área 3: Videojuegos y realidad virtual
* **P5. Aventura conversacional:** Motor de narrativa interactiva ramificada con toma de decisiones, escenas, inventario, personajes (aliado, enemigo, neutral) y guardado.
* **P6. Simulador de físicas 2D:** Entorno de simulación cinemática con detección de colisiones, múltiples bolas con comportamientos físicos y telemetría.

#### Área 4: Productos software en contenedores
* **P7. Reparto de contenedores en nodos:** Planificador de asignación de carga en clúster según capacidad de CPU y memoria, nodos especializados e interfaz con barras de ocupación.
* **P8. Catálogo de servicios + generador de config:** Asistente paso a paso (*wizard*) para parametrizar servicios (web, BD, worker), catálogo e historial de despliegues.

#### Área 5: Inteligencia artificial y big data
* **P9. Motor de recomendación:** Sistema basado en afinidad entre gustos y catálogos de ítems categorizados (película, música, libro) con cálculo de coincidencia por etiquetas.
* **P10. Analizador de reseñas:** Analizador de sentimiento léxico sobre comentarios con diccionarios de palabras clave y estadísticas por producto.

#### Área 6: Recursos y servicios en la nube
* **P11. Cotizador cloud:** Presupuestador interactivo de infraestructura cloud con cálculo de costes según recurso (cómputo, almacenamiento, red) y comparación de ofertas.
* **P12. Dashboard de monitorización:** Panel de control visual para métricas y telemetría de sistemas, lectura de sensores (CPU, memoria, red) y umbrales de alerta.

---

### 3. Actividad 2. Elección y consenso en el equipo (15 min)

```text
┌────────────────────────────────────────────────────────────────────────┐
│               FICHA DE ELECCIÓN DE RETO (1 POR EQUIPO)                 │
├────────────────────────────────────────────────────────────────────────┤
│ Equipo: ______________________________________________________________ │
│ Integrantes: _________________________________________________________ │
│                                                                        │
│ 1.ª Opción prioritaria: ______________________________________________ │
│ 2.ª Opción de reserva:  ______________________________________________ │
│ 3.ª Opción de reserva:  ______________________________________________ │
└────────────────────────────────────────────────────────────────────────┘
```

* Los 4 integrantes de cada equipo se reúnen en el aula para debatir vocaciones e intereses.
* Seleccionan sus 3 opciones y entregan la ficha física al profesor.

> 🎙️ **Nota.** El profesor os explicará las dudas técnicas de los proyectos y recogerá las fichas con vuestras preferencias.

---

### 4. Adjudicación en pizarra (5 min)
* El profesor adjudica los proyectos en directo garantizando variedad temática en el aula.
* Se registra la asignación oficial en el acta docente (*ej. Equipo 01 ➔ P11. Cotizador cloud; Equipo 02 ➔ P1. Simulador de phishing...*).

---

### 5. Cierre del día 11 (5 min)

```text
╔════════════════════════════════════════════════════════════════════════╗
║                       ESTADO AL CIERRE DE HOY                          ║
╠════════════════════════════════════════════════════════════════════════╣
║ [ ] Identificador de equipo asignado (por ejemplo: equipo-02).         ║
║ [ ] Proyecto adjudicado de la bolsa de proyectos.                      ║
║ [ ] Comprobación técnica de puesto completada (terminal y GitHub).     ║
║ [ ] Ruta de carpetas anotada para el inicio de las clases.             ║
╚════════════════════════════════════════════════════════════════════════╝