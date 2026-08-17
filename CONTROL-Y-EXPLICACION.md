# Control y explicación del proyecto

Este archivo es tu bitácora: qué se hizo, por qué, y cómo explicarlo si el profe (o vos mismo
repasando) pregunta algo. Se va actualizando en cada etapa, no se borra lo anterior.

---

## Etapa 1 — Diseño de un Sistema de Notas (POO básica) · ✅ Entregada

### Qué se hizo
1. Se analizó el PDF completo de las 3 tareas y sus 3 rúbricas antes de empezar a escribir.
2. Se detectó que la rúbrica de la Etapa 1 tiene **8 indicadores**, aunque las "indicaciones
   específicas" del documento solo describen 6 puntos en texto — los indicadores 7 y 8
   (diagrama de casos de uso y diagrama de secuencia) solo aparecen en la tabla de
   calificación. Se cubrieron los 8, no solo los 6 explicados en el texto.
3. Se diseñó el sistema con 4 clases: `Estudiante`, `Curso`, `Nota` y `Profesor`.
   `Profesor` no es obligatoria (el mínimo es Estudiante/Curso/Nota), se agregó porque el
   documento lo permite explícitamente y porque la Etapa 3 la va a necesitar para aplicar
   herencia — así no hay que rediseñar nada más adelante.
4. **No se aplicó herencia en esta etapa**, a propósito: el documento no la pide todavía
   (la exige hasta la III Tarea), así que meterla ahora habría sido agregar algo no pedido.
5. Se armó el documento completo en HTML con diagramas UML dibujados a mano en SVG
   (no con una herramienta externa), y se exportó a PDF con Chromium en modo headless.
6. Se revisó el PDF **página por página como imagen** (no solo el código fuente) y se
   encontraron y corrigieron 3 líneas de código que se salían del margen de la página
   (quedaban cortadas) más un choque de texto en el diagrama de secuencia.

### Indicadores de la rúbrica cubiertos (24 pts)

| # | Indicador | Dónde está en el documento | Cómo explicarlo si preguntan |
|---|---|---|---|
| 1 | Diseñar las clases principales | Sección 1 | Estudiante/Curso/Nota son las mínimas del documento; se agregó Profesor porque un curso necesita quién lo imparta y porque la Etapa 3 la va a pedir para herencia. |
| 2 | Definir atributos y métodos | Sección 2 (tablas por clase) | Cada clase tiene 3-4 atributos privados y al menos 2 métodos además de los get/set. |
| 3 | Encapsulamiento con get/set | Sección 3 | Todos los atributos son `private`; solo se accede por `get`/`set`, así el sistema controla qué valores entran (ej. evitar un promedio inválido). |
| 4 | Constructores | Sección 4 (clases completas) | El constructor corre automáticamente con `new` y llena los atributos principales para que el objeto nazca con datos válidos, no vacío. |
| 5 | Explicar el método main | Sección 5 (7 pasos numerados) | Java reserva memoria en el heap, corre el constructor, y la variable guarda la *referencia* al objeto, no el objeto en sí. Cada `new` crea un objeto independiente. |
| 6 | Diagrama de clases UML | Sección 6 | 4 clases con atributos/métodos y 3 tipos de relación: asociación (Profesor-Curso), agregación (Curso-Nota, rombo vacío) y composición (Estudiante-Nota, rombo relleno). |
| 7 | Diagrama de casos de uso UML | Sección 7 | 2 actores (Estudiante, Profesor) y sus funcionalidades; ambos casos de uso incluyen "Calcular promedio" con `<<include>>`. |
| 8 | Diagrama de secuencia UML | Sección 8 | Flujo de "registrar una nota": Profesor → Main crea la Nota → Curso la agrega → Estudiante actualiza su promedio, con activaciones y mensajes de retorno. |

### Dónde está todo
- `etapa-1-diseno-poo/etapa-1-sistema-notas.pdf` → el entregable.
- `etapa-1-diseno-poo/etapa-1-sistema-notas.html` → fuente editable (por si hay que ajustar
  algo antes de reexportar el PDF).

### Decisiones que quedaron registradas (por si alguien pregunta "por qué así")
- Se usó Chromium headless para exportar el PDF (no Word ni Google Docs) porque permite
  controlar el diseño y los diagramas SVG con precisión.
- Los diagramas UML no vienen de una herramienta como Draw.io o Lucidchart: se dibujaron a
  mano en SVG dentro del mismo documento, siguiendo la notación UML estándar (cajas de 3
  compartimentos, rombos de agregación/composición, actores, líneas de vida).

---

## Etapa 2 — Lógica y estructuras de datos · ⏳ Pendiente

*(se completa cuando se trabaje esta etapa)*

## Etapa 3 — Integración final · ⏳ Pendiente

*(se completa cuando se trabaje esta etapa)*
