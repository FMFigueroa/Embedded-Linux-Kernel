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

Tras cuatro décadas de uso, los informáticos siguen considerando el sistema operativo Unix
como uno de los sistemas más potentes y elegantes que existen. Desde la creación de Unix en
1969, la creación de Dennis Ritchie y KenThompson se ha convertido en una criatura de puntas de pierna, un sistema cuyo diseño ha resistido la prueba del tiempo con pocas contusiones en su nombre.
Unix surgió de Multics, un proyecto fallido de sistema operativo multiusuario en el que Bell
Laboratories estuvo involucrado. Con el proyecto Multics terminado, los miembros del Centro de Investigación de Ciencias de la Computación de Bell Laboratories se encontraron sin un sistema operativo interactivo capaz. En el verano de 1969, los programadores de Bell Lab esbozaron un
diseño de sistema de archivos que finalmente evolucionó a Unix. Probando su diseño, Thompson implementó el nuevo sistema en un PDP-7 que de otro modo estaría inactivo. En 1971, Unix fue portado a la
PDP-11, y en 1973, el sistema operativo fue reescrito en C, un paso sin precedentes en
el momento, pero que allanó el camino para la futura portabilidad. El primer Unix ampliamente utilizado
fuera de Bell Labs estaba Unix System, Sixth Edition, más comúnmente llamado V6.
Otras compañías portaron Unix a nuevas máquinas. Acompañando a estos puertos estaban
mejoras que resultaron en varias variantes del sistema operativo. En 1977, Laboratorios Bell
lanzó una combinación de estas variantes en un solo sistema, Unix System III; en 1982,
AT&T lanzó el Sistema V

#### Primera a sexta ediciones de UNIX

Entre 1969 y 1979, UNIX pasó por varios lanzamientos, conocidos como ediciones.
Esencialmente, estos lanzamientos fueron instantáneas de la versión de desarrollo en evolución en
AT&T. [Salus, 1994] señala las siguientes fechas para las primeras seis ediciones de UNIX:

- First Edition, November 1971: By this time, UNIX was running on the PDP-11 and already had a FORTRAN compiler and versions of many programs still used today, including ar, cat, chmod, chown, cp, dc, ed, find, ln, ls, mail, mkdir, mv, rm, sh, su, and who.
- Second Edition, June 1972: By this time, UNIX was installed on ten machines within AT&T.
- Third Edition, February 1973: This edition included a C compiler and the first implementation of pipes.
- Fourth Edition, November 1973: This was the first version to be almost totally written in C.
- Fifth Edition, June 1974: By this time, UNIX was installed on more than 50 systems.
- Sixth Edition, May 1975: This was the first edition to be widely used outside AT&T.

Durante el período de estos lanzamientos, el uso y la reputación de UNIX comenzaron a extenderse,
primero dentro de AT&T y luego más allá. Una importante contribución a este creciente conciencia fue la publicación de un artículo sobre UNIX en la revista ampliamente leída Comunicaciones de la ACM ([Ritchie & Thompson, 1974]).
En ese momento, AT&T tenía un monopolio autorizado por el gobierno en el sistema telefónico estadounidense. Los términos del acuerdo de AT&T con el gobierno de EE. UU. impedían de vender software, lo que significaba que no podía vender UNIX como producto.
En cambio, a partir de 1974 con la Quinta Edición, y especialmente con la Sexta Edición, AT&T licenció UNIX para uso en universidades por una tarifa de distribución nominal. los distribuciones universitarias incluían documentación y el código fuente del núcleo (alrededor de 10.000 líneas en ese momento).
El lanzamiento de UNIX de AT&T en las universidades contribuyó en gran medida a la popularidad
y el uso del sistema operativo, y en 1977, UNIX estaba funcionando en unos 500 sitios, incluyendo 125 universidades en los Estados Unidos y varios otros países. UNIX ofreció a las universidades un sistema operativo multiusuario interactivo que era barato pero potente, en una época en que los sistemas operativos comerciales eran muy caros. También dio a los departamentos universitarios de ciencias de la computación el código fuente de un sistema operativo real sistema, que podrían modificar y ofrecer a sus estudiantes para aprender y experimentar con. Algunos de estos estudiantes, armados con conocimientos de UNIX, se convirtieron Evangelistas de UNIX. Otros fundaron o se unieron a la multitud de empresas emergentes que venden estaciones de trabajo informáticas económicas que ejecutan el sistema operativo UNIX de fácil portabilidad.
