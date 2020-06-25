---
title: Terminale Windows - Configurazione di Powerline
description: Questa esercitazione illustra come configurare Powerline in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: 2896ede288e0e466f68323a87e5a4b07bd509d3c
ms.sourcegitcommit: bae07a8dd2010a95de4d53b1465abe226e4ad18e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/26/2020
ms.locfileid: "83856349"
---
# <a name="tutorial-set-up-powerline-in-windows-terminal"></a><span data-ttu-id="e2874-103">Esercitazione: Configurare Powerline in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="e2874-103">Tutorial: Set up Powerline in Windows Terminal</span></span>

<span data-ttu-id="e2874-104">Powerline offre un'esperienza personalizzata del prompt dei comandi che include i prompt e la codifica a colori per gli stati di GIT.</span><span class="sxs-lookup"><span data-stu-id="e2874-104">Powerline provides a customized command prompt experience providing Git status color-coding and prompts.</span></span>

![Terminale Windows - PowerShell per Powerline](./../images/powerline-powershell.png)

<span data-ttu-id="e2874-106">In questa esercitazione verranno illustrate le procedure per:</span><span class="sxs-lookup"><span data-stu-id="e2874-106">In this tutorial, you learn how to:</span></span>

> [!div class="checklist"]
>
> * <span data-ttu-id="e2874-107">Configurare Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2874-107">Set up Powerline in PowerShell</span></span>
> * <span data-ttu-id="e2874-108">Configurare Powerline in WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="e2874-108">Set up Powerline in Ubuntu/WSL</span></span>
> * <span data-ttu-id="e2874-109">Aggiungere i glifi Powerline mancanti</span><span class="sxs-lookup"><span data-stu-id="e2874-109">Add missing Powerline glyphs</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e2874-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="e2874-110">Prerequisites</span></span>

### <a name="install-a-powerline-font"></a><span data-ttu-id="e2874-111">Installare un tipo di carattere Powerline</span><span class="sxs-lookup"><span data-stu-id="e2874-111">Install a Powerline font</span></span>

<span data-ttu-id="e2874-112">Powerline usa i glifi per applicare stili al prompt.</span><span class="sxs-lookup"><span data-stu-id="e2874-112">Powerline uses glyphs in order to style the prompt.</span></span> <span data-ttu-id="e2874-113">Se il tipo di carattere non include glifi Powerline, è possibile che nel prompt vengano visualizzati diversi caratteri Unicode '&#x25AF;' sostitutivi.</span><span class="sxs-lookup"><span data-stu-id="e2874-113">If your font does not include Powerline glyphs, you may see several Unicode replacement characters '&#x25AF;' throughout your prompt.</span></span> <span data-ttu-id="e2874-114">Anche se [Cascadia Mono](./../cascadia-code.md) non include i glifi Powerline, puoi installare Cascadia Code PL o Cascadia Mono PL, che invece li includono.</span><span class="sxs-lookup"><span data-stu-id="e2874-114">Though [Cascadia Mono](./../cascadia-code.md) does not include Powerline glyphs, you can install Cascadia Code PL or Cascadia Mono PL, which have the Powerline glyphs included.</span></span> <span data-ttu-id="e2874-115">Questi tipi di carattere possono essere installati dalla [pagina delle versioni di Cascadia Code in GitHub](https://github.com/microsoft/cascadia-code/releases).</span><span class="sxs-lookup"><span data-stu-id="e2874-115">These fonts can be installed from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span>

## <a name="set-up-powerline-in-powershell"></a><span data-ttu-id="e2874-116">Configurare Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2874-116">Set up Powerline in PowerShell</span></span>

### <a name="powershell-prerequisites"></a><span data-ttu-id="e2874-117">Prerequisiti di PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2874-117">PowerShell prerequisites</span></span>

<span data-ttu-id="e2874-118">Se non lo hai già fatto, [installa GIT per Windows](https://git-scm.com/downloads).</span><span class="sxs-lookup"><span data-stu-id="e2874-118">If you don't already have it, [install Git for Windows](https://git-scm.com/downloads).</span></span>

<span data-ttu-id="e2874-119">Usa PowerShell per installare Posh-Git e Oh-My-Posh:</span><span class="sxs-lookup"><span data-stu-id="e2874-119">Using PowerShell, install Posh-Git and Oh-My-Posh:</span></span>

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

> [!TIP]
> <span data-ttu-id="e2874-120">Se non è già stato fatto, può essere necessario installare NuGet.</span><span class="sxs-lookup"><span data-stu-id="e2874-120">You may need to install NuGet if you don't already have it.</span></span> <span data-ttu-id="e2874-121">La riga di comando di PowerShell chiederà se si vuole installare NuGet in questo caso.</span><span class="sxs-lookup"><span data-stu-id="e2874-121">Your PowerShell command line will ask if you want to install NuGet if this is the case.</span></span> <span data-ttu-id="e2874-122">Selezionare Sì.</span><span class="sxs-lookup"><span data-stu-id="e2874-122">Select [Y] Yes.</span></span> <span data-ttu-id="e2874-123">Può anche essere necessario confermare l'installazione di moduli di [PSGallery](https://docs.microsoft.com/powershell/scripting/gallery/getting-started?view=powershell-7), un 'repository non attendibile'.</span><span class="sxs-lookup"><span data-stu-id="e2874-123">You may also need to approve that you are installing modules from [PSGallery](https://docs.microsoft.com/powershell/scripting/gallery/getting-started?view=powershell-7), an 'untrusted repository'.</span></span> <span data-ttu-id="e2874-124">Selezionare Sì.</span><span class="sxs-lookup"><span data-stu-id="e2874-124">Select [Y] Yes.</span></span>

<span data-ttu-id="e2874-125">[Posh-Git](https://github.com/dahlbyk/posh-git) aggiunge al prompt informazioni sullo stato di GIT, nonché il completamento tramite tasto TAB per comandi, parametri, repository remoti e nomi di ramo GIT.</span><span class="sxs-lookup"><span data-stu-id="e2874-125">[Posh-Git](https://github.com/dahlbyk/posh-git) adds Git status information to your prompt as well as tab-completion for Git commands, parameters, remotes, and branch names.</span></span> <span data-ttu-id="e2874-126">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) offre funzionalità relative al tema per il prompt di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2874-126">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) provides theme capabilities for your PowerShell prompt.</span></span>

<span data-ttu-id="e2874-127">Se usi PowerShell Core, installa PSReadline:</span><span class="sxs-lookup"><span data-stu-id="e2874-127">If you are using PowerShell Core, install PSReadline:</span></span>

```powershell
Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
```

<span data-ttu-id="e2874-128">[PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) consente di personalizzare l'ambiente di modifica da riga di comando in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2874-128">[PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) lets you customize the command line editing environment in PowerShell.</span></span>

### <a name="customize-your-powershell-prompt"></a><span data-ttu-id="e2874-129">Personalizzare il prompt di PowerShell</span><span class="sxs-lookup"><span data-stu-id="e2874-129">Customize your PowerShell prompt</span></span>

<span data-ttu-id="e2874-130">Apri il profilo di PowerShell con `notepad $PROFILE` o con l'editor di testo che preferisci.</span><span class="sxs-lookup"><span data-stu-id="e2874-130">Open your PowerShell profile with `notepad $PROFILE` or the text editor of your choice.</span></span> <span data-ttu-id="e2874-131">Non si tratta del profilo di Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="e2874-131">This is not your Windows Terminal profile.</span></span> <span data-ttu-id="e2874-132">Il profilo di PowerShell è uno script eseguito ogni volta che viene avviato PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2874-132">Your PowerShell profile is a script that runs every time PowerShell starts.</span></span> <span data-ttu-id="e2874-133">[Altre informazioni sui profili di PowerShell](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="e2874-133">[Learn more about PowerShell profiles](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span></span>

<span data-ttu-id="e2874-134">Nel profilo di PowerShell aggiungi quanto segue alla fine del file:</span><span class="sxs-lookup"><span data-stu-id="e2874-134">In your PowerShell profile, add the following to the end of the file:</span></span>

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```

<span data-ttu-id="e2874-135">A questo punto, ogni nuova istanza inizia con l'importazione di Posh-Git e Oh-My-Posh e continua con l'impostazione del tema Paradox di Oh-My-Posh.</span><span class="sxs-lookup"><span data-stu-id="e2874-135">Now, each new instance starts by importing Posh-Git and Oh-My-Posh, then setting the Paradox theme from Oh-My-Posh.</span></span> <span data-ttu-id="e2874-136">Oh-My-Posh include diversi [temi predefiniti](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span><span class="sxs-lookup"><span data-stu-id="e2874-136">Oh-My-Posh comes with several [built-in themes](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span></span>

### <a name="set-cascadia-code-pl-as-fontface-in-settings"></a><span data-ttu-id="e2874-137">Impostare Cascadia Code PL come tipo di carattere nelle impostazioni</span><span class="sxs-lookup"><span data-stu-id="e2874-137">Set Cascadia Code PL as fontFace in settings</span></span>

<span data-ttu-id="e2874-138">Per impostare il tipo di carattere Cascadia Code PL da usare con PowerLine (dopo il download, la decompressione e l'installazione nel sistema), sarà necessario aprire le [impostazioni del profilo](../customize-settings/profile-settings.md) nel file settings.json selezionando **Impostazioni** nel menu a discesa di Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="e2874-138">To set the Cascadia Code PL font for use with PowerLine (after downloading, unzipping, and installing on your system), you will need to open your [profile settings](../customize-settings/profile-settings.md) in your settings.json file by selecting **Settings** (Ctrl+,) from your Windows Terminal drop-down menu.</span></span>

<span data-ttu-id="e2874-139">Una volta aperto il file settings.json, trovare il profilo di Windows PowerShell e aggiungere `"fontFace": "Cascadia Code PL"` per designare Cascadia Code PL come tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="e2874-139">Once your settings.json file opens, find the Windows PowerShell profile and add: `"fontFace": "Cascadia Code PL"` to designate Cascadia Code PL as the font.</span></span> <span data-ttu-id="e2874-140">In questo modo saranno disponibili i glifi Powerline di Cascadia Code.</span><span class="sxs-lookup"><span data-stu-id="e2874-140">This will provide those nice Cascadia Code Powerline glyphs.</span></span> <span data-ttu-id="e2874-141">La modifica sarà osservabile nel terminale non appena si seleziona **Salva** nell'editor.</span><span class="sxs-lookup"><span data-stu-id="e2874-141">You should notice the change in your terminal as soon as you select **Save** in your editor.</span></span>

<span data-ttu-id="e2874-142">Il file settings.json del profilo di Windows PowerShell sarà ora simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="e2874-142">Your Windows PowerShell profile settings.json file should now look like this:</span></span>

```json
{
    // Make changes here to the powershell.exe profile.
    "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
    "name": "Windows PowerShell",
    "commandline": "powershell.exe",
    "fontFace": "Cascadia Code PL",
    "hidden": false
},
```

## <a name="set-up-powerline-in-wsl-ubuntu"></a><span data-ttu-id="e2874-143">Configurare Powerline in WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="e2874-143">Set up Powerline in WSL Ubuntu</span></span>

### <a name="wsl-ubuntu-prerequisites"></a><span data-ttu-id="e2874-144">Prerequisiti di WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="e2874-144">WSL Ubuntu prerequisites</span></span>

<span data-ttu-id="e2874-145">Ubuntu include diverse opzioni Powerline da cui eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e2874-145">Ubuntu has several Powerline options to install from.</span></span> <span data-ttu-id="e2874-146">Per questa esercitazione useremo Go e Powerline-Go:</span><span class="sxs-lookup"><span data-stu-id="e2874-146">This tutorial will be using Go and Powerline-Go:</span></span>

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

### <a name="customize-your-ubuntu-prompt"></a><span data-ttu-id="e2874-147">Personalizzare il prompt di Ubuntu</span><span class="sxs-lookup"><span data-stu-id="e2874-147">Customize your Ubuntu prompt</span></span>

<span data-ttu-id="e2874-148">Apri il file `~/.bashrc` con `nano ~/.bashrc` o con l'editor di testo che preferisci.</span><span class="sxs-lookup"><span data-stu-id="e2874-148">Open your `~/.bashrc` file with `nano ~/.bashrc` or the text editor of your choice.</span></span> <span data-ttu-id="e2874-149">Si tratta di uno script bash eseguito ogni volta che viene avviato bash.</span><span class="sxs-lookup"><span data-stu-id="e2874-149">This is a bash script that runs every time bash starts.</span></span> <span data-ttu-id="e2874-150">Aggiungi quanto segue, ma tieni presente che GOPATH potrebbe essere già presente:</span><span class="sxs-lookup"><span data-stu-id="e2874-150">Add the following, though beware that GOPATH may already exist:</span></span>

```bash
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

## <a name="additional-resources"></a><span data-ttu-id="e2874-151">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="e2874-151">Additional resources</span></span>

* <span data-ttu-id="e2874-152">Articolo su [come creare un prompt efficace in Terminale Windows](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx) di Scott Hanselman</span><span class="sxs-lookup"><span data-stu-id="e2874-152">[Scott Hanselman's "How to make a pretty prompt in Windows Terminal"](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx)</span></span>

* [<span data-ttu-id="e2874-153">Come modificare/configurare il prompt personalizzato di bash (PS1) in Linux</span><span class="sxs-lookup"><span data-stu-id="e2874-153">How to change/set up bash custom prompt (PS1) in Linux</span></span>](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)
