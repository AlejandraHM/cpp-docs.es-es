---
title: Entradas del registro (ATL)
ms.date: 11/04/2016
helpviewer_keywords:
- registry, ATL services entries
- registry, application IDs
ms.assetid: 881989b7-61bb-459a-a13e-3bfcb33e184e
ms.openlocfilehash: b61aae9ba9316dded1dcb11353e52eb2fffd49a2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50472883"
---
# <a name="registry-entries"></a>Entradas del Registro

DCOM introdujo el concepto de identificadores de aplicación (AppID), que agrupa las opciones de configuración para uno o más objetos DCOM en una ubicación centralizada en el registro. Especificar un AppID indicando su valor en el AppID valor bajo el CLSID del objeto con nombre.

De forma predeterminada, un servicio generado con ATL utiliza su CLSID como el GUID para su AppID. En `HKEY_CLASSES_ROOT\AppID`, puede especificar entradas específicas de DCOM. Inicialmente, existen dos entradas:

- `LocalService`, con un valor igual al nombre del servicio. Si no existe este valor, se utiliza en lugar de la `LocalServer32` clave en el CLSID.

- `ServiceParameters`, con un valor igual a `-Service`. Este valor especifica los parámetros que se pasarán al servicio cuando se inicia. Tenga en cuenta que estos parámetros se pasan al servicio `ServiceMain` funcione, no `WinMain`.

Cualquier servicio DCOM también tiene que crear otra clave bajo `HKEY_CLASSES_ROOT\AppID`. Esta clave es igual al nombre del archivo EXE y actúa como una referencia cruzada, ya que contiene un valor de AppID que apunta a las entradas de AppID.

## <a name="see-also"></a>Vea también

[Servicios](../atl/atl-services.md)

