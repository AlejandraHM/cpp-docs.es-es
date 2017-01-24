---
title: "El miembro &#39;&lt;nombreDeMiembro&gt;&#39; est&#225; en conflicto con el miembro &#39;&lt;nombreDeMiembro&gt;&#39; en el tipo base &#39;&lt;nombreDeTipoBase&gt;&#39; y, por lo tanto, no se debe declarar como &#39;Overloads&#39; | Microsoft Docs"
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
  - "bc40021"
  - "vbc40021"
helpviewer_keywords: 
  - "BC40021"
ms.assetid: 2ec72726-ab0e-4545-9c1e-2409eb54482e
caps.latest.revision: 10
caps.handback.revision: 10
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# El miembro &#39;&lt;nombreDeMiembro&gt;&#39; est&#225; en conflicto con el miembro &#39;&lt;nombreDeMiembro&gt;&#39; en el tipo base &#39;&lt;nombreDeTipoBase&gt;&#39; y, por lo tanto, no se debe declarar como &#39;Overloads&#39;
Una propiedad o un procedimiento usa la palabra clave [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md) para volver a declarar una propiedad o un procedimiento existente con el mismo nombre, pero la propiedad o el procedimiento existente se encuentra en la clase base.  
  
 La sobrecarga se usa para definir varias versiones de una propiedad o un procedimiento en la misma clase. No se puede definir una versión adicional de un miembro de clase base a menos que ese miembro de clase base ya especifique [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md).  
  
 De forma predeterminada, este mensaje es una advertencia. Para obtener más información sobre cómo ocultar las advertencias o cómo tratarlas como errores, vea [Configurar advertencias en Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Identificador de error:** BC40021  
  
### Para corregir este error  
  
-   Si quiere definir una versión adicional del miembro de clase base y tiene acceso al código fuente de la clase base, agregue la palabra clave [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md) a la definición de clase base.  
  
-   Si no tiene acceso al código fuente de la clase base, no se puede sobrecargar el miembro en una clase derivada. Quite la palabra clave `Overloads`.  
  
-   Si quiere reemplazar el miembro de clase base en lugar de definir una versión adicional del mismo, use la palabra clave [Overrides](../Topic/Overrides%20\(Visual%20Basic\).md) en lugar de `Overloads`.  
  
-   Si quiere ocultar el miembro de clase base con un nuevo miembro en la clase derivada, use la palabra clave [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md) en lugar de `Overloads`.  
  
## Vea también  
 [Sobrecarga de procedimientos](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Fundamentos de la herencia](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)