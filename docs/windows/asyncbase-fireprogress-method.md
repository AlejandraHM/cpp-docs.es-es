---
title: Fireprogress (método) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncBase::FireProgress
dev_langs:
- C++
helpviewer_keywords:
- FireProgress method
ms.assetid: 4512bef6-0ebc-4465-9b8a-4c9dfa82084c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 9d6cdab8d93394f4c51a4b99622d2f6f8604a87e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2018
ms.locfileid: "46414699"
---
# <a name="asyncbasefireprogress-method"></a>AsyncBase::FireProgress (Método)

Invoca el controlador de eventos de progreso actual.

## <a name="syntax"></a>Sintaxis

```cpp
void FireProgress(
   const typename ProgressTraits::Arg2Type arg
);
```

### <a name="parameters"></a>Parámetros

*arg*<br/>
Método de controlador de eventos que se va a invocar.

## <a name="remarks"></a>Comentarios

`ProgressTraits` se deriva de [ArgTraitsHelper (estructura)](../windows/argtraitshelper-structure.md).

## <a name="requirements"></a>Requisitos

**Encabezado:** async.h

**Espacio de nombres:** Microsoft::WRL

## <a name="see-also"></a>Vea también

[AsyncBase (clase)](../windows/asyncbase-class.md)