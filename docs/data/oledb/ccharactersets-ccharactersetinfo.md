---
title: CCharacterSets, CCharacterSetInfo | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- m_szCollateName
- m_szCatalog
- DEFAULT_COLLATE_NAME
- m_szCollateSchema
- FORM_OF_USE
- DEFAULT_COLLATE_SCHEMA
- m_szCollateCatalog
- CCharacterSets
- CHARACTER_SET_NAME
- DEFAULT_COLLATE_CATALOG
- CHARACTER_SET_SCHEMA
- m_szFormOfUse
- NUMBER_OF_CHARACTERS
- m_szSchema
- CHARACTER_SET_CATALOG
- CCharacterSetInfo
- m_nNumCharacters
- m_szName
dev_langs: C++
helpviewer_keywords:
- DEFAULT_COLLATE_SCHEMA
- m_nNumCharacters
- m_szSchema
- NUMBER_OF_CHARACTERS
- m_szCollateCatalog
- CCharacterSetInfo parameter class
- m_szCatalog
- CCharacterSets typedef class
- m_szCollateName
- m_szName
- m_szCollateSchema
- FORM_OF_USE OLE DB column
- CHARACTER_SET_NAME
- DEFAULT_COLLATE_CATALOG
- DEFAULT_COLLATE_NAME
- m_szFormOfUse
- CHARACTER_SET_SCHEMA
- CHARACTER_SET_CATALOG
ms.assetid: 029d068c-8bb2-4fc0-8709-78ce7f74446e
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 41945cbb34c8e984922d46671b591426d94067cd
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2017
---
# <a name="ccharactersets-ccharactersetinfo"></a>CCharacterSets, CCharacterSetInfo
Llamar a la clase de typedef **CCharacterSets** para implementar su clase de parámetro **CCharacterSetInfo**.  
  
## <a name="remarks"></a>Comentarios  
 Vea [clases de conjunto de filas de esquema y clases Typedef](../../data/oledb/schema-rowset-classes-and-typedef-classes.md) para obtener más información sobre el uso de clases typedef.  
  
 Esta clase identifica los juegos de caracteres definidos en el catálogo que son accesibles para un usuario determinado.  
  
 En la tabla siguiente se enumera los miembros de datos de la clase y sus columnas OLE DB correspondiente. Vea [conjunto de filas CHARACTER_SETS](https://msdn.microsoft.com/en-us/library/ms722638.aspx) en el *referencia del programador de OLE DB* para obtener más información sobre el esquema y las columnas.  
  
|Miembros de datos|Columnas de OLE DB|  
|------------------|--------------------|  
|m_szCatalog|CHARACTER_SET_CATALOG|  
|m_szSchema|CHARACTER_SET_SCHEMA|  
|m_szName|CHARACTER_SET_NAME|  
|m_szFormOfUse|FORM_OF_USE|  
|m_nNumCharacters|NUMBER_OF_CHARACTERS|  
|m_szCollateCatalog|DEFAULT_COLLATE_CATALOG|  
|m_szCollateSchema|DEFAULT_COLLATE_SCHEMA|  
|m_szCollateName|DEFAULT_COLLATE_NAME|  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** atldbsch.h  
  
## <a name="see-also"></a>Vea también  
 [CRestrictions (Clase)](../../data/oledb/crestrictions-class.md)