---
title: Generar informes financieros con estructuras de cuentas
description: "Describe cómo utilizar los estructuras de cuentas para crear varias vistas e informes para analizar los datos de rendimiento financiero."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: es-mx
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a>Trabajar con estructuras de cuentas
Use estructuras de cuentas para obtener información sobre los datos financieros almacenados en su catálogo de cuentas. Los esquemas de cuentas analizan cifras en cuentas de contabilidad y comparan los movimientos de contabilidad con los presupuestados. Los resultados se muestran en gráficos en el Área de tareas, como el gráfico de Flujo de caja.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona algunos esquemas de cuentas de ejemplo que puede utilizar inmediatamente o puede configurar sus propias filas y columnas para especificar las cifras que se compararán. Por ejemplo, puede crear esquemas de cuentas para calcular márgenes de beneficios en dimensiones como departamentos o grupos de clientes. Puede crear tantos resultados financieros personalizados como desee.  

Configurar estructuras de cuentas requiere obtener una comprensión de los datos financieros del catálogo de cuentas. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto. Para ello es necesario que se creen presupuestos. Para obtener más información, consulte [Crear presupuestos contables](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Categorías de cuentas y esquemas de cuentas
Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros. Después de configurar las categorías de cuentas en la ventana **Categorías de cuenta** y haya elegido la acción **Generar esquemas de cuentas**, se actualizan los esquemas de cuentas subyacentes para los informes financieros principales. La próxima vez que ejecute uno de estos informes, como el estado de cuenta de saldo, se agregan los nuevos totales y subtotales en función de los cambios que realizó. Para obtener más información, consulte [Contabilidad y catálogo de cuentas](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Para crear nuevos estructuras de cuentas  
 Usar estructuras de cuentas para analizar cifras en cuentas de contabilidad o comparar los movimientos de contabilidad con los presupuestados. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Nombre esquema cuenta**, elija la acción **Nuevo** para crear un nuevo nombre de esquema de cuenta.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija la acción **Editar esquema cuentas**.
5. En la ventana **Esquema cuentas** rellene los campos según sea necesario.  

    Cuando haya creado una nueva estructura de cuentas y haya configurado las filas, debe configurar las columnas. Puede configurarlas manualmente o bien puede asignar una plantilla de columna predefinida a la estructura de cuentas.
6. Elija la acción **Editar configuración de disposición de columna**.
7. En la ventana **Plantilla columna** rellene los campos según sea necesario.

> [!NOTE]  
>   Si no ha asignado una plantilla de columnas predeterminada a la estructura de cuentas, debe configurar las columnas manualmente.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Para crear una columna que calcule porcentajes  
En ocasiones, podría desear incluir una columna en una estructura de cuentas para calcular los porcentajes de un total. Por ejemplo, si tiene una serie de filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales que representa cada fila.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Nombres de estructura de cuentas**, seleccione un estructura de cuentas.  
3. Elija la acción **Editar esquema cuentas** para configurar una fila del esquema de cuentas para calcular el total en el que se basarán los porcentajes.  
4. Inserta una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.  
5. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo sumatorio**, especifique **Fijar base para porcentaje**. En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basará. Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.  
6. Elija la acción **Editar configuración de disposición de columna** para configurar una columna.  
7. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo columna**, seleccione **Fórmula**. En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida de %. Por ejemplo, si el número de columna N contiene los saldos periodos, escriba **N%**.  
8. Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.

## <a name="to-set-up-account-schedules-with-overviews"></a>Para configurar estructuras de cuentas con resúmenes  
Puede usar un estructura de cuentas para crear un estado de cuenta que compare las cifras de contabilidad con las cifras presupuestadas.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Nombres de estructura de cuentas**, seleccione un estructura de cuentas.  
3. Elija la acción **Editar esquema cuentas**  
4. En la ventana **Esquema cuentas**, en el campo **Nombre**, seleccione el nombre del esquema de cuentas predeterminado.
5. Elija la acción **Insertar cuentas**.  
6. Seleccione la cuenta que desea incluir en la declaración y, a continuación, seleccione el botón **Aceptar**.

    Estas cuentas se insertan en la estructura de cuentas. Si lo desea, puede modificar la plantilla de columna.  
7. Seleccione la acción **Resumen**.  
8. Haga clic en la ficha desplegable **Filtros dimensión** y asigne al filtro de presupuesto el nombre que desee.  
9. Elija el botón **Aceptar**.  

Ahora puede copiar y pegar el estado de cuenta de banco del presupuesto en una hoja de cálculo.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Comparación de períodos contables usando fórmulas de períodos
La estructura de cuentas puede comparar los resultados de diferentes períodos contables, como este mes en comparación con el mismo mes del año anterior. Para hacerlo, agregue una columna con el campo **Fórmula de periodo comparativo** y luego establezca ese campo en una fórmula de período.  

Los periodos contables no tienen que coincidir forzosamente con el calendario, pero todos los años fiscales deben tener el mismo número de periodos contables, aunque cada periodo puede tener distinta duración.   

[!INCLUDE[d365fin](includes/d365fin_md.md)] utiliza la fórmula de periodo para calcular el importe a partir del periodo comparativo en relación con el periodo representado por el filtro de fecha de la solicitud de informe. El periodo de comparación se basa en el periodo de la fecha de inicio del filtro fecha. Las abreviaturas de las especificaciones de periodo son:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Siglas</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>P</p></td>
<td><p>Periodo</p></td>
</tr>
<tr class="even">
<td><p>LP</p></td>
<td><p>Último periodo de un año, semestre o trimestre fiscal.</p></td>
</tr>
<tr class="odd">
<td><p>CP</p></td>
<td><p>Periodo actual de un año, semestre o trimestre fiscal.</p></td>
</tr>
<tr class="even">
<td><p>FY</p></td>
<td><p>Ejercicio. Por ejemplo, FY[1..3] significa el primer trimestre del ejercicio actual.</p></td>
</tr>
</tbody>
</table>

Ejemplos de fórmulas:


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fórmula</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;En blanco&gt;</p></td>
<td><p>Periodo actual</p></td>
</tr>
<tr class="even">
<td><p>-1P</p></td>
<td><p>Periodo anterior</p></td>
</tr>
<tr class="odd">
<td><p>-1AF[1..UP]</p></td>
<td><p>Todo el ejercicio anterior</p></td>
</tr>
<tr class="even">
<td><p>-1AF</p></td>
<td><p>Periodo actual del ejercicio anterior</p></td>
</tr>
<tr class="odd">
<td><p>-1AF[1..3]</p></td>
<td><p>Primer trimestre del ejercicio anterior</p></td>
</tr>
<tr class="even">
<td><p>-1AF[1..PA]</p></td>
<td><p>Desde el principio de ejercicio anterior hasta el periodo actual en el ejercicio anterior, ambos inclusive</p></td>
</tr>
<tr class="odd">
<td><p>-1AF[PA..UP]</p></td>
<td><p>Desde el periodo actual del ejercicio anterior hasta el último periodo del ejercicio anterior, ambos inclusive</p></td>
</tr>
</tbody>
</table>

Si desea calcular el importe del periodo de comparación para periodos de tiempo regulares, deberá introducir una fórmula en el campo **Fórmula fecha comparación**.

> [!NOTE]
> No siempre es transparente qué períodos está comparando porque puede establecer un filtro de fecha en un informe que abarca diferentes fechas a los períodos contables que se reflejan en los datos del plan de cuentas. Por ejemplo, cree una estructura de cuentas en el que desee comparar este período con el mismo período del año anterior, por lo que debe establecer el campo **Filtro de período de fecha de comparación** en *-1FY*. Luego, ejecute el informe el 28 de febrero y configure el filtro de fecha en enero y febrero. Como resultado, la estructura de cuentas compara enero y febrero de este año con enero del año pasado, que es el único período contable completado de los dos para el año pasado.  


## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
