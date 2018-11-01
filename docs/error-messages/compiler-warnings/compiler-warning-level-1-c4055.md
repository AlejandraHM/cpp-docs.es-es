---
title: Advertencia del compilador (nivel 1) C4052
ms.date: 11/04/2016
f1_keywords:
- C4055
helpviewer_keywords:
- C4055
ms.assetid: f9955421-16ab-46e5-8f9d-bf1639a519ef
ms.openlocfilehash: e9fcb4356d993d86b622fd49c4a75d587554f7c2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50601323"
---
# <a name="compiler-warning-level-1-c4055"></a>Advertencia del compilador (nivel 1) C4055

> '*conversión*': del puntero de datos '*type1*'a puntero a función'*type2*'

## <a name="remarks"></a>Comentarios

**Obsoleto:** esta advertencia no se genera mediante Visual Studio 2017 y versiones posteriores.

Un puntero de datos se convierte (quizás incorrectamente) en un puntero de función. Se trata de una advertencia de nivel 1 en /Za y una advertencia de nivel 4 en /Ze.

## <a name="example"></a>Ejemplo

El ejemplo siguiente genera la advertencia C4055:

```C
// C4055.c
// compile with: /Za /W1 /c
typedef int (*PFUNC)();
int *pi;
PFUNC f() {
   return (PFUNC)pi;   // C4055
}
```

En /Ze, esta es una advertencia de nivel 4.

```C
// C4055b.c
// compile with: /W4 /c
typedef int (*PFUNC)();
int *pi;
PFUNC f() {
return (PFUNC)pi;   // C4055
}
```
