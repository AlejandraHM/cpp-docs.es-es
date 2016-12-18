---
title: "asctime, _wasctime | Microsoft Docs"
ms.custom: ""
ms.date: "12/05/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "_wasctime"
  - "asctime"
apilocation: 
  - "msvcrt.dll"
  - "msvcr80.dll"
  - "msvcr90.dll"
  - "msvcr100.dll"
  - "msvcr100_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr120.dll"
  - "msvcr120_clr0400.dll"
  - "ucrtbase.dll"
  - "api-ms-win-crt-time-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "_tasctime"
  - "asctime"
  - "_wasctime"
dev_langs: 
  - "C++"
  - "C"
helpviewer_keywords: 
  - "_tasctime (función)"
  - "_wasctime (función)"
  - "asctime (función)"
  - "tasctime (función)"
  - "conversión de estructura de tiempo"
  - "hora, convertir"
  - "wasctime (función)"
ms.assetid: 974f1727-10ff-4ed4-8cac-2eb2d681f576
caps.latest.revision: 22
caps.handback.revision: 20
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# asctime, _wasctime
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Convierte una estructura en tiempo de `tm` a una cadena de caracteres.  Hay disponibles versiones más seguras de estas funciones; vea [asctime\_s, \_wasctime\_s](../../c-runtime-library/reference/asctime-s-wasctime-s.md).  
  
## Sintaxis  
  
```  
char *asctime(   
   const struct tm *timeptr   
);  
wchar_t *_wasctime(   
   const struct tm *timeptr   
);  
```  
  
#### Parámetros  
 `timeptr`  
 Estructura de hora o de fecha.  
  
## Valor devuelto  
 `asctime` devuelve un puntero al resultado de la cadena de caracteres; `_wasctime` devuelve un puntero al resultado de cadena de caracteres.  No hay ningún valor devuelto del error.  
  
## Comentarios  
 Versiones más seguras de estas funciones están disponibles; vea [asctime\_s, \_wasctime\_s](../../c-runtime-library/reference/asctime-s-wasctime-s.md).  
  
 La función de `asctime` convierte una hora almacenada como una estructura a una cadena de caracteres.  El valor de `timeptr` se obtiene normalmente de una llamada a `gmtime` o a `localtime`, que ambos devuelven un puntero a una estructura de `tm` , definido en TIME.H.  
  
|miembro del timeptr|Valor|  
|-------------------------|-----------|  
|`tm_hour`|Horas desde la medianoche \(0\-23\)|  
|`tm_isdst`|Positivo si el horario de verano está vigente; 0 si el horario de verano no está vigente; negativa si el estado de horario de verano es desconocido.  La biblioteca en tiempo de ejecución de C supone las reglas de los Estados Unidos para implementar el cálculo en tiempo \(DST\) de Guardar Daylight.|  
|`tm_mday`|Día del mes \(1\-31\)|  
|`tm_min`|Minutos después de la hora \(0\-59\)|  
|`tm_mon`|Mes \(0\-11; Enero \= 0\)|  
|`tm_sec`|Segundos después de minuto \(0\-59\)|  
|`tm_wday`|Día de la semana \(0\-6; Domingo \= 0\)|  
|`tm_yday`|Día del año \(0\-365; 1 de enero \= 0\)|  
|`tm_year`|Año \(año actual menos 1900\)|  
  
 Cadena de caracteres convierte también se ajusta según la configuración de zonas de la hora local.  Para obtener información sobre la configuración de la hora local, vea [tiempo](../../c-runtime-library/reference/time-time32-time64.md), [\_ftime](../../c-runtime-library/reference/ftime-ftime32-ftime64.md), y las funciones de [localtime](../../c-runtime-library/reference/localtime-localtime32-localtime64.md) y la función de [\_tzset](../../c-runtime-library/reference/tzset.md) para obtener información sobre la definición del entorno y las variables globales de la zona horaria.  
  
 El resultado de la cadena generado por `asctime` contiene exactamente 26 caracteres y tiene el formato `Wed Jan 02 02:03:55 1980\n\0`.  Se utiliza un reloj de 24 horas.  Todos los campos tienen un ancho constante.  El carácter de nueva línea y el carácter null ocupan las dos últimas posiciones de la cadena.  `asctime` utiliza un búfer único, estática asignado para contener la cadena devuelta.  Cada llamada a esta función destruye el resultado de la llamada anterior.  
  
 `_wasctime` es una versión con caracteres anchos de `asctime`.  Por lo demás, `_wasctime` y `asctime` se comportan de forma idéntica.  
  
 Estas funciones validan sus parámetros.  Si `timeptr` es un puntero null, o si contiene valores que se fuera\-de\- intervalo, se invoca el controlador no válido de parámetro, tal y como se describe en [Validación de parámetros](../../c-runtime-library/parameter-validation.md).  Si la ejecución puede continuar, la función devuelve `NULL` y establece en `errno` en `EINVAL`.  
  
### Asignación rutinaria de Genérico\- texto  
  
|Rutina TCHAR.H|\_UNICODE y \_MBCS no definidos|\_MBCS definido|\_UNICODE definido|  
|--------------------|-------------------------------------|---------------------|------------------------|  
|`_tasctime`|`asctime`|`asctime`|`_wasctime`|  
  
## Requisitos  
  
|Rutina|Encabezado necesario|  
|------------|--------------------------|  
|`asctime`|\<time.h\>|  
|`_wasctime`|\<time.h o\> wchar.h \<\>|  
  
## Ejemplo  
 Este programa coloca la hora del sistema en `aclock`entero largo, la convierte en la estructura `newtime` y la convierte al formato de cadena para la salida, mediante la función de `asctime` .  
  
```  
// crt_asctime.c  
// compile with: /W3  
  
#include <time.h>  
#include <stdio.h>  
  
int main( void )  
{  
    struct tm   *newTime;  
    time_t      szClock;  
  
    // Get time in seconds  
    time( &szClock );  
  
    // Convert time to struct tm form   
    newTime = localtime( &szClock );  
  
    // Print local time as a string.  
    printf_s( "Current date and time: %s", asctime( newTime ) ); // C4996  
    // Note: asctime is deprecated; consider using asctime_s instead  
}  
```  
  
  **Fecha y hora actual: Sun 3 de febrero de 11: 38:58 2002**   
## Equivalente en .NET Framework  
  
-   [System::DateTime::ToLongDateString](https://msdn.microsoft.com/en-us/library/system.datetime.tolongdatestring.aspx)  
  
-   [System::DateTime::ToLongTimeString](https://msdn.microsoft.com/en-us/library/system.datetime.tolongtimestring.aspx)  
  
-   [System::DateTime::ToShortDateString](https://msdn.microsoft.com/en-us/library/system.datetime.toshortdatestring.aspx)  
  
-   [System::DateTime::ToShortTimeString](https://msdn.microsoft.com/en-us/library/system.datetime.toshorttimestring.aspx)  
  
-   [System::DateTime::ToString](https://msdn.microsoft.com/en-us/library/system.datetime.tostring.aspx)  
  
## Vea también  
 [Administración del tiempo](../../c-runtime-library/time-management.md)   
 [ctime, \_ctime32, \_ctime64, \_wctime, \_wctime32, \_wctime64](../../c-runtime-library/reference/ctime-ctime32-ctime64-wctime-wctime32-wctime64.md)   
 [\_ftime, \_ftime32, \_ftime64](../../c-runtime-library/reference/ftime-ftime32-ftime64.md)   
 [gmtime, \_gmtime32, \_gmtime64](../../c-runtime-library/reference/gmtime-gmtime32-gmtime64.md)   
 [localtime, \_localtime32, \_localtime64](../../c-runtime-library/reference/localtime-localtime32-localtime64.md)   
 [time, \_time32, \_time64](../../c-runtime-library/reference/time-time32-time64.md)   
 [\_tzset](../../c-runtime-library/reference/tzset.md)   
 [asctime\_s, \_wasctime\_s](../../c-runtime-library/reference/asctime-s-wasctime-s.md)