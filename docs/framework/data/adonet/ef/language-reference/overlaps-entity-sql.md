---
title: OVERLAPS (Entity SQL)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 41743e89-79cb-4d7b-8a27-355b45024b61
caps.latest.revision: "3"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 22593af3f79e78621764ba293e65505a72b194f8
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/17/2018
---
# <a name="overlaps-entity-sql"></a>OVERLAPS (Entity SQL)
确定两个集合是否具有公共元素。  
  
## <a name="syntax"></a>语法  
  
```  
expression OVERLAPS expression  
```  
  
## <a name="arguments"></a>自变量  
 `expression`  
 返回一个集合以与从其他查询表达式返回的集合进行比较的任何有效查询表达式。 所有表达式都必须与 `expression`一样属于同一类型或属于公共基类型或派生类型。  
  
## <a name="return-value"></a>返回值  
 如果两个集合具有公共元素，则为`true` ；否则为 `false`。  
  
## <a name="remarks"></a>备注  
 OVERLAPS 提供的功能等效于以下：  
  
 `EXISTS ( expression INTERSECT expression )`  
  
 OVERLAPS 是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符之一。 所有 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 集运算符都是从左到右进行求值。 有关优先级信息[!INCLUDE[esql](../../../../../../includes/esql-md.md)]集运算符，请参阅[EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md)。  
  
## <a name="example"></a>示例  
 以下 Entity SQL 查询使用 OVERLAPS 运算符以确定两个集合是否具有公共值。 此查询基于 AdventureWorks 销售模型。 若要编译并运行此查询，请执行下列步骤：  
  
1.  执行 [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。  
  
2.  将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：  
  
 [!code-csharp[DP EntityServices Concepts 2#OVERLAPS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#overlaps)]  
  
## <a name="see-also"></a>请参阅  
 [实体 SQL 引用](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
