# Project1-Weather Station
 Proyecto de una estación meteorológica realizada para una placa STM32F4. 


## Información del proyecto 
El Proyecto se basa en realizar una estación meteorológico en nuestra placa. Disponemos de los siguientes sensores:
* Temperatura
* Luminosidad
* Sonido
* Viento
* Precipitación

Los tres primeros sensores (temperature, light y sound) medirán los valores para lo que
están diseñados, es decir la temperatura, la luminosidad y el ruido del entorno donde se encuentra
desplegado la estación. Mientras que el sensor touch sustituirá a un sensor de precipitación que
indicará si actualmente llueve, es decir al tocar sobre el touch se simulará que una gota de lluvia ha
sido detectada. Por otro lado, al no disponer de anemómetro se utilizará el angulo rotatorio para
generar una señal que simulará la del propio anemómetro. La señal recibida atenderá al siguiente
comportamiento.

La generación de la señal del viento es proporcionada al estudiante mediante la entrega en campus
virtual de los proyectos PlatformIO y CubeMX, los cuales deberán ser modificados para añadir el
resto de componentes de la estación. Por lo tanto, y de acuerdo a la configuración realizada en
dichos proyectos, el ángulo rotatorio deberá ser conectado en el puerto A0 (pin PA0), que al
establecer un valor en dicho sensor se generará por el pin PA5 una señal con el comportamiento de
la figura anterior.
La estación actualizará sus datos cada cinco segundos, no es necesario una monitorización
continua de los sensores (no se trata de un sistema crítico).

Los valores recogidos se visualizarán por Bluetooth o LCD.
Además, los sensores para viento, temperatura y sonido dispondrán de un panel físico
compuesto por tres pares de LEDs (verde y rojo) y un botón. Cada par de LEDs estará
asociado a un sensor de los citados anteriormente e inicialmente estarán activados en verde. En el
código se establecerá un umbral para cada uno de los sensores (incluidos en la plantilla como
defines), que en el caso de superar dicho umbral cambiará el estado del LED a rojo y permanecerá
en ese estado aunque el sensor capture un valor menor al del umbral. El botón servirá de reset para
establecer el estado inicial (todos los LEDs en verde).

La solución entregada deberá aplicar las técnicas estudiadas durante el curso: máquinas de
estados finitas (FSM), uso de timers, uso de interrupciones, ...

## Datos relevantes
La configuración en STM32CUBEMX junto a los datos relevantes de la práctica se encuentran en el documento en el documento pdf del repositorio.
Entre los datos relevantes podemos encontrar:
 La configuración en STM32CUBEMX junto a los datos relevantes de la práctica se encuentran en el documento en el documento pdf del repositorio.
* Fórmulas: Calcular el valor de la velocidad, luminosidad, temperatura y sonido con los datos que nos proporcionan los sensores.
* Diagrama de estados: Diagrama de estados Mealy para los LEDs que indican si se ha superado el threshold de sonido, temperatura y viento.
* Detalles del código: Métodos importantes del código escrito en .c.
* Escenarios del video: Escenarios necesarios para demostrar el correcto funcionamiento del código.



