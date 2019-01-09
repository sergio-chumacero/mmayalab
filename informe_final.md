# Análisis de los Sistemas de Información Sectorial para la Gestión Hídrico Ambiental y Propuestas para su Implementación y Operativización en Cuencas Estratégicas

Informe final de la consultoría realizada del 20-12-2018 al 10-12-2019. (Producto 1)

**Autor:** *Sergio Chumacero Figueroa*

## 0. Contenidos

* 1. [Antecedentes](#antecedentes)
* 2. [Objetivos](#objetivos)
* 3. [Metodología](#metodologia)
* 4. [Trabajo Previo](#trabajo_previo)
* 5. [Herramientas de Cuenca: Nodos de Cuenca y SATD](#satd)
* 6. [Sistemas de Información del MMAyA: SIARH](#siarh)
* 7. [Propuesta: Base Tecnológica hacia el Desarrollo y Operativización de las Herramientas de Cuenca con respecto los Sistemas de Información existentes](#propuesta)
    * 7.1 [Modelo de Ciclo de Vida de Datos](#ciclo_datos)
    * 7.2 [Sistemas de Intercambio Automatizado de Datos](#api)
    * 7.3 [Computo Cloud](#cloud)


## 1. Antecedentes <a name='antecedentes'></a>

En apoyo al "[Programa Plurianual de gestión integrada de Recursos Hídricos y Manejo Integral de Cuencas 2017-2020](http://www.mmaya.gob.bo/uploads/PNC-Programacio%CC%81nPlurianual2017-2020.pdf)", el "Programa de Gestión Integral con Enfoque de Cuenca" (PROCUENCA) tiene como objetivo general, crear condiciones en cuencas estratégicas para la implementación de planes directores de cuencas para la gestión integrada de recursos hídricos conforme a las directrices del "Plan Nacional de Cuencas".

El programa PROCUENCA se implementa simultáneamiente en dos niveles:

1. A nivel nacional, en apoyo a la construcción de politicas y mecanismos de acción sectorial en torno a la gestión y manejo de cuencas.

2. A nivel de cuencas estratégicas seleccionadas como piloto, tanto para la aplicación y validación de las estrategias e instrumentos sectoriales, como para la generación de nuevas experiencias, aprendizajes y conocimientos que contribuyan al marco estratégico, orientador y operativo del plan nacional de cuencas.

Uno de los objetivos del programa PROCUENCA es el establecimiento de procesos de gestión de información hídrico-ambiental en las dos cuencas que interviene: Las cuencas **Azero** y **Guadalquivir**.

<center>Cuenca Azero (Chuquisaca)</center>

<img src="./img/azero_small.png" alt="IMAGE ALT TEXT HERE" width="240" height="400" border="10" />

<center>Cuenca Guadalquivir (Tarija)</center>

<img src="./img/guadalquivir_small.png" alt="IMAGE ALT TEXT HERE" width="240" height="400" border="10" />

En el campo de recolección y manejo de datos hídrico-ambientales a nivel nacional, el Ministerio de Medio Ambiente y Agua (**MMAyA**) cuenta con multiples sistemas de información existentes.

Frente a esta situación, el MMAyA a través de su Dirección General de Planificación y Área de Sistemas, está desarrollando el sistema **SIARH** (Sistema de Informacíon Ambiental y de Recursos Hídricos) con el fin de centralizar los distintos sistemas.

Los puntos de acceso al sistema por parte de los distintos actores o **Nodos de Cuenca** deberán ser implementados de manera conjunta al SIARH.

Al mismo tiempo, el MMAyA realizó avances en el marco teórico del Sistema de Apoyo a la Toma de Decisiones (**SATD**) como herramienta para la gestión de Planes Directores de Cuencas, que se encuentra en proceso de conceptualización para ser implementado en la cuenca Katari.

En este contexto, se ha identificado la necesidad de contar con un servicio para la
caracterización de los aspectos conceptuales y operativos de los sistemas del MMAyA para la emisión de criterios y recomendaciones que contribuyan a establecer las líneas de apoyo del Programa PROCUNCA al desarrollo y operativización de estos sistemas en las cuencas estratégicas en las que trabaja (Azero y Guadalquivir).

## 2. Objetivos <a name='objetivos'></a>

Con el fin de aclarar el panorama actual en el campo de manejo de datos del sector y proponer herramientas de apoyo a los objetivos del PROCUENCA relacionados a la gestión de información, se establecieron los siguientes objetivos:

* Descripción y análisis del sistema de información del MMAyA en relación al SATD y Nodos de Cuenca con miras a su implementación y operativización en las cuencas Azero y Guadalquivir.
* Recomendaciones, apreciaciones, análisis y propuestas con respecto a los siguientes temas:
    * Integración de sistemas del MMAyA relacionados a cuencas y recursos hídricos a nivel de manejo y gestión de datos.
    * Desarrollo de los sistemas de información a nivel de cuencas estratégicas en relación al SATD y su integración con el sistema de información del MMAyA.
    * Tecnologías relacionadas a los temas previos:
        * Sistemas de intercambio automatizado de datos.
        * Entornos de computo Cloud.
* Elaboración de una base de datos para las cuencas Azero y Guadalquivir, con información disponible y relevante para la gestión hídrico-ambiental.

## 3. Metodología <a name='metodologia'></a>

Para la elaboración de esta consultoría se partió de una serie de reuniones con personal de la Dirección General de Planificación y el Área de Sistemas del MMAyA, así como con personal de PROCUENCA para establecer la situación general de los sistemas de información actuales relacionados a la gestión hídrico-ambiental en cuencas estratégicas y obtener acceso a los sistemas y datos disponibles.

Específicamente, conté con acceso a:
* Los sistemas de acceso público del MMAyA.
* La versión en desarrollo del Sistema de Información Ambiental y de Recursos Hídricos (SIARH).
* Datos de oferta Hídrica Superficial proporcionados de manera directa.
* Datos de la cuenca Guadalquivir proporcionados de manera directa.

Junto con la información derivada de estas reuniones, hice uso también del trabajo previo realizado en dos consultorías previas:

* [1] <a name='bisit'></a> Análisis del Estado del Software y Hardware de Sistemas de Información del Sector de Medio Ambiente y Agua, para la Consolidación de un Sistema Integrado de Información. (21.09.2017 - BISIT S.R.L.)
* [2] <a name='southern'></a> Implementación de la Página Web y Análisis e Ingeniería a Diseño Final del Sistema de Información Geográfico SISGE-KATARI de la Cuenca Katari y Lago Menor del Titicaca. (Southern STH S.R.L)
    * Producto Final - Diseño del Sistema SIG Web y especificaciones Técnicas
    
Con respecto al objetivo 2, en base al trabajo previo, los datos recopilados y la información derivada de las reuniones, elaboré las propuestas de tecnologías específicas detalladas en este documento que considero de gran relevancia como base para la implementación del SATD y Nodos de Cuenca en las cuencas Azero y Guadalquivir.

Estas tecnologías y su uso en el sector se adaptan a un modelo general de ciclo de vida de datos, que también detallamos en este documento.

Finalmente, implementé uno de los componentes del ciclo de vida descritos (la fase de consumo) haciendo uso de varias de las tecnologías propuestas. Esta implementación responde al objetivo 3, almacenando la información recopilada de las cuencas estratégicas y proveyendo un entorno de trabajo completo, capaz de responder a las necesidades básicas del SATD.

## 4. Trabajo Previo <a name="trabajo_previo"></a>

En el campo de recolección y manejo de datos hídrico-ambientales a nivel nacional, el MMAyA cuenta con multiples sistemas de información existentes.

Un relevamiento exhaustivo de estos sistemas fue realizado en [[1]](#bisit). Como producto de esta consultoría se presentó también un análisis comparativo respecto a un sistema ideal para el MMAyA (definido en la misma consultoría), producto del cual los consultores derivan las siguientes recomendaciones:
* La aplicación de **ciencia de datos** como paradigma para la recopilacion y procesamiento de la información.
* La constitución del "Centro de Gestión del Conocimiento en Agua Saneamiento y Medio Ambiente", que se basa en la centralización de la infraestructura tecnológica del MMAyA.


Actualmente el MMAyA a través de su Dirección General de Planificación y Área de Sistemas, está desarrollando el sistema **SIARH** (Sistema de Informacíon Ambiental y de Recursos Hídricos). El SIARH tiene como objetivo la centralización de los distintos sistemas existentes del MMAyA bajo una sola plataforma de desarrollo alimentado por un sistema central de base de datos que opere en un servidor físico en sus instalaciones de obrajes. 

## 5. Herramientas de Cuenca: Nodos de Cuenca y SATD <a name="satd"></a>

<div align="center"><img src="./img/nodos_cuenca.png"/></div>
<div align="center"><img src="./img/satd.png"/></div>

## 6. Sistemas de Información del MMAyA: SIARH <a name="siarh"></a>

A continuación enlistamos los sistemas de información del MMAyA, su estado actual, su función principal, el tipo de datos que manejan y la relevancia de estos datos con respecto al SATD y Nodos de Cuenca. Para mayor información técnica y de infraestructura de estos sistemas, referirse a [[1]](#bisit). 

**Sistemas altamente relevantes para el SATD**

Los siguientes sistemas contienen información altamente relevante para la implementación del SATD. La relevancia de los datos con respecto al SATD fue acordada de manera conjunta con técnicos del MMAyA.

Cabe remarcar que encima de la base de datos de estos subsistemas, usualmente se encuentra en producción un sistema de gestión de estos datos haciendo uso de aplicaciones web.

* **[SIRH](http://sys.sirh.gob.bo)** (Sistema de Información de Recursos Hídricos) - Proporcionar información de recursos hídricos a nivel nacional. Los datos 

* **[GEOSIRH](http://geo.sirh.gob.bo)**  (Sistema de Información de Recursos Hídricos Geográficos) - Gestión de información georeferenciada de recursos hídricos a nivel nacional. Datos: Áreas de planes directores de cuencas, Áreas de cuencas transfronterizas, datos de unidades de cuenca, datos de unidades de calidad de agua, datos de unidades de riesgos hidrológicos, proyectos de riego. 

* **[VIBH](http://vibh.mmaya.gob.bo)** (GeoVisor de Manejo de Información de Balances Hídricos) - Aplicación web con el fin de gestionar la información de balance hídrico a nivel nacional. Datos georeferenciados: Matrices de escurrimiento, evapotranspiración, flujo base, precipitación, streamflow.

* **[SIASBO](http://http://dev.sirh.gob.bo/index.php?module=siasbo&smodule=geovisor)** (Sistema de Información de Agua Subterránea en Bolivia) - Datos georeferenciados de pozos y manantiales.


**Sistemas eventualmente relevantes para el SATD**

* **[SIAB](https://siab.sirh.gob.bo/)** (Sistema de Información de Agua Potable y Saneaminento en Bolivia) - Aplicación web con el fin de gestionar información de agua potable y saneamiento en áreas rurales. Datos: Reportes de proyectos.
* **[SNIA](http://snia.mmaya.gob.bo)** (Sistema Nacional de Información Ambiental) - Aplicación web con el fin de administrar los procesos de prevención y control de la calidad ambiental. Datos: Inspecciones UGA y UFCA, datos de educación ambiental, datos de toneladas de exportación para disposición final, datos de SAO importado vs. cupo anual, registro de archivos vinculados a documentos ambientales.


**Sistemas relevantes para Nodos de Cuenca** 

* **[SISMO](http://sismo.cuencasbolivia.org)** (Sistema de Planificación, Seguimiento y Monitoreo) - Aplicación web con el fin de realizar seguimiento y monitoreo a los planes directores de cuenca. Datos: Matrices de Indicadores y POA.
* **[SISPM](http://priorizacion.cuencasbolivia.org)** (Sistema de Priorización de Microcuencas) - Aplicación web con el fin de realizar la priorización de microcencas en el marco de planes directores de cuencas. Datos: PDMs, POAs y estudios de investigación.

**Sistemas activos pero no-relevantes**

Los siguientes sistemas se encuentran actualmente activos, pero no manejan datos relevantes al SATD o Nodos de Cuenca.

* **[CODICE](http://codice.mmaya.gob.bo)** - Manejo de correspondencia.
* **[SIAL](http://sial.mmaya.gob.bo)** (Sistema de Almacenes) - Gestión de ítems dentro de almacenes.
* **Contabilidad Visual** - Aplicación de escritorio con el fin de gestionar la información contable de acuerdo a parámetros del POA.
* **[Sistema de RRHH](http://personal.mmaya.gob.bo)** (Sistema de Recursos Humanos) - Aplicación web con el fin de gestionar los recursos humanos del MMAyA.


**Sistemas inactivos**

Los siguientes subsistemas se encuentran actualmente inactivos, lo que significa que sus funciones fueron transferidas a otro sistema, que todavía se encuentra en desarrollo o que sus funciones ya no son utilizadas.

* **[SIAM](http://siam.mmaya.gob.bo)** (Sistema de Información de Agua y Medio Ambiente) - Sistema general de información subsectorial. Maneja matrices de proyectos, ejecución presupuestaria, inicio y entrega de obras.
* **[SIG-SNIA](http://http://190.129.84.22/sig_snia/)** (Geovisor del sistema SNIA)
* **[SISGP](http://sisgp.mmaya.gob.bo)** (Sistema de Información de Gestión de Proyectos en Pre-Inversión)
* **ContaPOA** (Sistema de Monitoreo de Ejecución Presupuestaria y POA) - Aplicación de escritorio con el fin de gestionar la información contable de acuerdo a parámetros del POA.
* **SPYS** (Sistema de Programación y Seguimiento) - Aplicación de escritorio con el fin de gestionar la información contable de la oficina central del MMAyA.


## 7. Propuesta: Base Tecnológica hacia el Desarrollo y Operativización de las Herramientas de Cuenca con respecto los Sistemas de Información existentes <a name="propuesta"></a>
    
    
### 7.1 Modelo de Ciclo de Vida de Datos <a name="ciclo_datos"></a>
### 7.2 Sistemas de Intercambio Automatizado de Datos <a name="api"></a>
### 7.3 Computo Cloud <a name="cloud"></a>



