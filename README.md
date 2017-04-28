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

		Los optional como ya sabemos deben ser tratados con mucho cuidado 

		como declarar un optional

		var variable:Int? // este por defecto viene con nil

		para sacar el valor de la caja usamos el !

		variable! // Saca el valor de la caja

		if para detectar si el el optional esta bueno

		if let v1 = optional1, let v2 = optional2, v1<v2{
			ok
		}else{
			no cumple
		}

		tambien podemos usar el if con != nil

		if variable != nil{
			print(variable!) en este caso debemos sacar el valor de la caja.
		}


# Creación de vistas de la aplicación y Controllers

	- Arquitectura de una aplicación en iOS

		info.plist -> en este archivo se puede configurar practicamente
		todos los aspectos de la app, hasta se puede definir que vista sale primero
		cuando se ejecuta la aplicacion.

		En IOS el MVC no funciona tal como esta definido, si que es un Modelo ||| Vista-Controlador
		ya que estos dos ultimos estan juntos.

	- Storyboards

		Comand + R = Compilar

		Cuando se esta creando las varibles que apuntan a los elementos del storyboard
		se ve una opcion que dice "Storage" que el valor que acepta es weak y strong

		weak: Borra la memoria de la varibale una vez se utiliza
		strong: Variable es como si fuera global

		@IBAction: A este se le puede asignar mas de un boton o accion y diferenciarlos
		mediante el metodo isEqual que trae el objeto sender, tambien dicho objeto trae mas
		metodos

		* Para asociar mas de boton se desliza la + del @IBAction hacia el elemento en 
		el storyboard

	- UITableView de forma simple

		Los Table view controller: Se usan para manejar tablas estaticas,

		Nota: Cuando se le agrega un action a un campo de texto si se le asigna la accion
		el primero esta bien. Pero si se desea agregar esa accion a otros campos de texto 
		arrastrando el mas se debe formatear la accion ya que se le coloca la de por defecto

		Corregir error de que no se ve la tabla: esto sucede si viene con codigo pre fabricado y no 
		se le esta asignando el delagate, borrar ester codigo si no se va usar

		* Style: Grouped es el mejor estilo para las tablas estaticas

	- Programatic Views

	- Vista de Login

		**** Como crear una alerta y presentarla ****

		let alerta = UIAlertController(title: "Atencion", message: "Desea seguir con la accion", preferredStyle: .alert)
        
        // Creamos las acciones que tendra la alerta
        
        let cancelar = UIAlertAction(title: "No!", style: .cancel, handler: {
            //Clousures
            accion in
            print("El usuario cancelo")
        })
        
        let seguir = UIAlertAction(title: "Continuar", style: .default, handler: {
            accion in
            print(accion)
        })
        
        // Agregamos las accion a la alerta
        
        alerta.addAction(cancelar)
        alerta.addAction(seguir)
        
        // Prentamos la alerta
        
        self.present(alerta, animated: true, completion: nil) 

	- UITabBarController

		Es una manera de navegacion por tabs, es cuando ves
		la barra de navegacion abajo en el app esto es UITabBarController

		Nota: Se permiten hasta 5 elementos en el tap, pero lo recomendable es 4
		elementos mas de hay se ve mal

		El controlador que manejara el principal debe de heredar de "UITabBarController"

		* viewDidAppear() -> es una funcion que se utiliza para agregar
		contenido dinamico a la aplicacion, se debe instanciar el del metodo padre
		con super.viewDidAppear(parameter)

		- viewControllers -> es un array que contiene todas las vistas del UITabBarController.
		Como es un array de vistas estas se pueden gestionar como cambiar titulos a agregarles badge

		Ejemplo de agregar una vista dinamicamente.

		```
			override func viewDidAppear(_ animated: Bool){

				super.viewDidAppear(animated);

				let newVista = UIViewController()
				newVista.view.backgroundColor = UIColor.green

				// Agregamos un titulo en el tabBar
				newVista.title = "Un Titulo corto y descriptivo"


				// Agregmos la vista al array de vistas
				self.viewControllers!.append(newVista)

				// Edicion directamente
				self.viewControllers![2].title="OKOK"

			}

		```

		Como agregar mas vistas al UITabBarController?
		Hago clic derecho sobre el el Tab Principal y lo deslizo hacia la vista que le deceo
		asociar, una vez haga esto en el menu (Retationship Segue > View Controller)

	- UINavigationController

		Es un controlador que me permite realizar una navegacion sencilla en IOS.

		Para entender la diferencia entre en UITabBarController vs UINavigationController
		es que el UINavigationController se utiliza para navegacion entre secciones en especifico
		de una seccion en especifico:

		Ej: menu usuario, donde se pueda gestionar todo los usuarios en diferentes pantallas mediante
		el UINavigationController (CRUD)

		Mientras que el UITabBarController es para el menu principal

		Nota: Al igual que el UITabBarController se vera en el storyboard el 
		UINavigationController que a este le puedo asignar un Controller que herede desde
		el UINavigationController en este caso y poder manipular sus vistas.

		Cada seccion en especifico debe tener un UINavigationController Inicial !Important

	- Multiple View Controller

		Nota: es bueno asignar las pantallas de login mediante un segue al home de la app
		y que sea un segue "modality" osea un modal.

		** Para poder manejar las relaciones desde codigo siempre es bueno asignar un ID
		a las relaciones

		**** self.performSegue() -> Que es esto?
		es un metodo de los viewControllers que me permite ejecutar una relacion entre vistas
		mediante el ID de estas relacion. es un IrA por decirlo así


		*** SESSIONES EVER STYLE ^^ ***

		Como guardar sessiones por decirlo asi, para guardar preferencias del usuario
		como por ejemplo si desea que se le envien notificaciones o guardar un token de inicio
		de session para saltar pantallas en caso de ser true

		SET

		UserDefault.standard.setValue("VALOR", forKey: "Identificador");

		// Salvamos
		UserDefault.standard.synchronize()

		GET

		UserDefault.standard.value(forKey: "Identificador o token")
		// Eso devuelve un optional ya que puede que no exita, tratar como tal

		NOTA: en dicha session se pueden guardar token para consultar informacion
		en un webservice o lo que sea.

		*** Cerrar modales ***

		Esto es para que no te suceda lo que ocurria en la version anterior del app
		que una vez que creabas un contacto, y por amor al arte le dabas para atras una
		vez creado regresaba al formulario, por eso esta clase de vistas deben estar en un modal
		para cerrarlas una vez se crea o se realiza la accion

		Nota: es como ir hacia atras ../../../ se colocan los ../ que son necesarios
		para ir hacia atras en este caso de ser ../ es "presentingViewController"
		y al final se instancia el metodo "dismiss()" para cerrar dichos modales

		EJ: presentingViewController?.presentingViewController?.dismiss();

		Si se solo se quiere cerrar un modal se coloca solo "dismiss()" dentro de este

		OK??


		***** NOTA IMPORTANTE *****

		Como instertar un UINavigationController o un UITabBarController en una vista?
		Menu > Editor > Embed In

	- ScrollViews

		Esta es una vista que me permite agregar mas contenido que el tamaño que tiene la pantalla

		* El elemento se llama asi mismo, y se coloca dentro de la vista

		* Este como es un elemento se debe tratar como tal y se debe agregar al codigo como 
		un @IBOutlet

		Horizontal con botones EJEMPLO

		@IBOutlet weak var grid: UIScrollView!
    
	    override func viewDidLoad() {
	        super.viewDidLoad()
	        
	        for i in 0...5{
	            
	            let newGrid = UIView()
	            
	            // Set Tamanio
	            
	            if i == 0{
	                newGrid.frame = CGRect(x: 0, y: 0, width: self.grid.frame.size.width, height: self.grid.frame.size.height)
	            }else{
	                newGrid.frame = CGRect(x: CGFloat(i)*self.view.frame.size.width+CGFloat(15*i), y: 0, width: self.grid.frame.size.width, height: self.grid.frame.size.height)
	            }
	            
	            newGrid.backgroundColor = UIColor(red: CGFloat(arc4random_uniform(255))/255.0, green: CGFloat(arc4random_uniform(255))/255.0, blue: CGFloat(arc4random_uniform(255))/255.0, alpha: 1.0)
	            
	            grid.addSubview(newGrid)
	        }
	        
	        grid.contentSize = CGSize(width: ((self.view.frame.size.width+CGFloat(15))*6)-15, height: self.grid.frame.size.height)
	        grid.showsVerticalScrollIndicator = false
	    }
	    
	    @IBAction func Excecute(_ sender: UIButton) {
	        
	        
	        let currentX = grid.contentOffset.x
	        
	        let vistaActual = Int(currentX / grid.frame.size.width)
	        
	        var nuevaVista = 0
	        
	        if sender.currentTitle! == "Anterior"{
	            
	            nuevaVista = vistaActual - 1;
	            
	        }else if sender.currentTitle! == "Siguiente"{
	            
	            nuevaVista = vistaActual + 1
	        }else if sender.currentTitle! == "Cerrar"{
	            
	            self.dismiss(animated: true, completion: nil)
	            
	        }
	        
	        if(nuevaVista<0 || nuevaVista > 5){
	            return
	        }
	        
	        let newX = CGFloat(nuevaVista) * self.grid.frame.size.width
	        
	        grid.contentOffset = CGPoint(x: newX, y: grid.contentOffset.y)
	    }

	    VERTICAL EJEMPLO ^^^

	    @IBOutlet weak var scroll: UIScrollView!
    
	    var hasta:Int = 10

	    override func viewDidLoad() {
	        super.viewDidLoad()

	        // Do any additional setup after loading the view.
	        
	        for i in 0...self.hasta{
	            
	            let vista = UIView()
	            
	            if i == 0{
	                vista.frame = CGRect(x: 0, y: 0, width: self.view.frame.size.width, height: scroll.frame.size.height)
	            }else{
	                vista.frame = CGRect(x: 0, y: CGFloat(i)*scroll.frame.size.height+CGFloat(15*i), width: self.view.frame.size.width, height: scroll.frame.size.height)
	            }
	            
	            vista.backgroundColor = UIColor(red: CGFloat(arc4random_uniform(255))/255.0, green: CGFloat(arc4random_uniform(255))/255.0, blue: CGFloat(arc4random_uniform(255))/255.0, alpha: 1.0)
	            
	            scroll.addSubview(vista)
	        }
	        
	        scroll.contentSize = CGSize(width: self.view.frame.size.width, height: (scroll.frame.size.height+CGFloat(15))*CGFloat((self.hasta+1)) - 15)
	    }


	    Como cargar imagenes en un scroll vertical?

	    for i in 0...hasta{
            
            let img = URL(string: "http://lorempixel.com/375/375/")
            
            let session = URLSession(configuration: .default)
            
            let res = session.dataTask(with: img!) { (data, response, error) in
                if let e = error {
                    print("Error downloading cat picture: \(e)")
                } else {
                    // No errors found.
                    // It would be weird if we didn't have a response, so check for that too.
                    if let res = response as? HTTPURLResponse {
                        print("Downloaded cat picture with response code \(res.statusCode)")
                        if let imageData = data {
                            // Finally convert that Data into an image and do what you wish with it.
                            let image = UIImage(data: imageData)
                            
                            let carView = UIImageView(image: image)
                            
                            if i == 0{
                                carView.frame = CGRect(x: 0, y: 0, width: self.view.frame.size.width, height: self.gridImg.frame.size.height)
                            }else{
                                carView.frame = CGRect(x: 0, y: CGFloat(i)*self.gridImg.frame.size.height+CGFloat(15*i), width: self.view.frame.size.width, height: self.gridImg.frame.size.height)
                            }
                            
                            self.gridImg.addSubview(carView)
                            
                            
                            // Do something with your image.
                        } else {
                            print("Couldn't get image: Image is nil")
                        }
                    } else {
                        print("Couldn't get response code for some reason")
                    }
                }
            }
            
            res.resume()
            
        }
        
        self.gridImg.contentSize = CGSize(width: self.view.frame.size.width, height: (gridImg.frame.size.height+CGFloat(15))*CGFloat((self.hasta+1)) - 15)

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

