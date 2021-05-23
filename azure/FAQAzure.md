# Azure  

1. [¿Qué es Azure?](#qué-es-azure)
2. [¿Cómo accedo, gestiono los recursos en Azure?](#cómo-gestiono-los-recursos-en-Azure)
3. [¿Qué niveles de servicio puedo acceder?](#qué-niveles-de-servicio-puedo-acceder)
4. [¿Cómo se organizan los recursos en Azure?](#cómo-se-organizan-los-recursos-en-Azure)

## Enlaces de interes

- [Virtual Networks](https://docs.microsoft.com/en-us/azure/virtual-network/)
- Command line
    - [Assign Azure roles using Azure PowerShell](https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-powershell)
    - [Assign Azure roles using Azure CLI](https://docs.microsoft.com/en-us/azure/role-based-access-control/role-assignments-cli)

## ¿Qué es Azure?

Azure es la plataforma en la nube de Microsoft.

## ¿Cómo accedo, gestiono los recursos en Azure?

Existen diversas formas de acceder y gestionar los recursos en Azure
1. [***Azure Portal:***](https://docs.microsoft.com/en-us/azure/developer/python/cloud-development-provisioning#azure-portal)
    - Es la interfaz web.
2. [***Azure Powershell:***](https://docs.microsoft.com/en-us/powershell/azure/?view=azps-5.9.0)
    - Interfaz por línea de comandos, utilizando la consola de powershell.
3. [***Azure CLI:***](https://docs.microsoft.com/en-us/cli/azure/)
    - Interfaz por línea de comandos, utilizando comandos az al estilo bash.
4. [***Azure Cloud Shell:***](https://docs.microsoft.com/en-us/azure/cloud-shell/overview)
    - Interfaz de línea de comando, utilizando  los comandos az desde el propio navegador, sin necesidad de instalar la consola en local.
    - Se dispone tanto de la opción powershell como bash (comandos az)
5. [***Azure libraries (SDK):***](https://azure.microsoft.com/en-us/downloads/)
    - Es la interfaz programática. Disponemos de diversos lenguajes de programación 
        - [.net](https://docs.microsoft.com/en-us/dotnet/azure/sdk/azure-sdk-for-dotnet)
        - [javascript](https://docs.microsoft.com/en-us/azure/developer/javascript/?view=azure-node-latest)
        - [python](https://docs.microsoft.com/en-us/azure/developer/python/?view=azure-python)        
        - [go](https://aka.ms/azsdk/go/docs)
6. [***Azure Rest API***]()
    - > [The Azure REST API is Azure's programmatic interface, provided via secure REST over HTTP because Azure's data centers are all inherently connected to the Internet.](https://docs.microsoft.com/en-us/azure/developer/python/cloud-development-provisioning#azure-rest-api-and-azure-libraries)

## ¿Qué niveles de servicio puedo acceder?
    - IaaS (Infraestructure as a Service)
    - PaaS (Platform as a Service)
    - SaaS (Software as a Service)

## ¿Cómo se organizan los recursos en Azure?
    - Cada vez que se crea un recurso siempre hay que identificar tres niveles de agrupamiento    
        - Suscripciones
        - Grupos de recursos
        - Regiones
    
## ¿Un recurso puede definirse en dos grupos diferentes?
    - No, los recursos solo existen en el grupo de recursos donde se crea.
