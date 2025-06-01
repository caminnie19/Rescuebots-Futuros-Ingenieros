
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
