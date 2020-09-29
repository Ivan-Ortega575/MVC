<h1>Instituto Tecnológico de Milpa Alta ll
  
<h1>Patron MVC</h1>

<h2>Introducción (Definición de MVC y su relación con los patrones de diseño de software)</h2>

Modelo Vista Controlador (MVC) es un estilo de arquitectura de software que separa los datos de una aplicación, la interfaz de usuario, y la lógica de control en tres componentes distintos.
Se trata de un modelo muy maduro y que ha demostrado su validez a lo largo de los años en todo tipo de aplicaciones, y sobre multitud de lenguajes y plataformas de desarrollo.

•	El Modelo que contiene una representación de los datos que maneja el sistema, su lógica de negocio, y sus mecanismos de persistencia.

•	La Vista, o interfaz de usuario, que compone la información que se envía al cliente y los mecanismos interacción con éste.

•	El Controlador, que actúa como intermediario entre el Modelo y la Vista, gestionando el flujo de información entre ellos y las transformaciones para adaptar los datos a las necesidades de cada uno.

<h2>¿Que framework utiliza el modelo MVC?</h2>
  
  El MVC o Modelo-Vista-Controlador es un patrón de arquitectura de software que, utilizando 3 componentes (Vistas, Models y Controladores) separa la lógica de la aplicación de la lógica de la vista en una aplicación. Es una arquitectura importante puesto que se utiliza tanto en componentes gráficos básicos hasta sistemas empresariales; la mayoría de los frameworks modernos utilizan MVC (o alguna adaptación del MVC) para la arquitectura, entre ellos podemos mencionar a Ruby on Rails, Django, AngularJS y muchos otros más.
Frameworks MVC


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

create schema if not exists estudiante;

use estudiante;

create table if not exists estudiante(
  id_estudiante int not null auto_increment primary key,
  nombre varchar(45) not null, 
  paterno varchar(45) not null, 
  materno varchar(45) not null, 
  movil varchar(45) not null
)engine =  innodb;

insert into estudiante(nombre, paterno, materno, movil) values("Ivan", "Manzanita", "Ortega", "5577655927");

<h2>VISTA</h2>

//<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <link rel="stylesheet" href="css/bootstrap4/bootstrap.css">
  <link rel="stylesheet" href="css/sweetalert2/sweetalert2.min.css">
</head>
//<body>

<div class="container">
      <div class="row mt-5">
      <div class="col-sm-4"></div>
        <div class="col-sm-4  mt-5">
          <div class="card" style="width: 18rem;">
            <img class="card-img-top" src="img/error_capa_8.png" alt="Card image cap">
            <div class="card-body">
              <form>
                <div class="form-group d-flex justify-content-end">
                  <a class="badge badge-light" href="view/registro.php">Registrarse</a>
                </div>
                <div class="form-group">
                  <label for="mi_usuario">Usuario</label>
                  <input type="text" class="form-control" id="mi_usuario" placeholder="Ingresa tu usuario">
                </div>
                <div class="form-group">
                  <label for="mi_password">Password</label>
                  <input type="password" class="form-control" id="mi_password" placeholder="Password">
                </div>
                <div class="form-check d-flex justify-content-end">
                  <!-- <button type="submit" class="btn btn-dark">Entrar</button> -->
                  <span class="btn btn-dark" id="btn_entrar_al_sistema">Entrar</span>
                </div>
              </form>
            </div>
          </div>
        </div>
        <div class="col-sm-4"></div>
      </div>
    </div>



<h2>CONTROLADOR</h2>

<?php 

  session_start();
  require_once "conexion.php";

  $objeto_conexion = conexion();

  $usuario_recibido = $_POST['usuario'];
  $password_recibido = sha1($_POST['password']);

  $query_de_busqueda = "SELECT * FROM usuarios WHERE usuario='$usuario_recibido' and password='$password_recibido'";

  $resultado_del_query= mysqli_query($objeto_conexion, $query_de_busqueda);

  if(mysqli_num_rows($resultado_del_query) > 0){
    $_SESSION['user']=$usuario_recibido;
    echo 1;
  }else{
    echo 0;
  }
  
?>









