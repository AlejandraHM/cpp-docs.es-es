---
title: "&#39;New&#39; no se puede usar en una interfaz | Microsoft Docs"
ms.custom: ""
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30375"
  - "bc30375"
helpviewer_keywords: 
  - "BC30375"
ms.assetid: c1e06108-1b52-4cbe-8cae-e816a0dbac0b
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;New&#39; no se puede usar en una interfaz
Una [Dim \(Instrucción\)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md) usa una cláusula [New \(Operador\)](../Topic/New%20Operator%20\(Visual%20Basic\).md) al declarar una variable para que sea un tipo de interfaz.  
  
 Aunque una interfaz sea un tipo de referencia, no se puede crear una instancia de esta. Puede usar `New` solo para crear una instancia de una clase o una estructura.  
  
 **Identificador de error:** BC30375  
  
### Para corregir este error  
  
1.  Si la variable va a ser un tipo de interfaz, quite la palabra clave `New`.  
  
2.  Si la variable va a hacer referencia a una instancia, declárela para que sea de un tipo de clase o estructura. Conserve la palabra clave `New` para crear una instancia.  
  
## Vea también  
 [Interface \(Instrucción\)](../Topic/Interface%20Statement%20\(Visual%20Basic\).md)   
 [Class \(Instrucción\)](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Structure \(Instrucción\)](../Topic/Structure%20Statement.md)