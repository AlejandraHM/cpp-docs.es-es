---
title: "Error del compilador C2182 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2182"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2182"
ms.assetid: dfd8d47d-9606-496e-bd96-4bf41ba1f857
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Error del compilador C2182
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifier': uso no válido del tipo 'void'  
  
 Una variable se declara de tipo `void`.  
  
 El ejemplo siguiente genera la advertencia C2182:  
  
```  
// C2182.cpp // compile with: /c int main() { int i = 10; void &ir = i;   // C2182 cannot have a reference to type void int &ir = i;   // OK }  
```