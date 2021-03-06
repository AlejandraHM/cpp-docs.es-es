---
title: Redistribuir una aplicación ATL
ms.date: 11/04/2016
helpviewer_keywords:
- ATL, redistributing
- redistributing ATL
- redistributing OLE DB templates
- OLE DB templates, redistributing
ms.assetid: 9a696b22-2345-43ec-826b-be7cb8cfd676
ms.openlocfilehash: 183363f7e69fc6d14ce3f9e681992e774b198928
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50517109"
---
# <a name="redistributing-an-atl-application"></a>Redistribuir una aplicación ATL

A partir de Visual Studio 2012, Active Template Library (ATL) es una biblioteca solo de encabezado. Los proyectos ATL no tienen un vínculo dinámico a la opción de ATL. No se necesita ninguna biblioteca ATL redistribuible.

Si redistribuye una aplicación ejecutable ATL, debe registrar el archivo .exe (y cualquier control que contenga) ejecutando el siguiente comando:

```
filename /regserver
```

donde `filename` es el nombre del archivo ejecutable.

En Visual Studio 2010, puede generarse un proyecto ATL para una configuración MinDependency o MinSize. La configuración MinDependency es lo que se obtiene al establecer la propiedad **Uso de ATL** en **Vínculo estático a ATL** en la página de propiedades **General** y al establecer la propiedad **Biblioteca en tiempo de ejecución** en **Multiproceso (/MT)** en la página de propiedades **Generación de código** (carpeta C/C++).

La configuración MinSize es lo que se obtiene al establecer la propiedad **Uso de ATL** en **Vínculo dinámico a ATL** en la página de propiedades **General**, o bien al establecer la propiedad **Biblioteca en tiempo de ejecución** en **DLL multiproceso (/MD)** en la página de propiedades **Generación de código** (carpeta C/C++).

MinSize hace que el archivo de salida sea lo más pequeño posible, pero requiere la presencia de los archivos ATL100.dll y Msvcr100.dl (si seleccionó la opción **DLL multiproceso (/MD)**) en el equipo de destino. ATL100.dll debe registrarse en el equipo de destino para garantizar que esté presente toda la funcionalidad de ATL. ATL100.dll contiene exportaciones ANSI y Unicode.

Si compila el proyecto de plantillas ATL u OLE DB para un destino MinDependency, no tendrá que instalar ni registrar ATL100.dll en el equipo de destino, si bien puede obtener una imagen de programa de mayor tamaño.

Si redistribuye una aplicación ejecutable ATL, debe registrar el archivo .exe (y cualquier control que contenga) ejecutando el siguiente comando:

```
filename /regserver
```

donde `filename` es el nombre del archivo ejecutable.

## <a name="see-also"></a>Vea también

[Redistribuir archivos de Visual C++](../ide/redistributing-visual-cpp-files.md)