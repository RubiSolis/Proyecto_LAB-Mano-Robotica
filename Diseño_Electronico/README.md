Mano Robótica para la Enseñanza de Lengua de Señas

INTEGRANTES: Solis Rubi, Ocampo Abril
DOCENTES A CARGO: Prof. Nano, Prof. Salamero
MATERIA: LAB 1 - DIV "A"
INSTITUCIÓN: Universidad Blas Pascal - Ingeniería en Informática

ÍNDICE

Introducción
Descripción del Circuito
Materiales
Conexiones Detalladas
Conclusión
1. Introducción
En este documento se describe cómo conectar una mano robótica utilizando servos, una placa Arduino Mega y una protoboard. La mano robótica se controla a través de movimientos programados que pueden activarse desde una aplicación móvil desarrollada en App Inventor, y el código se carga en el Arduino Mega.

2. Descripción del Circuito
El circuito consiste en un Arduino Mega conectado a varios servomotores a través de una protoboard. Cada servo está controlado por un pin de la placa Arduino, que envía señales de control para mover cada “dedo” de la mano robótica.

3. Materiales
1 x Arduino Mega
1 x Protoboard
8 x Servomotores (uno para cada dedo y algunos movimientos adicionales)
Cables de conexión
Fuente de alimentación para los servos (si es necesario)
4. Conexiones Detalladas
Arduino Mega

Pines Digitales: Los pines digitales de la placa Arduino Mega se conectan a los pines de señal de los servos. A continuación se describe la conexión de cada pin de Arduino con su respectivo servo:

Pin 2 a la señal del primer servo.
Pin 3 a la señal del segundo servo.
Pin 4 a la señal del tercer servo.
Pin 5 a la señal del cuarto servo.
Pin 6 a la señal del quinto servo.
Pin 7 a la señal del sexto servo.
Pin 8 a la señal del séptimo servo.
Pin 9 a la señal del octavo servo.
Servos

Alimentación y Tierra: Los pines de alimentación (rojos) de todos los servos están conectados entre sí y luego a una fuente de alimentación de 5V en la protoboard. Los pines de tierra (negros) de los servos también están conectados entre sí y se unen al pin GND de la protoboard, que se conecta a la tierra de la placa Arduino Mega.

Protoboard

La protoboard permite distribuir la energía y la conexión a tierra de todos los servos de forma ordenada. Todos los cables de alimentación y tierra de los servos están conectados en filas de la protoboard que están unidas a las fuentes de alimentación y tierra del Arduino Mega.

Módulo Bluetooth HC-05

Conexiones del Módulo Bluetooth HC-05

Alimentación: El módulo HC-05 está conectado a la fuente de 3.3V y 5V de la placa Arduino Mega.
Tierra: El pin de tierra del HC-05 está conectado al GND de la protoboard y del Arduino Mega.
Pines de Comunicación:
Pin 22 del Arduino Mega está conectado al pin de transmisión (TX) del HC-05.
Pin 24 está conectado al pin de recepción (RX) del HC-05.
Pin 26 se utiliza para la configuración o control adicional del módulo.
Estas conexiones permiten que el Arduino Mega reciba y envíe datos al módulo Bluetooth, facilitando la interacción entre el dispositivo controlador (como una app en App Inventor) y la mano robótica.

5. Conclusión
Este esquema de conexión permite controlar una mano robótica con ocho servos, cada uno conectado a un pin digital de la placa Arduino Mega. La protoboard facilita la distribución de la alimentación y tierra para todos los servos. Este diseño es ideal para proyectos de enseñanza de lenguaje de señas, ya que permite programar movimientos específicos de cada "dedo" de la mano robótica desde el Arduino.

