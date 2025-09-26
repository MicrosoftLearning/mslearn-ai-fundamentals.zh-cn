---
lab:
  title: 在 Azure AI Foundry 门户中使用内容理解提取数据
---

# 在 Azure AI Foundry 门户中使用内容理解提取数据

Azure AI 内容理解提供文档、音频文件、视频和图像的多模态分析，用于提取信息。

在本练习中，你将在 Azure AI Foundry 门户（Microsoft 用于创建智能应用程序的平台）中使用 Azure AI 内容理解，从发票中提取数据。 

此练习大约需要 **25** 分钟。

## 创建 Azure AI Foundry 项目进行内容理解

1. 在 Web 浏览器中打开 [Azure AI Foundry 门户](https://ai.azure.com)，网址为：`https://ai.azure.com`，然后使用 Azure 凭据登录。 关闭首次登录时打开的任何使用技巧或快速入门窗格，如有必要，使用左上角的 **Azure AI Foundry** 徽标导航到主页，类似下图所示（若已打开**帮助**面板，请关闭）：

    ![Azure AI Foundry 门户主页的屏幕截图。](./media/ai-foundry-portal.png)

1. 滚动到页面底部，然后选择“浏览 Azure AI 服务”磁贴。****

    ![“浏览 Azure AI 服务”磁贴的屏幕截图。](./media/ai-services.png)

1. 在“Azure AI 服务”页上，选择“试用内容理解”磁贴。****

    ![“试用内容理解”按钮的屏幕截图。](./media/try-content-understanding.png)

1. 在“内容理解”页中，选择“创建要启动的项目”。**** 然后在“创建项目”对话框中，选择建议的资源类型（Azure AI Foundry 资源）：********

    ![分析结果的屏幕截图。](./media/resource-type.png)

1. 在“下一步”页中，输入一个有效的项目名称。**** 然后，选择“高级选项”，并指定以下设置：****
    - **Azure AI Foundry 资源**：*Azure AI Foundry 资源的有效名称*
    - **订阅**：Azure 订阅
    - **资源组**：*创建或选择资源组*
    - 区域****：选择以下位置之一\*：
        * 美国西部
        * 瑞典中部
        * 澳大利亚东部

    \*** 在撰写本文时，内容理解仅在这些区域中可用。

    ![项目设置的屏幕截图。](./media/content-project-settings.png)

1. 选择**创建**。 等待设置过程完成。 可能需要几分钟时间。

## 从发票中提取信息

1. 从 `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf` 中下载 [contoso-invoice-1.pdf](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf)。 

1. 在“内容理解”页上，选择“试用”选项卡，然后选择“发票数据提取”磁贴。********

    ![内容理解“试用”页的屏幕截图。](./media/content-understanding-invoice.png)

    提供了示例发票。

1. 选择示例发票并使用“运行分析”按钮从中提取信息。**** 分析完成后，查看结果。

    ![分析示例发票的结果的屏幕截图。](./media/sample-invoice-analysis.png)

1. 使用“浏览文件”链接上传之前下载的 contoso-invoice-1.pdf 文档，并对该文件运行分析。********

    ![分析 Contoso 发票的结果的屏幕截图。](./media/contoso-invoice-analysis.png)

    请注意，即使此发票的格式与示例不同，内容理解分析器也能够从此发票中提取信息。

1. 在显示所提取字段的右侧窗格中，查看“结果”选项卡，了解将发送到客户端应用程序的 JSON 响应。**** 开发人员将编写代码来处理此响应，并使用提取的字段执行某些操作。

    ![分析 Contoso 发票的结果的屏幕截图。](./media/invoice-analysis-json.png)

## 清理

如果已完成内容理解服务的使用，则应删除在本练习中创建的资源，以避免产生不必要的 Azure 成本。

- 在 Azure 门户中，删除为这些练习创建的资源组。
