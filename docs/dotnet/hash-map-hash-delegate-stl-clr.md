---
title: "hash_map::hash_delegate (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::hash_map::hash_delegate"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "hash_delegate (miembro) [STL/CLR]"
ms.assetid: ae451fbe-a10c-457f-9b54-94dd9d93e8c4
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# hash_map::hash_delegate (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Busca un elemento que coincida con una clave especificada.  
  
## Sintaxis  
  
```  
hasher^ hash_delegate();  
```  
  
## Comentarios  
 La función miembro devuelve el delegado utilizado para convertir un valor de clave en un entero.  Se utiliza el hash una clave.  
  
## Ejemplo  
  
```  
// cliext_hash_map_hash_delegate.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
int main()   
    {   
    Myhash_map c1;   
    Myhash_map::hasher^ myhash = c1.hash_delegate();   
  
    System::Console::WriteLine("hash(L'a') = {0}", myhash(L'a'));   
    System::Console::WriteLine("hash(L'b') = {0}", myhash(L'b'));   
    return (0);   
    }  
  
```  
  
  **hash \(L'a\) \= 1616896120**  
**hash \(L'b\) \= 570892832**   
## Requisitos  
 cliext \<\/hash\_map de**Encabezado:** \>  
  
 cliext de**Espacio de nombres:**  
  
## Vea también  
 [hash\_map](../dotnet/hash-map-stl-clr.md)   
 [hash\_map::hasher](../dotnet/hash-map-hasher-stl-clr.md)