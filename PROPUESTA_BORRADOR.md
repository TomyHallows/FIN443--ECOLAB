# Propuesta inicial — EcoLab

Estado: borrador para revisión del grupo, preparado el 2 de noviembre de 2026. No es la propuesta definitiva ni acredita cumplimiento del requisito de cinco referencias del proyecto.

**Pregunta:** ¿Las estrategias de asignación basadas en riesgo mejoran el rendimiento ajustado por riesgo de una cartera equiponderada fuera de muestra y después de costos?

**Motivación:** una cartera elegida con toda la historia puede parecer superior sin que esa ventaja sea reproducible. Interesa distinguir mejoras implementables de resultados atribuibles a selección retrospectiva y costos omitidos.

**Datos:** universo de activos, fuente, período y frecuencia pendientes de acuerdo. Se documentarán disponibilidad histórica, activos retirados, eventos corporativos, faltantes y permisos de uso.

**Método propuesto:** implementar en R carteras equiponderada, mínima varianza, inversa de volatilidad y ERC. Fijar previamente el esquema de estimación y rebalanceo. Evaluar por ventanas cronológicas, usando únicamente el pasado para decidir. Comparar CAGR, volatilidad, Sharpe, caída máxima y rotación antes y después de costos. Elegir el test estadístico una vez fijadas las hipótesis y las referencias metodológicas.

**Aporte propio propuesto:** construir una comparación reproducible sobre el universo elegido, analizar sensibilidad a costos e incorporar una prueba automática que cambie el futuro y exija conservar las decisiones históricas. No se afirma originalidad científica sin revisar la literatura.

**Sesgo principal:** sobreajuste por selección entre numerosas variantes. Prevención: protocolo previo, registro de experimentos y muestra final reservada. Controles adicionales: causalidad temporal, supervivencia y costos.

**Referencias:** pendientes de selección final y verificación de disponibilidad en la sección. Cada paper deberá respaldar una afirmación específica y contar con referencia APA, DOI y PDF cuando corresponda.

**Pendientes del grupo:** número e integrantes; aprobar pregunta; definir datos; seleccionar referencias; crear o identificar repositorio; agregar colaboradores y profesor con sus usuarios confirmados.
