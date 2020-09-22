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
# <a name="custom-terminal-guide"></a><span data-ttu-id="7ce37-103">Guida al terminale personalizzato</span><span class="sxs-lookup"><span data-stu-id="7ce37-103">Custom Terminal guide</span></span>

<span data-ttu-id="7ce37-104">Di seguito sono riportate alcune combinazioni di colori da provare o utilizzare come base per i propri progetti.</span><span class="sxs-lookup"><span data-stu-id="7ce37-104">Here are some color schemes for you to try or use as the basis of your own designs.</span></span>

## <a name="installing-schemes"></a><span data-ttu-id="7ce37-105">Installazione degli schemi</span><span class="sxs-lookup"><span data-stu-id="7ce37-105">Installing schemes</span></span>

<span data-ttu-id="7ce37-106">Copiare il codice JSON dalla sezione **"schemes"** nella sezione corretta in settings.json, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7ce37-106">Copy the JSON from the **"schemes"** section into the correct section in settings.json, for example:</span></span>

<span data-ttu-id="7ce37-107">Prima di:</span><span class="sxs-lookup"><span data-stu-id="7ce37-107">Before:</span></span>

```json
"schemes:" [],
```

<span data-ttu-id="7ce37-108">Dopo:</span><span class="sxs-lookup"><span data-stu-id="7ce37-108">After:</span></span>

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

<span data-ttu-id="7ce37-109">Aggiungere quindi la sezione specifica del profilo, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7ce37-109">Then add the profile-specific section, for example:</span></span>

<span data-ttu-id="7ce37-110">Prima di:</span><span class="sxs-lookup"><span data-stu-id="7ce37-110">Before:</span></span>

```json
{
    "guid": "{234ab24f-34dd-ff3-ade434aad345}",
    "name": "Command Prompt",
    "commandline": "cmd.exe",
    "hidden": false
}
```

<span data-ttu-id="7ce37-111">Dopo:</span><span class="sxs-lookup"><span data-stu-id="7ce37-111">After:</span></span>

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

## <a name="frosted-glass"></a><span data-ttu-id="7ce37-112">Vetro ghiacciato</span><span class="sxs-lookup"><span data-stu-id="7ce37-112">Frosted Glass</span></span>

![Tema vetro smerigliato terminale Windows](./../images/frosted-glass-theme.png)

[<span data-ttu-id="7ce37-114">Dettagli</span><span class="sxs-lookup"><span data-stu-id="7ce37-114">Details</span></span>](frosted-glass-theme.md)

## <a name="powerline"></a><span data-ttu-id="7ce37-115">Powerline</span><span class="sxs-lookup"><span data-stu-id="7ce37-115">Powerline</span></span>

![Terminale Windows - PowerShell per Powerline](./../images/powerline-powershell.png)

[<span data-ttu-id="7ce37-117">Dettagli</span><span class="sxs-lookup"><span data-stu-id="7ce37-117">Details</span></span>](powerline-in-powershell.md)

## <a name="raspberry-ubuntu"></a><span data-ttu-id="7ce37-118">Raspberry Ubuntu</span><span class="sxs-lookup"><span data-stu-id="7ce37-118">Raspberry Ubuntu</span></span>

![Windows Terminal Raspberry Ubuntu](./../images/raspberry-ubuntu.png)

[<span data-ttu-id="7ce37-120">Dettagli</span><span class="sxs-lookup"><span data-stu-id="7ce37-120">Details</span></span>](raspberry-ubuntu.md)

## <a name="retro-command"></a><span data-ttu-id="7ce37-121">Comando retrò</span><span class="sxs-lookup"><span data-stu-id="7ce37-121">Retro Command</span></span>

![Prompt dei comandi retrò del terminale di Windows](./../images/retro-command-prompt.png)

[<span data-ttu-id="7ce37-123">Dettagli</span><span class="sxs-lookup"><span data-stu-id="7ce37-123">Details</span></span>](retro-command-prompt.md)

## <a name="share"></a><span data-ttu-id="7ce37-124">Condividi!</span><span class="sxs-lookup"><span data-stu-id="7ce37-124">Share!</span></span>

<span data-ttu-id="7ce37-125">Si dispone di uno schema di terminale di Windows che si desidera condividere?</span><span class="sxs-lookup"><span data-stu-id="7ce37-125">Do you have a Windows Terminal scheme you would like to share?</span></span> <span data-ttu-id="7ce37-126">Mostraci su [Twitter](https://twitter.com/WindowsDocs)!</span><span class="sxs-lookup"><span data-stu-id="7ce37-126">Show us on [Twitter](https://twitter.com/WindowsDocs)!</span></span>
