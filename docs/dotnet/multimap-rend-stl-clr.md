---
title: 'multimap:: rend (STL/CLR) | Documentos de Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::multimap::rend
dev_langs:
- C++
helpviewer_keywords:
- rend member [STL/CLR]
ms.assetid: f8d3f683-eeab-4a8b-af3f-fb6653114594
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: de3fd95db962b5bc4c5d5622c15b5dd67f5060e7
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33134250"
---
# <a name="multimaprend-stlclr"></a>multimap::rend (STL/CLR)
Designa el final de la secuencia controlada inversa.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
reverse_iterator rend();  
```  
  
## <a name="remarks"></a>Comentarios  
 La función miembro devuelve un iterador inverso que apunta inmediatamente después del principio de la secuencia controlada. Por tanto, designa el `end` de la secuencia inversa. Utilícelo para obtener un iterador que designa el `current` final de la secuencia controlada mostrada en orden inverso, pero su estado puede cambiar si cambia la longitud de la secuencia controlada.  
  
## <a name="example"></a>Ejemplo  
  
```  
// cliext_multimap_rend.cpp   
// compile with: /clr   
#include <cliext/map>   
  
typedef cliext::multimap<wchar_t, int> Mymultimap;   
int main()   
    {   
    Mymultimap c1;   
    c1.insert(Mymultimap::make_value(L'a', 1));   
    c1.insert(Mymultimap::make_value(L'b', 2));   
    c1.insert(Mymultimap::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Mymultimap::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// inspect first two items in reversed sequence   
    Mymultimap::reverse_iterator rit = c1.rend();   
    --rit;   
    --rit;   
    System::Console::WriteLine("*-- --rend() = [{0} {1}]",   
        rit->first, rit->second);   
    ++rit;   
    System::Console::WriteLine("*--rend() = [{0} {1}]",   
        rit->first, rit->second);   
    return (0);   
    }  
  
```  
  
```Output  
 [a 1] [b 2] [c 3]  
*-- --rend() = [b 2]  
*--rend() = [a 1]  
```  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** \<cliext/mapa >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>Vea también  
 [multimap (STL/CLR)](../dotnet/multimap-stl-clr.md)   
 [multimap:: begin (STL/CLR)](../dotnet/multimap-begin-stl-clr.md)   
 [multimap:: end (STL/CLR)](../dotnet/multimap-end-stl-clr.md)   
 [multimap::rbegin (STL/CLR)](../dotnet/multimap-rbegin-stl-clr.md)