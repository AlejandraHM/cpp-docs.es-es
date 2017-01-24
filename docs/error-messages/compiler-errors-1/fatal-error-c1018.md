---
title: "Error irrecuperable C1018 | Microsoft Docs"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C1018"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C1018"
ms.assetid: 2ceb8a99-30b2-4b80-bf42-e9f3305b3c52
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error irrecuperable C1018
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

\#elif inesperada  
  
 La directiva `#elif` aparece fuera de una construcción `#if`, `#ifdef` o `#ifndef`. Use `#elif` solamente dentro de una de estas construcciones.  
  
 El ejemplo siguiente genera la advertencia C1018:  
  
```  
// C1018.cpp #elif      // C1018 #endif int main() {}  
```  
  
 Posible solución:  
  
```  
// C1018b.cpp #if 1 #elif #endif int main() {}  
```