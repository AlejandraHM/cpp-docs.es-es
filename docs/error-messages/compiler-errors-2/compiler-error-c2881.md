---
title: "Error del compilador C2881 | Microsoft Docs"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2881"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2881"
ms.assetid: b49c63c2-b064-4d4b-a75e-ddd2af947522
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C2881
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'espacioDeNombres1' : ya se utiliza como alias para 'espacioDeNombres2'  
  
 No se puede usar el mismo nombre como alias para dos espacios de nombres.  
  
 El código siguiente genera el error C2881:  
  
```  
// C2881.cpp  
// compile with: /c  
namespace A {  
   int k;  
}  
  
namespace B {  
   int i;  
}  
  
namespace C = A;  
namespace C = B;   // C2881 C is already an alias for A  
```