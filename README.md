# TR10RS1 cambio de Sistema Operativo e información adicional

**Descargo de responsabilidad: esto es solo una guía sobre como se le puede cambiar el sistema operativo que tiene la tablet canaima TR10RS1 y no me hago responsable del daño que usted le pueda causar a esta, si procede será bajo su propio riesgo.**

**Advertencia: después de haber eliminado como 12 particiones o más del sistema operativo Android que trae la tablet canaima para poder instalar otro sistema operativo me percaté de que ya no administra la energía de la batería como lo haría normalmente, lo más probable es que en algunas de estás particiones esté la información que se encarga de administrarla y dar el indicativo visual del led de cuando está totalmente cargada, el típico indicador en la pantalla de la batería cargándose o el ícono en el sistema operativo que indica el porcentaje de la batería, por lo que deduzco que los controladores para ello están en alguna de estas particiones, sin embargo la batería sigue funcionando como siempre, solo que por software no muestra su capacidad de carga.**
**También al ponerla a cargar mientras está apagada esta se enciende automáticamente y busca arrancar en el sistema operativo instalado**

**Nota: si gustas ayudarme a desarrollar los controladores, ya sea adaptándolos o creándolos desde 0 que son necesarios para la administración de carga de la batería tu ayuda será más que bienvenida y puedes contactarme desde el correo electrónico que está en mi perfil**

Características a tener en cuenta de la tablet canaima **TR10RS1**:

- Procesador: [**Intel Atom Z3735F**](https://www.intel.la/content/www/xl/es/products/sku/80274/intel-atom-processor-z3735f-2m-cache-up-to-1-83-ghz/specifications.html) **x86** de **4 núcleos** a **1.33Ghz**.
- Memoria RAM: **1GB**(256MBx4) **DDR3L-RS** a **1333Mhz** (capacidad máxima de 2GB).
- Almacenamiento interno: **EMMC de 16GB**/(32GB).
- Entre otros: el resto se puede encontrar por internet.

## ¿Qué sistema operativo se le puede instalar?

Toda tablet con procesador **x86**, es posible cambiarle el sistema operativo por casi cualquiera que se desee, ya sea **Windows**, **GNU Linux** o incluso una versión de **Android-x86** más reciente.

## ¿Es posible instalar Windows?

Si es posible, sin embargo no lo recomiendo debido a los siguientes motivos:

1) La **capacidad máxima** de memoria **RAM** que soporta es de **2GB**, aunque se le cambie el **procesador** no supera este número y no hay una gran mejoría al hacerlo debido a que la frecuencia base del procesador es la misma y la frecuencia turbo no se aleja casi nada del que ya tiene instalado, por lo que Windows se movería bastante lento (y casi cualquier otro sistema operativo en general).
2) La capacidad **máxima** del **EMMC** (que es la memoria interna) es de **16GB**, pero según [**este documento**](https://www.ecs.com.tw/en/Product/TabletPC/TR10RS/download) puede ser de hasta **32GB** y **Windows** requiere como mínimo:
   - Windows 7/8: **16GB** para **32 bits** y **20GB** para **64 bits**.
   - Windows 10: **32GB**.
3) No se puede usar una **Micro SD** para instalar el sistema operativo.
4) Tiene una zona para soldar un **socket M.2 KEY B** [similar a este](https://www.aliexpress.us/item/3256808154255875.html?spm=a2g0o.cart.similar_items.2.166e38da7MIhhp&utparam-url=scene%3Aimage_search%7Cquery_from%3Acart_soldout_item&algo_pvid=da5d7f27-763d-4646-83dd-43f20accda91&algo_exp_id=da5d7f27-763d-4646-83dd-43f20accda91&pdp_ext_f=%7B%22order%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%212.20%212.20%21%21%212.20%212.20%21%402103010e17484491025982536e26fc%2112000044657681317%21sea%21US%213854250801%21X&gatewayAdapt=4itemAdapt), desconozco si funcionará a primeras o haya que agregar los controladores a la **BIOS** haciendo un **BIOS Mod** para que reconozca un **SSD M.2 KEY B tipo SATA**, pero solo de ser posible colocarlo se podría instalar Windows allí.
5) **Falta de controladores**, debido a que no hay soporte oficial para los controladores en **Windows** por parte del **fabricante** quizás no tenga la mejor experiencia de usuario y esté limitado en algunas características.

## ¿Qué sistema operativo es recomendable?

**GNU Linux** sin lugar a dudas, debido a que cuenta con **controladores** necesarios para hacer que la tablet canaima **TR10RS1** funcione generalmente bien.

Un ejemplo de ello:

![Imagen del SO Linux iniciando](/img/IMG_20250529_170318.jpg)
![Imagen del SO Linux iniciado](/img/IMG_20250529_170611.jpg)

Nota: yo instalé Debian y debido al limitado hardware de la tablet canaima hacerlo sin interfaz gráfica fue más rápido.

## ¿Qué funciona?

- ### En linux:

  - Pantalla
  - Táctil (no probado)
  - Sonido (solo por la salida HDMI)
  - Jack de audio (no funciona)
  - Botones de volumen
  - USB OTG
  - WiFi
  - Bluetooth
  - Indicador de carga de la batería (funciona solo el led, pero no lo hace correctamente)
  - Cámaras (no funcionan)
  - Micro HDMI
  - Micro SD (no la reconoce en el arranque/boot)

- ### En Windows

  - En proceso

## ¿Qué utilidad podría tener un equipo con hardware tan limitado?

Existen diferentes proyectos que se pueden realizar con computadoras con hardware limitado, los ejemplos perfectos son las [**Raspberry Pi**](https://www.raspberrypi.com/).

Algunos podrían ser:

- Router WiFi + AP.
- TV Box
- Servidor multimedia.
- Servidor de páginas web.
- Instalar klipper/octoprint para manipular una impresoras 3D (mi caso).
- E-book.
- Entre otros.

## ¿Cómo entrar en la BIOS?

Primero hay que tenerla **rooteada** con el proyecto de [**TR10-TOOL**](https://github.com/neocarvajal/TR10-TOOL) se puede lograr o con cualquier otro método que se desee para que permita entrar en la BIOS presionando la tecla **"F2"** con cualquier teclado.

## ¿Se le puede remover el logo del gobierno?

Si, habilitando el **"Quick boot"** en **"Main-->Boot Features-->Quick Boot=Enabled"** desde la **BIOS** este desaparece.

## ¿Se puede instalar cualquier sistema operativo?

No, debido a que esta **BIOS** está basada en **EFIx64 (UEFI)** lo que no hace posible la instalación de sistemas operativos basados en **Legacy**.

## ¿Cómo poder arrancar (bootear) desde una unidad USB?

Primero hay que deshabilitar el modo **"Secure BOOT"** se logra colocando una **contraseña de administrador** en **"Security-->Set Supervisor Password"** a la **BIOS** para poder acceder a **Secure Boot Configuration** y desactivarlo en **"Secure Boot Configuration-->Secure Boot Option=Disabled"**, luego si lo desea puede quitar la contraseña de administrador después de hacerlo, y luego colocar la unidad USB de primero en el orden de **arranque (BOOT)** en **"Boot-->Boot Priority Order"** con las teclas **"+"** y **"-"** del teclado numérico, por último guardar los cambios presionando la tecla **"F10"** y guardar los cambios pulsando **"enter"** en **"yes"**.

## ¿Cuántos puertos USB tiene?

Solo tiene instalado de forma física **1 USB (micro B)**, sin embargo se puede aumentar agregando un **OTG micro B** y un **USB HUB**, otro método puede ser que se le añada otro adicional si se usa la comunicación serial UART con un traductor de [UART a USB](https://www.aliexpress.us/item/3256806418302191.html?spm=a2g0o.cart.similar_items.1.166e38da7MIhhp&utparam-url=scene%3Aimage_search%7Cquery_from%3Acart_soldout_item&algo_pvid=d5e3b5f2-f276-4b62-98ed-692b26c2e417&algo_exp_id=d5e3b5f2-f276-4b62-98ed-692b26c2e417&pdp_ext_f=%7B%22order%22%3A%22271%22%7D&pdp_npi=4%40dis%21USD%218.11%212.66%21%21%2158.05%2119.03%21%402101ea7117484497414076128ed5b5%2112000037796709909%21sea%21US%213854250801%21X&gatewayAdapt=4itemAdapt), o usando el socket del **M.2 KEY B** que tiene las conexiones para un **USB** en sus pines.

## Notas finales

Si gustas que continue con mi **proyecto personal** de investigación sobre las tablet canaima **TR10RS1**, incluya información sobre su antecesor la **TR10CS1** o simplemente gustas darme tu opinión al respecto, por favor házmelo saber en el **correo electrónico** que está en mi **perfil**