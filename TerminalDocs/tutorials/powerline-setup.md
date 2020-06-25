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
# <a name="tutorial-set-up-powerline-in-windows-terminal"></a>Esercitazione: Configurare Powerline in Terminale Windows

Powerline offre un'esperienza personalizzata del prompt dei comandi che include i prompt e la codifica a colori per gli stati di GIT.

![Terminale Windows - PowerShell per Powerline](./../images/powerline-powershell.png)

In questa esercitazione verranno illustrate le procedure per:

> [!div class="checklist"]
>
> * Configurare Powerline in PowerShell
> * Configurare Powerline in WSL Ubuntu
> * Aggiungere i glifi Powerline mancanti

## <a name="prerequisites"></a>Prerequisiti

### <a name="install-a-powerline-font"></a>Installare un tipo di carattere Powerline

Powerline usa i glifi per applicare stili al prompt. Se il tipo di carattere non include glifi Powerline, è possibile che nel prompt vengano visualizzati diversi caratteri Unicode '&#x25AF;' sostitutivi. Anche se [Cascadia Mono](./../cascadia-code.md) non include i glifi Powerline, puoi installare Cascadia Code PL o Cascadia Mono PL, che invece li includono. Questi tipi di carattere possono essere installati dalla [pagina delle versioni di Cascadia Code in GitHub](https://github.com/microsoft/cascadia-code/releases).

## <a name="set-up-powerline-in-powershell"></a>Configurare Powerline in PowerShell

### <a name="powershell-prerequisites"></a>Prerequisiti di PowerShell

Se non lo hai già fatto, [installa GIT per Windows](https://git-scm.com/downloads).

Usa PowerShell per installare Posh-Git e Oh-My-Posh:

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

> [!TIP]
> Se non è già stato fatto, può essere necessario installare NuGet. La riga di comando di PowerShell chiederà se si vuole installare NuGet in questo caso. Selezionare Sì. Può anche essere necessario confermare l'installazione di moduli di [PSGallery](https://docs.microsoft.com/powershell/scripting/gallery/getting-started?view=powershell-7), un 'repository non attendibile'. Selezionare Sì.

[Posh-Git](https://github.com/dahlbyk/posh-git) aggiunge al prompt informazioni sullo stato di GIT, nonché il completamento tramite tasto TAB per comandi, parametri, repository remoti e nomi di ramo GIT. [Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) offre funzionalità relative al tema per il prompt di PowerShell.

Se usi PowerShell Core, installa PSReadline:

```powershell
Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
```

[PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) consente di personalizzare l'ambiente di modifica da riga di comando in PowerShell.

### <a name="customize-your-powershell-prompt"></a>Personalizzare il prompt di PowerShell

Apri il profilo di PowerShell con `notepad $PROFILE` o con l'editor di testo che preferisci. Non si tratta del profilo di Terminale Windows. Il profilo di PowerShell è uno script eseguito ogni volta che viene avviato PowerShell. [Altre informazioni sui profili di PowerShell](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).

Nel profilo di PowerShell aggiungi quanto segue alla fine del file:

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```

A questo punto, ogni nuova istanza inizia con l'importazione di Posh-Git e Oh-My-Posh e continua con l'impostazione del tema Paradox di Oh-My-Posh. Oh-My-Posh include diversi [temi predefiniti](https://github.com/JanDeDobbeleer/oh-my-posh#themes).

### <a name="set-cascadia-code-pl-as-fontface-in-settings"></a>Impostare Cascadia Code PL come tipo di carattere nelle impostazioni

Per impostare il tipo di carattere Cascadia Code PL da usare con PowerLine (dopo il download, la decompressione e l'installazione nel sistema), sarà necessario aprire le [impostazioni del profilo](../customize-settings/profile-settings.md) nel file settings.json selezionando **Impostazioni** nel menu a discesa di Terminale Windows.

Una volta aperto il file settings.json, trovare il profilo di Windows PowerShell e aggiungere `"fontFace": "Cascadia Code PL"` per designare Cascadia Code PL come tipo di carattere. In questo modo saranno disponibili i glifi Powerline di Cascadia Code. La modifica sarà osservabile nel terminale non appena si seleziona **Salva** nell'editor.

Il file settings.json del profilo di Windows PowerShell sarà ora simile al seguente:

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

## <a name="set-up-powerline-in-wsl-ubuntu"></a>Configurare Powerline in WSL Ubuntu

### <a name="wsl-ubuntu-prerequisites"></a>Prerequisiti di WSL Ubuntu

Ubuntu include diverse opzioni Powerline da cui eseguire l'installazione. Per questa esercitazione useremo Go e Powerline-Go:

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

### <a name="customize-your-ubuntu-prompt"></a>Personalizzare il prompt di Ubuntu

Apri il file `~/.bashrc` con `nano ~/.bashrc` o con l'editor di testo che preferisci. Si tratta di uno script bash eseguito ogni volta che viene avviato bash. Aggiungi quanto segue, ma tieni presente che GOPATH potrebbe essere già presente:

```bash
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

## <a name="additional-resources"></a>Risorse aggiuntive

* Articolo su [come creare un prompt efficace in Terminale Windows](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx) di Scott Hanselman

* [Come modificare/configurare il prompt personalizzato di bash (PS1) in Linux](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)
