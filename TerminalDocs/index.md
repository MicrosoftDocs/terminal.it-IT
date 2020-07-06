---
title: Panoramica di Terminale Windows
description: Informazioni su Terminale Windows e su come può migliorare il flusso di lavoro della riga di comando.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: abc0397c3f26da92980377aac2df466fe1bf190e
ms.sourcegitcommit: d8e23557224bc50a82a36dc80ac68b9d11dfdde9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720117"
---
# <a name="what-is-windows-terminal"></a><span data-ttu-id="ad3f8-103">Che cos'è Terminale Windows?</span><span class="sxs-lookup"><span data-stu-id="ad3f8-103">What is Windows Terminal?</span></span>

<span data-ttu-id="ad3f8-104">Terminale Windows è un'applicazione di terminale moderna destinata agli utenti di strumenti da riga di comando, come il prompt dei comandi, PowerShell e il sottosistema Windows per Linux (WSL, Windows Subsystem for Linux).</span><span class="sxs-lookup"><span data-stu-id="ad3f8-104">Windows Terminal is a modern terminal application for users of command-line tools and shells like Command Prompt, PowerShell, and Windows Subsystem for Linux (WSL).</span></span> <span data-ttu-id="ad3f8-105">Le principali funzionalità includono più schede e riquadri, il supporto per i caratteri Unicode e UTF-8, un motore di rendering del testo con accelerazione della GPU e la possibilità di personalizzare temi, testo, colori, sfondo e combinazioni di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-105">Its main features include multiple tabs, panes, Unicode and UTF-8 character support, a GPU accelerated text rendering engine, and the ability to create your own themes and customize text, colors, backgrounds, and shortcut key bindings.</span></span>

![Screenshot di Terminale Windows](./images/overview.png)

> [!NOTE]
> [<span data-ttu-id="ad3f8-107">Qual è la differenza tra una console, un terminale e una shell?</span><span class="sxs-lookup"><span data-stu-id="ad3f8-107">What's the difference between a console, a terminal, and a shell?</span></span>](https://www.hanselman.com/blog/WhatsTheDifferenceBetweenAConsoleATerminalAndAShell.aspx) <span data-ttu-id="ad3f8-108">Spiegazione di Scott Hanselman.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-108">Read Scott Hanselman's explanation.</span></span>

## <a name="multiple-profiles-supporting-a-variety-of-command-line-applications"></a><span data-ttu-id="ad3f8-109">Più profili che supportano un'ampia gamma di applicazioni da riga di comando</span><span class="sxs-lookup"><span data-stu-id="ad3f8-109">Multiple profiles supporting a variety of command-line applications</span></span>

<span data-ttu-id="ad3f8-110">All'interno di Terminale Windows puoi eseguire qualsiasi applicazione dotata di un'interfaccia della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-110">Any application that has a command-line interface can be run inside Windows Terminal.</span></span> <span data-ttu-id="ad3f8-111">Queste applicazioni includono PowerShell, il prompt dei comandi, Azure Cloud Shell e qualsiasi distribuzione WSL, come Ubuntu o Oh-My-Zsh.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-111">This includes everything from PowerShell and Command Prompt to Azure Cloud Shell and any WSL distribution such as Ubuntu or Oh-My-Zsh.</span></span>

## <a name="customized-schemes-and-configurations"></a><span data-ttu-id="ad3f8-112">Configurazioni e schemi personalizzati</span><span class="sxs-lookup"><span data-stu-id="ad3f8-112">Customized schemes and configurations</span></span>

<span data-ttu-id="ad3f8-113">Puoi configurare Terminale Windows con un'ampia varietà di combinazioni di colori e impostazioni.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-113">You can configure your Windows Terminal to have a variety of color schemes and settings.</span></span> <span data-ttu-id="ad3f8-114">Per informazioni su come creare una combinazione di colori personalizzati, vedi la [pagina Combinazioni di colori](./customize-settings/color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="ad3f8-114">To learn how to make your own color scheme, visit the [Color schemes page](./customize-settings/color-schemes.md).</span></span> <span data-ttu-id="ad3f8-115">Puoi anche trovare configurazioni personalizzate del terminale nella [raccolta di terminali personalizzati](./custom-terminal-gallery/powerline-in-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="ad3f8-115">You can also find custom Terminal configurations in the [Custom terminal gallery](./custom-terminal-gallery/powerline-in-powershell.md).</span></span>

## <a name="custom-key-bindings"></a><span data-ttu-id="ad3f8-116">Combinazioni di tasti personalizzate</span><span class="sxs-lookup"><span data-stu-id="ad3f8-116">Custom key bindings</span></span>

<span data-ttu-id="ad3f8-117">In Terminale Windows puoi usare un'ampia varietà di combinazioni di tasti personalizzate in base alle tue preferenze.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-117">There are a variety of custom key combinations you can use in Windows Terminal to have it feel more natural to you.</span></span> <span data-ttu-id="ad3f8-118">Se una specifica scelta rapida da tastiera non soddisfa le tue esigenze, puoi cambiarla come preferisci.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-118">If you don't like a particular keyboard shortcut, you can change it to whatever you prefer.</span></span>

<span data-ttu-id="ad3f8-119">Ad esempio, la combinazione predefinita di tasti di scelta rapida per la copia di testo dalla riga di comando è <kbd>CTRL+MAIUSC+C</kbd>.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-119">For example, the default shortcut key binding to copy text from the command line is <kbd>ctrl+shift+c</kbd>.</span></span> <span data-ttu-id="ad3f8-120">Puoi sostituirla con <kbd>CTRL+1</kbd> o con qualsiasi altra combinazione a scelta.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-120">You can change this to <kbd>ctrl+1</kbd> or whatever you prefer.</span></span> <span data-ttu-id="ad3f8-121">Per aprire una nuova scheda, la combinazione predefinita di tasti di scelta rapida è <kbd>CTRL+MAIUSC+T</kbd>, ma puoi scegliere di sostituirla con <kbd>CTRL+2</kbd>.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-121">To open a new tab, the default shortcut is <kbd>ctrl+shift+t</kbd>, but maybe you want to change this to <kbd>ctrl+2</kbd>.</span></span> <span data-ttu-id="ad3f8-122">La combinazione predefinita di tasti di scelta rapida per passare tra le schede aperte è <kbd>CTRL+TAB</kbd>, ma puoi sostituirla con <kbd>CTRL+-</kbd> e usarla per creare invece una nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-122">The default shortcut to flip between the tabs you have open is <kbd>ctrl+tab</kbd>, this could be changed to <kbd>ctrl+-</kbd> and used to create a new tab instead.</span></span>

<span data-ttu-id="ad3f8-123">Per informazioni sulla personalizzazione delle combinazioni di tasti, vedi la [pagina Combinazioni di tasti](./customize-settings/key-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="ad3f8-123">You can learn about customizing your key bindings on the [Key bindings page](./customize-settings/key-bindings.md).</span></span>

## <a name="unicode-and-utf-8-character-support"></a><span data-ttu-id="ad3f8-124">Supporto di caratteri Unicode e UTF-8</span><span class="sxs-lookup"><span data-stu-id="ad3f8-124">Unicode and UTF-8 character support</span></span>

<span data-ttu-id="ad3f8-125">Terminale Windows può visualizzare caratteri Unicode e UTF-8, ad esempio emoji e i caratteri di un'ampia varietà di lingue.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-125">Windows Terminal can display Unicode and UTF-8 characters such as emoji and characters from a variety of languages.</span></span>

## <a name="gpu-accelerated-text-rendering"></a><span data-ttu-id="ad3f8-126">Rendering del testo con accelerazione della GPU</span><span class="sxs-lookup"><span data-stu-id="ad3f8-126">GPU accelerated text rendering</span></span>

<span data-ttu-id="ad3f8-127">Terminale Windows usa la GPU per il rendering del testo, assicurando prestazioni più elevate rispetto all'esperienza predefinita della riga di comando Windows.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-127">Windows Terminal uses the GPU to render its text, thus providing improved performance over the default Windows command-line experience.</span></span>

## <a name="background-image-support"></a><span data-ttu-id="ad3f8-128">Supporto per immagini di sfondo</span><span class="sxs-lookup"><span data-stu-id="ad3f8-128">Background image support</span></span>

<span data-ttu-id="ad3f8-129">Nella finestra di Terminale Windows puoi aggiungere immagini e GIF di sfondo.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-129">You can have background images and gifs inside your Windows Terminal window.</span></span> <span data-ttu-id="ad3f8-130">Per informazioni su come aggiungere immagini di sfondo al tuo profilo, vedi la [pagina Impostazioni del profilo](./customize-settings/profile-settings.md#background-image-settings).</span><span class="sxs-lookup"><span data-stu-id="ad3f8-130">Information on how to add background images to your profile can be found on the [Profile settings page](./customize-settings/profile-settings.md#background-image-settings).</span></span>

## <a name="command-line-arguments"></a><span data-ttu-id="ad3f8-131">Argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="ad3f8-131">Command line arguments</span></span>

<span data-ttu-id="ad3f8-132">Per avviare Terminale Windows in una specifica configurazione, puoi usare gli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-132">You can set Windows Terminal to launch in a specific configuration using command-line arguments.</span></span> <span data-ttu-id="ad3f8-133">Puoi specificare quale profilo aprire in una nuova scheda e quale cartella dovrà essere selezionata, puoi aprire il terminale con riquadri della finestra divisi e scegliere quale scheda dovrà avere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="ad3f8-133">You can specify which profile to open in a new tab, which folder directory should be selected, open the terminal with split window panes, and choose which tab should be in focus.</span></span>

<span data-ttu-id="ad3f8-134">Ad esempio, per aprire Terminale Windows da PowerShell con tre riquadri, di cui quello a sinistra esegue un profilo del prompt dei comandi e quello a destra è diviso tra PowerShell e il profilo predefinito che esegue WSL, immetti:</span><span class="sxs-lookup"><span data-stu-id="ad3f8-134">For example, to open Windows Terminal from PowerShell with three panes, with the left pane running a Command Prompt profile and the right pane split between your PowerShell and your default profile running WSL, enter:</span></span>

```bash
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

<span data-ttu-id="ad3f8-135">Per informazioni su come configurare gli argomenti della riga di comando, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="ad3f8-135">Learn how to set up command-line arguments on the [Command line arguments page](./command-line-arguments.md).</span></span>
