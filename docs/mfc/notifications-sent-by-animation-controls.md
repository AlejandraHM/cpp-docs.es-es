---
title: Notificaciones enviadas por los controles de animación | Documentos de Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- notifications [MFC], animation controls
- CAnimateCtrl class [MFC], notifications
- controls [MFC], animation
- animation controls [MFC], notifications
ms.assetid: 584f5824-446b-4a1a-85f7-ef61842c8186
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c1696389ce3dc40c5d02ec660ebaeb6bf3e6c3ec
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33345256"
---
# <a name="notifications-sent-by-animation-controls"></a>Notificaciones enviadas por los controles de animación
Un control de animación ([CAnimateCtrl](../mfc/reference/canimatectrl-class.md)) envía dos tipos diferentes de mensajes de notificación. Las notificaciones se envían en forma de [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) mensajes.  
  
 El [mensaje ACN_START](http://msdn.microsoft.com/library/windows/desktop/bb761891) mensaje se envía cuando el control de animación ha empezado a reproducir un clip. El [mensaje ACN_STOP](http://msdn.microsoft.com/library/windows/desktop/bb761893) mensaje se envía cuando el control de animación ha terminado o ha dejado de reproducir un clip.  
  
## <a name="see-also"></a>Vea también  
 [Usar CAnimateCtrl](../mfc/using-canimatectrl.md)   
 [Controles](../mfc/controls-mfc.md)

