---
title: "Elegir la experiencia de usuario para mostrar u ocultar características avanzadas | Documentos de Microsoft"
description: "Obtenga información sobre lo que significan las capas de experiencia de usuario Básico y Esencial para la interfaz de usuario, las áreas de aplicación y su empresa."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/17/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: dc7e739bc2b8ac9e8efce3a0f52acb945352416e
ms.openlocfilehash: 0a94d94e58b2aa3f04639a00904b5370c91b1132
ms.contentlocale: es-mx
ms.lasthandoff: 04/19/2018

---
# <a name="changing-which-features-are-displayed"></a>Cambiar las funciones que se muestran
[!INCLUDE[d365fin](includes/d365fin_md.md)] está diseñado para ayudarle a dirigir su empresa, independientemente de la línea de negocio en la que se encuentre. En el núcleo de [!INCLUDE[d365fin](includes/d365fin_md.md)], se encuentran los informes financieros y los procesos de ventas y compras. Agregue experiencias según las necesidades de su negocio con extensiones de AppSource o cambiando la configuración de Experiencia para su empresa. Para obtener más información, vea [Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md), o la sección siguiente "Elegir una experiencia de usuario para mostrar u ocultar características".

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Elegir una experiencia de usuario para mostrar u ocultar características
La experiencia de usuario determina qué parte de la funcionalidad básica está disponible cuando usted y sus compañeros usan [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede elegir la experiencia de usuario de su empresa en la ventana **Información empresa**, en el campo **Experiencia**.

> [!NOTE]  
> Esta esta configuración se aplica a todos los usuarios de la empresa. Los usuarios pueden personalizar aún más su propia experiencia cambiando el diseño y el contenido de la página. Para obtener más información, vea [Personalización del área de trabajo y las páginas](ui-personalization-user.md).  

La siguiente tabla enumera la experiencias que están disponibles actualmente.

| Experiencia | Impacto en la interfaz de usuario |
| --- | --- |
| **Básico** |Muestra solo las acciones y los campos principales dentro de la funcionalidad empresarial más común, como ventas, compras, inventario y finanzas. |
| **Esencial** |Muestra todas las acciones y campos para todas las funcionalidades de negocio comunes.|
| **Prima de emisión** |Muestra todas las acciones y campos para todas las funcionalidades empresariales, incluidas las de Fabricación y Gestión de servicios.|

> [!NOTE]  
> Las experiencias que se pueden seleccionar en [!INCLUDE[d365fin](includes/d365fin_md.md)] dependen de su licencia de solución, denominada un plan. Para obtener información acerca de los planes de **Esencial** y **Premium**, consulte [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) en el sitio de marketing de Microsoft Dynamics 365.

> [!IMPORTANT]  
> Todos los usuarios habituales de una solución deben tener asignado el mismo plan, Essential o Premium, antes de poder seleccionar esa experiencia para la empresa. En consecuencia, un usuario no puede acceder a las funciones Premium si uno o más usuarios solo pueden acceder a las funciones Essential. Este no es el caso para los usuarios no regulares del tipo Miembro del equipo, Administrador interno, Contable externo y Administrador delegado, a quienes se les puede asignar un plan diferente al de otros usuarios en la solución.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Habilitar características premium después de actualizar un plan
Los usuarios se asignan a planes en el Centro de administración de Office 365 en relación con el trabajo general para crear los usuarios de Business Central. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

A continuación, puede definir a qué funciones y ventanas específicas de la experiencia se les permite a esos usuarios acceder mediante la asignación de conjuntos de permisos. Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).

### <a name="to-update-plan-changes-in-users-groups"></a>Para actualizar los cambios del plan en grupos de usuarios
Cuando haya realizado un cambio en los planes de los usuarios en el Centro de administración de Office 365, como asignar más usuarios al plan Premium, debe reflejar el cambio en [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Inicie sesión como administrador.
2. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Usuarios** y, a continuación, seleccione el vínculo relacionado.
3. En la ventana **Usuarios**, seleccione la acción **Actualizar todos los grupos de usuarios**.

Toda la información nueva sobre los planes de los usuarios y sus grupos de usuarios asignados ahora se actualizan de acuerdo con los cambios del plan.

### <a name="to-select-the-premium-experience"></a>Para seleccionar la experiencia Premium
Ahora puede proceder a seleccionar la nueva experiencia.
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Información de la empresa** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Información empresa**, en la ficha desplegable **Experiencia del usuario**, seleccione Premium en el campo **Experiencia**.

## <a name="see-also"></a>Consulte también .
[Crear nuevas en empresas](about-new-company.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)    
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
