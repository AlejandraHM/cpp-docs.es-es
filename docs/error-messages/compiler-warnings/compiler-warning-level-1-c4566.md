---
title: Advertencia del compilador (nivel 1) C4566
ms.date: 11/04/2016
f1_keywords:
- C4566
helpviewer_keywords:
- C4566
ms.assetid: 65f40730-e86f-447c-b37b-16caadcfe311
ms.openlocfilehash: c864feb2478e9f99ad6e4c0087dcef72b55de601
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50460273"
---
# <a name="compiler-warning-level-1-c4566"></a>Advertencia del compilador (nivel 1) C4566

carácter representado por el nombre de carácter universal 'char' no se puede representar en la página de códigos actual (página)

No todos los caracteres Unicode se pueden representar en la página de códigos ANSI actual.

Cadenas de caracteres estrechos (caracteres de byte único) se convierten en caracteres multibyte, mientras que no lo son cadenas anchas (caracteres de dos bytes).

El ejemplo siguiente genera C4566:

```
// C4566.cpp
// compile with: /W1
int main() {
   char c1 = '\u03a0';   // C4566
   char c2 = '\u0642';   // C4566

   wchar_t c3 = L'\u03a0';   // OK
   wchar_t c4 = L'\u0642';   // OK
}
```