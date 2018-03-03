---
title: Advertencia de compilador Error C2603 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2603
dev_langs:
- C++
helpviewer_keywords:
- C2603
ms.assetid: 9ca520d0-f082-4b65-933d-17c3bcf8b02c
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: c06c5747a3d785242e8b926fe6e1eaa251a2d8b4
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2603"></a>Advertencia C2603 de Error del compilador  
  
> '*función*': hay demasiados objetos static de ámbito de bloque con constructores y destructores en la función  
  
En las versiones del compilador de Visual C++ antes de Visual Studio 2015, o cuando la [/Zc: threadsafeinit](../../build/reference/zc-threadsafeinit-thread-safe-local-static-initialization.md) se especifica la opción del compilador, hay un límite de 31 en el número de objetos estáticos puede tener en una función insertada visible externamente .  
  
Para resolver este problema, se recomienda adoptar una versión más reciente del conjunto de herramientas del compilador de Visual C++, o si es posible, quite la opción del compilador/Zc: threadsafeinit. Si esto no es posible, considere la posibilidad de combinar los objetos estáticos. Si los objetos son del mismo tipo, considere la posibilidad de uso de una matriz estática de ese tipo y hacer referencia a miembros individuales según sea necesario.
  
## <a name="example"></a>Ejemplo  
  
El código siguiente genera la advertencia C2603 y muestra una forma de corregirlo:  
  
```cpp  
// C2603.cpp  
// Compile by using: cl /W4 /c /Zc:threadSafeInit- C2603.cpp
struct C { C() {} };  
extern inline void f1() {  
    static C C01, C02, C03, C04, C05, C06, C07, C08, C09, C10;
    static C C11, C12, C13, C14, C15, C16, C17, C18, C19, C20;
    static C C21, C22, C23, C24, C25, C26, C27, C28, C29, C30, C31;  
    static C C32;   // C2603 Comment this line out to avoid error  
}  
```
