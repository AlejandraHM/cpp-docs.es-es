---
title: Identificadores de comando
ms.date: 11/04/2016
helpviewer_keywords:
- command IDs, MFC
- command IDs
ms.assetid: e0171a2b-45b9-41fa-945d-ec2f7602ded0
ms.openlocfilehash: ecec4a7bd705dc74a3f45cc07da4abcdb168f43f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50445635"
---
# <a name="command-ids"></a>Identificadores de comando

Un comando se describe con detalle por su identificador de comando (codificados en el **WM_COMMAND** mensaje). Este identificador se asigna al objeto de interfaz de usuario que genera el comando. Normalmente, se denominan identificadores para la funcionalidad del objeto de interfaz de usuario que están asignados.

Por ejemplo, un elemento de borrar todo en el menú Edición podría asignarse un identificador como **ID_EDIT_CLEAR_ALL**. La biblioteca de clases predefine algunos identificadores, especialmente para los comandos que el marco de trabajo propia, controla como **ID_EDIT_CLEAR_ALL** o **ID_FILE_OPEN**. Va a crear otros identificadores de comando.

Al crear sus propios menús de Visual C++ editor de menús, es una buena idea a la biblioteca de clases de seguir la convención de nomenclatura como se muestra en **ID_FILE_OPEN**. [Comandos estándar](../mfc/standard-commands.md) explica los comandos estándares definidos por la biblioteca de clases.

## <a name="see-also"></a>Vea también

[Objetos de interfaz de usuario e identificadores de comando](../mfc/user-interface-objects-and-command-ids.md)

