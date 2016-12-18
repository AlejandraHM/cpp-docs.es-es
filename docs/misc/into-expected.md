---
title: "Se esperaba &#39;Into&#39;. | Microsoft Docs"
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
  - "bc36615"
  - "vbc36615"
helpviewer_keywords: 
  - "BC36615"
ms.assetid: 24062dd9-a973-43b6-88d3-c11adc5a3736
caps.latest.revision: 5
caps.handback.revision: 5
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Se esperaba &#39;Into&#39;.
Se ha especificado una cláusula `Aggregate`, `Group By` o `Group Join` sin un operador `Into`. El operador `Into` se usa para identificar las funciones de agregado que se van a aplicar a los resultados de la consulta y para identificar el miembro del tipo de resultados de la consulta que va a contener los resultados agrupados \(usando la función de agregado `Group`\).  
  
 **Identificador de error:** BC36615  
  
### Para corregir este error  
  
1.  Agregue el operador `Into` a la cláusula `Aggregate`, `Group By` o `Group Join`. A continuación se muestra un ejemplo:  
  
    ```vb#  
    Dim orders = From order In orderList _ Order By order.OrderDate _ Group By OrderDate = order.OrderDate _ Into OrdersByDate = Group  
    ```  
  
## Vea también  
 [Aggregate \(Cláusula\)](../Topic/Aggregate%20Clause%20\(Visual%20Basic\).md)   
 [Group By \(Cláusula\)](../Topic/Group%20By%20Clause%20\(Visual%20Basic\).md)   
 [Group Join \(Cláusula\)](../Topic/Group%20Join%20Clause%20\(Visual%20Basic\).md)   
 [Introducción a LINQ en Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ](../Topic/LINQ%20in%20Visual%20Basic.md)