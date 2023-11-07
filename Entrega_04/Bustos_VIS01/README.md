#### La idea original era crear una visualización atómica que respondiese una preguntas muy simples: ¿Dónde habitan estos felinos en Chile? ¿En qué regiones? ¿Todos estos felinos estan en todas las regiones? En resumen, despejar todas las incógnitas sobre el lugar en que habitan de una manera muy visual y, al mismo tiempo, interactiva. Para ello se usó Plotly, en su mapa "Scatter Plots on Mapbox in Python" el cual se puede encontrar en el siguiente link: https://plotly.com/python/scattermapbox/

#### Como se puede observar, hay más de un script, esto debido a que inicialmente pensé en hacer el codigo sin una base de datos en csv como tal, luego pasé a hacer la base manualmente (hasta que me di cuenta que iba a estar demasiado tiempo haciendola), por lo que comencé desde 0.

##### Primero, se buscó una base de datos en csv que tuviese las coordenadas de las regiones de Chile para asignarlas a los valores investigados de los felinos, fue encontrada en este link: https://github.com/altazor-1967/Comunas-de-Chile/blob/master/Latitud%20-%20Longitud%20Chile.csv

#### Aqui manualmente se realizó una lista con las coordenadas de cada region, dando como resultado: 

## Región de Arica y Parinacota: -18.4746 -70.29792
## Región de Tarapacá: -20.2439	-70.1389
## Región de Antofagasta: -23.6508	-70.3950
## Región de Atacama: -27.0658	-70.8258
## Región de Coquimbo: -29.9708	-71.3069
## Región de Valparaíso: -33.0333	-71.6667
## Región Metropolitana: -33.4372	-70.6572
## Región de O’Higgins: -34.1619	-70.7408
## Región del Maule: -35.4228	-71.6569
## Región del Ñuble: -36.6008	-72.1089
## Región del Biobío: -36.8150	-73.0289
## Región de La Araucanía: -38.7269	-72.5989
## Región de Los Ríos: -39.8142	-73.2458
## Región de Los Lagos: -41.4539	-72.9928
## Región de Aysén: -45.4119	-72.6978
## Región de Magallanes: -53.1478	-70.9069

#### La idea de esto era crear un CSV con cada felino y las coordenadas segun lo investigado, dando como resultado aparte esto: 

## Leopardus colocola: Tarapaca, coquimbo,  bio-bio, araucania, los rios, los lagos, Aysen, magallanes
## Leopardus geoffroyi: Magallanes y Aysen
## Leopardus guigna: Coquimbo, Valparaiso, Metropolitana, O'higgins, Maule, Ñuble, Biobio, La araucania, los rios, los lagos, aysen
## Leopardus jacobita: Arica y parinacota, antofagasta y tarapaca
## Puma concolor: Todas las regiones 

#### Con estos datos, se realizó el codigo presente en "filtrar_datos.ipynb"

## Esto dio como resultado el CSV "datos_gatos_latitudes", con el cual finalmente se trabajó en el mapa deseado, en los Scripts se puede ver el proceso, el cual dio como resultado un mapa interactivo con el cual haciendo click en el gato se muestra o se deja de mostrar la zona geográfica de Chile en la cual habitan los felinos. 