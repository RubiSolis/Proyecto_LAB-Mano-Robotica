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

1. Librerías Incluidas

#include <ESP8266WiFi.h>
#include <Servo.h>

ESP8266WiFi.h: Esta librería permite que el microcontrolador ESP8266 se conecte a una red Wi-Fi y actúe como un servidor.

Servo.h: Esta librería permite controlar servomotores, que son utilizados en la mano robótica para simular los movimientos de los dedos.


2. Configuración de la Red Wi-Fi

const char* ssid = "NOMBRE_RED";         // Nombre de la red Wi-Fi
const char* password = "CONTRASEÑA_RED";  // Contraseña de la red Wi-Fi

Aquí se define el nombre de la red Wi-Fi y su contraseña, que son necesarios para conectar el ESP8266 a la red.


3. Definición de Servos
Servo pulgar, indice, medio, anular, meñique, palma, rotaciona; // Definición de los servos


Memoria actualizada
¡Claro! Vamos a desglosar el código de la mano robótica para que sea más fácil de entender. Este código está diseñado para controlar una mano robótica a través de un servidor Wi-Fi utilizando un módulo ESP8266. A continuación, explicaré cada parte del código y su propósito.

1. Librerías Incluidas
cpp
Copiar código
#include <ESP8266WiFi.h>
#include <Servo.h>
ESP8266WiFi.h: Esta librería permite que el microcontrolador ESP8266 se conecte a una red Wi-Fi y actúe como un servidor.
Servo.h: Esta librería permite controlar servomotores, que son utilizados en la mano robótica para simular los movimientos de los dedos.
2. Configuración de la Red Wi-Fi
cpp
Copiar código
const char* ssid = "NOMBRE_RED";         // Nombre de la red Wi-Fi
const char* password = "CONTRASEÑA_RED";  // Contraseña de la red Wi-Fi
Aquí se define el nombre de la red Wi-Fi y su contraseña, que son necesarios para conectar el ESP8266 a la red.
3. Definición de Servos
cpp
Copiar código
Servo pulgar, indice, medio, anular, meñique, palma, rotaciona; // Definición de los servos
Se crean instancias de la clase Servo para cada parte de la mano robótica (pulgar, índice, medio, anular, meñique, palma y un servo para la rotación).

5. Pines de los Servos
6. 
const int pinPulgar = D1;  // D1 como ejemplo
const int pinIndice = D2;   // D2 como ejemplo
const int pinMedio = D3;    // D3 como ejemplo
const int pinAnular = D4;   // D4 como ejemplo
const int pinMeñique = D5;  // D5 como ejemplo
const int pinPalma = D6;     // D6 como ejemplo
const int pinRotaciona = D7; // D7 como ejemplo

Se asignan pines del microcontrolador a cada servo. Estos pines serán utilizados para controlar la posición de cada servo.

5. Inicialización del Servidor

WiFiServer server(80);

Se crea un objeto server que escuchará en el puerto 80 (puerto HTTP) para recibir solicitudes de clientes a través de la red Wi-Fi.


6. Función setup()

void setup() {
  Serial.begin(115200);
  WiFi.begin(ssid, password);
  ...
}


Serial.begin(115200): Inicia la comunicación serial a una velocidad de 115200 baudios, que se usa para enviar datos al monitor serial.

WiFi.begin(ssid, password): Inicia la conexión a la red Wi-Fi con las credenciales proporcionadas.

Dentro de setup(), también se inicializan los servos y se define la posición inicial de la mano robótica.


7. Bucle Principal loop()

void loop() {
  WiFiClient client = server.available(); // Esperar conexión de cliente
  if (client) {
    String request = client.readStringUntil('\r'); // Leer la solicitud del cliente
    ...
    client.stop(); // Termina la conexión
  }
}

Este bucle está en ejecución continua. Espera a que un cliente se conecte al servidor.

Cuando se recibe una conexión, lee la solicitud del cliente (por ejemplo, "/hola" o "/gato") y llama a la función correspondiente para ejecutar un movimiento específico de la mano.


8. Funciones de Movimiento
Las funciones como raton(), gato(), oso(), etc., son responsables de los movimientos de la mano robótica. Cada función contiene instrucciones para mover los servos a ciertas posiciones.


9. Posición Inicial
    Todos los servos comenzaras desde una posicion indicada

Conclucion: 

Funciones de Movimiento: Cada función está diseñada para realizar un gesto específico, y se puede personalizar según sea necesario.
Este código permite que la mano robótica realice movimientos específicos basados en los comandos que recibe a través de la red Wi-Fi. Si tienes más preguntas sobre una parte específica del código o quieres más detalles, ¡hazmelo saber!



