---
title: Permitir los pagos de clientes mediante servicios de pago | Documentos de Microsoft
description: Facilite a los clientes el pago de las facturas activando los servicios de pago.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5853080ef39196e95c293415e9b81502ff03d5ed
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a>Permitir los pagos de clientes mediante servicios de pago
Como alternativa a recopilar pagos a través de transferencia bancaria o tarjetas de crédito, los clientes pueden pagar a través de su cuenta con servicios de pago, como Microsoft Pay, PayPal o WorldPay.  

Al habilitar un servicio de pago en [!INCLUDE[d365fin](includes/d365fin_md.md)], hay disponible un vínculo al servicio en los documentos de venta que envíe por correo electrónico a los clientes. Los clientes pueden utilizar el vínculo para ir al servicio de pago y pagar la factura, directamente desde el documento de venta. Si no desea incluir el vínculo, por ejemplo, si un cliente paga en efectivo, puede quitar el servicio de pago de la factura antes de registrarla.  

Las extensiones Microsoft Pay, estándar de pagos de PayPal y estándar de pagos de WorldPay están instaladas en [!INCLUDE[d365fin](includes/d365fin_md.md)] y están preparadas para que las active.  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a>Para activar un servicio de pago en [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Servicios de pago** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Servicios de pago**, seleccione la acción **Nuevo**.  
3. Seleccione el servicio de pago y luego cierre la ventana.  
4. En la ventana **Servicios de pago**, seleccione la acción **Configuración**.  
5. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Cierre la ventana.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Para seleccionar un servicio de pago en una factura de ventas
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas venta** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la factura de venta que desee pagar mediante el servicio de pago.  
3. En el campo **Servicio de pago**, elija el servicio de pago.  

    > [!NOTE]  
    > El campo **Servicio de pago** solo está disponible si ha activado el servicio de pago.  

## <a name="see-also"></a>Consulte también  
[Configuración de ventas](sales-setup-sales.md)  
[Ventas](sales-manage-sales.md)  
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] usando extensiones](ui-extensions.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
