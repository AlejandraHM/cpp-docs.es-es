---
title: "Error del compilador C2135 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2135"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2135"
ms.assetid: aa360d22-4f79-4de1-b384-93cadd10975f
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# Error del compilador C2135
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'bit operator': operación de campo de bits no válida  
  
 No se puede aplicar el operador address\-of \(`&`\) a un campo de bits.  
  
 El ejemplo siguiente genera la advertencia C2135:  
  
```  
// C2135.cpp struct S { int i : 1; }; struct T { int j; }; int main() { &S::i;   // C2135 address of a bit field &T::j;   // OK }  
```