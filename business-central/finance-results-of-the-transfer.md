---
title: Resultados de transferencia | Documentos de Microsoft
description: "En este tema se describe qué ocurre después de transferir movimientos de contabilidad a los movimientos de costo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bc693bf3f3339b54a5d8d8847beb06c3fc018a0f
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Resultados de la transferencia de movimientos de contabilidad a movimientos de costo
Durante la transferencia de movimientos de contabilidad a movimientos de costo, [!INCLUDE[d365fin](includes/d365fin_md.md)]  crea conexiones en los movimientos de la tabla **Mov. contabilidad**, la tabla **Mov. costo** y la tabla  **Registro costos** para permitir realizar un seguimiento de las conexiones entre los movimientos de costos y los movimientos de contabilidad.  

## <a name="general-ledger-entries"></a>Movs. contabilidad  
Para cada movimiento de contabilidad que se transfiere a la contabilidad de costos, [!INCLUDE[d365fin](includes/d365fin_md.md)] rellena el campo de costo **N.º de movimiento**.  

## <a name="cost-entries"></a>Movs. costo  
Para cada movimiento de costo, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número de movimiento del movimiento de contabilidad correspondiente en el campo **Nº mov. contabilidad** en la tabla **Mov. costo**.  

Para movimientos de costo combinados, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número del movimiento del último movimiento de contabilidad, que es el movimiento con el número más alto de movimiento.  

El campo **Cuenta** en la tabla **Mov. costo** contiene el número de la cuenta de la que provino el movimiento de costo.  

Para movimientos de costo únicos, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere el texto de registro del movimiento de contabilidad al campo de texto **Descripción**. Para movimientos combinados, el campo de texto muestra que estos movimientos se transfieren como movimientos combinados. Por ejemplo, para un movimiento combinado del mes de octubre de 2013, el texto puede ser **Movimientos combinados, octubre de 2013**.  

## <a name="cost-register"></a>Registro costos  
En la tabla **Registro costos**, [!INCLUDE[d365fin](includes/d365fin_md.md)] crea un movimiento con la transferencia de origen de la contabilidad. El movimiento registra el primer y último número de los movimientos de contabilidad que se transfieren, además del primer y último número de movimientos de costo creados.  

## <a name="see-also"></a>Consulte también  
[Transferir movimientos de contabilidad general a movimientos de costo](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
[Criterios para la transferencia de movimientos de contabilidad a movimientos de costo](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md)   
[Transferencia automática y movimientos combinados](finance-automatic-transfer-combined-entries.md)   
[Transferencia y registro de movimientos de costo](finance-transfer-and-post-cost-entries.md)  
