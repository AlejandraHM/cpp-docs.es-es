---
title: Advertencia del compilador (nivel 3) C4240
ms.date: 11/04/2016
f1_keywords:
- C4240
helpviewer_keywords:
- C4240
ms.assetid: a2657cdb-18e1-493f-882b-4e10c0bca71d
ms.openlocfilehash: fe5306cc7909138fea0159553b53c2adc6a46dc0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50498246"
---
# <a name="compiler-warning-level-3-c4240"></a>Advertencia del compilador (nivel 3) C4240

extensión no estándar utilizada: acceso a 'classname' se ha definido como 'especificador de acceso', previamente se ha definido como 'especificador de acceso'

La compatibilidad con ANSI ([/Za](../../build/reference/za-ze-disable-language-extensions.md)), no se puede cambiar el acceso a una clase anidada. En las extensiones de Microsoft (/Ze) de forma predeterminada, es posible, con esta advertencia.

## <a name="example"></a>Ejemplo

```
// C4240.cpp
// compile with: /W3
class X
{
private:
   class N;
public:
   class N
   {   // C4240
   };
};

int main()
{
}
```