---
title: Error del compilador C2944 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2944
dev_langs:
- C++
helpviewer_keywords:
- C2944
ms.assetid: f209e668-e72f-442a-a438-8c4ff43a404a
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 4c23665d165bf425362b1b85135c53c667d8278c
ms.contentlocale: es-es
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2944"></a>Error del compilador C2944
'class': el identificador de clase de tipo se redefinió como argumento de valor de una plantilla  
  
 No puede usar una clase genérica o de plantilla, en lugar de un símbolo, como argumento de tipo de plantilla.  
  
 El ejemplo siguiente genera la advertencia C2944:  
  
```  
// C2944.cpp  
// compile with: /c  
template<class T>  
class TC { };   
  
template <int TC<int> > struct X1 { };   // C2944  
  
template <class T > struct X2 {};  
```  
  
 También se puede producir el error C2944 al usar genéricos:  
  
```  
// C2944b.cpp  
// compile with: /clr /c  
generic<class T>  
ref class GC {};  
  
template <int GC<int> > struct X2 { };   // C2944  
template <class T> struct X3 {};   // OK  
```
