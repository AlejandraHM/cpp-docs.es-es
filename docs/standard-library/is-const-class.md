---
title: "is_const (Clase) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "std.tr1.is_const"
  - "is_const"
  - "std::tr1::is_const"
  - "std.is_const"
  - "std::is_const"
  - "type_traits/std::is_const"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "is_const (clase) [TR1]"
  - "is_const"
ms.assetid: 55b8e887-9c3f-4a1d-823a-4a257337b205
caps.latest.revision: 20
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 20
---
# is_const (Clase)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Comprueba si el tipo es const.  
  
## Sintaxis  
  
```  
template<class Ty>  
    struct is_const;  
```  
  
#### Parámetros  
 `Ty`  
 Tipo que se va a consultar.  
  
## Comentarios  
 Una instancia del predicado de tipo es true si `Ty` es `const-qualified`.  
  
## Ejemplo  
  
```  
// std_tr1__type_traits__is_const.cpp   
// compile with: /EHsc   
#include <type_traits>   
#include <iostream>   
  
struct trivial   
    {   
    int val;   
    };   
  
int main()   
    {   
    std::cout << "is_const<trivial> == " << std::boolalpha   
        << std::is_const<trivial>::value << std::endl;   
    std::cout << "is_const<const trivial> == " << std::boolalpha   
        << std::is_const<const trivial>::value << std::endl;   
    std::cout << "is_const<int> == " << std::boolalpha   
        << std::is_const<int>::value << std::endl;   
    std::cout << "is_const<const int> == " << std::boolalpha   
        << std::is_const<const int>::value << std::endl;   
  
    return (0);   
    }  
  
```  
  
  **is\_const\<trivial\> \=\= false**  
**is\_const\<const trivial\> \=\= true**  
**is\_const\<int\> \=\= false**  
**is\_const\<const int\> \=\= true**   
## Requisitos  
 **Encabezado:** \<type\_traits\>  
  
 **Espacio de nombres:** std  
  
## Vea también  
 [\<type\_traits\>](../standard-library/type-traits.md)   
 [is\_volatile \(Clase\)](../standard-library/is-volatile-class.md)