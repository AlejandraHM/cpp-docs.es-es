---
title: Advertencia del compilador (nivel 1) C4677
ms.date: 11/04/2016
f1_keywords:
- C4677
helpviewer_keywords:
- C4677
ms.assetid: a8d656a1-e2ff-4f8b-9028-201765131026
ms.openlocfilehash: 66b8d42b63bcbf328703523c4eeda7a047f4643c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50533021"
---
# <a name="compiler-warning-level-1-c4677"></a>Advertencia del compilador (nivel 1) C4677

'function': signatura de miembro no privado contiene un tipo privado de ensamblado 'tipo_privado'

Un tipo que tiene accesibilidad pública fuera del ensamblado usa un tipo que tiene acceso privado fuera del ensamblado. Un componente que se hace referencia al tipo de ensamblado público no podrá usar el miembro de tipo o los miembros que hacen referencia al tipo privado de ensamblado.

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera C4677.

```
// C4677.cpp
// compile with: /clr /c /W1
delegate void TestDel();
public delegate void TestDel2();

public ref class MyClass {
public:
   static event TestDel^ MyClass_Event;   // C4677
   static event TestDel2^ MyClass_Event2;   // OK
};
```