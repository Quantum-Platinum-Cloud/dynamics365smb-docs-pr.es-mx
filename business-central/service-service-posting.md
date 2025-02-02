---
title: Registro de servicio
description: La funcionalidad de registro de servicios le permite procesar los documentos de manera eficaz y mantener una política de servicio al cliente satisfactoria.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="service-posting" />Registro de servicio
La funcionalidad de registro de servicios le permite procesar los documentos de manera eficaz y mantener una política de servicio al cliente satisfactoria. Puede crear y actualizar documentos registrados, así como crear movimientos en el área de servicio y en otros módulos para garantizar una correcta actualización.  

> [!NOTE]  
>  A continuación se describe el registro del servicio independientemente del modo en que los artículos se controlan en el almacén.  
>   
>  En una ubicación en la que no se haya establecido el control de almacén como elemento obligatorio, las acciones de registro se realizan directamente desde la página **Líneas servicio**. En ubicaciones que requieran control de almacén, las acciones de registro descritas, salvo Enviar y Consumir, se realizan indirectamente mediante distintas funciones de envío de almacén, dependiendo de la configuración. Para obtener más información, vea [Realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship" />Envío
La opción enviar permite registrar el tiempo y los productos que se hayan especificado en las líneas de un pedido de servicio una vez haya finalizado el servicio. Se crea una entrega registrada y se llevan a cabo actualizaciones en el módulo Inventario y otros módulos de [!INCLUDE[prod_short](includes/prod_short.md)] a fin de reflejar que los productos se han excluido del inventario y se han enviado al cliente. En concreto, se generan movimientos de producto, de valores, de servicio y de garantía.  

Si el almacén está configurado para requerir el control de almacén, el envío y el movimiento de los productos de línea de servicio funcionan de la misma forma que para otros documentos de origen. La única diferencia es que los productos de línea de servicio pueden consumirse externa o internamente, lo cual requiere dos funciones diferentes de lanzamiento.

## <a name="invoice" />Facturar
Esta opción se utiliza a fin de emitir una factura para el cliente al que desea cobrar el servicio. Normalmente, la factura recoge la diferencia entre la cantidad enviada registrada por la función **Registrar envío** y la cantidad consumida registrada por la función **Registrar consumo**. No se puede facturar algo que no se ha enviado. Al ejecutar la función **Registrar factura**, crea una factura de servicio registrada y actualiza los documentos registrados antes de concordarlos con las cantidades que se incluyen en la factura emitida. Al igual que en otros procedimientos de registro, se generan los movimientos correspondientes, incluidos los de contabilidad.  

## <a name="ship-and-invoice" />Entregar y facturar
La opción de envío y facturación permite realizar entregas de servicio y de factura al mismo tiempo.  

## <a name="ship-and-consume" />Enviar y consumir
Con la opción consumo puede registrar los productos, los costos o las horas que se hayan empleado en un servicio pero que no se pueden incluir en la factura del cliente. No se emite una factura, pero puede emitir documentos de entrega y de consumo de servicio de forma simultánea a fin de reflejar que algunos productos u horas se han proporcionado al cliente sin cargo alguno. Asimismo, se crean los movimientos correspondientes para registrar el consumo.  

> [!NOTE]  
>  El procedimiento de registro de servicios permite realizar un registro parcial. Puede crear un envío o factura parciales rellenando los campos **Cantidad a enviar** y**Cdad. a facturar** en las líneas de servicio individuales de los pedidos de servicio antes del registro. Tenga en cuenta que no puede crear una factura de algo no se ha enviado. Es decir, para poder facturar, debe haber registrado un envío, o bien debe elegir enviar y facturar al mismo tiempo.  

Una vez completado el registro, podrá ver los documentos de servicio registrados desde las páginas correspondientes **Entrega de servicio regis.** y **Factura servicio registrada**. Los movimientos registrados que se han creado pueden verse en diversas páginas que contienen movimientos registrados, como **Movs. contabilidad**, **Movs. producto**, **Movs. almacén**, **Movs. servicio**, **Movs. proyectos** y **Movs. garantía**.  

## <a name="to-view-information-about-a-posted-service-document" />Para ver información sobre un documento de servicio registrado
Cuando se registra una factura, una remisión o una nota de crédito de servicio, la información del documento se transfiere a las páginas **Fact. ventas (servicio) regis.**, **Entrega de servicio registrado** o **Nota de crédito de ventas (servicio) regis.** respectivamente. No puede escribir, modificar ni eliminar información en estas páginas. En ellas puede imprimir un albarán, una factura o una nota de crédito de.  

El procedimiento siguiente utiliza una factura de servicio registrada como ejemplo, pero es posible aplicar el mismo procedimiento a las entregas de servicio registradas y al histórico de notas de crédito.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Factura de servicio registrada** y, a continuación, elija el vínculo relacionado.  
2. Abra la factura de servicio registrada que desee ver.  
3. Para obtener un resumen de la factura registrada, elija la acción **Estadísticas**.  

    Se abre la página **Estad. pedido servicio**. Dicha página muestra información tal como la cantidad, el importe, el IVA, el costo, los beneficios y el crédito máximo del cliente en el documento registrado.

## <a name="see-also" />Consulte también
[Registrar pedidos de servicio](service-how-to-post-service-orders.md)   
[Crear pedidos de servicio](service-how-to-create-service-orders.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
