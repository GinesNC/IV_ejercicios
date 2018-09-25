# Ejercicios Tema 1: _Introducción a la infraestructura virtual: concepto y soporte físico_

## Ejercicio 1
 #### Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años. Consultar [este artículo en Infoautónomos sobre el tema](https://infoautonomos.eleconomista.es/consultas-a-la-comunidad/988/).

La amortización de, por ejemplo, este servidor [Dell](https://www.dell.com/es-es/work/shop/servidores-almacenamiento-y-redes/smart-value-flexi-poweredge-t640-8x35-3104-1x8gb-1x300gb-15k-sas-h330-3y-nbd/spd/poweredge-t640/pet6401) que cuesta unos 1338,14€, sin I.V.A. y debido a que se puede deducir en el trimestre de la compra, no es necesario tenerlo en cuenta para los cálculos.

Si partimos de la situación de que empezamos el 1 de enero, la amortización para 4 y 7 años es:
- 4 años: 1338,14 / 4 = **334,54 €/año**

- 7 años: 1338,14 / 7 = **191,16 €/año**

<!-- https://getquipu.com/blog/como-amortizo-los-bienes-de-inversion/ -->

## Ejercicio 2
 #### Usando las tablas de precios de servicios de alojamiento en Internet “clásicos”, es decir, que ofrezcan Virtual Private Servers o servidores físicos, y de proveedores de servicios en la nube, comparar el coste durante un año de un ordenador con un procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) y con el resto de las características similares (tamaño de disco duro equivalente a transferencia de disco duro) en el caso de que la infraestructura comprada se usa sólo el 1% o el 10% del tiempo.

 En mi caso he escogido para comparar lo que ofrecen [1and1](https://www.1and1.es/servidores-virtuales) y [Arsys](https://www.arsys.es/servidores/vps). Ambas configuraciones los mismos cores virtuales, en concreto uno, de un procesador Intel Xeon y almacenamiento SSD de 50 y 40 GB respectivamente. También ofrecen el mismo hypervisor: VMware. Con respecto al tiempo de uso no se puede elegir, ya que al pagar se hace un contrato de un tráfico ilimitado.

 Todos los precios son sin I.V.A. por lo que el precio final sería un poco más caro. En 1and1 ofrecen esta configuración en una promoción de un año por 4,99€/mes y luego pasaría a 9,99€/mes. En Arsys el precio si se contrata anual es de 10€/mes y si se contrata por meses serían 13€/mes. En base a esto elegiría 1and1, ya que el primer año saldría por la mitad que Arsys.
## Ejercicio 3
  #### En general, cualquier ordenador con menos de 5 o 6 años tendrá estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden? Si usas una máquina virtual, ¿qué resultado da? ¿Y en una Raspberry Pi o, si tienes acceso, el procesador del móvil?

  El procesador de mi pc es un Intel(R) Core(TM) i7-3610QM CPU @ 2.30GHz. tras la ejecución de la orden

    egrep '^flags.*(vmx|svm)' /proc/cpuinfo

<!-- ** -->

  Sale lo siguiente:

    flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov
    pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx rdtscp
    lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc
    cpuid aperfmperf pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16
    xtpr pdcm pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx
    f16c rdrand lahf_lm cpuid_fault epb pti retpoline spec_ctrl tpr_shadow vnmi
    flexpriority ept vpid fsgsbase smep erms xsaveopt dtherm ida arat pln pts

Repetido tantas veces como cores lógicos tiene el procesador.

## Ejercicio 4
  #### 1. Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok.

  ![Salida de la orden](https://www.dropbox.com/s/bw1rb54idtjgobb/kvm-ok.png?dl=0)

  #### 2. Instalar un hipervisor para gestionar máquinas virtuales, que más adelante se podrá usar en pruebas y ejercicios.

  Como hipervisor he elegido VirtualBox, ya que lo he usado varias veces y estoy más familiarizado.

## Ejercicio 5
  #### Darse de alta en servicios de nube usando ofertas gratuitas o cupones que pueda proporcionar el profesor.

## Ejercicio 6
  #### Darse de alta en una web que permita hacer pruebas con alguno de los sistemas de gestión de nube anteriores.
