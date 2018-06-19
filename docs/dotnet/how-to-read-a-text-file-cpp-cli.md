---
title: 'Cómo: leer un archivo de texto (C++ / CLI) | Documentos de Microsoft'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- reading text files
- text files, reading
ms.assetid: 80551c01-d769-4b6d-8db7-fd53bde21b62
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: c350ea9cd8b71378d059a93ac80ca808d4f48790
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/04/2018
ms.locfileid: "33130203"
---
# <a name="how-to-read-a-text-file-ccli"></a>Cómo: Leer un archivo de texto (C++/CLI)
En el ejemplo de código siguiente se muestra cómo abrir y leer un archivo una línea de texto a la vez, mediante el uso de la <xref:System.IO.StreamReader> clase que se define en el <xref:System.IO?displayProperty=fullName> espacio de nombres. Una instancia de esta clase se utiliza para abrir un archivo de texto y, a continuación, el <xref:System.IO.StreamReader.ReadLine%2A?displayProperty=fullName> método se utiliza para recuperar cada línea.  
  
 Este ejemplo de código lee un archivo que tiene denominado textfile.txt y contiene texto. Para obtener información sobre este tipo de archivo, consulte [Cómo: escribir un archivo de texto (C++ / CLI)](../dotnet/how-to-write-a-text-file-cpp-cli.md).  
  
## <a name="example"></a>Ejemplo  
  
```  
// text_read.cpp  
// compile with: /clr  
#using<system.dll>  
using namespace System;  
using namespace System::IO;  
  
int main()  
{  
   String^ fileName = "textfile.txt";  
   try   
   {  
      Console::WriteLine("trying to open file {0}...", fileName);  
      StreamReader^ din = File::OpenText(fileName);  
  
      String^ str;  
      int count = 0;  
      while ((str = din->ReadLine()) != nullptr)   
      {  
         count++;  
         Console::WriteLine("line {0}: {1}", count, str );  
      }  
   }  
   catch (Exception^ e)  
   {  
      if (dynamic_cast<FileNotFoundException^>(e))  
         Console::WriteLine("file '{0}' not found", fileName);  
      else  
         Console::WriteLine("problem reading file '{0}'", fileName);  
   }  
  
   return 0;  
}  
```  
  
## <a name="see-also"></a>Vea también  
 [E/S de archivos y secuencias](http://msdn.microsoft.com/Library/4f4a33a9-66b7-4cd7-a285-4ad3e4276cd2)   
 [Programación de .NET con C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)