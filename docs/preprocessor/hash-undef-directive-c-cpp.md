---
title: '#undef (directiva) (C/C ++)'
ms.date: 11/04/2016
f1_keywords:
- '#undef'
helpviewer_keywords:
- '#undef directive'
- undef directive (#undef)
- preprocessor, directives
ms.assetid: 88900e0e-2c19-4a63-b681-f3d3133c24ca
ms.openlocfilehash: cb3a08165e41f336df0e141f50310f191cd83257
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50537272"
---
# <a name="undef-directive-cc"></a>#undef (Directiva) (C/C++)
Quita (anula la definición de) un nombre creado previamente con `#define`.

## <a name="syntax"></a>Sintaxis

```
#undef
identifier
```

## <a name="remarks"></a>Comentarios

El **#undef** directiva quita la definición actual de *identificador*. Por lo tanto, las apariciones posteriores de *identificador* se omiten el preprocesador. Para quitar una definición de macro con **#undef**, asigne a la macro *identificador* ; no proporcionan una lista de parámetros.

También puede aplicar el **#undef** la directiva a un identificador que no tiene ninguna definición anterior. De este modo se garantiza que el identificador no esté definido. No se realiza el reemplazo de macros en **#undef** instrucciones.

El **#undef** directiva se empareja normalmente con un `#define` directiva para crear una región en un programa de origen en el que un identificador tiene un significado especial. Por ejemplo, una función específica del programa de origen puede utilizar constantes de manifiesto para definir valores específicos del entorno que no afecten al resto del programa. El **#undef** directiva también funciona con el `#if` directiva para controlar la compilación condicional del programa de origen. Consulte [#if, #elif, #else y #endif directivas](../preprocessor/hash-if-hash-elif-hash-else-and-hash-endif-directives-c-cpp.md) para obtener más información.

En el ejemplo siguiente, la **#undef** directiva quita las definiciones de una constante simbólica y una macro. Observe que solo se proporciona el identificador de la macro.

```
#define WIDTH 80
#define ADD( X, Y ) ((X) + (Y))
.
.
.
#undef WIDTH
#undef ADD
```

**Específicos de Microsoft**

Las macros pueden estar indefinidas desde la línea de comandos mediante el `/U` seguido de los nombres de macros se definen. El efecto de emitir este comando es equivalente a una secuencia de `#undef` *nombre de la macro* instrucciones al principio del archivo.

**FIN de Específicos de Microsoft**

## <a name="see-also"></a>Vea también

[Directivas de preprocesador](../preprocessor/preprocessor-directives.md)