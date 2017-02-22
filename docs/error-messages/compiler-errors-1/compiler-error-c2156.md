---
title: "Error del compilador C2156 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2156"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2156"
ms.assetid: 136f9c67-2c27-4f61-b7e6-ccd202eca697
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Error del compilador C2156
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

pragma debe estar fuera de la función  
  
 Un pragma que debe especificarse a nivel global \(fuera de un cuerpo de función\) está dentro de una función.  
  
 El ejemplo siguiente genera la advertencia C2156:  
  
```  
// C2156.cpp #pragma optimize( "l", on )   // OK int main() { #pragma optimize( "l", on )   // C2156 }  
```