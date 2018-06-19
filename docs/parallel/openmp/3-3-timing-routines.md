---
title: 3.3 rutinas temporales | Documentos de Microsoft
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 21060d64-cbe8-4e38-8718-3a68d6a57be3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b3b8fc16e34124419362d5989131c2cf66df30b6
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2018
ms.locfileid: "33694916"
---
# <a name="33-timing-routines"></a>3.3 Rutinas temporales
Las funciones descritas en esta sección admiten un temporizador de reloj portátil:  
  
-   El `omp_get_wtime` función devuelve la hora de reloj transcurrido.  
  
-   El `omp_get_wtick` función devuelve segundos entre ciclos de reloj sucesivas.