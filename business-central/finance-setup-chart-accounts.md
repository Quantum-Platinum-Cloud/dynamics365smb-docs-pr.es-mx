---
title: Configurar un plan contable
description: "Puede cambiar las cuentas predeterminadas en el catálogo de cuentas (COA) y puede agregar nuevas cuentas."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 9f84af8bb4ac3be9132ab621906c463cfc9b91ff
ms.contentlocale: es-mx
ms.lasthandoff: 05/17/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a>Configurar o cambiar el catálogo de cuentas
El catálogo de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros. [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.
Sin embargo, puede cambiar las cuentas predeterminadas y puede agregar nuevas cuentas.  

## <a name="adding-or-changing-accounts"></a>Agregar o cambiar cuentas
Desde el catálogo de cuentas, puede abrir cada cuenta de contabilidad y agregar o cambiar opciones.

> [!NOTE]  
>   Puede eliminar una cuenta contable. Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:  

* El saldo de la cuenta debe ser cero.  
* El campo **Permite borrar ctas. anteriores a** se debe configurar en la ventana **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.  
* Si se selecciona el campo **Chequear uso ctas. cont.** en la ventana **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] impedirá que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el plan de cuentas.  

## <a name="see-also"></a>Consulte también
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de otros sistemas financieros](across-import-data-configuration-packages.md)(across-import-data-configuration-packages.md)  
[Trabajar con estructuras de cuentas](bi-how-work-account-schedule.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
