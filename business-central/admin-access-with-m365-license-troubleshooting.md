---
title: Solucionar problemas de acceso con licencias de Microsoft 365
description: Aprenda cómo puede solucionar los problemas de acceso a Business Central con solo una licencia de Microsoft 365.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams
ms.openlocfilehash: 750a78eb32568bea07d6851ff69c0b2cfea3ab49
ms.sourcegitcommit: 61fdaded30310ba8bdf95f99e76335372f583642
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745055"
---
# <a name="troubleshoot-access-with-microsoft-365-licenses"></a>Solucionar problemas de acceso con licencias de Microsoft 365

## <a name="symptoms"></a>Síntomas

Al acceder a un registro en Teams, se le muestra un mensaje de error en una pestaña o detalles de la tarjeta similar a:

"Esta página utiliza datos de tablas relacionadas a las que no tiene acceso. Para trabajar con todas las características de esta página, comuníquese con su administrador".

## <a name="cause"></a>Causa

Lo más probable es que le falten permisos de objeto para las tablas a las que se vincula la página actual o el registro.

## <a name="symptoms"></a>Síntomas

Se habilitó el acceso, pero los usuarios reciben un error de permiso al acceder a cualquier registro.

## <a name="cause"></a>Causa

Si habilita el acceso en el centro de administración de Business Central, pero no asigna permisos en la página Configuración de licencias, cualquiera que intente acceder a los registros de Business Central en Teams tendrá su registro de usuario aprovisionado sin permiso para ningún objeto. Business Central es seguro por diseño: los administradores primero deben configurar a qué datos se puede acceder en Teams. 

## <a name="resolution"></a>Resolución

La personalización de los permisos en la página Configuración de licencia solo afectará a los usuarios recién creados. También debe asignar los permisos que faltan a los usuarios que ya se han creado a través de la página de lista de usuarios. 

## <a name="symptoms"></a>Síntomas

Cuando comparto un vínculo en Teams, otros reciben el error "Al obtener acceso a Business Central con una licencia de Microsoft 365, solo se pueden ver datos en Microsoft Teams".

## <a name="cause"></a>Causa

Al compartir un vínculo de Business Central a un chat o canales de Teams, al navegar por un vínculo siempre se navegará fuera de Microsoft Teams cuando los datos ya no sean accesibles para una persona que tenga una licencia de Microsoft 365.

## <a name="resolution"></a>Resolución

Al compartir páginas o registros, incluya la versión preliminar del vínculo como una tarjeta o comparta los datos como una pestaña en el chat o el canal.

## <a name="see-also"></a>Consulte también .

[Acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md#minimum-requirements)  
[Configurar acceso con licencias de Microsoft 365](admin-access-with-m365-license-setup.md)  
[Integración de Business Central y Microsoft Teams](across-teams-overview.md)
[Compartir registros de Business Central y vínculos de página en Microsoft Teams](across-working-with-teams.md)  
[Solución de problemas de integración de Teams](admin-teams-troubleshooting.md)  