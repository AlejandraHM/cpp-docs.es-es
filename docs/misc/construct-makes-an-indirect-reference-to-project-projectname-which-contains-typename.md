---
title: "La construcci&#243;n hace una referencia indirecta al proyecto &#39;&lt;nombreProyecto&gt;&#39;, que contiene &#39;&lt;nombreTipo&gt;&#39;. | Microsoft Docs"
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
  - "vbc31533"
  - "bc31533"
helpviewer_keywords: 
  - "BC31533"
ms.assetid: e3f55f9f-92be-4ecb-bc8f-9e57049a0805
caps.latest.revision: 6
caps.handback.revision: 6
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# La construcci&#243;n hace una referencia indirecta al proyecto &#39;&lt;nombreProyecto&gt;&#39;, que contiene &#39;&lt;nombreTipo&gt;&#39;.
La construcción hace una referencia indirecta al proyecto '\<nombreProyecto\>', que contiene '\<nombreTipo\>'. Agregue una referencia de proyecto a '\<nombreProyecto\>' a su proyecto.  
  
 Una expresión o instrucción obtiene acceso a un tipo definido en otro proyecto, pero el proyecto no tiene una referencia directa al proyecto que lo define.  
  
 El tipo puede ser una clase, estructura, interfaz, módulo o enumeración.  
  
 El proyecto que define el tipo mencionado genera un ensamblado que contiene el tipo. Si el proyecto no hace referencia directamente al proyecto que lo define, el compilador no puede garantizar que el ensamblado que contiene el tipo esté en la solución y disponible para el acceso.  
  
 **Identificador de error:** BC31533  
  
### Para corregir este error  
  
-   Determine qué proyecto define el tipo citado y agregue una referencia de proyecto a él.  
  
## Vea también  
 [NIB: Hacer referencia a espacios de nombres y componentes](http://msdn.microsoft.com/es-es/568fa759-796b-44cd-bf5e-1cf8de6e38fd)   
 [Administrar referencias en un proyecto](../Topic/Managing%20references%20in%20a%20project.md)   
 [NIB: Administrar referencias](http://msdn.microsoft.com/es-es/910912ce-0dc9-4569-9274-32c44a20cb2c)   
 [NIB: Cómo: Agregar o quitar referencias usando el cuadro de diálogo Agregar referencia](http://msdn.microsoft.com/es-es/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)