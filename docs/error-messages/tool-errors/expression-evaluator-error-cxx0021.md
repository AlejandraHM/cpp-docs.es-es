---
title: Error del evaluador de expresiones CXX0021
ms.date: 11/04/2016
f1_keywords:
- CXX0021
helpviewer_keywords:
- CXX0021
- CAN0021
ms.assetid: d6c0c35a-16c2-42c0-a7d2-e910350a47f0
ms.openlocfilehash: 373829e7200a556b3f832b1da127b4e33aa75749
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50447806"
---
# <a name="expression-evaluator-error-cxx0021"></a>Error del evaluador de expresiones CXX0021

struct o union utilizados como escalar

Se utilizó una estructura o unión en una expresión, pero no se especificó ningún elemento.

Al manipular una estructura o variable de unión, el nombre de la variable puede aparecer por sí mismo, sin un calificador de campo. Si se usa una estructura o unión en una expresión, se deben calificar con el elemento específico deseado.

Especifique el elemento cuyo valor es que se usará en la expresión.

Este error es idéntico a CAN0021.