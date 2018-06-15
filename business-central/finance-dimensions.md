---
title: Trabajar con dimensiones | Documentos de Microsoft
description: "Puede utilizar dimensiones para clasificar movimientos, por ejemplo, por departamentos o proyecto, por lo que le será muy fácil realizar un seguimiento de los datos y analizarlos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 349a4d54a95999e3e2c2b19cc2a40c2dd1afd445
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="working-with-dimensions"></a>Trabajar con dimensiones
Para simplificar la realización de análisis en documentos, como pedidos de venta, puede utilizar dimensiones. Las dimensiones son atributos y valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de ellos. Por ejemplo, las dimensiones pueden indicar de qué proyecto o departamento procede un movimiento.  

Por ejemplo, en lugar de tener que configurar cuentas contables generales independientes para cada departamento y proyecto puede usar dimensiones. De este modo, dispone de la posibilidad de análisis, sin crear un catálogo de cuentas complicado. Para obtener más información, consulte [Inteligencia empresarial](bi.md).

Otro ejemplo es configurar una dimensión que se llame *Departamento* y usarla junto con esta dimensión cuando registre documentos de ventas. Así podrá usar herramientas la de inteligencia empresarial para ver qué departamento vende cada producto.
Cuantas más dimensiones use, más detallados serán los informes en los que pueda basar sus decisiones empresariales. Por ejemplo, un movimiento de ventas individual puede incluir información de múltiples dimensiones, por ejemplo:  

* La cuenta en la que se registró la venta del producto  
* Dónde se vendió el producto
* Quién lo vendió
* El tipo de cliente que lo compró  

## <a name="analyzing-by-dimensions"></a>Analizar por dimensiones
La funcionalidad Dimensiones desempeña una función importante en la inteligencia empresarial, por ejemplo al definir vistas de análisis. Para obtener más información, vea [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

> [!TIP]
> Como una forma rápida de analizar datos transaccionales por dimensiones, puede filtrar por dimensiones los totales del plan de cuentas y movimientos en todas las ventanas **Movimientos**. Busque la acción **Establecer filtro de dimensiones**.

## <a name="dimension-sets"></a>Grupos de dimensiones
Un grupo de dimensiones es una combinación única de valores de dimensión. Se almacena como movimientos de grupo de dimensiones en la base de datos. Cada movimiento de grupo de dimensiones representa un valor de dimensión único. El grupo de dimensiones se identifica por medio de un id común del grupo de dimensiones que está asignado a cada movimiento de grupo de dimensiones que pertenece al grupo de dimensiones.  

Cuando crea una línea de diario, cabecera de documentos o línea de documentos, puede especificar una combinación de valores de dimensión. En lugar de explícitamente guardar cada valor de dimensión en la base de datos, un Id. de grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos para especificar el grupo de dimensiones.  

## <a name="setting-up-dimensions"></a>Configurar dimensiones
Puede definir las dimensiones y los valores de dimensión para clasificar los diarios y los documentos, como pedidos de venta y pedidos de compra. Las dimensiones se configuran en la ventana **Dimensiones**, donde se crea una línea para cada dimensión, como *Proyecto*, *Departamento*, *Área* y *Vendedor*.

También se configuran los valores de dimensión. Por ejemplo, los valores pueden ser departamentos de su empresa. Los valores de dimensiones se pueden configurar en una estructura jerárquica similar al catálogo de cuentas, de modo que los datos se puedan desglosar en diversos niveles de granularidad y se puedan totalizar subconjuntos de valores de dimensiones. Puede definir tantas dimensiones y valores de dimensión como necesite y cualquier usuario de su empresa puede usarlos.

También puede configurar algunas dimensiones globales y abreviadas:  

* Las **dimensiones globales** se usan como filtros, por ejemplo, en informes y procesos. Solo puede utilizar dos dimensiones globales, por lo que debería elegir las dimensiones que use a menudo.
* Las **dimensiones abreviadas** están disponibles como campos en líneas de diario y documento. Puede crear un máximo de seis.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Configurar dimensiones predeterminadas para clientes, proveedores y otras cuentas
Puede asignar una dimensión predeterminada para una determinada cuenta. La dimensión se copiará en el diario o el documento cuando introduzca el número de cuenta en una línea, pero puede eliminar o cambiar el código de la línea si es necesario. También puede convertir una dimensión en obligatoria para registrar un movimiento con un tipo de cuenta específico.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Dimensiones** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Dimensiones**, seleccione la dimensión correspondiente y elija la acción **Dimensión predet. tipo cta**.  
4.  Rellene una línea para cada nueva dimensión predeterminada que quiera configurar. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Si desea hacer que una dimensión sea obligatoria pero no desea asignar un valor predeterminado a la dimensión, deje el campo **Cód. valor dimensión** en blanco y seleccione **Obligatorio** en el campo **Registro valor**.  

> [!WARNING]  
>  Si una cuenta se utiliza en el trabajo por lotes **Ajustar tipos de cambio** o el trabajo por lotes **Reg. var. inventario en cont.**, no seleccione las opciones **Código obligatorio** o **Igual código**. Estos procesos no pueden utilizar códigos de dimensión.  

> [!NOTE]  
>  Si es necesario asignar a una cuenta una dimensión distinta a la dimensión predeterminada ya configurada para el tipo de cuenta, deberá configurar una dimensión predeterminada para dicha cuenta. La dimensión predeterminada de la cuenta en concreto sustituirá a la dimensión predeterminada del tipo de cuenta.  

### <a name="to-set-up-default-dimension-priorities"></a>Para configurar prioridades de dimensiones predeterminadas  
Distintos tipos de cuentas, por ejemplo, una cuenta de cliente y una cuenta de producto, pueden tener configuradas dimensiones predeterminadas diferentes. Como resultado, un movimiento puede tener más de una propuesta de dimensión predeterminada para una dimensión. Para evitar este tipo de conflictos, puede aplicar reglas de prioridad a los diversos orígenes.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Prioridades dimensión predeterminadas** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Prioridades dimensión predet.**, en el campo **Cód. origen**, escriba el código de origen para la tabla de movimientos para la que se aplicarán las prioridades de dimensión predeterminadas.  
3.  Rellene una línea para cada prioridad de dimensión predeterminada que desee para el código de origen seleccionado.
4.  Repita el procedimiento para la cada código de origen para el que quiera configurar prioridades de dimensión predeterminadas.  

> [!IMPORTANT]  
>  Si configura dos tablas con la misma prioridad en un mismo código de origen, [!INCLUDE[d365fin](includes/d365fin_md.md)] seleccionará siempre la tabla con el Id. de tabla inferior.  

### <a name="to-set-up-dimension-combinations"></a>Para configurar combinaciones de dimensión  
Para evitar registrar movimientos con dimensiones contradictorias o irrelevantes, puede bloquear o limitar determinadas combinaciones de dos dimensiones. Una dimensión está bloqueada si no es posible registrar ambas dimensiones en el mismo movimiento independientemente de los valores de dimensión. Una combinación de dimensión limitada le permite registrar ambas dimensiones en el mismo movimiento, pero únicamente para determinadas combinaciones de valores de dimensión.

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Combinaciones dimensión** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Combinación dimensión**, seleccione el campo de la combinación de dimensión y seleccione una de las opciones siguientes.  

    |Campo|Descripción|
    |----------------------------------|---------------------------------------|  
    |**Nº limitaciones**|Esta combinación de dimensión no tiene restricciones. Se permiten todos los valores de dimensión.|  
    |**Limitado**|Esta combinación de dimensión tiene determinadas restricciones en función de los valores de dimensión que introduzca. Debe definir las limitaciones en la ventana **Combinación valor dimensión**.|  
    |**Bloqueado**|Esta combinación de dimensión no está permitida.|  

3.  Si selecciona la opción **Limitado**, debe definir las combinaciones de valores de dimensión que están bloqueadas. Para ello, elija el campo para definir la combinación de dimensión.  
4.  A continuación, seleccione una combinación de valores de dimensión que esté bloqueada y escriba **Bloqueado** en el campo. Un campo en blanco significa que la combinación de valores de dimensión está permitida. Repita el proceso con múltiples dimensiones bloqueadas.  

> [!NOTE]  
>  Las mismas dimensiones se repiten tanto en las filas como en las columnas, por lo que todas las combinaciones de dimensiones aparecen dos veces. [!INCLUDE[d365fin](includes/d365fin_md.md)] muestra automáticamente el valor en ambos campos. No puede realizar ninguna selección en los campos de la esquina superior izquierda hacia abajo, ya que estos campos tienen la misma dimensión tanto en las filas como en las columnas.  
>   
>  La opción seleccionada no será visible hasta que no salga del campo.  
>   
>  Para mostrar el nombre de la dimensión en lugar del código, seleccione el campo **Muestra nombre columna**.

### <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Obtener una visión general de las dimensiones utilizadas varias veces
La ventana **Dimensiones predet.-Múltiple** especifica cómo un grupo de cuentas usa dimensiones y valores de dimensión. Puede hacerlo resaltando varias cuentas y, a continuación, especificando las dimensiones y los valores de dimensión predeterminados para todas las cuentas que ha resaltado en la lista de cuentas. Al especificar las dimensiones predeterminadas para las cuentas resaltadas, el sistema sugerirá estas dimensiones y valores de dimensión cuando se utilice una de ellas, por ejemplo, en una línea de diario. Esto facilita el registro de movimientos, ya que los campos de dimensión se rellenan automáticamente. No obstante, los valores de dimensión sugeridos se pueden cambiar en, por ejemplo, una línea de diario.

La ventana **Dimensiones predet.-Múltiple** contiene los campos siguientes:
|Campo|Descripción|
|----------------------------------|---------------------------------------|  
|**Cód. dimensión**|Muestra todas las dimensiones que se han definido como dimensiones predeterminadas en una o varias cuentas resaltadas. Seleccionando el campo, puede ver una lista de todas las dimensiones disponibles. Si selecciona una dimensión, la dimensión seleccionada se definirá como la dimensión predeterminada para todas las cuentas resaltadas.|
|**Cód. valor dimensión**|Muestra un valor de dimensión único o el término (Problema). Si en el campo se muestra un valor de dimensión, todas las cuentas resaltadas tienen el mismo valor de dimensión predeterminado para una dimensión. Si en el campo se muestra el término (Problema), no todas las cuentas resaltadas tienen el mismo valor de dimensión predeterminado para una dimensión. Al seleccionar el campo, podrá ver una lista de todas las dimensiones que están disponibles para una dimensión. Si selecciona un valor de dimensión, el valor de dimensión seleccionado se definirá como el valor de dimensión predeterminado para todas las cuentas resaltadas.|
|**Registro valor**|Muestra una regla de valor al registrar única o el término (Problema). Si en el campo se muestra la regla de valor al registrar, todas las cuentas resaltadas tienen la misma regla de valor al registrar para un valor de dimensión. Si en el campo se muestra el término (Problema), no todas las cuentas resaltadas tienen la misma regla de valor al registrar para un valor de dimensión. Al seleccionar el campo Valor al registrar, podrá ver una lista de reglas de valor al registrar. Si selecciona una regla de valor al registrar, la regla de valor al registrar seleccionada se aplicará a todas las cuentas resaltadas.|

### <a name="example-of-dimension-setup"></a>Ejemplo de configuración de dimensiones
Supongamos que su empresa desea realizar un seguimiento de las transacciones en función de la estructura organizativa y las ubicaciones geográficas. Para ello, puede configurar dos dimensiones en la ventana **Dimensiones**:

* **ÁREA**  
* **DEPARTAMENTO**  

| Código | Nombre | Título código | Título filtro |
| --- | --- | --- | --- |
| ÁREA |Área |Código de área |Filtro Área |
| DPTO |Departamento |Código de departamento |Filtro departamento |

Para **ÁREA**, agregue los siguientes valores de dimensión:

| Código | Nombre | Tipo valor dimensión |
| --- | --- | --- |
| 10 |América |Inicio-tot. |
| 20 |América del Norte |Estándar |
| 30 |Pacífico |Estándar |
| 40 |Sudamérica |Estándar |
| 50 |América, total |Fin-Tot |
| 60 |Europa |Inicio-tot. |
| 70 |UE |Estándar |
| 80 |No perteneciente a la UE |Estándar |
| 90 |Europa, Total |Fin-Tot |

Para las dos áreas geográficas principales, América y Europa, agregue subcategorías para las regiones indentando los valores de dimensión. De esta manera podrá elaborar informes sobre ventas o gastos en regiones, y obtener totales de las áreas geográficas más grandes. También puede usar países o regiones como valores de dimensión, o condados o municipios/ciudades, dependiendo de la empresa.  
> [!NOTE]  
>   Para configurar una jerarquía, los códigos deben estar en orden alfabético. Esto incluye los códigos de los valores de dimensión que se proporcionan en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Para **DEPARTAMENTO**, agregue los siguientes valores de dimensión:

| Código | Nombre | Tipo valor dimensión |
| --- | --- | --- |
| ADMIN |Administración |Estándar |
| PROD |Producción |Estándar |
| CCIAL |Ccial |Estándar |

Con esta configuración, agregará las dos dimensiones como las dos dimensiones globales en la ventana **Configuración de contabilidad**. Esto significa que puede usar ÁREA Y DEPARTAMENTO como filtros para los movimientos de contabilidad, así como en todos los informes y esquemas de cuentas. También están disponibles ambas dimensiones globales de forma automática para el uso en líneas de movimientos y cabeceras de documentos, como dimensiones abreviadas.  

## <a name="using-dimensions"></a>Usar dimensiones
En un documento como una orden de venta, puede agregar información de dimensión de una línea en particular y del mismo documento. Por ejemplo, en la ventana **Pedido de ventas**, puede introducir valores de dimensión para las dos primeras dimensiones abreviadas en las líneas de venta individuales y puede agregar más información de dimensión si elige el botón **Dimensiones**.  

Si trabaja con un diario, puede agregar información de dimensiones a un movimiento del mismo modo, si ha configurado dimensiones abreviadas como campos directamente en las líneas de diario.  

Puede configurar dimensiones predeterminadas para cuentas o tipos de cuenta, para que esas dimensiones o valores de dimensión se completen automáticamente.

## <a name="to-view-global-dimensions-in-ledger-entry-windows"></a>Para ver dimensiones globales en ventanas de movimientos de contabilidad  
El nombre y la definición de las dimensiones globales los establece la empresa. Para ver las dimensiones globales correspondientes a su empresa, abra la ventana **Configuración contabilidad**.  

En una ventana de movimiento de contabilidad, puede ver si hay dimensiones globales para los movimientos. Las dos dimensiones globales difieren del resto de las dimensiones porque se pueden utilizar como filtros en cualquier lugar de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Plan de cuentas**, seleccione la acción **Movimientos**.  
3.  Para ver únicamente los movimientos relevantes, establezca uno o más filtros en la ventana.  
4.  Para ver todas las dimensiones de un movimiento, seleccione el movimiento y elija la acción **Dimensiones**.  

> [!NOTE]  
>  La ventana **Dimensiones movimiento** muestra las dimensiones de un movimiento de contabilidad cada vez. A medida que se desplaza por los movimientos, el contenido de la ventana **Dimensiones movimiento** va cambiando según corresponda.  

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
