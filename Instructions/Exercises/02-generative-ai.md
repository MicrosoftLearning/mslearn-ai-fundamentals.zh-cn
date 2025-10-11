---
lab:
  title: 探索 Azure AI Foundry 门户中的生成式 AI
---

# 在 Azure AI Foundry 门户中探索生成式 AI

生成式 AI 描述 AI 中用于创建内容的一类功能。 人们经常与聊天应用程序中内置的生成式 AI 交互。 在本练习中，你将试用 Azure AI Foundry 门户（Microsoft 创建智能应用程序的平台）中的生成式 AI。 

此练习大约需要 **20** 分钟。

## 在 Azure AI Foundry 门户中创建项目

1. 在 Web 浏览器中打开 [Azure AI Foundry 门户](https://ai.azure.com)，网址为：`https://ai.azure.com`，然后使用 Azure 凭据登录。 关闭首次登录时打开的任何使用技巧或快速入门窗格，如有必要，使用左上角的 **Azure AI Foundry** 徽标导航到主页，类似下图所示（若已打开**帮助**面板，请关闭）：

    ![Azure AI Foundry 门户主页的屏幕截图。](./media/ai-foundry-portal.png)

1. 在“浏览模型和功能”部分中，搜索 `gpt-4o`。**** 然后，在搜索结果中，选择 gpt-4o 模型以查看其详细信息。****

    ![gpt-4o 详细信息页的屏幕截图。](./media/gpt-4o-details.png)

1. 选择“使用此模型”****。

1. 在“**创建项目**”向导中，输入项目有效名称。 然后，展开“高级选项”，为项目指定以下设置：****
    - Azure AI Foundry 资源：**** 输入有效的 AI Foundry 资源名称。**
    - **订阅**：Azure 订阅
    - **资源组**：*创建或选择资源组*
    - 区域****：选择任意一个“AI Foundry 推荐”区域****\*
    
    \**模型部署受区域配额的限制。如果选择了可用配额不足的区域，以后可能需要为新资源选择一个备用区域。*

1. 选择**创建**。 等待创建项目。 可能需要几分钟时间。

    如果系统提示将模型部署到其他区域，请使用默认设置执行此操作。

## 在 Azure AI Foundry 的聊天操场中探索生成式 AI

1. 创建项目后，在左侧的任务窗格中，选择“操场”。**** 

    >*提示*：如有必要，单击顶部的“展开”图标，展开菜单以阅读其内容。

1. 在 Azure AI Foundry 的“操场”页中，选择“**试用聊天操场**”。 关闭打开的所有提示或快速入门窗格。

    聊天操场是一个用户界面，可用于尝试使用不同的生成式 AI 模型构建聊天应用程序。

    ![gpt-4o 详细信息页的屏幕截图。](./media/chat-playground.png)

    >*提示*：如果未在“聊天操场”屏幕上看到“设置”窗格，请扩展窗口大小。****  

1. 若要使用聊天操场，需要将其与已部署的模型相关联。 在“聊天操场”的“设置”窗格中，确认已选择先前部署的 gpt-4o 模型。******** 

    >*注意*：每次在“设置”窗格中进行更改后，都需要选择“应用更改”。********

1. 在“设置”窗格中，记下模型的默认说明和上下文信息，应类似于：****

    `You are an AI assistant that helps people find information.`

    这些类型的指令通常称为系统提示**，用于为模型的响应提供指导和约束。

1. 查看“聊天历史记录”窗格，其中包含一些可帮助你开始使用的示例提示，还有一个用于你输入自己的提示的查询框。** 

1. 让我们尝试使用具有特定目标的提示生成响应。 在“聊天”框中，输入以下提示：

    ```prompt
    I'm planning a trip to Paris in September. Can you help me?
    ```

1. 查看回应。 请注意，你收到的具体响应可能因生成式 AI 的性质而异。

1. 让我们尝试另一个提示： 输入以下内容：

    ```prompt
    Where's a good location in the city to stay?
    ```

1. 查看响应，其中应提供巴黎的一些住宿地点。 请注意，聊天会话会保留先前提示的上下文，因此它知道所说的“城市”是巴黎。

1. 根据先前的提示和响应进行迭代，以优化结果。 输入以下提示：

    ```prompt
    Can you give me more information about dining options near the first location?
    ```

1. 查看响应，该响应应提供上一响应中某个位置附近的餐饮选项。 

1. 现在，让我们提供一个来源，用于在特定信息范围内为响应打好基础。 输入以下内容： 

    ```prompt
    Based on the information at https://en.wikipedia.org/wiki/History_of_Paris, what were the key events in the city's history?
    ```

1. 查看响应，该响应应基于提供的网站提供信息。 

1. 让我们尝试添加上下文，以最大化响应的相关性。 输入以下提示： 

    ```prompt
    What three places do you recommend I stay in Paris to be within walking distance to historical attractions? Explain your reasoning.
    ```

1. 查看响应及其推理。  

1. 现在为响应设定明确的期望。 输入以下提示：

    ```prompt
    What are the top 10 sights to see in Paris? Answer with a numbered list in order of popularity.
    ```

1. 查看响应，该响应应提供一个在巴黎看到的景点编号列表。

## 查看客户端代码

1. 在“聊天操场”页的顶部，选择“查看代码”。****
1. 查看为多种编程语言、SDK 和身份验证选项提供的代码示例。

    当开发人员在生成与已部署模型聊天的客户端应用程序时，这些代码示例可帮助他们快速开始。

1. 关闭示例代码窗口。

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 **Azure 门户** ([https://portal.azure.com](https://portal.azure.com))，然后选择包含你所创建的资源的资源组。
1. 选择“删除资源组”，然后输入资源组名称进行确认********。 这样便会删除该资源组。
