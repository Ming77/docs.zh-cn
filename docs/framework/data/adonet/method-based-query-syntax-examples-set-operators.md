---
title: "基于方法的查询语法示例：集运算符 (LINQ to DataSet)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: fa93af15-28af-4b5e-846b-897308410edb
caps.latest.revision: "2"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 637e1c2fe66bcfd31b0392076b8b1058d0008482
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/17/2018
---
# <a name="method-based-query-syntax-examples-set-operators-linq-to-dataset"></a>基于方法的查询语法示例：集运算符 (LINQ to DataSet)
本主题中的示例演示如何使用<xref:System.Linq.Enumerable.Distinct%2A>， <xref:System.Linq.Enumerable.Except%2A>， <xref:System.Linq.Enumerable.Intersect%2A>，和<xref:System.Linq.Enumerable.Union%2A>运算符执行的数据行集的基于值的比较运算。[加载数据到显示数据集](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)请参阅[比较 Datarow](../../../../docs/framework/data/adonet/comparing-datarows-linq-to-dataset.md)有关详细信息<xref:System.Data.DataRowComparer>。  
  
 `FillDataSet`中指定这些示例中使用的方法[加载数据到数据集](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)。  
  
 本主题中的示例使用 AdventureWorks 示例数据库中的 Contact、Address、Product、SalesOrderHeader 和 SalesOrderDetail 表。  
  
 本主题中的示例使用以下`using` / `Imports`语句：  
  
 [!code-csharp[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP LINQ to DataSet Examples#ImportsUsing](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#importsusing)]  
  
 有关详细信息，请参阅[如何： 创建 LINQ to DataSet 项目在 Visual Studio 中](../../../../docs/framework/data/adonet/how-to-create-a-linq-to-dataset-project-in-vs.md)。  
  
## <a name="distinct"></a>Distinct  
  
### <a name="example"></a>示例  
 此示例使用 <xref:System.Linq.Enumerable.Distinct%2A> 方法移除序列中的重复元素。  
  
 [!code-csharp[DP LINQ to DataSet Examples#DistinctRows](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#distinctrows)]
 [!code-vb[DP LINQ to DataSet Examples#DistinctRows](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#distinctrows)]  
  
## <a name="except"></a>Except  
  
### <a name="example"></a>示例  
 此示例使用 <xref:System.Linq.Enumerable.Except%2A> 方法返回出现在第一个表中但不出现在第二个表中的联系人。  
  
 [!code-csharp[DP LINQ to DataSet Examples#Except2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#except2)]
 [!code-vb[DP LINQ to DataSet Examples#Except2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#except2)]  
  
## <a name="intersect"></a>Intersect  
  
### <a name="example"></a>示例  
 此示例使用 <xref:System.Linq.Enumerable.Intersect%2A> 方法返回同时出现在两个表中的联系人。  
  
 [!code-csharp[DP LINQ to DataSet Examples#Intersect2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#intersect2)]
 [!code-vb[DP LINQ to DataSet Examples#Intersect2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#intersect2)]  
  
## <a name="union"></a>联合  
  
### <a name="example"></a>示例  
 此示例使用 <xref:System.Linq.Enumerable.Union%2A> 方法返回这两个表的任一表中特有的联系人。  
  
 [!code-csharp[DP LINQ to DataSet Examples#Union2](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/CS/Program.cs#union2)]
 [!code-vb[DP LINQ to DataSet Examples#Union2](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DP LINQ to DataSet Examples/VB/Module1.vb#union2)]  
  
## <a name="see-also"></a>请参阅  
 [将数据加载到数据集中](../../../../docs/framework/data/adonet/loading-data-into-a-dataset.md)  
 [LINQ to DataSet 示例](../../../../docs/framework/data/adonet/linq-to-dataset-examples.md)  
 [标准查询运算符概述](http://msdn.microsoft.com/library/24cda21e-8af8-4632-b519-c404a839b9b2)
