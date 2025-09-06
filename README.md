# Informe de Prestamos Bancarios

Para monitorear y evaluar las actividades crediticias y el desempeño de nuestro banco, necesitamos crear un Informe de Préstamos Bancarios completo. Este informe tiene como objetivo proporcionar información sobre las métricas clave relacionadas con los préstamos y sus cambios a lo largo del tiempo. El informe nos ayudará a tomar decisiones basadas en datos, realizar un seguimiento de la salud de nuestra cartera de préstamos e identificar tendencias que pueden informar nuestras estrategias de préstamos.

## Tabla de contenido
- [Descripción general del proyecto](#descripción-general-del-proyecto)
- [Fuente de datos](#fuente-de-datos)
- [Herramientas](#herramientas)
- [Limpieza de datos y preparacion](#limpieza-de-datos-y-preparacion)
- [EDA Analisis exploratorio de datos](#eda-analisis-exploratorio-de-datos)
- [Graficos requeridos](#graficos-requeridos)

### Descripción general del proyecto

En nuestro proyecto Informe de préstamos bancarios, nuestro objetivo es representar visualmente métricas y tendencias críticas relacionadas con los préstamos utilizando una variedad de tipos de gráficos. Estos gráficos proporcionarán una visión clara y perspicaz de nuestras operaciones de préstamo, facilitando la toma de decisiones basada en datos y permitiéndonos obtener información valiosa sobre varios parámetros de préstamos.

<img width="1150" height="598" alt="Screenshot 2025-09-06 174251" src="https://github.com/user-attachments/assets/7129bf29-2e25-4c4c-bde0-96b7df8d1c40" />

<img width="1156" height="593" alt="Screenshot 2025-09-06 172120" src="https://github.com/user-attachments/assets/c52bb4fe-ad1b-4f93-8f47-f78fc2b27f09" />



### Fuente de datos

Prestamos_finacieros: Este dataset contiene información detallada sobre solicitudes y comportamiento de préstamos bancarios, útil para análisis financiero, segmentación de riesgo y visualización estratégica. Las columnas incluyen:

- id_prestamo: Identificador único del préstamo

- estado: Estado geográfico del solicitante

- tipo_de_aplicacion: Individual o conjunta

- años_trabajando: Antigüedad laboral declarada

- ocupacion: Tipo de empleo del solicitante

- riesgo / sub_riesgo: Clasificación de riesgo crediticio

- tipo_de_vivienda: Propia, alquilada o hipotecada

- fecha_de_emicion: Fecha de emisión del préstamo

- ultima_fecha_consulta_credito: Última revisión del historial crediticio

- fecha_del_ultimo_pago / fecha_del_proximo_pago: Historial de pagos

- estado_del_prestamo: Activo, cerrado, en mora, etc.

- id_deudor: Identificador del solicitante

- proposito: Motivo del préstamo (personal, auto, educación, etc.)

- duracion: Plazo del préstamo en años

- estado_de_verificacion: Validación de ingresos u otros datos

- ingresos_anuales: Ingreso declarado por el solicitante

- relacion_deuda_ingreso: Ratio entre deuda y ingreso

- cuota: Pago mensual estimado

- tipo_de_interes: Fijo o variable

- monto_del_prestamo: Valor total solicitado

- total_acc: Número de cuentas abiertas del solicitante

- pago_total: Suma total pagada hasta la fecha


### Herramientas

  - Excel - Limpieza de datos, Visualizacion de datos, Dashboard

### Limpieza de datos y preparacion 

En la fase inicial realizamos las siguientes tareas:
1. Carga e inspección de datos
2. Manejo de valores nulos y duplicados
3. Correccion de valores a un formato adecuado

### EDA Analisis exploratorio de datos

#### Explorar los datos bancarios para responder preguntas clave de rendimiento, como:
1.	Total de solicitudes de préstamo: Necesitamos calcular el número total de solicitudes de préstamo recibidas durante un período específico. Además, es esencial monitorear las solicitudes de préstamos mensuales hasta la fecha (MTD) y realizar un seguimiento de los cambios mes a mes (MoM).

2.	Monto total financiado: Comprender la cantidad total de fondos desembolsados como préstamos es crucial. También queremos vigilar el monto total financiado de MTD y analizar los cambios mes a mes (MoM) en esta métrica.

3.	Monto total recibido: El seguimiento del monto total recibido de los prestatarios es esencial para evaluar el flujo de efectivo del banco y el reembolso del préstamo. Debemos analizar el monto total recibido mes hasta la fecha (MTD) y observar los cambios mes a mes (MoM).

4.	Tasa de interés promedio: El cálculo de la tasa de interés promedio en todos los préstamos, MTD, y el monitoreo de las variaciones mes a mes (MoM) en las tasas de interés proporcionará información sobre el costo total de nuestra cartera de préstamos.

5.	Relación deuda-ingreso promedio (DTI): Evaluar el DTI promedio de nuestros prestatarios nos ayuda a medir su salud financiera. Necesitamos calcular el DTI promedio para todos los préstamos, MTD y realizar un seguimiento de las fluctuaciones mes a mes (MoM).

#### KPI de préstamos buenos vs préstamos incobrables
Para evaluar el rendimiento de nuestras actividades crediticias y evaluar la calidad de nuestra cartera de préstamos, necesitamos crear un informe completo que distinga entre "Préstamos buenos" y "Préstamos incobrables" en función de criterios específicos del estado del préstamo
##### KPI de buenos préstamos:
1.	Porcentaje de solicitud de préstamo bueno: Necesitamos calcular el porcentaje de solicitudes de préstamo clasificadas como 'Préstamos buenos'. Esta categoría incluye préstamos con un estado de préstamo de 'Totalmente pagado' y 'Actual'.
2.	Solicitudes de préstamos buenos: Identificar el número total de solicitudes de préstamos que se incluyen en la categoría 'Préstamo bueno', que consiste en préstamos con un estado de préstamo de 'Totalmente pagado' y 'Actual'.
3.	Monto financiado por un buen préstamo: Determinar el monto total de los fondos desembolsados como 'Préstamos buenos'. Esto incluye los montos principales de los préstamos con un estado de préstamo de 'Totalmente pagado' y 'Actual'.
4.	Monto total recibido de un préstamo bueno: Seguimiento del monto total recibido de los prestatarios por 'Préstamos buenos', que abarca todos los pagos realizados en préstamos con un estado de préstamo de 'Totalmente pagado' y 'Actual'.
##### KPI de préstamos incobrables:
1.	Porcentaje de solicitudes de préstamos incobrables: Cálculo del porcentaje de solicitudes de préstamos categorizadas como 'Préstamos incobrables'. Esta categoría incluye específicamente préstamos con un estado de préstamo de 'Cancelado'.
2.	Solicitudes de préstamos incobrables: Identificar el número total de solicitudes de préstamos categorizadas como 'Préstamos incobrables', que consiste en préstamos con un estado de préstamo de 'Cancelado'.
3.	Monto financiado por préstamos incobrables: Determinar la cantidad total de fondos desembolsados como 'Préstamos incobrables'. Esto comprende los montos principales de los préstamos con un estado de préstamo de 'Cancelado'.
4.	Monto total recibido de préstamos incobrables: Seguimiento del monto total recibido de los prestatarios por 'Préstamos incobrables', que incluye todos los pagos realizados en préstamos con un estado de préstamo de 'Cancelado'.

### Graficos requeridos
1. Tendencias mensuales por fecha de emisión (gráfico de líneas):Este gráfico de líneas mostrará cómo el "Total de solicitudes de préstamo", el "Monto total financiado" y el "Monto total recibido" varían con el tiempo, lo que nos permitirá identificar la estacionalidad y las tendencias a largo plazo en las actividades de préstamo.

2. Análisis regional por estado (mapa completo):Este mapa completo representará visualmente las métricas de préstamos categorizadas por estado, lo que nos permitirá identificar regiones con una actividad crediticia significativa y evaluar las disparidades regionales.

3. Análisis del plazo del préstamo (gráfico de anillos): Este gráfico de anillos mostrará estadísticas de préstamos basadas en diferentes términos de préstamo, lo que nos permitirá comprender la distribución de préstamos en varias duraciones de plazo.

4. Análisis de la longitud de los empleados (gráfico de barras): Este gráfico de barras ilustrará cómo se distribuyen las métricas de préstamos entre los prestatarios con diferentes duraciones de empleo, lo que nos ayudará a evaluar el impacto del historial de empleo en las solicitudes de préstamos.

5. Desglose del propósito del préstamo (gráfico de barras): Este gráfico de barras proporcionará un desglose visual de las métricas de préstamos basadas en los propósitos declarados de los préstamos, lo que ayudará a comprender las razones principales por las que los prestatarios buscan financiamiento.

6. Análisis de propiedad de vivienda (mapa de árbol): Este mapa de árbol mostrará métricas de préstamos categorizadas por diferentes estados de propiedad de vivienda, lo que permitirá una visión jerárquica de cómo la propiedad de la vivienda afecta las solicitudes y desembolsos de préstamos.
