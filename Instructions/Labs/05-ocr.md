---
lab:
  title: 在 Vision Studio 中读取文本
---

# 在 Vision Studio 中读取文本

在本练习中，你将使用 Azure AI 服务探索 Azure AI 视觉的光学字符识别功能。 你将使用 Vision Studio 来试验提取图像中的文本，而无需编写任何代码。

检测和解释图像中嵌入的文本是一个常见的计算机视觉难题。 这称为光学字符识别 (OCR)。 在本练习中，你将使用 Azure AI 服务资源，其中包括 Azure AI 视觉服务。 然后，你将使用 Vision Studio 通过不同类型的图像试用 OCR。

## 创建 Azure AI 服务资源

你可以将 Azure AI 视觉的 OCR 功能与 Azure AI 服务的多服务资源配合使用。**** 在 Azure 订阅中创建一个 Azure AI 服务资源（如果尚未这样做）。

1. 在另一个浏览器标签页中，打开 Azure 门户 ([https://portal.azure.com](https://portal.azure.com?azure-portal=true))，并使用与 Azure 订阅关联的 Microsoft 帐户登录。****

1. 单击“&#65291;创建资源”按钮，然后搜索“Azure AI 服务”。 选择创建 Azure AI 服务计划。 随后你会转到一个页面，可在其中创建 Azure AI 服务资源。 使用以下设置对其进行配置：
    - **订阅**：Azure 订阅。
    - **资源组**：选择或创建具有唯一名称的资源组。
    - 区域****：美国东部。
    - **名称**：输入唯一名称。
    - **定价层**：*标准 S0。*
    - “选中此框即表示我确认我已阅读并理解以下所有条款”****：“已选择”**。

1. 依次选择“查看 + 创建”和“创建”，然后等待部署完成********。

## 将 Azure AI 服务资源连接到 Vision Studio

接下来，将上面预配的 Azure AI 服务资源连接到 Vision Studio。

1. 在另一个浏览器标签页中，导航到 Vision Studio ([https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com?azure-portal=true))。****

1. 使用帐户登录，并确保使用的目录与已创建 Azure AI 服务资源的目录相同。

1. 在 Vision Studio 主页上，选择“视觉入门”标题下的“查看所有资源”********。

    ![“查看所有资源”链接在 Vision Studio 中的“视觉入门”下突出显示。](./media/analyze-images-vision/vision-resources.png)

1. 在“选择要处理的资源”页面上，将鼠标光标悬停在你前面在列表中创建的资源上，并选中资源名称左侧的框，然后选择“选择作为默认资源”。********

    > **注意**：如果未列出你的资源，可能需要刷新**** 页面。

    ![系统会显示“选择要处理的资源”对话，并在其中突出显示并选中 cog-ms-learn-vision-SUFFIX 认知服务资源。 此时会突出显示“选择作为默认资源”按钮。](./media/analyze-images-vision/default-resource.png)

1. 通过选择屏幕右上角的“x”关闭设置页面。

## 在 Vision Studio 中提取图像中的文本
    
1. 在 Web 浏览器中，导航到 Azure 门户 ([https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com?azure-portal=true))****。

1. 在“视觉入门”登陆页上，选择“光学字符识别”，然后选择“提取图像中的文本”磁贴。************

1. 在“试用”子标题下，通过阅读并选中对应的框来确认资源使用策略。****  

1. 选择 [https://aka.ms/mslearn-ocr-images****](https://aka.ms/mslearn-ocr-images) 以下载 ocr-images.zip****。 然后打开文件夹。

1. 在门户中，选择“浏览文件”，然后导航到计算机上下载了 ocr-images.zip 的文件夹。******** 选择“advert.jpg”，然后选择“打开”********。

1. 现在查看返回的内容：
    - 在“检测到的属性”中，图像中找到的任何文本都将组织成区域、线条和字词的分层结构。****
    - 在图像中，文本的位置由范围框指示，如下所示：

    ![图像中概述的文本的图像](media/read-text-computer-vision/text-bounding-boxes.png)

1. 现在可以尝试另一个图像。 选择“浏览文件”，然后导航到保存来自 GitHub 的文件的文件夹。**** 选择“letter.jpg”****。

    ![类型化字母的图像。](media/read-text-computer-vision/letter.jpg)

1. 查看第二张图像的结果。 它应返回文本和文本和范围框。 如果你有时间，可尝试 note.jpg 和 receipt.jpg。********

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 Azure 门户 ([https://portal.azure.com](https://portal.azure.com?azure-portal=true)****)，然后选择包含你所创建的资源的资源组。
1. 选择该资源并选择“删除”，然后选择“是”以******** 进行确认。 这样便会删除该资源。

## 了解详细信息

若要详细了解此服务的用途，请参阅有关[光学字符识别](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-ocr)的 Azure AI 视觉文档。
