# Índice
* [¿Qué es la POA?](#que-es-la-poa)
* [POA y POO](#poa-y-poo)
* [Conceptos clave](#conceptos-clave)
* [Ventajas y desventajas](#ventajas-y-desventajas)
* [Aplicaciones y lenguajes](#aplicaciones-y-lenguajes)
  * [Aplicaciones](#aplicaciones)
  * [Lenguajes](#lenguajes)

# Programación Orientada a Aspectos (POA)

## ¿Qué es la POA?

La Programación Orientada a Aspectos (POA) es una metodología de programación que permite separar las funcionalidades transversales del código en módulos independientes llamados aspectos. Esto hace que el código sea más modular, reutilizable y fácil de mantener. Por funcionalidades transversales nos referimos a aquellas que se repite en varias partes de un programa, independientemente de si las secciones en las que aparece tienen relación directa.

La evolución de los sistemas de software ha seguido un camino desde el código espagueti hasta la programación orientada a objetos (POO). El código espagueti era difícil de leer y mantener debido a la falta de estructura. La POO introdujo la idea de encapsular datos y funcionalidades en objetos, lo que hizo que el código fuera más modular y reutilizable. Sin embargo, la POO no aborda bien los aspectos transversales, como la sincronización, la distribución y el manejo de errores.

>  📌 **Ejemplo:** Imagina que estás desarrollando un sistema de registro de usuarios. La validación de datos (por ejemplo, verificar que un correo electrónico sea válido) es una tarea que se repite en múltiples partes del sistema (registro, recuperación de contraseña, etc.). En lugar de repetir este código en cada lugar, la POA te permite crear un "aspecto" de validación y aplicarlo a los puntos del código donde sea necesario.

   ![WhatsApp Image 2024-11-10 at 5 23 50 PM](https://github.com/user-attachments/assets/7b0111b7-74b3-47a0-9899-7fbd3ace740a)


## POA y POO

A primera vista daría la impresión que la POA y la POO son en realidad el mismo paradigma. Sin embargo, esta primera impresión es errónea. Un análisis más profundo revela las diferencias entre los paradigmas:


> 📝 **Nota:** La Programación Orientada a Aspectos basa su filosofía en tratar las obligaciones transversales de los programas como módulos separados.


- Tanto la POA como la POO crean implementaciones modularizadas y con mínimo acoplamiento. 
- La diferencia radica en que mientras la POA se enfoca en los conceptos que se entrecruzan, la POO se enfoca en los conceptos comunes y los ubica en un árbol de herencia.

  ![image](https://github.com/user-attachments/assets/097eb323-9bdb-4f1d-8a74-1b2963ae0c44)

En POA la implementación de los conceptos son independientes. Esta independencia la distingue de las técnicas inherentes a la POO. En POA, el flujo de composición va desde los conceptos que se entrecruzan al concepto principal; mientras que en la POO el flujo va en dirección opuesta.

La POO organiza el código en torno a objetos con atributos y métodos, mientras que la POA se enfoca en modularizar las funcionalidades transversales que afectan a múltiples objetos. La POO es ideal para modelar el mundo real en términos de objetos, mientras que la POA es excelente para manejar aspectos que cortan las fronteras de los objetos, como la gestión de transacciones o la seguridad. En resumen, la POO se ocupa de la estructura estática del sistema, mientras que la POA se enfoca en la dinámica y los aspectos transversales.

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

POA trata de solucionar los extremos más comunes en la programación: 

- Código mezclado: tener todo en un mismo módulo, que puedan simultáneamente convivir más de un requerimiento. Lo que dificulta la comprensión, el mantenimiento y la reutilización del código. 

- Código diseminado: se refiere a como los requerimientos están esparcidos sobre varios módulos, lo que resulta en una implementación fragmentada y difícil de mantener. 

Las ventajas sobre este paradigma es que se busca un punto de equilibrio en estos extremos, que se pueda sacar provecho, lo que permite: 

1. Mayor reusabilidad 

2. Legibilidad 

3. Mínimo acoplamiento y máxima cohesión (independientes pero buen trabajo en equipo). 

4. intensidad el principio de dividir y conquistar. 

5. implementaciones modularizadas. 

Así también existen desventajas al tratar de unir o implementar una manera de separar los componentes y los aspectos, pero que todo siga comunicado y trabajando en equipo, lo que genera: 

1. Posibles choques entre el código funcional y el código de aspectos. 

2. Posibles choques entre los aspectos (trabajan bien independientemente, pero no en equipo). 

3. Fragilidad. 

4. Incremento de carga computacional. 

5. Documentación: Al tratarse de un paradigma relativamente nuevo comparado con otros, esto causa que la documentación e implementaciones del mismo no tengan documentaciones robustas como, por ejemplo, la programación orientada a objetos. Esto puede suponer un problema para desarrolladores con poca experiencia o para proyectos de gran envergadura que deban depender en gran medida de este paradigma. 

# Aplicaciones y lenguajes

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


