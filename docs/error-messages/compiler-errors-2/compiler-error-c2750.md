---
title: "Error del compilador C2750 | Microsoft Docs"
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
  - "C2750"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2750"
ms.assetid: 30450034-feb5-448c-9655-b8c5f3639695
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C2750
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'tipo' : no se puede utilizar 'new' en el tipo de referencia; utilice 'gcnew' en su lugar  
  
 Para crear una instancia de un tipo CLR, que haga que la instancia se coloque en la pila de recolección de elementos no utilizados, deberá utilizar [gcnew](../../windows/ref-new-gcnew-cpp-component-extensions.md).  
  
 El código siguiente genera el error C2750:  
  
```  
// C2750.cpp  
// compile with: /clr  
ref struct Y1 {};  
  
int main() {  
   Y1 ^ x = new Y1;   // C2750  
  
   // try the following line instead  
   Y1 ^ x2 = gcnew Y1;  
}  
```