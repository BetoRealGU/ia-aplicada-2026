# Selección de modelo generativo para el proyecto CiberEscudo

## Descripción del proyecto

CiberEscudo es un proyecto de ciberseguridad que busca ayudar a los usuarios a proteger sus datos personales, reconocer posibles amenazas informáticas y conocer buenas prácticas para utilizar internet de forma segura. La inteligencia artificial se utilizaría como apoyo para explicar conceptos, responder preguntas generales de seguridad y orientar a los usuarios sobre medidas preventivas.

## Modelos evaluados

Durante este laboratorio utilicé ChatGPT, ya que no contaba con acceso a Google AI Studio para modificar directamente la temperatura del modelo.

En el curso también se consideran herramientas como Gemini, DeepSeek y los modelos disponibles en Google AI Studio. Para completar una comparación justa, únicamente deben marcarse como evaluados aquellos que realmente se hayan probado en el laboratorio o durante la semana 1.

## Evidencia de tokens

Tokens de mi documento de referencia: 1,610 tokens.

Caracteres del documento: 9,023.

Número de páginas: 4.

Caracteres por token del documento completo: 5.60.

En la comparación de idiomas, la frase corta en español utilizó 9 tokens y la versión en inglés utilizó 8 tokens. Para el párrafo de aproximadamente 100 palabras, el español utilizó 139 tokens y el inglés 125 tokens.

Los resultados muestran que el texto en español utilizó más tokens en las muestras analizadas. Esto puede depender de las palabras utilizadas, la longitud de la traducción y la manera en que el tokenizador divide el texto. Por eso, conviene medir los documentos del proyecto antes de procesarlos.

## Evidencia de temperatura

Para tareas de precisión, como explicar medidas de protección de datos o redactar avisos de privacidad, elegiría una temperatura baja, como 0.2, siempre que el modelo permita configurarla directamente. El objetivo sería obtener respuestas claras y consistentes.

Para tareas creativas, como proponer nombres, ideas o mensajes para CiberEscudo, elegiría una temperatura más alta, como 1.0, si está disponible, para explorar respuestas más variadas.

En este laboratorio utilicé ChatGPT sin acceso al control directo de temperatura. Las nueve respuestas normales presentaron tres formulaciones diferentes. En las pruebas con instrucciones predecibles, las tres respuestas fueron diferentes; en las instrucciones creativas también fueron diferentes. El grupo creativo presentó 35 palabras distintas, frente a 25 del grupo predecible.

Estas pruebas permiten comparar las respuestas obtenidas mediante instrucciones diferentes, pero no demuestran directamente el efecto de temperaturas numéricas, porque no pude modificar ese parámetro.

## Evidencia de contexto

El documento de referencia tenía cuatro páginas y aproximadamente 1,610 tokens en la medición inicial.

En el experimento, ChatGPT encontró el código de verificación AZUL-7342 cuando utilicé una, dos y cuatro copias del documento. Cuando utilicé ocho copias, respondió que el código no aparecía.

La estimación para ocho copias fue de aproximadamente 12,880 tokens, sin contar con exactitud las instrucciones y el resto del mensaje.

Este resultado muestra que, al aumentar la cantidad de texto, el modelo puede tener dificultades para recuperar información específica. Sin embargo, no demuestra por sí solo que se haya alcanzado el límite máximo de la ventana de contexto.

En la prueba de posición, el modelo identificó correctamente el código cuando se encontraba al inicio, a la mitad y al final del documento.

Para CiberEscudo, mediría la extensión de los documentos antes de enviarlos al modelo. Si fueran muy extensos o el modelo omitiera datos importantes, los dividiría en secciones y comprobaría las respuestas con el documento original.

## Decisión

**Modelo elegido:** ChatGPT, como selección inicial para desarrollar y probar CiberEscudo, porque fue la herramienta disponible durante este laboratorio.

**Configuración para tareas de precisión:** utilizar instrucciones claras, solicitar respuestas concretas y verificar la información con fuentes confiables. Si la plataforma permite controlar la temperatura, se probaría un valor bajo, como 0.2.

**Configuración para tareas creativas:** solicitar varias alternativas mediante instrucciones explícitas. Si la plataforma permite controlar la temperatura, se probaría un valor más alto, como 1.0.

**Restricciones de datos:** no introducir contraseñas, claves privadas, información bancaria, datos personales innecesarios ni documentos confidenciales sin autorización. Las respuestas generadas por la inteligencia artificial deben revisarse antes de utilizarlas para tomar decisiones relacionadas con la ciberseguridad.

**Conclusión:** ChatGPT es una opción inicial para el proyecto CiberEscudo, pero la selección es provisional. Antes de utilizarlo con usuarios reales, será necesario probar su precisión, comprobar sus respuestas, evaluar la privacidad y comparar su rendimiento con otras herramientas disponibles.
