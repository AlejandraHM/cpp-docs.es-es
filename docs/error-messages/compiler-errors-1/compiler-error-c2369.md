---
title: "Error del compilador C2369 | Microsoft Docs"
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
  - "C2369"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2369"
ms.assetid: 2a3933f6-2313-40ff-800f-921b296fdbbf
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C2369
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'matriz': nueva definición; subíndices distintos  
  
 La matriz se declaró con un subíndice diferente.  
  
 El ejemplo siguiente genera la advertencia C2369:  
  
```  
// C2369.cpp // compile with: /c int a[10]; int a[20];   // C2369 int b[20];   // OK  
```