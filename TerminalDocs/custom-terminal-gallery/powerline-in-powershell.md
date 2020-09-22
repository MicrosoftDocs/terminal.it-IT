---
title: Windows Terminal Powerline in configurazione di PowerShell
description: Si tratta della configurazione e del tema per Powerline in PowerShell.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.openlocfilehash: 0c754cac9e286e1a928c2ddf3e711c552cc67d3c
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988682"
---
# <a name="powerline-in-powershell-theme-for-windows-terminal"></a><span data-ttu-id="02252-103">Tema di Powerline in PowerShell per il terminale Windows</span><span class="sxs-lookup"><span data-stu-id="02252-103">Powerline in PowerShell theme for Windows Terminal</span></span>

<span data-ttu-id="02252-104">Il prompt viene applicato allo stile tramite Powerline e usa il `Cascadia Code PL` tipo di carattere, che può essere scaricato dalla [pagina delle versioni di GitHub di Cascadia code](https://github.com/microsoft/cascadia-code/releases).</span><span class="sxs-lookup"><span data-stu-id="02252-104">The prompt is styled using Powerline and is using the `Cascadia Code PL` font, which can be downloaded from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="02252-105">Informazioni su come configurare Powerline</span><span class="sxs-lookup"><span data-stu-id="02252-105">Learn how to set up Powerline</span></span>](./../tutorials/powerline-setup.md)

![Terminale Windows - PowerShell per Powerline](./../images/powerline-powershell.png)

```json
    {
        "theme": "dark",
        "profiles": [
            {
                "name" : "Powershell",
                "source" : "Windows.Terminal.PowershellCore",
                "acrylicOpacity" : 0.7,
                "colorScheme" : "Campbell",
                "cursorColor" : "#FFFFFD",
                "fontFace" : "Cascadia Code PL",
                "useAcrylic" : true
            }
        ]
    }
```
