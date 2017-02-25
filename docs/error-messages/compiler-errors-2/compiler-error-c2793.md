---
title: "Error del compilador C2793 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2793"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2793"
ms.assetid: ce35f4e8-c357-40ca-95c4-15ff001ad69d
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Error del compilador C2793
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'token' : símbolo \(token\) inesperado después de '::', se esperaba un identificador o la palabra clave 'operator'  
  
 Los únicos tokens que pueden seguir a `__super::` son un identificador o la palabra clave `operator`.  
  
 El ejemplo siguiente genera C2793:  
  
```  
// C2793.cpp  
struct B {  
   void mf();  
};  
  
struct D : B {  
   void mf() {  
      __super::(); // C2793  
   }  
};  
```