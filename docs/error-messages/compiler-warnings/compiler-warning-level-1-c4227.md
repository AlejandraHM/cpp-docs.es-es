---
title: Compilador advertencia (nivel 1) C4227 | Documentos de Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4227
dev_langs:
- C++
helpviewer_keywords:
- C4227
ms.assetid: 78f98374-c00b-4000-aefa-1b1c67b4666b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0f3c0cced0e27d3f981c30251d4b9e1d78169559
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33273594"
---
# <a name="compiler-warning-level-1-c4227"></a>Advertencia del compilador (nivel 1) C4227
ha utilizado un anacronismo: se omiten los calificadores de referencia  
  
 Utilizar calificadores como `const` o `volatile` con referencias de C++ supone una práctica obsoleta.  
  
## <a name="example"></a>Ejemplo  
  
```  
// C4227.cpp  
// compile with: /W1 /c  
int j = 0;  
int &const i = j;   // C4227  
```