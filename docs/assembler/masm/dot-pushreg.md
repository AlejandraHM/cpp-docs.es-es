---
title: . PUSHREG | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: .PUSHREG
dev_langs: C++
helpviewer_keywords: .PUSHREG directive
ms.assetid: e0c83758-dfed-40ea-afe6-cb833c8d2d30
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: f85e1082c38eb2880ff6ad3c15b4842ebf015ca6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2017
---
# <a name="pushreg"></a>.PUSHREG
Genera un `UWOP_PUSH_NONVOL` entrada al código de desenredado de número con el desplazamiento actual en el prólogo de registro especificado.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
.PUSHREG register  
```  
  
## <a name="remarks"></a>Comentarios  
 . PUSHREG permite a los usuarios de ml64.exe especificar cómo se desenreda una función de marco y solo se permite en el prólogo, que abarca desde el [PROC](../../assembler/masm/proc.md) declaración de marco para el [. ENDPROLOG](../../assembler/masm/dot-endprolog.md) directiva. Estas directivas no generan código; solo generan `.xdata` y `.pdata`. . PUSHREG debe ir precedida de instrucciones que realmente se implementan las acciones que puede desenredar. Es una buena práctica para ajustar las directivas de desenredado y el código que están concebidos para desenredar en una macro para asegurarse de acuerdo.  
  
 Para obtener más información, consulte [MASM para x64 (ml64.exe)](../../assembler/masm/masm-for-x64-ml64-exe.md).  
  
## <a name="sample"></a>Ejemplo  
  
### <a name="description"></a>Descripción  
 El ejemplo siguiente muestra cómo insertar tegisters no volátil.  
  
### <a name="code"></a>Código  
  
```  
; ml64 ex1.asm /link /entry:Example1 /SUBSYSTEM:CONSOLE  
_text SEGMENT  
Example1 PROC FRAME  
   push r10  
.pushreg r10  
   push r15  
.pushreg r15  
   push rbx  
.pushreg rbx  
   push rsi  
.pushreg rsi  
.endprolog  
   ; rest of function ...  
   ret  
Example1 ENDP  
_text ENDS  
END  
```  
  
## <a name="see-also"></a>Vea también  
 [Referencia de directivas](../../assembler/masm/directives-reference.md)