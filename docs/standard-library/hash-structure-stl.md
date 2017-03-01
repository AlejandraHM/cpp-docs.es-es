---
title: "Estructura hash (biblioteca estándar de C++) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- thread/std::hash
dev_langs:
- C++
ms.assetid: 4a8bf5bc-4334-4070-936b-98585f8a073b
caps.latest.revision: 13
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 3f69f0c3176d2fbe19e11ce08c071691a72d858d
ms.openlocfilehash: 599560617d55c32de25775d74dcf27240994c36b
ms.lasthandoff: 02/24/2017

---
# <a name="hash-structure-c-standard-library"></a>Estructura hash (biblioteca estándar de C++)
Define una función miembro que devuelve un valor que se determina de forma exclusiva mediante `Val`. La función miembro define una función [hash](../standard-library/hash-class.md) adecuada para asignar valores de tipo `thread::id` a una distribución de valores de índice.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
template <>  
struct hash<thread::id> :   
    public unary_function<thread::id, size_t>  
{  
    size_t operator()(thread::id Val) const;

 
};  
```  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** thread  
  
 **Espacio de nombres:** std  
  
## <a name="see-also"></a>Vea también  
 [Referencia de archivos de encabezado](../standard-library/cpp-standard-library-header-files.md)   
 [\<thread>](../standard-library/thread.md)   
 [Struct unary_function](../standard-library/unary-function-struct.md)

