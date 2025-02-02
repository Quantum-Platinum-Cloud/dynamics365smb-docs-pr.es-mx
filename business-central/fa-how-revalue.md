---
title: Revalorizar activos fijos
description: 'Obtenga información sobre cómo ajustar el valor de los activos fijos, registrar nuevos importes como amortización o apreciación, y registrar costes de adquisición adicionales.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5628, 5629, 5633'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="revalue-fixed-assets" />Revalorizar activos fijos

La revalorización de activos fijos está formada por apreciaciones, depreciaciones o ajustes de valor general.

Cuando haya aumentado el valor de un activo fijo, registre una línea de diario con un importe mayor, una apreciación, en el libro de amortización. El nuevo importe se registra como una apreciación en función de la configuración del registro de activos fijos.

Cuando haya disminuido el valor de un activo fijo, registre una línea de diario con un importe menor, una depreciación, en el libro de amortización. El nuevo importe se registra como una depreciación en función de la configuración del registro de activos fijos.

El ajuste de valores se utiliza para ajustar los diversos valores de los activos fijos como, por ejemplo, los cambios generales de precio. El proceso **Ajustar valores activos** puede utilizarse para cambiar diversos importes como, por ejemplo, importes de apreciación y depreciación.

## <a name="to-post-an-appreciation-from-the-fixed-asset-gl-journal" />Para registrar una apreciación desde el diario general de activos fijos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.  
2. Cree una línea inicial de diario y rellene los campos según sea necesario.
3. En el campo **A/F Tipo registro**, seleccione **Reevaluación**.
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de apreciaciones.

    > [!NOTE]  
    >   El paso 4 solo funciona si ha configurado lo siguiente: en la página **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cta. apreciación** contiene la cuenta de cargo y el campo **Cta. contrap. apreciación** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación. Para obtener más información, vea [Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Seleccione la acción **Registrar**.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal" />Para registrar una depreciación desde el diario general de activos fijos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.  
2. Cree una línea inicial de diario y rellene los campos según sea necesario.
3. En el campo **A/F Tipo registro**, seleccione **Depreciación**.
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de depreciaciones.

    > [!NOTE]  
    >   El paso 4 solo funciona si ha configurado lo siguiente: en la página **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cta. depreciación** contiene la cuenta de abono y el campo **Cta. gastos depreciación** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para las depreciaciones. Para obtener más información, vea [Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Seleccione la acción **Registrar**.

## <a name="to-perform-general-revaluation-of-fixed-assets" />Para realizar una revalorización general de activos fijos

El ajuste de valores se utiliza para ajustar los diversos valores de los activos fijos como, por ejemplo, los cambios generales de precio. El proceso **Ajustar valores activos** puede utilizarse para cambiar diversos importes como, por ejemplo, importes de apreciación y depreciación. La casilla **Permite ajuste valores** de la página **Libro amortización** debe estar seleccionada.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Índice de activos fijos** y, luego, elija el vínculo relacionado.  
2. Rellene los campos según sea necesario.
3. Elija el botón **Aceptar**.

    Las líneas de revalorización se crean según su configuración en el paso 2. Las líneas se crean en el diario de activos fijos o en el diario general de activos fijos dependiendo de su configuración de plantilla y sección en la página **Configuración del diario A/F**. Para obtener más información, consulte [Configurar información general del activo fijo](fa-how-setup-general.md).
4. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.  
5. Seleccione el diario con los activos fijos que desea revalorizar y, a continuación, elija la acción **Movimientos**.  
6. Compruebe los movimientos creados y, a continuación, seleccione la acción **Registrar** para registrarlos en el diario.

    > [!TIP]  
    >   Si los números de ajuste son solo para fines de simulación, puede crear un libro de amortización especial que los guarde. Así estos movimientos no afectarán a ninguno de los libros de amortización.

## <a name="to-post-additional-acquisition-costs" />Para registrar costos de adquisición adicionales

Puede registrar costos de adquisición adicionales de un activo fijo de la misma forma que registra el costo de adquisición original: desde una factura de compra o desde un diario de activos fijos. Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).  

Si ya ha calculado la amortización para el activo fijo, active la casilla **Depr. de costo de adquisición** para que el costo de adquisición adicional sea menor que el valor residual amortizado, en proporción al importe con el que se amortizó anteriormente el activo fijo. Esto asegura que el periodo de amortización no cambia.  

El porcentaje de amortización se calcula así:  

*P = (Total amortización x 100) / Base amortizable*

*Importe amortización = (P/100) x (Coste adicional – Valor residual)*  

Recuerde activar la casilla **A/F Amort. hasta fecha reg.** en la factura, las líneas del diario general de activos fijos o del diario de activos fijos, para asegurarse de que la amortización se calcula desde la última fecha de registro de activos fijos hasta la fecha de registro del costo de adquisición adicional.

### <a name="example---posting-additional-acquisition-costs" />Ejemplo: registro de costos adicionales

Se compra una máquina el 1 de agosto de 2000. El costo de adquisición es de 4800. El método de amortización es lineal durante cuatro años.

El 31 de agosto de 2000 se ejecuta el proceso **Calcular amortización**. La amortización se calcula como:

*valor neto x número de días de amortización / número total de días de amortización = 4800 x 30 / 1440 = 100*  

El 15 de septiembre de 2000 se registra una factura por pintar la máquina. El importe de la factura es 480.

Si seleccionó la casilla **A/F Amort. hasta fecha reg.** en la factura antes de registrar, se realiza el siguiente cálculo:  

15 días de amortización (del 01/09/00 al 15/09/00) se calculan así:

*valor neto x número de días de amortización / número restante de días de amortización = (4800 - 100) x 15 / 1410 = 50*

Si seleccionó la casilla **Depr. de costo de adquisición** en la factura antes de registrar, se realiza el siguiente cálculo:  

*El coste adicional se amortiza en ((150 x 100) / 4800) / 100 x 480 = 15*

La base de amortización es ahora *5280 = (4800 + 480)* y la amortización acumulada es *165 = (100 + 50 + 15)*, correspondiente a 45 días de amortización del costo de adquisición total. Esto significa que el activo se amortizará por completo en el tiempo estimado de cuatro años.  

Para ejecutar el proceso **Calcular amortización** sobre el 30/09/00 se realiza el siguiente cálculo:  

*La vida de amortización restante es de 3 años, 10 meses y 15 días = 1395 días*  

*El valor neto es (5280-165) = 5115*  

*El importe de amortización para septiembre 2000: 5115 x 15 / 1395 = 55,00*  

*Total de amortización = 165 + 55 = 220*  

Si no seleccionó la casilla **A/F Amort. hasta fecha reg.**, el activo perdería 15 días de amortización, ya que el proceso **Calcular amortización** efectuado el 30/09/00 calcularía la amortización del 15/09/00 al 30/09/00. Esto quiere decir que cuando se ejecuta el proceso **Calcular amortización** el 30/09/00, el cálculo es el siguiente:  

*El tiempo de amortización restante es de 3 años, 10 meses y quince días = 1395 días*  

*El valor neto es (4800 + 480 - 100 - 15) = 5165*

*El importe de amortización para septiembre 2000: 5165 x 15 / 1395 = 55,54*  

*Total de amortización = 100 +15 + 55,54 = 170,54*

## <a name="see-related-microsoft-trainingtrainingpathsmanage-advanced-fixed-assets-transactions" />Consultar la [formación de Microsoft](/training/paths/manage-advanced-fixed-assets-transactions/) relacionada

## <a name="see-also" />Consulte también .

[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
