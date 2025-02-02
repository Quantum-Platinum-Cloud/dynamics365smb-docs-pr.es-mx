---
title: Creación de presupuestos contables
description: Describe cómo crear presupuestos contables para prever diferentes actividades financieras y asignar dimensiones para fines de inteligencia empresarial.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '113, 120, 121, 154, 350, 422, 7132, 7133, 7138, 7139, 9203, 9219, 9239, 9373, 9374'
ms.date: 08/24/2022
ms.author: edupont
---
# <a name="create-gl-budgets" />Crear presupuestos contables

Puede tener varios presupuestos para idénticos periodos de tiempo si crea presupuestos con nombres distintos. En primer lugar, debe configurar el nombre del presupuesto e introducir las cifras del presupuesto. El nombre del presupuesto se incluye en todos los movimientos de presupuesto que cree.  

Al crear un presupuesto, puede definir cuatro dimensiones específicas del presupuesto, llamadas dimensiones presupuestarias, para cada presupuesto. Seleccione las dimensiones de presupuesto para cada uno de los presupuestos a partir de las dimensiones que ya ha configurado. Es posible utilizar las dimensiones de presupuesto para filtrar en un presupuesto y para agregar información de dimensiones a movimientos de presupuesto. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

Los presupuestos juegan un papel importante en la inteligencia empresarial. Entre los ejemplos se incluyen los estados de cuenta financieros en función de los informes financieros que incluyen movimientos de presupuesto o al analizar los importes presupuestados frente a los reales en el catálogo de cuentas. Obtenga más información en [Inteligencia de negocios](bi.md).

En contabilidad de costos, trabaja con los presupuestos de costos de forma similar. Más información en [Crear presupuestos de costo](finance-create-cost-budgets.md).  

## <a name="to-create-a-new-gl-budget" />Para crear un nuevo presupuesto contable

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Presupuestos contables** y luego elija el enlace relacionado.  
2. Elija la acción **Editar lista** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Seleccione la acción **Editar presupuesto**.
4. En la parte superior de la página **Presupuesto** rellene los campos según sea necesario para definir lo que se muestra.  

    Solo se mostrarán los movimientos que contengan el nombre del presupuesto que ha introducido en el campo **Nombre presupuesto**. Dado que acaba de crear el nombre del presupuesto, no hay movimientos que coincidan con el filtro. Por tanto, la página está vacía.  
5. Para escribir una cantidad, seleccione la celda correspondiente de la matriz. Se abre la página **Movs. pptos. contabilidad**.  
6. Cree una nueva línea y rellene el campo **Importe**. Cierre la página **Movs. pptos. contabilidad**.  
7. Repita los pasos de 5 y 6 hasta que escriba todos los importes del presupuesto.  

> [!NOTE]  
> En la ficha desplegable **Filtros** puede filtrar la información de presupuesto por las dimensiones de presupuesto que haya configurado con ese nombre de presupuesto.

## <a name="exporting-and-importing-gl-budgets-with-excel" />Exportar e importar presupuestos contables con Excel

Prácticamente en todas las demás páginas, puede exportar datos en páginas de presupuesto a Microsoft Excel para su posterior procesamiento o análisis. Más información en [Exportar los datos de negocio a Excel](about-export-data.md).

> [!NOTE]
> El catálogo de cuentas, en el que se basan los presupuestos de contabilidad general (G/L), tiene líneas de tipo de cuenta Mayor que contienen el total de las líneas siguientes. Cuando se exporta un presupuesto contable, se exportan los datos de todas las líneas independientemente del tipo de cuenta. Sin embargo, solo se pueden volver a importar los datos de las líneas del tipo Registro. 

En consecuencia, al importar un presupuesto contable, todos los valores que existían en las líneas de cabecera se eliminan. Esto sirve para evitar cantidades totales erróneas después de importar datos que se han creado o editado en Excel.

### <a name="scenario" />Escenario

Usted sabe que el nuevo costo de los salarios presupuestados será en moneda local ($) 1 200 000. Desea permitir que el departamento de Salarios presupueste las tres líneas específicas (de tipo de cuenta Publicación) para empleados a tiempo completo, empleados a tiempo parcial y ayuda temporal. Las tres líneas se agrupan bajo una línea de encabezado de Salarios.

Introduzca 1 200 000 en la línea Mayor, exporte el presupuesto a Excel, luego, envíelo al departamento de Salarios y dígales que distribuyan los $ 1 200 000.

El departamento de Salarios distribuye el importe en las tres cuentas contables. Cuando vuelve a importar al presupuesto contable, las tres cuentas se completan con los nuevos datos de Excel, que suman 1.200.000 $ y la línea Mayor está en blanco.

## <a name="see-related-microsoft-trainingtrainingmodulesbudgets-exchange-rates-dynamics-365-business-centralindex" />Consultar la [formación de Microsoft](/training/modules/budgets-exchange-rates-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también .

[Exportar los datos de negocio a Excel](about-export-data.md)  
[Finanzas](finance.md)  
[Inteligencia empresarial](bi.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
