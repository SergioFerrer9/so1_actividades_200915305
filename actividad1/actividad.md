# TIPOS DE KERNEL Y SUS DIFERENCIAS

## Existen diferentes tipos de kernel para diferentes sistemas operativos y dispositivos finales. Conforme a sus características, pueden dividirse en tres grupos:

1.  Kernel monolítico. Un kernel grande para todas las tareas. Es el único responsable de la gestión de la memoria y de los procesos, de la comunicación entre procesos y proporciona funciones de soporte de drivers y hardware. Los sistemas operativos que usan el kernel monolítico son Linux, OS X y Windows.

2.  Microkernel. El microkernel se ha diseñado intencionadamente de un tamaño pequeño para que en caso de fallo no paralice todo el sistema operativo. No obstante, para que pueda asumir las mismas funciones que un kernel grande, está dividido en varios módulos. Como ejemplo de aplicación solo existe el componente Mach de OS X, ya que hasta ahora no hay ningún sistema operativo con microkernel.

3.  Kernel híbrido. La combinación del kernel monolítico y el microkernel se denomina kernel híbrido. En este caso, el kernel grande se hace más compacto y modulable. Otras partes del kernel pueden cargarse dinámicamente. Esto ya ocurre en cierta medida en Linux y OS X.

# USER MODE vs KERNER MODE

## El procesador cambia entre los dos modos según el tipo de código que se esté ejecutando en el procesador. Las aplicaciones se ejecutan en modo usuario y los componentes principales del sistema operativo se ejecutan en modo kernel. Si bien muchos controladores se ejecutan en modo kernel, algunos controladores pueden ejecutarse en modo de usuario.

## USER MODE

Cuando una aplicación informática se está ejecutando, está en el modo de usuario. Algunos ejemplos son la aplicación de Word, PowerPoint, leer un archivo PDF y navegar por Internet. Estos son programas de aplicación por lo que la computadora está en modo usuario. Cuando el proceso está en modo de usuario y requiere algún recurso de hardware, esa solicitud se envía al kernel. Como hay un acceso limitado al hardware en este modo, se le conoce como modo menos privilegiado, modo esclavo o modo restringido .

En modo usuario, los procesos obtienen su propio espacio de direcciones y no pueden acceder al espacio de direcciones que pertenece al núcleo. Entonces, la falla de un proceso no afectará el sistema operativo. Si hay una interrupción, solo afecta a ese proceso en particular.

## KERNERL MODE

Cuando el proceso se ejecuta en modo de usuario y si ese proceso requiere recursos de hardware como RAM , impresora, etc., ese proceso debe enviar una solicitud al kernel. Estas solicitudes se envían a través de llamadas al sistema. Luego, la computadora ingresa al Modo Kernel desde el modo de usuario. Cuando se completa la tarea, el modo vuelve a cambiar al modo de usuario desde el modo kernel. Esta transición se conoce como “ cambio de contexto ”. El modo kernel también se denomina modo de sistema o modo privilegiado . No es posible ejecutar todos los procesos en el modo kernel porque si un proceso falla, todo el sistema operativo puede fallar.

[**DIAGRAMA**](./kernel.png)

[**REFERENCIA**](https://www.differencebetween.com/difference-between-user-mode-and-vs-kernel-mode/)