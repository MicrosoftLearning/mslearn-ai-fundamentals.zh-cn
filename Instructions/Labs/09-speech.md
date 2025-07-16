---
lab:
  title: 在 Azure AI Foundry 门户中探索语音
---

# 在 Azure AI Foundry 门户中探索语音

Azure AI 语音服务可将语音转换为文本，以及将文本转换为可听语音。**** 你可以使用 AI 语音创建一个应用程序，该应用程序可以转换会议笔记或基于采访录音生成文本。

在本练习中，你将使用 Azure AI Foundry 门户（Microsoft 创建智能应用程序的平台）中的 Azure AI 语音，以使用内置的试用体验转录音频。 

## 在 Azure AI Foundry 门户中创建项目

1. 在 Web 浏览器中打开 [Azure AI Foundry 门户](https://ai.azure.com)，网址为：`https://ai.azure.com`，然后使用 Azure 凭据登录。 关闭首次登录时弹出的所有提示或快速入门窗格。 

1. 在浏览器中，导航到 `https://ai.azure.com/managementCenter/allResources` 并选择“**创建**”。 然后选择创建*新的 Azure AI Foundry 资源*的选项。

1. 在*创建项目*向导中，输入项目有效名称。

1. 展开“*高级选项*”，为项目指定以下设置：
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

1. 在“*操场*”页上，选择“**语音操场**”磁贴以试用一些 Azure AI 语音功能。

## 在 Azure AI Foundry 的语音操场中探索语音转文本

让我们在 Azure AI Foundry 的语音操场中试用*语音转文本*。 

1. 在“*语音*”页上，向下滚动并选择“*试用语音功能*”下的“**实时听录**”。 你将被带到“*语音操场*”。 

1. 选择 [https://aka.ms/mslearn-speech-files****](https://aka.ms/mslearn-speech-files) 以下载 speech.zip。**** 打开  文件夹。 

1. 在“*上传文件*”下，选择“**浏览文件**”并导航到保存相应文件的文件夹。 选择 WhatAICanDo.m4a，然后选择********“打开”。

    ![浏览文件](media/recognize-synthesize-speech/browse-files-speech.png)

1. 语音服务将实时听录和显示文本。 如果你的计算机上有音频，你可以在转换文本的同时听录音。

1. 查看输出，该输出应已成功识别音频并将其听录为文本。

在本练习中，你在 Azure AI Foundry 的语音操场中试用了 Azure AI 语音服务。 然后，你使用实时听录来转录音频录制内容。 你可以在播放音频文件时看到生成的听录文本。

## 清理

如果不打算做更多的练习，请删除任何不再需要的资源。 这可以避免产生任何不必要的成本。

1. 打开 [Azure 门户]( https://portal.azure.com)，然后选择包含你所创建的资源的资源组。
1. 选择该资源并选择“删除”，然后选择“是”以******** 进行确认。 这样便会删除该资源。

## 了解详细信息

本练习演示了语音服务的众多功能之一。 若要详细了解此服务的更多用途，请参阅[“语音”页](https://azure.microsoft.com/services/cognitive-services/speech-services)。
