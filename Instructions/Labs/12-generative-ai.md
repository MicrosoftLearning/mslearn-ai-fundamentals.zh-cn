---
lab:
  title: 使用 Microsoft Copilot 探索生成式 AI
---
# 使用 Microsoft Copilot 探索生成式 AI

在本练习中，你将使用 Microsoft Copilot 探索生成式 AI。 

## 登录到 Microsoft Copilot

1. 打开 [copilot.microsoft.com](https://copilot.microsoft.com?azure-portal=true) 并使用个人 Microsoft 帐户登录。

1. Microsoft Copilot 使用生成式 AI 来增强必应搜索结果。 这意味着，与仅返回现有内容的搜索不同，Microsoft Copilot 可以基于自然语言建模和 Web 信息整合新的响应。  

1. 在屏幕底部，你将看到一个窗口“**向我提问吧**”。 在窗口中输入提示时，Copilot 会基于整个对话线程来返回响应。 例如，我们可以尝试提出一系列有关旅行的问题。

## 使用提示生成响应

1. 键入提示：`What are 3 pros and cons of traveling in the winter?`。 系统将在响应前显示“*正在搜索...* ”和“*正在生成...* ”。 该模型使用搜索的响应作为基础信息来生成原始响应。 请注意，响应末尾包含指向其来源的链接。 

![Copilot 对旅行提示的响应的屏幕截图，其中以项目符号列表的形式列出了三个优点和三个缺点。](./media/generative-ai/bing-copilot-response-traveling.png) 

> **注意**：如果未看到“正在生成...”消息或项目符号列表形式的响应，则表示 Copilot 尚未运行。** 你需要返回到登录菜单，并使用个人帐户连接正在使用的当前帐户。 
 
1. 键入提示：`Find me 3 more pros`。 你使用此提示的意思是，你希望看到 3 个尚未列出的冬季旅行的 3 个更积极的理由。 请注意，使用此提示，你是在要求 Copilot 执行两项仅凭搜索而无法执行的操作：使用以前的聊天响应排除新响应中返回的内容，以及使用上一个聊天的主题而不明确说明。 

1. 键入提示：`Where are 3 places I can go to find fewer crowds?`。 

    > **注意**：请注意，虽然 Copilot 能够提供相关的响应，但它可能会在继续时丢掉对话线程的早期“记忆”。 因此，你得到的响应可能与冬季旅行没有直接关系。 这在很大程度上与令牌输入限制有关。 当聊天“记住”对话的早期部分时，这是因为它已从对话中保存了一定数量的令牌。 随着新令牌通过新的提示和响应引入，聊天会放弃旧的令牌。 

1. 聊天窗口旁边的“新建主题****”按钮非常有用。 单击该按钮可清除上一个对话线程，从而使新主题响应不再基于上一主题。 使用聊天窗口旁边的“**新建主题**”图标清除消息历史记录。 

## 尝试图像生成

1. 现在，我们来看一个图像生成示例。 键入提示：`Create an image of an elephant eating a hamburger`。 请注意，在 Copilot 返回响应之前，将会显示一条消息“我将尝试创建...”。** 

    ![大象吃火腿汉堡的屏幕截图。](./media/generative-ai/dall-e-elephant.png)

    重要的是，请注意，响应可能看起来相似，但并不相同。 这是因为响应会有变化。  

1. 在响应中，底部会显示“由 DALL-E 提供支持”文本。 在自然语言输入生成图像时，请考虑 DALL-E 是如何基于大语言模型的。 

1. 单击屏幕右上角的 Microsoft 必应图标，即可返回到 Copilot 的聊天。 

## 尝试代码生成

1. 现在，我们来看看代码生成和翻译的示例。 键入提示：`Use Python to create a list`。 

1. 键入提示：`Translate that into C#`。 请注意，由于 Copilot 知道参考对话历史记录，因此你无需指定“那个”是什么。

## 奖励任务

1. 键入提示：`What are 3 examples of generative AI helping people?`。 你可以将它用作一种集思广益的方式，构思你自己的 Copilot 创意！  
