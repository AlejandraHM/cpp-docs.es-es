---
title: no_dual_interfaces | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- no_dual_interfaces
dev_langs:
- C++
helpviewer_keywords:
- no_dual_interfaces attribute
ms.assetid: 9acd5d9d-4a49-4cdc-9470-73a2c23cf512
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: ba20fcba43cc23dfce447d7e91955a43c28a6a31
ms.sourcegitcommit: d51ed21ab2b434535f5c1d553b22e432073e1478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/23/2018
---
# <a name="nodualinterfaces"></a>no_dual_interfaces
**C++ Specific**  
  
 Cambia la manera en que el compilador genera las funciones de contenedor para los métodos de interfaz dual.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
no_dual_interfaces  
```  
  
## <a name="remarks"></a>Comentarios  
 Normalmente, el contenedor llamará al método a través de la tabla de funciones virtuales para la interfaz. Con `no_dual_interfaces`, el contenedor llama en su lugar **IDispatch:: Invoke** para invocar el método.  
  
 **FIN de específicos de C++**  
  
## <a name="see-also"></a>Vea también  
 [atributos #import](../preprocessor/hash-import-attributes-cpp.md)   
 [#import (directiva)](../preprocessor/hash-import-directive-cpp.md)