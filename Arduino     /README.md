Mano Robótica para la Enseñanza de Lengua de Señas

INTEGRANTES: Solis Rubi Ocampo Abril

DOCENTES A CARGO prof Nano prof Salamero

MATERIA: LAB 1 - DIV "A"

INSTITUCION: Universidad Blas Pascal - Ingenieria en informatica

INDICE -Introduccion -Cambios -Materiales -problemas -soluciones -Conclusion

INTRODUCCION: Analizaremos el codigo de la mano robotica para entender un poco mas a profundidad como hace los movimientos para recrear las señas establecidas en el app inventor, alojamiento de el codigo en el arduino
Alcances: Entender como se crean a traves de distintos bloques de codigo y librerias los movimientos de la mano Ocalis y ademas explicar como alojar el codigo en el arduino Mega para que almacene en su memoria el cosigo 

DESCRIPCION DE ARDUINO 

Codificacion: Esta creado por el lenguaje C++ que es compatible con la plataforma ARDUINO para compilar y almacenar el codigo fuente

Elementos fisicos: 
Netbook o omputadora 
Cable USB 
Arduino Mega

Plataforma de codigo abierto: 
Arduino es una plataforma de código abierto que combina hardware y software fácil de manejar para construir proyectos electrónicos, este vamos a utlizar 

PASOS PARA CONECTAR ARDUINO MEGA DESDE LA PLATAFORMA Arduino

1-Instala el Software de Arduino
Descarga e instala el IDE de Arduino desde la página oficial (https://www.arduino.cc/).

2-Conecta el Arduino Mega al computador
Usa un cable USB tipo A-B (como el de una impresora) para conectar el Arduino Mega al puerto USB de tu computadora.

3-Selecciona la Placa
Abre el IDE de Arduino. Ve al menú Herramientas > Placa > Arduino Mega o Mega 2560 y selecciona tu modelo.

4-Selecciona el Puerto
En el mismo menú de Herramientas, ve a Puerto y selecciona el puerto COM correspondiente al Arduino Mega (generalmente, el que aparece después de la conexión).

5-Copia y Pega el Código
Copia el código que te proporcionaré y pégalo en el editor del IDE de Arduino, reemplazando cualquier contenido que esté en la ventana.

6-Compila el Código
Haz clic en el ícono de “Verificar” (✓) para asegurarte de que el código no tenga errores.

7-Carga el Código
Una vez compilado, haz clic en el botón de “Subir” (→) para cargar el código en tu Arduino Mega. La plataforma mostrará “Subido” cuando el proceso haya terminado exitosamente.

8-Verifica la Conexión
Si el código incluye una función de prueba, verifica que el Arduino Mega ejecute el programa tal como se planeó.

IMPORTANTE:
El codigo proporcionado esta en esta carpeta en un archivo llamado codigo++


Explicacion de codigo: 

1. Librería Incluida
#include <Servo.h>
Servo.h: Esta librería permite controlar servomotores, que son utilizados en la mano robótica para simular los movimientos de los dedos.

2. Definición de Servos
Servo pulgar, indice, medio, anular, meñique, abductor, rotacion1; // Definición de los servos

Memoria actualizada
¡Claro! Vamos a desglosar el código de la mano robótica para que sea más fácil de entender. Este código está diseñado para controlar una mano robótica a través de un modulo bluetooth HC-05 

1.1. Declaración de los servos:
El código comienza incluyendo la librería Servo.h, que se usa para controlar servomotores en Arduino. Luego, se declaran los servos que controlan las articulaciones de los dedos y las partes de la muñeca:

Servos de los dedos: Pulgar, índice, medio, anular, meñique.
Servo de abducción: Para mover el pulgar hacia fuera o hacia dentro.
Servos de rotación Para permitir la rotación 

Servo pulgar, indice, medio, anular, menique, abductor, rotacion1;

1.2. Configuración inicial (función setup()):
En el setup(), se configura la comunicación serial tanto con el monitor de Arduino como con el módulo Bluetooth HC-05 para recibir comandos.

Se inicializan los pines donde están conectados los servos.
Los servos se colocan inicialmente en posiciones predeterminadas, asegurándose de que estén en un estado conocido antes de que comience la ejecución.

Serial.begin(9600);    // Inicia la comunicación con el monitor serial.
Serial1.begin(9600);   // Inicia la comunicación con el módulo Bluetooth HC-05.

// Asignación de pines a los servos.
pulgar.attach(9); 
indice.attach(2);  
medio.attach(3);   
anular.attach(4); 
menique.attach(5);  
abductor.attach(7);
rotacion1.attach(8);  // Asigna el pin 8 para el servo de rotación.

// Posiciones iniciales de los servos.
pulgar.write(0);
indice.write(0);
medio.write(0);
anular.write(0);
menique.write(0);
rotacion1.write(180); // Rotación inicial.
abductor.write(90);   // Posición inicial del abductor.

1.3. Lectura de comandos desde el Bluetooth (función loop()):
En el loop(), el Arduino escucha constantemente los comandos enviados desde el dispositivo móvil (a través del módulo Bluetooth). Cuando recibe un comando (por ejemplo, '1', '2', etc.), ejecuta un bloque de código específico asociado a ese comando.

Los comandos se leen usando Serial1.read(), que obtiene los datos enviados por el Bluetooth.


 if (Serial1.available()) {
    valor = Serial1.read();  // Lee el comando recibido
    Serial.print("Comando recibido: ");
    Serial.println(valor);
}


1.4. Acciones específicas para cada comando:
Cada comando (como '1', '2', '3', etc.) mueve los servos de la mano robótica de una manera particular. Por ejemplo:

Comando '1': Realiza un movimiento de rotación del pulgar y lo mueve hacia afuera y hacia adentro.
Comando '2': Mueve todos los dedos hacia adelante y luego los regresa.
Comando '3': Realiza un movimiento de rotación y luego mueve los dedos de la mano robótica.
Comando '5': Mueve el pulgar y el meñique juntos hacia fuera y hacia adentro.
Cada comando puede tener un conjunto de movimientos complejos de los servos, realizados mediante bucles for que modifican la posición de los servos en pasos pequeños (con el uso de write()), con un delay() entre cada paso para controlar la velocidad del movimiento.

1.5. Retardos y sincronización:
Cada movimiento de servo está acompañado de un delay() para controlar la velocidad con la que se mueven. Esto asegura que los movimientos sean suaves y no ocurran demasiado rápido.

1.6. Finalización:
Cada comando se ejecuta en su propio bloque condicional if o else if, lo que permite que diferentes patrones de movimiento sean activados dependiendo del comando recibido desde el dispositivo móvil.

Conclucion: 

Funciones de Movimiento: Cada función está diseñada para realizar un gesto específico, y se puede personalizar según sea necesario.
Este código permite que la mano robótica realice movimientos específicos basados en los comandos que recibe a traves de la comunicacion entre el arduino mega y el modulo bluetooth HC-05. Si tienes más preguntas sobre una parte específica del código o quieres más detalles, ¡hazmelo saber!



