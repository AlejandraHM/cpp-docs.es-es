---
title: pop_macro | Documentos de Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- vc-pragma.pop_macro
- pop_macro_CPP
dev_langs:
- C++
helpviewer_keywords:
- pop_macro pragma
- pragmas, pop_macro
ms.assetid: 3b5489d0-69ba-4c66-b572-2748af0f12bb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7790cadf9b5bc0b9a1fa37b5131f4fb704142ad2
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2018
---
# <a name="popmacro"></a>pop_macro
Establece el valor de la *macro_name* macro en el valor en la parte superior de la pila para esta macro.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
#pragma pop_macro("  
macro_name  
")  
  
```  
  
## <a name="remarks"></a>Comentarios  
 En primer lugar debe emitir una [push_macro](../preprocessor/push-macro.md) para *macro_name* para poder realizar una **pop_macro**.  
  
## <a name="example"></a>Ejemplo  
  
```  
// pragma_directives_pop_macro.cpp  
// compile with: /W1  
#include <stdio.h>  
#define X 1  
#define Y 2  
  
int main() {  
   printf("%d",X);  
   printf("\n%d",Y);  
   #define Y 3   // C4005  
   #pragma push_macro("Y")  
   #pragma push_macro("X")  
   printf("\n%d",X);  
   #define X 2   // C4005  
   printf("\n%d",X);  
   #pragma pop_macro("X")  
   printf("\n%d",X);  
   #pragma pop_macro("Y")  
   printf("\n%d",Y);  
}  
```  
  
```Output  
1  
2  
1  
2  
1  
3  
```  
  
## <a name="see-also"></a>Vea también  
 [Directivas pragma y la palabra clave __Pragma](../preprocessor/pragma-directives-and-the-pragma-keyword.md)