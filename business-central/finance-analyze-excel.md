---
title: Trabajar con resúmenes financieros en Excel
description: Obtenga más información sobre cómo abrir los informes de resultados financieros en Microsoft Excel desde Business Central para un mejor análisis.
author: edupont04
ms.topic: overview
ms.search.keywords: 'accountant, accounting, financial report'
ms.search.form: 9027
ms.date: 08/23/2022
ms.author: edupont
---
# <a name="analyzing-financial-statements-in-microsoft-excel" />Análisis de resultados financieros en Microsoft Excel

[!INCLUDE [prod_short](includes/prod_short.md)] proporciona indicadores clave de rendimiento (KPI) y obtiene una descripción general de las finanzas de su empresa. Los siguientes son ejemplos de formas de analizar KPI y resúmenes en Excel:

* Abra listas en Excel y analice los datos. 
* Exporte informes financieros de gran volumen como el balance o el balance de ingresos a Excel, analice los datos e imprima los informes.  

> [!TIP]
> De manera predeterminada, los informes que puede ver en Excel están diseñados para ayudarlo a analizar el año en curso. Sin embargo, el balance de ingresos es una excepción. Ese informe le permite filtrar los datos para incluir años anteriores en sus análisis.

## <a name="getting-the-overview-and-the-details-in-excel" />Obtención de panorama y detalles en Excel

En las áreas de tareas Administrador empresarial y Contador, la acción **Informes** le permite elegir los informes financieros para verlos en Excel. Cuando elige un estado de cuenta, se abrirá en Excel o Excel en línea. Un complemento conecta los datos a [!INCLUDE [prod_short](includes/prod_short.md)]. Sin embargo, tiene que iniciar sesión con la misma cuenta que utilice en [!INCLUDE [prod_short](includes/prod_short.md)]. En la tabla siguiente se enumeran los informes y dónde están disponibles.  


|Informar  |Área de tareas  |
|---------|---------|
|Saldo                 | Administrador empresarial, contable |
|Estado de cuenta de ingresos              | Administrador empresarial, contable |
|Estado de cuenta de flujos de caja       | Administrador empresarial, contable |
|Estado de cuenta de ganancias retenidas| Administrador empresarial, contable |
|Impuestos ventas recogidos         | Administrador empresarial, contable |
|Estados de cuenta de cliente           | Administrador empresarial, contable |
|Antigüedad pago         | Contable |
|Antigüedad de los cobros      | Contable |

Digamos que desea profundizar en su flujo de caja. En el área de tareas Administrador de negocio o Contador, puede abrir el informe **Estado de flujo de efectivo** en Excel, pero lo que realmente sucede es que exportamos los datos correspondientes y creamos un libro de Excel basado en una plantilla predefinida. Dependiendo de su navegador, se le pedirá que abra o guarde el libro.  

En Excel, ve una pestaña donde los datos se establecen en la primera hoja de cálculo. Todos los datos que se exportaron también están presentes en otras hojas de trabajo en caso de que lo necesite. Puede imprimir el informe de inmediato o puede modificarlo hasta que tenga el panorama y los detalles que desee. Utilice el complemento [!INCLUDE [prod_short](includes/prod_short.md)] de Excel para filtrar y analizar datos.  

### <a name="understanding-the-excel-templates" />Conocer las plantillas de Excel

Los informes de Excel predefinidos se basan en los datos de la empresa actual. Por ejemplo, la empresa de demostración ha configurado el catálogo de cuentas para enumerar tres cuentas de efectivo en *Activos circulantes*: 10100 **Cuenta de cheques**, 10200 **Cuenta de ahorro** y 10300 **Caja chica**. Las cuentas tienen el campo **Subcategoría de cuenta** establecido en *Efectivo* y es su cantidad combinada la que aparece como *Efectivo* en el informe de Excel **Balance**.  

Otras hojas del libro de Excel muestran los datos que hay detrás del informe. Para averiguar qué hay detrás de las agrupaciones en los informes de Excel, es posible que deba filtrar las listas en [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="the-include-prodshortincludesprodshortmd-excel-add-in" />Complemento [!INCLUDE [prod_short](includes/prod_short.md)] de Excel

Su experiencia con [!INCLUDE [prod_short](includes/prod_short.md)] incluye un complemento de Excel. Dependiendo de su suscripción, se iniciará sesión automáticamente o debe proprocioanr sus detalles de inicio de sesión para [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Ver y editar en Excel desde Business Central](across-work-with-excel.md).  

El complemento le permite obtener nuevos datos de [!INCLUDE [prod_short](includes/prod_short.md)], y puede insertar cambios en [!INCLUDE [prod_short](includes/prod_short.md)]. Sin embargo, la capacidad de insertar datos en la base de datos no está disponible para los informes financieros que peude ver en Excel.  

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Consultar la [formación de Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también

[Ver y editar en Excel desde Business Central](across-work-with-excel.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con Business Central](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
