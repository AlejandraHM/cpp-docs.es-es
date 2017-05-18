---
title: Clase IPersistStorageImpl | Documentos de Microsoft
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- IPersistStorageImpl
- ATLCOM/ATL::IPersistStorageImpl
- ATLCOM/ATL::IPersistStorageImpl::GetClassID
- ATLCOM/ATL::IPersistStorageImpl::HandsOffStorage
- ATLCOM/ATL::IPersistStorageImpl::InitNew
- ATLCOM/ATL::IPersistStorageImpl::IsDirty
- ATLCOM/ATL::IPersistStorageImpl::Load
- ATLCOM/ATL::IPersistStorageImpl::Save
- ATLCOM/ATL::IPersistStorageImpl::SaveCompleted
dev_langs:
- C++
helpviewer_keywords:
- storage, ATL
- IPersistStorageImpl class
ms.assetid: d652f02c-239c-47c7-9a50-3e9fc3014fff
caps.latest.revision: 20
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0e0c08ddc57d437c51872b5186ae3fc983bb0199
ms.openlocfilehash: a5a855f81072316510efb47c3f9650a5feafa39b
ms.contentlocale: es-es
ms.lasthandoff: 02/24/2017

---
# <a name="ipersiststorageimpl-class"></a>Clase IPersistStorageImpl
Esta clase implementa la [IPersistStorage](http://msdn.microsoft.com/library/windows/desktop/ms679731) interfaz.  
  
> [!IMPORTANT]
>  Esta clase y sus miembros no se pueden utilizar en las aplicaciones que se ejecutan en [!INCLUDE[wrt](../../atl/reference/includes/wrt_md.md)].  
  
## <a name="syntax"></a>Sintaxis  
  
```
template <class T>  
class ATL_NO_VTABLE IPersistStorageImpl : public IPersistStorage
```  
  
#### <a name="parameters"></a>Parámetros  
 `T`  
 La clase derivada de `IPersistStorageImpl`.  
  
## <a name="members"></a>Miembros  
  
### <a name="public-methods"></a>Métodos públicos  
  
|Nombre|Descripción|  
|----------|-----------------|  
|[IPersistStorageImpl::GetClassID](#getclassid)|Recupera el CLSID del objeto.|  
|[IPersistStorageImpl::HandsOffStorage](#handsoffstorage)|Indica al objeto para liberar todos los objetos de almacenamiento y entrar en modo de HandsOff. Devuelve la implementación de ATL `S_OK`.|  
|[IPersistStorageImpl::InitNew](#initnew)|Inicializa un nuevo almacenamiento.|  
|[IPersistStorageImpl::IsDirty](#isdirty)|Comprueba si los datos del objeto ha cambiado desde que se guardó por última vez.|  
|[IPersistStorageImpl::Load](#load)|Carga las propiedades del objeto desde el almacenamiento especificado.|  
|[IPersistStorageImpl::Save](#save)|Guarda las propiedades del objeto en el almacenamiento especificado.|  
|[IPersistStorageImpl::SaveCompleted](#savecompleted)|Notifica a un objeto que puede volver al modo Normal para escribir en su objeto de almacenamiento. Devuelve la implementación de ATL `S_OK`.|  
  
## <a name="remarks"></a>Comentarios  
 `IPersistStorageImpl`implementa el [IPersistStorage](http://msdn.microsoft.com/library/windows/desktop/ms679731) interfaz, lo que permite a un cliente para solicitar que la carga del objeto y guardar sus mediante un almacenamiento de datos persistentes.  
  
 La implementación de esta clase requiere la clase `T` para realizar una implementación de la `IPersistStreamInit` disponible a través de la interfaz `QueryInterface`. Normalmente esto significa que esa clase `T` debe derivar de [IPersistStreamInitImpl](../../atl/reference/ipersiststreaminitimpl-class.md), proporcionar una entrada para `IPersistStreamInit` en el [mapa COM](http://msdn.microsoft.com/library/ead2a1e3-334d-44ad-bb1f-b94bb14c2333)y usar un [mapa de propiedades](http://msdn.microsoft.com/library/bfe30be6-62c3-4dc2-bd49-21ef96f15427) para describir los datos persistentes de la clase.  
  
 **Artículos relacionados con** [Tutorial ATL](../../atl/active-template-library-atl-tutorial.md), [crear un proyecto ATL](../../atl/reference/creating-an-atl-project.md)  
  
## <a name="inheritance-hierarchy"></a>Jerarquía de herencia  
 `IPersistStorage`  
  
 `IPersistStorageImpl`  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** atlcom.h  
  
##  <a name="getclassid"></a>IPersistStorageImpl::GetClassID  
 Recupera el CLSID del objeto.  
  
```
STDMETHOD(GetClassID)(CLSID* pClassID);
```  
  
### <a name="remarks"></a>Comentarios  
 Consulte [IPersist:: GetClassID](http://msdn.microsoft.com/library/windows/desktop/ms688664) en el [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)].  
  
##  <a name="handsoffstorage"></a>IPersistStorageImpl::HandsOffStorage  
 Indica al objeto para liberar todos los objetos de almacenamiento y entrar en modo de HandsOff.  
  
```
STDMETHOD(HandsOffStorage)(void);
```  
  
### <a name="return-value"></a>Valor devuelto  
 Devuelve `S_OK`.  
  
### <a name="remarks"></a>Comentarios  
 Consulte [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/windows/desktop/ms679742) en el [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)].  
  
##  <a name="initnew"></a>IPersistStorageImpl::InitNew  
 Inicializa un nuevo almacenamiento.  
  
```
STDMETHOD(InitNew)(IStorage*);
```  
  
### <a name="remarks"></a>Comentarios  
 La implementación de ATL se delega en el [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interfaz.  
  
 Consulte [IPersistStorage:InitNew](http://msdn.microsoft.com/library/windows/desktop/ms687194) en el [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)].  
  
##  <a name="isdirty"></a>IPersistStorageImpl::IsDirty  
 Comprueba si los datos del objeto ha cambiado desde que se guardó por última vez.  
  
```
STDMETHOD(IsDirty)(void);
```  
  
### <a name="remarks"></a>Comentarios  
 La implementación de ATL se delega en el [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interfaz.  
  
 Consulte [IPersistStorage:IsDirty](http://msdn.microsoft.com/library/windows/desktop/ms683910) en el [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)].  
  
##  <a name="load"></a>IPersistStorageImpl::Load  
 Carga las propiedades del objeto desde el almacenamiento especificado.  
  
```
STDMETHOD(Load)(IStorage* pStorage);
```  
  
### <a name="remarks"></a>Comentarios  
 La implementación de ATL se delega en el [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interfaz. **Carga** utiliza una secuencia llamada "Contenido" para recuperar los datos del objeto. El [guardar](#save) método originalmente crea esta secuencia.  
  
 Consulte [IPersistStorage:Load](http://msdn.microsoft.com/library/windows/desktop/ms680557) en el [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)].  
  
##  <a name="save"></a>IPersistStorageImpl::Save  
 Guarda las propiedades del objeto en el almacenamiento especificado.  
  
```
STDMETHOD(Save)(IStorage* pStorage, BOOL fSameAsLoad);
```  
  
### <a name="remarks"></a>Comentarios  
 La implementación de ATL se delega en el [IPersistStreamInit](http://msdn.microsoft.com/library/windows/desktop/ms682273) interfaz. Cuando **guardar** primero llama, crea una secuencia llamada "Contenido" en el almacenamiento especificado. Esta secuencia se utiliza en llamadas posteriores a **guardar** y en las llamadas a [carga](#load).  
  
 Consulte [IPersistStorage:Save](http://msdn.microsoft.com/library/windows/desktop/ms680680) en el [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)].  
  
##  <a name="savecompleted"></a>IPersistStorageImpl::SaveCompleted  
 Notifica a un objeto que puede volver al modo Normal para escribir en su objeto de almacenamiento.  
  
```
STDMETHOD(SaveCompleted)(IStorage*);
```  
  
### <a name="return-value"></a>Valor devuelto  
 Devuelve `S_OK`.  
  
### <a name="remarks"></a>Comentarios  
 Consulte [IPersistStorage:SaveCompleted](http://msdn.microsoft.com/library/windows/desktop/ms679713) en el [!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)].  
  
## <a name="see-also"></a>Vea también  
 [Almacenamientos y secuencias](http://msdn.microsoft.com/library/windows/desktop/aa380352)   
 [Clase IPersistStreamInitImpl](../../atl/reference/ipersiststreaminitimpl-class.md)   
 [Clase IPersistPropertyBagImpl](../../atl/reference/ipersistpropertybagimpl-class.md)   
 [Información general de la clase](../../atl/atl-class-overview.md)

