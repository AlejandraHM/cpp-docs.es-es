---
title: "Error del compilador C3049 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3049"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3049"
ms.assetid: 6ddf54f6-2c30-4d04-b637-98c6c922c533
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Error del compilador C3049
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'arg': argumento no válido en la cláusula 'default' de OpenMP  
  
 Se pasó un valor incorrecto a una cláusula [default](../../parallel/openmp/reference/default-openmp.md).  
  
 El ejemplo siguiente genera la advertencia C3049:  
  
```  
// C3049.cpp // compile with: /openmp /c int main() { int n1 = 1; #pragma omp parallel default(private)   // C3049 // try the following line instead // #pragma omp parallel default(shared) { ++n1; } }  
```