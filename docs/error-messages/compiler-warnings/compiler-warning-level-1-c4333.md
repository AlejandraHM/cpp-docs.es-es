---
title: Advertencia del compilador (nivel 1) C4333
ms.date: 11/04/2016
f1_keywords:
- C4333
helpviewer_keywords:
- C4333
ms.assetid: d3763c52-6110-4da0-84db-5264e3f3f166
ms.openlocfilehash: b0f87b5d839dcfbb577af567a1a51a95daf716f0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50557357"
---
# <a name="compiler-warning-level-1-c4333"></a>Advertencia del compilador (nivel 1) C4333

'operador': desplazamiento a la derecha por cantidad demasiado grande, la pérdida de datos

Una operación de desplazamiento a la derecha era demasiado grande.  Todos los bits significativos son desplazados y el resultado siempre será cero.

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera C4333.

```
// C4333.cpp
// compile with: /c /W1
unsigned shift8 (unsigned char c) {
   return c >> 8;   // C4333

   // try the following line instead
   // return c >> 4;   // OK
}
```