---
title: 'Cómo: sobrecargar funciones con punteros internos y punteros nativos (C++ / c++ / CLI) | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- Functions with interior and native pointers, overloading
ms.assetid: d70df625-4aad-457c-84f5-70a0a290cc1f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 0aeacce18f7a12ece21c7ee2136a1f1be267a47f
ms.sourcegitcommit: 38af5a1bf35249f0a51e3aafc6e4077859c8f0d9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/09/2018
ms.locfileid: "40015841"
---
# <a name="how-to-overload-functions-with-interior-pointers-and-native-pointers-ccli"></a>Cómo: Sobrecargar funciones con punteros internos y punteros nativos (C++/CLI)
Las funciones se pueden sobrecargar dependiendo de si el tipo de parámetro es un puntero interior o puntero nativo.  
  
> [!IMPORTANT]
>  Esta característica del lenguaje es compatible con la `/clr` opción del compilador, pero no mediante el `/ZW` opción del compilador.  
  
## <a name="example"></a>Ejemplo  
  
### <a name="code"></a>Código  
  
```cpp  
// interior_ptr_overload.cpp  
// compile with: /clr  
using namespace System;  
  
// C++ class  
struct S {  
   int i;  
};  
  
// managed class  
ref struct G {  
   int i;  
};  
  
// can update unmanaged storage  
void f( int* pi ) {  
   *pi = 10;  
   Console::WriteLine("in f( int* pi )");  
}  
  
// can update managed storage  
void f( interior_ptr<int> pi ) {  
   *pi = 10;   
   Console::WriteLine("in f( interior_ptr<int> pi )");  
}  
  
int main() {  
   S *pS = new S;   // C++ heap  
   G ^pG = gcnew G;   // common language runtime heap  
   f( &pS->i );  
   f( &pG->i );  
};  
```  
  
```Output 
in f( int* pi )  
in f( interior_ptr<int> pi )  
```  
  
## <a name="see-also"></a>Vea también  
 [interior_ptr (C++/CLI)](../windows/interior-ptr-cpp-cli.md)