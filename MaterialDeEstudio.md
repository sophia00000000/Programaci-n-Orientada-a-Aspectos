# Índice
* [¿Qué es la POA?](#que-es-la-poa)
* [POA y POO](#poa-y-poo)
* [Conceptos clave](#conceptos-clave)
* [Ventajas y desventajas](#ventajas-y-desventajas)
  * [Ventajas](#ventajas)
  * [Desventajas](#desventajas)
* [Aplicaciones y lenguajes](#aplicaciones-y-lenguajes)
  * [Aplicaciones](#aplicaciones)
  * [Lenguajes](#lenguajes)
* [Ejemplos](#ejemplos)

# Programación Orientada a Aspectos (POA)

## ¿Qué es la POA?

La Programación Orientada a Aspectos (POA) permite manejar funcionalidades transversales, como seguridad o sincronización, que atraviesan múltiples módulos de un programa. Por funcionalidades transversales nos referimos a aquellas que se repite en varias partes de un programa, independientemente de si las secciones en las que aparece tienen relación directa.

A diferencia de la Programación Orientada a Objetos (POO), donde se encapsulan datos y comportamientos en clases, el POA organiza "aspectos" que no se encajan bien en la estructura de objetos. Esta evolución aborda problemas de modularidad y mantenimiento, ofreciendo una estructura más compacta y especializada para la separación de preocupaciones en el desarrollo de software.

## POA y POO

A primera vista daría la impresión que la POA y la POO son en realidad el mismo paradigma. Sin embargo, esta primera impresión es errónea. Un análisis más profundo revela las diferencias entre los paradigmas:

> 📝 **Nota:** La Programación Orientada a Aspectos basa su filosofía en tratar las obligaciones transversales de los programas como módulos separados.

- Tanto la POA como la POO crean implementaciones modularizadas y con mínimo acoplamiento. 
- La diferencia radica en que mientras la POA se enfoca en los conceptos que se entrecruzan, la POO se enfoca en los conceptos comunes y los ubica en un árbol de herencia.

  ![image](https://github.com/user-attachments/assets/097eb323-9bdb-4f1d-8a74-1b2963ae0c44)

En POA la implementación de los conceptos son independientes. Esta independencia la distingue de las técnicas inherentes a la POO. En POA, el flujo de composición va desde los conceptos que se entrecruzan al concepto principal; mientras que en la POO el flujo va en dirección opuesta.

# Conceptos clave

## Aspecto (Aspect): 
Funcionalidad trasversal de la aplicación, ejemplo más común es el logging ya que afecta a todas las partes de la aplicación que genera un suceso. 

## Punto de enlace (joint point)
Punto de programa donde un aspecto puede ser conectado. ya sea: 
- Llamada a un método 
- Lanzamiento de una excepción 
- Modificación de un campo. 

## Consejo (advise): 
Es la implementación del aspecto, es decir, contiene el código que implementa la nueva funcionalidad. Se insertan en la aplicación en los joint points. 

## Punto de corte (point cut):
Es una expresión que define que advice se usa en cada joint point, para seleccionar los puntos de unión concretos donde se desea ejecutar un asesoramiento (advice). 

Los joinpoints son los lugares donde puede ocurrir algo, mientras que los pointcuts son las reglas que determinan dónde ocurrirá algo. 

## Introducción:
Permite añadir métodos o atributos a clases ya existentes.

## Destinatario (Target):
Clase sobre la que se aplica un aspecto, el consejo  

## Resultante (Proxy): 
Objeto resultante de aplicar los advice a un objeto.  

## Tejedor (Weaver):
Tiene un papel similar al del compilador en otros paradigmas, se encarga de mezclar los diferentes componentes con los aspectos, ayudándose de las reglas de recomposición que proporcionan los puntos de enlace.  

El resultado de este proceso de tejido es un código ejecutable de todo el sistema.



## Ventajas y desventajas

### Ventajas

### Desventajas

# Aplicaciones y lenguajes
## LOA 
Los Lenguajes Orientados a Aspectos son herramientas que permiten separar la lógica principal de una aplicación de las "preocupaciones transversales" como el logging, la seguridad o la gestión de transacciones. Esto se logra mediante la definición de aspectos, módulos que encapsulan esta lógica adicional y se "tejen" en el código principal en puntos específicos llamados joinpoints. 
- AspectJ
- Spring AOP
- Cool

Aplicaciones: 

- Manejo de Transacciones: Garantiza la integridad de los datos, separa la lógica de negocio de la gestión de transacciones. 

- Sincronización: Coordina la ejecución de hilos y procesos, evita condiciones de carrera y acceso no autorizado a recursos. 

- Control de Acceso y Seguridad: encapsulación para la centralización y gestión de permisos. 

- Logging: Centralización del registro, facilita la depuración y el análisis de la aplicación, flexibilidad para personalizar los mensajes de registro según necesidades. 

- Manejo de Excepciones: Unificación de la gestión de excepciones, mejora la robustez.

- Monitoreo del Rendimiento y Testing


### Aplicaciones

### Lenguajes

## Ejemplos

