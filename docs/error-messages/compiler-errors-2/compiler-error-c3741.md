---
title: "Error del compilador C3741 | Microsoft Docs"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3741"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3741"
ms.assetid: ed311315-cc32-49c9-97fa-01b293d81526
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C3741
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'clase': debe ser una coclase cuando el parámetro 'layout\_dependent' de event\_receiver se establece en true  
  
 Cuando `layout_dependent=true` para una clase [event\_receiver](../../windows/event-receiver.md), la clase también debe tener el atributo [coclass](../../windows/coclass.md).  
  
 El ejemplo siguiente genera C3741:  
  
```  
// C3741.cpp  
// compile with: /c  
// C3741 expected  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
#include <atlcom.h>  
[module(name="xx")];  
  
[object, uuid("00000000-0000-0000-0000-000000000001")]  
__interface I{ HRESULT f(); };  
  
// Delete the following line to resolve.  
[ event_receiver(com, layout_dependent=true)]  
  
// class or struct must be declared with coclass  
// Uncomment the following line to resolve.  
// [ event_receiver(com, layout_dependent=true), coclass, uuid("00000000-0000-0000-0000-000000000002")]  
struct R : I {  
   HRESULT f(){ return 0; }  
   R(){}  
   R(I* a){ __hook(I, a); }  
};  
```