---
title: "El argumento de tipo &#39;&lt;typeargumentname&gt;&#39; no satisface la restricci&#243;n &#39;Structure&#39; para el par&#225;metro de tipo &#39;&lt;typeparametername&gt;&#39; | Microsoft Docs"
ms.custom: ""
ms.date: "12/08/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc32105"
  - "bc32105"
helpviewer_keywords: 
  - "BC32105"
ms.assetid: 09e5a837-8afd-4360-86bd-157e53c47513
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# El argumento de tipo &#39;&lt;typeargumentname&gt;&#39; no satisface la restricci&#243;n &#39;Structure&#39; para el par&#225;metro de tipo &#39;&lt;typeparametername&gt;&#39;
Un argumento de tipo proporcionado a un tipo genérico no satisface la restricción de tipo de valor en su parámetro de tipo correspondiente.  
  
 Una lista de restricciones impone requisitos al argumento de tipo pasado al parámetro de tipo. Si no incluye ninguna clase o interfaz específica en la lista de restricciones, puede imponer un requisito general especificando uno de los elementos siguientes:  
  
-   El argumento de tipo debe ser un tipo de valor \(incluya la restricción [Structure \(Visual Basic\)](http://msdn.microsoft.com/es-es/263ce115-ac36-4c05-8cb7-0e0eead5c6d0)\)  
  
-   El argumento de tipo debe ser un tipo de referencia \(incluya la restricción [Class \(Visual Basic\)](http://msdn.microsoft.com/es-es/0777c6e6-46bc-451b-ad70-57b49d4ef4f7)\)  
  
 No es posible especificar `Structure` y `Class` para el mismo parámetro de tipo y no se pueden especificar estas restricciones más de una vez.  
  
 **Identificador de error:** BC32105  
  
### Para corregir este error  
  
-   Seleccione un argumento de tipo de cualquier tipo de valor.  
  
## Vea también  
 [Tipos genéricos en Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Tipos de valor y tipos de referencia](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Cómo: Utilizar una clase genérica](../Topic/How%20to:%20Use%20a%20Generic%20Class%20\(Visual%20Basic\).md)