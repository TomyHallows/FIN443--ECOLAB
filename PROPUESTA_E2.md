# E2 — EcoLab: propuesta para inscripción

Estado: propuesta preparada el 9 de noviembre de 2026, pendiente de aprobación del profesor. No se ha iniciado el análisis empírico.

## Pregunta
¿Las carteras de mínima varianza y paridad de riesgo superan a una cartera equiponderada en Sharpe neto de costos fuera de muestra sobre diez sectores estadounidenses entre 2007 y 2025?

## Equipo
- Joaquín Gutierrez — @joaquingutierrezf.
- Tomás Hallows — @TomyHallows.
- Cristobal Jara — @cristobalj13.
- Santiago Liu — @saduniform90.
- José Tomás Moran — @jtomasmoran.

Las cuentas invitadas deben aceptar las invitaciones. Profesor: @rodrigo-ortizh, colaborador confirmado. Los RUT y correos se incluyen en la inscripción privada, no en este repositorio público.

## Datos propuestos
Kenneth French Data Library, “10 Industry Portfolios [Daily]”: retornos sectoriales ponderados por capitalización. Fuente: https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html
Período 2006–2025; 2006 para estimación inicial y evaluación desde el primer rebalanceo elegible de 2007. Para sensibilidad de 504 días se requiere historia previa adicional o un período de evaluación común; no se compararán intervalos diferentes sin declararlo.
Tasa libre de riesgo diaria: archivo diario de factores Fama/French de la misma biblioteca, con fechas alineadas.
Conservar una copia fechada de los datos, su checksum y las condiciones de uso; verificar permiso de redistribución. No se ha descargado ni validado aún esta base.
Los sectores son portafolios de investigación, no ETF negociables. Los costos son escenarios de reasignación entre sectores, no costos observados ni una reproducción completa de la operativa subyacente.

## Método propuesto
Implementación en R de equiponderada, mínima varianza sin ventas cortas (optimización restringida) y contribuciones iguales al riesgo (ERC). Pesos suman uno; estimación con 252 observaciones previas, incluido el cierre de rebalanceo, aplicación a partir del día siguiente.
Rebalanceo mensual. Entre rebalanceos se dejan derivar los pesos con los retornos; medir rotación frente a esos pesos previos a la operación, incluyendo la inversión inicial.
Evaluar CAGR, volatilidad, Sharpe con exceso diario sobre la tasa libre de riesgo diaria, caída máxima, rotación y métricas netas.
Escenarios de costos propuestos: 0, 10, 25 y 50 puntos base por unidad transada. Fijar las convenciones de costos y las hipótesis antes de evaluar.
Desarrollo y validación cronológicos en 2007–2015; tramo final 2016–2025 reservado sin ajustes retrospectivos. Reportar los períodos por separado además de la historia completa.

## Aporte propio
Estimar el costo a partir del cual cada estrategia pierde su ventaja de Sharpe frente a la equiponderada. Si nunca tiene ventaja o no hay cruce en el rango evaluado, informarlo sin forzar un umbral. Analizar sensibilidad de ventana en fechas comunes.

## Validación prevista
Casos manuales pequeños, restricciones de pesos, igualdad de contribuciones ERC, costos nulos, inversión inicial, deriva de pesos, modificación de datos futuros sin alterar decisiones pasadas, invariancia al orden de columnas y comprobación de unidades porcentuales/faltantes.
Las diferencias observadas de Sharpe no se declararán significativas sin inferencia apropiada; si se comparan múltiples variantes, considerar dependencia temporal y multiplicidad.

## Referencias iniciales candidatas
Existencia y datos bibliográficos revisados en el trabajo previo. Registro en el foro E2, disponibilidad, cuartil JCR y asignación de responsables pendientes; no se presentan como referencias ya reservadas.

1. Cederburg, S., O’Doherty, M. S., Wang, F., & Yan, X. S. (2020). On the performance of volatility-managed portfolios. *Journal of Financial Economics, 138*(1), 95–117. https://doi.org/10.1016/j.jfineco.2020.04.015
   Uso propuesto: límites de la extrapolación de resultados dentro de muestra y gestión de volatilidad; no constituye una réplica de ERC.
2. Garlappi, L., Uppal, R., & Wang, T. (2007). Portfolio selection with parameter and model uncertainty: A multi-prior approach. *The Review of Financial Studies, 20*(1), 41–81. https://doi.org/10.1093/rfs/hhl003
   Uso propuesto: incertidumbre de estimación y contexto de robustez; no se afirma implementar su modelo.
3. Romano, J. P., & Wolf, M. (2005). Stepwise multiple testing as formalized data snooping. *Econometrica, 73*(4), 1237–1282. https://doi.org/10.1111/j.1468-0262.2005.00615.x
   Uso propuesto: comparaciones múltiples y límites de elegir retrospectivamente la mejor estrategia.

## Pendientes de inscripción
Aceptación de invitaciones pendientes; número de grupo y nomenclatura fin443-grupoXX; comprobar cuartiles JCR y registrar tres referencias disponibles en el foro E2; enviar inscripción con copia a los cinco integrantes y obtener visto bueno.
