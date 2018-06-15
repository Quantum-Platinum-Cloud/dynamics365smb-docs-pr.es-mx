---
title: Bienvenido | Documentos de Microsoft
description: "Describe las guías de configuración asistida, los vídeos, los temas de ayuda y las páginas y las ventanas que se usan para empezar a realizar operaciones empresariales en Business Central."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365, setup, wizard, experience
ms.date: 02/19/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 5508b9336b0e6bffcc47632b95eac3691ab3891c
ms.contentlocale: es-mx
ms.lasthandoff: 04/18/2018

---
# <a name="getting-ready-for-doing-business"></a>Preparación para hacer negocios
Enhorabuena, acaba de iniciar su primera empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Para ayudarle a empezar a hacer negocios, puede visitar la ventana **Asistencia de negocio** donde puede iniciar guías de configuración asistida, vídeos o temas de ayuda para determinadas tareas de configuración. A la ventana se accede desde el gráfico en el área de trabajo **Administrador de negocio** eligiendo el menú desplegable **Asistencia de negocio** y, a continuación, eligiendo la acción **Mostrar configuración y recursos de ayuda**. Al actualizar la página, el gráfico se reemplaza por los recursos de configuración y ayuda.

En el Área de tareas, en la barra de navegación superior, encontrará el menú **Configuración y extensiones**. Aquí tiene acceso a una lista de configuraciones asistidas que pueden ayudarle a empezar. Una vez haya migrado los datos, como los proveedores, clientes o productos de su sistema financiero existente, está listo para empezar. Pero en función de sus necesidades, considere si la otra configuración asistida puede ayudarle. Si un área no está cubierta por una configuración asistida, elija la acción **Configuración manual** para obtener acceso a las ventanas de configuración donde puede rellenar los campos de configuración de todas las áreas manualmente. Para obtener más información, consulte también [Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).

> [!NOTE]  
>   La lista de guías de configuración, las extensiones y los servicios que están disponibles varían según la experiencia del usuario que elija para la empresa. La experiencia **Básica** ofrece menos acceso que la experiencia **Esencial**. La primera vez que inicie sesión, use la experiencia Básica. Para obtener más información, consulte [Cambiar las funciones que se muestran](ui-experiences.md).

En la ventana **Configuración asistida**, encontrará lo siguiente con la experiencia **Básico**:

| Configuración asistida | Descripción |
| --- | --- |
| Configurar la empresa |Crea una nueva empresa de prueba para que pueda introducir datos y probar [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si empezó con el paseo de introducción, es probable que ya lo haya **Completado**. |
| Migrar datos empresariales |Permite importar datos empresariales existentes, como proveedores, clientes y productos desde Excel o Quickbooks. |
| Configurar impuesto de ventas |Lo ayuda a empezar con grupos de impuestos predeterminados y la asignación de códigos de área de impuesto que puede asignar a clientes y proveedores para calcular automáticamente los impuestos sobre las ventas en los documentos de venta o compra. |
| Configurar correo electrónico |Le prepara para enviar correos electrónicos directamente de, por ejemplo, pedidos o contactos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. |
| Configurar complementos de Office |Le posibilita usar y ejecutar [!INCLUDE[d365fin](includes/d365fin_md.md)] desde Outlook. |
| Config. flujo trabajo aprob. |Le permite notificar automáticamente al aprobador cuando un usuario intente crear o cambiar determinados valores en documentos, líneas de diario o tarjetas, como por ejemplo un importe por encima del límite especificado. |
| Config. registro correo elect. |Le permite iniciar sesión en la correspondencia por correo electrónico en [!INCLUDE[d365fin](includes/d365fin_md.md)] para realizar el seguimiento de las interacciones. |
| Configurar el conector de Business Central |Le permite conectar con Dynamics 365 for Sales que le posibilita la sincronización de datos como los contactos y la información de los pedidos. |

Cuando ha ejecutado un asistente de configuración, se marca como **Completado**. Para ejecutar el asistente de configuración, seleccione los tres puntos también denominados menú contextual y, a continuación, seleccione **Iniciar configuración**.

## <a name="role-center"></a>Área de tareas
En el Área de tareas tiene información general de su negocio. A la izquierda puede ver una barra de navegación que le da un acceso sencillo a los clientes, proveedores, productos, etc. En el centro se encuentra el mosaico **Actividades**. **Actividades** muestra los datos actuales y se puede hacer clic o pinchar sobre él para conseguir un acceso fácil al documento seleccionado. Los **Indicadores de rendimiento clave** pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de caja o ingresos y gastos. También puede crear una lista de **Clientes favoritos** en el Área de tareas para las cuentas con las que hace negocios a menudo o a las que necesita prestar especial atención.
Use las flechas para contraer parte de la página y haga más espacio para mostrar datos específicos. En la parte superior del Área de tareas encontrará todas las acciones que se pueden realizar con el contenido actual. Todo esto también se puede contraer y solo necesita hacer clic o pinchar en el área contraída para volverlo a ver.

> [!TIP]  
> Puede volver al Área de tareas seleccionando el nombre de la empresa en la esquina superior izquierda.

## <a name="company-information"></a>Información empresa
En **Configuración de la empresa** puede ver y editar información de configuración sobre la empresa actual, mucha de la cual se rellenó previamente si completó la configuración asistida **Configurar empresa** al registrarse en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si desea cambiar el logotipo de la empresa, la información de contacto, la configuración del banco o la información de los impuestos, puede hacerlo desde esta ventana.    

## <a name="adding-users-and-permissions"></a>Agregar usuarios y permisos
Si necesita agregar más usuarios, se realiza de centro de administración de Office 365. Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc). Una vez se hayan creado los usuarios en Office 365, se pueden importar en la ventana **Usuarios** mediante la acción **Obtener usuarios desde Office 365**. Después podrá continuar con la asignación de permisos a usuarios y la organización en grupos de usuarios. Para obtener más información, vea [Administrar usuarios y permisos](ui-how-users-permissions.md).  

## <a name="getting-help"></a>Obtener ayuda
En [!INCLUDE[d365fin](includes/d365fin_md.md)] encontrará las herramientas de información que pueden guiarle a través de varios procesos empresariales. En cada herramienta de información encontrará un vínculo denominado **Obtener ayuda** que le llevará a la ayuda del producto. El signo de interrogación de la esquina superior derecha también le dirige a la ayuda del producto.

## <a name="next-steps"></a>Pasos siguientes
Según sus datos migrados, ahora puede empezar a crear nuevos documentos de compra o venta. Use la sección **Mi empresa** de la página **Inicio** para crear rápidamente una nueva cotización de venta, una factura de venta, una orden de venta, una factura de compra o un registro de pago.

## <a name="see-also"></a>Consulte también
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
