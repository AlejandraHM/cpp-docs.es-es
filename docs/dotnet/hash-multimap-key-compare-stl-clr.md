---
title: 'hash_multimap:: key_compare (STL/CLR) | Documentos de Microsoft'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- cliext::hash_multimap::key_compare
dev_langs:
- C++
helpviewer_keywords:
- key_compare member [STL/CLR]
ms.assetid: 011f5bc3-0e40-48fe-9d6f-f6960210a27a
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 7394d12b7f17da61b966399203837430b3a7713f
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2017
---
# <a name="hashmultimapkeycompare-stlclr"></a>hash_multimap::key_compare (STL/CLR)
El delegado para dos claves de ordenación.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
Microsoft::VisualC::StlClr::BinaryDelegate<GKey, GKey, bool>  
    key_compare;  
```  
  
## <a name="remarks"></a>Comentarios  
 El tipo es un sinónimo para el delegado que determina el orden de sus argumentos de la claves.  
  
## <a name="example"></a>Ejemplo  
  
```  
// cliext_hash_multimap_key_compare.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_multimap<wchar_t, int> Myhash_multimap;   
int main()   
    {   
    Myhash_multimap c1;   
    Myhash_multimap::key_compare^ kcomp = c1.key_comp();   
  
    System::Console::WriteLine("compare(L'a', L'a') = {0}",   
        kcomp(L'a', L'a'));   
    System::Console::WriteLine("compare(L'a', L'b') = {0}",   
        kcomp(L'a', L'b'));   
    System::Console::WriteLine("compare(L'b', L'a') = {0}",   
        kcomp(L'b', L'a'));   
    System::Console::WriteLine();   
  
// test a different ordering rule   
    Myhash_multimap c2 = cliext::greater<wchar_t>();   
    kcomp = c2.key_comp();   
  
    System::Console::WriteLine("compare(L'a', L'a') = {0}",   
        kcomp(L'a', L'a'));   
    System::Console::WriteLine("compare(L'a', L'b') = {0}",   
        kcomp(L'a', L'b'));   
    System::Console::WriteLine("compare(L'b', L'a') = {0}",   
        kcomp(L'b', L'a'));   
    return (0);   
    }  
  
```  
  
```Output  
compare(L'a', L'a') = True  
compare(L'a', L'b') = True  
compare(L'b', L'a') = False  
  
compare(L'a', L'a') = False  
compare(L'a', L'b') = False  
compare(L'b', L'a') = True  
```  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** \<cliext/hash_map >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>Vea también  
 [hash_multimap (STL/CLR)](../dotnet/hash-multimap-stl-clr.md)   
 [hash_multimap:: key_comp (STL/CLR)](../dotnet/hash-multimap-key-comp-stl-clr.md)   
 [hash_multimap:: KEY_TYPE (STL/CLR)](../dotnet/hash-multimap-key-type-stl-clr.md)   
 [hash_multimap::value_compare (STL/CLR)](../dotnet/hash-multimap-value-compare-stl-clr.md)