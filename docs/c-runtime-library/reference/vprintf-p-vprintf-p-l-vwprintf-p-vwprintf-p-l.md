---
title: _vprintf_p, _vprintf_p_l, _vwprintf_p, _vwprintf_p_l | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _vwprintf_p
- _vprintf_p
- _vprintf_p_l
- _vwprintf_p_l
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- _vwprintf_p_l
- vprintf_p
- _vprintf_p_l
- _vwprintf_p
- vprintf_p_l
- vwprintf_p_l
- vwprintf_p
- vtprintf_p
- _vtprintf_p
- _vprintf_p
dev_langs:
- C++
helpviewer_keywords:
- _vtprintf_p_l function
- _vtprintf_p function
- vtprintf_p function
- _vwprintf_p function
- _vwprintf_p_l function
- _vprintf_p function
- _vprintf_p_l function
- vprintf_p_l function
- vwprintf_p function
- vprintf_p function
- vtprintf_p_l function
- vwprintf_p_l function
- formatted text [C++]
ms.assetid: 3f99bde3-c891-493d-908f-30559c421058
caps.latest.revision: 17
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: e257f037a05c45f5b98e64ea55bd125af443b0be
ms.openlocfilehash: bcf46edc032856c7fa6b74d928cd08c04dcfac26
ms.contentlocale: es-es
ms.lasthandoff: 03/29/2017

---
# <a name="vprintfp-vprintfpl-vwprintfp-vwprintfpl"></a>_vprintf_p, _vprintf_p_l, _vwprintf_p, _vwprintf_p_l
Escribe salida con formato mediante un puntero a una lista de argumentos, y habilita la especificación del orden en el que se usan los argumentos.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
int _vprintf_p(  
   const char *format,  
   va_list argptr   
);  
int _vprintf_p_l(  
   const char *format,  
   locale_t locale,  
   va_list argptr   
);  
int _vwprintf_p(  
   const wchar_t *format,  
   va_list argptr   
);  
int _vwprintf_p_l(  
   const wchar_t *format,  
   locale_t locale,  
   va_list argptr   
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `format`  
 Especificación de formato.  
  
 `argptr`  
 Puntero a la lista de argumentos.  
  
 `locale`  
 Configuración regional que se va a usar.  
  
 Para más información, vea [Especificaciones de formato](../../c-runtime-library/format-specification-syntax-printf-and-wprintf-functions.md).  
  
## <a name="return-value"></a>Valor devuelto  
 `_vprintf_p` y `_vwprintf_p` devuelven el número de caracteres escritos, sin incluir el carácter de terminación nulo, o un valor negativo si se produce un error de salida.  
  
## <a name="remarks"></a>Comentarios  
 Cada una de estas funciones toma un puntero a una lista de argumentos y, a continuación, aplica formato a los datos determinados y los escribe en `stdout`. Estas funciones solo se diferencian de `vprintf_s` y `vwprintf_s` en que tienen la capacidad de especificar el orden en el que se usan los argumentos. Para más información, vea [printf_p (Parámetros de posición)](../../c-runtime-library/printf-p-positional-parameters.md).  
  
 `_vwprintf_p` es la versión de caracteres anchos de `_vprintf_p`. Las dos funciones se comportan exactamente igual si el flujo se abre en modo ANSI. `_vprintf_p` no admite actualmente la salida en un flujo UNICODE.  
  
 Las versiones de estas funciones con el sufijo `_l` son idénticas salvo que usan el parámetro locale pasado en lugar de la configuración regional del subproceso actual.  
  
> [!IMPORTANT]
>  Asegúrese de que `format` no es una cadena definida por el usuario. Para obtener más información, vea [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795)(Evitar saturaciones del búfer).  
  
 Si `format` es un puntero nulo, o si la cadena de formato contiene caracteres de formato no válidos, se invoca al controlador de parámetros no válidos, como se explica en [Validación de parámetros](../../c-runtime-library/parameter-validation.md). Si la ejecución puede continuar, las funciones devuelven -1 y establecen `errno` en `EINVAL`.  
  
### <a name="generic-text-routine-mappings"></a>Asignaciones de rutina de texto genérico  
  
|Rutina TCHAR.H|_UNICODE y _MBCS no definidos|_MBCS definido|_UNICODE definido|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vtprintf_p`|`_vprintf_p`|`_vprintf_p`|`_vwprintf_p`|  
|`_vtprintf_p_l`|`_vprintf_p_l`|`_vprintf_p_l`|`_vwprintf_p_l`|  
  
## <a name="requirements"></a>Requisitos  
  
|Rutina|Encabezado necesario|Encabezados opcionales|  
|-------------|---------------------|----------------------|  
|`_vprintf_p`, `_vprintf_p_l`|\<stdio.h> y \<stdarg.h>|\<varargs.h>*|  
|`_vwprintf_p`, `_vwprintf_p_l`|\<stdio.h> o \<wchar.h> y \<stdarg.h>|\<varargs.h>*|  
  
 \* Necesario para la compatibilidad con UNIX V.  
  
 La consola no se admite en las aplicaciones de [!INCLUDE[win8_appname_long](../../build/includes/win8_appname_long_md.md)]. Se deben redirigir los identificadores estándar de flujo que están asociados a la consola, `stdin`, `stdout` y `stderr`, antes de que las funciones en tiempo de ejecución de C puedan usarlos en aplicaciones de [!INCLUDE[win8_appname_long](../../build/includes/win8_appname_long_md.md)]. Para obtener más información sobre compatibilidad, vea [Compatibilidad](../../c-runtime-library/compatibility.md).  
  
## <a name="see-also"></a>Vea también  
 [E/S de secuencia](../../c-runtime-library/stream-i-o.md)   
 [vprintf (Funciones)](../../c-runtime-library/vprintf-functions.md)   
 [_fprintf_p, _fprintf_p_l, _fwprintf_p, _fwprintf_p_l](../../c-runtime-library/reference/fprintf-p-fprintf-p-l-fwprintf-p-fwprintf-p-l.md)   
 [_printf_p, _printf_p_l, _wprintf_p, _wprintf_p_l](../../c-runtime-library/reference/printf-p-printf-p-l-wprintf-p-wprintf-p-l.md)   
 [_sprintf_p, _sprintf_p_l, _swprintf_p, _swprintf_p_l](../../c-runtime-library/reference/sprintf-p-sprintf-p-l-swprintf-p-swprintf-p-l.md)   
 [vsprintf_s, _vsprintf_s_l, vswprintf_s, _vswprintf_s_l](../../c-runtime-library/reference/vsprintf-s-vsprintf-s-l-vswprintf-s-vswprintf-s-l.md)   
 [va_arg, va_copy, va_end, va_start](../../c-runtime-library/reference/va-arg-va-copy-va-end-va-start.md)   
 [_vfprintf_p, _vfprintf_p_l, _vfwprintf_p, _vfwprintf_p_l](../../c-runtime-library/reference/vfprintf-p-vfprintf-p-l-vfwprintf-p-vfwprintf-p-l.md)   
 [_printf_p, _printf_p_l, _wprintf_p, _wprintf_p_l](../../c-runtime-library/reference/printf-p-printf-p-l-wprintf-p-wprintf-p-l.md)   
 [printf_p (Parámetros de posición)](../../c-runtime-library/printf-p-positional-parameters.md)
