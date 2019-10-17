---
title: 教程：从 Visual Studio Code 创建应用服务
description: 教程步骤 3，从 VS Code 扩展创建应用服务。
services: app-service
author: kraigb
manager: barbkess
ms.service: app-service
ms.topic: conceptual
ms.date: 09/12/2019
ms.author: kraigb
ms.custom: seo-python-october2019
ms.openlocfilehash: 8a2a719ee578553bb2033469e64c2df34351e36e
ms.sourcegitcommit: bed07b313eeab51281d1a6d4eba67a75524b2f57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/09/2019
ms.locfileid: "72172513"
---
# <a name="tutorial-create-the-app-service-from-visual-studio-code"></a>教程：从 Visual Studio Code 创建应用服务

[上一步：准备应用](tutorial-deploy-app-service-on-linux-01.md)

在此步骤中，我们创建需向其部署应用的 Azure 应用服务的实例。 在部署代码之前，请先执行此步骤，这样就可以在下一步根据需要配置自定义启动文件。

1. 在“Azure：函数”  应用服务”资源管理器中，选择 **+** 命令以创建新的应用服务，或者打开命令面板 (**F1**)，然后选择“Azure 应用服务:  创建新的 Web 应用”。 （在应用服务术语中，“Web 应用”是与 Web 应用代码相对应的**主机**，不是应用代码本身。）

    ![应用服务资源管理器中的“创建新的应用服务”按钮](media/app-service-create-new.png)

1. 在接下来的提示窗口中执行以下操作：

    - 输入应用的名称，该名称必须在应用服务上全局唯一；通常使用你的名称或公司名称，后接应用名称。
    - 选择 **Python 3.7** 作为运行时。

1. 如果显示一条消息，指示新应用服务已创建，请选择“查看输出”，  ，以便切换到  VS Code 中的“输出”窗口。 输出显示已创建的 Azure 资源组和应用服务计划的名称，以及应用服务的 URL。

    ![在创建应用服务后显示的消息](media/app-service-created.png)

1. 若要确认应用服务是否正常运行，请在“Azure:  应用服务”资源管理器中展开订阅，右键单击应用服务名称，然后选择“浏览网站”： 

    ![应用服务资源管理器中的应用服务上的“浏览网站”命令](media/browse-website-command.png)

1. 由于你尚未将自己的代码部署到应用服务（在下一步这样做），因此仅显示默认应用：

    ![Linux 上的应用服务上的默认 Python 应用](media/default-python-app.png)

## <a name="optional-upload-an-environment-variable-definitions-file"></a>（可选）上传环境变量定义文件

如果有环境变量定义文件，也可使用该文件配置应用服务环境。 （若要详细了解此类通常有 *.env* 扩展的文件，请参阅 [Visual Studio Code - Python 环境](https://code.visualstudio.com/docs/python/environments#environment-variable-definitions-file)。）

1. 在“Azure：函数”  应用服务”资源管理器中，展开所需应用服务的节点，然后右键单击“应用程序设置”节点并选择“上传本地设置”。  

1. VS Code 会提示你输入 *.env* 文件的位置，然后将该文件上传到应用服务。

1. 上传完成后，即可展开“应用程序设置”节点，查看各个值。  也可在 Azure 门户中查看它们，方法是：导航到应用服务，然后选择“配置”。 

1. 如果在 Azure 门户中直接创建设置，则可将设置保存到定义文件中，方法是：右键单击“应用程序设置”节点，然后选择“下载远程设置”。   此过程确保你在存储库中有这些设置，而不是仅在门户中有。

> [!div class="nextstepaction"]
> [我创建了应用服务](tutorial-deploy-app-service-on-linux-04.md)

[我遇到了问题](https://www.research.net/r/PWZWZ52?tutorial=vscode-appservice-python&step=03-create-app-service)
