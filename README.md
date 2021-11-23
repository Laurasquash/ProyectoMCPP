# PROYECTO FINAL LAURA TOVAR

## Descripción y motivación

En la ciudad de Bogotá las entidades que se encargan de la ejecución de obras y del mantenimiento de las son el IDU (Instituto de Desarrollo Urbano) y la UMV (Unidad de Mantenimiento Vial y precisamente, estas entidades han firmado un convenio para ejecutar obras de mantenimiento en la malla vial de Bogotá en el mes de Julio de 2021. Los temas de movilidad de la ciudad son complejos, y dicho convenio pretende contribuir a la reactivación económica de la ciudad con la generación de 117 empleos y mejorar el bienestar de los ciudadanos con una mejor movilidad en 3 grandes corredores viales. <br>

La motivación y preguntas que se quieren resolver se centran en los siguientes aspectos:

1.	En el Plan Distrital de Desarrollo se indican las estrategias para temas de movilidad. Se pretende analizar el texto para determinar si el tema de estado de malla vial y reparaciones son tomadas en cuenta. En otras palabras, que temas considera el PDD en la sección de movilidad. 

2.	Teniendo en cuenta el estado de la malla vial, quiero saber ¿Cuales son las localidades con mejores y peores condiciones viales?

3.	El convenio interadministrativo 1274 de 2021, que une a IDU y a UMV para realizar actividades de mantenimiento y rehabilitación, por lo que quisiera saber si las reparaciones (huecos) que actualmente registra el estado de la malla vial están siendo considerados por las UMV en los registros de segmentos terminados. 

4.	De los 3 grandes corredores viales dentro del convenio se encuentran La Avenida Boyacá, La Avenida Carrera 80 y La Avenida José Celestino Mutis, entonces, quiero determinar el estado de estas vías (malo, bueno o regular) y cuales son las localidades implicadas.



## Métodos utilizados

1.	Análisis de texto NLTK <br>
-	Descargué el Plan Distrital de Desarrollo (PDD), en la sección ‘Movilidad Bogotá’ consultada en http://www.sdp.gov.co/sites/default/files/bases_del_pdd_un_nuevo_contrato_social_2020_2024_documento_uno.pdf , utilicé el texto para ver las palabras más comunes sobre el tema y palabras relacionadas. 

2.	Pandas <br>
-	Utilizar pandas para hacer un EDA, limpiar bases, hacer filtros de variables que considero importantes. a las siguientes bases de datos del Portal de Datos abiertos Bogotá y Datos abiertos Secretaría de Movilidad.

-	Malla Vial Bogotá: características de vías en la ciudad de Bogotá. Tomado de https://datos.movilidadbogota.gov.co/datasets/movilidadbogota::malla-vial-integral-bogota-d-c/about 

-	Segmentos intervenidos por la UMV: Fuente UMV (Unidad de Mantenimiento Vial) con los reportes diarios desde 04/01/2021 hasta el 30/09/2021. Tomado de https://datosabiertos.bogota.gov.co/organization/umv 

3.	Tableau <br>
-	Utilicé las herramientas de tablas dinámicas para mejor visualización de ambas bases de datos, utilizando los filtros de Tableau pude hacer el merge de las bases ya que me interesaba conocer el estado de las vías de los segmentos intervenidos por la UMV en lo que llevamos del 2021.

-	Elaboración de tablas y gráficas con filtros de variables de interés. 

4.	Qgis <br>
-	Elaboración de mapas con los datos geoespaciales utilizando la herramienta de Open Street Maps.

-	Básicamente, teniendo en cuenta el número de huecos intervenidos por localidad,  identificar el estado vial por localidades

-	Existen 3 Corredores principales de interés, La Avenida Boyacá, la Avenida Agoberto Mejía y la Avenida Jose Ceslestino Mutis, los las cuales se resaltan en un mapa y se verifican los segmentos intervenidos.



## Hallazgos

1. Las palabras en el Plan Distrital de Desarrollo 2020-2024 más comunes no se refieren específicamente al manteminiento vial o mejoramiento de los segmentos viales en Bogotá. Se refieren entonces a las obras del metros, ciclorutas y biciusuarios y los tiempos de desplazamiento

![NTLK](https://user-images.githubusercontent.com/92479409/142977769-a4f49e5f-dbf9-4981-b368-24a6fb4c913b.png)



2. Las localidades con mas huecos tapados fueron:
-	Usaquen-> 31.701
-	Suba-> 27.210
-	Kennedy->22.807
-	Fontibon-> 16.556
-	Barrios Unidos->15.847
-	Chapinero->14.426

![N huecos por localidad (1)](https://user-images.githubusercontent.com/92479409/142977860-2f0f3655-e976-4401-9ace-99f39be6def3.png)


3. Se describe el tipo de reparación que se le aplicó al segmento vial por localidad <br>
-	La actividad que mas se realiza es el parcheo
-	Para ambos procedimiento se requieren 10 trabajadores
-	Antonio Nariño, Bosa, Chapinero, Engativá, Fontibón, Kennedy, Puente Aranda, Teusaquillo, Usaquén.
-	Usaquén, Suba, Teusaquillo, Kennedy, Engativá son las localidades donde se realizaron procesos de rehabilitación.
-	Teusaquillo, Candelaria, Chapinero, Usaquén, Suba son las localidades que han tenido mas tipos de intervención entonces, se puede presumir que el estado de la malla vial en esas localidades es malo. <br>

![Tipo Actividad por localidad](https://user-images.githubusercontent.com/92479409/142977883-f220066b-071c-4c4e-8058-71f24cb95aa7.png)




4. Filtros de calles, avenidas y carreras por localidad y su estado vial. Las localidades que deberían ser el foco para reparación de segmentos viales podrían ser: Engativa, Kennedy, Rafael Uribe Uribe, Suba, Tesusaquillo.

![Estado vial por localidad tabla](https://user-images.githubusercontent.com/92479409/142977909-f65789ff-99a4-4e15-9eb2-f18457951d07.png)


5. Mapa 1:
- El 24.728929518023904% de las vías en Bogotá están en buen estado
- El 21.60021028497996% de las vías en Bogotá están en buen estado
- El 40.34770037310981% de las vías en Bogotá están en buen estado

![mapa localidades 1](https://user-images.githubusercontent.com/92479409/142977933-48d865c5-728e-43c5-81a7-489fc28a8a76.png)



6. Mapa 2: De acuerdo al numero de huecos reparados y al tipo de actividad que se realiza en cada localidad vemos que las
localidades donde se realizaron mas intervenciones de mantenimiento presentan mejoría en el estado vial

![mapa Estado vial localidades 2](https://user-images.githubusercontent.com/92479409/142977941-8c0f3876-8962-4257-b861-b550746fedf9.png)


7. Mapa 3: Recordando el convenio de UMV y el IDU los tres corredores principales. La reflexión es:
- ¿El convenio si es necesario?
- ¿Que pasa con las otras vías principales?

![mapa corredores ppales 3](https://user-images.githubusercontent.com/92479409/142977961-8f88d98b-71db-46a3-9d83-d9c326cbda84.png)



