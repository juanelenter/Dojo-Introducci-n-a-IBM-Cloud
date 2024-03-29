# Dojo: Introducción a IBM Cloud. 

<p align="center">
  <img src="Images/logo.webp" width="600">   
</p> 

## Introducción al dojo 

El objetivo general de este dojo es familiarizar al lector con los conceptos fundamentales de la nube de IBM y poner en marcha algunas de las herramientas más sencillas y útiles de esta plataforma.   

Se realizarán cuatro laboratorios para poner en práctica estos conceptos y verificar la utilidad de la plataforma IBM Cloud.    

En el laboratorio 0 se hará un “reconocimiento de terreno” para comenzar a entender la plataforma y los servicios que ofrece. El laboratorio 1 consiste en desplegar una aplicación utilizando Cloud Foundry. En el laboratorio 2, se creará una aplicación utilizando el servicio: “Continuous delivery toolchain”. En el último laboratorio, se estudiará el uso del IBM Cloud Command Line Interface para manejar un servicio de la nube.     


## Índice  

* [**Introducción**](#introducción)  

  - [¿Qué es IBM Cloud?](#qué-es-IBM-cloud)  

  - [¿Qué se puede crear en IBM Cloud?](#qué-se-puede-crear-en-IBM-cloud)  

  - [Categorías de servicios](#categorías-de-servicios)  
  
  - [Regiones](#regiones)  

* [**Laboratorio 0: Descubriendo IBM Cloud**](#laboratorio-0-descubriendo-ibm-cloud)  

  - [Creación de una cuenta de IBM Cloud](#creación-de-una-cuenta-de-ibm-cloud)  

  - [Dashboard](#dashboard)   

  - [Menú superior](#menú-superior)   

  - [Tipos de cuenta](#tipos-de-cuenta)  
  
  - [Grupos](#grupos)


* [**Laboratorio 1: Crear una aplicación a partir de un application starter**](#laboratorio-1-crear-una-aplicación-a-partir-de-un-application-starter) 
 
   - [Introducción a Cloud Foundry](#introducción-a-cloud-foundry)  

   - [Creación de la aplicación](#creación-de-la-aplicación)  

* [**Laboratorio 2: Crear una aplicación utilizando IBM Cloud Continuous Delivery Toolchains**](#laboratorio-2-crear-una-aplicación-utilizando-ibm-cloud-continuous-delivery-toolchains)  

   - [DevOps y Continuous Delivery Toolchains](#devops-y-continuous-delivery-toolchains)  
  
   - [Despliegue de la aplicación](#despliegue-de-la-aplicación)  

* [**Laboratorio 3: Manejar un servicio a través de IBM CLI**](#laboratorio-3-manejar-un-servicio-a-través-de-ibm-cli)  

   - [Command Line Interface (CLI)](#command-line-interface-cli)  

   - [Despliegue de la aplicación](#despliegue-de-la-aplicación-desde-cli)  


# Introducción   
  
¿Qué es IBM Cloud? ¿Cómo surgió? ¿Para qué se utiliza? ¿Cómo se diferencia de otras plataformas similares cómo AWS, Azure y Google Cloud?    

En esta sección intentaremos responder a estas preguntas, dando un marco teórico a los laboratorios que siguen.   

### ¿Qué es IBM Cloud? 

En 2014, IBM lanzó Bluemix (hoy IBM Cloud): una plataforma que ofrece servicios a través de la red. En esta plataforma, el usuario puede acceder a tres tipos de servicios: infrastructure as a service (IaaS), software as a service (SaaS) y platform as a service (PaaS), pagando únicamente por los recursos que consume. La principal diferencia entre estos servicios es la cantidad de interacción que se tiene con el hardware:    


<p align="center">   
   <img src="Images/modelos_de_cloud.png" width="500">   
 </p>   


Además, en estos tres tipos de utilización de la nube, el proveedor efectua un distinto porcentaje de las tareas, alivianando más o menos el trabajo del cliente. 

  <p align="center">   
   <img src="Images/responsabilities.PNG" width="600">   
 </p>   

 

Si bien la computación en la nube tiene varias desventajas cómo la extrema centralización de los recursos y la dependencia de la conexión a internet, estas limitantes son ampliamente superadas por la escalabilidad, seguridad, fiabilidad y flexibilidad que ofrece esta plataforma.    


### ¿Qué se puede crear en IBM Cloud? 

IBM Cloud permite crear los siguientes componentes: 

 **Aplicaciones**, es decir programas  como aplicaciones web y móviles que los desarrolladores crean en varios entornos (ej: Cloud Foundry). 

**Servicios**, es decir una extensión de una funcionalidad “lista para ser utilizada” alojada en IBM Cloud. 

### Categorías de servicios 

IBM Cloud ofrece servicios, tanto propios como de terceros, que pueden utilizarse para el armado de su aplicación. Estos servicios se pueden dividir en 4 grandes cateogrías: 


 <p align="center">   
   <img src="Images/services.PNG" width="700">  
</p>   
 
### **Watson**  

Permite agregarle a su aplicación el poder de la inteligencia artificial (AI) a través de APIs de reconocimiento del habla, visual y procesamiento del lenguaje natural. 


### **Data & Analysis**  

Ayuda a obtener datos de bases de datos en la nube integradas, construir aplicaciones basadas en datos y para el análisis de estos. 

### **Developer services** 

Podemos encontrar las siguientes sub-categorías:  

* **Integration services**:  

    * **APIs**: Servicios para crear, administrar y correr APIs  

    * **Integrate**: Servicios para acceder a los workloads que se ejecutan en el entorno local de la organización, como puede ser API Connect.  

* **Mobile**: Servicios que utilizan la infraestructura backend móvil para crear, monitorear y probar aplicaciones moviles  


* **Internet of Things**: Servicios para comunicarse con dispositivos conectados, sensores y más  

* **Functions**: Basado en Apache OpenWhisk, brinda servicios para desarrollar código liviano que se ejecuta bajo demanda.  

* **Application Services**: Servicios como puede ser Blockchain, Event Streams, entre otros  

* **DevOps**: Herramientas que ayudan a innovar creando aplicaciones de forma mas rápida y económica  
  
* **Security**: Servicios para brindar seguridad a las aplicaciones  

  

### **Infrastructure services**  

Podemos encontrar estas sub-categorías: 

* **Computo**: bare-metal servers, virtual servers, serverless computing, contenedores  

* **Network**: content delivery network (CDN), virtual private network (VPN) tunnels and firewalls    

* **Almacenamiento** 

* **Seguridad**:  Servicios de seguimiento de actividad e identidad  

### Regiones 

Actualmente IBM Cloud se encuentra en 18 zonas en 6 regiones diferentes situadas en Estados Unidos (Dallas y Washington, DC), Alemania, Reino Unido, Japon y Australia. Al desplegar tu aplicación o infraestructura en la nube de IBM, es importante tener en cuenta estas regiones. 

Estas son algunas recomendaciones a tener en cuenta: 

- Para una baja latencia de la aplicación, es recomendable seleccionar la región más cercana a sus usuarios. 

- Para cumplir con los requisitos de seguridad de datos de ciertos países, seleccione la región donde debe almacenar los datos de la aplicación. 

- Para lograr una alta disponibilidad, se recomienda seleccionar múltiples regiones. Si su aplicación falla en una región, todavía está disponible en otra región. 

**Nota**: No todos los servicios de IBM Cloud están disponibles en todas las regiones. 


**Cómo cambiar de región** 

Por defecto, IBM Cloud le asigna la región más cercana a su ubicación. Para cambiar la región hacemos uso de la herramienta CLI (Command Line Interface), ejecutando los siguientes comandos:  
(Es necesario haber descargado la herramienta CLI, para ver cómo instalarla dirigirse a [CLI](#command-line-interface-cli)
Comando que muestra tu actual región 

``` 

Ibmcloud cs region 

``` 

Comando para listar las regiones disponibles 

```  

Ibmcloud cs regions  

``` 

Comando para cambiar de región, donde “regionname” es el nombre de la región a la cual querés cambiar, por ejemplo us-south 

```  

Ibmcloud cs region-set regionname 

``` 

*Bottom line:*   


El concepto de **computación en la nube** hace referencia al “suministro de recursos informáticos flexibles y a petición, desde aplicaciones hasta centros de datos, a través de Internet y con un modelo de pago según uso.” (ref: https://www.ibm.com/es-es/cloud/learn/cloud-computing).    
  

Las clouds flexibilizan, automatizan y simplifican una enorme cantidad de procedimientos que anteriormente debían ser gestionados internamente. El concepto de computación en la nube fue introducido en los 70’ por John McCarthy, sin embargo, la primera nube de uso masivo: AWS, fue lanzada por Amazon en 2006. La nube de IBM, lanzada 8 años después, capta el 8% del cloud computing mundial.   

# Laboratorio 0: Descubriendo IBM Cloud   

Antes de empezar a utilizar los servicios que ofrece IBM Cloud es necesario abrir una cuenta.    

### Creación de una cuenta en IBM Cloud  

Por defecto, IBM Cloud crea una cuenta **"Lite"**. Este tipo de cuenta no tiene costo y te permite utilizar la mayoria de los servicios de la nube, con algunas limitaciones. Más adelante veremos los diferentes [tipos de cuentas](#tipos-de-cuenta).  

  
La creación de la cuenta es un procedimiento muy sencillo:  

* Entre a  https://cloud.ibm.com   

<p align="center"> 
  <img src="Images/create.png" width="500">   
</p>   

* Cree su cuenta accediendo a "Create an IBM Cloud account" y complete los datos personales.   


<p align="center">   
  <img src="Images/form.PNG" width="700">   
</p>   

* Recibirá un mail a la dirección de correo indicada anteriormente donde deberá realizar la confirmación de la cuenta.   


<p align="center">
  <img src="Images/confirm.png" width="700"> 
</p>   

*  Una vez hecha la verificación, inicie sesión.    

<p align="center">  
  <img src="Images/session.png" width="700">  
</p>  

### Dashboard  

Lo primero que verá una vez iniciada la sesión será un Dashboard.   

<p align="center">   
  <img src="Images/dashboard.PNG" width="700">   
</p>   
  

Cada usuario de IBM Cloud puede personalizar su dashboard. Por defecto, allí encontraremos los siguientes elementos:   
  

Elemento             | Función  
---------------------|----------------------------------------  
**Resource summary** | Visualizar los recursos que estan siendo actualmente utilizados en esta cuenta 
**Planned maintenance** | Ver los eventos de mantenimiento planificados  
**Location status** | Información sobre el estado de los data centres por continente  
**Apps** | Historial de apps creadas.  
**Support cases** | Resumen de los casos de soporte actualmente abiertos 
**Usage** | Historial del uso de la cuenta en IBM Cloud 
**User access** | Listados los usuarios con acceso a esta cuenta  
**Learn** | Acceso a tutoriales e información general acerca de IBM Cloud  
**Recommended offerings** | Recomendaciones de servicios  


### Menú superior  

Otra sección esencial dentro de la página IBM Cloud es el Catálogo. En esta podremos encontrar todos los servicios que ofrece la nube, separados en categorías.  Cada servicio tiene cuatro posibles etiquetas:   

**Lite**: refiere a servicios que tienen una opción de prueba gratuita 

**IBM**: refiere a servicios propios de IBM   

**Community**: refieren a los servicios de la comunidad, externos a IBM   

**IAM enabled**: refieren a los servicios que siguen el protocolo IAM de autentificación y control de acceso a los recursos en la nube. (IAM = Identity and Access Management). (Para comprender en profundidad el funcionamiento del servicio IAM visitar el siguiente link: https://cloud.ibm.com/docs/iam?topic=iam-userroles&locale=en-us.)   

<p align="center">   
<img src="Images/catalog.png" width="700">   
</p>   

Desde el menú superior también se puede a acceder a las secciones: **Support**, **Docs** y **Manage**. En **Support** se encuentran las FAQs y las soluciones a los problemas más típicos mientras que en **Doc**s está la documentación de la IBM Cloud, acompañada de algunos tutoriales y guías para poner en marcha algunos servicios básicos. Desde **Manage** podremos administrar y configurar nuestra cuenta.  

### Tipos de cuenta  

Es importante saber que hay **tres tipos de cuenta** dentro de IBM Cloud: **Lite**, **Pago según uso** y **Suscripción**. Como se mencionó anteriormente, al registrarse, Lite es la opción gratuita por defecto. En cambio, las otras dos son pagas, ofrecen diferentes características y una experiencia más completa.  

En la siguiente tabla podemos ver la comparación entre los tipos de cuentas.  

<p align="center">   
<img src="Images/suscripciones.PNG" width="700">   
</p>   

**Actualizar la cuenta**   

Para actualizar la cuenta a una de **Pago según uso** o **Suscripción**:  

Vaya a Manage > Account > Account settings. 

Allí podrá encontrar las dos opciones y elegir la que desee.  

<p align="center">   
  <img src="Images/upgrade.PNG" width="700">   
</p>  

La pagina cuenta con un **cost estimator**, el cual se encuentra en la barra del menú superior. Esta opción permite seleccionar, desde el catálogo, los servicios que estimas que utilizarás para así poder pagar de acuerdo al uso, en el caso de una cuenta **Pago según uso**.  

### Grupos 
Los grupos son una forma de organizar los recursos de su cuenta. Esta forma de organización permite rápidamente la repartición de accesos y roles a los distintos recursos. 
<p align="center">   
  <img src="Images/grupos.png" width="700">   
</p>  

Cuando cree un servicio, podrá indicar a grupo pertence dicho servicio.
<p align="center">   
  <img src="Images/grupos2.png" width="700">   
</p>  

Un pequeño resumen de lo que vimos hasta ahora: https://www.youtube.com/watch?v=VXqbRNwXC2A.   

 
### **IMPORTANTE**: Los siguientes laboratorios son guías detalladas: un paso a paso de algunas funcionalidades simples disponibles en IBM Cloud. Es de vital importancia que **NO** siga ciegamente las instrucciones. Salga del camino, explore desviaciones, equivóquese, borre todo, vuelva a comenzar y analice hasta el fondo los conceptos introducidos.    

Corto video introductorio al desarrollo en la nube: https://www.youtube.com/watch?time_continue=52&v=Bsy6mhRc7ZA   


# Laboratorio 1: Crear una aplicación a partir de un application starter

En esta sección veremos cómo crear una aplicación utilizando Cloud Foundry. 

### Introducción a Cloud Foundry
Este es una PaaS (plataforma como servicio), open source y gratuita. Cloud Foundry pone a disposición un entorno preparado para la ejecución de aplicaciones web.   

<p align="center">   
   <img src="Images/cfexplicacion.PNG" width="600">   
 </p>   

Utilizar Cloud Foundry tiene los siguientes beneficios: 

<p align="center">   
  <img src="Images/xqcf.PNG" width="700">   
</p> 

### Creación de la aplicación
Comencemos con la creación de la aplicación. 
 
* Acceder al Catálogo de servicios de IBM Cloud y recorrerlo hasta llegar a la sección Cloud Foundry. 

 <p align="center">   
  <img src="Images/catcf.png" width="700">   
</p> 

A modo de ejemplo utilizaremos Liberty for Java, pero puede elegir cualquier opción.   

* Seleccione una opción, debería ver el siguiente formulario: 

<p align="center">   
   <img src="Images/CreateCloudFoundryApp.PNG" width="700">   
 </p>   


* Elija un nombre para su aplicación y luego pulse **"Create"**. (El host name debe ser único, se recomienda agregarle al nombre de la aplicación sus iniciales o el nombre de la empresa acompañado de la fecha de creación de esta.) 

<p align="center">   
   <img src="Images/CreateCloudFoundryApp.PNG" width="700">   
 </p>   

* Se desplegará un dashboard con información acerca de la aplicación.   

  <p align="center">   
   <img src="Images/runningcf.png" width="700">   
 </p>   


* **Getting Started**: permite seguir la guía paso a paso proporcionada o directamente descargar el código de la aplicación.    

* **Sección Runtime**: sirve para visualizar la cantidad de instancias actualmente creadas y la cantidad de memoria utilizada por cada instancia, pudiendo aumentar y disminuir las cantidades en ambos casos.   

* **Sección Logs**:  da la posibilidad de ver los mensajes mientras la aplicación se va armando, permitiendo así entender en caso de error. 
  

<p align="center">   
   <img src="Images/Running.PNG" width="700">   
 </p>  

Al finalizar el despliegue de la aplicación (pasó del estado Starting a Running) se habilitará la opción *Visit App URL* donde podremos acceder a nuestra aplicación.   

<p align="center">   
   <img src="Images/HelloWorld.PNG" width="700">   
</p>   

Por último, desde **"Resource List"** podrá borrar la aplicación, haciendo lugar para el Laboratorio 2.

# Laboratorio 2: Crear una aplicación utilizando IBM Cloud Continuous Delivery Toolchains

* **Objetivo**:  En esta sección veremos cómo crear una aplicación utilizando IBM Cloud Continuous Delivery Toolchains a partir de un repositorio de GitHub ya existente. Utilizaremos como ejemplo una aplicación construida en NodeJS la cual utiliza una base de datos Cloudant NoSQL para organizar archivos.   

#### Devops y Continuous Delivery Toolchains  

¿ Qué es **IBM Cloud Continuous Delivery Toolchains** ? ¿ En que contexto se utiliza ?  

Para comprender este servicio se debe manejar el concepto de *“DevOps”*.  

El término *DevOps* proviene de fusionar las palabras “Development” y “Operations”. DevOps hace referencia a la unión de los equipos de Desarrollo y Operaciones para mantener el ciclo de vida de un programa, desde la escritura del código hasta el despliegue. En pocas palabras: 

- DevOps es una **metodología** para creación de software. 

- DevOps se basa en la integración entre desarrolladores de software y administradores de sistemas. 

- DevOps permite fabricar software más rápidamente, con mayor calidad, menor coste y una altísima frecuencia de releases. 

Entonces, volviendo a la pregunta inicial, IBM Cloud Continuous Delivery provee herramientas para construir, testear y desplegar aplicaciones usando herramientas y prácticas de DevOps. Este servicio permite:  

- Integrar herramientas que soportan el desarrollo, despliegue de una aplicación. 

- Usar pipelines automatizadas para efectuar un “continuous delivery”. 

- Usar el web IDE para subir el código desde cualquier lugar. 

- Colaborar con un equipo usando Git para controlar las versiones del programa.   

<p align="center">   
  <img src="Images/deliverytoolchain.PNG" width="500">   
</p>   

Un posible esquema de funcionamiento de la herramienta: 

<p align="center">   
  <img src="Images/esquemafunctoolchain.PNG" width="500">   
</p>   

 

(ref: http://www.redbooks.ibm.com/redbooks/pdfs/sg248374.pdf) 

### Despliegue de la aplicación

Ahora si estamos listos para comenzar con la parte práctica del laboratorio. 

 * Primero, debemos acceder al repositorio http://github.com/ibmecod/nodejs-cloudant.   

 <p align="center">   
   <img src="Images/github.PNG" width="700">   
 </p>   

 * Hacer click en  **Deploy to IBM Cloud**. Esto desplegará la aplicación automáticamente en el entorno de IBM Cloud.   

 <p align="center">   
  <img src="Images/deploy.PNG" width="700">   
</p>   

  
<p align="center">   
  <img src="Images/deploy2.PNG" width="700">   
 </p>   


* Seleccionar la opción **Delivery Pipeline** de las herramientas de Integración   

  

<p align="center"> 
  <img src="Images/tool integrations.PNG" width="700">   
</p>   
  

Dentro de Delivery Pipeline debemos llenar los siguientes campos   

<p align="center">   
  <img src="Images/deliveryPipeline.PNG" width="700">   
</p>   



Si no contamos con una **IBM Cloud API key**,  hacer click en el botón **Create**. Esto creará una API key automáticamente.   

  

<p align="center">   
  <img src="Images/apikey.PNG" width="700">   
</p>   

Finalmente, hacemos click en el botón Deploy   
  

<p align="center">   
  <img src="Images/toolchains.PNG" width="700">   
</p>   
  

Una vez allí, seleccionamos el icono de **Delivery Pipeline** y una vez que finalice la **Deploy Stage** (estado: Stage Passed), tendremos el link para acceder a nuestra aplicación   
  

<p align="center">  
  <img src="Images/deploystage.PNG" width="700">  
</p>  

<p align="center">   
 <img src="Images/aplicacion.PNG" width="700">  
</p>   

Al igual que en el Laboratorio 1 es conveniente eliminar el servicio ya que no lo vamos a utilizar.

# Laboratorio 3: Manejar un servicio a través de IBM CLI 

 ### Command Line Interface (CLI) 

Además de tener la interfaz web, los servicios de la nube se pueden manejar desde una terminal. La herramienta de IBM para realizar esta tarea es IBM CLI.  

Para Instalar la última versión de IBM Cloud CLI ejecutar los siguientes comandos: 

En Mac y Linux: 
 

 ``` curl -sL https://ibm.biz/idt-installer | bash ``` 

En Windows: 
 

 ``` [Net.ServicePointManager]::SecurityProtocol = "Tls12"; iex(New-Object Net.WebClient).DownloadString('https://ibm.biz/idt-win-installer') ``` 

 

### Despliegue de la aplicación desde CLI 

A continuación, se detallan los simples pasos que hay que seguir para desplegar una aplicación desde la terminal.   


* Descargar el repositorio de la aplicación de ejemplo a través del siguiente link  http://github.com/ibmecod/nodejs-cloudant y guardarlo en una nueva carpeta.   


* Abrir una terminal y navegar hasta la carpeta con los archivos de la aplicación de ejemplo.   
  
* Ingrese a su usuario con el siguiente comando  

``` 

ibmcloud login -a https://api.ng.bluemix.net  

``` 


* Cree un instancia del servicio **"Cloudant Database"** con el siguiente comando. (Cloudant es un servicio de base de datos distribuida no relacional). 
  
``` 

imbcloud service offerings 

``` 

* Cree una instancia de **"Cloudant NoSQL database"** con el siguiente comando  

``` 

ibmcloud service create cloudantNoSQLDB Lite myCloudantDB 

``` 

* Haga un "push" a la nube de su aplicación con el siguiente comando: 

``` 

ibmcloud app push favapp-tor-0517 -c "node app.js" -m 128M --no-manifest --no-start 

``` 

Se le denomina “bind” a la asociación de dos o más programas.  

* Efectuar un bind del servicio a la aplicación (reemplace favapp-tor-05017 por el nombre que le quiera dar a su aplicación):  

``` 

ibmcloud service bind favapp-tor-0517 myCloudantDB 

``` 


* Lance la aplicación:  

``` 

ibmcloud app start favapp-tor-0517 

``` 

Una vez desplegada la aplicación entre a su cuenta de ibm y vaya a “Resource list”, bajo Cloud Foundry apps debería aparecer su aplicación.  

<p align="center">    
  <img src="Images/cli_app.PNG" width="700">    
</p>    


Un instructivo más detallado sobre la creación de apps usando CLI:  https://cloud.ibm.com/docs/apps?topic=creating-apps-create-deploy-app-cli#create-deploy-app-cli  

  

Para seguir profundizando: https://www.youtube.com/watch?v=z-ByHuI41dU.  

# Conclusiones  

Esperamos que este dojo les haya sido útil para dar sus primeros pasos en IBM Cloud. En esta etapa usted debería: entender los fundamentos de la computación en la nube y de la plataforma de IBM, ser capaz de crear una aplicación utilizando un application starter o la herramienta Continuous Delivery Toolchain y debería ser capaz de manejar estos servicios básicos a través de la IBM CLI.  

Probablemente hayan notado que es una plataforma inmensa, con 190 servicios y mucho por explorar. A continuación, les brindamos algunos links para profundizar su conocimiento. También recomendamos realizar los tutoriales disponibles directamente en la plataforma de IBM Cloud. 

  http://www.redbooks.ibm.com/redbooks/pdfs/sg248374.pdf 

https://www.youtube.com/watch?v=vLMX9gyTEr4 
