---
lab:
  title: 探索 Azure OpenAI 服务
---

# 探索 Azure OpenAI

Azure OpenAI 服务将 OpenAI 开发的生成式 AI 模型引入 Azure 平台，使你能够开发功能强大的 AI 解决方案，这些解决方案受益于 Azure 云平台提供的服务的安全性、可伸缩性和集成。

在本练习中，你将探索 Azure OpenAI 服务，并使用该服务来部署和试验生成式 AI 模型。

该练习大约需要 25 分钟。

## 准备工作

你将需要一个已被批准访问 Azure OpenAI 服务的 Azure 订阅（针对文本模型、代码模型和 DALL-E 图像生成模型）。

- 若要注册免费的 Azure 订阅，请访问 [https://azure.microsoft.com/free](https://azure.microsoft.com/free)。
- 若要请求访问 Azure OpenAI 服务，请访问 [https://aka.ms/oaiapply](https://aka.ms/oaiapply)。

## 预配 Azure OpenAI 资源

必须先在 Azure 订阅中预配 Azure OpenAI 资源，然后才能使用 Azure OpenAI 模型。

1. 登录到 [Azure 门户](https://portal.azure.com)。
2. 请使用以下设置创建 Azure OpenAI 资源：
    - 订阅****：** 已被批准访问 Azure OpenAI 服务的 Azure 订阅。
    - 资源组****：** 选择现有的资源组，或者用你选择的名称新建一个。
    - 区域****：美国东部\*
    - **名称**：所选项的唯一名称**
    - **定价层**：标准版 S0

    > \* 不同区域的模型有不同的可用性和配额。 在此练习中，您将使用 GPT-35-Turbo 模型生成文字，使用 DALL-E 模型生成图像，这两种模型在美国东部都受支持。 

3. 等待部署完成。 然后在 Azure 门户中转至部署的 Azure OpenAI 资源。

## 探索 Azure OpenAI Studio

你可以使用 Azure OpenAI Studio 在 Azure OpenAI 服务中部署、管理和探索模型。

1. 在 Azure OpenAI 资源的“概述”页上，使用“浏览”按钮在新的浏览器选项卡中打开 Azure OpenAI Studio。或者直接导航到 [Azure OpenAI Studio](https://oai.azure.com/) 。

    首次打开 Azure OpenAI Studio 时，它应如下所示：

    ![Azure OpenAI Studio 的屏幕截图。](./media/generative-ai/ai-studio.png)

1. 查看左侧窗格中显示的页面。 你随时可以返回到顶部的主页。 此外，OpenAI Studio 还提供了多个支持以下操作的页面：
    - 在操场中试验模型。**
    - 管理模型部署和数据。

## 部署用于生成语言的模型

若要试验自然语言生成，则必须先部署一个模型。

1. 在“模型”页面上，查看 Azure OpenAI 服务实例中的可用模型。****
1. 选择“可部署”状态为“是”的任何 gpt-35-turbo 模型，然后选择“部署”****************：

    ![Azure AI Studio 中“模型”页面的屏幕截图。](./media/generative-ai/deploy-model.png)

1. 使用以下设置创建一个新部署：
    - 模型：gpt-35-turbo
    - **模型版本**：自动更新为默认值
    - 部署名称****：模型部署的唯一名称**
    - **高级选项**
        - **内容筛选器**：默认
        - **部署类型**：标准
        - **每分钟令牌速率限制**：5K\*
        - **启用动态配额**：已启用

    > \*每分钟 5,000 个令牌的速率限制足以完成此练习，同时也为使用同一订阅的其他人留出容量。

## 通过“聊天”** 操场使用该模型

现在，你已部署了一个模型，可以在“聊天”** 操场中使用该模型来基于你在聊天界面中提交的提示生成自然语言输出。

1. 在 [Azure OpenAI Studio](https://oai.azure.com/) 中导航到左窗格中的聊天操场。

    “聊天”** 操场提供了聊天机器人界面，你可以在该界面中与已部署的模型进行交互，如下所示：

    ![Azure OpenAI Studio 中“聊天”操场的屏幕截图。](./media/generative-ai/chat-playground.png)

1. 在“配置”**** 窗格中，确保已选择模型部署。
1. 在“助手设置”窗格中，选择“默认”系统消息模板，并查看此模板创建的系统消息。******** 该系统消息将定义模型在聊天会话中的行为方式。
1. 在****“聊天会话”部分中，输入以下用户消息。

    ```
   What is generative AI?
    ```

1. 观察模型返回的输出，该输出应提供生成式 AI 的定义。
1. 输入以下用户消息作为后续问题：

    ```
   What are three benefits it provides?
    ```

1. 查看输出，你会注意到聊天会话一直在跟踪以前的输入和响应以提供上下文（因此它正确地将“它”解读为“生成式 AI”），并且它基于所请求的内容提供合适的响应（它应返回生成式 AI 的三个好处）。

## 使用 DALL-E 操场生成图像**

除了语言生成模型，Azure OpenAI 服务还支持用于生成图像的 DALL-E 2 模型。

> **注意**：你必须在 Azure OpenAI 服务访问应用程序中应用并接收对 DALL-E 功能的访问权限，才能完成本练习的这一部分。

1. 在 [Azure OpenAI Studio](https://oai.azure.com/) 中导航到左窗格中的 DALL-E 操场****。
1. 输入以下提示：

    ```
    A robot eating spaghetti
    ```

1. 选择“生成****”并查看结果，结果应包含一张基于你在提示中提供的说明的图像，如下所示：

    ![Azure OpenAI Studio 中 DALL-E 操场的屏幕截图。](./media/generative-ai/dall-e-playground.png)

1. 通过修改提示生成第二个图像，以便：

    ```
    A robot eating spaghetti in the style of Rembrandt
    ```
1. 验证新图像是否符合提示的要求，如下所示：

    ![Azure OpenAI Studio 中 DALL-E 生成的图像的屏幕截图。](./media/generative-ai/dall-e-results.png)

## 清理

使用完 Azure OpenAI 资源后，请记得在 [Azure 门户](https://portal.azure.com/?azure-portal=true)中删除此次部署或整个资源。
