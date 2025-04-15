---
lab:
  title: 探索 Azure AI Foundry 门户中的生成式 AI
---

# 探索 Azure AI Foundry 门户中的生成式 AI

生成式 AI 描述 AI 中用于创建内容的一类功能。 人员通常与聊天应用程序中内置的生成式 AI 交互。 在本练习中，你将试用 Azure AI Foundry 门户（Microsoft 创建智能应用程序的平台）中的生成式 AI。 

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
 
1. 创建资源后，将转到项目的“*概述*”页。 在屏幕左侧菜单中，选择“**操场**”。
 
    ![项目屏幕上左侧菜单的屏幕截图，其中选择了“AI 服务”。](./media/azure-ai-foundry-playgrounds.png)  

## 在 Azure AI Foundry 的聊天操场中探索生成式 AI

1. 在 Azure AI Foundry 的“操场”页中，选择“**试用聊天操场**”。 聊天操场是一个用户界面，可用于尝试使用不同的生成式 AI 模型构建聊天应用程序。  

1. 若要使用聊天操场，需要将其与已部署的模型相关联。 在“聊天操场”中，选择“**创建部署**”。 搜索并选择 **gpt-4**。 

1. 在“*部署模型*”窗口中，保留默认命名和选择，然后选择“**部署**”。 模型可能需要一些时间才能部署。 可以通过在“*我的资产*”下的左侧菜单中选择 *“模型”和“终结点”*，来检查部署的状态。
1. 在聊天操场中，可以在“*部署*”选择菜单中显示已部署的模型时使用该模型。 确保选择已部署的模型。 重要的是，在对“*设置*”进行任何更改后，需要选择“**应用更改**”。 

1. 请考虑通过以下方法改进来自生成式 AI 助手的响应：
    - 从希望助手执行的具体目标开始
    - 根据先前的提示和响应进行迭代以完善结果
    - 提供一个来源，用于在特定信息范围内为响应打好基础
    - 添加上下文以最大限度地提高响应的适当性和相关性
    - 为响应设定明确的期望

1. 让我们尝试使用具有特定目标的提示生成响应。 在“聊天”框中，输入以下提示：

    ```prompt
    I'm planning a trip to Paris in September. Can you help me?
    ```

1. 查看回应。 **备注**：请记住，收到的特定响应可能因生成式 AI 的性质而异。
 
1. 让我们尝试另一个提示： 输入以下内容：

    ```prompt
    Where's a good location in Paris to stay? 
    ```

1. 查看响应，其中应提供巴黎的一些住宿地点。

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

1. 完成后，可以关闭浏览器窗口。