---
title: "GOTO (MASM) | Microsoft Docs"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "goto"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GOTO directive"
ms.assetid: 6a5f73e7-6784-4eae-ac52-4fc77a7f369f
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# GOTO (MASM)
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Transfiere el ensamblado*al macrolabel*marcado línea de **:**.  
  
## Sintaxis  
  
```  
  
GOTO   
macrolabel  
  
```  
  
## Comentarios  
 **IR A** sólo se permite en los bloques de [MACRO](../../assembler/masm/macro.md), de [PARA](../../assembler/masm/for-masm.md), de [FORC](../../assembler/masm/forc.md), de [REPETICIÓN](../../assembler/masm/repeat.md), y de **WHILE** .  La etiqueta debe ser la única directiva de línea y debe incluir un signo de dos puntos principal.  
  
## Vea también  
 [Directives Reference](../../assembler/masm/directives-reference.md)