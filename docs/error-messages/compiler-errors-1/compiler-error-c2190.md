---
title: "Error del compilador C2190 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2190"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2190"
ms.assetid: 34e15f85-d979-4948-80fc-46c414508a70
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Error del compilador C2190
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

la primera lista de parámetros es más larga que la segunda  
  
 Se ha declarado a una función de C por segunda vez con una lista de parámetros más corta.  C no admite funciones sobrecargadas.  
  
 El código siguiente genera el error C2190:  
  
```  
// C2190.c  
// compile with: /Za /c  
void func( int, float );  
void func( int  );   // C2190, different parameter list  
void func2( int  );   // OK  
```