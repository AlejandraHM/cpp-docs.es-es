---
title: Compilador advertencia (nivel 1) C4615 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4615
dev_langs:
- C++
helpviewer_keywords:
- C4615
ms.assetid: 7b107c01-0da2-4e01-8b40-93813e30b94c
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 41ddf5e421e5840fa5d17dfb6a619a0d4ee1099d
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-warning-level-1-c4615"></a>Advertencia del compilador (nivel 1) C4615
\#advertencia pragma: tipo de advertencia de usuario desconocido  
  
 Se utilizó un especificador de advertencia no válido con **pragma** [advertencia](../../preprocessor/warning.md). Para resolver el error, utilice un especificador de advertencia válido.  
  
 El ejemplo siguiente genera C4615:  
  
```  
// C4615.cpp  
// compile with: /W1 /LD  
#pragma warning(enable : 4401)   // C4615, 'enable' not valid specifier  
  
// use the code below to resolve the error  
// #pragma warning(default : 4401)  
```
