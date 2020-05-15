---
title: Terminale Windows - Configurazione di Powerline
description: Questa esercitazione illustra come configurare Powerline in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: f2004927097b13ba896b628bea0d7bd9f70d7266
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416266"
---
# <a name="tutorial-set-up-powerline-in-windows-terminal"></a><span data-ttu-id="292fc-103">Esercitazione: Configurare Powerline in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="292fc-103">Tutorial: Set up Powerline in Windows Terminal</span></span>

<span data-ttu-id="292fc-104">Powerline offre un'esperienza personalizzata del prompt dei comandi che include i prompt e la codifica a colori per gli stati di GIT.</span><span class="sxs-lookup"><span data-stu-id="292fc-104">Powerline provides a customized command prompt experience providing Git status color-coding and prompts.</span></span>

![Terminale Windows - PowerShell per Powerline](./../images/powerline-powershell.png)

<span data-ttu-id="292fc-106">In questa esercitazione verranno illustrate le procedure per:</span><span class="sxs-lookup"><span data-stu-id="292fc-106">In this tutorial, you learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="292fc-107">Configurare Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="292fc-107">Set up Powerline in PowerShell</span></span>
> * <span data-ttu-id="292fc-108">Configurare Powerline in WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="292fc-108">Set up Powerline in Ubuntu/WSL</span></span>
> * <span data-ttu-id="292fc-109">Aggiungere i glifi Powerline mancanti</span><span class="sxs-lookup"><span data-stu-id="292fc-109">Add missing Powerline glyphs</span></span>

## <a name="prerequisites"></a><span data-ttu-id="292fc-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="292fc-110">Prerequisites</span></span>

### <a name="install-a-powerline-font"></a><span data-ttu-id="292fc-111">Installare un tipo di carattere Powerline</span><span class="sxs-lookup"><span data-stu-id="292fc-111">Install a Powerline font</span></span>

<span data-ttu-id="292fc-112">Powerline usa i glifi per applicare stili al prompt.</span><span class="sxs-lookup"><span data-stu-id="292fc-112">Powerline uses glyphs in order to style the prompt.</span></span> <span data-ttu-id="292fc-113">Se il tipo di carattere usato non include i glifi Powerline, è possibile nel prompt che vengano visualizzati diversi caratteri di sostituzione Unicode ''.</span><span class="sxs-lookup"><span data-stu-id="292fc-113">If your font does not include Powerline glyphs, you may see several Unicode replacement characters '' throughout your prompt.</span></span> <span data-ttu-id="292fc-114">Anche se [Cascadia Mono](./../cascadia-code.md) non include i glifi Powerline, puoi installare Cascadia Code PL o Cascadia Mono PL, che invece li includono.</span><span class="sxs-lookup"><span data-stu-id="292fc-114">Though [Cascadia Mono](./../cascadia-code.md) does not include Powerline glyphs, you can install Cascadia Code PL or Cascadia Mono PL, which have the Powerline glyphs included.</span></span> <span data-ttu-id="292fc-115">Questi tipi di carattere possono essere installati dalla [pagina delle versioni di Cascadia Code in GitHub](https://github.com/microsoft/cascadia-code/releases).</span><span class="sxs-lookup"><span data-stu-id="292fc-115">These fonts can be installed from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span>

## <a name="set-up-powerline-in-powershell"></a><span data-ttu-id="292fc-116">Configurare Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="292fc-116">Set up Powerline in PowerShell</span></span>

### <a name="powershell-prerequisites"></a><span data-ttu-id="292fc-117">Prerequisiti di PowerShell</span><span class="sxs-lookup"><span data-stu-id="292fc-117">PowerShell prerequisites</span></span>

<span data-ttu-id="292fc-118">Se non lo hai già fatto, [installa GIT per Windows](https://git-scm.com/downloads).</span><span class="sxs-lookup"><span data-stu-id="292fc-118">If you don't already have it, [install Git for Windows](https://git-scm.com/downloads).</span></span>

<span data-ttu-id="292fc-119">Usa PowerShell per installare Posh-Git e Oh-My-Posh:</span><span class="sxs-lookup"><span data-stu-id="292fc-119">Using PowerShell, install Posh-Git and Oh-My-Posh:</span></span>

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

<span data-ttu-id="292fc-120">[Posh-Git](https://github.com/dahlbyk/posh-git) aggiunge al prompt informazioni sullo stato di GIT, nonché il completamento tramite tasto TAB per comandi, parametri, repository remoti e nomi di ramo GIT.</span><span class="sxs-lookup"><span data-stu-id="292fc-120">[Posh-Git](https://github.com/dahlbyk/posh-git) adds Git status information to your prompt as well as tab-completion for Git commands, parameters, remotes, and branch names.</span></span> <span data-ttu-id="292fc-121">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) offre funzionalità relative al tema per il prompt di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="292fc-121">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) provides theme capabilities for your PowerShell prompt.</span></span>

<span data-ttu-id="292fc-122">Se usi PowerShell Core, installa PSReadline:</span><span class="sxs-lookup"><span data-stu-id="292fc-122">If you are using PowerShell Core, install PSReadline:</span></span>

```powershell
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
```

<span data-ttu-id="292fc-123">[PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) consente di personalizzare l'ambiente di modifica da riga di comando in PowerShell.</span><span class="sxs-lookup"><span data-stu-id="292fc-123">[PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) lets you customize the command line editing environment in PowerShell.</span></span>

### <a name="customize-your-powershell-prompt"></a><span data-ttu-id="292fc-124">Personalizzare il prompt di PowerShell</span><span class="sxs-lookup"><span data-stu-id="292fc-124">Customize your PowerShell prompt</span></span>

<span data-ttu-id="292fc-125">Apri il profilo di PowerShell con `notepad $PROFILE` o con l'editor di testo che preferisci.</span><span class="sxs-lookup"><span data-stu-id="292fc-125">Open your PowerShell profile with `notepad $PROFILE` or the text editor of your choice.</span></span> <span data-ttu-id="292fc-126">Non si tratta del profilo di Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="292fc-126">This is not your Windows Terminal profile.</span></span> <span data-ttu-id="292fc-127">Il profilo di PowerShell è uno script eseguito ogni volta che viene avviato PowerShell.</span><span class="sxs-lookup"><span data-stu-id="292fc-127">Your PowerShell profile is a script that runs every time PowerShell starts.</span></span> <span data-ttu-id="292fc-128">[Altre informazioni sui profili di PowerShell](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="292fc-128">[Learn more about PowerShell profiles](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span></span>

<span data-ttu-id="292fc-129">Nel profilo di PowerShell aggiungi quanto segue alla fine del file:</span><span class="sxs-lookup"><span data-stu-id="292fc-129">In your PowerShell profile, add the following to the end of the file:</span></span>

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```

<span data-ttu-id="292fc-130">A questo punto, ogni nuova istanza inizia con l'importazione di Posh-Git e Oh-My-Posh e continua con l'impostazione del tema Paradox di Oh-My-Posh.</span><span class="sxs-lookup"><span data-stu-id="292fc-130">Now, each new instance starts by importing Posh-Git and Oh-My-Posh, then setting the Paradox theme from Oh-My-Posh.</span></span> <span data-ttu-id="292fc-131">Oh-My-Posh include diversi [temi predefiniti](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span><span class="sxs-lookup"><span data-stu-id="292fc-131">Oh-My-Posh comes with several [built-in themes](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span></span>

## <a name="set-up-powerline-in-wsl-ubuntu"></a><span data-ttu-id="292fc-132">Configurare Powerline in WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="292fc-132">Set up Powerline in WSL Ubuntu</span></span>

### <a name="wsl-ubuntu-prerequisites"></a><span data-ttu-id="292fc-133">Prerequisiti di WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="292fc-133">WSL Ubuntu prerequisites</span></span>

<span data-ttu-id="292fc-134">Ubuntu include diverse opzioni Powerline da cui eseguire l'installazione.</span><span class="sxs-lookup"><span data-stu-id="292fc-134">Ubuntu has several Powerline options to install from.</span></span> <span data-ttu-id="292fc-135">Per questa esercitazione useremo Go e Powerline-Go:</span><span class="sxs-lookup"><span data-stu-id="292fc-135">This tutorial will be using Go and Powerline-Go:</span></span>

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

### <a name="customize-your-ubuntu-prompt"></a><span data-ttu-id="292fc-136">Personalizzare il prompt di Ubuntu</span><span class="sxs-lookup"><span data-stu-id="292fc-136">Customize your Ubuntu prompt</span></span>

<span data-ttu-id="292fc-137">Apri il file `~/.bashrc` con `nano ~/.bashrc` o con l'editor di testo che preferisci.</span><span class="sxs-lookup"><span data-stu-id="292fc-137">Open your `~/.bashrc` file with `nano ~/.bashrc` or the text editor of your choice.</span></span> <span data-ttu-id="292fc-138">Si tratta di uno script bash eseguito ogni volta che viene avviato bash.</span><span class="sxs-lookup"><span data-stu-id="292fc-138">This is a bash script that runs every time bash starts.</span></span> <span data-ttu-id="292fc-139">Aggiungi quanto segue, ma tieni presente che GOPATH potrebbe essere già presente:</span><span class="sxs-lookup"><span data-stu-id="292fc-139">Add the following, though beware that GOPATH may already exist:</span></span>

```bash
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

## <a name="additional-resources"></a><span data-ttu-id="292fc-140">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="292fc-140">Additional resources</span></span>

* <span data-ttu-id="292fc-141">Articolo su [come creare un prompt efficace in Terminale Windows](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx) di Scott Hanselman</span><span class="sxs-lookup"><span data-stu-id="292fc-141">[Scott Hanselman's "How to make a pretty prompt in Windows Terminal"](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx)</span></span>

* [<span data-ttu-id="292fc-142">Come modificare/configurare il prompt personalizzato di bash (PS1) in Linux</span><span class="sxs-lookup"><span data-stu-id="292fc-142">How to change/set up bash custom prompt (PS1) in Linux</span></span>](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)
