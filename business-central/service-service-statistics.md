---
title: Estadísticas servicio
description: 'Obtenga una visión general del contenido y las estadísticas de los documentos de servicio, como órdenes, cotizaciones, facturas, notas de crédito, líneas de servicio, etc.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---

# <a name="viewing-service-statistics" />Visualización de estadísticas de servicio
Puede utilizar estadísticas para analizar los documentos de servicio y determinar el cómo de bien está gestionando sus procesos de servicio. Puede analizar los contratos de servicio, los productos, las cotizaciones, las órdenes, las facturas y las notas de crédito si elige la acción **Estadísticas**. Para los productos y los contratos de servicios, también puede usar **Análisis prod. servicio** o **Análisis contrato** para ver un resumen de los movimientos de servicio para un producto de servicio determinado.   

## <a name="viewing-statistics-for-service-orders" />Visualización de estadísticas de un pedido de servicio
La función estadísticas de pedido de servicio le da una rápida visión general del contenido de todo el pedido de servicio, los detalles de las líneas de servicio específicas e información relacionada con la facturación, el envío, el consumo y la deuda del cliente.  

Los datos estadísticos del pedido de servicio pertinente se muestran en la página **Estadísticas pedido servicio**. Puede abrir la página de estadísticas relevante desde un pedido de servicio. En la página **Pedidos de servicio** seleccione **Estadísticas**. Las fichas desplegables de esta página muestran información acerca de cantidad, importe, IVA, costo, beneficio y límite de crédito del cliente. Los importes incluidos en la página están en la misma divisa que el pedido de servicio, a menos que se indique lo contrario.  

### <a name="view-totals-for-a-service-order" />Ver totales de un pedido de servicio
Puede ver el importe total en las líneas de servicio, con y sin IVA, el importe de IVA, el costo y el beneficio de las líneas de servicio. La página también muestra información específica de productos, como el peso, el volumen, y la cantidad de lotes.  

### <a name="view-shipping-information" />Visualización de información de envío
Puede ver la información sobre los productos, los recursos o los costos de envío. Para obtener esta información, se utilizan los valores especificados en el campo **Cantidad a enviar** de cada línea de servicio del pedido.  

### <a name="view-order-details" />Ver detalles de pedido
Puede ver la información sobre los productos, las horas de los recursos y los costos que se van a facturar y consumir. La siguiente tabla describe esta informaicón.  

|Columna | Descripción|  
|------------|---------------------------------------|  
|**Facturación**|Muestra importes del pedido de servicio que se van a registrar como facturados.|  
|**Consumo**|Muestra la cantidad y el costo de los artículos o recursos que se registrarán como consumidos.|  
|**Total**|Muestra los importes totales del pedido de servicio que se obtienen como resultado de sumar los importes de facturación con los importes de consumo.|  

### <a name="analyze-service-order-lines" />Analizar líneas de pedido de servicio
Puede analizar la información por los tipos de líneas de servicio incluidos en el pedido de servicio. Los importes se muestran por separado para:  

* Productos  
* Recursos  
* Costos y cuentas contables  

### <a name="view-customer-information" />Ver Información de cliente
Vea el saldo de la cuenta del cliente, además del crédito máximo que se puede facilitar al cliente para el que ha creado el documento de servicio.

## <a name="viewing-service-item-statistics" />Visualización de estadísticas de producto de servicios
En la página **Estadísticas de productos de servicio**, puede ver la información actualizada acerca un producto de servicio basada en los siguientes tipos de registros de movimientos de servicio:  

* Recursos  
* Productos  
* Costo de servicio  
* Contratos de servicio  
* Total  

Para cada tipo de movimiento, puede ver el importe facturado, la utilización (importe), el importe de costo, la cantidad, la cantidad facturada y consumida, el importe de las ganancias y el porcentaje de las ganancias. El porcentaje de las ganancias se calcula según la fórmula siguiente:  

* (Importe de la factura - Utilización (costo)) x 100/Importe de la factura  

## <a name="use-trendscapes" />Usar Trendscapes
Para productos de servicio y contratos de servicio, las páginas **Análisis producto de servicio** o **Análisis contrato de servicio** proporciona un resumen desplazable de movimientos de servicio de un periodo de tiempo para un producto o un contrato de servicio determinado. Para ver el análisis, abra el producto de servicio o el contrato de servicio, elija la acción **Estadísticas** y después seleccione **Análisis**.

Al desplazarse en la lista, los importes se calculan en la divisa loca según el intervalo de tiempo especificado. Se calculan todos los importes procedentes de los movimientos de servicio, los cuales son movimientos creados al registrar pedidos de servicio o facturas de servicio.

Puede filtrar la lista especificando los productos de servicio a incluir.  

> [!Tip]  
>  Si ha definido el intervalo de tiempo como **Día** y desea examinar un periodo largo, conviene cambiar a un intervalo más amplio, como **Trimestre**. Una vez que haya encontrado el periodo deseado, puede volver al intervalo original para ver los datos con más detalle.   

## <a name="viewing-gains-and-losses-on-contracts" />Visualización de beneficios y pérdidas en contratos
Los movimientos de beneficios o pérdidas de contrato se generan cuando se convierte una cotización de contrato a un contrato de servicio, cuando se agregan o eliminan líneas de contrato de un contrato de servicio o cuando se cancela un contrato. Puede ver las pérdidas y ganancias de contrato en las páginas siguientes.  

|Página | Descripción|  
|----------------|---------------------------------------|  
|**Pérd./gan. contr. (Contratos)**|Para ver las pérdidas y ganancias de contrato por contrato de servicio.|  
|**Pérd./gan. contrato (Grupos)**|Para ver las pérdidas y ganancias de contrato por grupo de contrato de servicio.|  
|**Pérd./gan. contrato (Clientes)**|Para ver las pérdidas y ganancias de contrato por cliente.|  
|**Pérd./gan. contrato (Razones)**|Para ver las pérdidas y ganancias de contrato por código de razón.|  
|**Pérd./gan. contr. (Cen. resp.)**|Para ver las pérdidas y ganancias de contrato por centro de responsabilidad.|  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , ingrese el nombre de la página que se mostrará y luego elija el enlace relacionado.  
2. Rellene los criterios del filtro que desea aplicar. Por ejemplo, en la página **Pérdidas/ganancias en contrato (Razones)**, seleccione un valor para **Filtro código razón**.  
3. Elija la acción **Mostrar matriz**.

## <a name="viewing-statistics-for-posted-service-documents" />Visualización de estadísticas de documentos de servicio registrados
La función de estadísticas de servicio permite obtener un resumen estadístico del contenido de los documentos de servicio registrados, como envío registrado, factura registrada y nota de crédito registrada.  

La información estadística se muestra en la página de estadísticas del documento de servicio registrado correspondiente. Puede abrir la página de estadísticas correspondiente desde la entrega de servicio registrado, la factura de servicio registrada o los documentos de nota de crédito de servicio registrados. Para cada uno de estos tipos de documento, elija la acción **Estadística**. Por ejemplo, en la página **Facturas servicios reg.**, elija la acción **Estadística**.  

### <a name="posted-service-shipment-statistics" />Estadísticas de entregas de servicios registradas
La página **Estadísticas entrega de servicio** proporciona un resumen de un entrega de servicio registrado. Esto incluye información sobre el contenido físico del envío, como la cantidad de productos enviados, las horas o los costos de los recursos y el peso y el volumen de los productos enviados.  

### <a name="posted-service-invoice-statistics" />Estadísticas de facturas de servicios registradas
Puede ver un resumen estadístico de una factura de servicio registrada en la página **Estadísticas facturas servicios**. Puede ver los totales de la factura de servicio registrada. Estos datos incluyen el importe total de las líneas de servicio (con y sin IVA) que se han registrado como facturadas, el importe del IVA, el costo y el beneficio de la factura registrada. Las página también muestra la siguiente información:  

* Los productos en las líneas de factura de servicio, como el peso, el volumen y la cantidad de lotes.  
* El saldo de la cuenta de cliente y el crédito máximo que puede ampliar al cliente.  

### <a name="posted-service-credit-memo-statistics" />Estadísticas de notas de crédito de servicios registradas
Puede utilizar la página **Estadísticas de nota de crédito de servicios** para obtener un resumen estadístico de las líneas de una nota de crédito de servicio registrada. El resumen puede incluir:

* Los importes totales de la nota crédito registrada, mostrados como cantidad, importe, IVA, costo y beneficio. Asimismo, es información sobre los productos de las líneas de servicio de la nota crédito registrada, como la cantidad, el peso y el volumen.  
* Información general sobre el cliente, como su límite de crédito y el saldo de su cuenta.  

## <a name="see-also" />Consulte también
[Crear pedidos de servicio ](service-how-to-create-service-orders.md)   
[Crear productos de servicio](service-how-to-create-service-items.md)   
[Servicio de planificación](service-plan-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
