# Instrucciones para Codex — EcoLab

## Contexto

Proyecto del curso FIN443, Programación en Finanzas. Consultar LEEME.md y la propuesta antes de editar. La pregunta provisional compara estrategias basadas en riesgo con una cartera equiponderada fuera de muestra y después de costos. No convertir decisiones pendientes en hechos.

## Convenciones y contrato propuestos

- Usar R, funciones explicables y rutas relativas a la raíz del proyecto.
- Conservar datos originales en datos/; escribir productos en resultados/.
- Comando previsto para E2: Rscript codigo/main.R; datos y configuración se documentarán en la propuesta. No afirmar que funciona hasta implementarlo y ejecutarlo.
- Retornos simples; volatilidad muestral anualizada por sqrt(252); para E2 usar la tasa libre de riesgo diaria de la fuente y Sharpe de excesos diarios, según PROPUESTA_E2.md. No trasladar automáticamente la tasa fija de los desafíos.
- CAGR por días calendario/365.25, unidades en fracciones en archivos y redondeo únicamente para presentación.
- Registrar las convenciones definitivas de rebalanceo, pesos entre rebalanceos, rotación, costos y financiación. No confundir un ejercicio del curso con un backtest de mercado implementable.
- Para entregas individuales, seguir el contrato exacto de su enunciado, que prevalece sobre este diseño provisional.

## Validación crítica

1. Extraer los requisitos antes de programar y relacionarlos con pruebas concretas.
2. Inspeccionar fechas, duplicados, formatos, faltantes, activos de inicio tardío y eventos corporativos.
3. No usar información futura para limpiar datos, escoger universo, estimar parámetros o decidir pesos. Verificar el efecto de los ajustes históricos sobre la causalidad del pipeline completo.
4. Fijar estrategias, parámetros, benchmark y costos antes de evaluar. Registrar todas las pruebas, incluidas las que no dieron buenos resultados.
5. Separar desarrollo, validación y evaluación final cronológicamente. No retocar la estrategia usando el período final.
6. Probar invariancia de pesos pasados al modificar el futuro, sumas de pesos, resultados manuales pequeños y exportación de archivos.
7. Para afirmar una mejora, distinguir magnitud económica de evidencia estadística; considerar comparaciones múltiples cuando corresponda.
8. Reportar limitaciones, pruebas realmente ejecutadas y resultados desfavorables. No prometer calificaciones ni rendimientos.

## Evidencia e integridad

No inventar datos, resultados, referencias, integrantes, números de grupo, enlaces, cuartiles ni verificaciones. Verificar artículos en fuentes primarias y vincularlos a afirmaciones concretas. No presentar una adaptación como réplica exacta. Documentar ayuda de IA y revisión humana. Mantener un solo contenido de instrucciones si se crean versiones para otras herramientas.
