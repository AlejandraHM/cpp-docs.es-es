---
title: Definiciones de tipo &lt;new&gt; | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: aef01de1-06b5-4b6c-aebc-2c9f423d7e47
caps.latest.revision: 7
manager: ghogen
translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: b652d0a1eac1615d1e1b0aed1df05d6a9ee661a3
ms.lasthandoff: 02/24/2017

---
# <a name="ltnewgt-typedefs"></a>Definiciones de tipo &lt;new&gt;
||  
|-|  
|[new_handler](#new_handler)|  
  
##  <a name="a-namenewhandlera--newhandler"></a><a name="new_handler"></a> new_handler  
 El tipo que apunta a una función que se puede usar como un controlador nuevo.  
  
```
typedef void (*new_handler)();
```  
  
### <a name="remarks"></a>Comentarios  
 Este tipo de función de controlador se llama mediante **operatornew** o `operator new[]` cuando no pueden satisfacer una solicitud de almacenamiento adicional.  
  
### <a name="example"></a>Ejemplo  
  Vea [set_new_handler](../standard-library/new-functions.md#set_new_handler) para obtener un ejemplo que usa `new_handler` como un valor devuelto.  
  
## <a name="see-also"></a>Vea también  
 [\<new>](../standard-library/new.md)




