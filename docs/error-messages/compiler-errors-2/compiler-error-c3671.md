---
title: "Error del compilador C3671 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3671"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3671"
ms.assetid: d684e4ae-87e2-4424-80bb-6f346652c831
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Error del compilador C3671
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'función\_1': la función no reemplaza 'función\_2'  
  
 Cuando se utiliza sintaxis de reemplazo explícita, el compilador genera un error si no se reemplaza una función.  Para obtener más información, vea [Invalidaciones explícitas](../../windows/explicit-overrides-cpp-component-extensions.md).  
  
## Ejemplo  
 El ejemplo siguiente genera el error C3671.  
  
```  
// C3671.cpp  
// compile with: /clr /c  
ref struct S {  
   virtual void f();  
};  
  
ref struct S1 : S {  
   virtual void f(int) new sealed = S::f;   // C3671  
   virtual void f() new sealed = S::f;  
};  
```