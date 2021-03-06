---
title: auto_inline
ms.date: 11/04/2016
f1_keywords:
- auto_inline_CPP
- vc-pragma.auto_inline
helpviewer_keywords:
- pragmas, auto_inline
- auto_inline pragma
ms.assetid: f7624cd1-be76-429a-881c-65c9040acf43
ms.openlocfilehash: a3e49941271ec294ddb69861d12e3451332770fe
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50633354"
---
# <a name="autoinline"></a>auto_inline
Excluye cualquier función definida dentro del intervalo donde **desactivar** se especifica a partir del que se consideran candidatas para la expansión automática alineada.

## <a name="syntax"></a>Sintaxis

```
#pragma auto_inline( [{on | off}] )
```

## <a name="remarks"></a>Comentarios

Para usar el **auto_inline** pragma, colóquela delante e inmediatamente después (no en) una definición de función. La pragma surte efecto en cuanto aparece en la primera definición de función.

## <a name="see-also"></a>Vea también

[Directivas pragma y la palabra clave __Pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)