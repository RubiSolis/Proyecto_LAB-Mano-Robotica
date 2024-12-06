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










Conclucion: 

Funciones de Movimiento: Cada función está diseñada para realizar un gesto específico, y se puede personalizar según sea necesario.
Este código permite que la mano robótica realice movimientos específicos basados en los comandos que recibe a través de la red Wi-Fi. Si tienes más preguntas sobre una parte específica del código o quieres más detalles, ¡hazmelo saber!



