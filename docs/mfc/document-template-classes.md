---
title: Clases de plantillas de documentos
ms.date: 11/04/2016
f1_keywords:
- vc.classes.document
helpviewer_keywords:
- document templates [MFC], classes
ms.assetid: 901749e9-8048-44a0-b5e2-361554650a73
ms.openlocfilehash: b15263005f8bd6a8fdc9f9f29ea268fe8a6b95a3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50448079"
---
# <a name="document-template-classes"></a>Clases de plantillas de documentos

Objetos de plantilla de documento coordinan la creación de documento, vista y los objetos de ventana de marco cuando un documento nuevo o se crea la vista.

[CDocTemplate](../mfc/reference/cdoctemplate-class.md)<br/>
La clase base para las plantillas de documento. No se utiliza esta clase nunca directamente; en su lugar, use una de las otras clases de plantilla de documento derivadas de esta clase.

[CMultiDocTemplate](../mfc/reference/cmultidoctemplate-class.md)<br/>
Una plantilla para los documentos de la interfaz de múltiples documentos (MDI). Las aplicaciones MDI pueden tener varios documentos abiertos a la vez.

[CSingleDocTemplate](../mfc/reference/csingledoctemplate-class.md)<br/>
Una plantilla para los documentos de la interfaz de único documento (SDI). Las aplicaciones SDI tienen solo un documento abierto a la vez.

## <a name="related-class"></a>Clase relacionada

[CCreateContext](../mfc/reference/ccreatecontext-structure.md)<br/>
Una estructura pasada por una plantilla de documento a las funciones de creación de ventanas para coordinar la creación de objetos de documento, vista y ventana de marco.

## <a name="see-also"></a>Vea también

[Información general de clases](../mfc/class-library-overview.md)

