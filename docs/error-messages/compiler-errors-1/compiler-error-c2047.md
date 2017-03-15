---
title: "Error del compilador C2047 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2047"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2047"
ms.assetid: 686a5a81-3857-4753-84a0-5c2e7149cbee
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Error del compilador C2047
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

palabra clave default no válida  
  
 La palabra clave `default` solo puede aparecer en una instrucción `switch`.  
  
 El ejemplo siguiente genera la advertencia C2047:  
  
```  
// C2047.cpp int main() { int i = 0; default:   // C2047 switch(i) { case 0: break; } }  
```  
  
 Posible solución:  
  
```  
// C2047b.cpp int main() { int i = 0; switch(i) { case 0: break; default: break; } }  
```