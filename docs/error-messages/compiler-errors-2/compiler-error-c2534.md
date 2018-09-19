---
title: Error del compilador C2534 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2534
dev_langs:
- C++
helpviewer_keywords:
- C2534
ms.assetid: 481f9f54-5b51-4aa0-8eea-218f10807705
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2febeeeb3b6c0e394070339f2310a22c1326ab5c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049038"
---
# <a name="compiler-error-c2534"></a>Error del compilador C2534

'identifier': constructor no puede devolver un valor

Un constructor no puede devolver un valor o tienen un tipo de valor devuelto (ni siquiera un `void` tipo de valor devuelto).

Este error puede corregirse mediante la eliminación de la `return` instrucción desde la definición del constructor.

El ejemplo siguiente genera C2534:

```
// C2534.cpp
class A {
public:
   int i;
   A() { return i; }   // C2534
};
```