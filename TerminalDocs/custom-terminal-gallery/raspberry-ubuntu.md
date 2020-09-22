---
title: Configurazione di Windows Terminal Raspberry Ubuntu
description: Questo è il tema di Raspberry Ubuntu.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.openlocfilehash: 9e1c315b4da3729e37edca409de0865d3e7dfdb1
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988646"
---
# <a name="raspberry-ubuntu-in-windows-terminal"></a>Raspberry Ubuntu nel terminale Windows

![Windows Terminal Raspberry Ubuntu](./../images/raspberry-ubuntu.png)

```json
    {
        "theme": "dark",
        "profiles": [
            {
                "name" : "Ubuntu",
                "source" : "Windows.Terminal.Wsl",
                "colorScheme" : "Raspberry",
                "cursorColor" : "#FFFFFF",
                "fontFace" : "Cascadia Code",
                "padding" : "5, 5, 5, 5",
                "suppressApplicationTitle": true,
                "tabTitle": "Ubuntu"
            }
        ],
        "schemes": [
            {
                "name" : "Raspberry",
                "background" : "#3C0315",
                "black" : "#282A2E",
                "blue" : "#0170C5",
                "brightBlack" : "#676E7A",
                "brightBlue" : "#80c8ff",
                "brightCyan" : "#8ABEB7",
                "brightGreen" : "#B5D680",
                "brightPurple" : "#AC79BB",
                "brightRed" : "#BD6D85",
                "brightWhite" : "#FFFFFD",
                "brightYellow" : "#FFFD76",
                "cyan" : "#3F8D83",
                "foreground" : "#FFFFFD",
                "green" : "#76AB23",
                "purple" : "#7D498F",
                "red" : "#BD0940",
                "white" : "#FFFFFD",
                "yellow" : "#E0DE48"
            }
        ]
    }
```
