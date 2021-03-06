---
title: "配置加密类"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- configuration files [.NET Framework], cryptography
- cryptographic algorithms
- security [.NET Framework], encryption
- cryptography, classes
- .NET Framework application configuration, cryptography
- default cryptography
ms.assetid: eee3ccb8-2c0d-4f35-b38d-6892a46c14e5
caps.latest.revision: "9"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: 23bd6007beb870895316a565283ee7e7354c931b
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="configuring-cryptography-classes"></a>配置加密类
[!INCLUDE[winsdklong](../../../includes/winsdklong-md.md)]允许计算机管理员配置的默认加密算法和.NET Framework 和相应地编写的应用程序使用的算法实现。  例如，具有自己的加密算法的实现的企业可以将该实现作为默认而不是在中提供实现[!INCLUDE[winsdkshort](../../../includes/winsdkshort-md.md)]。 虽然使用加密的托管应用程序始终可以选择显式地绑定到特定的实现，但建议他们通过使用加密配置系统创建加密对象。  
  
## <a name="in-this-section"></a>本节内容  
 [将算法名称映射到加密类](../../../docs/framework/configure-apps/map-algorithm-names-to-cryptography-classes.md)  
 描述如何将算法名称映射到加密类。  
  
 [将对象标识符映射到加密算法](../../../docs/framework/configure-apps/map-object-identifiers-to-cryptography-algorithms.md)  
 描述如何将对象标识符映射到加密算法。  
  
## <a name="related-sections"></a>相关章节  
 [Cryptographic Services](../../../docs/standard/security/cryptographic-services.md)  
 提供的加密服务提供的概述[!INCLUDE[winsdkshort](../../../includes/winsdkshort-md.md)]。  
  
 [加密设置架构](../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 描述将友好算法名映射到实现密码算法的类的元素。
