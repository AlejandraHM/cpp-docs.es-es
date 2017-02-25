---
title: "Error del compilador C3137 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3137"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3137"
ms.assetid: 70bb1313-2e87-43ed-a0d8-33fa6ff475e4
caps.latest.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 10
---
# Error del compilador C3137
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'propiedad' : no se puede inicializar una propiedad  
  
 No se puede inicializar una propiedad, por ejemplo, en la lista de inicializaciones de un constructor.  
  
 El código siguiente genera C3137:  
  
```  
// C3137.cpp  
// compile with: /clr /c  
ref class CMyClass {  
public:  
   property int Size {  
      int get() {  
         return 0;  
      }  
      void set( int i ) {}  
   }  
  
   CMyClass() : Size( 1 ) {   // C3137  
      // to resolve this C3137, remove the initializer from the  
      // ctor declaration and perform the assignment as follows  
      // Size = 1;  
   }  
};  
```  
  
 El código siguiente genera C3137:  
  
```  
// C3137_2.cpp  
// compile with: /clr:oldSyntax /c  
__gc class CMyClass {  
public:  
   __property int get_Size() {  
      return 0;  
   }  
   __property void set_Size(int i) {}  
  
   CMyClass() : Size(1) {   // C3137  
      // to resolve this C3137, remove the initializer from the  
      // ctor declaration and perform the assignment as follows  
      // Size = 1;  
   }  
};  
```