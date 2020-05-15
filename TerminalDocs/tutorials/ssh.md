---
title: Terminale Windows - SSH
description: Questa esercitazione illustra come configurare una connessione SSH in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: c418460cd47935ed8b8eb57ebdb89322d543a20e
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415866"
---
# <a name="tutorial-ssh-in-windows-terminal"></a><span data-ttu-id="da1b2-103">Esercitazione: SSH in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="da1b2-103">Tutorial: SSH in Windows Terminal</span></span>

<span data-ttu-id="da1b2-104">Windows 10 include un client SSH predefinito che è possibile usare in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="da1b2-104">Windows 10 has a build-in SSH client that you can use in the Windows Terminal.</span></span>

<span data-ttu-id="da1b2-105">Questa esercitazione illustra come configurare un profilo che usa SSH in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="da1b2-105">In this tutorial, you'll learn how to set up a profile in Windows Terminal that uses SSH.</span></span>

## <a name="create-a-profile"></a><span data-ttu-id="da1b2-106">Creare un profilo</span><span class="sxs-lookup"><span data-stu-id="da1b2-106">Create a profile</span></span>

<span data-ttu-id="da1b2-107">Per avviare una sessione SSH al prompt dei comandi, esegui `ssh user@machine`. Ti verrà richiesto di immettere la password.</span><span class="sxs-lookup"><span data-stu-id="da1b2-107">You can start an SSH session in your command prompt by executing `ssh user@machine` and you will be prompted to enter your password.</span></span> <span data-ttu-id="da1b2-108">Per creare un profilo di Terminale Windows che esegue questa operazione all'avvio, aggiungi l'impostazione `commandline` a un profilo nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="da1b2-108">You can create a Windows Terminal profile that does this on startup by adding the `commandline` setting to a profile in your settings.json file.</span></span>

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="resources"></a><span data-ttu-id="da1b2-109">Risorse</span><span class="sxs-lookup"><span data-stu-id="da1b2-109">Resources</span></span>

* [<span data-ttu-id="da1b2-110">Come abilitare e usare i nuovi comandi SSH predefiniti di Windows 10</span><span class="sxs-lookup"><span data-stu-id="da1b2-110">How to Enable and Use Windows 10’s New Built-in SSH Commands</span></span>](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
