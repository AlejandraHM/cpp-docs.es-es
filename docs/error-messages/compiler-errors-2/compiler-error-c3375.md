---
title: Error del compilador C3375 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3375
dev_langs:
- C++
helpviewer_keywords:
- C3375
ms.assetid: f1df78c6-e6ca-48f3-8b29-4e1710002bf3
caps.latest.revision: 5
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: fdf91445a1a6594b8b708dfbf43ff8ad86993c51
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3375"></a>Error del compilador C3375
'function': función delegada ambigua  
  
 Una creación de instancias de delegado podría haber tenido lugar en una función miembro estática o, como un delegado sin enlazar, en una función de instancia, por lo que el compilador emitió este error.  
  
 Para obtener más información, consulte [delegate (extensiones de componentes de C++)](../../windows/delegate-cpp-component-extensions.md).  
  
## <a name="example"></a>Ejemplo  
 El ejemplo siguiente genera la advertencia C3375.  
  
```  
// C3375.cpp  
// compile with: /clr  
ref struct R {  
   static void f(R^) {}  
   void f() {}  
};  
  
delegate void Del(R^);  
  
int main() {  
   Del ^ a = gcnew Del(&R::f);   // C3375  
}  
```
