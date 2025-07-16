---
lab:
  title: 在 Azure AI Foundry 门户中分析文本
---

# 在 Azure AI Foundry 门户中分析文本

自然语言处理 (NLP) 是 AI 的一个分支，用于处理手写以及口头语言。 你可以使用 NLP 来生成从文本或语音中提取语义含义或使用自然语言制作合理响应的解决方案。

Azure AI 语言服务包含文本分析，具有实体识别、关键短语提取、摘要和情绪分析等功能。 例如，假设虚构的旅行社 Margie's Travel 鼓励客户提交关于酒店住宿的评价。 可以使用语言服务提取命名实体、识别关键短语、总结文本等。

在本练习中，你将在 Azure AI Foundry 门户（Microsoft 创建智能应用程序的平台）中使用 Azure AI 语言，来分析酒店评论。 

## 在 Azure AI Foundry 门户中创建项目

1. 在 Web 浏览器中打开 [Azure AI Foundry 门户](https://ai.azure.com)，网址为：`https://ai.azure.com`，然后使用 Azure 凭据登录。 关闭首次登录时弹出的所有提示或快速入门窗格。 

1. 在浏览器中，导航到 `https://ai.azure.com/managementCenter/allResources` 并选择“**创建**”。 然后选择创建*新的 Azure AI Foundry 资源*的选项。

1. 在“*创建项目*”向导中，输入项目有效名称。

1. 展开“*高级选项*”，为你的项目指定以下设置：
    - 订阅：Azure 订阅
    - **资源组**：创建或选择资源组
    - **区域**：请选择以下位置之一：
        * 美国东部
        * 法国中部
        * 韩国中部
        * 西欧
        * 美国西部

    等待创建项目和中心。

1. 创建项目后，你将访问项目详细信息的“*概述*”页。

1. 在屏幕左侧菜单中，选择“**操场**”。

1. 在“*操场*”页上，选择“**语言操场**”磁贴以试用一些 Azure AI 语言功能。

## 在 Azure AI Foundry 门户中使用 Azure AI 语言提取命名实体

*命名实体*是描述具有适当名称的人员、地点和对象的字词。 让我们使用 Azure AI 语言的命名实体提取功能来识别评论中的信息类型。

1. 在语言操场中，选择“**提取信息**”。 然后选择“**提取命名实体**”磁贴。 

1. 在“*示例*”下，复制并粘贴以下评论：

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. 选择**运行**。 查看输出。 请注意，在“*详细信息*”部分中，提取的实体如何附带其他信息，例如类型和置信度分数。 置信度分数表示标识的类型实际上属于该类别的可能性。

## 在 Azure AI Foundry 门户中使用 Azure AI 语言提取关键短语

*关键短语*是文本中最重要的信息片段。 让我们使用 Azure AI 语言的关键短语提取功能从评论中提取重要信息。

1. 在语言操场中，选择“**提取信息**”。 然后选择“**提取关键短语**”磁贴。 

1. 在“*示例*”下，复制并粘贴以下评论：

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. 选择**运行**。 查看输出。 请注意“*详细信息*”部分中提取的不同短语。 这些短语应最能体现文本的含义。

## 在 Azure AI Foundry 门户中使用 Azure AI 语言总结文本
 
1. 让我们看看 Azure AI 语言的摘要功能。 在语言操场中，选择“*总结信息*”，然后选择“**总结文本**”磁贴。

1. 在“*示例*”下，复制并粘贴以下评论：
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. 选择**运行**。 查看输出。 请注意“*详细信息*“中的”*提取摘要*“为最突出的句子提供排名分数。   

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 **Azure 门户** ([https://portal.azure.com](https://portal.azure.com))，然后选择包含你所创建的资源的资源组。

1. 选择该资源并选择“**删除**”，然后选择“**是**”以进行确认。 这样便会删除该资源。

## 了解详细信息

要详细了解此服务的用途，请参阅[语言服务页面](https://learn.microsoft.com/azure/ai-services/language-service/overview)。
