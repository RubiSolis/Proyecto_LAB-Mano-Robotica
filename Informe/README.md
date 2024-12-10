# Mano Robótica para Enseñar Lenguaje de Señas

Un proyecto interactivo diseñado para enseñar lenguaje de señas utilizando una mano robótica controlada mediante una aplicación móvil.

## Descripción

Este proyecto combina hardware y software para facilitar el aprendizaje del lenguaje de señas. La aplicación móvil permite a los usuarios seleccionar señas y realizar pruebas para evaluar su conocimiento. La mano robótica imita cada seña seleccionada, haciendo que el aprendizaje sea visual e interactivo.

## Características principales

- **Modo de aprendizaje**: Aprende señas seleccionando niveles organizados.
- **Pruebas interactivas**: Evalúa tus conocimientos con un examen que proporciona retroalimentación inmediata.
- **Control por Bluetooth**: La aplicación se conecta a la mano robótica mediante Bluetooth para realizar las señas en tiempo real.
- **Estadísticas de desempeño**: Muestra resultados al finalizar el examen (porcentaje correcto, incorrecto y tiempo total).

## Instalación

### Requisitos previos

1. Arduino IDE para cargar el código en la mano robótica.
2. Android Studio (o similar) para compilar la aplicación móvil.
3. Hardware:
   - Arduino (compatible con Bluetooth).
   - Servomotores para la mano robótica.
   - Sensor Bluetooth HC-05 o similar.
   - Componentes básicos como resistencias y cables.

### Pasos de instalación

1. **Configuración del hardware**:
   - Ensambla la mano robótica con servomotores y conéctala al Arduino.
   - Conecta el módulo Bluetooth al Arduino.

2. **Carga del código Arduino**:
   - Abre el archivo `hand_control.ino` en Arduino IDE.
   - Configura el puerto y placa adecuados y sube el código.

3. **Instalación de la aplicación móvil**:
   - Abre el proyecto en Android Studio.
   - Compila y despliega la app en tu dispositivo.

4. **Conexión Bluetooth**:
   - Asegúrate de emparejar el dispositivo móvil con el módulo Bluetooth.

## Uso

1. **Inicio**:
   - Abre la aplicación y selecciona "Comenzar".
2. **Modo de aprendizaje**:
   - Selecciona la opcion "Niveles" y veras las diferentas señas para aprender.
3. **Modo de prueba**:
   - Completa las 12 preguntas del examen y revisa tus estadísticas al final.
4. **Conexión con la mano robótica**:
   - La app enviará las instrucciones a la mano mediante Bluetooth.


