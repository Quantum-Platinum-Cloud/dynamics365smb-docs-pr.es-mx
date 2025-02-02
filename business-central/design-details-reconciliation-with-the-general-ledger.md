---
title: 'Detalles de diseño: Conciliación con contabilidad | Documentos de Microsoft'
description: 'En este tema se describe la conciliación con la contabilidad cuando registra transacciones de inventario, como pueden ser remisiones de venta, salida de producción o ajustes negativos.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, reconciliation, general ledger, inventory'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-reconciliation-with-the-general-ledger" />Detalles de diseño: Conciliación con contabilidad
Cuando registra transacciones del inventario, como envíos de ventas, salida de producción o ajustes negativos, se registran los cambios realizados en la cantidad y en los valores del inventario en los movimientos de contabilidad y en los movimientos de valores, respectivamente. El siguiente paso en el proceso será registrar los valores de existencias en las cuentas del inventario del módulo de contabilidad.  

Existen dos formas de conciliar el inventario con la contabilidad:  

* Esto se hace manualmente ejecutando el proceso **Reg. var. inventario en cont.**.  
* Automáticamente, cada vez que se registra una transacción de inventario.  

## <a name="post-inventory-cost-to-gl-batch-job" />Trabajo por lote Reg. var. inventario en cont.
Cuando ejecute el proceso **Reg. var. inventario en cont.**, se crearán los movimientos de contabilidad según los movimientos de valuación. Puede resumir los movimientos de contabilidad por cada movimiento de valoración o crear movimientos de contabilidad por cada combinación de fecha de registro, código de ubicaciones, grupo de registro de inventario, grupo contable general del negocio y grupo contable general del producto.  

Las fechas de registro de los movimientos de contabilidad se establecerán en la fecha de registro del movimiento de valoración correspondiente, excepto si el movimiento de valoración se encuentra en un periodo contable cerrado. En este caso, se omite el movimiento de valoración y se debe cambiar la configuración de contabilidad o del usuario para activar el registro dentro del rango de fechas.  

Cuando ejecute el proceso **Reg. var. inventario en cont.**, es posible que se produzcan errores porque falta la configuración o porque la configuración de dimensión no es compatible. Si el proceso encuentra errores relacionados con la configuración de dimensión, omitirá dichos errores y utilizará las dimensiones del movimiento de valor. Para otros errores, el trabajo por lotes no registra los movimientos de valores y muestra una lista de ellos al final del informe, en una sección llamada **Movimientos omitidos**. Para registrar dichos movimientos, deberá primeramente arreglar las causas de los errores. Para ver una lista con los errores antes de ejecutar el proceso, puede ejecutar el informe **Reg. var. ex. en cont. - Test**. Este informe muestra un listado con todos los errores encontrados durante un proceso de registro de prueba. Puede solucionar dichos errores y después ejecutar el trabajo por lotes de registro de costos de inventario sin que se omita ningún movimiento.  

## <a name="automatic-cost-posting" />Variación existencias automát.
Para configurar que el registro de costos en contabilidad se ejecute automáticamente al registrar una transacción de inventario, seleccione la casilla **Variación existencias automát.** en la página **Configuración de inventario**. La fecha de registro del movimiento de contabilidad es la misma que la fecha de registro del movimiento de producto.  

## <a name="account-types" />Tipos de cuenta
Durante la conciliación, los valores de inventario se registran en la cuenta de inventario en la hoja de balance. El mismo importe, pero con el signo contrario, se registra en la cuenta de contrapartida correspondiente. Normalmente, la cuenta de contrapartida es una cuenta de ganancias y pérdidas. No obstante, cuando se registra un costo directo relacionado con un consumo o una salida, la cuenta de contrapartida es una cuenta de balance. El tipo del movimiento de producto y del movimiento de valoración determina en qué cuenta de contabilidad se realizará el registro.  

El tipo de movimiento indica en qué cuenta de contabilidad se registrará. Se determina mediante el signo de la cantidad en el movimiento de producto o la cantidad valuada del movimiento de valoración, ya que las cantidades siempre tienen el mismo signo. Por ejemplo, un movimiento de venta con una cantidad positiva describe una salida de inventario fruto de una venta, y un movimiento de venta con una cantidad negativa describe una entrada de inventario fruto de una devolución de venta.  

### <a name="example" />Ejemplo
En el ejemplo siguiente se muestra una cadena de bicicleta que se ha fabricado con eslabones comprados. En este ejemplo se muestra cómo se usan los diferentes tipos de cuenta contable en un escenario típico.  

La casilla **Regis. cto. previsto en contab.** de la página **Configuración de inventario** está seleccionada y la configuración siguiente está definida.  

En la tabla siguiente se muestra cómo está configurado el eslabón en la ficha de producto.  

|Configurar el campo|Valor|  
|-----------------|-----------|  
|**Valoración existencias**|Estándar|  
|**Coste estándar**|$ 1,00|  
|**Tasa costos generales**|$ 0,02|  

En la tabla siguiente se muestra cómo está configurada la cadena en la ficha de producto.  

|Configurar el campo|Valor|  
|-----------------|-----------|  
|**Valoración existencias**|Estándar|  
|**Coste estándar**|$ 150,00|  
|**Tasa costos generales**|$ 25,00|  

En la tabla siguiente se muestra cómo está configurado el centro de trabajo en la ficha de centro de trabajo.  

|Configurar el campo|Valor|  
|-----------------|-----------|  
|**Costo unitario directo**|$ 2,00|  
|**Porcentaje de costo indirecto**|10|  

##### <a name="scenario" />Caso
1. El usuario compra 150 eslabones y registra el pedido de compra como recibido. (Compra)  
2. El usuario registra el pedido de compra como facturado. Esto crea un importe general de 3,00 $ que debe asignarse y un importe de desviación de 18,00 $. (Compra)  

    1. Se borran las cuentas provisionales. (Compra)  
    2. Se registra el costo directo. (Compra)  
    3. Se calcula y se registra el costo indirecto. (Compra)  
    4. La desviación de compra se calcula y se registra (solo en los productos de costo estándar). (Compra)  
3. El usuario vende una cadena y registra el pedido de venta como enviado. (Venta)  
4. El usuario registra el pedido de venta como facturado. (Venta)  

    1. Se borran las cuentas provisionales. (Venta)  
    2. El costo de productos vendidos (CV) se registra. (Venta)  

        ![Resultados de los registros de ventas con las cuentas de contabilidad.](media/design_details_inventory_costing_3_gl_posting_sales.png "Resultados de los registros de ventas con las cuentas de contabilidad")  
5. El usuario registra el consumo de 150 eslabones, que es el número de eslabones usados para producir una cadena. (Consumo, Material)  

    ![Resultados de los registros de material con las cuentas de contabilidad.](media/design_details_inventory_costing_3_gl_posting_material.png "Resultados de los registros de material con las cuentas de contabilidad")  
6. El centro de trabajo ha usado 60 minutos para producir la cadena. El usuario registra el costo de conversión. (Consumo, Capacidad)  

    1. Se registran los costes directos. (Consumo, Capacidad)  
    2. Se calculan y se registran los costes indirectos. (Consumo, Capacidad)  

        ![Resultados de los registros de capacidad con las cuentas de contabilidad.](media/design_details_inventory_costing_3_gl_posting_capacity.png "Resultados de los registros de capacidad con las cuentas de contabilidad")  
7. El usuario registra el costo esperado de una cadena. (Salida)  
8. El usuario acaba la orden de producción y ejecuta el proceso **Valorar existencias - movs. producto**. (Salida)  

    1. Se borran las cuentas provisionales. (Salida)  
    2. El costo directo se transfiere de la cuenta de trabajo en curso a la cuenta de inventario. (Salida)  
    3. El costo indirecto (costos generales) se transfiere de la cuenta de costo indirecto a la cuenta de inventario. (Salida)  
    4. Esto genera un importe de desviación de 157,00 $. Las desviaciones solo se calculan para los productos de costo estándar. (Salida)  

        ![Resultados de los registros de salida con las cuentas de contabilidad.](media/design_details_inventory_costing_3_gl_posting_output.png "Resultados de los registros de salida con las cuentas de contabilidad")  

        > [!NOTE]  
        >  Por simplificar, se muestra solo una cuenta de desviación. En la realidad hay cinco cuentas distintas:  
        >   
        >  * Desviac. material  
        >  * Desviac. capacidad  
        >  * Desviación cost. gen. capdad.  
        >  * Desviac. de subcontratación  
        >  * Desviación coste gen. fab.  

9. El usuario revaloriza la cadena de 150,00 $ a $ 140,00. (Ajuste/Revalorización/Redondeo/Transferencia)  

    ![Resultados de los registros de ajustes con las cuentas de contabilidad.](media/design_details_inventory_costing_3_gl_posting_adjustment.png "Resultados de los registros de ajustes con las cuentas de contabilidad")  

Para obtener más información acerca de la relación entre los tipos de cuenta y los distintos tipos de movimientos de valoración, consulte [Detalles de diseño: cuentas de contabilidad](design-details-accounts-in-the-general-ledger.md).  

## <a name="see-also" />Consulte también
[Detalles de diseño: Costo de inventario](design-details-inventory-costing.md)   
[Detalles de diseño: Registro de costo esperado](design-details-expected-cost-posting.md)   
[Detalles de diseño: Ajuste de costo](design-details-cost-adjustment.md)
[Gestión de costos de inventario](finance-manage-inventory-costs.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
