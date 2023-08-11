# henry_project
El siguiente proyecto se basa en la creacion de un modelo de recomendación, el cual nos aproxima bastante al ambito laboral al cual nos enfrentaremos, recibiendo una base de datos la cual se encontraba sin ningun tipo de orden ni relacion, abordando de forma integral todas las etapas de limpieza de un data set, etapas que se lograron evidenciar en el proceso de corregir o eliminar datos formateados incorrectamente, duplicados o incompletos dentro de un gran conjunto de datos, es importante acotar que el modelo se realizo a traves de una tecnologia de codigo abierto con la finalidad de mejorarlo mas adelante o reusar el codigo para otro tipo de recomendación como por ejemplo para restaurantes, museos, libros o de algun otro tipo de interes, otras personas podrian usar el codigo y reproducirlo ya que la gran mayoría de empresas que existen en el mundo dependen de un insumo fundamental: los datos. Los datos son lo que le permite operar de manera eficiente y tomar las mejores decisiones, estimar comportamientos futuros y muchas cosas más siempre y cuando se cuente con las personas que saben almacenarlo en bases de datos, transformarlos y aprovecharlos de la mejor manera.

También es importante mencionar que la implementación del modelo se hace a través de una tecnología de código abierto, que permite que otras personas puedan reproducir y mejorar el modelo en el futuro. Por último, el modelo puede ser extendido a otros problemas de recomendación, como el de música o libros, ya que la metodología es muy generalizable. 😃

Este proyecto de machine learning se encuentra en la intersección de las áreas de big data, aprendizaje automático y análisis de datos. En particular, usa técnicas de preprocesado de datos, modelado, evaluación y visualización de resultados, que son temas clave en estas áreas.

A continuación una breve explicación paso a paso de lo que se hizo para llegar al producto final (Modelo de recomendación ML)

PRIMERA PARTE: ETL
En primera instancia extraemos los dataset para trabajar en ellos, hacemos transformaciones como desanidado de diccionarios y listas, unas columnas con valores nulos se reemplazaron por 0 o fueron eliminadas, eliminamos columnas innecesarias y creamos algunas columnas según lo requerido.

SEGUNDA PARTE: API
Para el desarrollo de la API: Se propone disponibilizar los datos usando el framework FastAPI.

Se hicieron las siguientes consultas:

---->idioma de la película (Idioma: str): Se ingresa un idioma, ejemplo: 'en' y te devuelve la cantidad de películas producidas en ese idioma.

---->duración de la película (Pelicula: str): Se ingresa una pelicula ejemplo: 'Toy Story'. Debe devolver la duracion y el año.

---->franquicia (Franquicia: str): Se ingresa la franquicia, retornando la cantidad de peliculas, ganancia total y promedio

---->pais( Pais: str ): Se ingresa un país por ejemplo: 'United States of America', retornando la cantidad de peliculas producidas en el mismo.

---->productoras(Productora: str ): Se ingresa la productora, entregandote el revunue total y la cantidad de peliculas que realizo.

---->director de la película (nombre_director ): Se ingresa el nombre de un director que se encuentre dentro de un dataset, por ejemplo: 'John' debiendo devolver el éxito del mismo medido a través del retorno. Además, deberá devolver el nombre de cada película con la fecha de lanzamiento, retorno individual, costo y ganancia de la misma, en formato lista.
