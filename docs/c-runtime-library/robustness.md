---
title: Solidez
ms.date: 11/04/2016
f1_keywords:
- c.runtime
helpviewer_keywords:
- robustness [CRT]
ms.assetid: 7f1a87f8-eff9-4b76-ae9b-d133d3de6adf
ms.openlocfilehash: 9244ba430efab01cd82b8ad773ad669470d67cff
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50454709"
---
# <a name="robustness"></a>Solidez

Use las siguientes funciones de la biblioteca en tiempo de ejecución de C para mejorar la solidez del programa.

## <a name="run-time-robustness-functions"></a>Funciones de solidez en tiempo de ejecución

|Función|Usar|
|--------------|---------|
|[_set_new_handler](../c-runtime-library/reference/set-new-handler.md)|Transfiere el control al mecanismo de control de errores si el operador **new** no puede asignar memoria.|
|[_set_se_translator](../c-runtime-library/reference/set-se-translator.md)|Controla las excepciones Win32 (excepciones estructuradas de C) como con excepciones con tipo de C++.|
|[set_terminate](../c-runtime-library/reference/set-terminate-crt.md)|Instala su propia función de finalización a la que debe llamar [terminate](../c-runtime-library/reference/terminate-crt.md).|
|[set_unexpected](../c-runtime-library/reference/set-unexpected-crt.md)|Instala su propia función de finalización a la que debe llamar [unexpected](../c-runtime-library/reference/unexpected-crt.md).|

## <a name="see-also"></a>Vea también

[Rutinas en tiempo de ejecución Universal C por categoría](../c-runtime-library/run-time-routines-by-category.md)<br/>
[SetUnhandledExceptionFilter](https://msdn.microsoft.com/library/windows/desktop/ms680634.aspx)<br/>
