---
title: CComObjectRoot (clase)
ms.date: 11/04/2016
f1_keywords:
- CComObjectRoot
- atlcom/ATL::CComObjectRoot
helpviewer_keywords:
- CComObjectRoot class
ms.assetid: f8797c38-6e73-4f67-85c2-71654cffa8eb
ms.openlocfilehash: 4761aa9ae9c8ffacfb393311d7e058b1450b4628
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50554981"
---
# <a name="ccomobjectroot-class"></a>CComObjectRoot (clase)

Esta definición de tipo de [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md) se hace plantilla en el modelo del servidor de subprocesamiento predeterminado.

## <a name="syntax"></a>Sintaxis

```
typedef CComObjectRootEx<CComObjectThreadModel> CComObjectRoot;
```

## <a name="remarks"></a>Comentarios

`CComObjectRoot` es un `typedef` de [CComObjectRootEx](../../atl/reference/ccomobjectrootex-class.md) hace plantilla en el modelo del servidor de subprocesamiento predeterminado. Por lo tanto [CComObjectThreadModel](atl-typedefs.md#ccomobjectthreadmodel) hará referencia alguno [CComSingleThreadModel](../../atl/reference/ccomsinglethreadmodel-class.md) o [CComMultiThreadModel](../../atl/reference/ccommultithreadmodel-class.md).

`CComObjectRootEx` controla la administración de recuento de referencia de objeto para objetos agregados y agregados. Si no se agrega el objeto y mantiene el puntero para el desconocido externo si se agrega el objeto contiene el recuento de referencias de objeto. Para los objetos agregados, `CComObjectRootEx` métodos que pueden usarse para controlar el error del objeto interno para construir y se elimina proteger el objeto contra eliminación cuando se publican las interfaces internas externo o el objeto interno.

## <a name="requirements"></a>Requisitos

**Encabezado:** atlcom.h

## <a name="see-also"></a>Vea también

[CComObjectRootEx (clase)](../../atl/reference/ccomobjectrootex-class.md)<br/>
[CComAggObject (clase)](../../atl/reference/ccomaggobject-class.md)<br/>
[CComObject (clase)](../../atl/reference/ccomobject-class.md)<br/>
[CComPolyObject (clase)](../../atl/reference/ccompolyobject-class.md)<br/>
[Información general de clases](../../atl/atl-class-overview.md)
