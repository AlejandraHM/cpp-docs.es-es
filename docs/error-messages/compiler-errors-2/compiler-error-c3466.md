---
title: Error del compilador C3466 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3466
dev_langs:
- C++
helpviewer_keywords:
- C3466
ms.assetid: 69a877d9-a749-474b-bfc3-8d3fd53ba8fd
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: b4610f7a47784dfa93339e06f09f6a576b02455d
ms.contentlocale: es-es
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3466"></a>Error del compilador C3466
'type': no se puede reenviar una especialización de una clase genérica  
  
 No se puede usar en una especialización de una clase genérica de reenvío de tipos.  
  
 Para obtener más información, consulte [Type Forwarding (C++ / CLI)](../../windows/type-forwarding-cpp-cli.md).  
  
## <a name="example"></a>Ejemplo  
 En el ejemplo siguiente se crea un componente.  
  
```  
// C3466.cpp  
// compile with: /clr /LD  
generic<typename T>  
public ref class GR {};  
  
public ref class GR2 {};  
```  
  
## <a name="example"></a>Ejemplo  
 El ejemplo siguiente genera la advertencia C3466.  
  
```  
// C3466_b.cpp  
// compile with: /clr /c  
#using "C3466.dll"  
[assembly:TypeForwardedTo(GR<int>::typeid)];   // C3466  
[assembly:TypeForwardedTo(GR2::typeid)];   // OK  
```
