---
title: "Error del compilador C2054 | Microsoft Docs"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2054"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2054"
ms.assetid: 37f7c612-0d7d-4728-9e67-ac4160555f48
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Error del compilador C2054
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

se esperaba '\(' a continuación de 'identificador'  
  
 El identificador de función se utiliza en un contexto que requiere paréntesis.  
  
 Este error puede producirse por omitir un signo igual \(\=\) en una inicialización compleja.  
  
 El código siguiente genera el error C2054:  
  
```  
// C2054.c  
int array1[] { 1, 2, 3 };   // C2054, missing =  
```  
  
 Posible solución:  
  
```  
// C2054b.c  
int main() {  
   int array2[] = { 1, 2, 3 };  
}  
```