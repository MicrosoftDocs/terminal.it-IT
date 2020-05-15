---
title: Configurazione del prompt dei comandi retro del terminale Windows
description: Questa è la configurazione per un prompt dei comandi retrò nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.service: terminal
ms.openlocfilehash: 877f849dd33666a1825bee2ed9da29a8b2341517
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416526"
---
# <a name="retro-command-prompt-in-windows-terminal"></a>Prompt dei comandi retrò nel terminale di Windows

Il prompt usa il `PxPlus IBM VGA8` tipo di carattere, che non è incluso nel terminale di Windows.

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
