---
title: Error del compilador C2170 | Documentos de Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2170
dev_langs:
- C++
helpviewer_keywords:
- C2170
ms.assetid: d5c663f0-2459-4e11-a8bf-a52b62f3c71d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ad0d19dff10d04d155d8071ffb349664f6b3104e
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33171095"
---
# <a name="compiler-error-c2170"></a>Error del compilador C2170
'identificador': no se ha declarado como una función, no puede ser intrínseco  
  
### <a name="to-fix-by-checking-the-following-possible-causes"></a>Posibles causas del error:  
  
1.  Pragma `intrinsic` se utiliza para un elemento que no es una función.  
  
2.  Pragma `intrinsic` se utiliza para una función sin forma intrínseca.