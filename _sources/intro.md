# **Predicción de PM10 mediante un enfoque de ensamblaje apilado basado en aprendizaje profundo y XGBoost** 

Un pronóstico preciso de PM10 es fundamental para implementar controles que mitiguen los efectos nocivos de este contaminante sobre la calidad del aire, el ecosistema y cada uno de sus integrantes, en especial la salud de los seres humanos. La exposición a la materia particulada, especialmente a partículas de menos de 10 micrómetros de diámetro, está directamente relacionada con una serie de problemas de salud, que incluyen enfermedades respiratorias, cardiovasculares y muertes prematuras. Según la Organización Mundial de la Salud (OMS), la contaminación del aire es uno de los mayores riesgos ambientales para la salud, causando aproximadamente 4,2 millones de muertes prematuras al año a nivel mundial [who2021](https://www.who.int/es/news-room/fact-sheets/detail/ambient-%28outdoor%29-air-quality-and-health). 

En esta investigación, trabajaremos con el conjunto de datos *"data_2017_2022.csv"*, el cual está compuesto por 4.084.061 registros obtenidos de un sistema de sensores distribuidos en 9 estaciones de medición de variables meteorológicas  ubicadas en el Valle del Cauca. Estas estaciones no solo miden nuestra variable objetivo, el PM10, sino también otros atríbutos y/o características asociadas al indice de la calidad del aire. La recolección de datos se realizó desde el 1 de enero de 2017 hasta el 31 de diciembre de 2022, abarcando un período total de 5 años. Dada la cantidad de datos faltantes y luego de un análisis exaustivo de los datos, se tomo la desición de trabajar con los datos de la estación `Compartir`. A continuación se describen cada uno de los atributos y target del conjunto de datos. 

* PM10: Concentración de material particulado con diámetro aerodinámico menor o igual a 10 micrómetros $(\mu g/m^3)$ (Target).

* fecha: Corresponde a la fecha y hora de la medición en formato ISO 8601 (AAAA-MM-DDTHH:MM:SSZ).

* estacion: Identifica la estación de monitoreo donde se realizó la medición.

* BC: Concentración de carbono negro o hollín en el aire $(\mu g/m^3)$.

* WD: Dirección del viento en grados $(°)$.

* H2S: Concentración de sulfuro de hidrógeno $(\mu g/m^3)$.

* HR: Humedad relativa del aire en porcentaje $(%)$

* RF: Cantidad de precipitación en milímetros $(mm)$.

* NO2: Concentración de dióxido de nitrógeno $(\mu g/m^3)$.

* O3: Concentración de ozono $(\mu g/m^3)$.

* PM2.5: Concentración de material particulado con diámetro aerodinámico menor o igual a 2.5 micrómetros $(\mu g/m^3)$.

* P: Presión atmosférica en hectopascales $(\text{hPa})$.

* RS: Radiación solar en vatios por metro cuadrado $(W/m^2)$.

* SO2: Concentración de dióxido de azufre $(\mu g/m^3)$..

* AT: Temperatura del aire en grados Celsius $(°C)$.

* AT_10_m: Temperatura del aire a 10 metros de altura en grados Celsius  $(°C)$.

* UV: Índice UV.

* WS: Velocidad del viento en metros por segundo cuadrado $m/s^2$.