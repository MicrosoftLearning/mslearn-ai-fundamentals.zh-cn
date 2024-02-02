---
lab:
  title: 使用 Language Studio 分析文本
---

# 使用 Language Studio 分析文本

在本练习中，你将通过分析一些示例酒店评价来探索 Azure AI 语言服务的功能。 你将使用 Language Studio 来了解这些评价大多是正面还是负面的。

自然语言处理 (NLP) 是 AI 的一个分支，用于处理手写以及口头语言。 你可以使用 NLP 来生成从文本或语音中提取语义含义或使用自然语言制作合理响应的解决方案。

例如，假设虚构的旅行社 Margie's Travel 鼓励客户提交关于酒店住宿的评价。 你可使用语言服务来识别关键短语，确定哪些评价是正面的，哪些是负面的，或者分析评价文本提到的已知实体（如位置或人员）。

Azure AI 语言服务包括文本分析和 NLP 功能。 其中包括识别文本中的关键短语，以及基于情绪的文本分类。

## 创建“语言”资源**

你可以将许多 Azure AI 语言功能与语言资源或 Azure AI 服务******** 资源配合使用。 在某些情况下，只能使用语言资源。 对于下面的练习，我们将使用语言**** 资源。 如果尚未这样做，可在 Azure 订阅中创建“语言”资源****。

1. 在另一个浏览器标签页中，打开 Azure 门户 ([https://portal.azure.com](https://portal.azure.com?azure-portal=true))，并使用与 Azure 订阅关联的 Microsoft 帐户登录。

1. 单击“&#65291; 创建资源”按钮，然后搜索“语言服务”******。 选择创建“语言服务”计划********。 你将转到相应页面以“选择其他功能”****。 保留默认选择，然后单击“继续创建资源”****。 

1. 在“创建语言”**** 页面上，使用以下设置对其进行配置：
    - **订阅**：Azure 订阅。
    - **资源组**：选择或创建具有唯一名称的资源组。
    - 区域****：美国东部。
    - **名称**：输入唯一名称。
    - **定价层**：“免费 F0”或“S”（如果“免费 F0”不可用）**
    - “选中此框即表示我确认我已阅读并理解以下所有条款”****：“已选择”**。

1. 依次选择“查看 + 创建”和“创建”，然后等待部署完成********。

## 在 Azure AI Language Studio 中配置资源

1. 在另一个浏览器标签页中，打开 Language Studio ([https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true)) 并登录。****

1. 当系统提示“选择 Azure 资源”**** 时，请进行以下配置：
    - “Azure 目录”****：默认目录，即正在使用的目录**
    - Azure 订阅****：选择要使用的订阅**
    - 资源语言****
    - “资源名称”：选择刚刚创建的语言资源******

然后选择“完成”。

> **重要说明**：截至 2023 年 7 月，Azure AI 服务包含以前称为认知服务和 Azure 应用 AI 服务的服务。 某些用户界面仍在将指称从 `Cognitive Services` 更新为 `Azure AI services`。 这两个名称指的是同一类型的资源。

> **注意**：如果系统未提示你选择语言资源，原因可能是订阅中有多个语言资源；在这种情况下，你应该******：
> 1. 在页面顶部的栏中，选择“设置(&#9881;)”****。 
> 1. 在“设置”页上，查看“资源”选项卡。
> 1. 选择刚刚创建的资源，然后选择“切换资源”****。 确保托管标识“已启用”****。
> ![启用语言资源。](media/analyze-text-language-service/language-resource-enabled.png)
> 1. 在页面顶部，选择“Language Studio”**** 以返回到 Language Studio 主页。

## 在 Language Studio 中分析评价

1. 在 Web 浏览器中，导航到 Language Studio ([https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true))****。

1. 在“欢迎使用 Language Studio”登陆页上，选择“对文本进行分类”选项卡，然后选择“分析情绪和挖掘观点”************ 磁贴。

1. 在“选择文本语言”下，选择“英语”******。

1. 在“选择 Azure 资源”下，选择资源。**

1. 在“输入自己的文本、上传文件或使用我们的示例文本之一”**，复制并粘贴以下评价：

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. 选中此框以确认了解演示会产生使用量，并可能产生费用，然后选择“运行”****。

1. 查看输出。 请注意，系统会分析文档的情绪以及每个句子****。 选择句子 1**** 以显示该句子的情绪分析。 

请注意，有一个总体情绪，后跟三个类别的分数：正面分数、中性分数、负面****** 分数。 在每个类别中，提供介于 0 和 1 之间的分数。 这些置信度分数表示提供的文本归入特定情绪的可能性。 

再次选择句子 1**** 以关闭。

1. 向上滚动以选择“清空文本框”****，然后复制并粘贴以下评价：

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```
    
    
1. 选择**运行**。 查看输出并查看情绪和置信度水平。

1. 再次选择“清空文本框”****，然后复制并粘贴以下评价：

    >非常吵闹，房间很小 美国旧金山 Lombard 酒店 2018/9/5 酒店位于 Lombard 街，这是一个非常繁忙的六车道街道，直通金门大桥。 从清晨到深夜一直车来车往，尤其是周末。 如果房间有更好的隔音，噪声就不会那么吵，但事实并非如此。 我得把棉球塞进耳朵里才能睡着，导致我第二天累到无法好好游玩城市。 房间非常小。 我选择这个房间是因为里面有两张双人床，但房间里几乎没有空间放这两张床。 四个家庭成员在这个房间里显得很挤。 尽管如此，房间还是很干净的，他们也在努力对房间进行更新。 酒店位于 Marina 地区，那里有很多好吃的地方，步行就能到达 Presidio。 对于有预算安排的年轻熬夜成年人来说，这可能是个不错的酒店

1. 选择“运行”****，同时查看情绪和置信度水平。 查看文本并将文本与服务返回的情绪分析进行比较。

在本练习中，你使用 Language Studio 创建新的语言资源或使用现有的语言资源。 在试用情绪和观点挖掘服务之前，你在“设置”中启用了相应资源。 然后，使用三段文本测试该服务。

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 Azure 门户 ([https://portal.azure.com](https://portal.azure.com)****)，然后选择包含你所创建的资源的资源组。
1. 选择该资源并选择“删除”，然后选择“是”以******** 进行确认。 这样便会删除该资源。

## 了解详细信息

要详细了解此服务的用途，请参阅[语言服务页面](https://learn.microsoft.com/azure/ai-services/language-service/overview)。
