---
title: "Error del compilador CS0206 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0206"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0206"
ms.assetid: d2f9838a-d8ae-4342-b8bd-fa5745619a26
caps.latest.revision: 8
caps.handback.revision: 8
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Error del compilador CS0206
Una propiedad o un indizador no se puede pasar como parámetro out o ref.  
  
 Existe una [propiedad](../Topic/Properties%20\(C%23%20Programming%20Guide\).md) que no está disponible para pasarla como parámetro [ref](../Topic/ref%20\(C%23%20Reference\).md) o [out](../Topic/out%20\(C%23%20Reference\).md). Para obtener más información, consulta [Pasar parámetros](../Topic/Passing%20Parameters%20\(C%23%20Programming%20Guide\).md).  
  
## Ejemplo  
 El ejemplo siguiente genera la advertencia CS0206:  
  
```  
// CS0206.cs public class MyClass { public static int P { get { return 0; } set { } } public static void MyMeth(ref int i) // public static void MyMeth(int i) { } public static void Main() { MyMeth(ref P);   // CS0206 // try the following line instead // MyMeth(P);   // CS0206 } }  
```