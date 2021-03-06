---
title: "在.NET 中分析字符串"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- parsing strings, about parsing strings
- IFormatProvider interface, parsing strings
- base types, parsing strings
- Parse method
- parsing strings
ms.assetid: 5e758b41-db93-456b-8999-99b7304b090d
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 811db42e04e73d7acbc03e303297b19fdf643384
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="parsing-strings-in-net"></a>在.NET 中分析字符串
分析操作将表示某种 .NET 基类型的字符串转换为该基类型。 例如，分析操作用于将字符串转换为浮点数字或日期和时间值。 最常用于执行分析操作的方法是 `Parse` 方法。 因为分析是格式设置（涉及将基类型转换为其字符串表示形式）的反向操作，所以有许多相同规则和约定适用。 正如格式设置使用实现的对象<xref:System.IFormatProvider>接口以提供实现的对象的区分区域性的格式设置信息，分析也使用<xref:System.IFormatProvider>接口来确定如何解释的字符串表示形式. 有关详细信息，请参阅[格式化类型](../../../docs/standard/base-types/formatting-types.md)。  
  
## <a name="in-this-section"></a>本节内容  
 [分析数值字符串](../../../docs/standard/base-types/parsing-numeric.md)  
 描述如何将字符串转换为.NET 数值类型。  
  
 [分析日期和时间字符串](../../../docs/standard/base-types/parsing-datetime.md)  
 描述如何将字符串转换为.NET **DateTime**类型。  
  
 [分析其他字符串](../../../docs/standard/base-types/parsing-other.md)  
 描述如何将转换将字符串读入**Char**，**布尔**，和**枚举**类型。  
  
## <a name="related-sections"></a>相关章节  
 [格式设置类型](../../../docs/standard/base-types/formatting-types.md)  
 描述基本格式设置的概念，如格式说明符和格式提供程序。  
  
 [.NET 中的类型转换](../../../docs/standard/base-types/type-conversion.md)  
 描述如何将类型转换。  
  
 [基类型](../../../docs/standard/base-types/index.md)  
 描述你可以对.NET 基类型执行的常见操作。
