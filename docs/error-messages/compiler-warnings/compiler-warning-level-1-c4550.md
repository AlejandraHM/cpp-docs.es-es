---
title: Advertencia del compilador (nivel 1) C4550
ms.date: 11/04/2016
f1_keywords:
- C4550
helpviewer_keywords:
- C4550
ms.assetid: f902b4ed-5f17-48ea-b693-92f4fb8c8054
ms.openlocfilehash: eff3548ef43075a86f52086caf9b79158ad70cb9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50640770"
---
# <a name="compiler-warning-level-1-c4550"></a>Advertencia del compilador (nivel 1) C4550

expresión se evalúa como una función que le falta una lista de argumentos

Un puntero a una función sin referencia falta una lista de argumentos.

## <a name="example"></a>Ejemplo

```
// C4550.cpp
// compile with: /W1
bool f()
{
   return true;
}

typedef bool (*pf_t)();

int main()
{
   pf_t pf = f;
   if (*pf) {}  // C4550
   return 0;
}
```