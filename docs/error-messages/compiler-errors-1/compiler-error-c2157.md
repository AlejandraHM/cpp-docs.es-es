---
title: Error del compilador C2157 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2157
dev_langs:
- C++
helpviewer_keywords:
- C2157
ms.assetid: babbca24-16dc-4b69-be14-a675029249c1
caps.latest.revision: 8
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 152b55fb228d73b03df615fd336e40e984521432
ms.contentlocale: es-es
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2157"></a>Error del compilador C2157
'function': se debe declarar antes de usarse en la lista pragma  
  
 El nombre de función no se declara antes de que se hace referencia en la lista de funciones para una [alloc_text](../../preprocessor/alloc-text.md) pragma.  
  
 El ejemplo siguiente genera la advertencia C2157:  
  
```  
// C2157.cpp  
// compile with: /c  
#pragma alloc_text( "func", func)   // C2157  
  
// OK  
extern "C" void func();  
#pragma alloc_text( "func", func)  
```
