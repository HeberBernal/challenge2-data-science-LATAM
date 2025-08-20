 Mi objetivo con este proyecto fue realizar un análisis de datos para entender el problema de la evasión de clientes (conocido como Churn). Buscaba identificar los factores clave que llevan a nuestros clientes a cancelar su servicio, lo cual nos permitirá desarrollar estrategias efectivas para retenerlos, mejorar nuestra rentabilidad y asegurar la sostenibilidad de la empresa a largo plazo.

🔹 Limpieza y Tratamiento de Datos
El primer paso de mi análisis fue asegurar la calidad de los datos. Para ello, importé la base de datos telecom_customer_churn.csv a un entorno de Python. Al revisar la información, identifiqué que la columna de TotalCharges contenía 11 valores nulos y estaba guardada como tipo de texto en lugar de un número. Para corregirlo, eliminé los registros con valores nulos y convertí la columna al tipo de dato numérico (float). También, decidí eliminar la columna customerID, ya que es un identificador único que no tiene valor para el análisis predictivo. Con estos pasos, la base de datos quedó lista para ser explorada.

🔹 Análisis Exploratorio de Datos (EDA)
Mi análisis exploratorio reveló hallazgos importantes sobre el comportamiento de nuestros clientes:

Tasa de Evasión: Descubrí que la tasa de Churn es del 26.5%, lo que representa una porción considerable de nuestra base de clientes y subraya la urgencia de actuar.
<img width="917" height="617" alt="image" src="https://github.com/user-attachments/assets/094bb42c-2a3e-4b60-814c-6bb5f0ca348e" />


Factores Demográficos: Analicé variables como el género y el estado civil. Los datos mostraron que no hay una diferencia notable en la evasión por género. Sin embargo, encontré que los clientes que no tienen dependientes tienen una mayor probabilidad de irse.

Duración del Servicio (Tenure): Aquí está el punto más crítico. Pude identificar una correlación muy fuerte: los clientes que más se van son los que tienen poco tiempo con la empresa. Por ejemplo, al visualizar los datos, se ve claramente cómo la tasa de Churn es mucho más alta en los primeros meses de servicio.

Servicios Contratados: Un análisis de los servicios adicionales reveló que los clientes que contratan servicios como seguridad en línea, soporte técnico o protección de dispositivos tienen una tasa de evasión notablemente más baja. Esto me dice que el valor agregado en los servicios es un factor clave en la retención.
<img width="451" height="640" alt="image" src="https://github.com/user-attachments/assets/f19aaf00-50fb-4ccb-8fc4-c9906a0a0965" />

<img width="1133" height="325" alt="image" src="https://github.com/user-attachments/assets/3fafa5fa-0ce6-4d35-b533-f51c057d413b" />


🔹 Conclusiones e Insights
A partir de mis análisis, pude extraer las siguientes conclusiones:

Vulnerabilidad del Primer Año: La etapa más crítica para la retención de clientes es el primer año de servicio. Si logramos que los clientes superen ese período, su lealtad aumenta drásticamente.

El Valor Agregado Fomenta la Lealtad: Ofrecer servicios de seguridad y soporte no solo nos genera ingresos, sino que funciona como una "ancla" para los clientes, haciéndolos menos propensos a buscar a la competencia.

Perfil de Cliente en Riesgo: He identificado un perfil de cliente con alto riesgo de Churn: es un cliente nuevo, que no tiene dependientes y que no ha contratado servicios adicionales de seguridad o soporte técnico.

🔹 Recomendaciones
Con base en todo lo que les acabo de mostrar, les propongo las siguientes sugerencias estratégicas para reducir la evasión de clientes:

Implementar un Programa de Bienvenida: Necesitamos un plan de contacto proactivo para los nuevos clientes durante sus primeros 6-12 meses. Podemos ofrecer llamadas de seguimiento, encuestas de satisfacción o tutoriales para asegurar una experiencia positiva desde el principio.

Promover la Adopción de Servicios Adicionales: Les propongo que ofrezcamos períodos de prueba gratuitos o descuentos en paquetes que incluyan servicios de seguridad y soporte. Esto no solo aumentaría la retención, sino también los ingresos a largo plazo.

Desarrollar un Modelo Predictivo de Churn: Utilizando los datos, podemos construir un modelo de aprendizaje automático que identifique a los clientes en riesgo en tiempo real. Esto nos permitiría intervenir de forma personalizada con ofertas de retención antes de que decidan irse.
