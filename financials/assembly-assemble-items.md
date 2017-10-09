---
title: "Gestión de ensamblado | Documentos de Microsoft"
description: "Apoyar a las empresas que suministran los productos a sus clientes agrupando los componentes en procesos sencillos sin necesidad de la funcionalidad de fabricación pero con características para ensamblar artículos que se integran con las existentes, como son planificación, reservas y almacén."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d945858b3a26126a2def48d88ff1132f598c0916
ms.contentlocale: es-mx
ms.lasthandoff: 09/22/2017

---
# <a name="assembly-management"></a>Gestión de ensamblaje
Para apoyar a las empresas que suministran los productos a sus clientes agrupando los componentes en procesos sencillos sin necesidad de la funcionalidad de fabricación, [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye las características para ensamblar artículos que se integran con las existentes, como son planificación, reservas y almacén.  

 Un producto de ensamblado se define como uno sellable que contenga un L.M. de ensamblado.

 Los pedidos de ensamblado son pedidos internos, como las órdenes de producción, que se utilizan para gestionar el proceso de ensamblado y para conectar los requisitos de venta con las actividades de almacén correspondientes. Los pedidos de ensamblado difieren de otros tipos de pedido porque implican la salida y el consumo cuando se están registrando. La cabecera del pedido de ensamblado se comporta de modo similar a una línea del pedido de venta, y las líneas del pedido de ensamblado se comportan de forma similar a las líneas del diario de consumo. Para obtener más información, consulte Pedido de ensamblado.  

 Para utilizar una estrategia de inventario puntual y la capacidad de personalizar los productos según las solicitudes del cliente, los pedidos de ensamblado pueden crearse y vincularse automáticamente tan pronto como se cree la línea del pedido de venta. El vínculo entre la demanda de venta y el suministro del ensamblado permite a los procesadores del pedido de venta personalizar el producto de ensamblado de forma dinámica, comprometer las fechas de entrega según la disponibilidad del componente, así como registrar la salida el envío del producto ensamblado directamente en la interfaz del pedido de venta. Para obtener más información, consulte [Procedimiento: Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

 En una línea del pedido de venta, puede vender una cantidad que está disponible y se debe realizar el picking de las existencias junto con una cantidad que se debe ensamblar para el pedido. Existen ciertas reglas para controlar la distribución de estas cantidades para asegurar que las cantidades de ensamblar para pedido tengan prioridad sobre las cantidades del inventario en un envío parcial. Para obtener más información, consulte la sección "Escenarios de combinación" en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Hay una funcionalidad especial para controlar el envío de las cantidades del ensamblar para pedido. Cuando una cantidad de ensamblar para pedido está lista para enviarse, el empleado del almacén responsable registra un picking de inventario para la línea o líneas en cuestión. A cambio, esto crea un movimiento de inventario para los componentes, registra la salida de ensamblado y el envío del pedido de venta. Para obtener más información, vea la sección "Tratamiento de productos ensamblar para pedido en los picking de inventario" en [Cómo realizar picking de productos con picking inventario](warehouse-how-to-pick-items-with-inventory-picks.md).

En la tabla siguiente se describe una secuencia de tareas, con vínculos a temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Saber la diferencia entre los artículos que ensamblan justo antes de los pedidos de venta de envío y los artículos que ensamblan para almacenamiento.|[Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Rellene los campos en las fichas de ubicación y en la configuración del inventario para definir cómo fluyen los artículos en el departamento de ensamblaje.|[Procedimiento: configure almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Personalizar un producto de ensamblado a la solicitud de un cliente durante el proceso de venta y convertirlo en venta cuando se acepte.|[Procedimiento: Cotización de una venta de ensamblar para pedido](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Agrupe los componentes para crear un artículo en un proceso sencillo, para pedido o para stock.|[Procedimiento: ensamble productos](assembly-how-to-assemble-items.md)|  
|Vender productos de ensamblado que no están disponibles actualmente mediante un pedido de ensamblado vinculado para suministrar la cantidad total o parcial del pedido de venta.|[Procedimiento: Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md)|
|Cuando algunos productos de ensamblar para pedido ya se encuentran en el inventario, descuente esa cantidad de pedido de ensamblado y resérvela del inventario.|[Procedimiento: Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Cuando está vendiendo productos de ensamblado del inventario y ninguno de los productos está disponible, inicie un pedido de ensamblado para suministrar automáticamente una parte o toda la cantidad del pedido de venta.|[Procedimiento: Venta de productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Deshacer un pedido de ensamblado registrado, por ejemplo porque la orden se publicó con errores que deben corregirse.|[Procedimiento: deshacer registro de ensamblado](assembly-how-to-undo-assembly-posting.md)|
|Saber la diferencia entre ensamblado L.M. y producción L.M. y las diferencias de procesamiento correspondientes.|[Trabajar con listas de materiales](inventory-how-work-BOMs.md)|
|Saber cómo se gestiona el consumo de ensamblado y a la salida cuando se registran los pedidos de ensamblado y cómo se procesan y se distribuyen a la contabilidad el artículo y los precios de costos de recurso derivados.|[Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a>Consulte también  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
