# henry_project
El siguiente proyecto se basa en la creacion de un modelo de recomendación, el cual nos aproxima bastante al ambito laboral al cual nos enfrentaremos, recibiendo una base de datos la cual se encontraba sin ningun tipo de orden ni relacion, abordando de forma integral todas las etapas de limpieza de un data set, etapas que se lograron evidenciar en el proceso de corregir o eliminar datos formateados incorrectamente, duplicados o incompletos dentro de un gran conjunto de datos, es importante acotar que el modelo se realizo a traves de una tecnologia de codigo abierto con la finalidad de mejorarlo mas adelante o reusar el codigo para otro tipo de recomendación como por ejemplo para restaurantes, museos, libros o de algun otro tipo de interes, otras personas podrian usar el codigo y reproducirlo ya que la gran mayoría de empresas que existen en el mundo dependen de un insumo fundamental: los datos. Los datos son lo que le permite operar de manera eficiente y tomar las mejores decisiones, estimar comportamientos futuros y muchas cosas más siempre y cuando se cuente con las personas que saben almacenarlo en bases de datos, transformarlos y aprovecharlos de la mejor manera.

En este proyecto de modelo de recomendacion abordamos las magnitudes fundamentales en el procesamiento de datos que son las  características que definen uno de los principales retos de este proyecto que consistió en el hecho de analizar, identificar y corregir datos en bruto que estaban desordenados, equivocados y mal procesados, usando metodos y tecnicas aprendidas a lo largo de los modulos anteriores.

Daremos un recorrido por cada etapa de la creacion del modelo de recomendación.

PRIMERA PARTE: ETL
Se inicio desde 0, haciendo trabajos de Data Engineer para lograr obtener un MVP (como era lo recomendado) en esta etapa se extrajeron datos que se encontraban anidados en estructuras como diccionarios y listas de diccionarios, lo que conceptualmente no permitia hacer lo que se tenia previsto, por esto se aplicaron extracciones de los datos de las estructuras mencionadas arriba, ademas de eso se tuvieron que reemplazar valores que se encontraban nulos, vacios con ceros o en algunos casos se eliminaron algunas de las filas las cuales previamente fueron estudiadas para evitar perdida de informacion valiosa, al mismo tiempo que se desanidaron los datos se eliminaron columnas que resultaron con informacion duplicada esto con la finalidad de optimizar al maximo los recursos con los que se trabajaron ya que finalmente debian tener el tamaño correcto para su manipulacion posterior. 

SEGUNDA PARTE: API
bajo el uso del framework FastAPI se propone colocar a disposicion los datos de la empresa de Streaming

Se crearon seis funciones las cuales se explican a continuacion 
*def peliculas_idioma( Idioma: str ):* Se ingresa un idioma (como están escritos en el dataset, no hay que traducirlos!). Debe devolver la cantidad de películas producidas en ese idioma.

*def peliculas_duracion( Pelicula: str ):* Se ingresa una pelicula. Debe devolver la duracion y el año.

*def franquicia( Franquicia: str ):* Se ingresa la franquicia, retornando la cantidad de peliculas, ganancia total y promedio

*def peliculas_pais( Pais: str ):* Se ingresa un país (como están escritos en el dataset, no hay que traducirlos!), retornando la cantidad de peliculas producidas en el mismo.

*def productoras_exitosas( Productora: str ):* Se ingresa la productora, entregandote el revunue total y la cantidad de peliculas que realizo.

*def get_director( nombre_director ):* Se ingresa el nombre de un director que se encuentre dentro de un dataset debiendo devolver el éxito del mismo medido a través del retorno. Además, deberá devolver el nombre de cada película con la fecha de lanzamiento, retorno individual, costo y ganancia de la misma, en formato lista.

