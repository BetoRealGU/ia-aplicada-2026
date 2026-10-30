# Introducción, alcance y requisitos

## 1. Introducción

El Proyecto de áreas verdes en Aguascalientes tiene como propósito atender la falta de información sistemática para identificar, priorizar y dar seguimiento a las áreas verdes de la ciudad que requieren atención o ampliación. Para ello, se propone utilizar inteligencia artificial mediante un modelo de lenguaje generativo capaz de clasificar los reportes enviados por los ciudadanos, facilitando su organización y consulta por parte del personal de las dependencias municipales encargadas de las áreas verdes.

## 2. Alcance

**Incluye:**

* Recopilación y clasificación de reportes ciudadanos relacionados con las áreas verdes.
* Uso de un modelo de lenguaje generativo para clasificar los reportes.
* Identificación de necesidades de atención o ampliación de áreas verdes.
* Anonimización de datos personales y ubicaciones antes de procesarlos.
* Aplicación de precauciones para reducir sesgos y riesgos identificados.

**No incluye:**

* [DATO PENDIENTE: exclusiones del alcance, según la ficha del proyecto (Avance 1)].

## 3. Requisitos funcionales

* RF-1. El sistema deberá recibir reportes ciudadanos relacionados con las áreas verdes de Aguascalientes.
* RF-2. El sistema deberá clasificar los reportes mediante un modelo de lenguaje generativo.
* RF-3. El sistema deberá organizar la información para facilitar la identificación y priorización de áreas verdes que requieren atención o ampliación.
* RF-4. El sistema deberá permitir que el personal municipal consulte los reportes clasificados.
* RF-5. El sistema deberá facilitar el seguimiento de los reportes recibidos. [DATO PENDIENTE: mecanismo de seguimiento].

## 4. Requisitos no funcionales

* RNF-1. Privacidad: Los datos personales y las ubicaciones deberán anonimizarse antes de procesar los reportes.
* RNF-2. Mitigación de sesgos: [DATO PENDIENTE: medida concreta contra el sesgo de cobertura, según el Avance 4].
* RNF-3. Seguridad y responsabilidad: Se deberán aplicar las precauciones de mitigación definidas por el equipo para reducir los riesgos asociados al uso de inteligencia artificial.

---

## Declaración de generación asistida

* **Modelo usado:** ChatGPT (versión: [DATO PENDIENTE]).
* **Fecha de generación del borrador:** [DATO PENDIENTE: fecha].
* **Número de correcciones aplicadas:** 3.
* **Correcciones:**
  1. Alcance, "No incluye": se eliminaron tres exclusiones que el modelo inventó (y etiquetó mal como [DATO PENDIENTE]); se dejó un pendiente a la espera de confirmar con el Avance 1.
  2. RF-5: el mecanismo de seguimiento se mantiene como [DATO PENDIENTE] por no estar definido.
  3. RNF-2: se reemplazó la frase vaga "deberá considerar el sesgo de cobertura" por un pendiente, a la espera de la medida concreta del Avance 4.
* **Prompt usado:**

```
Eres redactor técnico. Escribe la sección "Introducción, alcance y requisitos" de un documento técnico para el siguiente proyecto. Usa únicamente la información que te doy; si necesitas un dato que no está, escribe [DATO PENDIENTE] en lugar de inventarlo.

Nombre del proyecto: Proyecto de áreas verdes en Aguascalientes
Problema que resuelve: Falta de información sistemática para identificar, priorizar y dar seguimiento a las áreas verdes de la ciudad que requieren atención o ampliación.
Usuarios: Personal de dependencias municipales encargadas de áreas verdes y ciudadanos que envían reportes.
Tipo de IA propuesto: Clasificación de reportes ciudadanos con un modelo de lenguaje generativo.
Restricciones de datos: Los reportes pueden contener datos personales y ubicaciones, por lo que se debe anonimizar antes de procesarlos. Se identificaron sesgos de cobertura (zonas con más reportes reciben más atención) y riesgos asociados, para los cuales el equipo definió precauciones de mitigación.

Estructura: 1. Introducción (un párrafo), 2. Alcance (qué incluye y qué no incluye, en viñetas), 3. Requisitos funcionales (5 viñetas numeradas RF-1 a RF-5), 4. Requisitos no funcionales (3 viñetas RNF-1 a RNF-3).
Extensión máxima: 400 palabras. Español.
```
