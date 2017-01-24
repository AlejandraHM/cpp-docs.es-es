---
title: "Error del compilador C3014 | Microsoft Docs"
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
  - "C3014"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3014"
ms.assetid: af1c5b0c-dbf9-4274-b06a-c6c2cdcf2a52
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C3014
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

se esperaba un bucle for después de la directiva 'directive' de OpenMP  
  
 Es un error para cualquier cosa que no sea un bucle `for` seguir inmediatamente a una directiva `#pragma omp for`.  
  
 El ejemplo siguiente genera la advertencia C3014:  
  
```  
// C3014.cpp // compile with: /openmp int main() { int i = 0; #pragma omp parallel { #pragma omp for for (i = 0; i < 10; ++i)   // OK { } } #pragma omp parallel for for (i = 0; i < 10; ++i)   // OK { } #pragma omp parallel { #pragma omp for {   // C3014 for (i = 0; i < 10; ++i) { } } } #pragma omp parallel for {   // C3014 for (i = 0; i < 10; ++i) { } } #pragma omp parallel { #pragma omp for i *= 2;   // C3014 for (i = 0; i < 10; ++i) { } } #pragma omp parallel for i *= 2;   // C3014 for (i = 0; i < 10; ++i) { } }  
```