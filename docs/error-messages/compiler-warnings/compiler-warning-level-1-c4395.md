---
title: "Advertencia del compilador (nivel 1) C4395 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4395"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4395"
ms.assetid: 8051469a-3a39-4677-80f7-1300fbffe8ea
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Advertencia del compilador (nivel 1) C4395
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'función' : a la función miembro se invocará en una copia del miembro de datos initonly 'miembro'  
  
 Se llamó a una función miembro en un miembro de datos [initonly](../../dotnet/initonly-cpp-cli.md).  C4395 advierte que la función no puede modificar el miembro de datos de **initonly**.  
  
 El código siguiente genera el error C4395:  
  
```  
// C4395.cpp  
// compile with: /W1 /clr  
public value class V {  
public:  
   V(int data) : m_data(data) {}  
  
   void Mutate() {  
      System::Console::WriteLine("Enter Mutate: m_data = {0}", m_data);  
      m_data *= 2;  
      System::Console::WriteLine("Leave Mutate: m_data = {0}", m_data);  
   }  
  
   int m_data;  
};  
  
public ref class R {  
public:  
   static void f() {  
      System::Console::WriteLine("v.m_data = {0}", v.m_data);  
      v.Mutate();   // C4395  
      System::Console::WriteLine("v.m_data = {0}", v.m_data);  
   }  
  
private:  
   initonly static V v = V(4);  
};  
  
int main() {  
   R::f();  
}  
```