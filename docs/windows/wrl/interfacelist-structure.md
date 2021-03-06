---
title: InterfaceList (estructura)
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::InterfaceList
helpviewer_keywords:
- InterfaceList structure
ms.assetid: 6ec3228d-eb3e-4b7e-aef1-7dcf17bdf61a
ms.openlocfilehash: 70565081338f953abb65d2cdc7c5f1eb869f75e5
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/16/2019
ms.locfileid: "54337726"
---
# <a name="interfacelist-structure"></a>InterfaceList (estructura)

Admite la infraestructura WRL y no está pensado para utilizarse directamente desde el código.

## <a name="syntax"></a>Sintaxis

```cpp
template <typename T, typename U>
struct InterfaceList;
```

### <a name="parameters"></a>Parámetros

*T*<br/>
Un nombre de interfaz la primera interfaz en la lista recursiva.

*U*<br/>
Un nombre de interfaz las interfaces restantes en la lista recursiva.

## <a name="remarks"></a>Comentarios

Se utiliza para crear una lista recursiva de las interfaces.

## <a name="members"></a>Miembros

### <a name="public-typedefs"></a>Definiciones de tipos públicas

|Name|Descripción|
|----------|-----------------|
|`FirstT`|Sinónimo de parámetro de plantilla *T*.|
|`RestT`|Sinónimo de parámetro de plantilla *U*.|

## <a name="inheritance-hierarchy"></a>Jerarquía de herencia

`InterfaceList`

## <a name="requirements"></a>Requisitos

**Encabezado:** implements.h

**Espacio de nombres**: Microsoft::WRL::Details

## <a name="see-also"></a>Vea también

[Microsoft::WRL::Details (espacio de nombres)](microsoft-wrl-details-namespace.md)