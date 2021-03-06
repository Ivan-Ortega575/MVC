<h1>Instituto Tecnológico de Milpa Alta ll
  
<h1>Patron MVC</h1>

![MVC](https://user-images.githubusercontent.com/72004435/94627687-d4420580-0283-11eb-8018-9d465231d391.png)


<h2>Introducción (Definición de MVC y su relación con los patrones de diseño de software)</h2>

Modelo Vista Controlador (MVC) es un estilo de arquitectura de software que separa los datos de una aplicación, la interfaz de usuario, y la lógica de control en tres componentes distintos.
Se trata de un modelo muy maduro y que ha demostrado su validez a lo largo de los años en todo tipo de aplicaciones, y sobre multitud de lenguajes y plataformas de desarrollo.

•	El Modelo que contiene una representación de los datos que maneja el sistema, su lógica de negocio, y sus mecanismos de persistencia.

•	La Vista, o interfaz de usuario, que compone la información que se envía al cliente y los mecanismos interacción con éste.

•	El Controlador, que actúa como intermediario entre el Modelo y la Vista, gestionando el flujo de información entre ellos y las transformaciones para adaptar los datos a las necesidades de cada uno.

<h2>¿Que framework utiliza el modelo MVC?</h2>
  
Un framework es una estructura software compuesta de componentes personalizables e intercambiables para el desarrollo de una aplicación. Es un marco (Framework) en el que nosotros vamos a definir piezas. El marco define las reglas del juego a las que nos tenemos que atener. Pensemos en ellos como un puente para realizar código más rápido y fácil.
Los objetivos principales que persigue un framework para la web son: acelerar el proceso de desarrollo, reutilizar código ya existente y promover mejores prácticas de desarrollo como el uso de patrones de diseño.
Haciendo una analogía, podemos imaginar que el framework es un conjunto de ingredientes culinarios cortados y preparados para usarlos. Según qué componentes utilizamos y cómo los hayamos cocinado, crearemos un plato u otro.

-Ejemplos de frameworks

•	CodeIgniter (php) 

•	CakePHP 

•	Symfony 

•	Ruby on Rails

•	Padrino 

•	ASP.NET


![PHP-MVC-framework1](https://user-images.githubusercontent.com/72004435/94627537-79a8a980-0283-11eb-9e9f-b130ea9cb484.png)


<h2>¿Qué ventajas ofrece el modelo MVC?</h2>

Entre las principales ventajas que puede ofrecernos un desarrollo MVC podemos destacar las siguientes:
Separación clara de dónde tiene que ir cada tipo de lógica, facilitando el mantenimiento y la escalabilidad de nuestra aplicación.
Sencillez para crear distintas representaciones de los mismos datos.
Facilidad para la realización de pruebas unitarias de los componentes, así como de aplicar desarrollo guiado por pruebas (Test Driven Development o TDD).
Reutilización de los componentes.
No existe ciclo de vida de las páginas. Con menos peso, menos complejidad.
Motor de Routing asociando una URL concreta con su correspondiente controlador, permitiendo URL semánticas. Las URL semánticas se indexan mejor en los buscadores, siendo más adecuadas para el posicionamiento web.
Recomendable para el diseño de aplicaciones web compatibles con grandes equipos de desarrolladores y diseñadores web que necesitan gran control sobre el comportamiento de la aplicación.

<h2>¿Qué otros modelos/framework existen de patrones de diseño? </h2>

Si bien los patrones y tácticas son fundamentales en la creación arquitecturas de software, estos conceptos resultan abstractos y en ocasiones no es claro cómo conectarlos con la tecnología que se usa para el desarrollo. Es así que otro elemento clave son los Frameworks. Estos son elementos reutilizables de software que proveen funcionalidades genéricas enfocadas a resolver cuestiones recurrentes. Existen frameworks para resolver distintos aspectos de una aplicación; por ejemplo, Java Server Faces (JSF) es un framework para  crear interfaces de usuario en aplicaciones web. Existen muchos otros frameworks para resolver todo tipo de aspectos, como el manejo de XML, el acceso a bases de datos relacionales, manejo de concurrencia, etcétera.
Los frameworks típicamente se basan en patrones y tácticas. Un ejemplo de ello es el framework Swing para creación de interfaces de usuario en Java, que aplica patrones como Modelo-Vista-Controlador (MVC), Observador y Composite; e incorpora tácticas de modificabilidad y usabilidad tales como la generalización de módulos y la separación de elementos de interfaz de usuario.

<h2>Ejemplifique un modelo MVC en el lenguaje de preferencia (Se consideran la organización de los archivos)</h2>

<h1>LOGIN</h1>

<h2>MODELO</h2>

![Slide1 (2)](https://user-images.githubusercontent.com/72004435/94626010-bd011900-027f-11eb-8752-1d907c9d685b.JPG)



<h2>VISTA</h2>

![Slide1 (2)](https://user-images.githubusercontent.com/72004435/94626367-968fad80-0280-11eb-9bbe-eaceb15e45e4.JPG)



<h2>CONTROLADOR</h2>

![Slide1 (2)](https://user-images.githubusercontent.com/72004435/94626772-5da40880-0281-11eb-93c7-d7f062ec76a2.JPG)










