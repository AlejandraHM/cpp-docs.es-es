---
title: Error del compilador C2030 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2030
dev_langs:
- C++
helpviewer_keywords:
- C2030
ms.assetid: 5806cead-64df-4eff-92de-52c9a3f5ee62
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b0c5849c372cc4c7ebf27dbe010e65d406ad1ab1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032907"
---
# <a name="compiler-error-c2030"></a>Error del compilador C2030

un destructor con accesibilidad 'protected private' no puede ser miembro de una clase declarada 'sealed'

Una clase de Windows en tiempo de ejecución declarada como `sealed` no puede tener un destructor privado protegido. En tipos sealed solo se permiten destructores no virtuales privados y virtuales públicos. Para obtener más información, consulte [clases y structs Ref](../../cppcx/ref-classes-and-structs-c-cx.md).

Para corregir este error, cambie la accesibilidad del destructor.