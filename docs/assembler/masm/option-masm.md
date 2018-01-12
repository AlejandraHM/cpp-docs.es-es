---
title: "OPCIÓN (MASM) | Documentos de Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: option
dev_langs: C++
helpviewer_keywords: OPTION directive
ms.assetid: 8e10dabd-e36f-4586-ab01-ada96736b0bd
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: f449606b143bfbf188e878b261f3d35017846862
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2017
---
# <a name="option-masm"></a>OPTION (MASM)
Habilita y deshabilita las características del ensamblador.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
OPTION   
optionlist  
  
```  
  
## <a name="remarks"></a>Comentarios  
 Las opciones disponibles incluyen:  
  
|||||  
|-|-|-|-|  
|**CASEMAP**|**DOTNAME**|**NODOTNAME**|**EMULADOR**|  
|**NOEMULATOR**|**EPÍLOGO**|**EXPR16**|**EXPR32**|  
|**IDIOMA**|**LJMP**|**NOLJMP**|**M510**|  
|**NOM510**|**NOKEYWORD**|**NOSIGNEXTEND**|**DESPLAZAMIENTO**|  
|**OLDMACROS**|**NOOLDMACROS**|**OLDSTRUCTS**|**NOOLDSTRUCTS**|  
|**PROC**|**PRÓLOGO**|**SOLO LECTURA**|**NOREADONLY**|  
|**EL ÁMBITO**|**NOSCOPED**|**SEGMENT**|**SETIF2**.|  
  
 La sintaxis de LENGUAJE es **opción idioma:***x*, donde *x* es uno de C, SYSCALL, STDCALL, PASCAL, FORTRAN o BASIC.  SYSCALL, PASCAL, FORTRAN y BASIC no son compatibles con utiliza con [. MODELO](../../assembler/masm/dot-model.md) sin formato.  
  
## <a name="see-also"></a>Vea también  
 [Referencia de directivas](../../assembler/masm/directives-reference.md)