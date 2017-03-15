---
title: "Error del compilador C2118 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2118"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2118"
ms.assetid: bf4315d0-f085-4323-b813-96ee61a13bde
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# Error del compilador C2118
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

subíndice negativo  
  
 El valor que define el tamaño de la matriz supera el valor máximo de matriz o es menor que cero.  
  
 El código siguiente genera el error C2118:  
  
```  
// C2118.cpp  
int main() {  
   int array1[-1];   // C2118  
   int array2[3];   // OK  
}  
```