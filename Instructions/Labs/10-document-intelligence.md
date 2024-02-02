---
lab:
  title: 在 Document Intelligence Studio 中提取表单数据
---

# 在 Document Intelligence Studio 中提取表单数据

Azure AI 文档智能能够分析和提取表单和文档中的信息，然后标识字段名称和数据。 

文档智能是如何建立在光学字符识别 (OCR) 之上的？ 虽然 OCR 可以读取打印文档或手写文档，但 OCR 是以非结构化格式提取文本，这很难存储在数据库中或用于进行分析。 文档智能通过捕获文本的结构（如键/值对和表中的信息）来帮助理解非结构化数据。 

在本练习中，你将了解文档智能中的预生成模型，该模型经过训练以识别收据中的数据。 

> 注意：**** Azure AI 文档智能是 Azure 表单识别器的新名称。 你仍可在 Azure 门户或 Document Intelligence Studio 中看到 Azure 表单识别器。

## 创建** 文档智能资源

你可以通过创建文档智能资源或 Azure AI 服务资源来使用 Azure AI 文档智能****。 在本练习中，你将创建** 文档智能资源（如果你还没有文档智能资源）。

1. 在另一个浏览器标签页中，打开 Document Intelligence Studio，并使用 Microsoft 帐户登录。[](https://formrecognizer.appliedai.azure.com/studio)
1. 选择“设置”，然后选择“资源********”选项卡。选择“创建新资源”****。
1. 在“创建资源”对话框中，输入以下内容：
    - **订阅**：Azure 订阅。
    - **资源组**：选择或创建具有唯一名称的资源组。
    - “新资源名称”****：输入一个唯一名称**。
    - 位置****：选择区域**。
    - **定价层**：“免费 F0”（如果不可用，请选择“标准 SO”）**。
1. 选择“继续”，然后选择“完成”********。 等待资源部署完毕。

    >注意：如果未显示你的资源，你可能需要刷新******** 页面。

使 Document Intelligence Studio 保持打开状态。

## 在 Document Intelligence Studio 中分析收据

现在，你已准备好分析虚构的 Northwind Traders 零售公司的收据。

1. 选择 [https://aka.ms/mslearn-receipt****](https://aka.ms/mslearn-receipt) 以将示例文档下载到计算机。 打开  文件夹。 
1. 选择“Form Recognizer Studio”以返回到“开始使用 Document Intelligence Studio”页面，然后在“收据”下选择“试用****。********
1. 在“预生成”下拉列表中，确保选中“收据”****。
1. 选择“浏览文件”，然后导航到保存相应图片的文件夹。**** 选择收据图片，然后选择“打开”****。 图像显示在屏幕左侧。

    ![Northwind 收据。](media/document-intelligence/northwind-receipt.jpg)

1. 在右侧，选择“运行分析”****。
1. 分析运行后，将返回结果。 请注意，该服务已识别特定数据字段，例如商家的名称、地址、电话号码和交易日期与时间，以及行项、小计、税费和总金额。 每个字段旁边显示有字段正确的百分比概率。

在本练习中，你已使用 Document Intelligence Studio 创建文档智能资源。 然后，你使用该服务分析了一张收据。 从返回的结果中，你了解了文档智能如何识别特定字段，从而能够更轻松地处理日常文档中的数据。 在关闭 Document Intelligence Studio 之前，何不尝试一些示例收据（包括那些使用不同语言的收据）？

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 [Azure 门户]( https://portal.azure.com)，然后选择包含你所创建的资源的资源组。
1. 选择该资源并选择“删除”，然后选择“是”以******** 进行确认。 这样便会删除该资源。

## 了解详细信息

本练习仅演示了 AI 文档智能服务的部分功能。 若要详细了解此服务的用途，请参阅[文档智能](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview?view=doc-intel-3.1.0)。
