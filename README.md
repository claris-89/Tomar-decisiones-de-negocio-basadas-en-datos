# Tomar-decisiones-de-negocio-basadas-en-datos

### Descripción del Proyecto
En este proyecto, como analista de una tienda online, se busca aumentar los ingresos mediante la evaluación y priorización de hipótesis propuestas por el departamento de marketing y el análisis de una prueba A/B. Se aplicarán marcos como ICE y RICE para clasificar las hipótesis, y se analizarán los resultados del test A/B para tomar decisiones informadas sobre estrategias de negocio.

### Objetivos
1. Priorización de hipótesis:
- Evaluar hipótesis utilizando los frameworks ICE y RICE.
- Identificar las hipótesis con mayor potencial de impacto para aumentar los ingresos.
- Comparar cómo cambia la priorización entre ambos métodos.

2. Análisis del Test A/B:
- Evaluar el comportamiento de los usuarios de los grupos A y B en términos de ingresos, tamaño promedio de pedidos y tasa de conversión.
- Detectar anomalías en los datos y estudiar su impacto.
- Probar la significancia estadística de las diferencias entre grupos.

3. Tomar decisiones basadas en datos:
- Decidir si continuar, detener o concluir la prueba basándose en los resultados obtenidos.

###  Descripción de los Datos
Parte 1: Priorización de Hipótesis
- Hypotheses: Breve descripción de cada hipótesis.
- Reach: Alcance esperado de usuarios (escala de 1 a 10).
- Impact: Impacto esperado en los usuarios (escala de 1 a 10).
- Confidence: Nivel de confianza en la hipótesis (escala de 1 a 10).
- Effort: Recursos necesarios para probar la hipótesis (escala de 1 a 10).

Parte 2: Test A/B
Pedidos:
- Archivo: /datasets/orders_us.csv
- transactionId: Identificador único del pedido.
- visitorId: Identificador único del usuario.
- date: Fecha del pedido.
- revenue: Ingresos generados por el pedido.
- group: Grupo al que pertenece el usuario (A o B).

Visitas:
- Archivo: /datasets/visits_us.csv
- date: Fecha.
- group: Grupo del test A/B.
- visits: Número de visitas en el grupo correspondiente.

### Metodología
Parte 1: Priorización de Hipótesis
1. Aplicación del framework ICE:
- Fórmula: $$\text{ICE} = \frac{\text{Impact} \times \text{Confidence}}{\text{Effort}}$$
- Clasificar las hipótesis en orden descendente según su puntaje ICE.

2. Aplicación del framework RICE:
- Fórmula: $$\text{RICE} = \frac{\text{Reach} \times \text{Impact} \times \text{Confidence}}{\text{Effort}}$$
- Clasificar las hipótesis en orden descendente según su puntaje RICE.

3. Comparación entre ICE y RICE:
- Analizar cómo el factor Reach afecta la priorización.
- Explicar los cambios en el orden de las hipótesis y su impacto.

Parte 2: Análisis del Test A/B
1. Ingresos acumulados:
- Gráficos comparativos del ingreso acumulado para los grupos A y B.
- Identificación de patrones o diferencias significativas.

2. Tamaño promedio de pedido:
- Cálculo y representación gráfica del tamaño de pedido promedio acumulado.
- Evaluar tendencias entre los grupos.

3. Tasa de conversión:
- Fórmula: $$\text{Tasa de Conversión} = \frac{\text{Pedidos}}{\text{Visitas}}$$
- Representar gráficamente las tasas diarias para ambos grupos.

4. Identificación de anomalías:
- Gráficos de dispersión para analizar:
    - Número de pedidos por usuario.
    - Precios de los pedidos.
- Cálculo de percentiles 95 y 99 para definir umbrales de anomalías.

5. Pruebas de significancia estadística:
- Evaluar diferencias en la conversión y el tamaño promedio de pedido:
    - Datos en bruto: Sin filtrar anomalías.
    - Datos filtrados: Excluyendo valores anómalos.
- Metodología: Pruebas t para dos muestras independientes.
- Nivel de significancia: α = 0.05.

6. Decisión basada en resultados:
- Concluir si detener la prueba, declarar un grupo líder o continuar el análisis.

### Colclusión 
Las pruebas A/B son una herramienta valiosa para los negocios, ya que permiten evaluar de manera precisa si los cambios implementados están atrayendo más clientes. Estas pruebas facilitan la mejora continua de la experiencia del usuario, impulsan la conversión y mejoran las tasas de retención. Sin embargo, es crucial analizar los resultados obtenidos para determinar la efectividad de las modificaciones realizadas.

En este trabajo, se llevaron a cabo pruebas A/B para evaluar el impacto de ciertos cambios en el comportamiento de los usuarios. Los resultados mostraron que ni los datos en bruto ni los datos filtrados presentaron diferencias significativas. Específicamente, los datos sin procesar no revelaron una diferencia estadísticamente significativa entre los grupos en términos de tamaño promedio de compra.

Dado que no se observaron diferencias significativas, se concluye que no es conveniente continuar con la prueba. Continuar con ella representaría un gasto innecesario que no justifica los beneficios esperados. Por lo tanto, se recomienda detener la prueba y considerar otras estrategias o enfoques que puedan ser más efectivos para alcanzar los objetivos del negocio.

En resumen, aunque las pruebas A/B son una herramienta poderosa para la optimización de la experiencia del usuario y el aumento de la conversión, es fundamental evaluar los resultados de manera crítica. En este caso, la falta de diferencias significativas sugiere que los cambios implementados no tuvieron el impacto deseado, y por lo tanto, no se justifica seguir invirtiendo recursos en esta prueba específica.
