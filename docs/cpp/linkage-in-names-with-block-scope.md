---
title: "Vinculación en nombres con ámbito de bloque | Documentos de Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- scope [C++], linkage rules
- linkage [C++], scope linkage rules
- names [C++], scope linkage rules
- block scope [C++]
- external linkage, scope linkage rules
ms.assetid: 73efa91a-f761-47f7-bbd9-9f9e3508e218
caps.latest.revision: 8
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: de093c90e0da4a906d8aefebfb7048733c1a1f1d
ms.contentlocale: es-es
ms.lasthandoff: 09/25/2017

---
# <a name="linkage-in-names-with-block-scope"></a>Vinculación en nombres con ámbito de bloque
Las siguientes reglas de vinculación se aplican a los nombres con ámbito de bloque (nombres locales):  
  
-   Nombres declarados como `extern` tienen vinculación externa a menos que se hubieran declarado previamente como **estático**.  
  
-   El resto de los nombres con ámbito de bloque no tienen vinculación.  
  
## <a name="see-also"></a>Vea también  
 [Programa y vinculación](../cpp/program-and-linkage-cpp.md)
