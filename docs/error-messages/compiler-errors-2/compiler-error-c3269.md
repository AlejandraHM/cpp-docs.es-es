---
title: Error del compilador C3269 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3269
dev_langs:
- C++
helpviewer_keywords:
- C3269
ms.assetid: c575f067-244d-4dd5-bf58-9e7630ea58b7
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: f1eb014e107326aa8c85b2439444c63525f26a77
ms.contentlocale: es-es
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3269"></a>Error del compilador C3269
'función': una función miembro de tipo administrado o WinRTtype no se puede declarar con '...'  
  
Las funciones de miembro de clase administradas y WinRT no pueden declarar listas de parámetros de longitud variable.  
  
El ejemplo siguiente genera el error C3269 y muestra cómo corregirlo:  
  
```  
// C3269_2.cpp  
// compile with: /clr  
  
ref struct A  
{  
   void func(int i, ...)   // C3269  
   // try the following line instead  
   // void func(int i )  
   {  
   }  
};  
  
int main()  
{  
}  
```  

