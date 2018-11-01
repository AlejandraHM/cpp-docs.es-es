---
title: Advertencia del compilador (nivel 1) C4600
ms.date: 11/04/2016
f1_keywords:
- C4600
helpviewer_keywords:
- C4600
ms.assetid: f023a2a1-7fc4-463f-a434-dc93fcd3f4e9
ms.openlocfilehash: fcfefd5b858df653551e7f3061a41d168c8ff3f0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50489614"
---
# <a name="compiler-warning-level-1-c4600"></a>Advertencia del compilador (nivel 1) C4600

\#pragma 'macro name': se esperaba una cadena vacía no válida

No se puede especificar una cadena vacía al insertar o extraer un nombre de macro con el [pop_macro](../../preprocessor/pop-macro.md) o [push_macro](../../preprocessor/push-macro.md).

El ejemplo siguiente genera C4600:

```
// C4600.cpp
// compile with: /W1
int main()
{
   #pragma push_macro("")   // C4600 passing an empty string
}
```