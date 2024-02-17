---
lab:
  title: 浏览 Speech Studio
---

# 浏览 Speech Studio

Azure AI 语音服务可将语音转换为文本，以及将文本转换为可听语音。**** 你可以使用 AI 语音创建一个应用程序，该应用程序可以转换会议笔记或基于采访录音生成文本。

在本练习中，你将使用 Azure AI Speech Studio 试用 Azure AI 语音服务的功能。 

## 创建 Azure AI 语音资源**

可以通过创建语音**** 资源或 Azure AI 服务**** 资源来使用语音服务。

在本练习中，你将创建 AI 语音资源（除非已有一个可以使用的资源）。

1. 在另一个浏览器标签页中，打开 Azure AI Speech Studio，并使用 Microsoft 帐户登录。[](https://speech.microsoft.com/)

1. 依次选择“设置”和“创建资源”********。 使用以下设置对其进行配置：
    - “新资源的名称”****：输入一个唯一名称**。
    - **订阅**：Azure 订阅。
    - 区域****：** 选择[支持的区域](https://learn.microsoft.com/azure/ai-services/speech-service/regions)。
    - **定价层**：“免费 F0”（如果不可用，请选择“标准 S0”）**。
    - **资源组**：选择或创建具有唯一名称的资源组。
1. 选择“创建资源”****。 等待资源创建完毕，然后选择“使用资源****”。 此时将显示“语音入门”页面。

## 在 Speech Studio 中探索语音转文本功能

1. 选择 [https://aka.ms/mslearn-speech-files****](https://aka.ms/mslearn-speech-files) 以下载 speech.zip。**** 打开  文件夹。 

1. 在“语音入门”页面上的“语音转文本”下，查找“实时语音转文本”****。 选择“试用实时语音转文本功能”****。

    ![语音入门](media/recognize-synthesize-speech/try-out-speech-to-text.png)

1. 在“选择音频文件”下，选择“浏览文件”并导航到保存相应文件的文件夹。****** 选择 WhatAICanDo.m4a，然后选择********“打开”。

    ![浏览文件](media/recognize-synthesize-speech/browse-files-speech.png)

1. 语音服务将实时听录和显示文本。 如果你的计算机上有音频，你可以在转换文本的同时听录音。
1. 查看输出，该输出应已成功识别音频并将其听录为文本。

    > 注意：**** 如果收到错误消息，请等待几分钟，然后再重试。 语音资源首次使用时会需要一些时间。

在本练习中，你在 Speech Studio 中创建了一个 AI 语音资源。 然后，使用实时语音转文本服务来听录录音内容。 你可以在播放音频文件时看到生成的听录文本。

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 [Azure 门户]( https://portal.azure.com)，然后选择包含你所创建的资源的资源组。
1. 选择该资源并选择“删除”，然后选择“是”以******** 进行确认。 这样便会删除该资源。

## 了解详细信息

本练习仅演示了语音服务的部分功能。 若要详细了解此服务的更多用途，请参阅[“语音”页](https://azure.microsoft.com/services/cognitive-services/speech-services)。
