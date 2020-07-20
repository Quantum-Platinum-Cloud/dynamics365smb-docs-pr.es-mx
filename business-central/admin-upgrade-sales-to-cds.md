---
title: Actualización de una integración con Dynamics 365 Sales | Microsoft Docs
description: Obtenga información sobre cómo preparar Dynamics 365 Business Central para integrarse con Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 2a5f58ac904ea05f4410ac9e1b804df1cb01c609
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410679"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a>Actualización de una integración con Dynamics 365 Sales
[!INCLUDE[d365fin](includes/d365fin_md.md)] se integra con [!INCLUDE[d365fin](includes/cds_long_md.md)], lo que facilita la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)], o incluso aplicaciones que crea usted mismo. Si está integrando por primera vez, le recomendamos que lo haga a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Para obtener más información, vea [Integración con Common Data Service](admin-common-data-service.md).

Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede continuar sincronizando datos utilizando su configuración. Sin embargo, si actualiza [!INCLUDE[d365fin](includes/d365fin_md.md)] o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

> [!NOTE]
> La reconexión a través de [!INCLUDE[d365fin](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga. Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a>Para actualizar su conexión para usar Common Data Service
1. Abra la página **Configuración de conexión de Microsoft Dynamics 365** y elija **Habilitar** para desactivar la conexión existente con [!INCLUDE[crm_md](includes/crm_md.md)].
2. Abra la página **Configuración de conexión de Common Data Service** y elija **Habilitar** para activar la conexión.
  
   Después de habilitar la conexión CDS, la solución de integración base de CDS de Business Central se implementa en Common Data Service.
3. Desinstalar la solución de integración de Microsoft Dynamics 365 Business Central de Dynamics 365 Sales siguiendo [Desinstalar o eliminar un tema de solución](/powerapps/developer/common-data-service/uninstall-delete-solution) 

4. En la página Configuración de conexión de Microsoft Dynamics 365, elija Habilitar para activar la conexión a [!INCLUDE[crm_md](includes/crm_md.md)].
  
   Después de habilitar la conexión a Sales, la solución de integración de Business Central se implementa en Sales. Esto permite la integración con entidades que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)], como órdenes de venta, cotizaciones y facturas.
5. Elija **Volver a implementar la solución de integración** para instalar y configurar la Solución de integración de Business Central actualizada.
6. En la página **Configuración de conexión de Sales**, elija **Usar configuración de sincronización predeterminada** para inicializar las asignaciones de tablas de integración para [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Consulte también
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Integración con Common Data Service](admin-common-data-service.md)