---
title: "__emul, __emulu | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "__emulu_cpp"
  - "__emul"
  - "__emul_cpp"
  - "__emulu"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "__emul (función intrínseca)"
  - "__emulu (función intrínseca)"
ms.assetid: 79545236-cca2-40b8-a4e1-8abce9b26311
caps.latest.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 10
---
# __emul, __emulu
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

**Específicos de Microsoft**  
  
 Realiza las multiplicaciones que desbordan lo que puede contener un entero de 32 bits.  
  
## Sintaxis  
  
```  
__int64 __emul(  
   int a,  
   int b  
);  
unsigned __int64 __emulu(  
   unsigned int a,  
   unsigned int b  
);  
```  
  
#### Parámetros  
 \[in\] `a`  
 El primer operando entero de multiplicación.  
  
 \[in\] `b`  
 El segundo operando entero de multiplicación.  
  
## Valor devuelto  
 El resultado de multiplicación.  
  
## Requisitos  
  
|Intrínseco|Arquitectura|  
|----------------|------------------|  
|`__emul`|x86, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
|`__emulu`|x86, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
  
 **Archivo de encabezado** \<intrin.h\>  
  
## Comentarios  
 `__emul` utiliza dos valores con signo de 32 bits y devuelve el resultado de multiplicación como valor entero con signo de 64 bits.  
  
 `__emulu` utiliza dos valores de entero sin signo de 32 bits y devuelve el resultado de multiplicación como valor de entero sin signo de 64 bits.  
  
## Ejemplo  
  
```  
// emul.cpp  
// compile with: /EHsc  
// processor: x86, x64  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
#pragma intrinsic(__emul)  
#pragma intrinsic(__emulu)  
  
int main()  
{  
   int a = -268435456;   
   int b = 2;   
  
   __int64 result = __emul(a, b);  
  
   cout << a << " * " << b << " = " << result << endl;  
  
   unsigned int ua = 0xFFFFFFFF; // Dec value: 4294967295  
   unsigned int ub = 0xF000000;  // Dec value: 251658240  
  
   unsigned __int64 uresult = __emulu(ua, ub);  
  
   cout << ua << " * " << ub << " = " << uresult << endl;  
  
}  
```  
  
## Output  
  
```  
-268435456 * 2 = -536870912  
4294967295 * 251658240 = 1080863910317260800  
```  
  
### Específico de Microsoft de FINAL  
  
## Vea también  
 [Intrínsecos del controlador](../intrinsics/compiler-intrinsics.md)