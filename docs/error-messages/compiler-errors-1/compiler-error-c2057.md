---
title: Error del compilador C2057 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2057
dev_langs:
- C++
helpviewer_keywords:
- C2057
ms.assetid: 038a99d6-1f5a-42fa-8449-03b4ff11ee0b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fb9018224d10fa0104ee461e8bbeb659173fc9f0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051736"
---
# <a name="compiler-error-c2057"></a>Error del compilador C2057

se esperaba una expresión constante

El contexto exige una expresión constante, una expresión cuyo valor se conoce en tiempo de compilación.

El compilador debe conocer el tamaño de un tipo en tiempo de compilación para poder asignar espacio para una instancia de ese tipo.

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera el error C2057 y muestra cómo corregirlo:

```
// C2057.cpp
int i;
int b[i];   // C2057 - value of i is unknown at compile time
int main() {
   const int i = 8;
   int b[i]; // OK - value of i is fixed and known to compiler
}
```

## <a name="example"></a>Ejemplo

C tiene reglas más restrictivas para las expresiones de constante.  El ejemplo siguiente genera el error C2057 y muestra cómo corregirlo:

```
// C2057b.c
#define ArraySize1 10
int main() {
   const int ArraySize2 = 10;
   int h[ArraySize2];   // C2057 - C does not allow variables here
   int h[ArraySize1];   // OK - uses preprocessor constant
}
```