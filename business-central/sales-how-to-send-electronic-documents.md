---
title: Enviar documentos electrónicos
description: Aprenda a utilizar Business Central para enviar facturas y notas de crédito electrónicos en formato PEPPOL.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="send-electronic-documents" />Enviar documentos electrónicos

La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] admite el envío de facturas electrónicas y notas de crédito en formato PEPPOL, un formato admitido por los proveedores de servicios de intercambio de documentos más importantes. El proveedor de servicios de intercambio de documentos entrega documentos electrónicos de un socio comercial a otro. Para proporcionar compatibilidad con otros formatos de documento electrónico, utilice el marco de intercambio de datos.  

 En la versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)], hay preconfigurado un servicio de intercambio de documentos listo para ser configurado según su empresa. Para obtener más información, vea [Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md). Sin embargo, en algunos casos, debe instalar una aplicación. Para más información, vea [Preguntas frecuentes sobre facturación electrónica](faq-electronic-invoicing.yml).  

 Para enviar una factura de venta como documento electrónico de PEPPOL, seleccione la opción **Documento electrónico** en el cuadro de diálogo **Registrar y enviar**. Puede configurar también perfil de envío de documentos predeterminado del cliente desde ese cuadro de diálogo. En primer lugar, debe configurar los distintos datos maestros, como la información de la empresa, los clientes, los productos y las unidades de medida. Se utilizan para identificar a los socios comerciales y los productos al convertir los datos de los campos de [Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)  

### <a name="to-send-an-electronic-sales-invoice" />Para enviar una factura de venta electrónica

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  

2. Cree una nueva factura de venta.  

3. Cuando la factura de venta esté lista para facturarse, seleccione la acción **Registrar y enviar**.  

     Si el perfil de envío predeterminado del cliente es **Documento electrónico**, entonces se mostrará en el cuadro de diálogo **Publicar y enviar confirmación**. De esta forma, solo tiene que elegir el botón **Sí** para contabilizar y enviar la factura de forma electrónica en el formato seleccionado.  

4. En el cuadro de diálogo **Registrar y enviar la confirmación**, seleccione el botón AssistEdit situado a la derecha del campo **Enviar documento a**.  

5. En el cuadro de diálogo **Enviar documento a**, en el campo **Documento electrónico**, seleccione **A través del servicio de intercambio de documentos**.  

6. En el campo **Formato**, seleccione **PEPPOL**.  

7. Elija el botón **Aceptar**. Aparece el cuadro de diálogo **Registrar y enviar la confirmación**. **Documento electrónico (PEPPOL)** se agrega al campo **Enviar documento a**.  

8. Elija el botón **Sí**.  

     Se registra la factura de venta y se envía al cliente en el formato PEPPOL.  

    > [!NOTE]  
    >  También puede enviar una factura de venta registrada como documento electrónico. El procedimiento es el mismo que el descrito en este tema para documentos de venta no registrada. En la página **Factura venta reg.**, elija la acción **Registro de actividades** para ver el estado del documento electrónico.  

## <a name="see-related-microsoft-trainingtrainingmoduleselectronic-documents-dynamics-365-business-centralindex" />Consultar la [formación de Microsoft](/training/modules/electronic-documents-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también

[Facturar ventas](sales-how-invoice-sales.md)  
[Configurar perfiles de envío de documentos](sales-how-setup-document-send-profiles.md)  
[Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Configurar un servicio de intercambio de documentos](across-how-to-set-up-a-document-exchange-service.md)  
[Configurar definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md)  
[Intercambio de datos en forma electrónica](across-data-exchange.md)  
[P+F sobre facturación electrónica](faq-electronic-invoicing.yml)  
[Funciones empresariales generales](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
