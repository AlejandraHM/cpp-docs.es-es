---
title: 'CBulkRowset:: setRows | Documentos de Microsoft'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL.CBulkRowset.SetRows
- CBulkRowset::SetRows
- CBulkRowset<TAccessor>.SetRows
- ATL.CBulkRowset<TAccessor>.SetRows
- CBulkRowset<TAccessor>::SetRows
- ATL::CBulkRowset<TAccessor>::SetRows
- ATL::CBulkRowset::SetRows
- CBulkRowset.SetRows
- SetRows
dev_langs: C++
helpviewer_keywords: SetRows method
ms.assetid: 7e92312a-bfd0-4c24-a799-62bef663f28e
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 543ea1fcc1a87319e9a9ca952417f76f140663f6
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2017
---
# <a name="cbulkrowsetsetrows"></a>CBulkRowset::SetRows
Establece el número de identificadores de fila recuperados por cada llamada.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
  
      void SetRows(  
   DBROWCOUNT nRows   
) throw( );  
```  
  
#### <a name="parameters"></a>Parámetros  
 `nRows`  
 [in] El nuevo tamaño del conjunto de filas (número de filas).  
  
## <a name="remarks"></a>Comentarios  
 Si se llama a esta función, debe ser antes de abre el conjunto de filas.  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** atldbcli.h  
  
## <a name="see-also"></a>Vea también  
 [CBulkRowset (Clase)](../../data/oledb/cbulkrowset-class.md)