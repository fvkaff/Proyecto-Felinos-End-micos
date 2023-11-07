#### La base de datos tiene componentes tanto cualitativos como cuantitativos, por un lado tiene la categorización de los gatos segun la region en la que habitan: Magallanes, Metropolitana, De Los lagos, etc; así con todas las regiones del país. Los links de donde se extrajo la información están al final de la ficha técnica. 

#### Al mismo tiempo, se buscaba que cada region tuviese sus coordenadas aproximadas para luego establecer eso como los puntos en los que los felinos, al relacionarse con ciertas regiones, se pusieran en el mapa. Inicialmente intenté hacerlo manualmente como se explicó en el README, pero eran demasiados datos puesto que plotly pedía los datos en el siguiente formato:

"data = {
    'lat': [-20.0, -33.5, -34.6, -43.0, -18.5, -30.0],
    'lon': [-69.0, -70.6, -71.3, -72.5, -70.0, -70.0],
    'region': ['Tarapacá', 'Valparaíso', 'La Serena', 'Magallanes', 'Arica y Parinacota', 'Todas las Regiones'],
    'category': ['Leopardus colocola', 'Leopardus colocola', 'Leopardus jacobita', 'Leopardus geoffroyi', 'Leopardus geoffroyi', 'Puma concolor'],
}"

#### Esa organización necesitaba que, si queria poner más de un gato por coordenada, tenia que repetir el nombre del gato en todas las regiones con cada gato, por lo que opté por crear la base de datos puesta en el csv mediante el proceso explicado en el README. Con esos datos se pudo crear con éxito la visualización atómica buscada: cada gato y sus respectivas regiones en las que habitan. 

# Se deja ademas la base de datos aportada por usuarios de Github para la latitud y longitud de las regiones del país. 

## Links de interés e información sobre las regiones y coordenadas

- https://www.nature.org/es-us/
- https://www.chile.travel/sin-categorizar/felinos-nativos-de-chile-estos-son-nuestros-propios-gatos-grandes-2/#:~:text=Gato%20Mont%C3%A9s%20Andino,superior%20a%20los%204%20kilos
- https://github.com/altazor-1967/Comunas-de-Chile/blob/master/Latitud%20-%20Longitud%20Chile.csv 
- https://laderasur.com/articulo/felinos-de-chile-una-guia-de-las-5-especies-que-habitan-el-pais/
- http://especies.mma.gob.cl/CNMWeb/Web/WebCiudadana/especies_endemicas.aspx