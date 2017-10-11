---
title: Error del compilador C3076 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3076
dev_langs:
- C++
helpviewer_keywords:
- C3076
ms.assetid: 8a87b3e4-2c17-4b87-9622-ef0962d6a34e
caps.latest.revision: 5
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: eb4668f69ca7d8680620c85b7a37b70c2c58c96b
ms.contentlocale: es-es
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3076"></a>Error del compilador C3076
'instancia': no se puede incrustar una instancia de un tipo de referencia, 'type', en un tipo nativo  
  
 Un tipo nativo no puede contener una instancia de un tipo CLR.  
  
 Para obtener más información, consulte [semántica de pila de C++ para los tipos de referencia](../../dotnet/cpp-stack-semantics-for-reference-types.md).  
  
## <a name="example"></a>Ejemplo  
 El ejemplo siguiente genera C3076.  
  
```  
// C3076.cpp  
// compile with: /clr /c  
ref struct U {};  
  
struct V {  
   U y;   // C3076  
};  
  
ref struct W {  
   U y;   // OK  
};  
```
