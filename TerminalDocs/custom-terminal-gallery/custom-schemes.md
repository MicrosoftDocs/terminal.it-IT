---
title: Guida agli schemi colori personalizzati
description: Alcune configurazioni di esempio per il terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 07/27/2020
ms.topic: sample
ms.openlocfilehash: b505abf18f1dcf5bf211193dd9918d7131d2ed06
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "91003644"
---
# <a name="custom-terminal-guide"></a>Guida al terminale personalizzato

Di seguito sono riportate alcune combinazioni di colori da provare o utilizzare come base per i propri progetti.

## <a name="installing-schemes"></a>Installazione degli schemi

Copiare il codice JSON dalla sezione **"schemes"** nella sezione corretta in settings.json, ad esempio:

Prima di:

```json
"schemes:" [],
```

Dopo:

```json
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
```

Aggiungere quindi la sezione specifica del profilo, ad esempio:

Prima di:

```json
{
    "guid": "{234ab24f-34dd-ff3-ade434aad345}",
    "name": "Command Prompt",
    "commandline": "cmd.exe",
    "hidden": false
}
```

Dopo:

```json
{
    "guid": "{234ab24f-34dd-ff3-ade434aad345}",
    "name": "Command Prompt",
    "commandline": "cmd.exe",
    "hidden": false,
    "colorScheme" : "Retro",
    "cursorColor" : "#FFFFFF",
    "cursorShape": "filledBox",
    "fontSize" : 16,
    "padding" : "5, 5, 5, 5",
    "tabTitle" : "Command Prompt",
    "fontFace": "PxPlus IBM VGA8",
    "experimental.retroTerminalEffect": true
}
```

## <a name="frosted-glass"></a>Vetro ghiacciato

![Tema vetro smerigliato terminale Windows](./../images/frosted-glass-theme.png)

[Dettagli](frosted-glass-theme.md)

## <a name="powerline"></a>Powerline

![Terminale Windows - PowerShell per Powerline](./../images/powerline-powershell.png)

[Dettagli](powerline-in-powershell.md)

## <a name="raspberry-ubuntu"></a>Raspberry Ubuntu

![Windows Terminal Raspberry Ubuntu](./../images/raspberry-ubuntu.png)

[Dettagli](raspberry-ubuntu.md)

## <a name="retro-command"></a>Comando retrò

![Prompt dei comandi retrò del terminale di Windows](./../images/retro-command-prompt.png)

[Dettagli](retro-command-prompt.md)

## <a name="share"></a>Condividi!

Si dispone di uno schema di terminale di Windows che si desidera condividere? Mostraci su [Twitter](https://twitter.com/WindowsDocs)!
