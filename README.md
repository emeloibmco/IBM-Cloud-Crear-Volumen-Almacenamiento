# IBM Cloud - Crear Volumen de Almacenamiento ☁💾
Los servidores virtuales son totalmente compatibles con *File Storage*, *Block Storage*, así como con *IBM® Cloud Object Storage*. Estos tipos de almacenamiento son los recomendados para unidades de clúster, almacenamiento de archivos compartidos, almacenamiento de archivado, grandes requisitos de almacenamiento o requisitos de rendimiento específicos.

La presente guía esta enfocada en la creación y configuración de diferentes tipos de almacenamiento, asi como la capacidad de adjuntar un almacenamiento como un volumen a una VSI. 
## Índice  📰
1. [Pre-Requisitos](#Pre-Requisitos-pencil)
2. [Crear servicio File Storage](#Crear-servicio-File-Storage-card_file_box)
3. [Consultar servicio File Storage](#Consultar-servicio-File-Storage-mag-card_file_box)
4. [Crear servicio Block Storage](#Crear-servicio-de-almacenamiento-Block-Storage-package)
5. [Consultar servicio Block Storage](#Consultar-servicio-Block-Storage-mag-package)
6. [Crear servicio Object Storage](#Crear-servicio-Object-Storage-file_cabinet)
7. [Consultar servicio Object Storage](#Consultar-servicio-Object-Storage-mag-file_cabinet)
8. [Crear volumen de Block Storage for VPC](#Crear-volumen-de-Block-Storage-for-VPC-cloud-package)
9. [Adjuntar volumen de Block Storage a una VSI en VPC](#Adjuntar-volumen-de-Block-Storage-a-una-VSI-en-VPC-cloud-computer)
10. [Consultar volumen de Block Storage desde una VSI en VPC](#Consultar-volumen-de-Block-Storage-desde-una-VSI-en-VPC-mag-computer)
11. [Referencias](#Referencias-pushpin)
12. [Autores](#Autores-black_nib)


## Pre-requisitos :pencil:
* Contar con una cuenta en <a href="https://cloud.ibm.com/"> IBM Cloud </a>.
* Contar con una *VPC* y un grupo de recursos.
* Contar con una *VSI* Linux en *VPC*.
<br />

## Crear servicio File Storage :card_file_box:
Para crear el servicio de almacenamiento *File Storage* en su cuenta de *IBM Cloud* complete los siguientes pasos:
<br />

1. Acceda al catálogo y busque el servicio *File Storage* en la categoría del Almacenamiento.
<br />

2. Seleccione el servicio *File Storage*. Posteriormente, se abrirá una ventana en la cual se muestra información relacionada con el servicio. De click en el botón ```Crear/To Create```.
<br />

3. Una vez cargue la nueva ventana complete la configuración del servicio de la siguiente manera:
* ```Ubicación/Location```: seleccione la ubicación en la cual desplegará el servicio.

**Detalles/Details**: 
* ```Método de Facturacción/Billing Method```: seleccione el método de facturación que desea utilizar ya se Por horas/For hours o Por meses/For month.
* ```Tamaño/Size```: especifique el tamaño, recuerde que debe ser un valor entre 20 y 12000 GB.
* ```Espacio de Instantáneas/Snapshot Space```: especifique el espacio de las instantáneas.

**Perfil de IOPS/IOPS Profile**: 
* ```Resistencia (niveles)/Resistance (levels)```: seleccione el nivel de resistencia en IOPS/GB.
* ```Rendimiento (personalizadas)/Performance (custom)```: Deje el valor por defecto (100).
<br />

4. Para finalizar, acepte los terminos y condiciones y de click en el botón ```Crear/To Create```.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Crear%20File%20Storage.gif"></p>

Observe las configuraciones realizadas en inglés.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/FileStorageEN.png"></p>
<br />

5. Espere unos minutos mientras se completa el aprovisionamiento del servicio de almacenamiento y observe su recurso en la ```Lista de Recursos/Resource List```.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/RS_FileStorage.PNG"></p>
<br />

> NOTA: En caso de no contar con los permisos para ver el recurso en la ```Lista de Recursos/Resource List```, puede ver el servicio de almacenamiento ingresando por ```Menú de navegación/Navigation Menu``` ➡ ```Infraestructura Clásica/Classic Infrastructure``` ➡ ```Almacenamiento/Storage``` ➡ ```File Storage```, como se muestra en la siguiente imagen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/AccesoFileStorage.gif"></p>
<br />

## Consultar servicio File Storage :mag: :card_file_box:
Para consultar el servicio de almacenamiento *File Storage* implementado en la sección anterior, de click sobre su recurso. Luego podrá observar las diferentes opciones que aparecen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/ConsultarFileStorage.gif"></p>
<br />

## Crear servicio Block Storage :package:
Para crear el servicio de almacenamiento *Block Storage* en su cuenta de *IBM Cloud* complete los siguientes pasos:
<br />

1. Acceda al catálogo y busque el servicio *Block Storage* en la categoría del Almacenamiento.
<br />

2. Seleccione el servicio *Block Storage*. Posteriormente, se abrirá una ventana en la cual se muestra información relacionada con el servicio. De click en el botón ```Crear/To Create```.
<br />

3. Una vez cargue la nueva ventana complete la configuración del servicio de la siguiente manera:
* ```Ubicación/Location```: seleccione la ubicación en la cual desplegará el servicio.

**Detalles/Details**: 
* ```Método de Facturacción/Billing Method```: seleccione el método de facturación que desea utilizar ya se Por horas/For hours o Por meses/For month.
* ```Tamaño/Size```: especifique el tamaño, recuerde que debe ser un valor entre 20 y 12000 GB.
* ```Espacio de Instantáneas/Snapshot Space```: especifique el espacio de las instantáneas.
* ```Tipo de SO/SO Type```: determine el tipo de sistema operativo que va utilizar.

**Perfil de IOPS/IOPS Profile**: 
* ```Resistencia (niveles)/Resistance (levels)```: seleccione el nivel de resistencia en IOPS/GB.
* ```Rendimiento (personalizadas)/Performance (custom)```: Deje el valor por defecto (100).
<br />

4. Para finalizar, acepte los terminos y condiciones y de click en el botón ```Crear/To Create```.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Crear%20Block%20Storage.gif"></p>

Observe las configuraciones realizadas en inglés.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/BlockStorageEN.png"></p>
<br />

5. Espere unos minutos mientras se completa el aprovisionamiento del servicio de almacenamiento y observe su recurso en la ```Lista de Recursos/Resource List```.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/RS_BlockStorage.PNG"></p>
<br />

> NOTA: En caso de no contar con los permisos para ver el recurso en la ```Lista de Recursos/Resource List```, puede ver el servicio de almacenamiento ingresando por ```Menú de navegación/Navigation Menu``` ➡ ```Infraestructura Clásica/Classic Infrastructure``` ➡ ```Almacenamiento/Storage``` ➡ ```Block Storage```, como se muestra en la siguiente imagen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/AccesoBlocktStorage.gif"></p>
<br />

## Consultar servicio Block Storage :mag: :package:
Para consultar el servicio de almacenamiento *Block Storage* implementado en la sección anterior, de click sobre su recurso. Luego podrá observar las diferentes opciones que aparecen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/ConsultaBlockStorage.gif"></p>
<br />

## Crear servicio Object Storage :file_cabinet:
Para crear el servicio de almacenamiento *Object Storage* en su cuenta de *IBM Cloud* complete los siguientes pasos:
<br />

1. Acceda al catálogo y busque el servicio *Object Storage* en la categoría del Almacenamiento.
<br />

2. Seleccione el servicio *Object Storage*. Posteriormente, se abrirá una ventana en la cual se muestra información relacionada con el servicio. De click en el botón ```Crear/To Create```.
<br />

3. Una vez cargue la nueva ventana complete la configuración del servicio de la siguiente manera:
* ```Seleccionar un plan de precios/Select a pricing plan```: especifique el plan de precios que desea utilizar para el despliegue de su servicio.

**Configurar su recurso/Configure your resource**: 
* ```Nombre de servicio/Service name```: indique un nombre exclusivo para su servicio.
* ```Seleccionar un grupo de recursos/Select a resource group```: especifique el grupo de recursos en el que va a trabajar.
<br />

4. Para finalizar de click en el botón ```Crear/To Create```.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Crear%20Object%20Storage.gif"></p>
<br />

## Consultar servicio Object Storage :mag: :file_cabinet:
Para consultar el servicio de almacenamiento *Object Storage* implementado en la sección anterior, de click sobre su recurso. Luego podrá observar las diferentes opciones que aparecen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/ConsultarObjectStorage.gif"></p>
<br />

## Crear volumen de Block Storage for VPC :cloud: :package:
Para crear el servicio de almacenamiento *Block Storage for VPC* en su cuenta de *IBM Cloud* complete los siguientes pasos:
<br />

1. Ingrese al  ```Menú de navegación/Navigation Menu``` ➡ ```Infraestructura VPC/VPC Infrastructure``` ➡ ```Almacenamiento/Storage``` ➡ ```Volúmenes de almacenamiento en bloques/Block storage volumes``` y de click en el botón ```Crear/To Create```.
<br />

2. Una vez cargue la nueva ventana complete la configuración del servicio de la siguiente manera:
* ```Nombre/Name```: indique un nombre exclusivo para su servicio.
* ```Grupo de recursos/Resource group```: especifique el grupo de recursos en el que va a trabajar.
* ```Ubicación/Location```: especifique el grupo de recursos en el que va a trabajar.

**Perfil de volumen/Volume profile**
* ```Niveles de IOPS/IOPS levels```: seleccione los niveles de IOPS con los que va a trabajar.
* ```Tamaño/Size```: especifique el tamaño, recuerde que debe ser un valor entre 10 y 2000 GB.
* ```Cifrado/Encryption```: seleccione el tipo de cifrado con lo que va a trabajar.
<br />

3. Para finalizar de click en el botón ```Crear/To Create```.
<br />

4. Espere unos minutos mientas se aprovisiona el servicio.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/CrearBlockStorageVPC.gif"></p>
<br />

## Adjuntar volumen de Block Storage a una VSI en VPC :cloud: :computer:
Para adjuntar el volumen de *Block Storage* a la *VSI* en *VPC*, complete los siguientes pasos:
<br />

1. En la pestaña ```Volúmenes de almacenamiento en bloques/Block storage volumes```, ubique el recurso, muévase hacia la derecha y de click en los tres puntos. Allí, seleccione la opción ```Conectar a instancia/Connect to instance```.
<br />

2. Posteriormente, seleccione la *VSI* con la que desea adjuntar el servicio y de click en el botón ```Conectar volumen```. Después de unos segundos le aparecerá un aviso indicando que el servicio se ha conectado. 
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/AdjuntarVSI-BS-VPC.gif"></p>
<br />

## Consultar volumen de Block Storage desde una VSI en VPC :mag: :computer:
El último paso consiste en consultar el volumen *Block Storage* desde la *VSI* que está en *VPC*. Para ello, se deben utilizar una serie de comandos que se presentan en los siguientes pasos:
<br />

1. Acceda a la *VSI* Linux mediante *SSH*. Para ello coloque:
```
ssh root@<ip_flotante>
```
Posteriormente, indique la contraseña establecida cuando realizó la respectiva configuración de su *VSI*.
<br />

2. Una vez se encuente dentro de la *VSI* obtenga información acerca de los dispositivos de bloque (*block*) que hay disponibles, utilice el comando:
```
lsblk 
```
Allí podrá identificar el volumen *Block Storage* con el nombre vdd y el tamaño determinado en la creación.
<br />

<p align="center"><img width="500" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/AccesoVSI.PNG"></p>
<br />

3. Posteriormente, para crear la partición del disco utilice:
```
fdisk -c /dev/vdd 
```
A continuación, le aparecerá un texto ```Command (m for help)```, allí utilice los siguientes comandos (en el mismo orden en que se indican) para completar el proceso de partición:
* Comando ```n``` para nueva particion.
* Comando ```p``` para partición primaria.
* Presione ```Enter``` cuando le aparezca ```Partition number```.
* Presione ```Enter``` cuando le aparezca ```First Sector``` en la opción ```default```.
* Presione ```Enter``` cuando le aparezca ```Last Sector``` en la opción ```default```.
<br />

<p align="center"><img width="500" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Particion1.PNG"></p>
<br />

* Comando ```t``` para cambiar la etiqueta y valor ```83``` que corresponde a Linux.
<br />

<p align="center"><img width="500" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Particion2.PNG"></p>
<br />

* Comando ```w``` para guardar los cambios.
<br />

<p align="center"><img width="300" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Particion3.PNG"></p>
<br />

4. El paso siguiente consiste en formatear el disco con el comando:
```
mkfs.ext4 /dev/vdd1
```
<br />

<p align="center"><img width="500" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Formatear1.PNG"></p>
<br />

5. Luego se debe montar el disco mediante los comandos:
```
mkdir /data1
mount /dev/vdd1 /data1
```
<br />

<p align="center"><img width="400" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/MontarDisk.PNG"></p>
<br />

5. Se debe configurar el montaje de forma permanente mediante:
```
vi /etc/fstab
```
<br />

<p align="center"><img width="300" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Configurar1.PNG"></p>
<br />

Dentro del editor agregue la línea:
```
"/dev/vdd1       /data1          ext4    defaults        0 0"
```
<br />

<p align="center"><img width="400" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Configurar2.PNG"></p>
<br />

Guarde los cambios, coloque ```:q``` y luego presione ```Enter``` para salir del editor.
<br />

6. Realice la respectiva verificación con los comandos:
```
umount /data1
df -h
mount -a
df -h
```
<br />

<p align="center"><img width="300" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Verificar1.PNG"></p>
<br />

7. Para finalizar, utilice los comandos ```lsblk``` y ```df -h``` para observar información sobre el disco y la partición.
<br />

<p align="center"><img width="500" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/DiskParticionVSI.PNG"></p>
<br />



## Referencias :pushpin:
**File Storage**
* <a href="https://cloud.ibm.com/docs/FileStorage?topic=FileStorage-getting-started">Getting started with File Storage</a>.
* <a href="https://cloud.ibm.com/docs/FileStorage?topic=FileStorage-orderingFileStorage&interface=ui#orderingFileStorageUI">Ordering File Storage</a>.
<br />

**Block Storage**
* <a href="https://cloud.ibm.com/docs/BlockStorage/index.html#getting-started-with-block-storage">Getting started with Block Storage</a>.
<br />

**Object Storage**
* <a href="https://cloud.ibm.com/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage">Getting started with IBM Cloud Object Storage</a>.
<br />

**Block Storage for VPC**
* <a href="https://cloud.ibm.com/docs/vpc?topic=vpc-creating-block-storage&interface=ui">Creating block storage volumes</a>.
* <a href="https://cloud.ibm.com/docs/vpc?topic=vpc-attaching-block-storage&interface=ui">Attaching a block storage volume to an instance</a>.
<br />

## Autores :black_nib:
Equipo *IBM Cloud Tech Sales Colombia*.
