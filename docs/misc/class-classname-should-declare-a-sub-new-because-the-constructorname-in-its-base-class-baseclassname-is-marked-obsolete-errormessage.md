---
title: "La clase &#39;&lt;nombreClase&gt;&#39; debe declarar un &#39;Sub New&#39; porque &#39;&lt;constructorname&gt;&#39; de su clase base &#39;&lt;baseclassname&gt;&#39; est&#225; marcado como obsoleto: &#39;&lt;errormessage&gt;&#39; | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc41002"
  - "bc41002"
helpviewer_keywords: 
  - "BC41002"
ms.assetid: 6d034bbe-ab6a-433a-ae31-8c4a42faf7f8
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# La clase &#39;&lt;nombreClase&gt;&#39; debe declarar un &#39;Sub New&#39; porque &#39;&lt;constructorname&gt;&#39; de su clase base &#39;&lt;baseclassname&gt;&#39; est&#225; marcado como obsoleto: &#39;&lt;errormessage&gt;&#39;
Una declaración de clase no incluye un constructor y el constructor de clase base se marca con el atributo <xref:System.ObsoleteAttribute> y la directiva para tratarlo como advertencia.  
  
 Cuando una clase derivada no declara un constructor, [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] intenta generar un constructor sin parámetros implícito que llama a `MyBase.New()`. Si no hay ningún constructor accesible en la clase base que se pueda llamar sin argumentos, [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] no puede generar un constructor implícito. En este caso, el constructor necesario se marca con el atributo <xref:System.ObsoleteAttribute>, por lo que [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] no puede llamarlo.  
  
 Puede marcar que un elemento de programación ya no está en uso aplicándole <xref:System.ObsoleteAttribute>. Si lo hace, puede establecer la propiedad <xref:System.ObsoleteAttribute.IsError%2A> del atributo en `True` o `False`. Si se establece en `True`, el compilador trata un intento de usar el elemento como un error. Si se establece en `False` o se deja el valor predeterminado `False`, el compilador emite una advertencia si hay un intento de usar el elemento.  
  
 De forma predeterminada, este mensaje es una advertencia, ya que la propiedad <xref:System.ObsoleteAttribute.IsError%2A> de <xref:System.ObsoleteAttribute> es `False`. Para obtener información sobre cómo ocultar las advertencias o cómo tratarlas como errores, vea [Configurar advertencias en Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Identificador de error:** BC41002  
  
### Para corregir este error  
  
1.  Examine el mensaje de error indicado y tome las medidas adecuadas.  
  
2.  Use `Sub New` para declarar un constructor en la clase derivada.  
  
## Vea también  
 [NO ESTÁ EN LA COMPILACIÓN: Atributos usados en Visual Basic](http://msdn.microsoft.com/es-es/22231318-8a40-49af-9245-e0aab723563b)   
 [NO ESTÁ EN LA COMPILACIÓN: Aplicación de atributos](http://msdn.microsoft.com/es-es/2b1703ed-4437-49b3-bc0b-568094324f47)