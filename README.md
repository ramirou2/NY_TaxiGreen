# <h1 align=center> **Proyecto Final Grupal de HENRY** </h1>

<p align=center><img src="https://github.com/ramirou2/NY_TaxiGreen/assets/111613206/80d5c1d4-7cdb-40a3-b521-2b5e1b4b2b77" width=400> </p>

# <h1 align=center>**`NY_TaxiGreen: Análisis del movimiento de taxis en la ciudad de Nueva York y su relación con la calidad del aire y la contaminación sonora.`**</h1>

 📔: [Reporte Técnico Completo](https://crichubiava.atlassian.net/l/cp/14Q0CXYV)

### **`Equipo`**</h2>


| <img src="https://avatars.githubusercontent.com/u/111613206?v=4" width=100> | <img src="https://media.licdn.com/dms/image/D4E03AQFDK8a0LZX7Sw/profile-displayphoto-shrink_100_100/0/1689894810692?e=1698883200&v=beta&t=JrdjWkYa1aZ4cpdwUXwafdGS1AvVGMrxBdZ6Nzdaf9w" width=100> | <img src="https://avatars.githubusercontent.com/u/79583157?v=4" width=100> | <img src="https://avatars.githubusercontent.com/u/69260155?v=4" width=100> | <img src="https://media.licdn.com/dms/image/D4E03AQH0E5IuAOAKjQ/profile-displayphoto-shrink_800_800/0/1692194604387?e=1698883200&v=beta&t=3ahkSTiqFkN0p_kJJRXjWvi7GAUMVazlrRERdPc56vw" width=100> |
|:---------------:|:---------:|:---------:|:---------:|:---------:| 
|<sub> Araque Roldan Mauricio Alejandro (https://github.com/araquester)</sub>|<sub> Biava, Cristian (https://github.com/Crichu)</sub>|<sub> López Guerra, Adriana Gabriela(https://github.com/AdrianaGLG)</sub>|<sub>Luna Paez, Gastón Ramiro (https://github.com/ramirou2)</sub>|<sub> Rappaport, Fernando Ariel (https://github.com/TheFercho)</sub>|


### **`Esquema del Repositorio`**</h3>

```Python
.
├── Complementary  (Datasets complementarios)
|       └── fuel_consumption_ratings  
|       └── yellow_taxis
    ├── air_quality_data.csv  (Dataset_CM_01)
    ├── car_noise.csv  (Dataset_CM_02)
    ├── weather.csv  (Dataset_CM_03)
├── Datasets    (Datasets bases)
|       └── Datasets_Clean  
|            ├── Alternative Fuel Vehicles US.csv
|            ├── ElectricCarData_Clean.csv
|            ├── Electric_and_Alternative_Fuel_Charging_Stations.csv
|            ├── Light Duty Vehicles.csv
|            ├── Vehicle Fuel Economy Data.csv
|            ├── taxi+_zone_lookup.csv
|            ├── taxi_zones.csv
    ├── Alternative Fuel Vehicles US.csv  (Dataset_01)
    ├── Electric and Alternative Fuel Charging Stations.csv  (Dataset_02)
    ├── ElectricCarData_Clean.csv  (Dataset_03)
    ├── ElectricCarData_Norm.csv  (Dataset_04)
    ├── Light Duty Vehicles.csv  (Dataset_05)
    ├── Vehicle Fuel Economy Data.csv  (Dataset_06)
    ├── data_dictionary_trip_records_yellow.pdf
    ├── taxi+_zone_lookup.csv (Dataset_07)
    ├── taxi_zones.dbf
├── EDA_Notebooks
    ├── EDA_Dataset_01_&_03.ipynb
    ├── EDA_Dataset_02.ipynb
    ├── EDA_Dataset_06.ipynb
    ├── EDA_Dataset_CM_01.ipynb
    ├── EDA_Dataset_CM_02_&_03_&_Tripdata_2023_05_parquet.ipynb
    ├── EDA_fuel_consumption_ratings.ipynb
├── ETL_Notebooks
|        └── Normalizacion_Columnas
|           ├── normalizacion_Datasets_bases.ipynb
|           ├── normalizacion_Datasets_complementarios.ipynb
    ├── ETL_Dataset_01_&_03_&_04_&_07.ipynb
    ├── ETL_Dataset_02.ipynb
    ├── ETL_Dataset_06.ipynb
    ├── ETL_Dataset_07.ipynb
    ├── ETL_Dataset_CM_01.ipynb
    ├── ETL_Dataset_CM_02_&_03.ipynb
    ├── ETL_fuel_consumption_ratings.ipynb
├ .gitignore
├ README.md
├ requirements.txt


```

# <h2 align=left> **Informe** </h2>

### **`Propósito del proyecto`**

​Taxi Green, una empresa de servicios de transporte de pasajeros, que actualmente se encuentra operando en el sector de micros de media y larga distancia, está interesada en invertir en el sector de transporte de pasajeros con automóviles.

Con una visión de un futuro menos contaminado y ajustarse a las tendencias de mercado actuales, quieren corroborar la relación entre estos medios de transporte particulares con:

* Calidad del aire

* Contaminación sonora

Propósito: estudiar la posibilidad de implementar vehículos eléctricos a su flota; ya sea en su totalidad o parte de la misma.

Se pretende hacer un análisis preliminar del movimiento de los taxis en la ciudad de Nueva York, para poder obtener un marco de referencia y poder tomar decisiones bien fundamentadas.​

### **`Objetivo general`**

Análisis del movimiento vehicular en NYC y su relación con la contaminación del aire y sonora.

### **`Objetivos específicos`**

Comprobar:

Relación entre el mercado automotor y las actividades de transporte en la ciudad de Nueva York con:

    *   La calidad del aire (emisiones de CO2).

    *   La contaminación sonora.

    *   Efecto de las condiciones climáticas con la cantidad de viajes solicitados. 

### **`KPIs Propuestos`**

Se proponen los siguientes KPIs con base de medición trimestral:

* Promedio de emisión de CO2 de la nueva flota menor a 3

![](<Imagenes/KPI 01.jpg>)

* Ruido promedio por diseño de la nueva flota 50 dB

![](<Imagenes/KPI 02.jpg>)
  
* Vehículos eléctricos en la flota > 60%

![](<Imagenes/KPI 03.jpg>)
  
* autonomía de la nueva flota entre > 300 km

![](<Imagenes/KPI 04.jpg>)
  
* Antigüedad de la flota < 3 años (ningún vehículo puede tener más de 3 años)

![](<Imagenes/KPI 05.jpg>)

### **`Alcance (Desarrollar)`**

> [!IMPORTANT]
> Crucial information necessary for users to succeed.
> Debe tener:
>  * Análisis descriptivo del movimiento de los taxis en NYC (patrones por semana, franja horaria). Si hay datos, incluir también: micros, uber, vehículos particulares, tipos de motor (combustible, eléctrico, híbrido).
>
> * Análisis descriptivo de la relación entre uso de medios de transporte particulares y la calidad del aire según el área (¿Qué medios se utilizan y cuál es el nivel de contaminación del aire?).
>
> * Análisis descriptivo de la relación entre uso de medios de transporte particulares y la contaminación sonora (¿Qué medios se utilizan y cuál es el nivel de contaminación sonora?).
>
> * Modelo predictivo ML: evolución de la calidad del aire en función del uso de los medios de transporte (distintos escenarios considerando distintos tipos de medios de transporte)
>
> * Modelo predictivo ML: modelar la evolución de la contaminación sonora en función del uso de los medios de transporte (distintos escenarios considerando distintos tipos de medios de transporte)
>
> * Aplica para todo: comparar datos de autos a combustión, autos eléctricos, autos híbridos (la actividad que quiere estudiar la empresa) vs micros (la actividad actual de la empresa)

> [!NOTE]\
> Podría tener:
> * Modelo para analizar tarifas variables en base al movimiento de las distintas franjas de días y horarios y condiciones climáticas.
> * Análisis del retorno de la inversión en una flota de autos eléctricos.

> [!WARNING]\
> Fuera del alcance:
> * Análisis de marketing
> * Calificación de servicios y/o condutores

### **`Matriz de responsabilidades`**

:black_circle: Main

:small_red_triangle:  Support

![Matriz de Responsabilidades](<Imagenes/Matriz de responsabilidades.jpg>)



# <h2 align=left> **Plan de trabajo** </h2>

| Hito | Nombre | Entregables | Esperado | Fecha |
|:---------------:|:---------:|:---------:|:---------:|:---------:|
| Demo Sprint #1 | Data Ingest  Process | Puesta en marcha el proyecto y Trabajando los Datos: <br> * Kickoff del proyecto  <br>* Entendimiento de las necesidades <br>* Documentar alcance , objetivo y entregables <br>* KPI’s <br>* Implementación de stack propuesto | * Más de 4 KPIs <br>* Mencionar las tecnologías a usar <br>* Documentación de alcance del proyecto <br>* EDA preliminar, calidad del dato <br>* Repo Github <br>* Planificación y estimación de esfuerzos (Diagrama de Gantt) | 09/08/2023 |
|Demo Sprint #2 | Data Analytics & ML |Data Engineering:<br> * Arquitectura propuesta y diagrama<br> * Diccionarios de datos <br> * Creación del DW <br> * Automatizar el DW <br> * Carga incremental | * DW con herramientas Big Data (HDFS, Hive, Spark y/o motores No-SQL y/o Servicios Cluod) <br> * DW automatizado con carga inicial <br> * Al menos 2 tablas de hechos y 5 dimensionales  <br> * Carga incremental de datos (video) | 23/08/2023
| Demo Sprint #3 | Data Analytics y ML |Etapa de Analytics y Machine Learning <br> * Dashboard <br> * Reportes <br> * Storytelling <br> * Modelo ML <br> * Ajustes del modelo |* Implementar modelo de ML <br> * Implementar un reporte de visualización geográfica.|06/09/2023
| |Demo Final |  * Demo general del proyecto <br> * Entregable final<br> * Documentación| * Presentación dirigida a la dirección de la compañía. <br> * Retomar lo mostrado en presentaciones anteriores. <br> * Retoques finales en base a recomendaciones de HM y PO. | 06/09/2023 |
***

### <h3 align=left>**`Propuesta de trabajo`** </h3>
***

### Recopilación y limpieza
- [x] Se utilizan los archivos .csv provistos por el cliente. También se estudian los datasets complementarios facilitados por el cliente, así como también información extra recopilada por el equipo.
- [x] Los datasets provienen tanto de archivos .csv como de APIs. Estos últimos son extraídos con técnicas de web scrapping. 
- [x] Los dataset considerados necesarios para el desarrollo del producto final del proyecto, se limpian, ordenan y normalizan.
- [x] Además, se realiza un análisis exploratorio de datos con el objetivo de detectar insights de interés para el cliente.

`Tecnología y librerías utilizadas: Python, Pandas, Numpy, os`

### Creación de un diccionario y diagrama DER
- [x] Los datasets son procesados y analizados para generar un diccionario de las variables de interés. 
- [x] Se utiliza esta información para establecer un diagrama de entidad - relación que facilite su posterior análisis

### Disponibilización de la información
- [x] Se crea un DataWarehouse utilizando las herramientas Cloud de Google.

`Tecnología y librerías utilizadas: MySQL, Google Cloud`

### Análisis de la información y Dashboard interactivo
- [x] Se diseña un dashboard con información relevante para el negocio teniendo en cuanta los KPIs definidos para tal fin.

`Tecnología y librerías utilizadas: Power BI / Streamlit /Locker studio?`

### Modelo de Machine Learning
- [x] Modelo predictivo ML: evolución de la calidad del aire en función del uso de los medios de transporte (distintos escenarios considerando distinta composición de la flota en cuanto a modelos de auto)
- [x] Modelo predictivo ML: modelar la evolución de la contaminación sonora en función del uso de los medios de transporte (distintos escenarios considerando distinta composición de la flota en cuanto a modelos de auto)

`Tecnología y librerías utilizadas: Python, Pandas, Numpy, Seaborn, Matplotlib, sklearn`

### App / Web interactiva
- [x] El modelo de machine learnig de disponibiliza a través de una página web, facilitando la interacción con el cliente.
- [x] Tecnología y librerías utilizadas: Python, FastAPI, Render

### <h3 align=left>**`Definición de identidad visual de marca`** </h3>

### Desarrollo de un logotipo

El desarrollo de un logotipo implica la creación de un símbolo visual o un diseño gráfico que representa la esencia de la marca. El logotipo puede consistir en una combinación de elementos como formas, letras, imágenes o iconos que juntos comunican la identidad y los valores de la empresa. 

Para nuestro proyecto, desarrollamos el logotipo de la empresa consultora (Taxi Green) y el de nuestro grupo de trabajo (LBD) a través de la evaluación de las alternativas que ofrecían plataformas de diseño tales como:

- Tailor Brands | Small Business Set-up Made Easy 
- Logo Maker | Used By 2.3 Million Startups  
- Diseña un Logo con Nuestro Creador de Logo Gratis | FreeLogoServices  
- Crear Logos Gratis - Creador de logos - Free Logo Design

| <img src="Imagenes/Opcion Logo 01.jpg" width=200> | <img src="Imagenes/Opcion Logo 02.jpg" width=200> | <img src="Imagenes/Opcion Logo 03.jpg" width=200> | <img src="Imagenes/Opcion Logo 04.jpg" width=200> | <img src="Imagenes/Opcion Logo 05.jpg" width=200> |

