---
title: Error del compilador C2313
ms.date: 11/04/2016
f1_keywords:
- C2313
helpviewer_keywords:
- C2313
ms.assetid: f70eb19b-c0a3-4fb2-ade1-3890a589928d
ms.openlocfilehash: 276dea87770035967a08ca5ac3e95316832ffc1b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50641082"
---
# <a name="compiler-error-c2313"></a>Error del compilador C2313

'type1': está capturado por una referencia ('type2') en el número de línea

El tipo de excepción tiene dos controladores. El tipo del segundo elemento catch es una referencia del tipo de la primera.

El ejemplo siguiente genera la advertencia C2313:

```
// C2313.cpp
// compile with: /EHsc
#include <eh.h>
class C {};
int main() {
    try {
        throw "ooops!";
    }
    catch( C& ) {}
    catch( C ) {}   // C2313
}
```