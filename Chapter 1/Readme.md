# [Embedded Linux](https://github.com/FMFigueroa/Embedded-Linux-Kernel)

## Chapter 1 - Introducción a Linux Kernel

### Historia de Linux

Este capítulo presenta el kernel de Linux y el sistema operativo Linux, antes de entender Linux, primero debemos conocer sus origenes, primero hablemos del sistema operativo llamado Unix.
Unix fue creado por primera vez hace más de 40 años.

Linux es un miembro de la familia de sistemas operativos UNIX. En términos de computación, UNIX tiene una larga historia. La primera parte de este capítulo proporciona un breve resumen de esa historia comenzamos con una descripción de los orígenes del sistema UNIX y el lenguaje de programación C, y luego considere las dos corrientes clave que llevaron a el Sistema Linux tal como existe hoy: el proyecto GNU y el desarrollo de Linux núcleo.

Una de las características notables del sistema UNIX es que su desarrollo no fue controlado por un solo proveedor u organización. Más bien, muchos grupos, tanto comerciales como no comerciales, contribuyeron a su evolución. Esta historia dio lugar a muchos características innovadoras que se agregaron a UNIX, pero también tuvo la consecuencia negativa que las implementaciones de UNIX divergieron con el tiempo, por lo que escribir aplicaciones que trabajen en todas las implementaciones de UNIX se hizo cada vez más difícil. Esto condujo a una impulso para la estandarización de las implementaciones de UNIX.

### Una breve historia de UNIX y C

La primera implementación de UNIX se desarrolló en 1969 (el mismo año que Linus nació Torvalds) por Ken Thompson en Bell Laboratories, una división de la corporación telefónica AT&T. Fue escrito en ensamblador para una mini computadora Digital PDP-7. El nombre UNIX es un juego de palabras con MULTICS (Multiplexed Information and servicio informático), el nombre de un proyecto de sistema operativo anterior en el que AT&T colaboró ​​con el Instituto Tecnológico de Massachusetts (MIT) y General Electric. (AT&T ya se había retirado del proyecto frustrado por su inicial fracaso en el desarrollo de un sistema económicamente útil.) Thompson extrajo varias ideas para su nuevo sistema operativo de MULTICS, que incluye un sistema de archivos con estructura de árbol, un programa separado para interpretar comandos (el shell) y la noción de archivos como flujos de bytes no estructurados.

En 1970, UNIX fue reescrito en lenguaje ensamblador para un Digital recién adquirido Minicomputadora PDP-11, luego una máquina nueva y poderosa. Vestigios de este PDP-11 El patrimonio se puede encontrar en varios nombres que todavía se usan en la mayoría de las implementaciones de UNIX, incluyendo Linux.

Poco tiempo después, Dennis Ritchie, uno de los colegas de Thompson en Bell Laboratories y uno de los primeros colaboradores de UNIX, diseñó e implementó el lenguaje de programación C. Este fue un proceso evolutivo; C siguió a uno anterior lenguaje interpretado, B. B fue implementado inicialmente por Thompson y atrajo a muchos de sus ideas de un lenguaje de programación aún anterior llamado BCPL. Para 1973, C había maduró hasta un punto en el que el kernel de UNIX podría reescribirse casi por completo en el nuevo idioma UNIX se convirtió así en uno de los primeros sistemas operativos en ser escrito en un lenguaje de alto nivel, hecho que hizo posible su posterior portabilidad a otras arquitecturas de hardware.

La génesis de C explica por qué él y su descendiente C++ han llegado a usarse tan ampliamente como los lenguajes de programación de sistemas en la actualidad. Idiomas anteriores ampliamente utilizados fueron diseñados con otros propósitos en mente: FORTRAN para tareas matemáticas realizado por ingenieros y científicos; COBOL para procesamiento de sistemas comerciales
flujos de datos orientados a registros. C llenó un nicho hasta ahora vacío y, a diferencia de FOR TRAN y COBOL (que fueron diseñados por grandes comités), el diseño de C surgió de las ideas y necesidades de unas pocas personas que trabajan hacia un solo objetivo:
desarrollar un lenguaje de alto nivel para implementar el núcleo UNIX y asociados software. Al igual que el propio sistema operativo UNIX, C fue diseñado por profesionales programadores para su propio uso. El lenguaje resultante fue pequeño, eficiente, poderoso, conciso, modular, pragmático y coherente en su diseño.
