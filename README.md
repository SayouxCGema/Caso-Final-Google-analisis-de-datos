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
Nota: Solo se hace el análisis en las tablas que registran los minutos de sueño y los minutos de actividad diaria. El proceso de limpieza de datos, se aplicó en igual orden en ambas tablas.
