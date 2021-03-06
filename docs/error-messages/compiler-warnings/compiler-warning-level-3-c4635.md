---
title: Advertencia del compilador (nivel 3) C4635
ms.date: 11/04/2016
f1_keywords:
- C4635
helpviewer_keywords:
- C4635
ms.assetid: b2ba90de-c093-4a76-8076-b65878467574
ms.openlocfilehash: 21873a883b19924ce3ef41511d65f8ae640875f4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50479241"
---
# <a name="compiler-warning-level-3-c4635"></a>Advertencia del compilador (nivel 3) C4635

destino del comentario del documento XML: XML incorrectamente formado: motivo

El compilador encontró algún problema con las etiquetas XML.  Corrija el problema y vuelva a compilar

El ejemplo siguiente genera la advertencia C4635:

```
// C4635.cpp
// compile with: /doc /clr /W3 /c
/// <summary>
/// The contents of the folder have changed.
/// <summary/>   // C4635

// try the following line instead
// /// </summary>
public ref class Test {};
```

Observe que la salida de este ejemplo indica: **La etiqueta final 'member' no coincide con la etiqueta inicial 'summary'**.

El problema con este ejemplo es que la etiqueta final \<resumen > está incorrectamente formada y el compilador no lo reconoce como el \<resumen > etiqueta de cierre.  El \<miembro > etiqueta a la que está incrustada en el archivo .xdc por el compilador en cada compilación/doc.  Por lo tanto, el problema es que la etiqueta de cierre \</member >, no coincide con la etiqueta inicial anterior que el compilador ha procesado (\<resumen >.