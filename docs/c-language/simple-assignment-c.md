---
title: "Asignación simple (C) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- type conversion [C++], simple assignment
- data type conversion [C++], simple assignment
- operators [C], simple assignment
- assignment operators [C++], simple
- simple assignment operator
- equal sign
ms.assetid: e7140a0a-7104-4b3a-b293-7adcc1fdd52b
caps.latest.revision: 7
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 16d1bf59dfd4b3ef5f037aed9c0f6febfdf1a2e8
ms.openlocfilehash: c6f81732b4fccdac6ae0912b7617c28318da3e55
ms.contentlocale: es-es
ms.lasthandoff: 10/09/2017

---
# <a name="simple-assignment-c"></a>Asignación simple (C)
El operador de asignación simple asigna el operando derecho al operando izquierdo. El valor del operando derecho se convierte al tipo de la expresión de asignación y reemplaza el valor almacenado en el objeto designado por el operando izquierdo. Se aplican las reglas de conversión para asignación (vea [Conversiones de asignación](../c-language/assignment-conversions.md)).  
  
```  
double x;  
int y;  
  
x = y;  
```  
  
 En este ejemplo, el valor de `y` se convierte al tipo **double** y se asigna a `x`.  
  
## <a name="see-also"></a>Vea también  
 [Operadores de asignación de C](../c-language/c-assignment-operators.md)
