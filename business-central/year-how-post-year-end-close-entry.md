---
title: Revisar y registrar el movimiento de cierre del ejercicio | Documentos de Microsoft
description: "Describe cómo abrir el diario especificado en el proceso Cerrar resultados y, a continuación, revisar y registrar el movimiento de cierre de fin de año."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4263f6b3260dd5b8e8fad4f515dcdb61e12eb012
ms.contentlocale: es-mx
ms.lasthandoff: 03/22/2018

---
# <a name="post-the-year-end-closing-entry"></a>Registrar el movimiento de cierre del ejercicio
Después de usar el proceso **Asiento regularización** para generar los movimientos de cierre de fin de año, debe abrir el diario especificado en el proceso y revisar y registrar los movimientos.

## <a name="to-post-the-year-end-closing-entry"></a>Para registrar el movimiento de cierre del ejercicio
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario general** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Diario general**, en el campo **Nombre de sección**, seleccione la sección que contiene los movimientos de cierre.
3. Revise los movimientos.
4. Para registrar el diario, elija la acción **Registrar**.

> [!NOTE]  
>   Si se detecta algún error, se muestra un mensaje de error. Si el registro es correcto, se eliminan los movimientos registrados del diario. Una vez registrados, los movimientos se registran en cada una de las cuentas de regularización, de forma que sus saldos pasan a ser cero y el resultado del año se transfiere al balance.

## <a name="see-also"></a>Consulte también
[Cerrar periodos contables](year-close-account-periods.md)  
[Cierre de libros](year-close-books.md)  
[Asiento regularización](year-close-income-statement.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
