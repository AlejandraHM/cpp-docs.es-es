---
title: "La restricci&#243;n &#39;Structure&#39; no se puede combinar con una restricci&#243;n de tipo de clase espec&#237;fica. | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc32108"
  - "bc32108"
helpviewer_keywords: 
  - "BC32108"
ms.assetid: de461824-5aec-48d1-967d-b0e0609a8ba6
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# La restricci&#243;n &#39;Structure&#39; no se puede combinar con una restricci&#243;n de tipo de clase espec&#237;fica.
Una lista de restricciones incluye la restricción [Structure \(Visual Basic\)](http://msdn.microsoft.com/es-es/263ce115-ac36-4c05-8cb7-0e0eead5c6d0) y el nombre de una clase definida.  
  
 Una lista de restricciones impone requisitos al argumento de tipo pasado al parámetro de tipo. Puede especificar los requisitos siguientes en cualquier combinación:  
  
-   El argumento de tipo debe implementar una o varias interfaces  
  
-   El argumento de tipo debe heredar de al menos una clase.  
  
-   El argumento de tipo debe exponer un constructor sin parámetros al que el código de creación pueda tener acceso \(incluya la restricción `New`\).  
  
 Si no incluye ninguna clase o interfaz específica en la lista de restricciones, puede imponer un requisito más general especificando uno de los elementos siguientes:  
  
-   El argumento de tipo debe ser un tipo de valor \(incluya la restricción `Structure`\).  
  
-   El argumento de tipo debe ser un tipo de referencia \(incluya la restricción `Class`\).  
  
 No es posible especificar `Structure` y `Class` para el mismo parámetro de tipo y no se pueden especificar estas restricciones más de una vez.  
  
 **Identificador de error:** BC32108  
  
### Para corregir este error  
  
-   Si quiere que el argumento de tipo sea un tipo de valor, quite el nombre de clase de la lista de restricciones.  
  
-   Si quiere que el argumento de tipo herede del nombre de clase especificado, quite la palabra clave `Structure` de la lista de restricciones.  
  
## Vea también  
 [Tipos genéricos en Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Tipos de valor y tipos de referencia](../Topic/Value%20Types%20and%20Reference%20Types.md)