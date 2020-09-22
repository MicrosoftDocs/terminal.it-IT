---
title: Configurazione del prompt dei comandi retro del terminale Windows
description: Questa è la configurazione per un prompt dei comandi retrò nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.openlocfilehash: 821a3e367e57fca6a1f7fd7fd4911f55e888143e
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988647"
---
# <a name="retro-command-prompt-in-windows-terminal"></a><span data-ttu-id="1f43b-103">Prompt dei comandi retrò nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="1f43b-103">Retro Command Prompt in Windows Terminal</span></span>

<span data-ttu-id="1f43b-104">Il prompt usa il `PxPlus IBM VGA8` tipo di carattere, che non è incluso nel terminale di Windows.</span><span class="sxs-lookup"><span data-stu-id="1f43b-104">The prompt is using the `PxPlus IBM VGA8` font, which is not included in Windows Terminal.</span></span>

![Prompt dei comandi retrò del terminale di Windows](./../images/retro-command-prompt.png)

```json
    {
        "theme": "dark",
        "profiles": [
            {
                "name": "Command Prompt",
                "commandline": "cmd.exe",
                "closeOnExit" : true,
                "colorScheme" : "Retro",
                "cursorColor" : "#FFFFFF",
                "cursorShape": "filledBox",
                "fontSize" : 16,
                "padding" : "5, 5, 5, 5",
                "tabTitle" : "Command Prompt",
                "fontFace": "PxPlus IBM VGA8",
                "experimental.retroTerminalEffect": true
            }
        ],
        "schemes": [
            {
                "name": "Retro",
                "background": "#000000",
                "black": "#00ff00",
                "blue": "#00ff00",
                "brightBlack": "#00ff00",
                "brightBlue": "#00ff00",
                "brightCyan": "#00ff00",
                "brightGreen": "#00ff00",
                "brightPurple": "#00ff00",
                "brightRed": "#00ff00",
                "brightWhite": "#00ff00",
                "brightYellow": "#00ff00",
                "cyan": "#00ff00",
                "foreground": "#00ff00",
                "green": "#00ff00",
                "purple": "#00ff00",
                "red": "#00ff00",
                "white": "#00ff00",
                "yellow": "#00ff00"
            }
        ]
    }
```
