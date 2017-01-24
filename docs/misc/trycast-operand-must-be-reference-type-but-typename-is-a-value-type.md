---
title: "El operando &#39;TryCast&#39; debe ser el tipo de referencia, pero &#39;&lt;typename&gt;&#39; es un tipo de valor | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BC30792"
  - "vbc30792"
helpviewer_keywords: 
  - "BC30792"
ms.assetid: 3325fce5-dbc0-4d1d-9530-31f4720bfe6e
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# El operando &#39;TryCast&#39; debe ser el tipo de referencia, pero &#39;&lt;typename&gt;&#39; es un tipo de valor
El operador `TryCast` se usa con un tipo de valor para al menos uno de los argumentos.  
  
 `TryCast` comprueba si existe una relación de herencia o implementación entre los dos argumentos. Por lo tanto, solo permite tipos de referencia para los argumentos. Para obtener más información, consulta [Tipos de valor y tipos de referencia](../Topic/Value%20Types%20and%20Reference%20Types.md).  
  
 **Id. de error:** BC30792  
  
### Para corregir este error  
  
-   Use `DirectCast` o `CType` para realizar la conversión. Ambos permiten tipos de valor.  
  
## Vea también  
 [TryCast \(Operador\)](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md)   
 [DirectCast \(Operador\)](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md)   
 [CType \(Función\)](../Topic/CType%20Function%20\(Visual%20Basic\).md)   
 [Tipos de valor y tipos de referencia](../Topic/Value%20Types%20and%20Reference%20Types.md)