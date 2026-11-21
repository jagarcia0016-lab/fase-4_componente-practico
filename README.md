SOFTWARE FJ

Sistema integral de gestión de clientes, servicios y reservas

1. Descripción general

Software FJ es una aplicación desarrollada en Python mediante el paradigma de programación orientada a objetos (POO), cuyo propósito es gestionar los clientes, servicios y reservas de una empresa dedicada a ofrecer alquiler de salas, alquiler de equipos y asesorías especializadas.

El sistema está diseñado para funcionar sin utilizar bases de datos. La información se administra mediante objetos, clases y listas internas durante la ejecución del programa. Adicionalmente, incorpora un sistema de registro de eventos y errores mediante archivos de logs, permitiendo realizar un seguimiento de las operaciones y detectar posibles inconvenientes.

2. Objetivo del programa

Desarrollar un sistema modular, organizado y extensible que permita administrar clientes, servicios y reservas, aplicando los principios fundamentales de la programación orientada a objetos y mecanismos avanzados de manejo de excepciones para garantizar la continuidad de la aplicación ante situaciones inesperadas.

3. Estructura y componentes del sistema

El programa está organizado mediante las siguientes clases:

Entidad: clase abstracta que establece una estructura general para las entidades del sistema, incluyendo identificadores y nombres.

Cliente: permite registrar clientes mediante sus datos personales, implementando encapsulación y validaciones para el correo electrónico y el número telefónico.

Servicio: clase abstracta que establece las características generales de los servicios, incluyendo tarifas, disponibilidad y métodos para calcular costos.

ReservaSala: administra el servicio de alquiler de salas, considerando la tarifa por hora y la capacidad de personas.

AlquilerEquipo: gestiona el alquiler de equipos, teniendo en cuenta las tarifas por día y las unidades disponibles.

AsesoriaEspecializada: representa los servicios de asesoría profesional, permitiendo establecer una especialidad y calcular sus costos según la duración.

Reserva: relaciona un cliente con un servicio y administra la duración, el costo y el estado de cada reserva. Permite realizar operaciones de confirmación, cancelación y procesamiento.

SistemaSoftwareFJ: funciona como administrador general de la aplicación, gestionando las listas internas de clientes, servicios y reservas.

4. Principios de programación orientada a objetos implementados

El desarrollo aplica los siguientes conceptos:

Abstracción: mediante las clases abstractas Entidad y Servicio.

Herencia: las clases especializadas heredan las características de Servicio.

Polimorfismo: los diferentes servicios implementan sus propios métodos de descripción y cálculo.

Encapsulación: los atributos internos se protegen mediante propiedades y atributos privados.

Sobrecarga simulada: el método calcular_costo permite recibir diferentes combinaciones de parámetros para aplicar impuestos y descuentos.

5. Manejo de excepciones y registro de errores

El programa incorpora excepciones personalizadas para controlar situaciones como datos inválidos, clientes inexistentes, servicios no disponibles, reservas incorrectas y operaciones no permitidas.

También utiliza estructuras try/except, try/except/else y try/except/finally, además del encadenamiento de excepciones mediante la instrucción raise from.

Los eventos relevantes y los errores detectados se almacenan en el archivo software_fj.log, facilitando el seguimiento de las operaciones realizadas.

Una característica importante es que cada operación de prueba se ejecuta de manera independiente, de modo que los errores controlados no interrumpan el funcionamiento general del sistema.

6. Pruebas y demostración del funcionamiento

El programa ejecuta automáticamente 12 operaciones de demostración que incluyen:

Registro correcto de un cliente llamado Johan.

Intento de registro con correo electrónico inválido.

Intento de registro con teléfono incorrecto.

Creación y registro de tres servicios especializados.

Intento de creación de un servicio con tarifa negativa.

Creación, confirmación y procesamiento de una reserva exitosa.

Intento de reserva con un cliente inexistente.

Intento de reservar un servicio no disponible.

Intento de crear una reserva con duración inválida.

Creación y cancelación de una reserva.

Intento de procesar una reserva sin confirmación.

Comprobación de las diferentes variantes del cálculo de costos.

Al finalizar, el sistema presenta un informe estadístico que muestra las operaciones realizadas, las exitosas, los errores controlados, las reservas creadas, sus estados y la disponibilidad de los servicios.

7. Requisitos de ejecución

Tener instalado Python 3.10 o una versión superior.

Contar con un editor o entorno de desarrollo como IDLE, Visual Studio Code o PyCharm.

No requiere instalación de motores de bases de datos ni bibliotecas externas.

Para ejecutar el programa, se debe abrir el archivo software_fj_completo.py desde el entorno de desarrollo o utilizar el siguiente comando:

python software_fj_completo.py

8. Almacenamiento de información

El sistema utiliza listas y objetos para administrar temporalmente la información durante la ejecución. No implementa bases de datos ni almacenamiento permanente de clientes, servicios o reservas.

El único archivo generado automáticamente es software_fj.log, destinado al registro de eventos, operaciones y errores.

9. Conclusión

El proyecto Software FJ demuestra la aplicación práctica de los fundamentos de la programación orientada a objetos mediante el desarrollo de un sistema de gestión modular y funcional. Asimismo, evidencia la importancia del manejo avanzado de excepciones para controlar errores, mantener la estabilidad de una aplicación y garantizar que las operaciones puedan continuar ejecutándose de manera organizada.

La solución constituye una base extensible que permite incorporar nuevas categorías de servicios, funcionalidades y mecanismos de gestión en futuras versiones.
