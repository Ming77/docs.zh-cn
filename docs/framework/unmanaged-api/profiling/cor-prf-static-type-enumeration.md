---
title: "COR_PRF_STATIC_TYPE 枚举"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_PRF_STATIC_TYPE
api_location: mscorwks.dll
api_type: COM
f1_keywords: COR_PRF_STATIC_TYPE
helpviewer_keywords: COR_PRF_STATIC_TYPE enumeration [.NET Framework profiling]
ms.assetid: 441d7809-5b65-41a5-ba64-2910a8008315
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 76d43a620b64c771427cd30af770e70642dabe7a
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="corprfstatictype-enumeration"></a>COR_PRF_STATIC_TYPE 枚举
指示字段是否为静态的，并在字段为静态字段时指示应用于该字段的静态质量。 可以使用按位或运算以指示该字段具有多个组合这些值不同的静态质量。  
  
## <a name="syntax"></a>语法  
  
```  
typedef enum {  
    COR_PRF_FIELD_NOT_A_STATIC = 0x0,  
    COR_PRF_FIELD_APP_DOMAIN_STATIC = 0x1,  
    COR_PRF_FIELD_THREAD_STATIC = 0x2,  
    COR_PRF_FIELD_CONTEXT_STATIC = 0x4,  
    COR_PRF_FIELD_RVA_STATIC = 0x8  
} COR_PRF_STATIC_TYPE;  
```  
  
## <a name="members"></a>成员  
  
|成员|描述|  
|------------|-----------------|  
|`COR_PRF_FIELD_NOT_A_STATIC`|该字段不是静态的。|  
|`COR_PRF_FIELD_APP_DOMAIN_STATIC`|该字段是应用程序域静态。|  
|`COR_PRF_FIELD_THREAD_STATIC`|该字段是线程静态。|  
|`COR_PRF_FIELD_CONTEXT_STATIC`|该字段是上下文静态。|  
|`COR_PRF_FIELD_RVA_STATIC`|该字段是相对虚拟地址 (RVA) 的静态。|  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [分析枚举](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
