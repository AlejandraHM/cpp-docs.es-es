---
title: "Advertencia del compilador (nivel 4) C4400 | Microsoft Docs"
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
  - "C4400"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4400"
ms.assetid: f135fe98-4f92-4e07-9d71-2621b36ee755
caps.latest.revision: 4
caps.handback.revision: 4
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# Advertencia del compilador (nivel 4) C4400
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'tipo' : no se admiten los calificadores const\/volatile en este tipo  
  
 Los calificadores [const](../../cpp/const-cpp.md) y [volatile](../../cpp/volatile-cpp.md) no funcionarán con variables de tipos de Common Language Runtime.  
  
## Ejemplo  
 El ejemplo siguiente genera el error C4400.  
  
```  
// C4400.cpp  
// compile with: /clr /W4  
// C4401 expected  
using namespace System;  
#pragma warning (disable : 4101)  
int main() {  
   const String^ str;   // C4400  
   volatile String^ str2;   // C4400  
}  
```