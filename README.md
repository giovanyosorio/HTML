Las listas son una de las construcciones más usadas a la hora de elaborar textos, no sólo en HTML. No obstante, en HTML están también presentes y pueden ser de 3 tipos:

Listas Numeradas: que son aquellas que expresan un orden enre los diferentes elementos de la lista. Este orden podrá ser numérico, alfabético etc..
Listas no numeradas: que simplemente muestra los elementos de la lista uno tras otro.
Listas de definición: que muestran diversos términos junto con su definición.
A continuación vamos a ver el árbol DOM para cada una de esta variedades:

Lista Numeradas


Un ejemplo:
```html
    <!-- Listas numeradas -->
    <h3>Lista Numerada - Ordered List (ol)</h3>
    <ol>
        <li>Primer elemento</li>
        <li>Segundo elemento</li>
        <li>Tercer Elemento</li>
        <li>Cuarto elemento</li>
    </ol>
```
ol sería la etiqueta padre y cada uno de los elemento de la lista iría en una etiqueta li.

Listas no Numeradas


Un ejemplo:
```html
    <!-- Listas no numeradas-->
    <h3>Lista NO Numerada - Unordered List (ul)</h3>
    <ul>
        <li>Primer elemento</li>
        <li>Segundo elemento</li>
        <li>Tercer Elemento</li>
        <li>Cuarto elemento</li>
    </ul>
    ```
ul sería la etiqueta padre y cada uno de los elemento de la lista iría en una etiqueta li.

Listas de definición


Un ejemplo:
```html
    <!-- Listas de definición-->
    <h3> Lista de descripción - Description List (dl)</h3>
    <dl>
        <dt>Primer término</dt>
        <dd>Definición del primer término</dd>
        <dt>Segundo término</dt>
        <dd>Definición del segundo término</dd>
        <dt>Tercer término</dt>
        <dd>Definición del tercer término</dd>
        <dt>Cuarto término</dt>
        <dd>Definición del cuarto término</dd>
    </dl>
    ```html
dl sería la etiqueta padre y cada término se define mostrando consecutivamente las etiquetas dt, que se corresponde con el término que vamos a definir, y dd que es la definición del término anterior.


Tables
Otras de las construcciones básicas en HTML son las tablas.

Además de para la presentación de elementos se usaron históricamente para dar estructura a las páginas. No obstante, por motivos que explicaremos en el próximo curso de este itinerario, ya no se maqueta con tablas.

A pesar de eso siguen siendo un elemento importante y a continuación vamos a presentar varias formas de hacer tablas.

Tablas Simples
La estructura del árbol DOM más simple para una tabla sería similar a la siguiente:

Una etiqueta <table> que contiene toda la tabla.
Como hijos directos, tantas etiquetas como fijas queramos que tenga nuestra tabla.
Dentro de cada filas tantas celdas ( o ) como queramos que tengan nuestras filas.La única diferencia entre estas dos es que el contenido en la segunda se presenta centrado y el texto en negrita.
NOTA: Si no coinciden el número de celdas en todas las filas veremos que sucecen cosas “extrañas”.

NOTA: La anchura de las celdas de una misma columna será la anchura de la más ancha de la columna.

NOTA: La altura de las celdas de una misma fija será la altura de la más alta de la fila.



Un ejemplo sería:

    <table>
        <tr>
            <th>Nombre</th>
            <th>Apellidos</th>
            <th>Dirección</th>
        </tr>
        <tr>
            <td>Pepe</td>
            <td>Pérez</td>
            <td>Aquí</td>
        </tr>
        <tr>
            <td>Manuel</td>
            <td>López</td>
            <td>Allí</td>
        </tr>
        <tr>
            <td>María</td>
            <td>Fernández</td>
            <td>Mas allá</td>
        </tr>
        <tr>
            <td>Sara</td>
            <td>Gallardo</td>
            <td>Mas aquí</td>
        </tr>

    </table>
Tablas Completas
Existe además una forma más precisa y completa de construir tablas. Una forma que puede contener (aunque no es obligatorio) otras etiquetas dentro de la etiqueta raíz <table>. Estas nuevas etiquetas pueden ser:

<colgroup> que nos permite agrupar los columnas para darles estilos. Cada uno de esos grupos lo definiremos usando una etiqueta con un atributo span para definir el número de columnas de cada grupo.
<caption> para añadir un título o leyenda a la tabla en la parte superior.
<thead> que contendrá la fila (usualmente) o filas que sean la cabecera de una tabla.
<tbody> que es donde pondremos las filas que son el contenido propiamente dicho de la tabla, el cuerpo.
<tfoot> que es donde pondremos las filas que son el pie de nuestra tabla.


Un ejemplo sería:

<table>
        <colgroup>
            <col span="3" style="background-color: grey">
            <col style="background-color: yellow">
            <col style="background-color: green">
        </colgroup>
        <caption>Alumnos matriculados</caption>
        <thead>
            <tr>
                <th>Nombre</th>
                <th>Apellidos</th>
                <th>Dirección</th>
                <th>Teléfono</th>
                <th>Email</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Pepe</td>
                <td>Pérez</td>
                <td>Aquí</td>
                <td>11111111</td>
                <td>yosoy@pepe.es</td>
            </tr>
            <tr>
                <td>Manuel</td>
                <td>López</td>
                <td>Allí</td>
                <td>222222222</td>
                <td>yosoy@manuel.es</td>
            </tr>
            <tr>
                <td>María</td>
                <td>Fernández</td>
                <td>Mas allá</td>
                <td>33333333</td>
                <td>yosoy@maria.es</td>
            </tr>
            <tr>
                <td>Sara</td>
                <td>Gallardo</td>
                <td>Mas aquí</td>
                <td>44444444</td>
                <td>yosoy@sara.es</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td>Pie de la tabla donde pongo más texto para que se vea como crecen</td>
            </tr>
        </tfoot>
    </table>
Tablas Complejas
Con todo lo explicado anteriormente podemos ver que las tablas que conseguimos son relativamente sencillas. En la vida real, nos encontraremos con estructuras tabulares más complejas. Éstas también se pueden construir en HTML utilizando los siguientes atributos en las etiquetas y , es decir, en las celdas.

rowspan: me va a permitir que una celda ocupe más de una fila.
colspan: me va a permitir que una celda ocupe más de una columna.
NOTA: Antes de escribir el código HTML de una tabla compleja es recomendable estudiar su estructura previamente. Puede parecer broma pero yo sigo usando papel y lápiz para eso ;) (tú mismo)

Un ejemplo sería:

<table>
        <caption>HORARIO DE CLASE CURSO 2018-2019</caption>
        <thead>
            <tr>
                <th>HORAS</th>
                <th>Lunes</th>
                <th>Martes</th>
                <th>Miércoles</th>
                <th>Jueves</th>
                <th>Viernes</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>8:00</td>
                <td rowspan="2">Matemáticas</td>
                <td>Lengua</td>
                <td>Inglés</td>
                <td colspan="2">Ciencias</td>
            </tr>
            <tr>
                <td>9:00</td>
                <td>Historia</td>
                <td>Ciencias</td>
                <td>Matemáticas</td>
                <td>Lengua</td>
            </tr>
            <tr>
                <td>10:00</td>
                <th colspan="5">RECREO</th>
            </tr>
            <tr>
                <td>10:30</td>
                <td>Inglés</td>
                <td rowspan="2">Ciencias</td>
                <td>Matemáticas</td>
                <td>Lengua</td>
                <td>Historia</td>
            </tr>
            <tr>
                <td>11:30</td>
                <td>Historia</td>
                <td>Ciencias</td>
                <td>Matemáticas</td>
                <td>Inglés</td>
            </tr>
        </tbody>
    </table>

    
    Los formularios son otros de los elementos que se han asociado desde siempre a las páginas webs. Los hemos usado tanto que es difícil calcular cuántos formularios habremos rellenado a lo largo de nuestra larga vida (al menos la mía) como usuario de la web.

Formularios de registro, usuario y contraseña, solicitudes etc… son contextos en los que los podemos encontrar.

De un modo más formal podemos decir lo siguiente:

Los formularios son elementos, que como los enlaces, permiten una interacción del usuario con la página web.
Su tarea principal es recoger información. El usuario, por tanto, debe introducir esa información en los campos del formulario.
Una vez se ha recogido esa información el formulario la enviará al servidor, por correo o donde decida el programador para ser tratada, mostrada y/o almacenada.
Estructura del formulario
En un formulario nos podemos encontrar con muchos elementos.



El más importante de todo es el elemento padre, la etiqueta <form> que va a contener en su interior todos los elementos que conformen nuestros formularios.

Esta etiqueta puede tener varios atributos de entre los que destacamos:

method que indica cómo se va a pasar la información al destino. Puede ser por GET (se ve la información en la barra del navegador) y por POST ( no se ve y es la opción por defecto).
action que indica el destino de nuestros datos. Normalmente será una URL o dirección de Internet. Existen más opciones. Os invito a visitar la documentación de referencia.
A continuación vamos a ver algunos de los elementos más frecuentes y a describir su estructura y funcionamiento.

Labels e Input
Normalmente para la recogida de información los formularios usando etiquetas <input>. Pero, para poder saber qué campos estamos rellenando una buena práctica (se puede de otras maneras menos elegantes) es poner una etiqueta (etiqueta)delante de cada input para dar nombre y asociar ambas.

Un ejemplo sería:

<label for="nombre">Nombre:</label>
<input type="text" name="nombre" />
Aquí estamos asociando la etiqueta al campo usando los atributos for y name.

El campo que hemos usado para la recogida de información es un input. Existen muchos tipos que veremos con más detalle en el próximo apartado.

Listas desplegables
Son elementos que también hemos visto muchas veces. Al hacer click sobre ellos nos muestran varias opciones de las que podremos escoger una o varias.

Para crear listas desplegables usaremos las etiquetas <select> como etiqueta padre y una etiqueta <option> para cada una de las opciones que tengamos en la lista desplegable. Si queremos agrupar esas opciones las meteremos a su vez dentro de una etiqueta <optgroup>.

Un ejemplo sería:

<select name="provincia">
    <optgroup label="Aragon">
        <option value="Z">Zaragoza</option>
        <option>Huesca</option>
        <option selected>Teruel</option>
    </optgroup>

</select>
Fijaros los nuevos atributos que he metido.

Áreas de Texto
Son campos de formulario para meter texto largos. Tienen dos atributos interesantes.

rows: para indicar el número de filas que tiene el campo.
cols: para indicar el número de columnas que tiene el campo.
Un ejemplo sería:

<textarea cols="10" rows="10">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque voluptate corrupti ut earum, aliquam sint amet repellendus, vitae placeat repellat quis, ipsa qui. Velit placeat reiciendis tempore autem nostrum eaque?
</textarea>
Botones
La etiqueta <button> no creo que se necesario explicar para que sirve…Haz click!!!

El atributo más importante que tienen es type que puede tomar tres valores:

button: se comporta como un botón que puede estar presionado o no. Nada especial.
reset: al hacer click borra todos los datos introducidos previamente en el formulario y pone los valores por defecto.
submit: al hacer click envía los datos introducidos al destino que hemos puesto en el action del formulario.
Agrupando atributos
Hay situaciones en las que los campos de los formularios por significado, por importancia o por cualquier razón, queremos que se muestren agrupados. Para estos casos tenemos la etiqueta <fieldset> que la usaremos siguiente el siguiente esquema:



Siendo:

<legend> una etiqueta que contiene el nombre del grupo y que se mostrará en la parte de arriba.
controles todos los campos que queramos meter.
NOTA: la etiqueta tiene un borde por defecto

Un ejemplo sería:

<fieldset>
    <legend>Datos Personales</legend>
    <p>
        <label for="nombre">Nombre:</label>
        <input type="text" name="nombre" placeholder="Inserta Nombre" required />
    </p>
    <p>
        <label for="apellidos">Apellidos:</label>
        <input type="text" name="apellidos" value="Pérez" readonly />
    </p>

    <p>
        <label for="provincia">Provincia</label>
        <select name="provincia">
            <optgroup label="Aragon">
                <option value="Z">Zaragoza</option>
                <option>Huesca</option>
                <option selected>Teruel</option>
            </optgroup>

        </select>
    </p>

    <p>
        <input type="submit" value="Enviar" />
    </p>
</fieldset>
Atributos interesantes de los elementos de los formularios
Además existen una serie de atributos interesantes que podemos añadir a los controles o elementos de los formularios:

required que indica que un control es obligatorio de rellenar.
disabled que mostrará el elemento como deshabilitado.
readonly que nos dice que el campo es de sólo lectura.
placeholder que muestra un mensaje en los input dando pistas de lo que debemos poner. Al empezar a rellenarlo desaparece.
selected indica la opción seleccionada.
value el valor que tiene el elemento..
tabindex para asegurarnos que podemos navegar por los elementos usando el tabulador podemos establecer un orden para cada uno.
multiple para seleccionar varias opciones en una lista desplegable.
Y muchos más….




## Formulario

![image](https://user-images.githubusercontent.com/30839218/219141761-db9f36c8-1ea5-49f9-b7b2-1b98a51cc729.png)
    
![]([https://pandao.github.io/editor.md/examples/images/4.jpg](https://user-images.githubusercontent.com/30839218/219141761-db9f36c8-1ea5-49f9-b7b2-1b98a51cc729.png))

Muchos de ellos son nuevos en HTML5 por lo que es importante comprobar cómo se ven en los distintos navegadores o comprobarlo de manera previa usando la página HTML5 Test.

Tienen especial relevancia los siguientes:

Radio Groups
Checkboxes
Datalist
Radio Group
Es una agrupación de inputs que presenta opciones que queremos que sean excluyentes:

Un ejemplo sería:

<label for="genero">Sexo</label>
<input type="radio" name="genero" value="masculino" />Hombre<br />
<input type="radio" name="genero" value="fememino" checked />Mujer<br />
Para que sean excluyentes deben de tener el mismo valor para el atributo name y el type=”radio”

CheckBoxes
Es una agrupación de opciones que presenta opciones de las cuáles podemos elegir una o varias.

Un ejemplo sería:

    <label for="dispositivos">Dispositivos electrónicos</label><br />
    <input type="checkbox" name="dispositivos" value="pc" />PC<br />
    <input type="checkbox" name="dispositivos" value="table" />Tableta<br />
    <input type="checkbox" name="dispositivos" value="movil" />Móvil
Fijaros que para agruparlos deben de tener el mismo valor para name y el type=”checkbox”

Data Lista
Es una nueva forma en HTML5 de hacer una lista de valores posibles para un input.

Un ejemplo sería:

    <input list="editor">

    <datalist id="editor">
        <option value="Atom">
        <option value="NotePad++">
        <option value="VsCode">
        <option value="Sublime">
        <option value="Brackets">
    </datalist>
Con el atributo list indicamos la lista de opciones que vamos a tener y en la etiqueta metemos las que queramos.

Es importante destacar que podríamos meter otras opciones en el Input pero al usar esta estructura se nos ayuda a rellenarlo y a elegir la opción correcta.
