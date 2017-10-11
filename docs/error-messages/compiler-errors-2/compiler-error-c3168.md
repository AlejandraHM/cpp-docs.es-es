---
title: C3168 de Error del compilador | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3168
dev_langs:
- C++
helpviewer_keywords:
- C3168
ms.assetid: 4c36fcfb-c351-48ff-b4eb-78d2aa1b4d55
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 980341a7871d314e3173449234fbb597a5b55d63
ms.contentlocale: es-es
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3168"></a>C3168 de Error del compilador
'type': tipo de enumeración subyacente no válido  
  
El tipo subyacente especificado para el `enum` tipo no es válido. El tipo subyacente debe ser un tipo integral de C++ o un tipo CLR correspondiente.  
  
El ejemplo siguiente genera C3168:  
  
```  
// C3168.cpp  
// compile with: /clr /c  
ref class G{};  
  
enum class E : G { e };   // C3168  
enum class F { f };   // OK  
```  

