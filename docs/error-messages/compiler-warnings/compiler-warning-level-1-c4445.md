---
title: Compilador advertencia (nivel 1) C4445 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4445
dev_langs:
- C++
helpviewer_keywords:
- C4445
ms.assetid: 535e92a0-ba08-4dfc-89b2-af2dcdd7caeb
caps.latest.revision: 8
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
ms.openlocfilehash: ab6972edab2da855b859c05bf15ec4fc86a4d23a
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-warning-level-1-c4445"></a>Advertencia del compilador (nivel 1) C4445
'función': un método virtual no puede ser privado en un tipo WinRT o administrado  
  
 Si una función virtual es privada, un tipo derivado no puede tener acceso a ella. Para corregir este error, cambie la accesibilidad de la función miembro virtual a protegida o pública.
