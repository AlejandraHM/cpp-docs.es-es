---
title: Compilador Error C2756 | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2756
dev_langs:
- C++
helpviewer_keywords:
- C2756
ms.assetid: 42eb988d-4043-4dee-8fd4-596949f69a55
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 4ca6e01d1c4b2f7dda2a941eeef4599d62241fe3
ms.contentlocale: es-es
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2756"></a>Compilador Error C2756
'template type': no se permiten argumentos de plantilla predeterminados en una especialización parcial  
  
 La plantilla de una especialización parcial no puede contener un argumento predeterminado.  
  
 El siguiente ejemplo genera el error C2756 y muestra cómo corregirlo:  
  
```  
// C2756.cpp  
template <class T>  
struct S {};  
  
template <class T=int>  
// try the following line instead  
// template <class T>  
struct S<T*> {};   // C2756  
```
