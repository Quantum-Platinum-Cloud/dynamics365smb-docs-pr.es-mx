---
title: Tareas administrativas en Business Central | Documentos de Microsoft
description: "Algunas tareas de Business Central requieren administración y configuración centrales. Consulte cuáles son aprenda y qué hacer."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 05/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 93eced90155b9172595561bfc5b80c3c49ca11bc
ms.contentlocale: es-mx
ms.lasthandoff: 05/15/2018

---
# <a name="administration"></a>Administración
Normalmente, un rol de la empresa se encarga de las tareas de la administración central. El alcance de estas tareas puede depender del tamaño de la empresa, así como de las responsabilidades laborales del administrador. Estas tareas pueden incluir la administración de la sincronización de base de datos de las colas de proyectos y de correo electrónico, la configuración de usuarios, la personalización de la interfaz de usuario y la administración de las claves de cifrado.  

Es importante introducir los valores de configuración correctos desde el principio para el éxito de cualquier nuevo software de negocio. [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye varias guías de configuración que le ayudan a configurar datos fundamentales. Para obtener más información, consulte [Configurar Business Central](setup.md).

Tanto si utiliza RapidStart Services para implementar los valores de configuración como si los introduce manualmente en la nueva empresa, puede sustentar su decisiones de configuración con algunas recomendaciones generales para los campos de configuración seleccionados que son conocidos porque pueden provocar que la solución resulte ineficaz si están definidos forma incorrecta.  

Un superusuario o un administrador puede configurar el marco de intercambio de datos para que los usuarios puedan exportar e importar los datos de los archivos de banco y de nómina, por ejemplo, para diferentes procesos de tesorería.

> [!NOTE]
> Puede configurar una nueva empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)] con RapidStart Services, que es una herramienta diseñada para acortar los tiempos de implementación, mejorar la calidad de la implementación, introducir un método de repetición para las implementaciones y mejorar la productividad mediante la automatización y simplificación de las tareas periódicas. Para obtener más información, consulte ## [Configuración de una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Agregar usuarios, gestionar permisos y gestionar el acceso a los datos, asignar roles.|[Comprender Perfiles y Áreas de tareas](admin-users-profiles-roles.md)|  
|Asignar permisos a los usuarios, modificar conjuntos de permisos y agrupar usuarios por permisos.|[Gestionar usuarios y permisos](ui-how-users-permissions.md)|
|Clasifique la confidencialidad de los datos para los campos, de modo que pueda responder a las solicitudes de los asuntos relacionadas con sus datos personales.|[Clasificar confidencialidad de datos](admin-classifying-data-sensitivity.md)|
|Responda a las solicitudes de los asuntos relacionadas con sus datos personales.|[Respuesta a las solicitudes de datos personales](admin-responding-to-requests-about-personal-data.md)|
|Configurar una nueva unidad de negocio mediante plantillas|[Crear nuevas en empresas](about-new-company.md)|
|Cambie los campos y las acciones que se muestran en la interfaz de usuario para adaptarla a los procesos de la empresa. |[Personalización de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md) |
|Realizar un seguimiento de todas las modificaciones directas que realicen los usuarios a los datos de la base de datos para identificar el origen de los errores y de las modificaciones en los datos.|[Registrar cambios](across-log-changes.md)|  
|Introducir solicitudes únicas o periódicas para ejecutar informes o unidades de código.|[Usar colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)|  
|Administre, elimine, o comprima los documentos|[Eliminar documentos](admin-manage-documents.md)|  
|Exponga las páginas, las unidades de código y las consultas como servicios web.|[Publicar un servicio web](across-how-publish-web-service.md)|
|Como parte de la creación de aplicaciones de Connect entre soluciones de [!INCLUDE[d365fin](includes/d365fin_md.md)] y de terceros a través de las API de REST, defina plantillas que se utilizan para completar propiedades vacías en una entidad cuando crea una acción POST a través de una API.|[Configuración de plantillas API](admin-configuring-api-template.md)|

## <a name="see-also"></a>Consulte también
[Funciones empresariales](across-business-functionality.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Introducción](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
