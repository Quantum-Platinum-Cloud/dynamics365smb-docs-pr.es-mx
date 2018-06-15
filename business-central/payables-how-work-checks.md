---
title: Emitir, imprimir, cancelar y anular cheques | Documentos de Microsoft
description: "Describe cómo emitir cheques con el diario de pagos, imprimir cheques y anular o ver movimientos de cheques en Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: es-mx
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a>Realizar pagos por cheque
Puede emitir cheques electrónicos y manuales en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ambos métodos utilizan el diario de pagos para emitir los cheques a proveedores. También puede anular cheques y ver movimientos de cheques.

El siguiente procedimiento muestra cómo pagar a un proveedor con cheques por ordenador, mediante la liquidación del pago a la factura del proveedor relevante, la impresión del cheque y la contabilización del pago como pagado. Esto da como resultado entradas positivas en la contabilidad del proveedor, aplicadas a las entradas negativas y a los cheques físicos para el procesamiento en el banco.

Puede pagar con dos tipos de cheques. Para ambos tipos, el campo **Tipo contrapartida** o **Tipo de cuenta** debe contener **Cuenta bancaria**.

- **Cheque automático**: Seleccione esta opción si desea imprimir un cheque por el importe de la línea del diario de pagos. Debe imprimir los cheques antes de que pueda registrar las líneas del diario. Sólo puede seleccionar **Cheque automático** si
- **Cheque manual**: Seleccione esta opción si ha creado manualmente un cheque y desea crear el movimiento de cheque correspondiente a ese importe. Usando esta opción no puede imprimir el cheque.

> [!NOTE]  
> Para asegurarse de que su banco solo compensa cheques e importes validados, puede enviarles un archivo que contenga la información de proveedor, cheque y pago. Para obtener más información, vea [Exportar un archivo de Positive Pay](finance-how-positive-pay.md).

Su impresora tiene que haber configurado correctamente los documentos y usted deberá definir qué plantilla de cheques va a usar. Para obtener más información , vea [Definir plantillas de cheques](finance-how-define-check-layouts.md)

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Para pagar una factura de proveedor con un cheque automático
A continuación se describe cómo pagar a un proveedor mediante un cheque. Los pasos son similares al reembolso de un cheque.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de pagos** y, a continuación, seleccione el vínculo relacionado.
2. Rellene las líneas del diario de pagos. Para obtener más información, vea [Registre pagos y reembolsos](payables-how-post-payments-refunds.md).
3. En el campo **Cód. forma pago**, seleccione **Cheque**.
4. En el campo **Tipo pago por banco**, seleccione **Cheque automático**.
5. Seleccione la acción **Imprimir cheque**.
6. En la ventana **Cheque**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Seleccione el botón **Enviar a**, seleccione la opción **Documento PDF** y, a continuación, el botón **Aceptar**.

    Los cheques físicos ahora se pueden llevar al banco para que los procesen. Proceda a publicar el pago tal como se le aplica al proveedor y, por lo tanto, pagado en el sistema.
8. Seleccione la acción **Registrar**.

Se crean los movimientos de contabilidad de proveedores y de cuenta bancaria totalmente aplicados.

> [!NOTE]  
> Si quiere imprimir y pagar cheques en varias divisas de cuentas bancarias distintas, deberá ejecutar el proceso **Imprimir cheque** por separado para cada divisa y especificar la cuenta bancaria correspondiente.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Para anular los cheques imprimidos que no han sido registrados
Puede anular los cheques no registrados después de que hayan sido imprimidos usando la acción **Anular cheque** de la ventana **Diario de pagos**.

1. En la ventana **Diario de pagos**, seleccione **Anular cheque** y, a continuación, seleccione que cheques desea cancelar.

## <a name="to-void-checks"></a>Para anular cheques
Cuando se ha registrado el pago del cheque, solo puede cancelar (anular) cheques en los movimientos resultantes del banco.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cuentas bancarias** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la cuenta bancaria correspondiente, seleccione la acción **Editar** y, a continuación, seleccione la acción **Movs. cheques**.
3. En la ventana **Movs. cheques**, seleccione la acción **Anular cheque**.
4. Seleccione la casilla **Anular cheque solo**.
5. Elija el botón **Aceptar**.

## <a name="to-view-a-summary-of-posted-checks"></a>Para ver un resumen de los cheques registrados
Si desea revisar los cheques registrados, por ejemplo, para verificar los cheques múltiples pagados a un proveedor, puede usar el informe **Bancos - Desglose cheques**.
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Bancos - Desglose cheques** y, a continuación, seleccione el vínculo relacionado.
2. Establezca los filtros como relevantes y luego elija el botón **Vista previa**.

## <a name="see-also"></a>Consulte también
[Creación de pagos](payables-make-payments.md)  
[Administrar pagos](payables-manage-payables.md)  
[Configurar banca](bank-setup-banking.md)  
[Exportar un archivo de Positive Pay](finance-how-positive-pay.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
