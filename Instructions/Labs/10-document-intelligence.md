---
lab:
  title: 从 Azure AI Foundry 门户的文档中提取数据
---

# 从 Azure AI Foundry 门户的文档中提取数据

**Azure AI 文档智能**服务能够分析和提取表单和文档中的信息，然后标识字段名称和数据。 

文档智能是如何建立在光学字符识别 (OCR) 之上的？ 虽然 OCR 可以读取打印文档或手写文档，但 OCR 是以非结构化格式提取文本，这很难存储在数据库中或用于进行分析。 文档智能通过捕获文本的结构（如数据字段和表中的信息）来帮助理解非结构化数据。 

在本练习中，你将在 Azure AI Foundry 门户（Microsoft 创建智能应用程序的平台）中使用 Azure AI 文档智能的预生成模型，以识别收据中的数据。 

## 在 Azure AI Foundry 门户中创建项目

1. 在浏览器选项卡中，导航到 [Azure AI Foundry](https://ai.azure.com?azure-portal=true)。

1. 使用你的帐户登录。 

1. 在 Azure AI Foundry 门户主页上，选择“**创建项目**”。 在 Azure AI Foundry 中，项目是有助于组织工作的容器。  

    ![Azure AI Foundry 主页的屏幕截图，其中选择了“创建项目”。](./media/azure-ai-foundry-home-page.png)

1. 在“*创建项目*”窗格中，会看到生成的项目名称，可以按原样保留。 根据你过去是否创建了中心，你将看到要创建的*新* Azure 资源列表或现有中心的下拉列表。 如果看到现有中心的下拉列表，请选择“*新建中心*”，为中心创建唯一名称，然后选择“*下一步*”。  
 
    ![“创建项目”窗格的屏幕截图，其中包含中心和项目的自动生成的名称。](./media/azure-ai-foundry-create-project.png)

> **重要说明**：需要在特定位置预配的 Azure AI 服务才能完成实验室的其余工作。

1. 在同一“*创建项目*”窗格中，选择“**自定义**”并选择以下“**位置**”之一：美国东部、法国中部、韩国中部、西欧或美国西部，以完成实验室的其余工作。 然后选择“**创建**”。 

1. 记下所创建的资源： 
- Azure AI 服务
- Azure AI 中心
- Azure AI 项目
- 存储帐户
- 密钥保管库
- 资源组  
 
1. 创建资源后，将转到项目的“*概述*”页。 在屏幕上的左侧菜单中，选择“**AI 服务**”。
 
    ![项目屏幕上左侧菜单的屏幕截图，其中选择了“AI 服务”。](./media/azure-ai-foundry-ai-services.png)  

1. 在“*AI 服务*”页上，选择“*视觉 + 文档*”磁贴以试用 Azure AI 文档智能功能。

    ![在“AI 服务”页上选择的“视觉和文档”磁贴的屏幕截图。](./media/vision-document-tile.png)

## 使用 Azure AI Foundry 中的 Azure AI 文档智能分析收据 

现在，你已准备好分析虚构的 Northwind Traders 零售公司的收据。

1. 在“*视觉 + 文档*”页上，向下滚动并选择“**文档**”。 在“*特定文档的预生成模型*”下，选择“**收据**”磁贴。

1. 在“*试用*”下的下拉列表中，请注意，选择 Azure AI 服务资源。 保留原样。

1. 在计算机上，使用[**https://aka.ms/mslearn-receipt**](https://aka.ms/mslearn-receipt)打开收据的示例图像。 将其保存到 Downloads 文件夹或桌面。 
 
1. 在 Azure AI Foundry 的“*收据*”页上，选择“**浏览文件**”，然后导航到保存图片的文件夹。 选择收据图片，然后选择“打开”****。 图像显示在屏幕左侧。

    ![northwind 收据的屏幕截图。](media/document-intelligence/receipt.jpg)

1. 在右侧，选择“运行分析”****。

1. 分析运行后，将返回结果。 请注意，该服务已识别特定数据字段，例如商家的名称、地址、电话号码和交易日期与时间，以及行项、小计、税费和总金额。 每个字段旁边显示有字段正确的百分比概率。

    ![Azure AI Foundry 门户中收据分析结果的屏幕截图，其中显示数据字段周围的边界框，以及这些提取字段中的文本。](media/receipt-lab-result.png)

在本练习中，你已在 Azure AI Foundry 门户中使用了 Azure AI 文档智能的预生成收据模型。 从返回的结果中，你了解了文档智能如何识别特定字段，从而能够更轻松地处理日常文档中的数据。 在关闭演示之前，何不尝试一些示例收据（包括那些使用不同语言的收据）？

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 [Azure 门户]( https://portal.azure.com)，然后选择包含你所创建的资源的资源组。
1. 选择该资源并选择“删除”，然后选择“是”以******** 进行确认。 这样便会删除该资源。

## 了解详细信息

本练习仅演示了 AI 文档智能服务的部分功能。 若要详细了解此服务的用途，请参阅[文档智能](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview?view=doc-intel-3.1.0)。
