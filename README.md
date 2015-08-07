# mapa-colaborativo
Aplicación de creación y consulta de mapas colaborativos
Cuenta con un solo archivo javascript que adapta el uso de leaflet para mapa-colaborativo de chileayuda.
Para que se pueda visualizar un mapa, sus marcadores y categorías, es necesario enviar la información serializada con formato json

# Formato json de parámetros

Los parámetros necesarios para el correcto funcionamiento de la aplicación son 3:

-Marcadores
-Categorías
-Catastrofe

## Marcadores

Los marcadores deben estar agrupados por categorías, con lo cual tendríamos una lista de listas
Si tenemos una aplicación con 3 marcadores y 5 categorías, el parámetros sería:

[
	[
		{"fields": {
			"catastrophe": 1,
			"description": "Test1",
			"category": 1,
			"longitud": -73.134,
			"latitud": -41.77},
			"pk": 1,
			"model": "maps.mark"},
		{"fields": {
			"catastrophe": 1,
			"description": "Test2",
			"category": 1,
			"longitud": -71.25120878219604,
			"latitud": -29.900089908836293},
			"pk": 14,
			"model": "maps.mark"}
	],
	[],
	[
		{"fields": {
			"catastrophe": 1,
			"description": "Test3",
			"category": 3,
			"longitud": -71.25820398330687,
			"latitud": -29.899271436420502},
			"pk": 15,
			"model": "maps.mark"}
	],
	[],
	[]
]

## Categorías

[
	{	
		"pk": 6, "model": "maps.category", 
		"fields": {"style": 1, "category": "Categoria1", "catastrophe": 2}
	}, 
	{
		"pk": 7, "model": "maps.category",
		"fields": {"style": 2, "category": "Categoria2", "catastrophe": 2}
	},
		{"pk": 8, "model": "maps.category", 
		"fields": {"style": 3, "category": "Categoria3", "catastrophe": 2}
	}
]

## Catástrofe

{
	"pk": 2, "model": "maps.catastrophes", 
	"fields": {
		"latitud": -41.77,
		"longitud": -73.134,
		"description": "Volcan explota",
		"fecha": "2014-09-11",
		"name": "Calbuco"
	}
}


