---
title: Error irrecuperable C1071
ms.date: 11/04/2016
f1_keywords:
- C1071
helpviewer_keywords:
- C1071
ms.assetid: 489f1786-370e-4ecd-af67-538fe6e5bd4e
ms.openlocfilehash: 8fe6b0f3bb1253f72c97f29070ba81cdbdf80508
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50506709"
---
# <a name="fatal-error-c1071"></a>Error irrecuperable C1071

no se esperaba el final de archivo encontrado en el comentario

El compilador ha alcanzado el final del archivo mientras se analizaba un comentario.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>Posibles causas del error:

1. Falta el terminador de comentario (* /).

1. Falta el carácter de nueva línea después de un comentario en la última línea de un archivo de origen.

El ejemplo siguiente genera C1071:

```
// C1071.cpp
int main() {
}

/* this comment is fine */
/* forgot the closing tag        // C1071
```