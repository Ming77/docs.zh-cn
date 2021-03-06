---
title: "ICLRRuntimeHost 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRRuntimeHost
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRRuntimeHost
helpviewer_keywords: ICLRRuntimeHost interface [.NET Framework hosting]
ms.assetid: cb0c5f65-3791-47bc-b833-2f84f4101ba5
topic_type: apiref
caps.latest.revision: "26"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 247c50eb88f3b1814fd5342ded4ed3c98d4b60a6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="iclrruntimehost-interface"></a>ICLRRuntimeHost 接口
提供的功能类似于[ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)在.NET Framework 版本 1 包含以下更改提供的接口：  
  
-   添加[SetHostControl](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-sethostcontrol-method.md)方法以设置主机控件接口。  
  
-   提供一些方法省略`ICorRuntimeHost`。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[ExecuteApplication 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-executeapplication-method.md)|在基于清单的 ClickOnce 部署方案中用于指定要在新域中激活的应用程序。|  
|[ExecuteInAppDomain 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-executeinappdomain-method.md)|指定<xref:System.AppDomain>在其中执行指定的托管的代码。|  
|[ExecuteInDefaultAppDomain 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-executeindefaultappdomain-method.md)|调用中指定的程序集的指定类型的指定的方法。|  
|[GetCLRControl 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-getclrcontrol-method.md)|获取类型的接口指针[ICLRControl](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)主机可用于自定义的公共语言运行时 (CLR) 方面。|  
|[GetCurrentAppDomainId 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-getcurrentappdomainid-method.md)|获取的数字标识符<xref:System.AppDomain>，当前正在执行。|  
|[SetHostControl 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-sethostcontrol-method.md)|设置主机控件接口。 必须调用`SetHostControl`之前调用`Start`。|  
|[Start 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md)|初始化到进程中 CLR。|  
|[Stop 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-stop-method.md)|由运行时停止执行的代码。|  
|[UnloadAppDomain 方法](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-unloadappdomain-method.md)|卸载<xref:System.AppDomain>对应于指定的数字标识符。|  
  
## <a name="remarks"></a>备注  
 从开始[!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]，使用[ICLRMetaHost](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)接口以获取指向[ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)接口，，然后调用[iclrruntimeinfo:: Getinterface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-getinterface-method.md)方法以获取指向`ICLRRuntimeHost`。 在.NET framework 的早期版本，主机获取指向的指针`ICLRRuntimeHost`实例通过调用[CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)或[CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md)。 若要提供的任何.NET Framework 2.0 版中提供的技术实现，你必须使用`ICLRRuntimeHost`而不是`ICorRuntimeHost`。  
  
> [!IMPORTANT]
>  不要调用[启动](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md)方法之前调用[ExecuteApplication](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-executeapplication-method.md)激活基于清单的应用程序的方法。 如果`Start`首先，调用方法`ExecuteApplication`方法调用将失败。  
  
## <a name="requirements"></a>惠?  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** MSCorEE.h  
  
 **库：**作为 MSCorEE.dll 中的资源  
  
 **.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [CorBindToCurrentRuntime 函数](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md)  
 [CorBindToRuntimeEx 函数](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md)  
 [ICLRControl 接口](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [ICorRuntimeHost 接口](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)  
 [承载接口](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [CLRRuntimeHost 组件类](../../../../docs/framework/unmanaged-api/hosting/clrruntimehost-coclass.md)
