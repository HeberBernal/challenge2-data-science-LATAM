# challenge2-data-science-LATAM
1. Introducción
El objetivo de este análisis ha sido comprender el problema de la evasión de clientes, o "Churn", en TelecomX. A través de este proyecto, busqué identificar los factores y perfiles de clientes más propensos a cancelar su servicio, con el fin de proporcionar información valiosa para diseñar estrategias de retención efectivas.

2. Limpieza y Tratamiento de Datos
Mi primer paso fue preparar los datos para el análisis. Importé el archivo TelecomX_Data.json y, utilizando una función personalizada que creé, flatten_df, logré aplanar las estructuras de datos anidadas. Posteriormente, abordé la limpieza de variables críticas:

Valores Ausentes: Convertí la columna account_Charges.Total a un tipo numérico, manejando correctamente los valores vacíos que causaban errores. También me aseguré de que no hubiera valores nulos en la variable objetivo CHURN.

Renombramiento de Columnas: Renombré todas las columnas relevantes a un formato más claro y en español (ANTIGUEDAD_CLIENTE, CARGO_TOTAL, etc.).

Creación de Nuevas Características: Generé una nueva variable, Cuentas_Diarias, para explorar la relación entre el gasto diario y la evasión.

3. Análisis Exploratorio de Datos
He realizado varios análisis para explorar la distribución de la evasión y sus patrones. Mis hallazgos más importantes son:

Tasa de Evasión General: Mi primer análisis, un gráfico de pastel, mostró que el 26.5% de nuestros clientes ha cancelado el servicio, lo que confirma que la evasión es un problema significativo.

Análisis por Variables Categóricas: Los gráficos de barras y los resúmenes de tablas que generé me permitieron identificar las siguientes tendencias:

Contrato: Los clientes con contratos de Month-to-month tienen una tasa de evasión extremadamente alta, superando el 42%.

Método de Pago: Aquellos que pagan con Electronic check tienen la mayor tasa de evasión, con un 45%.

Servicio de Internet: Los clientes con Fiber optic se van con mucha más frecuencia que los de DSL.

Análisis por Variables Numéricas: Los histogramas me ayudaron a entender las diferencias entre los clientes que se quedaron y los que se fueron. Descubrí que los clientes que evaden tienen:

Una antigüedad promedio mucho menor. La mayoría de las cancelaciones ocurren en los primeros meses.

Cargos mensuales más altos en promedio.

Cargos totales más bajos en promedio, lo cual es lógico ya que no han estado con la empresa por mucho tiempo.

4. Conclusiones e Insights
Mis hallazgos confirman que la evasión no es un problema aleatorio. Los clientes que se van comparten un perfil muy claro:

Son clientes recientes con contratos flexibles (mes a mes).

Prefieren servicios de fibra óptica y pagan a través de cheque electrónico.

A pesar de ser clientes nuevos, tienen un alto cargo mensual.

Esto me lleva a pensar que los clientes nuevos, que optan por planes de alta velocidad y un método de pago menos estable, se sienten insatisfechos rápidamente y no tienen una razón para quedarse a largo plazo.

5. Recomendaciones
Basado en mi análisis, propongo las siguientes estrategias para reducir la evasión:

Estrategia de Retención de Clientes Nuevos: Implementar un programa de seguimiento para los clientes con menos de 6 meses de antigüedad y cargos mensuales altos. Esto podría incluir llamadas de cortesía, descuentos en servicios o acceso a soporte premium.

Promociones para Cambios de Contrato: Ofrecer incentivos atractivos (por ejemplo, descuentos o servicios gratuitos) a los clientes con contratos de Month-to-month para que migren a planes de un año o más.

Optimización del Servicio de Fibra Óptica: Investigar posibles problemas técnicos o de rendimiento en el servicio de fibra óptica, ya que su alta tasa de evasión sugiere insatisfacción.

Mejora en el Proceso de Pago: Analizar el método de Electronic check para identificar posibles fricciones o fallos que estén frustrando a los clientes.
