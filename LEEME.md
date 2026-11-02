# EcoLab — Programación en Finanzas (FIN443)

Estado: estructura inicial preparada para la actividad del bloque 2 de la clase 3. El nombre del grupo está confirmado; el número, integrantes, repositorio remoto, datos y propuesta definitiva están pendientes de confirmación.

## Pregunta provisional

¿Las estrategias de asignación basadas en riesgo mejoran el rendimiento ajustado por riesgo de una cartera equiponderada fuera de muestra, después de considerar costos de transacción?

La pregunta se propone a partir del tema indicado por el grupo: construir estrategias y portafolios, evaluar sus rendimientos y respaldar los resultados con papers científicos. No representa todavía una propuesta aprobada por todos los integrantes.

## Diseño propuesto

Comparar una cartera equiponderada con mínima varianza, inversa de volatilidad y contribuciones iguales al riesgo (ERC). Estimar los pesos con ventanas históricas y aplicarlos solamente después de la fecha de estimación. Evaluar CAGR, volatilidad, Sharpe, caída máxima, rotación y Sharpe neto de costos. Las conclusiones pueden indicar que una estrategia no mejora al benchmark.

## Datos

Pendiente: definir universo, fuente autorizada, período, frecuencia y tratamiento de activos retirados. Documentar ajustes por splits y dividendos y la fecha de descarga. No usar los datos simulados del curso como evidencia sobre rendimientos reales de mercado.

## Estructura

- datos/: archivos originales y documentación de su procedencia.
- codigo/: scripts y pruebas reproducibles.
- resultados/: salidas generadas automáticamente.
- AGENTS.md: instrucciones para Codex y convenciones del proyecto.
- PROPUESTA_BORRADOR.md: diseño inicial para revisión del grupo.

## Ejecución prevista

Desde la raíz del repositorio, una vez implementado el programa:

```text
Rscript codigo/ejecutar.R datos/precios.csv resultados 0.05
```

Este es el contrato propuesto; ejecutar.R todavía no existe. No se presenta el proyecto como un backtest ya implementado. El script deberá crear las salidas y ejecutarse sin intervención manual ni rutas fijas. Se registrará la versión de R y las dependencias utilizadas.

## Control del sesgo principal

El riesgo principal es el sobreajuste: probar muchas estrategias, ventanas o parámetros y seleccionar retrospectivamente la mejor. Antes de evaluar, registrar estrategias, parámetros, costos, benchmark y criterio de selección. Reservar el tramo final de datos para una sola evaluación, sin ajustar el modelo después de conocer ese resultado. Conservar un registro de todas las variantes probadas.

También se controlará look-ahead: los pesos de una fecha solo podrán depender de información disponible hasta ese momento. Una prueba cambiará los datos futuros y comprobará que no cambian los pesos ya decididos.

## Referencias y trazabilidad

Las referencias aún están en selección. Verificar título, autores, año, DOI y afirmación respaldada; registrar los artículos descartados por estar usados en la sección. No declarar exclusividad ni cuartil JCR sin evidencia. Registrar el apoyo de IA, las correcciones humanas y las pruebas ejecutadas.
