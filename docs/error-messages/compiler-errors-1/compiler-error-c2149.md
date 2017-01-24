---
title: "Error del compilador C2149 | Microsoft Docs"
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
  - "C2149"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2149"
ms.assetid: 7a106dab-d79f-41b9-85be-f36e86e4d2ab
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C2149
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifier': el ancho del campo de bits con nombre no puede ser igual a cero  
  
 Los campos de bits solo pueden tener un ancho de cero si no tienen nombre.  
  
 El ejemplo siguiente genera la advertencia C2149:  
  
```  
// C2149.cpp // compile with: /c struct C { int i : 0;   // C2149 int j : 2;   // OK };  
```