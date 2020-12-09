

## Crear el proyecto con dos Activities.

<img src="medio\1.PNG/">
<img src="medio\2.PNG/">
<img src="medio\3.PNG/">


## o Cree la segunda Activity yendo al panel Project > Android y dar clic derecho sobre la carpeta app de su proyecto y dar a New > Activity > Empty Activity, nombre este activity como Segunda.

## o Use el mismo nivel de API y el lenguaje de programación Kotlin. Al final crearemos dos Activities con las siguientes características

<img src="medio\4.PNG/">
<img src="medio\5.PNG/">

## Diseñando la primera Activity.

## Detallando las propiedades del activity_main

## o Abra activity_main.xml desde el panel Proyecto > Android si aún no está abierto. Si la pestaña Design (diseño) aún no está seleccionada, haga clic en ella.

<img src="medio\6.PNG/">

##  A continuación, se le presenta la estructura del activity, su trabajo será diseñar en base a lo mostrado, es posible que no obtenga el mismo diseño solicitado, pero se le recomienda explorar al momento de crear, es libre de diseñar a su manera, pero cuidando la estructura otorgada.

<img src="medio\7.PNG/">
<img src="medio\6.PNG/">

## o Establezca la propiedad visibility a invisible a los TextView del activity_main, estos serán activados en el momento en que la segunda activity le mande un resultado, en primera instancia están ocultos.

<img src="medio\8.PNG/">
<img src="medio\9.PNG/">

## o Establezca el evento onClick al botón del activity_main que tiene el identificador btEnviar, puede usar el siguiente código XML. Puede usar la corrección automática para generar el código correspondiente a este manejador de evento.

<img src="medio\11.PNG/">
<img src="medio\10.PNG/">

## En el caso de que no pueda generar el método a través de las correcciones automáticas, tiene la siguiente estructura.

<img src="medio\12.PNG/">

##  Agregando un Intent al MainActivity.kt

## o Abra el fichero MainActivity.kt

## o Agregue un object companion dentro de la clase MainActivity, no dentro de algún método, este servirá para simular un objeto estático que no cambia el valor de sus propiedades en toda la aplicación. El valor EXTRA_MESSAGE nos servirá para la clave del extra en el intent.

<img src="medio\13.PNG/">

## o Agregue el siguiente código en el método lanzarSegundaActivity, relacionado a la creación de un intent.

<img src="medio\14.PNG/">

### Al momento de crear esta sentencia  en la  parte de arriba se crea un import que es para declarar el Intent y no tener ningún error.

<img src="medio\15.PNG/">

## o Muestre el resultado en el momento en que la segunda activity fue lanzada.

## o Regrese a la activity principal e indique que instancias del ciclo de vida del activity se han ejecutado.

## Tarea 1.3: Compartiendo datos de Activity principal a la segunda.

## o Agregue el siguiente código para enviar datos activities, debe reemplazar el código anterior del método lanzarSegundaActivity. Muetre los resultados.

<img src="medio\16.PNG/">

##  Modificando la segunda activity para obtener los extras.

## o Abra el fichero Segunda.kt para agregar código al método onCreate().

<img src="medio\17.PNG/">

## o Obtenga el intent que activó esta activity.

<img src="medio\18.PNG/">

## o Obtenga la cadena que contiene el mensaje de los extras de Intent usando el valor del objeto creado en la activity principal y obtenerlo usando la clave MainActivity.EXTRA_MESSAGE: 

<img src="medio\19.PNG/">

## o Use findViewById() para obtener la referencia del TextView para el mensaje del layout. 

<img src="medio\20.PNG/">

## o Establezca el texto del TextView con la cadena obtenida del extra del intent.

<img src="medio\21.PNG/">

## o Ejecute la aplicación. Cuando escriba el mensaje en el MainActivity, haga clic en el botón Enviar, se lanza la SegundaActivity y se muestra el mensaje.

## o Muestre resultados a través de capturas de pantalla y comentarios.

## Tarea 1.4 Devolver datos al activity principal.

## Siga los siguientes pasos:

## o Abra el fichero activity_segunda.xml y verifique que dispone de la estructura indicada al principio de estas tareas con sus identificadores correspondientes.

## o Establezca el evento onClick al botón con identificador btRes, si lo hace en el XML lo puede realizar de esta manera:

## o Paso opcional por si no hizo el anterior: Si desea establecer el manejador del evento Clic a través de código Kotlin en el método onCrea().

## o Solamente queda crear el método devolverRespuesta(), el cual puede agregarlo después del cierre de llave del método onCreate()

##  Crear respuesta del intent en la segunda Activity.

## o Abre Segunda.kt por si aún no lo está.

## o Agrega un companion object para obtener una sola instancia de objeto sin necesidad de crear una nueva, esto se debe agregar después de la apertura de la llave de la clase Segunda, al inicio para no generar confusiones.

## o Agregue el código del método devolverRespuesta() creado en la tarea anterior.

