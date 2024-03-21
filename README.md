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
- Se elimnan valores duplicados.
- Los datos nos dicen que contamos con un total de 940 filas y ningún valor nulo. La variable de fechas, está en un formato incorrecto y debemos modificarlo Algunos datos son mediciones en kilometros, mientras que otros son de minutos. Voy a escoger las variables de minutos para el análisis. Fuente- Fitabase Data Dictionary: https://www.fitabase.com/media/1930/fitabasedatadictionary102320.pdf

Para limpiar y transformar los datos, selecciono la librería de Pandas en Python.

Nota: Solo se hace el análisis en las tablas que registran los minutos de sueño y los minutos de actividad diaria. El proceso de limpieza de datos, se aplicó en igual orden en ambas tablas.
