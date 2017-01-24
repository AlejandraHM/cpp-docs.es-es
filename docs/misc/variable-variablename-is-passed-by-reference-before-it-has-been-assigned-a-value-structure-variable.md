---
title: "La referencia pasa una variable &#39;&lt;nombreVariable&gt;&#39; antes de que se le haya asignado un valor (variable de estructura). | Microsoft Docs"
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
  - "bc42108"
  - "vbc42108"
helpviewer_keywords: 
  - "BC42108"
ms.assetid: 8f858dd7-db04-408e-ae67-e4ff2f0e5e30
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# La referencia pasa una variable &#39;&lt;nombreVariable&gt;&#39; antes de que se le haya asignado un valor (variable de estructura).
La referencia pasa una variable '\<nombreVariable\>' antes de que se le haya asignado un valor. Podría producirse una excepción de referencia nula en tiempo de ejecución. Asegúrese de que la estructura o todos los miembros de referencia se inicializan antes de usarlos.  
  
 Una llamada a procedimiento pasa una variable de estructura como argumento para un parámetro `ByRef` antes de asignar cualquier valor a la variable.  
  
 Si nunca se ha asignado un valor a una variable de estructura, cada miembro de la estructura contiene el valor predeterminado para su tipo de datos. Para un tipo de datos de referencia, el valor predeterminado es [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md). Leer un miembro de referencia que tiene un valor de `Nothing` puede producir una excepción <xref:System.NullReferenceException> en algunas circunstancias.  
  
 Cuando se pasa un argumento a un procedimiento `ByRef`, se expone a la variable subyacente del argumento a una posible modificación por parte del procedimiento.  
  
 De forma predeterminada, este mensaje es una advertencia. Para más información sobre cómo ocultar las advertencias o cómo tratarlas como errores, vea [Configurar advertencias en Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Identificador de error:** BC42108  
  
### Para corregir este error  
  
-   Si quiere que el procedimiento asigne valores a los miembros de estructura mediante el argumento `ByRef`, y si no importa si los miembros ya contienen valores, no es necesario realizar ninguna acción.  
  
-   Si la lógica del procedimiento lee un miembro de estructura antes de asignarle algún valor, y si el miembro es de un tipo de valor, asegúrese de que la lógica del procedimiento no depende de si el miembro contiene o no su valor predeterminado.  
  
-   Si la lógica del procedimiento lee un miembro de estructura antes de asignarle algún valor, y si el miembro es de un tipo de referencia, asegúrese de que la lógica del procedimiento puede controlar un valor de `Nothing`. Por ejemplo, podría usar una [Try...Catch...Finally \(Instrucción\)](../Topic/Try...Catch...Finally%20Statement%20\(Visual%20Basic\).md) para detectar una excepción <xref:System.NullReferenceException>.  
  
## Vea también  
 [Dim \(Instrucción\)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [Tipos de valor y tipos de referencia](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Pasar argumentos por valor y por referencia](../Topic/Passing%20Arguments%20by%20Value%20and%20by%20Reference%20\(Visual%20Basic\).md)   
 [ByRef](../Topic/ByRef%20\(Visual%20Basic\).md)   
 [Declaración de variable](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)   
 [Estructuras](../Topic/Structures%20\(Visual%20Basic\).md)   
 [Structure \(Instrucción\)](../Topic/Structure%20Statement.md)   
 [Solucionar problemas de variables](../Topic/Troubleshooting%20Variables%20in%20Visual%20Basic.md)