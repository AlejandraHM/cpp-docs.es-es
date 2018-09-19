---
title: Error del compilador C2071 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2071
dev_langs:
- C++
helpviewer_keywords:
- C2071
ms.assetid: f8c09255-a5c4-47e3-8089-3d875ae43cc5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 757110c88d3279964ab0c26f753e4d3b1f2889d5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/18/2018
ms.locfileid: "46025871"
---
# <a name="compiler-error-c2071"></a>Error del compilador C2071

'identificador': clase de almacenamiento no válida

`identifier` se ha declarado con un no válido [clase de almacenamiento](../../c-language/c-storage-classes.md). Este error puede producirse cuando se especifica más de una clase de almacenamiento para un identificador, o cuando la definición no es compatible con la declaración de clase de almacenamiento.

Para corregir este problema, averigüe la clase de almacenamiento previsto del identificador, por ejemplo, `static` o `extern`y corrija la declaración para hacer coincidir.

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera el error C2071.

```
// C2071.cpp
// compile with: /c
struct C {
   extern int i;   // C2071
};
struct D {
   int i;   // OK, no extern on an automatic
};
```

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera el error C2071.

```
// C2071_b.cpp
// compile with: /c
typedef int x(int i) { return i; }   // C2071
typedef int (x)(int);   // OK, no local definition in typedef
```