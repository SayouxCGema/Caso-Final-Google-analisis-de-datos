# Portafolio
## Introducción
- Presentación del trabajo final curso de Google Data Analytics.
- Introducción
- Fuentes de datos
- Proceso de limpieza y manipulación de datos
- Análisis
- Conclusiones




La empresa de Bellabeat es un fabricante de productos de alta tecnología orientados a la salud de la mujer. Urška Sršen, cofundadora y directora creativa de Bellabeat, cree que analizar los datos de actividad física de los dispositivos inteligentes podría desplegar nuevas oportunidades de negocio para la empresa.

Recopilar datos sobre la actividad física, el sueño, el estrés y la salud reproductiva le ha permitido a Bellabeat proporcionar a las mujeres conocimientos sobre su propia salud y sus hábitos. Desde su fundación, en 2013, Bellabeat creció a un ritmo vertiginoso y rápidamente se posicionó como empresa de bienestar impulsada por la tecnología para las mujeres.

El CEO de la empresa, necesita analizar los datos de uso de dispositivos inteligentes y recibir recomendaciones sobre cómo estas tendencias pueden colaborar en la estrategia de marketing de Bellabeat.




Fuentes de datos

[La fuente de datos utilizada para el análisis, está publicada en la plataforma de Kaggle](https://www.kaggle.com/datasets/arashnic/fitbit/data)

Es una base de datos que incluye el registro de treinta usuarios elegibles de Fitbit, los cuales han dado su consentimiento para el envío de datos personales de seguimiento, incluidos los resultados a nivel de minuto de la actividad física, la frecuencia cardíaca y la monitorización del sueño.



# Limpieza de los datos:
- El proceso de limpieza y manipulación de datos, lo realizo en las bases de datos con las que vamos a trabajar.
- Los datos nos dicen que contamos con un total de 940 filas y ningún valor nulo. La variable de fechas, está en un formato incorrecto y debemos modificarlo
- Algunos datos son mediciones en kilometros, mientras que otros son de minutos. Voy a escoger las variables de minutos para el análisis. [Fuente- Fitabase Data Dictionary](https://www.fitabase.com/media/1930/fitabasedatadictionary102320.pdf)
- Unificación de las tablas ya que estas estan por separado


# Análisis:
[Según la OMS](https://www.who.int/es/news-room/fact-sheets/detail/physical-activity) para que los adultos puedan estar con una adecuado estado de salud, deben realizar un mínimo de *30 minutos* de actividad física diaria. Estas se pueden distribuir en actividades físiscas más intensas durante al menos 150 a 300 minutos; o actividades físicas aeróbicas intensas durante al menos 75 a 150 minutos; o una combinación de ambas en la semana.

- Nuestra base de clientes, está teniendo un 73,3%  de minutos sedentarios. Lo cual no es recomendable, para tener una buena condición física. Mientras que solo un 2,6% de estos minutos, se dedican a minutos de actividad física más deportiva.

Se crea una variable para definir si los usuarios son personas de una intensa actividad física o no.
- Variable: **VeriActiveMinute<30** usuarios no deportivos **VeriActiveMinute>30** usuarios deportivos
Tenemos que un 68% de los usuarios no superan los 30 minutos de actividad física y solo un 32% de los usuarios si.

[Según una investigación publicada en el European Journal of Preventive Cardiology](https://academic.oup.com/eurjpc/article/30/18/1975/7226309?login=false) ,que analizó la relación entre los pasos diarios dados por las personas y el riesgo de muerte. Los investigadores encontraron que caminar 4.000 pasos al día reducía el riesgo de muerte por cualquier causa. Considerando que 4.000 pasos vienen a ser el equivalente a los 22 minutos mínimos de actividad física recomendados, estos ya mostraban beneficios a nivel de mortalidad.

- En base a ello, se crea una variable para definir el % de los usuarios que realizan menos de 4000 pasos diarios o no:
- Tenemos un 83.2% de usuarios que si realizan esta cantidad de pasos al día, mientras que solo el 16.8% no lo consiguen.

[Según ha publicado el The National Heart, Lung, and Blood Institute (NHLBI)(https://www.nhlbi.nih.gov/files/docs/public/sleep/In_Brief_YG_to_Sleep_Spanish_Final.pdf), en la edad adulta las horas de sueño deben de estar entre 7-8 horas. Escatimar sueño tiene su precio. Reducir tan solo 1 hora de sueño puede hacer que sea difícil concentrarse al día siguiente y que su tiempo de respuesta sea más lento. También afecta al estado anímico. Además de que tiene un gran impacto en nuestro estado de salud.

En base a ello, se crea una variable para agrupar a los usuarios que tienen al menos 7 horas de sueño y los que no.
- Se ha detectado que el día que mejor registro de calidad de las horas de sueño en la semana, suele ser los miércoles. Mientras que los martes, se muestra el día con menor cantidad de horas de sueño.
- Un 66.6% de los usuarios si que duermen diariamente las 7 horas mínimas para un correcto descanso, mientras que 33.7% no lo hace.


# Conclusiones y recomendaciones:
- El usuario parece que tiene mayor calidad de sueños el miércoles.
- Un 66% de las veces, está una buena calidad de sueño con un mínimo de 7 horas.
- Hasta ahora, se observa que los usuarios si que pueden tener una media de pasos diarios adecuadas, aunque no por ello se pueden definir como usuarios con una intensa actividad física.
- Los minutos registran que mayoritariamente los usuarios tienen más tendencia a minutos sedentarios, un 73.3%.

# Estrategias equipo de marketing:
-Para la estrategia de marketing que desea realizar el equipo de Bellabeat, se puede recomendar enfocarse en la importancia de conseguir realizar los 30 minutos de actividad física diaria. 
- Por ejemplo pueden crear un anuncio realizando un embudo, enfocado en atraer a los usuarios que necesitan mejorar su actividad física y calidad de sueño. Para ello, necesitan crear un prototipo de clientes con mayor cantidad de datos (demográficos, educación, etc)
- Se pueden enviar newsletter, informando sobre los benficios de la actividad física y como los productos de Blellabeat, podrían ayudarles a realizar el seguimiento de las mejoras.
- Se pueden enviar alertas al final de cada día, donde se haga un resumen de la actividad diaria y que les muestre un resumen de (calorías, km realizados, minutos de actividad).




Nota: Solo se hace el análisis en las tablas que registran los minutos de sueño y los minutos de actividad diaria. El proceso de limpieza de datos, se aplicó en igual orden en ambas tablas.
