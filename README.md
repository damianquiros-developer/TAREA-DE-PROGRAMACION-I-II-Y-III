# Tarea de Programación I, II y III — Sistema de Notas Estudiantiles

**Estudiante:** Damian Quirós Jiménez · **Sección:** 11-5 · **Colegio:** COTEPECOS
**Subárea:** Programación Web · **Nivel:** 11° · **II Semestre 2026**

Este proyecto se entrega en 3 tareas/etapas que se acumulan una sobre la otra. Todas giran
alrededor del mismo sistema: un **Sistema de Notas Estudiantiles** hecho en Java con POO.
La idea de mantenerlo todo en un solo repositorio es que las clases que se diseñan en la
Etapa 1 son literalmente las que se usan (y se les agrega cosas) en la Etapa 2 y la Etapa 3,
para no rehacer nada y que todo tenga coherencia de principio a fin (esto lo pide el
documento explícitamente para la Etapa 2: "Mantener coherencia con la primera etapa").

## Resumen de las 3 etapas

| Etapa | Nombre | Entregable | Puntos | Fecha límite (según doc) | Estado |
|---|---|---|---|---|---|
| 1 | Diseño de un Sistema de Notas (POO básica) | PDF teórico-explicativo | 24 pts | 14-15 octubre | ✅ Hecho |
| 2 | Lógica y estructuras de datos (Bucles, Arreglos y Matrices) | PDF teórico-explicativo | 15 pts | 13-14 octubre | ✅ Hecho |
| 3 | Integración final: Herencia, Polimorfismo e Interfaz Gráfica | PDF + proyecto NetBeans ejecutable (.zip) | 15 pts | 13-14 octubre | ⏳ Pendiente |

**Total del proyecto: 54 puntos.**

> Nota sobre las fechas: el documento original trae fechas distintas para cada tarea, pero
> las tres están dentro de la misma semana de octubre. Al final lo que importa es que las
> tres etapas se entreguen y que la 3 sea la última porque depende de las otras dos.

## Decisiones de diseño (para que quede registrado el porqué)

- **Clases elegidas:** `Estudiante`, `Curso`, `Nota` (las 3 mínimas que pide el documento)
  más `Profesor` (una de las dos opcionales que el documento sugiere: "puede agregar otras,
  por ejemplo, Profesor o Grupo"). Se eligió `Profesor` y no `Grupo` porque la **Etapa 3
  exige textualmente** una superclase `Persona` de la que hereden `Estudiante` y `Profesor`.
  Diseñar `Profesor` desde la Etapa 1 evita rehacer el diagrama de clases más adelante: en
  la Etapa 3 solo se añade la superclase `Persona` y las flechas de herencia, sin tocar lo
  demás.
- **Sin herencia todavía:** aunque ya sabemos que en la Etapa 3 habrá herencia, en la Etapa 1
  **no se aplica** porque el documento no la pide en esta parte (la pide explícitamente hasta
  la III Tarea, punto 1). Meterla antes de tiempo sería inventar un requisito que no está.
- **Relaciones del diagrama de clases:** se usaron 3 tipos de relación (asociación,
  agregación y composición) con multiplicidad en cada una, siguiendo el mismo nivel de
  detalle que el diagrama de ejemplo del documento (el del sistema de biblioteca).

## Cronograma de trabajo (plan de acción)

### Etapa 1 — Diseño de un Sistema de Notas (POO básica) — 24 pts ✅
1. Definir las 4 clases y su propósito dentro del sistema. *(Indicador 1)*
2. Definir atributos (mín. 3) y métodos (mín. 2) de cada clase. *(Indicador 2)*
3. Aplicar encapsulamiento con `private` + `get`/`set` en cada atributo. *(Indicador 3)*
4. Escribir el constructor de cada clase. *(Indicador 4)*
5. Explicar paso a paso qué pasa cuando se crea un objeto dentro de `main`. *(Indicador 5)*
6. Diagrama de clases UML completo (atributos, métodos, relaciones, multiplicidad). *(Indicador 6)*
7. Diagrama de Casos de Uso UML (actores + funcionalidades). *(Indicador 7)*
8. Diagrama de Secuencia UML (objetos, líneas de vida, mensajes). *(Indicador 8)*
9. Armar portada + orden + exportar a PDF.

### Etapa 2 — Lógica y estructuras de datos — 15 pts ✅
1. Explicar bucle `for`/`while` recorriendo una lista de `Estudiante`, con ejemplo de código.
2. Explicar cómo se guardan varios `Estudiante` o `Nota` en un arreglo.
3. Proponer una matriz de notas (filas = estudiantes, columnas = cursos) y explicar el
   recorrido con bucles anidados.
4. Explicar cómo los arreglos/matrices se integran con las clases de la Etapa 1.
5. Código completo: bucles + arreglos/matrices calculando el promedio general de cada
   estudiante.
6. Cada punto lleva: ejemplo descriptivo + código + explicación (como pide la observación
   del documento).

### Etapa 3 — Integración final — 15 pts (al final)
1. Crear la superclase `Persona` (nombre, identificación) y hacer que `Estudiante` y
   `Profesor` hereden de ella.
2. Polimorfismo: redefinir `mostrarDatos()` en cada subclase.
3. Interfaz gráfica en Swing (`JFrame`, `JPanel`, `JButton`, `JTextField`) para agregar,
   mostrar y calcular notas.
4. Integrar todo: clases + herencia + polimorfismo + interfaz, con `main` iniciando la
   ventana principal, y comentarios en el código.
5. Documentar el proceso completo, con capturas de pantalla del proyecto corriendo en
   NetBeans.
6. Esta etapa sí requiere ejecutar el proyecto en NetBeans y entregar la carpeta
   comprimida (.zip), a diferencia de las etapas 1 y 2 que son solo teóricas.

## Estructura del repositorio

```
tarea-de-programacion-i-ii-y-iii/
├── README.md                         <- este archivo (resumen + cronograma)
├── etapa-1-diseno-poo/
│   ├── etapa-1-sistema-notas.html    <- fuente del documento
│   └── etapa-1-sistema-notas.pdf     <- entregable en PDF ✅
├── etapa-2-estructuras-datos/
│   ├── etapa-2-estructuras-datos.html <- fuente del documento
│   └── etapa-2-estructuras-datos.pdf  <- entregable en PDF ✅
└── etapa-3-integracion-final/        <- pendiente (incluirá el proyecto NetBeans)
```
