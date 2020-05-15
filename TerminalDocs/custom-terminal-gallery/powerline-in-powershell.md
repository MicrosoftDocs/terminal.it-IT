---
title: Windows Terminal Powerline in configurazione di PowerShell
description: Si tratta della configurazione e del tema per Powerline in PowerShell.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.service: terminal
ms.openlocfilehash: 2e8e19647df456ab69347f923e75601ddfcc2e2f
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416546"
---
# <a name="powerline-in-powershell-theme-for-windows-terminal"></a>Tema di Powerline in PowerShell per il terminale Windows

Il prompt viene applicato allo stile tramite Powerline e usa il `Cascadia Code PL` tipo di carattere, che può essere scaricato dalla [pagina delle versioni di GitHub di Cascadia code](https://github.com/microsoft/cascadia-code/releases).

> [!div class="nextstepaction"]
> [Informazioni su come configurare Powerline](./../tutorials/powerline-setup.md)

![PowerShell Powerline di Windows Terminal](./../images/powerline-powershell.png)

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
