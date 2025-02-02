---
title: 'Procedimientos recomendados de configuración: políticas de reorden | Documentos de Microsoft'
description: El campo Política reorden en las fichas de producto ofrece cuatro métodos de planificación distintos que determinan la forma en que interactúan los parámetros individuales de planificación.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setup-best-practices-reordering-policies" />Procedimientos recomendados de configuración: políticas de reorden

El campo **Política reorden** en las fichas de producto ofrece cuatro métodos de planificación distintos que determinan la forma en que interactúan los parámetros individuales de planificación.  

Un procedimiento recomendado básico para seleccionar una política de reorden es la clasificación ABC del producto. Cuando se utiliza la clasificación ABC para el control y la planificación de suministros de inventario, los artículos se gestionan según tres clases distintas, en función del valor y el volumen en relación con las existencias totales. La distribución valor-volumen de las tres clases se muestra en la tabla siguiente.

|Clase|Porcentaje de volumen de existencias totales|Porcentaje de valor de existencias totales|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|nº 20|nº 20|
|P|60-70|10-30|

La clasificación ABC indica que se puede ahorrar esfuerzo y dinero aplicando un control más ligero a los artículos de bajo valor-volumen bajo que a los artículos de alto valor-volumen. Las ilustración siguiente muestra qué política de reorden de [!INCLUDE[prod_short](includes/prod_short.md)] es más adecuada para los artículos A, B, y C respectivamente.

![Clasificación ABC.](media/abc_classification.png "abc_classification")

La tabla siguiente proporciona los procedimientos recomendados para seleccionar entre las cuatro políticas.  

|Opción de configuración|Procedimiento recomendado|Comentario|  
|------------------|-------------------|-------------|  
|**Pedido**|Utilice para productos A.<br /><br /> Utilice para productos de fabricación contra pedido.<br /><br /> En la fabricación, utilice para productos de nivel superior y para componentes y semiterminados caros.<br /><br /> Utilice para productos que se compran como envíos directos y pedidos especiales.<br /><br /> No utilice si no acepta la reserva automática.|Los productos A, como los sofás de piel en una tienda muebles, son productos de alto valor con una velocidad de pedido baja e irregular donde no se acepta el inventario o los atributos necesarios varían. La mejor política de reorden es, por tanto, aquella que planifica específicamente para cada demanda.|  
|**Lote a lote**|Utilice para productos B.<br /><br /> En la fabricación, utilice para los componentes que se producen en varias listas de materiales. Esto garantiza que los pedidos de compra se combinen para el mismo proveedor, por lo que se pueden negociar mejores precios.<br /><br /> Utilice si no está seguro de la política de reorden que debe seleccionar.|Los productos B, como las sillas de comedor, tienen una velocidad de pedido regular y bastante alta, pero también costos de traslado elevados. La mejor política de reorden para los productos B es, por tanto, aquella que es económica y agrupa la demanda en el ciclo de reorden.<br /><br /> El 80 por ciento de los productos pueden utilizar esta política.<br /><br /> Se puede utilizar con éxito sin los parámetros de planificación.|  
|**Cdad. fija reordenada**|Utilice para productos C.<br /><br /> Combine con parámetros de puntos de reorden.<br /><br /> En la fabricación, utilice para los componentes de nivel inferior.<br /><br /> No utilice si el producto suele ser reservado.|Los productos C, como las tazas de té, son productos de valor inferior con una velocidad de pedido alta y regular. La mejor política de reorden para productos C es, por tanto, aquella que garantiza la disponibilidad constante y permanece siempre por encima de un punto de reorden.<br /><br /> Si el usuario reserva una cantidad para alguna demanda distante, se afectará a la base de la planificación. Aunque el nivel de inventario estimado es aceptable en relación con el punto de reorden, las cantidades pueden no estar disponibles debido a la reserva.|  
|**Cdad. máxima**|Utilice para productos C con altos costos de traslado o limitaciones de almacenamiento.<br /><br /> Combine con uno o más modificadores de pedidos (cantidad máxima o mínima de pedido o múltiplos de pedido).|Los productos C, como las tazas de té, son productos de valor inferior con una velocidad de pedido alta y regular. La mejor política de reorden para productos C es, por tanto, aquella que garantiza la disponibilidad constante y permanece siempre por encima de un punto de reorden, pero por debajo de un nivel de inventario máximo.<br /><br /> Para modificar el pedido propuesto, tal vez desee reducir la cantidad del pedido a una cantidad máxima especificada de pedido, aumentarla a una cantidad de pedido mínima especificada o redondearla para alcanzar un múltiplo de pedido especificado. **Nota**: Si se utiliza con un punto de reorden, el inventario permanecerá entre el punto de reorden y la cantidad máxima.|  

## <a name="see-related-microsoft-trainingtrainingpathsreplenish-items-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/paths/replenish-items-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

 [Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
 [Detalles de diseño: Gestión de directivas de reorden](design-details-handling-reordering-policies.md)  
 [Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
