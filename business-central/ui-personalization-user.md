---
title: Personalizar páginas (contiene vídeo)
description: Aprenda a personalizar la interfaz de usuario y personalizar el área de trabajo para que se adapte a su forma de trabajar y preferencias personales en Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 10/11/2022
ms.author: bholtorf
---
# <a name="personalize-your-workspace" />Personalice su área de trabajo

Puede personalizar el área de trabajo para que se adapte a sus preferencias y trabajo. Cambie las páginas para que muestren solo la información que necesita, donde la necesita. La personalización afecta solo a su espacio de trabajo. No cambia la forma en que otros trabajan.

Puede personalizar todo tipo de páginas, incluida la página Área de tareas. Para obtener más información sobre las áreas de tareas, vaya a [Área de tareas](ui-change-basic-settings.md#role-center).  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Puede realizar varios cambios, como mover u ocultar campos, columnas, acciones y partes completas, y agregar nuevos campos. La mayor parte de la personalización debe realizarse activando primero banner **Personalización**. Puede realizar ajustes simples, como el ancho de columna, inmediatamente en cualquier lista.

> [!NOTE]
> Los administradores pueden hacer los mismos cambios de diseño que los usuarios al personalizar el espacio de trabajo para un perfil que se asigna a múltiples usuarios. Para obtener más información sobre las páginas para roles, vaya a [Personalizar páginas para roles](ui-personalization-manage.md)<br /><br />
Los administradores también pueden anular o deshabilitar la personalización de los usuarios y pueden definir qué características están incluso disponibles para que los usuarios las vean en todas las empresas o en empresas específicas. Para obtener más información, consulte [Personalizar Business Central](ui-customizing-overview.md).

## <a name="video" />Vídeo

El siguiente video muestra algunas de las formas en que puede personalizar su área de tareas.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="to-change-the-width-of-a-column" />Para cambiar el ancho de una columna

Puede cambiar fácilmente el tamaño de las columnas en cualquier lista. Solo tiene que arrastrar el límite entre dos columnas a la izquierda o derecha.  

1. En la cabecera de una lista, seleccione y arrastre el límite entre dos columnas.
2. También puede hacer doble clic en el límite entre dos columnas para ajustar automáticamente el ancho de la columna. El ancho se ajusta al tamaño óptimo para facilitar la lectura.

En cuanto a otra personalización, los cambios que efectúe en el ancho de columna se almacenan en su cuenta y le siguen sin importar en qué dispositivo inicie sesión.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner" />Para empezar a personalizar una página a través del banner **Personalización**

1. Abra cualquier página que quiera personalizar.
2. En la esquina superior derecha, seleccione el icono ![Configuración](media/ui-experience/settings_icon_small.png "Icono de configuración para el Área de tareas") , y luego elija la acción **Personalizar**.

    El banner **Personalización** aparece en la parte superior para indicar que puede empezar a realizar cambios.

    > [!NOTE]
    > Para navegar durante la personalización, use Ctrl + clic en una acción si está resaltada por la punta de flecha.

    Si se muestra ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalizacion") o ![Personalización bloqueada](media/personalization-blocked-icon.png "Personalización bloqueada") en el banner, no puede personalizar la página. Para obtener más información, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).

3. Para agregar un campo, elija la acción **+ Campo**.
4. Desde el panel **Agregar campo a página**, arrastre y suelte un campo en la posición deseada en la página.
5. Para cambiar un elemento de la interfaz de usuario, señale el elemento, como una acción, un campo o una parte. El elemento se resalta inmediatamente con una punta de flecha o borde.
6. Elija el elemento y, a continuación, seleccione **Mover**, **Eliminar**, **Ocultar**, **Mostrar**, **Mostrar en "Mostrar más"**, **Mostrar cuando se contrae**, **Mostrar siempre**, **Establecer/Borrar inmovilización de panel** o **Incluir/Excluir de entrada rápida**, según el tipo y el estado del elemento de la interfaz de usuario. Para obtener más información, consulte [Qué puede personalizar](#What).
7. Cuando haya terminado de cambiar el diseño de una o más páginas, elija el botón **Listo** en el banner **Personalización**.

## <a name="a-namewhatawhat-you-can-personalize" /><a name="What"></a>Qué puede personalizar

|Qué desea hacer|Cómo hacerlo|Comentarios|
|----|------------|-------|
|Mover algo, un campo, una columna de la lista, un icono, una acción o una pieza|Señale en cualquier lugar qué desea mover y arrástrelo a su nueva posición. La posición se indica con una fina línea vertical u horizontal.<br /><br />![Icono No se puede mover aquí](media/personalization-cannot-move-here.png "Modo de personalización: icono No se puede mover aquí") indica que no puede mover el elemento a la posición seleccionada.|Las piezas son subdivisiones o áreas en una página que contienen elementos como múltiples campos, otra página, un gráfico o iconos.<br /><br />Para obtener más información sobre la personalización de acciones, consulte [Personalización de acciones](ui-personalization-user.md#Actions). |
|Ocultar algo, un campo, una columna de la lista, un icono, una acción o una pieza.|Elija la punta de flecha y elija <b>Ocultar</b>.|El elemento aparece en gris cuando está en modo de personalización. Si el campo que oculta también se muestra en el encabezado de la ficha desplegable cuando está contraída, el campo ya no aparecerá allí.|
|Mostrar acciones y partes ocultas.|Para un elemento atenuado (oculto), elija la punta de flecha y luego elija <b>Mostrar</b>.|El elemento oculto vuelve a estar visible.|
|Agregar un campo o columna.|En el banner <b>Personalización</b>, elija la acción <b>+ Campo</b>.<br /></br>El panel <b>Agregar campo a página</b> se abre a la derecha. Muestra los campos que se pueden agregar a la página.<br /><br />Para agregar un campo, arrástrelo de panel a la posición que desee. La posición se indica con una fina línea vertical u horizontal.|Cada página incluye un conjunto predefinido de campos que puede mostrar. Siga este procedimiento para agregar campos o columnas que no se han mostrado anteriormente o para mostrar los campos que ha ocultado.|
|Muestre un campo de la cabecera de una ficha desplegable cuando está contraída.|Elija la punta de flecha y, a continuación, seleccione <b>Mostrar cuando se contrae</b>. <br /> <br />Si no hace ve esta opción, significa que ya está establecida. En este caso, para dejar de mostrar el campo del encabezado de la ficha desplegable, elija <b>Mostrar siempre</b>.|*Ficha desplegable* es el término que se utiliza para un grupo de campos que aparecerán bajo un encabezado común. Utilice la opción <b>Mostrar cuando se contrae</b> para mostrar los campos más importantes. Si selecciona un campo del encabezado, se abrirá la ficha desplegable y con el enfoque en el campo seleccionado.<br /><br />Esta opción solo es aplicable si una página tiene una más de una ficha desplegable. Si hay solo una ficha desplegable, no se puede contraer, por lo que la opción <b>Mostrar cuando se contrae</b> no está disponible.|
|Hacer que un campo se muestre solo cuando seleccione **Mostrar más**.|Elija la punta de flecha y, a continuación, seleccione <b>Mostrar en "Mostrar más"</b>. <br /> <br />Si no ve la opción <b>Mostrar en "Mostrar más"</b>, significa que ya está establecida. En este caso, para que un campo se muestre siempre, no solo al seleccionar **Mostrar más**, elija <b>Mostrar siempre</b>.||
|Cambiar la inmovilización de panel de una lista a otra columna. |Elija la punta de la flecha de la columna que desee establecer como la última de la inmovilización de panel y, a continuación, elija <b>Establecer inmovilización de panel</b>.<br /><br/>Si desea volver a configurar la inmovilización de panel en su posición original diseñada, elija la punta de flecha para la columna actual y elija <b>Borrar inmovilización de panel</b>. Nota: No puede eliminar la inmovilización de panel.|La inmovilización de panel especifica las columnas que siempre aparecen a la izquierda, incluso durante el desplazamiento horizontal.|  
|Saltar un campo al presionar Entrar.|Elija la punta de flecha junto al campo, o la cabecera de columna en una lista y seleccione **Excluir de entrada rápida**. <br /><br /> Si no ve esta opción, significa que el campo ya está establecido para saltarlo. En este caso, para dejar de omitir el campo, elija **Incluir en entrada rápida**. |Consulte [Acelerar la entrada de datos con la entrada rápida](ui-enter-data.md#QuickEntry)|
|Reordenar y eliminar vistas que representan listas filtradas.|Elija la punta de flecha situada junto a una vista y luego elija **Mover**, **Eliminar** u **Ocultar**.|Consulte [Guardar y personalizar vistas de lista](ui-views.md)|  
|Agregue una nueva acción a una página o informe en su área de tareas.|Desde la página de destino, la página de solicitud de informe o la ventana Avisarme, elija el icono de marcador.|Consulte [Marcar una página o informe en su área de tareas](ui-bookmarks.md)|
|Siempre empiece una lista como expandida o contraída|Elija el botón **Expandir todo** o **Contraer todo** en la esquina superior izquierda de la lista. Alternativamente, elija la acción **Expandir todo** o **Contraer todo** en el menú de la primera columna. |Se aplica a las listas jerárquicas contraíbles.|

## <a name="a-nameactionsapersonalizing-the-action-bar-and-menus" /><a name="Actions"></a>Personalización de la barra de acciones y los menús

La personalización le permite decidir qué acciones se mostrarán en la barra de navegación, la barra de acciones y las áreas de tareas, y dónde se mostrarán. Puede mostrar, ocultar o mover acciones individuales o grupos de acciones.

El siguiente video muestra cómo personalizar acciones en páginas y áreas de tareas.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

La personalización de las barras de navegación y acciones se hace básicamente de la misma forma que con otros elementos de la interfaz de usuario. Sin embargo, lo que puede realizar con una acción o un grupo depende de dónde se encuentre la acción o el grupo. La mejor forma de averiguarlo es cambiar al modo de personalización y dejar que le guíen las puntas de flecha.

Hay un par de términos con los que debería estar familiarizado para entender mejor la personalización de las acciones: *grupo de acciones* y *categoría promocionada*.  

Un *grupo de acciones* es un elemento que se expande para mostrar otras acciones o grupos. Por ejemplo, en la página **Pedidos de venta**, un grupo de acciones es la acción **Funciones** que aparece cuando elige la acción **Acciones**.

Una *categoría promocionada* es un grupo de acciones que antes de la línea vertical `|` en la barra de acciones. Las categorías suelen incluir las acciones más utilizadas, para que pueda encontrarlas rápidamente. Por ejemplo, en la página **Pedidos de venta**, las acciones **Pedido**, **Lanzamiento** y **Registro** son categorías promocionadas.

> [!NOTE]  
> Para borrar la personalización, seleccione la punta de flecha alrededor del menú del diseñador de la pieza y luego elija **Borrar personalización**.

### <a name="to-remove-hide-and-show-actions-and-action-groups" />Para eliminar, ocultar y mostrar acciones y grupos de acciones

Cuando desee mostrar u ocultar una acción, las opciones situadas debajo de la punta de flecha definen lo que puede hacer dependiendo del estado de la acción. 

1. Elija la punta de flecha de una acción o grupo de acciones.
2. Elija de una de las siguientes opciones:

|Opción|Lo que hace|
|------|------------
|**Eliminar**|Esta opción aparece si la acción seleccionada también se muestra en otro lugar de la barra de navegación o barra de acciones. Al seleccionar esta opción se elimina la acción de la ubicación seleccionada para que ya no aparezca. La acción o grupo de acciones permanecerá en otros lugares. |
|**Ocultar**|Esta opción aparece si la acción o el grupo de acciones no se encuentra en otro lugar de la barra de navegación o barra de acciones. Como **Eliminar**, al elegir esta opción se provocará que la acción o el grupo de acciones desaparezca de la barra de navegación o barra de acciones. No obstante, en el modo de personalización, aún se mostrará la acción o el grupo de acciones en la posición actual, excepto que aparece atenuada.|
|**Mostrar**|Esta opción aparece si la acción o grupo de acciones ha sido previamente ocultada (atenuada). Al elegir esta opción se provocará que la acción o el grupo de acciones aparezca en la barra de navegación o barra de acciones.|

### <a name="to-move-actions-and-action-groups" />Para mover acciones y grupos de acciones

El lugar donde se pueden soltar acciones o grupos de acciones se indica mediante una línea horizontal entre dos acciones o un borde alrededor de un grupo de acciones. Existen las siguientes limitaciones:

- Puede mover acciones individuales a las categorías promocionadas, pero no puede reorganizar el orden de las acciones en la categoría.
- No puede mover un grupo de acciones a una categoría promocionada.

1. Para mover una acción o grupo de acciones, arrástrelo y suéltelo en la posición deseada, igual que hace con los campos y columnas.
2. Para mover una acción o un grupo de acciones a otro grupo de acciones que está vacío, arrastre la acción o el grupo de acciones al nuevo grupo y colóquelo en el cuadro **Colocar aquí una acción** .

## <a name="a-namepartsapersonalizing-parts" /><a name="Parts"></a>Personalizar partes

Las partes son áreas de una página que normalmente se componen de varios campos, gráficos u otro contenido. Una parte muestra un borde de color cuando se enfoca en la parte. Por ejemplo, una pantalla de inicio del área de tareas tiene varias partes. Debido a su límite bien definido, puede personalizar toda la parte, así como su contenido.

- Para mover una parte, arrástrela y suéltela en la posición deseada. Una línea de color indica las posiciones válidas en la pantalla. Por ejemplo, los cuadros informativos solo se pueden mover junto a otros cuadros informativos en el panel Cuadro informativo.
- Puede ocultar una parte eligiendo la opción **Ocultar** bajo la punta de flecha.
- Cuando comience a personalizar o navegue a una nueva página, cualquier parte que esté actualmente oculta aparecerá en la página con imágenes distintivas para indicar que están ocultas. Puede mostrar la parte eligiendo la opción **Mostrar** bajo la punta de flecha.

Puede borrar todos los cambios de personalización que haya realizado en una sola parte seleccionando la opción **Borrar personalización** bajo la punta de flecha de la parte. Borrar la personalización de una parte solo afecta a los cambios en el contenido de la parte, no a la ubicación ni a la visibilidad de la parte en la página.  

## <a name="to-clear-personalization" />Para borrar la personalización

En algún momento, es posible que desee borrar algunos o todos los cambios de personalización que hizo en esta página a lo largo del tiempo.

1. En el banner **Personalización**, elija la acción **Borrar personalización**.
2. Elija una de las siguientes opciones.  

> [!CAUTION]
> El borrado de la personalización no se puede deshacer.

|Opción|Lo que hace|
|------|------------
|**Solo menú de navegación**|Borra cualquier cambio de personalización que haya realizado en el menú de navegación que se comparte en el área de tareas y otras páginas. Tales cambios incluyen cualquier acción nueva que se haya agregado como marcador y cualquier cambio en los enlaces y grupos en el menú.|  
|**Solo acciones**|Borra todos los cambios de personalización que haya realizado en las barras de navegación o acciones en la página.|
|**Solo campos y columnas**|Borra todos los cambios de personalización que haya realizado en la página excepto cambios en la barra de navegación o de acciones. Tales cambios incluyen cambios en los campos, columnas, piezas e iconos. |
|**Todo**|Borra todos los cambios de personalización que haya realizado para que se parezca a la original. Tales cambios incluyen cambios en las barras de navegación y de acciones, campos, columnas, partes e iconos.|

## <a name="other-points-of-interest" />Otros puntos de interés

Para ayudarle a comprender mejor la personalización, le presentamos algunos consejos.

- Cuando realice cambios en una página de ficha que abre de una lista, los cambios tendrán efecto en todos los registros que abra de esa lista. Por ejemplo, digamos que abre un cliente específico desde la página de la lista Clientes y la personaliza agregando un campo. Cuando abra otros clientes de la lista, también se mostrará el campo que agregó.
- Los cambios realizados tendrán efecto en todas las áreas de tareas. Por ejemplo, si realiza un cambio en la lista Clientes cuando el área de tareas está configurada en administrador de negocio, también verá el cambio en la página **Clientes** cuando el área de tareas está configurada en Procesador de pedidos de ventas.
- Los cambios de una página realizados en un panel tendrán efecto en la página donde se muestre.  
- Solo puede agregar campos y columnas de una lista predefinida, que está basada en la página. No puede crear campos ni columnas nuevos.
- El elemento **Power Automate** en la barra de acciones
  - No puede ocultar o mover el elemento **Automatizar** o el subelemento **Power Automate** y sus acciones **Crear un flujo** y **Administrar flujos**.
  - Puede mover los flujos incluidos en el elemento **Automatizar**, pero no puede ocultarlos mediante la personalización. Mover el flujo hace una copia del flujo al destino, no lo eliminará del elemento **Automatizar**.

   > [!TIP]
   > Como administrador, puede ocultar el elemento **Automatización** de los usuarios. Obtenga más información en [Configurar la integración de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="see-related-microsoft-trainingtrainingmodulespersonalize-ui-dynamics-365-business-centralindex" />Consultar la [formación de Microsoft](/training/modules/personalize-ui-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también
[Personalizar páginas para perfiles](ui-personalization-manage.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
