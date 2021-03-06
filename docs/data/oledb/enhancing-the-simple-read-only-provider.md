---
title: Mejorar un proveedor sencillo de sólo lectura
ms.date: 10/26/2018
helpviewer_keywords:
- read-only poviders [C++]
- IRowsetLocate class
- IRowsetLocate class, adding to OLE DB template providers
- simple read-only poviders [C++]
ms.assetid: cba0e09f-44c1-41c1-9456-332aa13dc158
ms.openlocfilehash: 4b06eb77851df0bf0bd0d3ef91a3ea960835ccba
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50462925"
---
# <a name="enhancing-the-simple-read-only-provider"></a>Mejorar un proveedor sencillo de sólo lectura

Esta sección muestra cómo mejorar la [proveedor sencillo de sólo lectura](../../data/oledb/implementing-the-simple-read-only-provider.md) creado en la sección anterior. `IRowsetLocateImpl` crea una implementación para el `IRowsetLocate` interfaz y agrega compatibilidad con marcadores.

Si dispone de un proveedor de trabajo, desea mejorarlo para implementar la actualización del proveedor, controlar transacciones o mejorar el rendimiento del algoritmo de búsqueda de filas. Mayoría de las mejoras de proveedor implica agregar una interfaz a un objeto COM existente.

El ejemplo en los temas siguientes mejora el mecanismo de captura de filas mediante la adición del `IRowsetLocate` a la interfaz `CAgentRowset`. Los temas muestran cómo para:

- [Hacer RCustomRowset herede de IRowsetLocate](../../data/oledb/modifying-the-inheritance-of-rmyproviderrowset.md).

- [Determinar dinámicamente las columnas que se devuelven al consumidor](../../data/oledb/dynamically-determining-columns-returned-to-the-consumer.md).

## <a name="see-also"></a>Vea también

[Crear un proveedor sencillo de solo lectura](../../data/oledb/creating-a-simple-read-only-provider.md)<br/>
