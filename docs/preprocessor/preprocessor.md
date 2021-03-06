---
title: Preprocesador
ms.date: 11/04/2016
helpviewer_keywords:
- preprocessor
ms.assetid: e120eda3-b413-49f1-a07c-e9fb128cf500
ms.openlocfilehash: bd139dcbbbe519cc4c9750a657f8b47c5a5bcd18
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50530974"
---
# <a name="preprocessor"></a>Preprocesador
El preprocesador es un procesador de texto que manipula el texto de un archivo de código fuente como parte de la primera fase de traducción. El preprocesador no analiza el texto original, sino que lo divide en tokens con el fin de buscar llamadas a macros. Aunque el compilador invoca normalmente el preprocesador en el primer paso, también se puede invocar el preprocesador por separado para procesar el texto sin compilación.

El material de referencia del preprocesador incluye las siguientes secciones:

- [Directivas de preprocesador](../preprocessor/preprocessor-directives.md)

- [Operadores de preprocesador](../preprocessor/preprocessor-operators.md)

- [Macros predefinidas](../preprocessor/predefined-macros.md)

- [Pragmas](../preprocessor/pragma-directives-and-the-pragma-keyword.md)

**Específicos de Microsoft**

Puede obtener una lista de código fuente tras el preprocesamiento mediante el uso de la [/E](../build/reference/e-preprocess-to-stdout.md) o [/EP](../build/reference/ep-preprocess-to-stdout-without-hash-line-directives.md) opción del compilador. Ambas opciones invocan el preprocesador y envían el texto resultante al dispositivo de salida estándar que, en la mayoría de los casos, es la consola. La diferencia entre las dos opciones es que /E incluye las directivas `#line` y /EP elimina estas directivas.

**FIN de Específicos de Microsoft**

##  <a name="_predir_special_terminology"></a> Terminología especial

En la documentación del preprocesador, el término “argumento” hace referencia a la entidad que se pasa a una función. En algunos casos, se cambia por “real” o “formal”, que describe la expresión de argumento especificada en la llamada de función y la declaración de argumento especificada en la definición de función, respectivamente.

El término “variable” hace referencia a un objeto de datos de tipo C. El término “objeto” hace referencia tanto a objetos como a variables de C++; es un término inclusivo.

## <a name="see-also"></a>Vea también

[Referencia del preprocesador de C/C++](../preprocessor/c-cpp-preprocessor-reference.md)<br/>
[Fases de traducción](../preprocessor/phases-of-translation.md)