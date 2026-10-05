# InternacionalIA

Diagnóstico exploratorio de la internacionalización acelerada frente a la secuencial. Aplicación web de un solo fichero (`index.html`), sin servidor.

**Usar la app:** https://fborrasumh.github.io/internacionalia/ *(disponible cuando se publique)*

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23158465.svg)](https://doi.org/10.5281/zenodo.23158465)

## Qué hace

- **Describe una empresa** con datos generales y **15 dimensiones** agrupadas en cinco bloques (recursos y trayectoria, equipo directivo, conocimiento y redes, capacidades, producto y mercado), valoradas de 1 a 5 o «?» si no se sabe. Las dimensiones se pueden **añadir, quitar o renombrar**, definiendo qué significan el 1 y el 5.
- **Rellena las dimensiones desde un texto libre**: la IA propone un valor con una cita literal y el código comprueba que la cita está en el texto; las no verificadas quedan desmarcadas.
- **Diagnóstico exploratorio** razonado por la IA: potencial (de bajo a alto), escenario más plausible (acelerado, secuencial o mixto), factores favorables y limitantes con el dato en que se apoyan, el mecanismo causal y la perspectiva teórica (Uppsala, International New Ventures / born globals, redes, recursos y capacidades, emprendimiento internacional, digitalización), patrones entre dimensiones, comparación secuencial frente a acelerado, preguntas para afinar el diagnóstico y gráfico del efecto de cada dimensión (−2 a +2).
- **Simulación «¿qué ocurriría si…?»**: se cambian una o varias dimensiones y se compara con el diagnóstico base.
- **Evaluación crítica de la IA**: estabilidad (repite el diagnóstico), respeto a la información ausente (oculta una dimensión) y fundamentación de cada factor.
- **Casos docentes**: el profesorado genera con IA un caso ficticio con 5 preguntas y una guía con referencia, lo edita y lo exporta (Word y JSON; la ficha del alumnado no incluye la guía).
- **Alumnado**: abre un caso (el de ejemplo, uno de su profesor/a o uno generado con IA), valora el efecto de cada dimensión y **compara su análisis** con la guía del caso o con un diagnóstico independiente de la IA. No pone notas.
- **Exporta** informe en Word, CSV de efectos por dimensión y el proyecto completo en JSON (sin claves).

## Qué comprueba el código (y qué hace la IA)

La IA propone; el código comprueba:

- Que la evidencia de cada factor es una **cita literal** de los datos introducidos, o «dimensión: N/5» con el valor correcto. Si no, el factor se marca con ⚠.
- Que las dimensiones **sin información** tienen efecto 0 (si la IA les asigna uno, se corrige y se avisa), que no se usan como factor y que generan una pregunta (si la IA no la formula, la añade el código).
- Que hay un efecto por cada dimensión (sin repetidas ni inventadas) y que está entre −2 y +2.
- Que el potencial es coherente con la media de efectos y que ningún factor está clasificado en sentido contrario al efecto que la IA asigna a su dimensión.
- Que la IA no introduce **cifras ni años** que no estén en los datos (posibles referencias inventadas) ni perspectivas fuera del marco.
- En la simulación: variaciones grandes en dimensiones no modificadas y contradicciones entre la dirección que dice la IA y la suma de cambios.
- En los casos: que la narrativa no nombre literalmente las dimensiones, la longitud, el número de preguntas y la coherencia del tipo de proceso con la referencia.
- La comparación del alumnado con la referencia la calcula el código.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador y no aparece en ningún fichero exportado. Cada persona paga su uso: la app indica cuántas llamadas hace cada paso (diagnóstico, 1; estabilidad, de 1 a 4 adicionales; caso docente, 1; diagnóstico independiente de un caso, 2).

## Privacidad

Los datos de la empresa, los diagnósticos y los casos se guardan solo en el navegador (IndexedDB). A tu proveedor de IA sale el perfil de la empresa con correos, teléfonos y DNI/NIE enmascarados y, por defecto, **sin el nombre de la empresa**. Antes del primer envío de cada sesión se muestra exactamente lo que sale. El enmascarado solo cubre esos patrones: no pegues datos personales ni confidenciales que no quieras enviar.

## Límites

- Es un **diagnóstico exploratorio y de apoyo al análisis**. No es una predicción, no determina si una empresa debe internacionalizarse de forma acelerada ni valida empíricamente los determinantes de la internacionalización, y no sustituye un análisis académico o empresarial rigurosos.
- Los efectos por dimensión son **estimaciones cualitativas del modelo**, no coeficientes. El resultado depende de la información introducida y de valoraciones subjetivas (escala 1–5).
- El modelo puede variar entre ejecuciones; la prueba de estabilidad sirve para medirlo.
- La IA no tiene acceso a datos reales de la empresa ni del mercado. Las dimensiones añadidas no tienen perspectiva teórica asociada.
- La referencia con la que se compara el alumnado (guía del caso o diagnóstico independiente) es una estimación de la IA, no una respuesta correcta única.
- **Pruebas realizadas:** lógica y comprobaciones con casos en los que la IA «miente» a propósito, flujo completo con respuestas simuladas de los tres proveedores y revisión en escritorio y móvil. **No se ha probado con claves reales** de OpenAI, Gemini ni Claude, ni la calidad de los diagnósticos con empresas reales.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y María Antonia Vaquero Sánchez (Universidad Miguel Hernández de Elche).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · María Antonia Vaquero Sánchez [0009-0000-1724-5301](https://orcid.org/0009-0000-1724-5301)

## Cómo citar

Borrás Rocher, F. y Vaquero Sánchez, M. A. (2026). *InternacionalIA* (v1.0.0) [Software]. Universidad Miguel Hernández de Elche. DOI: [10.5281/zenodo.23158465](https://doi.org/10.5281/zenodo.23158465)

## Licencia

MIT. Véase [LICENSE](LICENSE).
