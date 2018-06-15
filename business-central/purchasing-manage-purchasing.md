---
title: Resumen de tareas para administrar las compras | Documentos de Microsoft
description: Describe las tareas para administrar sus procesos de compra o aprovisionamiento, incluido el modo en que funcionan las facturas de compra y los pedidos de compra.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e4f27c9ad628fa66f692a862e59cd0b306b02c6c
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="purchasing"></a>Compra
Cree una factura o una orden de compra para registrar el costo de las compras y para realizar el seguimiento de los pagos. Si necesita controlar un inventario, las facturas de compra también se utilizan para actualizar dinámicamente los niveles de inventario para que pueda minimizar sus costos de inventario y proporcionar un mejor servicio al cliente. Los costos de compra, incluidos los gastos del servicio, y los valores de inventario resultantes del registro de las facturas de compra contribuyen a las cifras de ganancias y otros KPI financieros en el área de tareas.

Debe usar órdenes de compra si el proceso de compra requiere que registre recibos parciales de una cantidad de la orden, por ejemplo, porque el proveedor no disponía de la cantidad total. Si vende productos que se entregan directamente desde el proveedor al cliente, como remisión directa, debe usar también órdenes de compra. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md). En todos los demás aspectos, las órdenes de compra funcionan de la misma forma que las facturas de compra.

Puede crear facturas automáticamente mediante el servicio OCR (reconocimiento óptico de caracteres) para convertir facturas PDF de sus proveedores en documentos electrónicos, que se convierten en facturas de compra mediante un flujo de trabajo. Para usar esta funcionalidad, primero debe registrarse en el servicio OCR y, a continuación, realizar algunas configuraciones. Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).      

Los productos pueden ser productos de inventario y servicios. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

Para todos los procesos de compra, puede introducir un flujo de trabajo de aprobación, por ejemplo, para requerir que el administrador de contabilidad apruebe las compras grandes. Para obtener más información, vea [Uso de flujos de trabajo de aprobación](across-how-use-approval-workflows.md).

En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.

| Para | Vea |
| --- | --- |
| Cree una factura de compra para registrar el contrato con un proveedor para comprar productos según términos de entrega y pago determinados. |[Registrar compras](purchasing-how-record-purchases.md) |
|Cree una cotización de compra para reflejar una solicitud de cotización del proveedor, que puede convertir posteriormente en un pedido de compra.|[Solicitar cotizaciones](purchasing-how-request-quotes.md)|
| Crear una factura de compra para todas las líneas en una factura de venta o las seleccionadas. |[Comprar productos para una venta](purchasing-how-purchase-products-sale.md) |
| Realice una acción en una factura de compra registrada sin abonar para crear automáticamente una nota de crédito y para cancelar la factura de compra o regenerarla para poder hacer correcciones. |[Corregir o cancelar facturas de venta sin abonar](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Cree una nota de crédito de compras para revertir una factura de compra registrada específica para reflejar qué productos se están devolviendo al proveedor y qué importe de pago se cobrará. |[Procesamiento de devoluciones de compra o cancelaciones](purchasing-how-register-new-vendors.md) |
|Prepárese a facturar varios albaranes del mismo proveedor una vez combinándolos en una factura.|[Agrupar albaranes en una factura única](purchasing-how-to-combine-receipts.md)|
| Aprenda cómo [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula cuando se debe solicitar un producto para recibirlo en una fecha determinada.|[Cálculo de la fecha de compras](purchasing-date-calculation-for-purchases.md)|

## <a name="see-also"></a>Consulte también
[Configurar compras](purchasing-setup-purchasing.md)  
[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md)  
[Administrar pagos](payables-manage-payables.md)  
[Administrar proyectos](projects-manage-projects.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
