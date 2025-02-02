---
title: Crear y administrar productos en catálogo
description: Aprenda a vender productos que no mantiene en su lista de productos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/08/2023
ms.custom: bap-template
ms.search.keywords: non-inventoriable
ms.search.forms: '5725, 5726, 5732'
---

# <a name="work-with-catalog-items" />Trabajar con productos del catálogo

Los elementos del catálogo son artículos que no administra en [!INCLUDE[prod_short](includes/prod_short.md)] hasta que los vende. Cuando usa la acción **Seleccionar producto del catálogo** para agregar un producto de catálogo a una línea en una orden, una cotización o una orden de venta abierta, el producto de catálogo se convierte en un producto normal.

> [!NOTE]  
> No puede seleccionar un producto del catálogo de la página **Factura de venta**.

Un producto del catálogo normalmente tiene el número del proveedor que lo suministra. Antes de que pueda convertir un artículo del catálogo en un artículo normal, debe especificar cómo convertir los números de artículos del proveedor a su numeración de artículos. Para obtener más información sobre la numeración de productos, consulte [Especificar cómo los números de producto del catálogo se convierten a su propia numeración](#specify-how-catalog-item-numbers-are-converted-to-your-own-numbering).  

> [!IMPORTANT]
> Los artículos del catálogo no deben confundirse con los artículos que no están en el inventario, que son artículos regulares a los que se les asigna el tipo **No inventario** para mantenerlos fuera de disponibilidad y de los cálculos de costos, por ejemplo, porque solo se usan internamente y tienen un bajo costo. Para obtener información sobre productos que no están en el inventario, vaya a [Acerca de los tipos de productos](inventory-about-item-types.md).

## <a name="create-a-catalog-item" />Crear un producto del catálogo

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos del catálogo** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="specify-how-catalog-item-numbers-are-converted-to-your-own-numbering" />Especificar cómo los números de productos del catálogo se convierten a su propia numeración

Antes de que pueda convertir un producto del catálogo en un producto normal, debe especificar cómo convertir los números de productos del proveedor a la estructura que usted utiliza para la numeración de productos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de productos de catálogo** y luego elija el enlace relacionado.
2. En el campo **N.º formato**, elija la opción que prefiera.

## <a name="convert-a-catalog-item-to-a-normal-item" />Convertir un producto del catálogo en un producto normal

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos del catálogo** y luego elija el enlace relacionado.
2. Abra la ficha de un producto del catálogo que desee convertir a uno normal.
3. En la página **Ficha de producto del catálogo**, seleccione la acción **Crear producto**.

Se crean una nueva tarjeta de producto rellenada previamente con la información del producto del catálogo y una plantilla de producto. Puede editar la información sobre el nuevo producto, si es necesario. Para obtener más información sobre la creación de productos, vaya a [Registrar nuevos productos](inventory-how-register-new-items.md).

## <a name="to-sell-a-catalog-item-and-convert-it-to-a-normal-item" />Para vender un producto del catálogo y convertirlo en un producto normal

En el siguiente proceso, se utiliza una orden de venta, pero los pasos son los mismos para las órdenes de venta abiertas y las cotizaciones.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**. Rellene los campos de la ficha desplegable **General** para cada pedido. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).
3. En una nueva línea de venta, en el campo **Tipo**, seleccione **Producto**, pero deje **N.º** campo vacío.
4. Elija la acción **Línea** y, a continuación, elija la acción **Seleccionar artículos del catálogo**.
5. En la página **Productos del catálogo**, seleccione el producto del catálogo que desee vender y, a continuación, haga clic en **Aceptar**.
6. Cuando la orden de venta esté completa, seleccione la acción **Registrar**.

> [!NOTE]  
> Una referencia de producto se crea automáticamente entre el número del producto del proveedor y su nuevo número de producto. Para obtener más información sobre las referencias de productos, vaya a [Usar referencias de productos](inventory-how-use-item-cross-refs.md).

## <a name="see-related-microsoft-trainingtrainingmodulescreate-sales-documents-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Crear pedidos especiales](sales-how-to-create-special-orders.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
