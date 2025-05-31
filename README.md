Materiales de ingeniería
====

Este repositorio contiene materiales de ingeniería de un modelo de vehículo autónomo que participa en la competición WRO Future Engineers en la temporada 2025.

Este repositorio trata de ser una versión fiel, traducida al español de la plantilla generada por la [World Robot Olympiad](https://github.com/World-Robot-Olympiad-Association/wro2022-fe-template/), tenga en cuenta que para la competencia internacional el texto debe estar en ingles.

<b>Recuerde que el repositorio debe ser público y siempre accesible.</b>

## Contenido

* `t-photos` contiene 2 fotos del equipo (una oficial y una foto divertida con todos los miembros del equipo)
* `v-photos` contiene 6 fotos del vehículo (de cada lado, de arriba a abajo)
* `video` contiene el archivo video.md con el enlace a un vídeo en el que existe una demostración de conducción
* `schemes` contiene uno o varios diagramas esquemáticos en formato JPEG, PNG o PDF de los componentes electromecánicos que ilustran todos los elementos (componentes electrónicos y motores) utilizados en el vehículo y cómo se conectan entre sí.
* `src` contiene el código del software de control de todos los componentes que se programaron para participar en la competición
* `models` es para los archivos de los modelos utilizados por impresoras 3D, máquinas de corte por láser y máquinas CNC para producir los elementos del vehículo. Si no hay nada que agregar a esta ubicación, se puede eliminar el directorio.
* `other` es para otros archivos que se pueden usar para entender cómo preparar el vehículo para la competencia. Puede incluir documentación sobre cómo conectarse a un SBC/SBM y cargar archivos allí, conjuntos de datos, especificaciones de hardware, descripciones de protocolos de comunicación, etc. Si no hay nada que agregar a esta ubicación, se puede eliminar el directorio.

## Introducción
Módulos del código y relación de componentes electromecánicos
El código del robot está compuesto por varios módulos principales en MakeCode, que incluyen:

Bloques Basic: utilizados para funciones básicas de control y estructura del programa.
Extensión NezhaV2: permite mover los motores y el servo de manera sencilla, controlando la velocidad del motor y la posición del servo en grados.
Variables: usadas para almacenar datos importantes como la cantidad de vueltas o la posición actual.
Lógica: para decidir cuándo girar, mover o detener el robot, y controlar la repetición de los movimientos.
Relación de componentes electromecánicos:
Placa Nezha V2: actúa como la interfaz entre la programación y los componentes físicos, permitiendo controlar el motor y el servo.
Motor de las ruedas traseras: conectado a la placa Nezha V2 en el puerto M2, motiva al robot para avanzar o retroceder y realizar las vueltas.
Servo de las ruedas delanteras: conectado a la placa en el puerto M3, controla la dirección del robot (direccional), girando a 45 grados en las esquinas de la pista.
Micro:bit: actúa como el cerebro del robot, ejecutando el programa de MakeCode y enviando las órdenes a la placa Nezha V2.
Proceso para construir, compilar y cargar el código:
Construcción: se ensamblan las piezas y componentes en la estructura del robot, conectando el motor trasero y el servo a la placa Nezha V2 en los puertos M2 y M3, respectivamente, y asegurando que la placa esté correctamente fijada al robot.
Programación: se ingresa el código en el entorno MakeCode, usando bloques para mover los motores y el servo, con las instrucciones para completar 3 vueltas en la pista cuadrada.
Compilación y carga: desde MakeCode, se compila el programa y se descarga como un archivo .hex, que luego se transfiere a la micro:bit conectándola a la computadora mediante un cable USB y copiando el archivo a la carpeta de la micro:bit. La micro:bit, con su programación cargada, luego controla el robot.
