## Curso de programación para iOS con Swift

# Bienvenido al curso

	- Bienvenido al curso de programación para iOS con Swift 3.0

	- Swift 3.0 y sus diferencias con la versión anterior

		array.reverse() // Voltea dicho arraglo en presente
		array.reversed() // Voltea dicho arreglo pero genera uno nuevo con dichos valores

# Swift, el lenguaje de programación de Apple

	- Datos básicos y tuplas

		Para concatenar se usa +
		Tambien para concatenar se usa el metodo .appending()
		Tambien se utiliza +=

		Tener en cuenta que las variables son objetos, por ende tienen metodos
		Eje: VarCadena.characters.count

		Tipo de datos
		var nomVariable : String = ""
		var numero : int

		Para hacer un casting o cast:
		Int(variable)
		Double(variable)

		***** Tuplas ******

		Son arreglos por decirlo asi, de diferentes valores

		Definicion de tuplas por indice:
		let errores = (404, "Not found")

		//Acceder a una posicion
		errores.0 || errores.1

		//Asignar variables o constantes a las posiciones de las tuplas
		let (code,message) = errores

		// Definir los nombres de las posiciones en la misma tupla
		let frutas = (cantidad: 20, fruta: "manzanas")

		La diferencia de los dos tipos de asignacion de nombre es que si creas la tupla con los
		nombres de sus posiciones, debes de acceder al valor con la nomenglatura clave.valor
		en cambio se le asignas variables despues de crearlas las variables contienen dicho valor. 

	- Colecciones o Array

		Los arreglos son solecciones de valores, en swift los arreglos solo pueden contener un solo
		tipo de valor.

		* Cabe destacar que este es una clase y por conciguiente cuenta con metodos

		Como declaramos un array

		var frutas = [String] (); // Forma corta, si se deine de esta menera no se pueden asignar
									 valores a la primera.

		var frutas:Array<String> = ["Mango", "Pera"];

		* Para interactuar o gestionar el array chequiar sus metodos

		// Como recorrer un array
		for valor in array{
			// valor
		}

	- Sets
		Estos son solecciones de valores irrepetibles, a estos se le asignan arreglos

		var VARIABLE:Set<TipoValor> = [array de valores];

		Nota: Como en swift todo es orientado a objetos esta VARIABLE tipo set tiene sus 
		respectivos metodos

		* VARIABLE.insert("valor") // Retorna una tupla con el estado de la insercion y la insecion
		// (true,insecion) Por lo que se le puede asignar variables para tener sus valores
		como cualquier cosa que retorne valores

		let (estado,valor) = VARIABLE.insert("valor")

		NOTA: Los set te brindan metodos especiales para gestionar dichos SET o ARRAYS
		como unir, ver diferencias, ver valores que no se repiten, etc.
		Es recomendable usarlos.

		**** METODOS A TENER EN CUENTA ****

		- insersection(SET o Array) -> devuelve un set con los elementos comunes entre los sets

		- symmetricDifference(SET o Array) -> devuelve un set con los elementos que no se repiten

		- containts('valor') -> determina si el valor existe en el set

		- union(SET o array) -> Une el set o array al set instanciado

		- subtract(SET o array) -> sinonimo de sustrer, quita los elemntos de uno en el otro.

		- isSuperset(of: SET o Array) -> determina si el parametro esta en el set
		retorna un boleano

		- isSubset(of: SET o Array) -> determina si el valor pasado no esta en en el set
		retorna un boleano 


	- Diccionarios

		Los diccionarios son array asociativos

		Ejemplo de crecion:

		var rangos = [String:String]()
		rangos["capitan"] = "Pedro"

		forma recomendeda:

		var rangos = ["capitan":"Ever", "mayor":"cuevas"]

		* como es un objeto, este trae todo sus metodos para poder gestionarlos

	- Sentencias de control

		Recordar los for nuevos:

		for i in 1...5{
			recorre 5 veces
		}

		agregar el menor que al for in

		for i in 1..<5{
			llega hasta el 4
		}

		_ : el guion bajo en los for se usa para recorrer pero sin asignar valores
		esto se usa para que en caso donde se desee recorrer ciertos elementos mucho
		mas rapidos.

		for _ in 1...10{

		}

		while condicion{

		}

		// recuerda el do while se sustituyo por el repeat

		repeat{

		}while condicion

		switch condicion{
			cases:
			default

		}

		NOTA: en los swift no hace faltan los breack dentro de los "case" ya que una vez 
		encuentre coincidencias sale de este.

	- Optionals

# Creación de vistas de la aplicación y Controllers

	- Arquitectura de una aplicación en iOS

	- Storyboards

	- UITableView de forma simple

	- Vista de Login

	- UITabBarController

	- UINavigationController

	- Multiple View Controller

	- ScrollViews

	- UITableView

	- UICollectionView

# Acceso a Hardware

	- Acceso a la cámara y UIImagePicker

	- MapKit

	- CoreLocation

# Animaciones y vistas avanzadas

	- UIView

	- Core Animation

	- Diseño para varios dispositivos con AutoLayout

	- Autolayout desde código

# Conexión a servicios de terceros

	- Añadir dependencias de terceros

	- Consumo de un Web Service con Urlsession

	- Convirtiendo nuestros datos en Objetos

	- Consumo de un Web Service: Alamofire

	- Login social con Facebook

	- Pasar datos entre vistas

