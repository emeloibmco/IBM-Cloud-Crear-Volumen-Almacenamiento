# IBM Cloud - Crear Volumen de Almacenamiento ☁💾

## Índice  📰
1. [Pre-Requisitos](#Pre-Requisitos-pencil)
2. [Crear servicio de almacenamiento File Storage](#Crear-servicio-de-almacenamiento-File-Storage-card_file_box)
3. [Consultar servicio de almacenamiento File Storage](#Consultar-servicio-de-almacenamiento-File-Storage-mag-card_file_box)
4. [Crear servicio de almacenamiento Block Storage](#Crear-servicio-de-almacenamiento-Block-Storage-package)
5. [Consultar servicio de almacenamiento Block Storage](#Consultar-servicio-de-almacenamiento-Block-Storage-mag-package)
6. [Crear servicio de almacenamiento Object Storage](#Crear-servicio-de-almacenamiento-Object-Storage-file_cabinet)
7. [Consultar servicio de almacenamiento Object Storage](#Consultar-servicio-de-almacenamiento-Object-Storage-mag-file_cabinet)
8. [Crear servicio de almacenamiento Block Storage for VPC](#Crear-servicio-de-almacenamiento-Block-Storage-for-VPC-cloud-package)
9. [Referencias](#Referencias-pushpin)
10. [Autores](#Autores-black_nib)


## Pre-requisitos :pencil:
* Contar con una cuenta en <a href="https://cloud.ibm.com/"> IBM Cloud </a>.
<br />

## Crear servicio de almacenamiento File Storage :card_file_box:
Para crear el servicio de almacenamiento *File Storage* en su cuenta de *IBM Cloud* complete los siguientes pasos:
<br />

1. Acceda al catálogo y busque el servicio *File Storage* en la categoría del Almacenamiento.
<br />

2. Seleccione el servicio *File Storage*. Posteriormente, se abrirá una ventana en la cual e muestra información relacionada con el servicio. De click en el botón ```Crear/To Create```.
<br />

3. Une vez cargue la nueva ventana complete la configuración del servicio de la siguiente manera:
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

## Consultar servicio de almacenamiento File Storage :mag: :card_file_box:
Para consultar el servicio de almacenamiento *File Storage* implementado en la sección anterior, de click sobre su recurso. Luego podrá observar las diferentes opciones que aparecen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/ConsultarFileStorage.gif"></p>
<br />

## Crear servicio de almacenamiento Block Storage :package:
Para crear el servicio de almacenamiento *Block Storage* en su cuenta de *IBM Cloud* complete los siguientes pasos:
<br />

1. Acceda al catálogo y busque el servicio *Block Storage* en la categoría del Almacenamiento.
<br />

2. Seleccione el servicio *Block Storage*. Posteriormente, se abrirá una ventana en la cual e muestra información relacionada con el servicio. De click en el botón ```Crear/To Create```.
<br />

3. Une vez cargue la nueva ventana complete la configuración del servicio de la siguiente manera:
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

> NOTA: En caso de no contar con los permisos para ver el recurso en la ```Lista de Recursos/Resource List```, puede ver el servicio de almacenamiento ingresando por ```Menú de navegación/Navigation Menu``` ➡ ```Infraestructura Clásica/Classic Infrastructure``` ➡ ```Almacenamiento/Storage``` ➡ ```File Storage```, como se muestra en la siguiente imagen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/AccesoBlocktStorage.gif"></p>
<br />

## Consultar servicio de almacenamiento Block Storage :mag: :package:
Para consultar el servicio de almacenamiento *Block Storage* implementado en la sección anterior, de click sobre su recurso. Luego podrá observar las diferentes opciones que aparecen.
<br />

<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/ConsultaBlockStorage.gif"></p>
<br />

## Crear servicio de almacenamiento Object Storage :file_cabinet:
<p align="center"><img width="700" src="https://github.com/emeloibmco/IBM-Cloud-Crear-Volumen-Almacenamiento/blob/main/Im%C3%A1genes/Crear%20Object%20Storage.gif"></p>
<br />

## Consultar servicio de almacenamiento Object Storage :mag: :file_cabinet:
<br />

## Crear servicio de almacenamiento Block Storage for VPC :cloud: :package:
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
* <a href="https://cloud.ibm.com/docs/vpc?topic=vpc-attaching-block-storage&interface=ui">Attaching a block storage volume</a>.
<br />

## Autores :black_nib:
Equipo *IBM Cloud Tech Sales Colombia*.
