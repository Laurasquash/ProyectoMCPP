# Proyecto Final Laura  Tovar

## Descrpción y motivacion

En la ciudad de Bogotá las entidades que se encargan de la ejecución de obras y del mantenimiento de las son el IDU (Instituto de Desarrollo Urbano) y la UMV (Unidad de Mantenimiento Vial y precisamente, estas entidades han firmado un convenio para ejecutar obras de mantenimiento en la malla vial de Bogotá en el mes de Julio de 2021. Los temas de movilidad de la ciudad son complejos, y dicho convenio pretende contribuir a la reactivación económica de la ciudad con la generación de 117 empleos y mejorar el bienestar de los ciudadanos con una mejor movilidad en 3 grandes corredores viales.

La motivación y preguntas que se quieren resolver se centran en los siguientes aspectos:

1.	En el Plan Distrital de Desarrollo se indican las estrategias para temas de movilidad. Se pretende analizar el texto para determinar si el tema de estado de malla vial y reparaciones son tomadas en cuenta. En otras palabras, que temas considera el PDD en la sección de movilidad. 

2.	Teniendo en cuenta el estado de la malla vial, quiero saber ¿Cuales son las localidades con mejores y peores condiciones viales?

3.	El convenio interadministrativo 1274 de 2021, que une a IDU y a UMV para realizar actividades de mantenimiento y rehabilitación, por lo que quisiera saber si las reparaciones (huecos) que actualmente registra el estado de la malla vial están siendo considerados por las UMV en los registros de segmentos terminados. 

4.	De los 3 grandes corredores viales dentro del convenio se encuentran La Avenida Boyacá, La Avenida Carrera 80 y La Avenida José Celestino Mutis, entonces, quiero determinar el estado de estas vías (malo, bueno o regular) y cuales son las localidades implicadas.



## Métodos utilizados

1.	Análisis de texto NLTK <br>
-	Descargué el Plan Distrital de Desarrollo (PDD), en la sección ‘Movilidad Bogotá’ consultada en http://www.sdp.gov.co/sites/default/files/bases_del_pdd_un_nuevo_contrato_social_2020_2024_documento_uno.pdf , utilicé el texto para ver las palabras más comunes sobre el tema y palabras relacionadas. 

2.	Pandas hacer EDA <br>
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

