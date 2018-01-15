---
title: "Notificaciones enviadas por los controles de animación | Documentos de Microsoft"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- notifications [MFC], animation controls
- CAnimateCtrl class [MFC], notifications
- controls [MFC], animation
- animation controls [MFC], notifications
ms.assetid: 584f5824-446b-4a1a-85f7-ef61842c8186
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: c57a33bf4b13397d4f296ef4e5aa8e137c2d3594
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2017
---
# <a name="notifications-sent-by-animation-controls"></a>Notificaciones enviadas por los controles de animación
Un control de animación ([CAnimateCtrl](../mfc/reference/canimatectrl-class.md)) envía dos tipos diferentes de mensajes de notificación. Las notificaciones se envían en forma de [WM_COMMAND](http://msdn.microsoft.com/library/windows/desktop/ms647591) mensajes.  
  
 El [mensaje ACN_START](http://msdn.microsoft.com/library/windows/desktop/bb761891) mensaje se envía cuando el control de animación ha empezado a reproducir un clip. El [mensaje ACN_STOP](http://msdn.microsoft.com/library/windows/desktop/bb761893) mensaje se envía cuando el control de animación ha terminado o ha dejado de reproducir un clip.  
  
## <a name="see-also"></a>Vea también  
 [Usar CAnimateCtrl](../mfc/using-canimatectrl.md)   
 [Controles](../mfc/controls-mfc.md)

