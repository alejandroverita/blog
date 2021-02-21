# CURSO PRACTICO DE MAQUETACION EN CSS

[Curso](https://platzi.com/clases/practico-css/ "Curso")

**Requisitos previos**
- [Desarrollo web online](https://platzi.com/clases/html5-css3/ "Desarrollo web online")

**Herramientas**
- [IDE ](https://code.visualstudio.com/ "IDE ")
- [Navegador](https://www.google.com/chrome/ "Navegador")

**Repositorio**
- [Proyecto Blog](https://github.com/degranda/Platzi-blog "Proyecto Blog")

<br>

[========]

## CHROME DEVTOOLS

Es una serie de herramientas que facilitan el proceso de desarrollo. Podemos ver en tiempo real que estamos haciendo con CSS,JS, podemos ver peticiones, imágenes y demás. Incluso podemos hacer debuggin para hallar problemas al momento de renderizarse.

**Tips:**

- Con F12 abres el inspector de elementos de manera más sencilla
- Con Ctrl + u puedes ver el codigo de tu pagina o de cualquier sitio web

**¿Cómo podemos acceder? **

Para acceder al Chrome Dev Tools podemos con:

1.  Accediendo a una página cualquiera y dandole click derecho + inspeccionar.
2. En el menú de Chrome, seleccionar More Tools > Developer Tools.
3. Usando la combinación de teclas Ctrl+Mayúsculas+I (Windows) y Cmd + Option + I (Mac).

<br>

[========]


## DISEÑO DEL PROYECTO

**Archivos del proyecto**
- [Archivos](https://github.com/degranda/Platzi-blog "Archivos")

**Enlaces útiles **

- [CSS TRICK](https://css-tricks.com/snippets/css/complete-guide-grid/ "CSS TRICK")
- [CSS REFERENCE](https://cssreference.io/css-grid "CSS REFERENCE")/
- [Developers Mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/grid "Developers Mozilla")
- [W3 SCHOOLS](https://www.w3schools.com/css/default.asp "W3 SCHOOLS")

<br>


[========]

## SETUP DEL PROYECTO

- index.html
- blog.html
- blogs.html
- perfil.html

**Carpetas**
- Assets
	- iconos
	- imagenes
- CSS
	- main.css

<br>

[========]


##  ARQUITECTURA DEL HEADER EN HTML

**Etiquetas semánticas HTML**

Semántica se refiere a todo aquello que tiene que ver con el significado de una palabra u expresión. En HTML, existen etiquetas con significado semántico, etiquetas que por si mismas brindan un poco de información sobre que tipo de contenido hay dentro de ellas.
|
El correcto etiquetado del contenido, con los tags que brindan una descripción de lo que hay entre la etiqueta de apertura y la etiqueta de cierre, permite dar información rápida sobre el contenido de cada etiqueta semántica, mediante el nombre de la propia etiqueta.
|
**¿Porqué es importante el buen uso de las etiquetas semánticas dentro de HTML?** 

🔶Permite una mejor legibilidad del contenido de un documento HTML, tanto para el desarrollador, como para un indexador de contenido.
🔶Al mejorar la legibilidad para los motores de búsqueda mejorará su posicionamiento.
🔶Permite el desarrollo de contenido escalable.
🔶Contenido ordenado y estructurado.

**¿Cómo hacer uso correcto de la semántica HTML?**

Selecciona la etiqueta que describa el significado del contenido que deseas marcar, gracias a que existe una gran variedad de etiquetas para poder usar, esto no será muy complicado.

🔴Etiquetas no semánticas ** div** y ** span** No describen nada sobre su contenido.

🟢Etiquetas semánticas **table>** y **p>** Describen claramente su contenido.

Algunas etiquetas semánticas: **

🔹p:** Define un parrafo.
🔹form: Define un formulario.
🔹table: Define una tabla.
🔹style: Define estilos para el documento.
🔹header: Define la típica sección de encabezado que normalmente contiene el logo y el menu de navegación .
🔹nav: Elemento que contiene los lincks de navegación.
🔹section: Define una sección en concreto del documento.
🔹footer: Define el píe de página de un documento o seccón.
🔹main: Define el contenido principal de un documento.
🔹aside: Define contenido relacionado con el contenido principal, pero que no forma parte de manera relevante para él.

Codigo de la clase:

    <link rel="stylesheet" href="/css/main.css">
    +
     </head>
     <body>
    -
    +   <header>
    +       <section>
    +           <div>
    +               <a href="">Facebook</a>
    +               <a href=""> Instagram</a>
    +               <a href=""> Linkedin</a>
    +               <a href="">Github</a>
    +           </div>
    +       </section>
    +       <nav>
    +           <section>
    +             <a href="">LOGO</a>
    +           </section>
    +           <section>
    +            <a href="perfil.html">Sobre mi</a>
    +           </section>
    +       </nav>
    +   </header>
    

<br>

[========]


##  ESTILOS EN EL HEADER 

    body {
        margin: 0;
        padding: 0;
        position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
    }
    
    a {
        text-decoration:  none;
        display: inline;
        color: black;
    
    }
    
    header {
        width: 100%;
        height: 140px;
        display: grid;
        grid-template-rows: 1fr 1fr;
    }
    
    header .header__icons--container {
        width: 100%;
        height: 50px;
        display: flex;
        background-color: #47cfac;
    }
    
    header .header__icons--container .icons {
        width: 300px;
        height: auto;
        display: flex;
        justify-items: flex-end;
        align-items: center;
        justify-content: space-between;
        justify-self: end;
        margin-right: 50px;
    }



<br>

[========]



## 	AGREGANDO ICONOS

[Pack de iconos usado en la clase:](https://www.flaticon.com/packs/social-media-86 "Pack de iconos usado en la clase:")

**HTML**

     <link rel="stylesheet" href="./css/font/font/flaticon.css">
    
    </head>
    <body>
       <header>
           <section class="header__icons--container">
               <div class="icons">
                   <a href=""> <span class="fimanager flaticon-001-facebook"></span></a>
                   <a href=""> <span class="fimanager flaticon-011-instagram"></span></a>
                   <a href=""> <span class="fimanager flaticon-003-whatsapp"></span></a>
                   <a href=""> <span class="fimanager flaticon-010-linkedin"></span></a>
               </div>


**CSS**

    header .icons span::before{
        /* los íconos se tratarán como fuentes */
        color: white;
        font-size: 30px;
    } 
	
	

<br>

[========]



## 	AGREGANDO IMÁGENES AL HEADER

**HTML**

     <nav>
               <section class="nav__logo--container">
                 <a href=""><img src="assets/img/Logo-negro.png" alt="Logo de mi blog"></a>
               </section>
               <section class="profile__link">
                <a href="perfil.html">Sobre mi</a>
               </section>
           </nav>
       </header> 
       <main>
            <div class="main__container">
                <h2 class="main__container--title">
                    Conoce las novedades y noticias del mundo Tech
                </h2>
                <div class="main__container--button">
                    <a href="/">Entra ya!</a>
                </div>
            </div>
       </main>



**CSS**

    nav {
        display: grid;
        grid-template-columns: 1fr 1fr;
        height: 90px;
    }
    
    
    nav .nav__logo--container {
    
        margin-left: 50px;
    
    }
    
    nav .nav__logo--container img {
        width: 220px;
        margin-top: 10px;
    }
    
    nav .profile__link {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        margin-right: 50px;
    }
    
    nav .profile__link a {
        color: black;
        border-bottom: 1px solid black;
    }
    
    main {
        height: 100%;
        background-image: url(../assets/img/Cover.png);
        background-size: cover;
        background-position: center;
        display: flex;
        justify-content: center;
    }
    
    main .main__container{
        text-align: center;
    }
    
    main .main__container .main__container--title {
        color: white;
        letter-spacing: 10px;
        font-size: 40px;
        width: 50rem
    }
    
    main .main__container .main__container--button {
        height: 40px;
        background-color: #47cfac;
        width: 100px;
        margin: 100px auto;
        display: grid;
    }
    
    main .main__container .main__container--button a {
        font-size: 15px;
        margin: auto;
        font-weight: bold;
    }



<br>

[========]


## MANEJO DE IMÁGENES DE BACKGROUND

    background-image: url('../assets/img/Cover1.png');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;


<br>

[========]

## AGREGANDO FUENTES

En el CSS:

@import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;500;700&family=Roboto+Slab:wght@400;700&family=Roboto:wght@400;500;700;900&display=swap');

`font-family: 'Roboto mono' 'monospace';`

## TERMINANDO EL HOME


## ESTILOS DEL BOTÓN

    .blogs__button {
        border: 1px solid #47cfac;
        padding: 10px 15px;
        font-size: 12px;
        transition: all .5s;
    
    }
    
    .blogs__button:hover{
        border: 1px solid white;
        color: white;
        background-color: #48cfad;
    }
	


## TRABAJANDO EN LA SECCION EL POST

## GRID CONTAINER


## CREAR LA PANTALLA DE BLOG

## AGREGANDO ESTILOS A LA PAGINA DE BLOG

## SECCION DE CONTACTO













