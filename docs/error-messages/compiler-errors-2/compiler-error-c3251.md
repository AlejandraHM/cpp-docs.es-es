---
title: Error del compilador C3251 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3251
dev_langs:
- C++
helpviewer_keywords:
- C3251
ms.assetid: 541c163e-5ee9-457c-a1e5-da860788b10d
caps.latest.revision: 6
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
ms.openlocfilehash: 085c8f75b1f1ed047f4b81c739448b6b2c97169c
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3251"></a>Error del compilador C3251
no se puede invocar el método de clase base en una instancia de tipo de valor  
  
 El siguiente error se produce porque `GetClass` es un miembro de `Microsoft.Runtime.Object`, no de `Microsoft.Runtime.Integer4`.
