Mano Robótica para la Enseñanza de Lengua de Señas

INTEGRANTES: Solis Rubi, Ocampo Abril
DOCENTES A CARGO: Prof. Nano, Prof. Salamero
MATERIA: LAB 1 - DIV "A"
INSTITUCIÓN: Universidad Blas Pascal - Ingeniería en Informática

ÍNDICE
1.Introducción
2.Descripción del Circuito
3.Materiales
4.Conexiones Detalladas
5.conclusion

1. Introducción
En este documento se describe cómo conectar una mano robótica utilizando servos, una placa Arduino Mega y una protoboard. La mano robótica se controla a través de movimientos programados que pueden activarse desde una aplicación móvil desarrollada en App Inventor, y el código se carga en el Arduino Mega.

2. Descripción del Circuito
El sistema consta de un Arduino Mega que controla 6 servomotores SG90. Cada servomotor está conectado a un pin digital de la placa Arduino, mientras que la energía y la tierra se distribuyen a través de una protoboard. Adicionalmente, un módulo Bluetooth HC-05 permite la comunicación inalámbrica entre el Arduino y la aplicación móvil.

3. Materiales
1 x Arduino Mega
1 x Protoboard
6 x Servomotores SG90 (uno para cada dedo y un movimiento adicional para la rotación de la muñeca)
Cables de conexión
Módulo Bluetooth HC-05
Fuente de alimentación externa para los servos (opcional)

4. Conexiones Detalladas
Arduino Mega: Pines Digitales
Pin 2: Servo del dedo índice
Pin 3: Servo del dedo medio
Pin 4: Servo del dedo anular
Pin 5: Servo del dedo meñique
Pin 7: Servo abductor (movimiento lateral del pulgar)
Pin 8: Servo para la rotación de la muñeca
Pin 9: Servo del dedo pulgar

Protoboard
Filas de energía (rojo): Conectadas a una fuente de 5V del Arduino Mega.
Filas de tierra (negro): Conectadas al GND del Arduino Mega.
6. Conexiones Detalladas
Arduino Mega

Módulo Bluetooth HC-05
Pin VCC: Conectado a el protoboard.
Pin GND: Conectado a GND de la protoboard.
Pin TX (Transmisión): Conectado al Pin 19 (RX1) del Arduino Mega.
Pin RX (Recepción): Conectado al Pin 18 (TX1) del Arduino Mega (con divisor de voltaje si necesario).
Pines Digitales: Los pines digitales de la placa Arduino Mega se conectan a los pines de señal de los servos. A continuación se describe la conexión de cada pin de Arduino con su respectivo servo:

5. Conclusión
Este diseño permite controlar una mano robótica equipada con seis servos utilizando un Arduino Mega y un módulo Bluetooth. La distribución de energía mediante la protoboard hace que las conexiones sean más organizadas y eficientes. Gracias a su capacidad de realizar movimientos precisos y programados, este proyecto es ideal para la enseñanza de lengua de señas. Además, su integración con una aplicación móvil ofrece una experiencia de usuario intuitiva y práctica.

