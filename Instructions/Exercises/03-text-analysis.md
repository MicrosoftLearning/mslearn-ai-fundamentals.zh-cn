---
lab:
  title: 在 Azure AI Foundry 门户中分析文本
---

# 在 Azure AI Foundry 门户中分析文本

Azure AI 语言包含文本分析，具有实体识别、关键短语提取、摘要和情绪分析等功能。 例如，假设虚构的旅行社 Margie's Travel 鼓励客户提交关于酒店住宿的评价。 可以使用语言服务提取命名实体、识别关键短语、总结文本等。

在本练习中，你将在 Azure AI Foundry 门户（Microsoft 创建智能应用程序的平台）中使用 Azure AI 语言，来分析酒店评论。 

此练习大约需要 **20** 分钟。

## 在 Azure AI Foundry 门户中创建项目

1. 在 Web 浏览器中打开 [Azure AI Foundry 门户](https://ai.azure.com)，网址为：`https://ai.azure.com`，然后使用 Azure 凭据登录。 关闭首次登录时打开的任何使用技巧或快速入门窗格，如有必要，使用左上角的 **Azure AI Foundry** 徽标导航到主页，类似下图所示（若已打开**帮助**面板，请关闭）：

    ![Azure AI Foundry 门户主页的屏幕截图。](./media/ai-foundry-portal.png)

1. 滚动到页面底部，然后选择“浏览 Azure AI 服务”磁贴。****

    ![“浏览 Azure AI 服务”磁贴的屏幕截图。](./media/ai-services.png)

1. 在 Azure AI 服务页上，选择“语言 + 翻译器”磁贴。****

    ![“语言 + 翻译器”磁贴的屏幕截图。](./media/language-tile.png)

1. 在“语言 + 翻译器”页上，选择“试用语言操场”。******** 然后，根据提示，使用以下设置创建一个新项目：
    - 项目名称****：输入有效的项目名称。**
    - 高级设置****：
        - **订阅**：Azure 订阅
        - **资源组**：*创建或选择资源组*
        - 区域****：选择任意一个“AI Foundry 推荐”区域******
        - AI Foundry 或 Azure OpenAI**** *使用有效的名称创建新的 Azure AI Foundry 资源*

1. 选择**创建**。 等待创建项目。 可能需要几分钟时间。

1. 项目创建完成后，你将转到一个“语言”操场（如果不是，请在左侧的任务窗格中选择“操场”，并从那里打开“语言”操场。）********

    语言操场是一个用户界面，可用于试用一些 Azure AI 语言功能。  

## 使用 Azure AI 语言分析文本

Azure AI 语言提供广泛的文本分析功能。

### 在 Azure AI Foundry 门户中使用 Azure AI 语言提取命名实体

*命名实体*是描述具有适当名称的人员、地点和对象的字词。 让我们使用 Azure AI 语言的命名实体提取功能来识别评论中的信息类型。

1. 在语言操场中，选择“**提取信息**”。 然后选择“**提取命名实体**”磁贴。 

1. 在“示例”下，输入以下评价：**

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. 选择**运行**。 查看输出。

    ![“语言”操场中“提取命名实体”界面的屏幕截图。](./media/entity-extraction.png)

    请注意，在“*详细信息*”部分中，提取的实体如何附带其他信息，例如类型和置信度分数。 置信度分数表示标识的类型实际上属于该类别的可能性。

### 在 Azure AI Foundry 门户中使用 Azure AI 语言提取关键短语

*关键短语*是文本中最重要的信息片段。 让我们使用 Azure AI 语言的关键短语提取功能从评论中提取重要信息。

1. 在语言操场中，选择“**提取信息**”。 然后选择“**提取关键短语**”磁贴。 

1. 在“示例”下，输入以下评价：**

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. 选择**运行**。 查看输出。

    ![“语言”操场中“提取关键短语”界面的屏幕截图。](./media/key-phrases.png)

    请注意“*详细信息*”部分中提取的不同短语。 这些短语应最能体现文本的含义。

### 在 Azure AI Foundry 门户中使用 Azure AI 语言总结文本
 
让我们看看 Azure AI 语言的摘要功能。

1. 在语言操场中，选择“**总结信息**”，然后选择“**总结文本**”磁贴。

1. 在“示例”下，输入以下评价：**
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. 选择**运行**。 查看输出。

    ![“语言”操场中“汇总文本”界面的屏幕截图。](./media/summarize-text.png)

    请注意“*详细信息*“中的”*提取摘要*“为最突出的句子提供排名分数。

### 分析文本中的情绪

情绪分析是分析酒店评价等文本时的常见任务。

1. 在“语言”操场中，选择“对文本进行分类”。**** 然后选择“分析情绪”磁贴。****

1. 在“示例”下，输入以下评价：**
    
    ```
    Disappointing Stay at The City Hotel
    The City Hotel, London
    9/5/2018
    My experience at The City Hotel in London was far from pleasant. The constant noise from nearby train tracks made it nearly impossible to sleep, with vibrations felt throughout the building. The rooms were outdated, dusty, and poorly maintained—dripping faucets, squeaky beds, and broken fixtures were just the beginning. Sound insulation was nonexistent, so every conversation from neighboring rooms was clearly audible. While the location near public transport was convenient and the staff were friendly, these positives couldn't make up for the overall discomfort and lack of value. I wouldn’t recommend this hotel to anyone seeking a restful or enjoyable stay.
    ```

1. 选择**运行**。 查看输出。

    ![“语言”操场中“情绪分析”界面的屏幕截图。](./media/sentiment-analysis.png)

    请注意，分析会为每个句子生成一个整体情绪分数和单个分数。

## 检测语言和翻译文本

Azure AI 语言可检测编写文本所用的语言。 此外，使用 Azure AI 翻译，可以轻松地将文本从一种语言翻译成另一种语言。

### 检测语言

首先，我们来检测编写评价所用的语言。

1. 在“对文本进行分类”窗格中，选择“检测语言”磁贴。********

1. 在“示例”下，输入以下评价：**
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. 选择**运行**。 查看输出。

    ![“语言”操场中“检测语言”界面的屏幕截图。](./media/detect-language.png)

    请注意，语言被检测为法语。 

### 翻译文本

现在，我们将法语评价翻译成英语。

1. 在页面顶部，使用“语言操场”页标题旁边的 &larr;（后退）链接查看所有可用的操场。********
1. 在操场列表中，打开“翻译操场”****。
1. 在“翻译”操场中，选择“文本翻译”。****
1. 在“配置”窗格中，选择以下语言选项：****
    - 源语言****：法语
    - 目标语言****：英语
1. 在“示例”下，输入法语评价：**
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. 选择“翻译”。**** 查看输出。

    ![“翻译”操场中“文本翻译”界面的屏幕截图。](./media/text-translation.png)

    请注意，法语评价将翻译成英语。

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 **Azure 门户** ([https://portal.azure.com](https://portal.azure.com))，然后选择包含你所创建的资源的资源组。
1. 选择“删除资源组”，然后输入资源组名称进行确认********。 这样便会删除该资源组。

## 了解详细信息

要详细了解此服务的用途，请参阅[语言服务页面](https://learn.microsoft.com/azure/ai-services/language-service/overview)。
