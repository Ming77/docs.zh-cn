---
title: "ICorProfilerInfo4::InitializeCurrentThread 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo4::InitializeCurrentThread
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo4::InitializeCurrentThread
helpviewer_keywords:
- ICorProfilerInfo4::InitializeCurrentThread method [.NET Framework profiling]
- InitializeCurrentThread method, ICorProfilerInfo4 interface [.NET Framework profiling]
ms.assetid: 18a3335c-8c75-476c-b6de-72c0bfedae5d
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4f3c261068b38861dca2633a490e46d9f44371d7
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilerinfo4initializecurrentthread-method"></a>ICorProfilerInfo4::InitializeCurrentThread 方法
初始化之前在同一线程调用的 API，因此可以避免该死锁的后续探查器的当前线程。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT InitializeCurrentThread ();  
```  
  
## <a name="remarks"></a>备注  
 我们建议调用`InitializeCurrentThread`将调用探查器的任何线程 API 尽管有挂起的线程。 此方法通常由采样探查器可创建自己的线程来调用[icorprofilerinfo2:: Dostacksnapshot](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-dostacksnapshot-method.md)方法来执行堆栈将指导此目标线程被挂起时。 通过调用`InitializeCurrentThread`后当探查器首先创建采样线程，探查器可以确保每个线程迟缓初始化 CLR 将执行在第一次调用期间`DoStackSnapshot`现在可以发生的安全地没有其他线程都时挂起。  
  
> [!NOTE]
>  `InitializeCurrentThread`执行初始化提前以完成任务，可采用锁，并可能发生死锁。 调用`InitializeCurrentThread`仅当没有任何挂起的线程时。  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [ICorProfilerInfo4 接口](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)  
 [Profiling 接口](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [分析](../../../../docs/framework/unmanaged-api/profiling/index.md)
