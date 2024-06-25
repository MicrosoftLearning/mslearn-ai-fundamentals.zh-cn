---
lab:
  title: 在 Vision Studio 中检测人脸
---

# 在 Vision Studio 中检测人脸

视觉解决方案通常需要 AI 能够检测人脸。 例如，假设虚构的零售公司 Northwind Traders 想要定位顾客在商店中的站立位置，以为其提供最佳帮助。 完成此任务的一种方法是确定图像中是否有人脸，如果有，则返回显示其位置的范围框坐标。

若要测试 Azure AI 人脸服务的人脸检测功能，可使用 [Azure Vision Studio](https://portal.vision.cognitive.azure.com/)。 这是一个基于 UI 的平台，可用于探索 Azure AI 视觉功能，而无需编写任何代码。

## 创建 Azure AI 服务资源

你可以将 Azure AI 人脸服务与 Azure AI 服务的多服务资源配合使用。**** 在 Azure 订阅中创建一个 Azure AI 服务资源（如果尚未这样做）。

1. 在另一个浏览器标签页中，打开 Azure 门户 ([https://portal.azure.com](https://portal.azure.com?azure-portal=true))，并使用与 Azure 订阅关联的 Microsoft 帐户登录。

1. 单击“&#65291;创建资源”按钮，然后搜索“Azure AI 服务”。 选择创建 Azure AI 服务计划。 随后你会转到一个页面，可在其中创建 Azure AI 服务资源。 使用以下设置对其进行配置：
    - **订阅**：Azure 订阅。
    - **资源组**：选择或创建具有唯一名称的资源组。
    - 区域****：选择离你最近的地理区域。** 如果在美国东部，请使用“美国东部 2”。
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

## 在 Vision Studio 中检测人脸 

1. 在 Web 浏览器中，导航到 Azure 门户 ([https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com?azure-portal=true))****。

1. 在“视觉入门”登陆页上，选择“人脸”选项卡，然后选择“检测图像中的人脸”磁贴。************

1. 在“试用”子标题下，通过阅读并选中对应的框来确认资源使用策略。****  

1. 选择每个示例图像并观察返回的人脸检测数据。

1. 现在，让我们尝试一些自己的图像。 选择 [https://aka.ms/mslearn-detect-faces****](https://aka.ms/mslearn-detect-faces) 以下载 detect-faces.zip****。 然后打开计算机上的相应文件夹。

1. 找到名为“store-camera-1.jpg”的文件，其中包含下图：****

    ![人们在商店中的图像。](./media/create-face-solutions/store-camera-1.jpg)

1. 上传 store-camera-1.jpg 并查看返回的人脸检测详细信息。****

1. 找到名为“store-camera-2.jpg”的文件，**** 其中包含下图：

    ![更多人在商店中的图像。](./media/create-face-solutions/store-camera-2.jpg)

1. 上传 store-camera-2.jpg 并查看返回的人脸检测详细信息。****

1. 找到名为“store-camera-3.jpg”的文件，其中包含下图：****

    ![人们在商店中的图像，其中有植物遮挡了人脸。](./media/create-face-solutions/store-camera-3.jpg)

1. 上传 store-camera-3.jpg 并查看返回的人脸检测详细信息。**** 请注意 Azure AI 人脸没有检测到被遮盖的人脸。

在本练习中，你了解了 Azure AI 服务如何检测图像中的人脸。 如果有时间，可以随意尝试示例图像或某些自己的图像。

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 Azure 门户 ([https://portal.azure.com](https://portal.azure.com?azure-portal=true)****)，然后选择包含你所创建的资源的资源组。
1. 选择该资源并选择“删除”，然后选择“是”以******** 进行确认。 这样便会删除该资源。

## 了解详细信息

若要详细了解此服务的用途，请参阅 [Azure AI 人脸服务页面](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-identity)。
