---
title: "Option Strict On no permite restricciones del tipo &#39;&lt;nombreTipo1&#39; para el tipo &#39;nombreTipo2&#39; al copiar del par&#225;metro ByRef &#39;&lt;nombrePar&#225;metro&gt;&#39; en el argumento correspondiente. | Microsoft Docs"
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
  - "bc32029"
  - "vbc32029"
helpviewer_keywords: 
  - "BC32029"
ms.assetid: fc9ae5d2-b506-47cf-a50c-116fda5ed206
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Option Strict On no permite restricciones del tipo &#39;&lt;nombreTipo1&#39; para el tipo &#39;nombreTipo2&#39; al copiar del par&#225;metro ByRef &#39;&lt;nombrePar&#225;metro&gt;&#39; en el argumento correspondiente.
Una llamada a procedimiento proporciona un argumento `ByRef` con un tipo de datos que se amplía hasta el tipo declarado del argumento, y `Option Strict` es `On`. La conversión de ampliación está permitida cuando el argumento se pasa al procedimiento, pero cuando el procedimiento modifica el contenido del argumento variable en el código de llamada, la conversión inversa es de restricción. No se permiten las conversiones de restricción con `Option Strict On`.  
  
 **Identificador de error:** BC32029  
  
### Para corregir este error  
  
-   Proporcione cada argumento `ByRef` en la llamada a procedimiento con el mismo tipo de datos que el tipo declarado o active `Option Strict Off`.  
  
## Vea también  
 [Option Strict \(Instrucción\)](../Topic/Option%20Strict%20Statement.md)   
 [Pasar argumentos por valor y por referencia](../Topic/Passing%20Arguments%20by%20Value%20and%20by%20Reference%20\(Visual%20Basic\).md)   
 [Conversiones de ampliación y de restricción](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Conversiones implícitas y explícitas](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)