---
title: Error del compilador C3480
ms.date: 11/04/2016
f1_keywords:
- C3480
helpviewer_keywords:
- C3480
ms.assetid: 7b2e055a-9604-4d13-861b-b38bda1a6940
ms.openlocfilehash: b856f607d764ac0a42781a80787663d965748317
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50626907"
---
# <a name="compiler-error-c3480"></a>Error del compilador C3480

'var': una variable de captura lambda debe pertenecer al ámbito de una función de inclusión

La variable de captura lambda no pertenece al ámbito de una función de inclusión.

### <a name="to-correct-this-error"></a>Para corregir este error

- Quite la variable de la lista de capturas de la expresión lambda.

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera el error C3480 porque la variable `global` no pertenece al ámbito de una función de inclusión:

```
// C3480a.cpp

int global = 0;
int main()
{
   [&global] { global = 5; }(); // C3480
}
```

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se resuelve C3480 quitando la variable `global` de la lista de captura de la expresión lambda:

```
// C3480b.cpp

int global = 0;
int main()
{
   [] { global = 5; }();
}
```

## <a name="see-also"></a>Vea también

[Expresiones lambda](../../cpp/lambda-expressions-in-cpp.md)