---
title: "ICorDebugType2 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
api_name: ICorDebugType2
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugType2
helpviewer_keywords: ICorDebugType2 interface
ms.assetid: 376fb03f-f1ef-4107-baa4-4d9d55884862
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 8d44514586a2e91dad3486b6dc04c26946148885
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugtype2-interface"></a>ICorDebugType2 接口
扩展 ICorDebugType 接口以检索的基类型或复杂 （用户定义的） 类型的类型标识符。  
  
## <a name="methods"></a>方法  
  
|方法||  
|------------|-|  
|[GetTypeID 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugtype2-gettypeid-method.md)|获取[COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md)此类型。|  
  
## <a name="remarks"></a>备注  
 此接口是 ICorDebugType 接口的逻辑扩展。  
  
> [!NOTE]
>  此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="example"></a>示例  
 下面的代码段演示如何使用[ICorDebugType2::GetTypeID](../../../../docs/framework/unmanaged-api/debugging/icordebugtype2-gettypeid-method.md)方法。  
  
```  
// (error checking omitted for brevity)  
// given an ICorDebugType *pType  
  
ICorDebugType2 *pType2 = NULL;  
pType->QueryInterface(IID_ICorDebugType2, &pType);  
  
COR_TYPEID id;  
pType2->GetTypeID(&id);  
  
// now we can use existing APIs to get information about this COR_TYPEID  
```  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorDebug.idl、 CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [调试接口](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
