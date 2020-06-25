---
title: Terminale Windows - SSH
description: Questa esercitazione illustra come configurare una connessione SSH in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: 02f4704b81cd0d287c207f0138ef27c537929711
ms.sourcegitcommit: bae07a8dd2010a95de4d53b1465abe226e4ad18e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/26/2020
ms.locfileid: "83856339"
---
# <a name="tutorial-ssh-in-windows-terminal"></a><span data-ttu-id="6964f-103">Esercitazione: SSH in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="6964f-103">Tutorial: SSH in Windows Terminal</span></span>

<span data-ttu-id="6964f-104">Windows 10 include un client SSH predefinito che è possibile usare in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="6964f-104">Windows 10 has a built-in SSH client that you can use in Windows Terminal.</span></span>

<span data-ttu-id="6964f-105">Questa esercitazione illustra come configurare un profilo che usa SSH in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="6964f-105">In this tutorial, you'll learn how to set up a profile in Windows Terminal that uses SSH.</span></span>

## <a name="create-a-profile"></a><span data-ttu-id="6964f-106">Creare un profilo</span><span class="sxs-lookup"><span data-stu-id="6964f-106">Create a profile</span></span>

<span data-ttu-id="6964f-107">Per avviare una sessione SSH al prompt dei comandi, esegui `ssh user@machine`. Ti verrà richiesto di immettere la password.</span><span class="sxs-lookup"><span data-stu-id="6964f-107">You can start an SSH session in your command prompt by executing `ssh user@machine` and you will be prompted to enter your password.</span></span> <span data-ttu-id="6964f-108">Per creare un profilo di Terminale Windows che esegue questa operazione all'avvio, aggiungi l'impostazione `commandline` a un profilo nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="6964f-108">You can create a Windows Terminal profile that does this on startup by adding the `commandline` setting to a profile in your settings.json file.</span></span>

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="specify-starting-directory"></a><span data-ttu-id="6964f-109">Specificare la directory iniziale</span><span class="sxs-lookup"><span data-stu-id="6964f-109">Specify starting directory</span></span>

<span data-ttu-id="6964f-110">Per specificare la directory iniziale per una sessione SSH richiamata da Terminale Windows, è possibile usare questo comando:</span><span class="sxs-lookup"><span data-stu-id="6964f-110">To specify the starting directory for a ssh session invoked by Windows Terminal, you can use this command:</span></span>

```bash
"commandline": "ssh -t bob@foo \"cd /data/bob && exec bash -l\""
```

<span data-ttu-id="6964f-111">Il flag `-t` forza l'allocazione del pseudo-terminale.</span><span class="sxs-lookup"><span data-stu-id="6964f-111">The `-t` flag forces pseudo-terminal allocation.</span></span> <span data-ttu-id="6964f-112">Questa funzionalità può essere usata per eseguire programmi arbitrari basati su schermo in un computer remoto, ad esempio per l'implementazione di servizi di menu.</span><span class="sxs-lookup"><span data-stu-id="6964f-112">This can be used to execute arbitrary screen-based programs on a remote machine, e.g. when implementing menu services.</span></span> <span data-ttu-id="6964f-113">Sarà necessario usare le virgolette doppie di escape perché le derivate di Bourne shell non eseguono analisi aggiuntive per una stringa racchiusa tra virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="6964f-113">You will need to use escaped double quotes as bourne shell derivatives don't do any additional parsing for a string in single quotes.</span></span>

<span data-ttu-id="6964f-114">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="6964f-114">For more information, see:</span></span>

* [<span data-ttu-id="6964f-115">Problema di GH: Come specificare la directory iniziale per una sessione SSH?</span><span class="sxs-lookup"><span data-stu-id="6964f-115">GH Issue: How to specify the starting directory for a ssh session?</span></span>](https://github.com/MicrosoftDocs/terminal/issues/25)
* [<span data-ttu-id="6964f-116">StackOverflow: Come usare SSH per accedere direttamente a una directory specifica?</span><span class="sxs-lookup"><span data-stu-id="6964f-116">StackOverflow: How can I ssh directly to a particular directory?</span></span>](https://stackoverflow.com/questions/626533/how-can-i-ssh-directly-to-a-particular-directory)

## <a name="resources"></a><span data-ttu-id="6964f-117">Risorse</span><span class="sxs-lookup"><span data-stu-id="6964f-117">Resources</span></span>

* [<span data-ttu-id="6964f-118">Come abilitare e usare i nuovi comandi SSH predefiniti di Windows 10</span><span class="sxs-lookup"><span data-stu-id="6964f-118">How to Enable and Use Windows 10’s New Built-in SSH Commands</span></span>](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
