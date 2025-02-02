---
title: Crear una nueva ruta
description: Tutorial para aprender a introducir manualmente toda la información para una nueva ruta en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# <a name="walkthrough-create-a-new-routing" />Tutorial: Crear una nueva ruta

En este artículo, le guiaremos por los pasos para usar los datos de demostración de Contoso Coffee para configurar manualmente una nueva ruta de producción en [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="scenario" />Caso

Oscar, el ingeniero de procesos de Contoso Coffee, decide crear una nueva ruta con el nombre *Nueva ruta de acceso*. Puesto que esta ruta es diferente a cualquier otra ruta de Contoso Coffee, Óscar debe introducir manualmente toda la información de enrutamiento.  

## <a name="steps" />Pasos

1. Cree el encabezado de la ruta.  

    1. Elija el icono ![Bombilla que abre la función Dígame, escriba Configuración asistida.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Rutas** y luego elija el vínculo relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº** |1099|
        |**Descripción** |Nueva ruta de acceso|
2. Cree las líneas de la ruta.

    1. En la ficha desplegable **Líneas**, agrega una nueva línea y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº operación** |10|
        |**Escriba** |Centro trabajo|
        |**Nº** |100|
        |**Tiempo preparación** |nº 20|
        |**Tiempo ejecución** |15|

    2. Agrega una nueva línea y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº operación** |nº 20|
        |**Escriba** |Centro trabajo|
        |**Nº** |200|
        |**Tiempo preparación** |30|
        |**Tiempo ejecución** |5|
3. Certifique la ruta.

    1. En el campo **Estado**, elija *Certificado*.  

La nueva ruta ya está configurada.  

## <a name="see-also" />Consulte también .

[Introducción a datos de demostración de Contoso Coffee](../contoso-coffee-intro.md)  
