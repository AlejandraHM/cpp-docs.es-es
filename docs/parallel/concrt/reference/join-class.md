---
title: Join (clase) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: reference
f1_keywords:
- join
- AGENTS/concurrency::join
- AGENTS/concurrency::join::join
- AGENTS/concurrency::join::accept_message
- AGENTS/concurrency::join::consume_message
- AGENTS/concurrency::join::link_target_notification
- AGENTS/concurrency::join::propagate_message
- AGENTS/concurrency::join::propagate_to_any_targets
- AGENTS/concurrency::join::release_message
- AGENTS/concurrency::join::reserve_message
- AGENTS/concurrency::join::resume_propagation
dev_langs:
- C++
helpviewer_keywords:
- join class
ms.assetid: d2217119-70a1-40b6-809f-c1c13a571c3f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 46073d07cbca27256ca169ab94e0fe027bf98b15
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118861"
---
# <a name="join-class"></a>join (Clase)
Un bloque de mensajería `join` es un bloque `propagator_block` de destino único y de varios orígenes ordenado, que combina los mensajes de tipo `T` de cada uno de sus orígenes.  
  
## <a name="syntax"></a>Sintaxis  
  
```
template<class T,
    join_type _Jtype = non_greedy>
class join : public propagator_block<single_link_registry<ITarget<std::vector<T>>>,
    multi_link_registry<ISource<T>>>;
```   
  
#### <a name="parameters"></a>Parámetros  
*T*<br/>
El tipo de carga de los mensajes Unido y propagados por el bloque.  
  
*_Jtype*<br/>
El tipo de `join` bloque es, ya sea `greedy` o `non_greedy`  
  
## <a name="members"></a>Miembros  
  
### <a name="public-constructors"></a>Constructores públicos  
  
|Name|Descripción|  
|----------|-----------------|  
|[join](#ctor)|Sobrecargado. Construye un `join` bloque de mensajería.|  
|[~ join (destructor)](#dtor)|Destruye el `join` bloque.|  
  
### <a name="protected-methods"></a>Métodos protegidos  
  
|Name|Descripción|  
|----------|-----------------|  
|[accept_message](#accept_message)|Acepta un mensaje que se ha proporcionado por este `join` bloque de mensajería, transferencia de la propiedad al llamador.|  
|[consume_message](#consume_message)|Consume un mensaje ofrecido previamente por el `join` bloque de mensajería y reservado por el destino, transfiriendo la propiedad al llamador.|  
|[link_target_notification](#link_target_notification)|Una devolución de llamada que notifica que se ha vinculado un nuevo destino para esta `join` bloque de mensajería.|  
|[propagate_message](#propagate_message)|Pasa de forma asincrónica un mensaje desde un `ISource` bloque a este `join` bloque de mensajería. Se invoca con el `propagate` método, cuando se llama a un bloque de origen.|  
|[propagate_to_any_targets](#propagate_to_any_targets)|Construye un mensaje de salida que contiene un mensaje de entrada de cada origen cuando todo haya propagado un mensaje. Envía este mensaje de salida a cada uno de sus destinos.|  
|[release_message](#release_message)|Libera una reserva de mensaje anterior. (Invalida [source_block:: release_message](source-block-class.md#release_message).)|  
|[reserve_message](#reserve_message)|Reserva un mensaje ofrecido previamente por este `join` bloque de mensajería. (Invalida [source_block:: reserve_message](source-block-class.md#reserve_message).)|  
|[resume_propagation](#resume_propagation)|Reanuda la propagación después de que se ha liberado una reserva. (Invalida [source_block:: resume_propagation](source-block-class.md#resume_propagation).)|  
  
## <a name="remarks"></a>Comentarios  
 Para obtener más información, consulte [bloques de mensajes asincrónicos](../../../parallel/concrt/asynchronous-message-blocks.md).  
  
## <a name="inheritance-hierarchy"></a>Jerarquía de herencia  
 [ISource](isource-class.md)  
  
 [ITarget](itarget-class.md)  
  
 [source_block)](source-block-class.md)  
  
 [propagator_block](propagator-block-class.md)  
  
 `join`  
  
## <a name="requirements"></a>Requisitos  
 **Encabezado:** agents.h  
  
 **Espacio de nombres:** simultaneidad  
  
##  <a name="accept_message"></a> accept_message 

 Acepta un mensaje que se ha proporcionado por este `join` bloque de mensajería, transferencia de la propiedad al llamador.  
  
```
virtual message<_OutputType>* accept_message(runtime_object_identity _MsgId);
```  
  
### <a name="parameters"></a>Parámetros  
*_MsgId*<br/>
El `runtime_object_identity` de la ofrecida `message` objeto.  
  
### <a name="return-value"></a>Valor devuelto  
 Un puntero a la `message` que el llamador tiene ahora la propiedad de objeto.  
  
##  <a name="consume_message"></a> consume_message 

 Consume un mensaje ofrecido previamente por el `join` bloque de mensajería y reservado por el destino, transfiriendo la propiedad al llamador.  
  
```
virtual message<_OutputType>* consume_message(runtime_object_identity _MsgId);
```  
  
### <a name="parameters"></a>Parámetros  
*_MsgId*<br/>
El `runtime_object_identity` de la `message` objeto consumido.  
  
### <a name="return-value"></a>Valor devuelto  
 Un puntero a la `message` que el llamador tiene ahora la propiedad de objeto.  
  
### <a name="remarks"></a>Comentarios  
 Similar a `accept`, pero siempre está precedido por una llamada a `reserve`.  
  
##  <a name="ctor"></a> combinación 

 Construye un `join` bloque de mensajería.  
  
```
join(
    size_t _NumInputs);

join(
    size_t _NumInputs,
    filter_method const& _Filter);

join(
    Scheduler& _PScheduler,
    size_t _NumInputs);

join(
    Scheduler& _PScheduler,
    size_t _NumInputs,
    filter_method const& _Filter);

join(
    ScheduleGroup& _PScheduleGroup,
    size_t _NumInputs);

join(
    ScheduleGroup& _PScheduleGroup,
    size_t _NumInputs,
    filter_method const& _Filter);
```  
  
### <a name="parameters"></a>Parámetros  
*_NumInputs*<br/>
El número de entradas esto `join` se permitirá el bloque.  
  
*_Filtrar*<br/>
Una función de filtro que determina si se deben aceptar mensajes ofrecidos.  
  
*_PScheduler*<br/>
El objeto `Scheduler` dentro del que se programa la tarea de propagación para el bloque de mensajería `join`.  
  
*_PScheduleGroup*<br/>
El objeto `ScheduleGroup` dentro del que se programa la tarea de propagación para el bloque de mensajería `join`. El objeto `Scheduler` utilizado está implícito en el grupo de programación.  
  
### <a name="remarks"></a>Comentarios  
 El runtime usa el programador predeterminado si no se especifican los parámetros `_PScheduler` o `_PScheduleGroup` .  
  
 El tipo `filter_method` es un functor con firma `bool (T const &)` que es invocado por este `join` bloque de mensajería para determinar si debe aceptar un mensaje proporcionado.  
  
##  <a name="dtor"></a> ~ join 

 Destruye el `join` bloque.  
  
```
~join();
```  
  
##  <a name="link_target_notification"></a> link_target_notification 

 Una devolución de llamada que notifica que se ha vinculado un nuevo destino para esta `join` bloque de mensajería.  
  
```
virtual void link_target_notification(_Inout_ ITarget<std::vector<T>> *);
```  
  
##  <a name="propagate_message"></a> propagate_message 

 Pasa de forma asincrónica un mensaje desde un `ISource` bloque a este `join` bloque de mensajería. Se invoca con el `propagate` método, cuando se llama a un bloque de origen.  
  
```
message_status propagate_message(
    _Inout_ message<T>* _PMessage,
    _Inout_ ISource<T>* _PSource);
```  
  
### <a name="parameters"></a>Parámetros  
*Parámetro _PMessage*<br/>
Un puntero al objeto `message`.  
  
*_PSource*<br/>
Un puntero al bloque de origen que proporciona el mensaje.  
  
### <a name="return-value"></a>Valor devuelto  
 Un [message_status](concurrency-namespace-enums.md) indicación de lo que el destino decidió hacer con el mensaje.  
  
##  <a name="propagate_to_any_targets"></a> propagate_to_any_targets 

 Construye un mensaje de salida que contiene un mensaje de entrada de cada origen cuando todo haya propagado un mensaje. Envía este mensaje de salida a cada uno de sus destinos.  
  
```
void propagate_to_any_targets(_Inout_opt_ message<_OutputType> *);
```  
  
##  <a name="release_message"></a> release_message 

 Libera una reserva de mensaje anterior.  
  
```
virtual void release_message(runtime_object_identity _MsgId);
```  
  
### <a name="parameters"></a>Parámetros  
*_MsgId*<br/>
El `runtime_object_identity` de la `message` objeto liberarse.  
  
##  <a name="reserve_message"></a> reserve_message 

 Reserva un mensaje ofrecido previamente por este `join` bloque de mensajería.  
  
```
virtual bool reserve_message(runtime_object_identity _MsgId);
```  
  
### <a name="parameters"></a>Parámetros  
*_MsgId*<br/>
El `runtime_object_identity` de la ofrecida `message` objeto.  
  
### <a name="return-value"></a>Valor devuelto  
 `true` Si el mensaje se ha reservado correctamente, `false` en caso contrario.  
  
### <a name="remarks"></a>Comentarios  
 Después de `reserve` se llama, si devuelve `true`, ya sea `consume` o `release` debe llamarse para aceptar o liberar la propiedad del mensaje.  
  
##  <a name="resume_propagation"></a> resume_propagation 

 Reanuda la propagación después de que se ha liberado una reserva.  
  
```
virtual void resume_propagation();
```  
  
## <a name="see-also"></a>Vea también  
 [simultaneidad Namespace](concurrency-namespace.md)   
 [Choice (clase)](choice-class.md)   
 [multitype_join (clase)](multitype-join-class.md)
