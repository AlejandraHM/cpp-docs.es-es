---
title: 'Cómo: declarar especificadores de invalidación (C++ / c++ / CLI)'
ms.date: 11/04/2016
helpviewer_keywords:
- override specifiers in native compilation, overriding
ms.assetid: d0551836-9ac7-41eb-a6e9-a4b3ef60767d
ms.openlocfilehash: a0c2d65aa44141b1dbe30fb39d66beabde93fa99
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "50555550"
---
# <a name="how-to-declare-override-specifiers-in-native-compilations-ccli"></a>Cómo: Declarar especificadores de invalidación en las compilaciones nativas (C++/CLI)

[sellado](../windows/sealed-cpp-component-extensions.md), [abstracta](../windows/abstract-cpp-component-extensions.md), y [invalidar](../windows/override-cpp-component-extensions.md) están disponibles en las compilaciones que no usan **/ZW** o [/CLR](../build/reference/clr-common-language-runtime-compilation.md).

> [!NOTE]
>  El ISO C ++ 11 estándar lenguaje tiene la [invalidar](../cpp/override-specifier.md) identificador y el [final](../cpp/final-specifier.md) identificador y ambos se admiten en Visual Studio, Use `final` en lugar de `sealed` en el código que está pensado para se compila como sólo nativo.

## <a name="example"></a>Ejemplo

### <a name="description"></a>Descripción

El ejemplo siguiente muestra que `sealed` es válida en compilaciones nativas.

### <a name="code"></a>Código

```cpp
// sealed_native_keyword.cpp
#include <stdio.h>
__interface I1 {
   virtual void f();
   virtual void g();
};

class X : public I1 {
public:
   virtual void g() sealed {}
};

class Y : public X {
public:

   // the following override generates a compiler error
   virtual void g() {}   // C3248 X::g is sealed!
};
```

## <a name="example"></a>Ejemplo

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra que `override` es válida en compilaciones nativas.

### <a name="code"></a>Código

```cpp
// override_native_keyword.cpp
#include <stdio.h>
__interface I1 {
   virtual void f();
};

class X : public I1 {
public:
   virtual void f() override {}   // OK
   virtual void g() override {}   // C3668 I1::g does not exist
};
```

## <a name="example"></a>Ejemplo

### <a name="description"></a>Descripción

En este ejemplo se muestra que `abstract` es válida en compilaciones nativas.

### <a name="code"></a>Código

```cpp
// abstract_native_keyword.cpp
class X abstract {};

int main() {
   X * MyX = new X;   // C3622 cannot instantiate abstract class
}
```

## <a name="see-also"></a>Vea también

[Especificadores de invalidación](../windows/override-specifiers-cpp-component-extensions.md)