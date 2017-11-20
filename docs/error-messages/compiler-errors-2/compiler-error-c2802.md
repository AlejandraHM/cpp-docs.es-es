---
title: Error del compilador C2802 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2802
dev_langs: C++
helpviewer_keywords: C2802
ms.assetid: 08b68c0e-9382-40ac-8949-39a7a2749e05
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: adc1b4178caebe9893727aaf8ff802d6f030e986
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2802"></a>Error del compilador C2802
miembro estático 'operator operador' no tiene parámetros formales  
  
 Un operador declarado por una `static` función miembro debe tener al menos un parámetro.  
  
 El ejemplo siguiente genera C2802:  
  
```  
// C2802.cpp  
// compile with: /clr /c  
ref class A {  
   static operator+ ();   // C2802  
   static operator+ (A^, A^);   // OK  
};  
```