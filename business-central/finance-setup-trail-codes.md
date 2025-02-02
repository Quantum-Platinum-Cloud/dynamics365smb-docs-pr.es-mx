---
title: Configurar códigos para trazas de auditorías
description: Aprenda sobre las tareas para configurar códigos de origen y códigos de auditoría que puede usar para realizar un seguimiento de pistas de auditoría.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails" />Configuración de códigos de origen y códigos de auditoría para pistas de auditoría

Todos los movimientos registrados se asignan automáticamente a un código de origen de forma que pueda realizarse un seguimiento del origen de las transacciones. Si desea asignar a los movimientos un código de origen adicional, utilice los códigos de motivo. Los códigos de motivo se utilizan para indicar el motivo por el que se ha creado un determinado movimiento. Al configurar códigos de auditoría, puede asignarlos a libros diario o a secciones de diarios, así como a líneas de diarios y a documentos individuales.  

Tanto para los códigos fuente como para los códigos de auditoría, use códigos que sean descriptivos y fáciles de recordar. El código debe ser único y puede configurar tantos códigos como desee.

## <a name="define-source-codes" />Definir los códigos de origen

A veces querrá saber cómo surge un movimiento determinado, por ejemplo, si procedía del registro de un diario general o de una factura de compra. Un código de origen indica dónde se creó un movimiento. Los movimientos se crean cuando se registran los diarios y facturas, y cuando se ejecutan determinados trabajos por lotes. Cada tipo de registro tiene un código de origen diferente que se asigna cuando se crean entradas individuales.  

El registro de diarios, pedidos, facturas o notas de crédito, así como la ejecución de diversos trabajos por lotes, genera movimientos en los estados de cuenta financieros. La página **Configuración códigos origen** contiene varias fichas desplegables, una por cada área de aplicación. Cada ficha desplegable contiene los códigos de origen correspondientes a esa área de aplicación.

Cuando registra o ejecuta un trabajo por lotes, el programa adjunta automáticamente el código de origen correspondiente al movimiento. Por ejemplo, al registrar desde el diario general, el programa codificará el movimiento con la abreviatura *DIAGEN*. Luego puede filtrar la página **Movs. contabilidad** para mostrar qué movimientos se publicaron desde el diario general o desde documentos de ventas, por ejemplo.

### <a name="to-define-source-codes" />Para definir códigos de origen

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono de Buscar por página o informe") , escriba **Configuración códigos origen** y luego elija el enlace relacionado.  

2. En la ventana **Configuración del código fuente**, especifique el código fuente relevante para cada tipo de registro y trabajo por lotes.  

Puede cambiar el contenido de un campo más tarde, y ese cambio afectará a futuros registros.

## <a name="change-source-codes" />Cambiar códigos de origen

Puede querer cambiar un código de origen. Por ejemplo, quiere modificar el código de origen *GENJNL* a *GNJ*.

### <a name="to-change-source-codes" />Para modificar códigos de origen

1. Elija el icono ![Buscar página o informe.](media/ui-search/search_small.png "Icono de Buscar por página o informe") , escriba **Códigos de origen** y luego elija el enlace relacionado.

2. En la línea que contiene el código que debe modificarse, seleccione el código en el campo **Código**.

3. Introduzca el nuevo código y, a continuación, elija el botón **Sí**. También puede modificar el contenido del campo **Descripción**.

Todos los nuevos movimientos que se registren posteriormente del diario general tendrán el nuevo código de origen.

## <a name="define-reason-codes" />Definir códigos de auditoría

Los códigos de auditoría complementan los código de origen y se utilizan para indicar por qué se creó una entrada. Puede asignar códigos de auditoría en movimientos individuales y puede asignar códigos permanentes a libros diarios y secciones de diario específicos. Cuando un código de auditoría está vinculado a una línea del diario o a una cabecera de ventas o de compra, se marcan todos los movimientos con el código de auditoria al registrarlos.  

### <a name="to-set-up-reason-codes" />Para configurar códigos de auditoría

1. Elija el icono ![Buscar página o informe.](media/ui-search/search_small.png "Icono de Buscar por página o informe")  , escriba **Códigos de auditoría** y luego elija el enlace relacionado.

2. En la ventana **Códigos auditoría**, introduzca el primer código en el campo **Código**. En el campo **Descripción**, escriba un texto explicativo.

Repita el procedimiento para cada código que desee utilizar. Puede configurar cualquier número de códigos.

El siguiente procedimiento describe cómo agregar un código de auditoría a un libro diario, pero se aplican pasos similares para agregar un código de auditoría a una línea del diario o sección del diario.  

### <a name="to-assign-reason-codes-to-journal-templates" />Para asignar códigos de auditoría a libros diarios

1. Elija el icono ![Buscar página o informe.](media/ui-search/search_small.png "Icono Buscar página o informe")  , escriba **Libros diario general**, y luego elija el enlace relacionado.

2. En la línea que contiene el libro diario seleccionado, en el campo **Código de motivo**, especifique el código relevante.

3. Cierre el libro diario.

El código de auditoría seleccionado se copiará en las nuevas secciones de diario creadas en este libro diario. Para asignar códigos de auditoría a libros diario de otras áreas de aplicación, deberá proceder del mismo modo.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents" />Para usar códigos de auditoría en documentos de compras y ventas

1. Abra el documento de compras correspondiente.

2. En la cabecera de ventas o de compra, escriba el código en el campo **Código de auditoría**.

Al registrar la factura, el código de auditoría se copia en cada movimiento de contabilidad, cliente y proveedor. No puede asignar códigos de auditoría distintos a cada una de las líneas de venta y compra porque todas las líneas se registran como un solo movimiento.

## <a name="see-related-microsoft-trainingtrainingpathsset-up-financial-management-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/paths/set-up-financial-management-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también

[Finanzas](finance.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Analizar el flujo de efectivo de la empresa](finance-analyze-cash-flow.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
