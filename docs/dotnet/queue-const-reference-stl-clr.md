---
title: Queue::const_reference (STL/CLR) | Documentos de Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::queue::const_reference
dev_langs:
- C++
helpviewer_keywords:
- const_reference member [STL/CLR]
ms.assetid: e2398b75-e072-4769-82df-f2607e29c6e4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 10b1036f475c92e26a8c980481be05a08867a210
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33158734"
---
# <a name="queueconstreference-stlclr"></a>queue::const_reference (STL/CLR)
El tipo de una referencia constante a un elemento.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
typedef value_type% const_reference;  
```  
  
## <a name="remarks"></a>Comentarios  
 El tipo describe una referencia constante a un elemento.  
  
## <a name="example"></a>Ejemplo  
  
```  
// cliext_queue_const_reference.cpp   
// compile with: /clr   
#include <cliext/queue>   
  
typedef cliext::queue<wchar_t> Myqueue;   
int main()   
    {   
    Myqueue c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display contents " a b c"   
    for (; !c1.empty(); c1.pop())   
        {   // get a const reference to an element   
        Myqueue::const_reference cref = c1.front();   
        System::Console::Write(" {0}", cref);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** \<cliext/cola >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>Vea también  
 [cola (STL/CLR)](../dotnet/queue-stl-clr.md)   
 [Queue::Reference (STL/CLR)](../dotnet/queue-reference-stl-clr.md)   
 [queue::value_type (STL/CLR)](../dotnet/queue-value-type-stl-clr.md)