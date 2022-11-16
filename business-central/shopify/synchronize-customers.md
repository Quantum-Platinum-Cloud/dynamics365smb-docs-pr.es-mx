---
title: Sincronizar clientes
description: Importar clientes desde o exportar a Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 1a796d1094401cd2ebc0efd54f752211d22bfb12
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: es-MX
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728665"
---
# <a name="synchronize-customers"></a>Sincronizar clientes

Cuando un pedido se importa desde Shopify, es esencial obtener la información sobre el cliente para el procesamiento posterior del documento en [!INCLUDE[prod_short](../includes/prod_short.md)]. Estas son las dos opciones principales para ello y sus combinaciones:

* Use un cliente especial para todos los pedidos.
* Importe la información real del cliente desde Shopify. Esta opción también está disponible cuando exporta clientes a Shopify primero desde [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="important-settings-when-importing-customers-from-shopify"></a>Configuraciones importantes al importar clientes desde Shopify

Da igual si importa clientes desde Shopify de forma masiva o al mismo tiempo que se importan los pedidos, las siguientes configuraciones le permiten administrar el proceso:

|Campo|Descripción|
|------|-----------|
|**Importación de cliente desde Shopify**|Seleccione **Todos los clientes** si planea importar clientes desde Shopify de forma masiva; ya sea manualmente usando la acción **Sincronizar clientes** o a través de la cola de trabajos para actualizaciones periódicas. Independientemente de la selección, la información del cliente siempre se importará junto con el pedido. Sin embargo, el uso de esta información depende de las **Plantillas de clientes de Shopify** y los ajustes del campo **Tipo de asignación de cliente**.|
|**Tipo de asignación de cliente**|Defina cómo desea que el conector realice la asignación.<br>- **Por correo electrónico/teléfono** si desea que el conector asigne el cliente de Shopify importado a un cliente existente en [!INCLUDE[prod_short](../includes/prod_short.md)] utilizando el correo electrónico y el teléfono.</br>- **Por información de dirección de facturación** si desea que el conector use la dirección del destinatario de la factura para asignar el cliente de Shopify importado a un cliente existente en [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Seleccione **Tomar siempre el cliente predeterminado** si desea que el sistema utilice un cliente del campo **N.º de cliente predeterminado** . |
|**Shopify puede actualizar clientes**| Seleccione este campo si desea que el conector actualice los clientes que encuentra, cuando la opción **Por correo electrónico/teléfono** o **Por información de dirección de facturación** se ha seleccionado en el campo **Tipo de asignación de cliente**.|
|**Crear clientes desconocidos automáticamente**| Seleccione este campo si desea que el conector cree los clientes que falten cuando las opciones **Por correo electrónico/teléfono** o **Por información de dirección de facturación** se hayan seleccionado en el campo **Tipo de asignación de cliente**. Se creará un nuevo cliente usando datos importados y el **Código de plantilla de cliente** definido en las páginas **Ficha de tienda de Shopify** o **Plantilla de cliente de Shopify**. Tenga en cuenta que el cliente de Shopify debe tener al menos una dirección. Si esta opción no está habilitada, deberá crear un cliente manualmente y vincularlo al cliente de Shopify. Siempre puede iniciar la creación de un cliente manualmente desde la página **Pedido de Shopify**.|
|**Código de plantilla de cliente**|Este campo se usa con **Creación automática de clientes desconocidos**.<br>- Elija la plantilla predeterminada que se utilizará para los clientes creados automáticamente. Asegúrese de que la plantilla seleccionada contenga los campos obligatorios, como los campos **Grupo de registro de negocio general**, **Grupo de registro de clientes**, y el IVA o los campos relacionados con impuestos.<br>- Puede definir plantillas por país o región en la página **Plantillas de clientes de Shopify**, que es útil para el cálculo de impuestos adecuado. <br>- Obtenga más información en [Configurar impuestos](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Plantilla de cliente por país

Algunas configuraciones se pueden definir en el nivel de país o región, o en el nivel de estado o provincia. Los ajustes se pueden configurar en [Envío y entrega](https://www.shopify.com/admin/settings/shipping) en Shopify.

Puede hacer lo siguiente para cada cliente mediante la **Plantilla de cliente de Shopify**:

1. Especificar el **N.º de cliente genérico**, que tiene prioridad sobre la selección en los campos **Importación de clientes desde Shopify** y **Tipo de asignación de cliente**. Se utiliza en el pedido de venta importado.
2. Defina el **Código de plantilla de cliente**, que se utiliza para crear clientes que falten si se ha habilitado **Crear clientes desconocidos automáticamente**. Si el **Código de plantilla de cliente** está vacío, entonces la función usa el **Código de plantilla de cliente** definido en la **Ficha de tienda de Shopify**.
3. Defina si los precios incluyen IVA o impuestos para pedidos importados.
4. En algunos casos, el **Código de plantilla de cliente** definido para un país no es suficiente para garantizar el cálculo correcto de los impuestos (por ejemplo, para países con impuesto sobre las ventas). En este caso, incluir **Áreas fiscales** podría ser una adición útil.

> [!NOTE]  
> Los códigos de país son códigos de país ISO 3166-1 alfa-2. Obtenga más información en [Código de país](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Exportar clientes a Shopify

Puede explotar los clientes existentes a Shopify de forma masiva. En cada caso, se crean un cliente y una dirección predeterminadas. Puede gestionar el proceso con las siguientes configuraciones:

|Campo|Descripción|
|------|-----------|
|**Exportar clientes a Shopify**|Seleccione esto si tiene previsto exportar todos los clientes de [!INCLUDE[prod_short](../includes/prod_short.md)] a Shopify en masa. Puede hacerlo manualmente, usando la acción **Sincronizar clientes**, o automáticamente, usando una cola de trabajos para actualizaciones recurrentes.<br> Al exportar clientes con direcciones que incluyen provincias/estados, asegúrese de que **Código ISO** se rellena para países/regiones.|
|**Puede actualizar clientes de Shopify**|Se usa junto con el ajuste **Exportar cliente a Shopify**. Habilite la opción si desea generar actualizaciones más tarde desde [!INCLUDE[prod_short](../includes/prod_short.md)] para los clientes que ya existen en Shopify.|

Los siguientes son requisitos para exportar un cliente:

* El cliente debe tener una dirección de correo electrónico válida.
* Se selecciona un país/región en la tarjeta de cliente, para clientes locales, con país/región en blanco el país/región especificado en la página **Información de la empresa** debe tener un código ISO definido.
* Si el cliente tiene un número de teléfono, el número debe ser único porque Shopify no aceptará un segundo cliente con el mismo número de teléfono.
* Si el cliente tiene un número de teléfono, debe estar en el formato E.164. Se admiten diferentes formatos si representan un número que se puede marcar desde cualquier parte del mundo. Los siguientes formatos son válidos:
  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Una vez que haya creado los clientes en Shopify, puedes enviarles invitaciones directas animándolos a activar sus cuentas.

### <a name="populate-customer-information-in-shopify"></a>Rellenar la información del cliente en Shopify

Un cliente en Shopify tiene nombre, apellido, correo electrónico y número de teléfono. Puede introducir el nombre y los apellidos a partir de los datos de la ficha del cliente en [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioridad|Campo en la ficha de cliente|Descripción|
|------|------|-----------|
|1|**Nombre contacto**|Máxima prioridad, si el campo **Nombre de contacto** está lleno y el campo **Origen de contacto** en la **Ficha de tienda de Shopify** contiene la opción *Nombre y apellido* o *Apellido y nombre* para definir cómo dividir los valores.|
|2|**Nombre 2**|Si el campo **Nombre 2** está lleno y el campo **Origen de nombre 2** en la **Ficha de tienda de Shopify** contiene la opción *Nombre y apellido* o *Apellido y nombre* para definir cómo dividir los valores.|
|3|**Nombre**|Prioridad más baja, si el campo **Nombre** está lleno y el campo **Origen de nombre** en la **Ficha de tienda de Shopify** contiene la opción *Nombre y apellido* o *Apellido y nombre* para definir cómo dividir los valores.|

Un cliente en Shopify también tiene una dirección predeterminada, que puede contener una empresa y dirección además de su nombre, apellido, correo electrónico o teléfono. Puede rellenar el campo **Empresa** en función de los datos de la ficha de cliente en [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioridad|Campo en la ficha de cliente|Descripción|
|------|------|-----------|
|1|**Nombre**|Máxima prioridad, si el campo **Origen de nombre** en la **Ficha de tienda de Shopify** contiene *Nombre de empresa*.|
|2|**Nombre 2**|Prioridad más baja, si el campo **Origen de nombre 2** en la **Ficha de tienda de Shopify** contiene *Nombre de empresa*.|

Para las direcciones en las que se utiliza el país o la provincia, seleccione *Código* o *Nombre* en el campo **Origen de país** en la **Ficha de tienda de Shopify**. Esto especifica el tipo de datos almacenados en [!INCLUDE[prod_short](../includes/prod_short.md)] en el campo **País**.

## <a name="sync-customers"></a>Sincronizar clientes

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda específica para la que desea sincronizar los clientes.
3. Seleccione la acción **Sincronizar clientes**.

Como alternativa, use la acción **Iniciar sincronización de cliente** en la ventana **Clientes de Shopify** o buscar el trabajo por lotes **Sincronizar clientes**.

Puede programar la tarea para que se realicen de forma automatizada. Obtenga más información en [Programar tareas recurrentes](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Consulte también .

[Introducción al conector para Shopify](get-started.md)  