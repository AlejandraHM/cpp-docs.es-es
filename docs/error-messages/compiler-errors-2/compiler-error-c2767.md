---
title: Error del compilador C2767
ms.date: 11/04/2016
f1_keywords:
- C2767
helpviewer_keywords:
- C2767
ms.assetid: e8f84178-a160-4d71-a236-07e4fcc11e96
ms.openlocfilehash: 6c13610b6fd7aae4b4232b836a0307867bd591d7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50550155"
---
# <a name="compiler-error-c2767"></a>Error del compilador C2767

administrado o falta de coincidencia de dimensión WinRTarray: se esperaban N argumentos - M proporcionado

Una declaración de matriz administrada o de WinRT estaba mal formada. Para obtener más información, vea [Matriz](../../windows/arrays-cpp-component-extensions.md).

El siguiente ejemplo genera el error C2767 y muestra cómo corregirlo:

```
// C2767.cpp
// compile with: /clr
int main() {
   array<int> ^p1 = new array<int>(2,3); // C2767
   array<int> ^p2 = new array<int>(2);   // OK
}
```