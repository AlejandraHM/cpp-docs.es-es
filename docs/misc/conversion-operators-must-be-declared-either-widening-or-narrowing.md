---
title: "Los operadores de conversi&#243;n se deben declarar como &#39;Widening&#39; o &#39;Narrowing&#39; | Microsoft Docs"
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
  - "vbc33017"
  - "bc33017"
helpviewer_keywords: 
  - "BC33017"
ms.assetid: 5972d955-ce1d-4348-a021-167eecb3a507
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Los operadores de conversi&#243;n se deben declarar como &#39;Widening&#39; o &#39;Narrowing&#39;
Una [Operator \(Instrucción\)](../Topic/Operator%20Statement.md) no especifica [Widening](../Topic/Widening%20\(Visual%20Basic\).md) ni [Narrowing](../Topic/Narrowing%20\(Visual%20Basic\).md).  
  
 Al definir un operador de conversión, debe declararlo como `Widening` o `Narrowing`. Se trata de características mutuamente excluyentes, por lo que no puede especificar ambas.  
  
 **Identificador de error:** BC33017  
  
### Para corregir este error  
  
-   Decida si el operador de conversión debe ser `Widening` o `Narrowing` e incluya la palabra clave adecuada en la instrucción `Operator`. Debe especificar uno u otro.  
  
## Vea también  
 [Conversiones de ampliación y de restricción](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Procedimientos de operador](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator \(Instrucción\)](../Topic/Operator%20Statement.md)   
 [Cómo: Definir un operador](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [Cómo: Definir un operador de conversión](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)