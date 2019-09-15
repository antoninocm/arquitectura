# Arquitectura
arquitectura mejor barrio
Estrategia:
Los mejores barrios donde vivir en España. 
La información objetiva valdrá para crear un mapa de las mayores 5 ciudades de España, ordenadas por zonas en 3 colores de mejor a peor( verde,naranja,rojo) que se subirá a una web.

En el estudio se tendrá en cuenta distintas variables y pesos que generarán un algoritmo que nos dará como resultado alguno de esos colores y su concentración.

En nuestro caso la base de datos de Airbnb será una variable que se tendrá en cuenta con peso negativo zonas con concentraciones muy altas de pisos en alquiler no suelen ser las mejores para vivir tranquilo.
Con la API de google maps se obtienen las zonas y los servicios de las mismas, creamos una base de datos que se revisará mensualmente..
Creamos base de datos con los delitos por barrio con la clasificación del INE y conseguimos los datos anuales de delitos por barrio en los departamento de estadísticas locales.

Arquitectura:
Cloud→ dataset (airbnb.csv, delitos, google map...) → Google Storage.
Enviador→ sacamos una tabla con el barrio y el color resultante del algoritmo.

Operaciones:
Cargar el csv airbnb en cloud actualizar una vez al mes.
Generar SQL con la API de google maps, con zonas, servicios y subirlo una vez al mes al cloud.
Generar SQL con las estadísticas locales una vez al año se sube al cloud 
