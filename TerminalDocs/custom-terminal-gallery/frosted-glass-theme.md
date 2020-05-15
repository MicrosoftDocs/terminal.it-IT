---
title: Configurazione del tema del vetro smerigliato di Windows
description: Si tratta di una configurazione di esempio per un tema con vetro smerigliato.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.service: terminal
ms.openlocfilehash: c6fa0ef042e48a151f0a29b557997f2bbed90495
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416536"
---
# <a name="frosted-glass-theme-in-windows-terminal"></a>Tema vetro smerigliato nel terminale di Windows

Il prompt viene applicato allo stile tramite Powerline e usa il `Cascadia Code PL` tipo di carattere, che può essere scaricato dalla [pagina delle versioni di GitHub di Cascadia code](https://github.com/microsoft/cascadia-code/releases).

> [!div class="nextstepaction"]
> [Informazioni su come configurare Powerline](./../tutorials/powerline-setup.md)

![Tema vetro smerigliato terminale Windows](./../images/frosted-glass-theme.png)

```json
    {
        "theme": "light",
        "profiles": [
            {
                "name" : "PowerShell",
                "source" : "Windows.Terminal.PowershellCore",
                "acrylicOpacity": 0.7,
                "colorScheme" : "Frost",
                "cursorColor" : "#000000",
                "fontFace" : "Cascadia Code PL",
                "useAcrylic": true
            }
        ],
        "schemes": [
            {
                "name" : "Frost",
                "background" : "#FFFFFF",
                "black" : "#3C5712",
                "blue" : "#17b2ff",
                "brightBlack" : "#749B36",
                "brightBlue" : "#27B2F6",
                "brightCyan" : "#13A8C0",
                "brightGreen" : "#89AF50",
                "brightPurple" : "#F2A20A",
                "brightRed" : "#F49B36",
                "brightWhite" : "#741274",
                "brightYellow" : "#991070",
                "cyan" : "#3C96A6",
                "foreground" : "#000000",
                "green" : "#6AAE08",
                "purple" : "#991070",
                "red" : "#8D0C0C",
                "white" : "#6E386E",
                "yellow" : "#991070"
            }
        ]
    }
```
