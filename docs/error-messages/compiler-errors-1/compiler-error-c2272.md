---
title: "Error del compilador C2272 | Microsoft Docs"
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
  - "C2272"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2272"
ms.assetid: 1517706a-9c27-452e-9b10-3424b3d232bc
caps.latest.revision: 10
caps.handback.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C2272
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'función' : modificadores no permitidos en funciones miembro static  
  
 Se declarado una función miembro `static` con un especificador de modelo de memoria \(como [const](../../cpp/const-cpp.md) o [volatile](../../cpp/volatile-cpp.md)\), pero no se permite el uso de este tipo de modificadores en funciones miembro `static`.  
  
 El código siguiente genera el error C2272:  
  
```  
// C2272.cpp  
// compile with: /c  
class CMyClass {  
public:  
   static void func1() const volatile;   // C2272  func1 is static  
   void func2() const volatile;   // OK  
};  
```