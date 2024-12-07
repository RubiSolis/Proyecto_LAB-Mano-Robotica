

 Diseño 3D Mano Robótica “Ocalis”
 

INTEGRANTES: Solis Rubi y Ocampo Abril

DOCENTES A CARGO: prof. Nano y prof. Salamero

MATERIA: LAB 1 - DIV "A"

INSTITUCION: Universidad Blas Pascal - Ingenieria en informatica


---
1. Introducción
La presente documentación describe el diseño y construcción de un prototipo de mano robótica, diseñado específicamente para realizar movimientos controlados y programados. Este proyecto tiene aplicaciones didácticas y experimentales, permitiendo a los usuarios interactuar con conceptos de robótica y control mecánico. En este informe se detalla la estructura física, los materiales utilizados y las especificaciones técnicas clave para su implementación.

----
2. Descripción General del Diseño
El diseño consta de una mano robótica montada sobre una base giratoria. La estructura está diseñada para optimizar la funcionalidad y facilitar la operación del sistema. La base cuadrada incluye un compartimento para alojar componentes electrónicos esenciales, como el Arduino Mega, una protoboard y el cableado, mientras que la mano está compuesta por diversas piezas modulares que permiten el control independiente de cada dedo mediante hilos tensores.

Base giratoria: Permite rotar la mano robótica en 180° mediante un servomotor SG90, ampliando su rango de operación.
Soporte de servomotores: Una estructura robusta contiene cinco servomotores SG90 encargados de controlar los dedos, asegurada por un soporte trasero que evita desequilibrios.
Sistema de tensores: Hilos de nailon (hilo chino) y tanza de 0.5 mm de cualquier marca se encargan de transmitir los movimientos desde los servomotores hacia los dedos.
Palma y dedos: La parte superior incluye una base con un orificio para guiar los tensores hacia la palma, que conecta los dedos articulados. Cada dedo está diseñado para movimientos individuales, garantizando precisión y flexibilidad.
---

3. Materiales Utilizados
Plástico:
Utilizado en la mayoría de las piezas de la estructura. Puede ser impreso en 3D para asegurar durabilidad y precisión en las dimensiones.
Cartón (en prototipo inicial):
La caja de soporte  del Arduino y protoboard fue construida en cartón como tambien el abductor del dedo pulgar, por simplicidad en el prototipo, pero es adaptable a impresión 3D.
Hilo chino:
Material flexible y resistente, utilizado para el control de los dedos.
Tanza de 0.5 mm:
Sirve como componente clave del sistema de tensores, proporcionando alta resistencia.
Servomotores SG90:
siete servomotores en total: uno para la rotación de la base y cinco para el control de los dedos.
---

4. Componentes Clave
Caja de almacenamiento:
Ubicada en la base, permite alojar el Arduino Mega, la protoboard y los cables, organizando el sistema eléctrico del dispositivo.
Soporte trasero para servomotores:
Proporciona estabilidad a la estructura que contiene los servomotores, evitando caídas o movimientos indeseados.
Sistema de tensores:
Diseñado para conectar los servomotores a las articulaciones de los dedos mediante un recorrido fluido por orificios estratégicamente ubicados.
Palma y dedos articulados:
Diseñados modularmente, permiten realizar movimientos complejos de forma precisa.

---

5. Especificaciones Técnicas**

Base giratoria:
Material: Plástico.
Servomotor: SG90.
Rotación: 360°.
Dimensiones de la caja:
Suficiente para alojar un Arduino Mega y una protoboard estándar.
Sistema de tensores:
Material: Hilo chino y tanza de 0.5 mm.
Energía:
Controlada mediante Arduino Mega, alimentado por una fuente de energía externa o baterías.
Peso soportado:
Optimizado mediante soportes traseros y uso de materiales ligeros.
Las dimensiones de cada componente se detallan a continuación para asegurar su correcta fabricación y ensamblaje:

- **Altura total del brazo**: 30 cm aprox
- **Base giratoria (naranja)**: 8x8 cm, altura de 3 cm
- **Base para servomotores de los dedos**: 6,7x2,5 cm, altura de 8,8 cm
- **Palma**: 6,5x1,4 cm, altura de 8,5 cm
- **Pulgar**: 2,6x1 cm, altura de 2,8 cm
- **Dedos (anular, medio, índice)**: 1,3x1,3 cm, altura de 2,5 cm
- **Meñique**: 1,3x1,3 cm, altura de 2,5 cm
- **Pulgar (dedo adicional)**: 1,3x1,3 cm, altura de 2,5 cm

6. Conclusión
Este prototipo combina diseño funcional y simplicidad en su construcción, asegurando que sea accesible para diversos usos educativos y experimentales. La flexibilidad de los materiales y la modularidad del diseño hacen que este proyecto sea adaptable a diferentes necesidades y mejorable con futuras iteraciones.


