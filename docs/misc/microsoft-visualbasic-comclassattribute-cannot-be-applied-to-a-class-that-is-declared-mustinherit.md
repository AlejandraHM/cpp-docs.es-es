---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; no se puede aplicar a una clase declarada como &#39;MustInherit&#39; | Microsoft Docs"
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
  - "BC32508"
  - "vbc32508"
helpviewer_keywords: 
  - "BC32508"
ms.assetid: c8af606d-f448-4703-98df-e594fd511f92
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; no se puede aplicar a una clase declarada como &#39;MustInherit&#39;
Una clase se declara con <xref:Microsoft.VisualBasic.ComClassAttribute>, pero su declaración especifica `MustInherit`.  
  
 Para poder elegirse como interoperabilidad COM, una clase de .NET Framework debe cumplir los requisitos siguientes:  
  
-   Debe ser `Public`, todos sus contenedores deben ser `Public` y debe exponer al menos un miembro `Public`.  
  
-   No debe ser *abstract*, es decir, no debe declararse con `MustInherit`.  
  
-   No debe ser genérica ni declararse dentro de un tipo de contenedor genérico.  
  
 **Id. de error:** BC32508  
  
### Para corregir este error  
  
-   Quite la palabra clave `MustInherit` de la declaración de clase.  
  
     O bien  
  
-   Si la clase o su elemento contenedor deben ser genéricos, elimine <xref:Microsoft.VisualBasic.ComClassAttribute> de la declaración de clase. No se puede exponer en COM.  
  
## Vea también  
 <xref:Microsoft.VisualBasic.ComClassAttribute>   
 [Interoperabilidad COM](../Topic/COM%20Interop%20\(Visual%20Basic\).md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)