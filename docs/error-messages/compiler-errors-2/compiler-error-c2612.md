---
title: "Error del compilador C2612 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2612"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2612"
ms.assetid: 6faacfd6-4455-41a2-808e-0f6799f84d6d
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Error del compilador C2612
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'car' final no válido en la lista de inicializadores de base\/miembro  
  
 Aparece un carácter después de la última base o miembro de una lista de inicializadores.  
  
 El código siguiente genera el error C2612:  
  
```  
// C2612.cpp  
class A {  
public:  
   int i;  
   A( int ia ) : i( ia ) + {};   // C2612  
};  
```