---
title: Terminale Windows - Configurazione di Powerline
description: Questa esercitazione illustra come configurare Powerline in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 1/28/2021
ms.topic: tutorial
ms.openlocfilehash: 0032a8253cb8d8c6311278267034043e5b0ee99a
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974912"
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

> [!VIDEO https://www.youtube.com/embed/lu__oGZVT98]

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
> Se non è già stato fatto, può essere necessario installare NuGet. La riga di comando di PowerShell chiederà se si vuole installare NuGet in questo caso. Selezionare Sì. Può anche essere necessario confermare l'installazione di moduli di [PSGallery](https://docs.microsoft.com/powershell/scripting/gallery/getting-started), un 'repository non attendibile'. Selezionare Sì.

[Posh-Git](https://github.com/dahlbyk/posh-git) aggiunge al prompt informazioni sullo stato di GIT, nonché il completamento tramite tasto TAB per comandi, parametri, repository remoti e nomi di ramo GIT. [Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) offre funzionalità relative al tema per il prompt di PowerShell.

Se usi PowerShell Core, installa PSReadline:

```powershell
Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
```

[PSReadline](https://docs.microsoft.com/powershell/module/psreadline) consente di personalizzare l'ambiente di modifica da riga di comando in PowerShell.

### <a name="customize-your-powershell-prompt"></a>Personalizzare il prompt di PowerShell

Apri il profilo di PowerShell con `notepad $PROFILE` o con l'editor di testo che preferisci. Non si tratta del profilo di Terminale Windows. Il profilo di PowerShell è uno script eseguito ogni volta che viene avviato PowerShell. [Altre informazioni sui profili di PowerShell](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles).

Nel profilo di PowerShell aggiungi quanto segue alla fine del file:

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```

A questo punto, ogni nuova istanza inizia con l'importazione di Posh-Git e Oh-My-Posh e continua con l'impostazione del tema Paradox di Oh-My-Posh. Oh-My-Posh include diversi [temi predefiniti](https://github.com/JanDeDobbeleer/oh-my-posh#themes).

### <a name="set-cascadia-code-pl-as-your-font"></a>Imposta Cascadia codice PL come tipo di carattere

Per impostare il tipo di carattere Cascadia del codice PL da usare con PowerLine (dopo il download, la decompressione e l'installazione nel sistema), è necessario aprire le [impostazioni del profilo](../customize-settings/profile-appearance.md) nel settings.jsfile selezionando **Impostazioni** (CTRL +,) dal menu a discesa del terminale di Windows. Questa operazione può essere eseguita anche usando l'interfaccia utente di impostazioni se è abilitata.

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
> [!TIP]
> Se si usa anche il terminale integrato in Visual Studio Code, è necessario aggiungere `"terminal.integrated.fontFamily": "Cascadia Code PL"` alle impostazioni Visual Studio Code per assicurarsi che Powerline funzioni anche in questo caso.

## <a name="set-up-powerline-in-wsl-ubuntu"></a>Configurare Powerline in WSL Ubuntu

### <a name="wsl-ubuntu-prerequisites"></a>Prerequisiti di WSL Ubuntu

Ubuntu include diverse opzioni Powerline da cui eseguire l'installazione. Per questa esercitazione useremo Go e Powerline-Go:

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

> [!TIP]
> Se si usa Ubuntu 18,04 o 16,04, è necessario installare prima la versione corretta di Golang:
> ```bash
> sudo add-apt-repository ppa:longsleep/golang-backports
> sudo apt update
> ```

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
