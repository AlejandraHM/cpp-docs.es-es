---
title: "Error del compilador C2894 | Microsoft Docs"
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
  - "C2894"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2894"
ms.assetid: 4e250579-2b59-4993-a6f4-49273e7ecf06
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C2894
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

no se puede declarar una vinculación C para las plantillas  
  
 Una plantilla definida dentro un bloque `extern`  "C" puede producir este error.  
  
 El código siguiente genera el error C2894:  
  
```  
// C2894.cpp  
extern "C" {  
   template<class T> class stack {};   // C2894 fail  
  
   template<class T> void f(const T &aT) {}   // C2894  
}  
```  
  
 El código siguiente genera el error C2894:  
  
```  
// C2894b.cpp  
// compile with: /c  
extern "C" template<class T> void f(const T &aT) {}   // C2894  
  
template<class T> void f2(const T &aT) {}   // OK  
```