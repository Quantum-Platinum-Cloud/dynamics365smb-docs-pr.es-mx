---
title: "Ver y editar la configuración básica en Financials | Documentos de Microsoft"
description: "Obtenga información sobre cómo cambiar algunos valores de configuración básicos en Financials, por ejemplo, el área de tareas, la empresa o la fecha de trabajo."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date
ms.date: 03/02/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 4fceff1a6cf728608a49182a9704f187d31767fe
ms.openlocfilehash: f71b0e7d53138be0f89abe4e7935ab7c21437d8e
ms.contentlocale: es-mx
ms.lasthandoff: 05/28/2018

---
# <a name="changing-basic-settings"></a>Cambiar la configuración básica
En la ventana **Mi configuración**, puede ver y cambiar la configuración básica de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Los cambios que realice sólo afectan a su área de trabajo; no a las áreas de trabajo de otros usuarios.  

## <a name="role-center"></a>Área de tareas
El Área de tareas representa la página Inicio, una pantalla de inicio que está designada para las necesidades específicas del trabajo en una empresa. Dependiendo de su función, el Área de tareas le brinda una descripción general del negocio, su departamento o sus tareas personales. También le ayuda a navegar por sus tareas diarias y encontrar el trabajo que le asignaron.

-   En la parte superior, la navegación le permite cambiar entre clientes, proveedores, artículos y otras listas importantes de información. Del mismo modo, las acciones le permiten iniciar tareas, como crear una nueva factura de venta, directamente desde el Área de tareas.

-   En el centro se encuentran las **Actividades**. Las actividades muestran datos actuales y se puede hacer clic en ellas o tocarlas para ver información más detallada. Los Indicadores de rendimiento clave pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de caja o ingresos y gastos. También puede crear una lista de clientes favoritos en la página de inicio para las cuentas con las que hace negocios a menudo o a las que necesita prestar especial atención.

### <a name="to-change-role-center"></a>Para cambiar el Área de tareas
El Área de tareas predeterminada es **Administrador empresarial**, pero puede seleccionar otra área de tareas que se adapte mejor a sus necesidades.
1. En la esquina superior derecha, elija el icono **Configuración** ![Configuración](media/ui-experience/settings_icon_small.png "Icono Configuración para el área de trabajo") y, a continuación, elija **Mi configuración**.
2. En la ventana **Mi configuración**, en el campo **Área de tareas**, seleccione el área de tareas que quiere establecer como estándar. Por ejemplo, seleccione **Contable**.
3. Elija el botón **Aceptar**.

## <a name="company"></a>Compañía
Una empresa funciona como un contenedor de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede haber múltiples empresas en una base de datos, pero solo se puede seleccionar una a la vez.

La empresa predeterminada se llama CRONUS y solo contiene datos de demostración.

> [!TIP]  
>   Si desea que se muestre un nombre distinto para la empresa en la aplicación (por ejemplo, como en el Área de tareas), establezca el campo **Nombre** en la página **Información empresa** o el campo **Nombre para mostrar** en la página **Empresas**.  

## <a name="work-date"></a>Fecha de trabajo
La fecha predeterminada de trabajo será normalmente la fecha actual. Es posible que tenga que cambiar temporalmente la fecha de trabajo para realizar tareas como la finalización de las transacciones de una fecha que no sea la fecha actual.

> [!TIP]  
>   Escriba **w** para introducir rápidamente la fecha de trabajo en un campo de fecha. Escriba **t** para introducir rápidamente la fecha actual en el campo de fecha.

> [!IMPORTANT]  
>   La fecha de trabajo se cambia solo hasta que cierre la empresa o hasta que la fecha cambie. Si abre una empresa diferente o la misma al día siguiente y debe utilizar una fecha de trabajo diferente, tendrá que volver a definirla.

## <a name="region"></a>Región
El valor **Región** determina cómo se muestran o se forman las fechas, los tiempos, los números, y divisas.   


## <a name="language"></a>Idioma
Cambia el idioma de la pantalla. Este campo aparece sólo cuando hay más de un idioma a elegir. 

El idioma inicial lo determina el administrador o la configuración de su navegador cuando inicia sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El idioma que establezca se usará en todos los dispositivos desde los que inicie sesión, como un teléfono o una tableta. 

## <a name="changing-when-i-receive-notifications"></a>Cambio al recibir notificaciones
Seleccione este vínculo para ver o cambiar las notificaciones que recibe sobre determinados eventos o cambios de estado, cuando va a facturar a un cliente que tiene un saldo vencido o cuando las existencias disponibles son inferiore a la cantidad que va a vender, por ejemplo. Para obtener más información, consulte [Notificaciones inteligentes](ui-smart-notifications.md).

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
