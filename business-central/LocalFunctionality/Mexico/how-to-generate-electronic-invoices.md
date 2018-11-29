---
title: "Procedimiento para generar facturas electrónicas"
description: "En Business Central, después de registrar una factura de venta, debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e3c70a8604fae1c4eaedeb06a37e139436e8f9fd
ms.contentlocale: es-mx
ms.lasthandoff: 09/28/2018

---
# <a name="generate-electronic-invoices"></a>Generar facturas electrónicas
Después de registrar una factura de venta en [!INCLUDE[d365fin](../../includes/d365fin_md.md)], debe generar una factura electrónica que se enviará al cliente. Asimismo, puede exportar dicha factura electrónica como un archivo XML, que puede guardar en una ubicación especificada.  

En el procedimiento siguiente se describe cómo generar facturas electrónicas para facturas de venta, aunque los mismos pasos también se aplican a facturas y notas de crédito de servicios.  

## <a name="to-generate-electronic-invoices-for-sales-invoices"></a>Para generar facturas electrónicas de facturas de ventas  

1.  Elija el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono de Buscar página o informe"), escriba **Factura venta reg.** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la factura registrada.  
3.  Elija la acción **Send Electronic Document**. De este modo, se enviará un correo electrónico al cliente con la factura electrónica adjuntada como archivo XML. Si seleccionó el campo **Enviar informe PDF** de la ventana **Configuración de contabilidad**, también se incluirá un documento PDF con el archivo XML.  
4.  Como alternativa, elija la acción **Exportar documento electrónico como XML**. Seleccione la ubicación donde desea guardar la factura electrónica como archivo XML.  

    Para comprobar la actividad de facturas electrónicas, en la ventana **Factura venta reg.**, en la ficha desplegable **Facturación**, se actualizarán los campos **Documento electrónico enviado** y **No. of E-Document Submissions**.  

> [!NOTE]  
>  ADD INCLUDE<!--[!INCLUDE[bp_refimplementation](../../includes/bp_refimplementation_md.md)]-->  

## <a name="see-also"></a>Consulte también  
 [Configurar la facturación electrónica](how-to-set-up-electronic-invoicing.md)   
  [Facturación electrónica](electronic-invoicing.md)  
  [Funcionalidad local de México](mexico-local-functionality.md)
