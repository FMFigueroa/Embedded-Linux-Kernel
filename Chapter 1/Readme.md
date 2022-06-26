# [Embedded Linux](https://github.com/FMFigueroa/Embedded-Linux-Kernel)

## Chapter 1 - Introducción a Linux Kernel

### Historia de Linux

Este capítulo presenta el kernel de Linux y el sistema operativo Linux, antes de entender Linux, primero debemos conocer sus origenes, primero hablemos del sistema operativo llamado Unix.
Unix fue creado por primera vez hace más de 40 años.

Linux es un miembro de la familia de sistemas operativos UNIX. En términos de computación, UNIX tiene una larga historia. La primera parte de este capítulo proporciona un breve resumen de esa historia comenzamos con una descripción de los orígenes del sistema UNIX y el lenguaje de programación C, y luego considere las dos corrientes clave que llevaron a el Sistema Linux tal como existe hoy: el proyecto GNU y el desarrollo de Linux núcleo.

Una de las características notables del sistema UNIX es que su desarrollo no fue controlado por un solo proveedor u organización. Más bien, muchos grupos, tanto comerciales como no comerciales, contribuyeron a su evolución. Esta historia dio lugar a muchos características innovadoras que se agregaron a UNIX, pero también tuvo la consecuencia negativa que las implementaciones de UNIX divergieron con el tiempo, por lo que escribir aplicaciones que trabajen en todas las implementaciones de UNIX se hizo cada vez más difícil. Esto condujo a una impulso para la estandarización de las implementaciones de UNIX.

### Una breve historia de UNIX y C

La primera implementación de UNIX se desarrolló en 1969 (el mismo año que Linus Torvalds nació ) por Ken Thompson en Bell Laboratories, una división de la corporación telefónica AT&T. Fue escrito en ensamblador para una mini computadora Digital PDP-7. El nombre UNIX es un juego de palabras con MULTICS (Multiplexed Information and servicio informático), el nombre de un proyecto de sistema operativo anterior en el que AT&T colaboró ​​con el Instituto Tecnológico de Massachusetts (MIT) y General Electric. (AT&T ya se había retirado del proyecto frustrado por su inicial fracaso en el desarrollo de un sistema económicamente útil.) Thompson extrajo varias ideas para su nuevo sistema operativo de MULTICS, que incluye un sistema de archivos con estructura de árbol, un programa separado para interpretar comandos (el shell) y la noción de archivos como flujos de bytes no estructurados.

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

### El nacimiento de BSD y System V

Enero de 1979 vio el lanzamiento de la séptima edición de UNIX, que mejoró la confiabilidad del sistema y proporcionó un sistema de archivos mejorado. Esta versión también contenía varias herramientas nuevas, incluidas awk, make, sed, tar, uucp, Bourne shell y un compilador FORTRAN 77. El lanzamiento de la séptima edición también es significativo porque, a partir de este punto, UNIX se bifurcó en dos variantes importantes: BSD y System V, cuyos orígenes ahora describimos brevemente.

Thompson pasó el año académico 1975/1976 como profesor invitado en la Universidad de California en Berkeley, la universidad de la que se había graduado. Allí, trabajó con varios estudiantes de posgrado, agregando muchas características nuevas a UNIX. (Uno de estos estudiantes, Bill Joy, posteriormente cofundó Sun Microsystems, una entrada temprana en el mercado de estaciones de trabajo UNIX.) Con el tiempo, muchos desarrollaron nuevas herramientas y funciones en Berkeley, incluido el shell C, el editor vi , un sistema de archivos mejorado (el Sistema de archivos rápidos de Berkeley), sendmail, un compilador Pascal y administración de memoria virtual en la nueva arquitectura Digital VAX.

Bajo el nombre de Berkeley Software Distribution (BSD), esta versión de UNIX, incluyendo su código fuente, llegó a ser ampliamente distribuido. La primera distribución completa fue 3BSD en diciembre de 1979. (Lanzamientos anteriores de Berkeley—BSD y 2BSD eran distribuciones de nuevas herramientas producidas en Berkeley, en lugar de UNIX completo distribuciones.)

En 1983, el Grupo de Investigación de Sistemas Informáticos de la Universidad de California en
Berkeley lanzó 4.2BSD. Esta versión fue importante porque contenía una implementación completa de TCP/IP, incluida la programación de aplicaciones de sockets (API) y una variedad de herramientas de red.
4.2BSD y su predecesor 4.1BSD se distribuyó ampliamente en universidades de todo el mundo. Ellos también formaron la base de SunOS (lanzado por primera vez en 1983), la variante de UNIX vendida por Sun.
Otros lanzamientos importantes de BSD fueron 4.3BSD, en 1986, y el lanzamiento final, 4.4BSD,
en 1993.

Mientras tanto, la legislación antimonopolio de EE. UU. forzó la disolución de AT&T ( maniobras legales comenzaron a mediados de la década de 1970, y la ruptura se hizo efectiva en 1982),
con la consecuencia de que, al dejar de tener el monopolio del teléfono se permitió a la empresa comercializar UNIX. Esto resultó en la liberación de System III (tres) en 1981. System III fue producido por UNIX Support de AT&T Group (USG), que empleó a muchos cientos de desarrolladores para mejorar UNIX y desarrollar aplicaciones UNIX (en particular, paquetes de preparación de documentos y herramientas de desarrollo de software). El primer lanzamiento de System V (cinco) siguió en 1983, y una serie de lanzamientos condujo al definitivo System V Release 4 (SVR4) en 1989, por momento en el que System V había incorporado muchas características de BSD, incluidas las instalaciones de trabajo en red. System V fue licenciado a una variedad de vendedores comerciales, quienes lo utilizaron como base de sus implementaciones UNIX.
Por lo tanto, además de las diversas distribuciones de BSD que se extendieron a través de la academia, a fines de la década de 1980, UNIX estaba disponible en una variedad de implementaciones comerciales en varios hardware. Estas implementaciones incluyeron SunOS de Sun y versiones posteriores Solaris, Ultrix y OSF/1 de Digital (actualmente, después de una serie de cambios de nombre y adquisiciones, HP Tru64 UNIX), AIX de IBM, HP-UX de Hewlett-Packard (HP), NeXTStep de NeXT, A/UX para Apple Macintosh y Microsoft y SCO XENIX para la arquitectura Intel x86-32. (A lo largo de este libro, la implementación de Linux para x86-32 se denomina Linux/x86-32).
contraste con los escenarios típicos de hardware propietario/sistema operativo del tiempo, donde cada proveedor producía una, o como mucho unas pocas, computadoras propietarias de arquitecturas de chips, en las que vendían sus propios sistemas operativos patentados.
La naturaleza propietaria de la mayoría de los sistemas de proveedores significaba que los compradores estaban bloqueados en un solo vendedor. Cambiar a otro sistema operativo y hardware propietarios la plataforma podría volverse muy cara debido a la necesidad de portar las aplicaciones existentes y volver a capacitar al personal. Este factor, junto con la aparición de estaciones de trabajo UNIX baratas para un solo usuario de una variedad de proveedores, hizo que el sistema UNIX portátil cada vez más atractivo desde una perspectiva comercial.

El elegante diseño original del sistema Unix, junto con los años de innovación y la mejora evolutiva que siguió, ha resultado en un potente, robusto y estable sistema operativo. Un puñado de características de Unix son el núcleo de su fortaleza.

Primero, Unix es simple: mientras que algunos sistemas operativos implementan miles de llamadas al sistema y tienen objetivos de diseño poco claros, los sistemas Unix implementan solo cientos de llamadas al sistema y tener un diseño sencillo, incluso básico.

En segundo lugar, en Unix, todo es un archivo.
Esto simplifica la manipulación de datos y dispositivos en un conjunto de llamadas al sistema central: open(), read(), write(), lseek() y close().

En tercer lugar, el kernel de Unix y las utilidades del sistema relacionadas son escrito en C, una propiedad que le da a Unix su increíble portabilidad a hardware diverso arquitecturas y accesibilidad a una amplia gama de desarrolladores. Cuarto, Unix tiene un proceso rápido
tiempo de creación y la única llamada al sistema fork(). Por último, Unix proporciona un sistema simple pero robusto primitivas de comunicación entre procesos (IPC) que, cuando se combinan con el proceso rápido tiempo de creación, permiten la creación de programas simples que hacen una cosa y la hacen bien.

Estos son los programas de un solo propósito se pueden unir para realizar tareas de complejidad creciente. Por lo tanto, los sistemas Unix exhiben capas limpias, con una fuerte separación entre la política y mecanismo.

En la actualidad, Unix es un sistema operativo moderno que admite tareas múltiples preventivas, subprocesos múltiples, memoria virtual, paginación bajo demanda, bibliotecas compartidas con carga bajo demanda y Redes TCP/IP. Muchas variantes de Unix escalan a cientos de procesadores, mientras que los otras sistemas Unix se ejecutan en dispositivos integrados pequeños. Aunque Unix ya no es una investigación proyecto, los sistemas Unix continúan beneficiándose de los avances en el diseño del sistema operativo mientras siendo un sistema operativo práctico y de propósito general.

Unix debe su éxito a la simplicidad y elegancia de su diseño. Su fuerza hoy se deriva de las decisiones inaugurales que Dennis Ritchie, Ken Thompson y que los otros primeros desarrolladores tomaron: elecciones que han dotado a Unix con la capacidad de evolucionar sin comprometerse.

### Una breve historia de Linux

El término Linux se usa comúnmente para referirse a todo el sistema operativo similar a UNIX del cual forma parte el kernel de Linux. Sin embargo, esto es algo así como un nombre inapropiado, ya que muchos de los componentes clave contenidos dentro de un comercial típico La distribución de Linux en realidad se originó a partir de un proyecto anterior al inicio de Linux por varios años.

Linus Torvalds desarrolló la primera versión de Linux en 1991 como sistema operativo para
ordenadores alimentados por el microprocesador Intel 80386, que en ese momento era un nuevo y
procesador avanzado. Linus, entonces estudiante de la Universidad de Helsinki, estaba perturbado por la falta de un sistema Unix poderoso pero libre. El sistema operativo de computadora personal reinante del día, el DOS de Microsoft, fue útil para Torvalds para poco más que jugar Prince of Persia.

Linus usó Minix, un Unix de bajo costo creado como ayuda para la enseñanza, pero se desanimó por
la incapacidad de realizar y distribuir fácilmente cambios en el código fuente del sistema (debido a licencia de Minix) y por decisiones de diseño tomadas por el autor de Minix.

En respuesta a su situación, Linus hizo lo que haría cualquier estudiante universitario normal:
Decidió escribir su propio sistema operativo. Linus comenzó escribiendo un terminal simple emulador, que usó para conectarse a sistemas Unix más grandes en su escuela. En el transcurso
del año académico, su emulador de terminal evolucionó y mejoró. En poco tiempo, Linus había
un Unix inmaduro pero completo en sus manos. Publicó un comunicado anticipado en Internet a fines de 1991.

El uso de Linux despegó, y las primeras distribuciones de Linux ganaron rápidamente muchos usuarios. Sin embargo, más importante para su éxito inicial es que Linux atrajo rápidamente a muchos desarrolladores: piratas informáticos que agregaban, cambiaban y mejoraban el código. Debido a los términos de su licencia, Linux evolucionó rápidamente hasta convertirse en un proyecto colaborativo desarrollado por muchos.

Un avance rápido hasta el presente. Hoy en día, Linux es un sistema operativo completo que también ejecuta en Alpha, ARM, PowerPC, SPARC, x86-64 y muchas otras arquitecturas. Funciona desde sistemas tan pequeños como un reloj hasta máquinas tan grandes como grupos de supercomputadoras que llenan una habitación.

Linux impulsa la electrónica de consumo más pequeña y los centros de datos más grandes. Hoy en día, el interés comercial en Linux es fuerte. Tanto las nuevas corporaciones específicas de Linux, como Red Hat y las potencias existentes, como IBM, están proporcionando soluciones basadas en Linux para necesidades integradas, móviles, de escritorio y de servidor.

Linux es un sistema similar a Unix, pero no es Unix. Es decir, aunque Linux toma prestadas muchas
ideas de Unix e implementa la API de Unix (según lo definido por POSIX y Single Especificación de Unix), no es un descendiente directo del código fuente de Unix como otros Unix sistemas. Donde se desea, se ha desviado del camino tomado por otras implementaciones, pero no ha abandonado los objetivos generales de diseño de Unix ni ha roto la interfaz de aplicación estandarizada.
Una de las características más interesantes de Linux es que no es un producto comercial; en cambio,
es un proyecto colaborativo desarrollado a través de Internet. Aunque Linus sigue siendo el creador de Linux y el mantenedor del núcleo, el progreso continúa a través de un tejido suelto.
grupo de desarrolladores. Cualquiera puede contribuir a Linux. El kernel de Linux, como ocurre con gran parte de el sistema, es un software gratuito o de código abierto.

Específicamente, el kernel de Linux tiene licencia bajo la Licencia Pública General GNU (GPL) versión 2.0. En consecuencia, puede descargar el código fuente y realizar las modificaciones que desee. La única advertencia es que si distribuir sus cambios, debe continuar brindando a los destinatarios los mismos derechos disfrutaste, incluida la disponibilidad del código fuente.

Linux es muchas cosas para muchas personas. Los elementos básicos de un sistema Linux son el kernel, C biblioteca, cadena de herramientas y utilidades básicas del sistema, como un proceso de inicio de sesión y shell. Un sistema Linux también puede incluir una implementación moderna del sistema X Window que incluye una función completa entorno de escritorio, como GNOME. Miles de aplicaciones gratuitas y comerciales existen para Linux. En este libro, cuando digo Linux normalmente me refiero al kernel de Linux. ambiguo, trato explícitamente de señalar si me estoy refiriendo a Linux como un sistema completo o solo el núcleo propiamente dicho. Estrictamente hablando, el término Linux se refiere solo al kernel.

### El Proyecto GNU

En 1984, Richard Stallman, un programador excepcionalmente talentoso que había sido
trabajando en el MIT, se dispuso a trabajar en la creación de una implementación UNIX "gratuita". de Stallman la perspectiva era moral, y libre se definía en un sentido legal, en lugar de un sentido financiero (ver http://www.gnu.org/philosophy/free-sw.html).
No obstante, lo legal es la libertad que Stallman describió conllevaba la consecuencia implícita de que software como los sistemas operativos estarían disponibles sin costo alguno oa muy bajo costo.

Stallman militó en contra de las restricciones legales impuestas a los sistemas operativos propietarios por parte de los vendedores de computadoras. Estas restricciones significaban que los compradores de software de computadora en general no podían ver el código fuente del software que estaban comprando.

comprando, y ciertamente no podrían copiarlo, cambiarlo o redistribuirlo. El Señaló que dicho marco alentaba a los programadores a competir entre sí y atesoran su trabajo, en lugar de cooperar y compartirlo.
En respuesta, Stallman inició el proyecto GNU (un acrónimo definido recursivamente para "GNU no es UNIX") para desarrollar un sistema similar a UNIX completo, disponible gratuitamente, consistente en un núcleo y todos los paquetes de software asociados, y alentó a otros a unirse a él. En 1985, Stallman fundó la Free Software Foundation (FSF), una organización sin fines de lucro para apoyar el proyecto GNU y el desarrollo de software libre en general.

Cuando se inició el proyecto GNU, BSD no era libre en el sentido que significaba Stallman. El uso de BSD todavía requería una licencia de AT&T y los usuarios podían no modificar y redistribuir libremente el código de AT&T que formaba parte de BSD.

Uno de los resultados importantes del proyecto GNU fue el desarrollo de la Licencia Pública General GNU (GPL), la encarnación legal de la noción de software libre de Stallman. Gran parte del software en una distribución de Linux, incluido el kernel, tiene licencia GPL o una de varias licencias similares. El software con licencia GPL debe estar disponible en forma de código fuente y debe poder redistribuirse libremente según los términos de la GPL. Las modificaciones al software con licencia GPL están permitidas libremente, pero cualquier distribución de dicho software modificado también debe estar bajo los términos de la GPL. Si el software modificado se distribuye en formato ejecutable, el autor también debe permitir a los destinatarios la opción de obtener la fuente modificada por no más del costo de distribución. La primera versión del
GPL se lanzó en 1989. La versión actual de la licencia, la versión 3, se lanzó en 2007. La versión 2 de la licencia, lanzada en 1991, sigue siendo de uso generalizado y es la licencia utilizada para el kernel de Linux. (Las discusiones sobre varias licencias de software libre se pueden encontrar en [St. Laurent, 2004] y [Rosen, 2005].)

El proyecto GNU inicialmente no produjo un núcleo UNIX en funcionamiento, pero produjo una amplia gama de otros programas. Dado que estos programas se diseñaron para ejecutarse en un sistema operativo similar a UNIX, podían usarse y se usaron en implementaciones UNIX existentes y, en algunos casos, incluso se trasladaron a otros sistemas operativos. Entre los programas más conocidos producidos por el proyecto GNU se encuentran el editor de texto Emacs, GCC (originalmente el compilador GNU C, pero ahora renombrado como colección de compiladores GNU, que comprende compiladores para C, C++ y otros lenguajes), bash shell y glibc (la biblioteca GNU C).

A principios de la década de 1990, el proyecto GNU había producido un sistema que estaba prácticamente completo, excepto por un componente importante: un núcleo UNIX en funcionamiento. El proyecto GNU había comenzado a trabajar en un diseño de kernel ambicioso, conocido como GNU/HURD, basado en el microkernel Mach. Sin embargo, la HURD estaba lejos de ser una forma que podría ser liberado. (Al momento de escribir este artículo, el trabajo continúa en HURD, que actualmente solo se ejecuta en la arquitectura x86-32).

Debido a que una parte significativa del código del programa que constituye lo que comúnmente se conoce como el sistema Linux en realidad se deriva del proyecto GNU, Stallman prefiere usar el término GNU/Linux para referirse a todo el sistema. La cuestión de la denominación (Linux versus GNU/Linux) es fuente de cierto debate en la comunidad del software libre. Dado que este libro se ocupa principalmente de la API del kernel de Linux, generalmente usaremos el término Linux.

El escenario estaba listo. Todo lo que se requería era un kernel en funcionamiento para ir con el otro sistema UNIX completo ya producido por el proyecto GNU.
