---
title: Error del compilador C2396
ms.date: 11/04/2016
f1_keywords:
- C2396
helpviewer_keywords:
- C2396
ms.assetid: 1b515ef6-7af4-400f-b4ed-564313ea15f6
ms.openlocfilehash: d320f78937fc60910bbed4a5b1b89841ea674fb7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50438104"
---
# <a name="compiler-error-c2396"></a>Error del compilador C2396

' your_type '': CLR o WinRT functionnot de conversión definido por el usuario válida. Debe convertir de o a: 'T^', 'T^%', 'T^&', donde T = 'your_type'

Una función de conversión en un tipo administrado o de Windows Runtime no tenía al menos un parámetro con un tipo igual al tipo que contiene la función de conversión.

El siguiente ejemplo genera el error C2396 y muestra cómo corregirlo:

```
// C2396.cpp
// compile with: /clr /c

ref struct Y {
   static operator int(char c);   // C2396

   // OK
   static operator int(Y^ hY);
   // or
   static operator Y^(char c);
};
```