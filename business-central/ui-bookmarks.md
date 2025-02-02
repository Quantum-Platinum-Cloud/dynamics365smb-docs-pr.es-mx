---
title: Marcador a una página o reporte en área de tareas
description: 'Con el nuevo icono de marcador, puede agregar una acción que abre una página o informe desde el menú de navegación de su área de tareas.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: null
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="bookmark-a-page-or-report-on-your-role-center" />Marque una página o informe en su área de tareas
Con el nuevo icono de marcador, puede agregar una acción que abre una página o informe desde el menú de navegación de su área de tareas. Los marcadores le permiten alcanzar rápidamente su contenido favorito o tareas comerciales. Agrega el marcador desde la página o informe de destino, lo que significa la pantalla que quiera vincular en el área de tareas para abrir.

El icono de marcador se muestra en la esquina superior derecha de una página y también en la ventana **Dígame** donde puede marcar de manera eficiente múltiples páginas o informes. Si ya existe un marcador para la página, el icono está oscuro y la información sobre herramientas indica "Marcado".

## <a name="to-bookmark-the-target-page" />Para marcar la página de destino
1. Abra cualquier página para la que desee un vínculo en su área de tareas.
2. Elija el icono ![Marcador.](media/ui_bookmark_icon.png "Marcador"). .

Ahora se agrega un nombre de acción según la página al menú de navegación en su área de tareas.

## <a name="to-bookmark-the-target-report" />Para marcar el informe de destino
1. Abra cualquier solicitud de informe para la que desee un vínculo en su área de tareas.
2. Elija el icono ![Marcador.](media/ui_bookmark_icon.png "Marcador") .

Ahora se agrega un nombre de acción según el informe al menú de navegación en su área de tareas.

## <a name="to-bookmark-a-page-or-report-from-the-tell-me-window" />Para marcar una página o un informe desde la ventana Avisarme
1. Abra la ventana **Dígame** e introduzca, por ejemplo, **Pedidos de venta**.
2. Pase el cursor sobre el resultado de búsqueda para la página o informe **Pedidos de venta** y luego elija el icono ![Marcador](media/ui_bookmark_icon.png "Marcador") .

Ahora se agrega un nombre de acción según la página o informe al menú de navegación en su área de tareas.


## <a name="frequently-asked-questions" />Preguntas más frecuentes

- **¿Puedo reorganizar mis marcadores?**  
Sí. Puede personalizar su área de tareas y mover las acciones a una secuencia más óptima o moverlas a grupos o subgrupos existentes.  
Aprenda a [Personalizar el área de trabajo](ui-personalization-user.md).

- **¿Cómo elimino un marcador?**  
En la página o informe de destino, vuelva a elegir el icono de marcador para eliminar la acción involucrada de su área de tareas. También puede personalizar su área de tareas y ocultar acciones temporalmente sin eliminarlas por completo.

- **¿Dónde encuentro mis marcadores?**  
Al agregar un marcador a una página o informe, la nueva acción se agrega al menú de navegación superior en su pantalla de inicio actual (área de tareas). Si tiene muchas acciones, es posible que deba activar el botón **Más** para mostrarlos todos porque la nueva acción siempre se agrega al final de esas acciones.
<!-- Should we add a screenshot here? -->

- **No tengo un icono de marcador. ¿Hay algo mal?**  
La capacidad de marcar una página o un informe es una de las muchas funciones de personalización del usuario en Business Central. Si no se muestra el icono de marcador, es probable que su administrador haya deshabilitado la personalización.

- **¿Por qué no puedo marcar ciertas páginas o informes?**  
No todas las páginas e informes se pueden agregar a favoritos. Cuando se ejecuta una página o un informe dentro de un contexto especial regido por la aplicación empresarial, no se muestra el icono de marcador. Por ejemplo, páginas que no se pueden encontrar en la ventana **Más información** pero se inician desde otro lugar no mostrará un icono de marcador. Del mismo modo, las páginas de solicitud de informes que solo se utilizan para recopilar filtros sin ejecutar el informe no mostrarán un icono de marcador.

  Ver detalles técnicos sobre [RunRequestPage](/dynamics365/business-central/dev-itpro/developer/methods-auto/report/reportinstance-runrequestpage-method) y [FilterPageBuilder](/dynamics365/business-central/dev-itpro/developer/methods-auto/filterpagebuilder/filterpagebuilder-data-type).

- **Al borrar mi personalización, ¿también se borrarán mis marcadores?**  
Sí. Los marcadores residen en el menú de navegación. Si borra los cambios en el menú de navegación desde cualquier página, o borra toda la personalización en el área de tareas, todas sus nuevas acciones se eliminarán permanentemente.

- **¿Por qué el icono de marcador continúa indicando que todavía no está marcado?**  
Cuando agrega un marcador, la nueva acción se agrega al menú de navegación en el área de tareas y las visitas posteriores a la página o informe muestran un ícono de marcador oscuro. Si personaliza su área de tareas y reorganiza sus acciones moviéndolas a grupos, el icono de marcador ya no estará oscuro y podrá agregar otro marcador a esa misma página o informe. Esto le permite agregar múltiples acciones a la misma página o informe y clasificarlas en diferentes grupos.

- **¿Por qué mi enlace a un informe muestra un informe diferente?**  
Algunos informes pueden ser sustituidos por otros informes después de aplicar una extensión a Business Central. Cuando se produce la sustitución, el texto de la nueva acción no se actualiza y continuará mostrando el nombre del informe original, pero navega hasta el informe más reciente. Para corregir el texto de la nueva acción, puede eliminar la nueva acción y agregarla nuevamente.
<!-- For more information on report substitution, see this link UNAVAILABLE AT THIS TIME -->

- **¿Están los marcadores disponibles para XMLports?**  
Nº En este momento, no es posible agregar acciones para abrir XMLports desde la interfaz de usuario.

- **¿Se traducirán mis marcadores cuando cambie mi idioma en Business Central?**  
Cuando se agrega una acción nueva, cualquier texto traducido que estaba disponible en ese momento se usará al marcar. Si se agrega texto traducido más tarde, la nueva acción no incluirá las traducciones más recientes.

- **¿Por qué no puedo agregar texto en una página directamente después de abrirla con el marcador?**<br> Cuando se marca una página, la página siempre se abrirá en el modo de visualización desde el marcador &mdash;incluso si estaba en el modo de edición cuando se marcó como favorito. Si selecciona el icono **Realizar cambios en la página** ![Muestra el icono de lápiz para editar la página.](media/edit-pencil.png) le permitirá agregar texto en los campos que son editables.


## <a name="see-also" />Consulte también
[Personalizar el área de trabajo](ui-personalization-user.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
