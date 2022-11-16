---
title: Sincronizar artículos e inventario
description: Configurar y ejecutar sincronizaciones de artículos entre Shopify y Business Central
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30116, 30117, 30126, 30127,
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 90144dfb2f84853f43ae85bf5a162f46cdb65286
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728395"
---
# <a name="synchronize-items-and-inventory"></a>Sincronizar artículos e inventario

Los **Artículos** en [!INCLUDE[prod_short](../includes/prod_short.md)] son equivalentes a los *productos* en Shopify, e incluyen bienes físicos, descargas digitales, servicios y tarjetas de regalo que puede vender. Hay dos razones principales para sincronizar los artículos:

1. La gestión de datos se realiza principalmente en [!INCLUDE[prod_short](../includes/prod_short.md)]. Necesita exportar todos o algunos datos desde allí a Shopify y hacerlo visible. Puede exportar el nombre del artículo, la descripción, la imagen, los precios, la disponibilidad, las variantes, los detalles del proveedor y el código de barras. Una vez exportados, puede revisar los elementos o hacerlos visibles inmediatamente.
2. Cuando un pedido de Shopify se importa, la información sobre los artículos es vital para el procesamiento posterior del documento en [!INCLUDE[prod_short](../includes/prod_short.md)].

Los dos escenarios anteriores siempre están habilitados.

Un tercer escenario es administrar datos en Shopify pero importar esos productos a granel para [!INCLUDE[prod_short](../includes/prod_short.md)]. Este escenario puede ser útil para eventos de migración de datos, como cuando quiere conectar una tienda en línea existente con un entorno [!INCLUDE[prod_short](../includes/prod_short.md)] nuevo.

## <a name="define-item-synchronizations"></a>Definir las sincronizaciones de artículos

1. Elija el icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. y entre en la **Tienda Shopify**. Abra la tienda para la que quiera configurar la sincronización de artículos.
2. En el campo **Sincronizar artículo**, seleccione la opción requerida.

   La siguiente tabla esboza las opciones.

|Opción|Descripción|
|------|-----------|
|**En blanco**| Los productos se importan junto con la importación de pedidos. Los productos se exportan a Shopify si un usuario ejecuta la acción **Agregar artículo** desde la página **Productos de Shopify**. Este es el proceso predeterminado.|
|**A Shopify**| Seleccione esta opción si, después de la sincronización inicial desencadenada por la acción **Agregar artículo**, planea actualizar los productos manualmente usando la acción **Sincronizar producto** o usando la cola de trabajos para actualizaciones periódicas. Recuerde habilitar el campo **Puede actualizar producto de Shopify**. Si no está habilitado, es igual a la opción **Vacío** (proceso predeterminado). Obtenga más información en la sección [Exportar artículos a Shopify](synchronize-items.md#export-items-to-shopify).|
|**Desde Shopify**| Elija esta opción si planea importar productos de Shopify de forma masiva, ya sea manualmente usando la acción **Sincronizar producto** o a través de la cola de trabajos para actualizaciones periódicas. Obtenga más información en la sección [Importar artículos de Shopify](synchronize-items.md#import-items-from-shopify).|

## <a name="import-items-from-shopify"></a>Importar artículos desde Shopify

Primero, importe artículos de Shopify de forma masiva o junto con pedidos para agregarlos a las tablas **Producto de Shopify** y **Variante de Shopify**. A continuación, asigne productos y variantes importados a artículos y variantes en [!INCLUDEprod_short]. Administre el proceso con las siguientes configuraciones:

|Campo|Descripción|
|------|-----------|
|**Crear artículos desconocidos automáticamente**|Cuando se importan productos y variantes de Shopify a [!INCLUDE[prod_short](../includes/prod_short.md)], la función [!INCLUDE[prod_short](../includes/prod_short.md)] siempre intenta encontrar primero el registro coincidente en la lista de artículos. **Asignación de SKU** afecta cómo se realiza la conciliación y crea un nuevo artículo o variante del artículo. Habilite esta opción si desea crear un nuevo producto o cuando no existe un registro correspondiente. El nuevo elemento se crea utilizando datos importados y el **Código de plantilla de artículos**. Si esta opción no está habilitada, deberá crear un artículo manualmente y usar la acción **Asignar producto** en la página **Productos de Shopify**.|
|**Código de plantilla de artículos**|Se usa con la opción de alternancia **Creación automática de artículos desconocidos**.<br>Elija la plantilla que desea usar para los elementos creados automáticamente.|
|**Asignación de SKU**|Elige cómo quiere usar el valor de **SKU** importado de Shopify durante el mapeo y la creación de artículos/variantes. Obtenga más información en la sección [Efecto de los SKU y códigos de barras definidos del producto de Shopify en el mapeo y la creación de artículos y variantes en Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**Separador de campo de SKU**|Use esto junto con **Asignación de SKU** ajustado a la opción **[N.º de artículo + Código de variante](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Defina un separador para usarlo para dividir la SKU.<br>Así, si en Shopify crea la variante con la SKU '1000/001', escribirá '/' en el campo **Separador de campo SKU** para crear el número de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] como '1000' y el código de variante del artículo como '001'.|
|**Prefijo de variante**|Se usa junto con **Asignación de SKU** ajustado a **Código de variante** o **N.º de articulo + Código de variante** como función alternativa cuando el SKU proveniente de Shopify esta vacío.<br>Si desea crear la variante de artículo en [!INCLUDE[prod_short](../includes/prod_short.md)] automáticamente, tendrá que introducir un valor en **Código**. Por defecto, se usa el valor definido en el campo SKU importado de Shopify. Sin embargo, si el SKU está vacío, generará un código que comenzará con el prefijo de variante definido y "001".|
|**Shopify puede actualizar artículo**|Elija esta opción si desea actualizar artículos y/o variantes automáticamente.|

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Efecto los SKU y códigos de barras del producto de Shopify en el mapeo y la creación de artículos y variantes en Business Central

Cuando los productos son importados desde Shopify a las tablas **Productos de Shopify** y **variantes de Shopify**, [!INCLUDE[prod_short](../includes/prod_short.md)] intenta encontrar registros existentes.

La siguiente tabla describe las diferencias entre las opciones del campo **Asignación de SKU**.

|Opción|Efecto en el mapeo|Efecto en la creación|
|------|-----------------|------------------|
|**En blanco**|El campo SKU no se usa en la rutina de mapeo de artículos.|Sin efecto en la creación del elemento.<br>Esta opción impide la creación de variantes. Cuando en el pedido de ventas, solo se usa el artículo principal. Una variante se sigue pudiendo mapear manualmente en la página **Productos de Shopify**.|
|**Nº producto**|Elíjalo si el campo SKU contiene el número de artículo.|Sin efecto en la creación de un elemento sin variantes. Para un artículo con variantes, cada variante se crea como un artículo separado.<br>Por lo tanto, si Shopify tiene un producto con dos variantes y sus SKU son '1000' y '2000', en [!INCLUDE[prod_short](../includes/prod_short.md)] el sistema creará dos artículos numerados '1000' y '2000'.|
|**Cód. variante**|El campo SKU no se usa en la rutina de mapeo de artículos.|Sin efecto en la creación del elemento. Cuando se crea una variante de artículo, el valor del campo SKU se usa como código. Si el SKU está vacío, se genera un código usando el campo **Prefijo de variante**.|
|**N.º artículo + Código de variante**|Seleccione esto si el campo SKU contiene un número de artículo. y el código de variante del artículo se separa por el valor definido en el campo **Separador de campos SKU**.|Cuando se crea un artículo, la primera parte del valor del campo SKU se designa como **N.º**. Si el campo SKU está vacío, un número de artículo se genera utilizando las series numéricas definidas en el campo **Código de plantilla de artículo** o **Números de artículo** de la página **Configuración de inventario**.<br>Cuando se crea un artículo, la función variante usa la segunda del valor del campo SKU se usa como **Código**. Si el campo de SKU está vacío, se genera un código usando el campo **Prefijo de variante**.|
|**N.º de artículo de proveedor**|Elíjalo si el campo SKU contiene el número de artículo de proveedor. En este caso, el **Número de proveedor de artículo** no se usa en la página **Tarjeta de artículo**; más bien se usa el **Número de artículo del proveedor** del **Catálogo de proveedores de artículos**. Si el registro encontrado de *Catálogo de proveedores de artículos* contiene un código de variante, este código se utiliza para mapear la variante de Shopify.|Si existe un proveedor correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)], el valor de SKU se usará como **Número de artículo del proveedor** en la página **Tarjeta de artículo** y como **Referencia del artículo** de tipo proveedor. <br>Impide la creación de variantes. Es útil cuando desea usar el artículo principal solo en el pedido de ventas. Todavía puodrá asignar una variante manualmente desde la página **Productos de Shopify**.|
|**Código de barras**|Elíjalo si el campo SKU contiene un código de barras. Se realiza una búsqueda entre **Referencias de artículos** del tipo de proveedor. Si el registro encontrado de Referencia de artículo contiene un código de variante, este código de variante se utiliza para mapear la variante de Shopify.|Sin efecto en la creación del elemento. <br>Impide la creación de variantes. Es útil cuando desea usar el artículo principal solo en el pedido de ventas. Todavía puodrá asignar una variante manualmente desde la página **Productos de Shopify**.|

En la tabla siguiente se describe los efectos del campo **Código de barras**.

|Efecto en el mapeo|Efecto en la creación|
|-----------------|------------------|
|Se realiza una búsqueda en las **Referencias de artículos** que contienen un tipo de código de barras para el valor definido en el campo **Código de barras** en Shopify. Si el registro encontrado de Referencia de artículo contiene un código de variante, este código de variante se utiliza para mapear la variante de Shopify.|El código de barras se guarda como **Referencia del artículo** para el artículo y variante de artículo.|

> [!NOTE]  
> Puede desencadenar el mapeo del producto/variantes seleccionados o todos los productos importados no mapeados seleccionando **Intentar buscar mapeo de producto** o **Intentar buscar asignaciones**.

## <a name="export-items-to-shopify"></a>Exportar elementos a Shopify

Elija los elementos de su lista de elementos que se exportarán a Shopify. Utilice la acción **Agregar artículo** en la página **Productos de Shopify** para agregar elementos a la lista de productos de Shopify.

Las siguientes configuraciones le permiten administrar el proceso de exportar artículos:

|Campo|Descripción|
|------|-----------|
|**Grupo de precios de cliente**|Determine el precio de un artículo en Shopify. Se toma el precio de venta de este grupo de precios de cliente. Si no se ingresa ningún grupo, se utiliza el precio en la ficha del artículo.|
|**Grupo de descuentos de cliente**|Determinar el descuento que se utilizará para calcular el precio de un artículo en Shopify. Los precios con descuento se almacenan en el campo **Precio** y el precio completo se almacena en el campo **Comparar en el precio**.|
|**Sincronizar texto adicional de artículo**|Seleccione esto para sincronizar el texto extendido del elemento. Como se agregará al campo *Descripción*, puede contener código HTML. |
|**Sincronizar atributos de artículo**|Seleccione esto para sincronizar los atributos del artículo. Los atributos tienen el formato de una tabla y se incluyen en el campo *Descripción* en Shopify.|
|**Código de idioma**|Seleccione esto si desea que las versiones traducidas se utilicen para el título, los atributos y el texto ampliado.|
|**Asignación de SKU**|Elija cómo desea completar el campo SKU en Shopify. Las opciones admitidas son:<br> - **N.º de artículo** para usar el n.º de artículo tanto para productos como para variantes.<br> - **N.º de artículo + Código de variante** para crear un SKU concatenando valores de dos campos. Para artículos sin variantes, solo se usa el número de artículo.<br>- **N.º de proveedor de artículo** para utilizar el número de proveedor del artículo definido en *Tarjeta de artículo* tanto para productos como para variantes.<br> - **Código de barras** para usar el tipo código de barras de **Referencia del artículo**. Esta opción respeta las variantes.|
|**Separador de campo de SKU**|Defina un separador para la opción **N.º de articulo + Código de variante**.|
|**Inventario seguido**| Elija cómo el sistema debe llenar el campo **Seguimiento de inventario** para productos exportados a Shopify. Puede actualizar la información de disponibilidad desde [!INCLUDE[prod_short](../includes/prod_short.md)] para productos en Shopify cuyo inventario de seguimiento está habilitado. Obtenga más información en la sección [Inventario](synchronize-items.md#sync-inventory-to-shopify).|
|**Directiva de inventario predeterminada**|Escoja *Denegar* para evitar existencias negativas en el lado de Shopify.|
|**Puede actualizar productos de Shopify**|Defina esto si [!INCLUDE[prod_short](../includes/prod_short.md)] solo puede crear elementos o también puede actualizar elementos. Seleccione esta opción si, después de la sincronización inicial desencadenada por la acción **Agregar artículo**, planea actualizar los productos manualmente usando la acción **Sincronizar producto** o usando la cola de trabajos para actualizaciones periódicas. Recuerde seleccionar **A Shopify** en el campo **Sincronización de elementos**.|
|**Código de plantilla de cliente**|Elija la plantilla predeterminada que se utilizará durante el cálculo del precio. Obtenga más información en [Configurar impuestos](setup-taxes.md).|

### <a name="fields-mapping-overview"></a>Información general de asignaciones de campos

|Shopify|Origen cuando se exporta desde [!INCLUDE[prod_short](../includes/prod_short.md)]|Destino cuando se importa a [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|De acuerdo con el campo **Estado de los productos creados** en la **Tarjeta de tienda de Shopify**. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Cargo | **Descripción**. Si el código de idioma está definido y existe una traducción del artículo correspondiente, se utilizará la traducción del artículo en lugar de la descripción.|**Descripción**|
|Descripción|Combina textos extendidos y atributos si las alternancias correspondientes en la tarjeta de Shopify están habilitadas. Respeta el código de idioma.|No utilizado.|
|Título de página SEO|Valor fijo: vacío. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Descripción meta de SEO|Valor fijo: vacío. Obtenga más información en la sección [Actualizaciones ad hoc de productos de Shopify](synchronize-items.md#ad-hoc-updates-of-shopify-products).|No utilizado.|
|Medios|**Imagen**. Obtenga más información en la sección [Sincronizar imágenes de elementos](synchronize-items.md#sync-item-images)|**Imagen**|
|Precio|El cálculo del precio del cliente final incluye el grupo de precios del artículo, el grupo de descuento del artículo, el código de moneda y el código de plantilla de cliente.|**Precio unitario**|
|Comparar por precio|El cálculo del precio sin descuento incluye el grupo de precios del artículo, el grupo de descuento del artículo, el código de moneda y el código de plantilla de cliente.|No utilizado.|
|Costo por producto|**Costo unitario**|**Costo unitario**|
|UA|Infórmese sobre esto en **Asignación de SKU** en la sección [Exportar elementos a Shopify](synchronize-items.md#export-items-to-shopify).|Obtenga más información sobre esto en la sección [Efecto de los SKU y códigos de barras definidos del producto de Shopify en el mapeo y la creación de artículos y variantes en Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Código de barras|**Referencias de artículos** de tipo código de barras.|**Referencias de artículos** de tipo código de barras.|
|Seguimiento de cantidad|De acuerdo con el campo **Inventario seguido** en la página **Tarjeta de tienda de Shopify**. Obtenga más información en la sección [Inventario](synchronize-items.md#sync-inventory-to-shopify).|No utilizado.|
|Continuar vendiendo cuando no haya existencias|De acuerdo con la **Directiva de inventario predeterminada** en la **Tarjeta de tienda de Shopify**. No importado.|No utilizado.|
|Tipo|**Descripción** de **Código de categoría de artículos**. Si el tipo no está especificado en Shopify, se agrega como un tipo personalizado.|**Código de categoría de artículos**. Mapeo por descripción.|
|Proveedor|**Nombre** del proveedor según el **N.º de proveedor**|Asignación de **N.º de proveedor** por nombre.|
|Peso|**Peso bruto**.|No utilizado.|
|Gravable|Valor fijo: habilitado.|No utilizado.|
|Códigos impositivos|**Código de grupo de impuestos**. Solo relevante para los impuestos. Obtenga más información en [Configurar impuestos](setup-taxes.md).|No utilizado.|

### <a name="tags"></a>Etiquetas

Revise las etiquetas importadas en el cuadro informativo **Etiquetas** en la página **Producto de Shopify**. En la misma página, para editar etiquetas, seleccione la acción **Etiquetas**.
Si la opción **A Shopify** está seleccionada en el campo **Artículo de sincronización**, las etiquetas asignadas se exportan a Shopify en la próxima sincronización.

## <a name="run-item-synchronization"></a>Ejecutar sincronización de artículos

La sincronización total o parcial de elementos se puede realizar de muchas maneras diferentes.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Sincronización inicial de elementos de Business Central a Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Agregar artículos**.
3. En el campo **Código de tienda**, escriba el código. Si abre la ventana **Producto de Shopify** de la página **Tarjeta de tienda**, el código de tienda se completará automáticamente.
4. Defina filtros en artículos según sea necesario. Por ejemplo, puede filtrar por el n.º de artículo. o código de categoría de artículo.
5. Elija **Aceptar**.

Los elementos resultantes se crean automáticamente en Shopify con precios, pero las imágenes y los niveles de inventario no están incluidos. La operación puede tardar algún tiempo si se agrega una gran cantidad de elementos.

### <a name="sync-products-from-shopify-to-business-central"></a>Sincronizar productos de Shopify a Business Central

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar artículos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar productos**.

Como alternativa, utilice la acción **Sincronizar productos** en la página **Productos de Shopify** o busque el trabajo por lotes **Sincronizar productos**.

Puede programar la tarea para que se realicen de forma automatizada. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

### <a name="ad-hoc-updates-of-shopify-products"></a>Actualizaciones ad hoc de productos de Shopify

Cuando se actualizan los registros en la tabla **Productos de Shopify**, los siguientes cambios se sincronizan con Shopify.

Actualizar:

* **Estado**: puede elegir entre activo, archivado o borrador.
* **Título de SEO**
* **Descripción de SEO**

Eliminación:

Según el valor de **Acción para productos eliminados** en la página **Tarjeta de tienda de Shopify**, el producto se actualiza en Shopify cuando se elimina el registro de la página **Productos de Shopify**.

* **En blanco**: no sucederá nada. Si es necesario, deberá realizar la acción requerida desde el **administrador de Shopify**.
* **Estado a Borrador**: el estado del producto en Shopify se establece en *Borrador*.
* **Estado a archivado**: el producto se archiva en Shopify.

## <a name="sync-item-images"></a>Sincronizar imágenes de artículo

La sincronización de imágenes se puede configurar para elementos sincronizados. Elija entre las siguientes opciones:

* **Deshabilitado**: la sincronización de imágenes se desactiva.
* **A Shopify**: las imágenes de los artículos se exportan a Shopify
* **Desde Shopify**: las imágenes de Shopify se importan a [!INCLUDE[prod_short](../includes/prod_short.md)]

La sincronización de imágenes se puede inicializar de las dos maneras que se describen a continuación.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Sincronzar imágenes de productos desde la página de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar imágenes para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar imágenes de productos**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Sincronzar imágenes de productos desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Sincronizar imágenes de productos**.

### <a name="image-synchronization-remarks"></a>Observaciones de sincronización de imágenes

* Al exportar imágenes de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify, las nuevas imágenes se añaden a Shopify, manteniendo intactas las imágenes antiguas. Si una imagen se actualiza en [!INCLUDE[prod_short](../includes/prod_short.md)], deberá eliminar las imágenes antiguas en el **administrador de Shopify**.
* Las imágenes que se exportan a Shopify que no cumplen con los requisitos definidos por Shopify no se importarán. Obtenga más información sobre [Tipos de medios de productos en help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify"></a>Sincronizar precios con Shopify

Los precios para artículos sincronizados se pueden exportar de las formas que se describen a continuación.

### <a name="sync-prices-from-the-shopify-products-page"></a>Sincronzar precios desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Seleccione la acción **Sincronizar precios con Shopify**.

### <a name="price-calculation-remarks"></a>Observaciones de cálculo de precios

* Para el cálculo del precio, es importante tener un valor en el campo **Plantilla de cliente predeterminada**. Obtenga más información en [Configurar impuestos](setup-taxes.md).
* Introduzca un **código de moneda** solo si su tienda en línea utiliza una moneda diferente a la moneda local ($). La divisa especificada debe tener tipos de cambio configurados. Si su tienda en línea usa la misma divisa que [!INCLUDE[prod_short](../includes/prod_short.md)], deje el campo vacío.
* Al determinar un precio, [!INCLUDE[prod_short](../includes/prod_short.md)] utiliza la lógica del "precio más bajo". Eso significa que, si el precio unitario definido en la ficha del artículo es inferior al definido en el grupo de precios, se utiliza el precio unitario de la ficha del artículo.

## <a name="sync-inventory-to-shopify"></a>Sincronizar inventario a Shopify

La sincronización de inventario se puede configurar para elementos ya sincronizados. Hay dos condiciones que se deben cumplir:

1. El seguimiento de inventario debe estar habilitado para un producto en Shopify. Si los artículos se exportan a Shopify, considere habilitar la alternancia **Inventario seguido** en la página **Tarjeta Shopify**. Obtenga más información en la sección [Exportar artículos a Shopify](synchronize-items.md#export-items-to-shopify).
2. La sincronización de inventario debe estar habilitada para **Ubicaciones de Shopify**.

### <a name="to-enable-inventory-sync"></a>Para habilitar la sincronización de inventario

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea sincronizar el inventario para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Ubicaciones** para abrir **Ubicaciones de tienda de Shopify**.
4. Elija la acción **Obtener almacenes de Shopify** para importar todos los almacenes definidos en Shopify. Puede encontrarlas en la configuración de [**Ubicaciones**](https://www.shopify.com/admin/settings/locations) del **Administrador de Shopify**.
5. En el campo **Filtro de ubicación**, agregue ubicaciones si desea incluir inventario solo de ubicaciones específicas. Por lo tanto, podría introducir *ESTE|OESTE* para que el inventario solo de estas dos ubicaciones esté disponible para la venta a través de la tienda en línea.
6. Deseleccione la alternancia **Desactivado** para habilitar la sincronización de inventario para ubicaciones de Shopify seleccionadas.

La sincronización de inventarios se puede inicializar de las dos maneras que se describen a continuación.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Sincronzar inventario desde la página de la tienda de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar el inventario para abrir la página **Tarjeta de tienda de Shopify**.
3. Elija la acción **Sincronizar inventario**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Sincronizar inventario desde la página de productos de Shopify

1. Vaya al icono ![Bombilla que abre la función Dígame](../media/ui-search/search_small.png "Dígame qué desea hacer") de búsqueda. , escriba **Productos de Shopify** y luego elija el enlace relacionado.
2. Elija la acción **Sincronizar inventario**.

### <a name="inventory-remarks"></a>Consideraciones sobre inventarios

* El conector calcula el **Saldo disponible proyectado** y lo exporta a Shopify.
* Puede consultar la información de existencias recibida de Shopify en la página **Cuadro informativo de inventario de Shopify**. En este cuadro informativo, obtendrá una descripción general de las existencias de Shopify y el último inventario calculado en [!INCLUDE[prod_short](../includes/prod_short.md)]. Hay un registro por ubicación.
* Si la información de existencias en Shopify es diferente de **Saldo disponible proyectado** en [!INCLUDE[prod_short](../includes/prod_short.md)], entonces las existencias se actualizarán en Shopify.

## <a name="see-also"></a>Consulte también .

[Introducción al conector para Shopify](get-started.md)  