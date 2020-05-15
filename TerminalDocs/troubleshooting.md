---
title: Risoluzione dei problemi di Terminale Windows
description: Informazioni sulle correzioni per i problemi comuni di Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 29d3ce72210c30fcbf38393d733c6157670465bb
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415876"
---
# <a name="troubleshooting-in-windows-terminal"></a><span data-ttu-id="91ce3-103">Risoluzione dei problemi di Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="91ce3-103">Troubleshooting in Windows Terminal</span></span>

<span data-ttu-id="91ce3-104">Questa guida descrive alcuni errori e problemi comuni che possono verificarsi in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="91ce3-104">This guide addresses some of the common errors and obstacles you may encounter when using Windows Terminal.</span></span>

## <a name="set-your-wsl-distribution-to-start-in-the-home--directory-when-launched"></a><span data-ttu-id="91ce3-105">Impostare la distribuzione di WSL in modo che venga avviata nella home directory `~`</span><span class="sxs-lookup"><span data-stu-id="91ce3-105">Set your WSL distribution to start in the home `~` directory when launched</span></span>

<span data-ttu-id="91ce3-106">Per impostazione predefinita, la directory `startingDirectory` di un profilo è `%USERPROFILE%` (`C:\Users\<YourUsername>`),</span><span class="sxs-lookup"><span data-stu-id="91ce3-106">By default, the `startingDirectory` of a profile is `%USERPROFILE%` (`C:\Users\<YourUsername>`).</span></span> <span data-ttu-id="91ce3-107">ovvero un percorso di Windows.</span><span class="sxs-lookup"><span data-stu-id="91ce3-107">This is a Windows path.</span></span> <span data-ttu-id="91ce3-108">Per WSL, tuttavia, è consigliabile usare invece il percorso della home directory WSL.</span><span class="sxs-lookup"><span data-stu-id="91ce3-108">For WSL, however, you may want to use the WSL home path instead.</span></span> <span data-ttu-id="91ce3-109">`startingDirectory` accetta solo un percorso di tipo Windows, quindi l'impostazione per l'avvio in una distribuzione WSL richiede un prefisso.</span><span class="sxs-lookup"><span data-stu-id="91ce3-109">`startingDirectory` only accepts a Windows-style path, so setting it to start within a WSL distribution requires a prefix.</span></span>

<span data-ttu-id="91ce3-110">A partire da Windows 10 versione 1903, puoi gestire i file system delle distribuzioni WSL usando il prefisso `\\wsl$\`.</span><span class="sxs-lookup"><span data-stu-id="91ce3-110">Beginning in Windows 10 version 1903, the file systems of WSL distributions can be addressed using the `\\wsl$\` prefix.</span></span> <span data-ttu-id="91ce3-111">Per qualsiasi distribuzione WSL con il nome `DistroName`, usa `\\wsl$\DistroName` come percorso di Windows che punta alla radice del file system della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="91ce3-111">For any WSL distribution with the name `DistroName`, use `\\wsl$\DistroName` as a Windows path that points to the root of that distribution's file system.</span></span>

<span data-ttu-id="91ce3-112">Ad esempio, l'impostazione seguente avvierà la distribuzione "Ubuntu-18.04" nel percorso file della home directory:</span><span class="sxs-lookup"><span data-stu-id="91ce3-112">For example, the following setting will launch the "Ubuntu-18.04" distribution in its home file path:</span></span>

```json
{
    "name": "Ubuntu-18.04",
    "commandline" : "wsl -d Ubuntu-18.04",
    "startingDirectory" : "//wsl$/Ubuntu-18.04/home/<Your Ubuntu Username>",
}
```

## <a name="setting-the-tab-title"></a><span data-ttu-id="91ce3-113">Impostazione del titolo della scheda</span><span class="sxs-lookup"><span data-stu-id="91ce3-113">Setting the tab title</span></span>

<span data-ttu-id="91ce3-114">Per fare in modo che il titolo della scheda venga impostato automaticamente dalla shell, [vedi questa esercitazione](./tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="91ce3-114">To have the shell automatically set your tab title, [visit the set the tab title tutorial](./tutorials/tab-title.md).</span></span> <span data-ttu-id="91ce3-115">Se vuoi impostare un titolo personalizzato per la scheda, apri il file settings.json e segui questa procedura:</span><span class="sxs-lookup"><span data-stu-id="91ce3-115">If you want to set your own tab title, open the settings.json file and follow these steps:</span></span>

1. <span data-ttu-id="91ce3-116">Nel profilo di una riga di comando a scelta aggiungi `"suppressApplicationTitle": true` per eliminare gli eventi di modifica del titolo che vengono inviati dalla shell.</span><span class="sxs-lookup"><span data-stu-id="91ce3-116">In the profile for the command line of your choice, add `"suppressApplicationTitle": true` to suppress any title change events that get sent from the shell.</span></span> <span data-ttu-id="91ce3-117">Se aggiungi *solo* questa impostazione al profilo, il titolo della scheda verrà impostato sul nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="91ce3-117">Adding *only* this setting to your profile will set the tab title to the name of your profile.</span></span>

2. <span data-ttu-id="91ce3-118">Se vuoi impostare un titolo di scheda personalizzato e non il nome del profilo, aggiungi `"tabTitle": "TITLE"`.</span><span class="sxs-lookup"><span data-stu-id="91ce3-118">If you want a custom tab title that is not the name of your profile, add `"tabTitle": "TITLE"`.</span></span> <span data-ttu-id="91ce3-119">Sostituisci "TITLE" con il titolo preferito per la scheda.</span><span class="sxs-lookup"><span data-stu-id="91ce3-119">Replacing "TITLE" with your preferred tab title.</span></span>

## <a name="command-line-arguments-in-powershell"></a><span data-ttu-id="91ce3-120">Argomenti della riga di comando in PowerShell</span><span class="sxs-lookup"><span data-stu-id="91ce3-120">Command line arguments in PowerShell</span></span>

<span data-ttu-id="91ce3-121">Per informazioni sul funzionamento degli argomenti della riga di comando in PowerShell, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="91ce3-121">Visit the [Command line arguments page](./command-line-arguments.md) to learn how command line arguments operate in PowerShell.</span></span>

## <a name="command-line-arguments-in-wsl"></a><span data-ttu-id="91ce3-122">Argomenti della riga di comando in WSL</span><span class="sxs-lookup"><span data-stu-id="91ce3-122">Command line arguments in WSL</span></span>

<span data-ttu-id="91ce3-123">Per informazioni sul funzionamento degli argomenti della riga di comando in WSL, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="91ce3-123">Visit the [Command line arguments page](./command-line-arguments.md) to learn how command line arguments operate in WSL.</span></span>

## <a name="problem-setting-startingdirectory"></a><span data-ttu-id="91ce3-124">Problema con l'impostazione di `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="91ce3-124">Problem setting `startingDirectory`</span></span>

<span data-ttu-id="91ce3-125">Se l'impostazione di `startingDirectory` viene ignorata nel profilo, verifica prima di tutto che la sintassi del file settings.json sia corretta.</span><span class="sxs-lookup"><span data-stu-id="91ce3-125">If the `startingDirectory` is being ignored in your profile, first check to make sure your settings.json's syntax is correct.</span></span> <span data-ttu-id="91ce3-126">Per semplificare la verifica della sintassi, `"$schema": "https://aka.ms/terminal-profiles-schema"` viene inserito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="91ce3-126">To help you check this syntax, `"$schema": "https://aka.ms/terminal-profiles-schema"` is automatically injected.</span></span> <span data-ttu-id="91ce3-127">Alcune applicazioni, ad esempio [Visual Studio Code](https://code.visualstudio.com/download), possono usare lo schema inserito per convalidare il file JSON durante le modifiche.</span><span class="sxs-lookup"><span data-stu-id="91ce3-127">Some applications, like [Visual Studio Code](https://code.visualstudio.com/download), can use that injected schema to validate your json file as you make edits.</span></span>

<span data-ttu-id="91ce3-128">Se le impostazioni sono corrette, è possibile che sia in esecuzione uno script di avvio che imposta separatamente la directory iniziale del terminale.</span><span class="sxs-lookup"><span data-stu-id="91ce3-128">If your settings are correct, you may be running a startup script that sets the starting directory of your terminal separately.</span></span> <span data-ttu-id="91ce3-129">PowerShell, ad esempio, prevede un proprio concetto separato dei profili.</span><span class="sxs-lookup"><span data-stu-id="91ce3-129">For example, PowerShell has its own separate concept of profiles.</span></span> <span data-ttu-id="91ce3-130">Se cambi qui la directory iniziale, questa impostazione avrà la precedenza su quella definita in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="91ce3-130">If you are changing your starting directory there, it will take precedence over the setting defined in Windows Terminal.</span></span>

<span data-ttu-id="91ce3-131">In alternativa, se esegui uno script usando l'impostazione del profilo `commandline`, è possibile che stia impostando qui la posizione.</span><span class="sxs-lookup"><span data-stu-id="91ce3-131">Alternatively, if you are running a script using the `commandline` profile setting, it may be that you are setting the location there.</span></span> <span data-ttu-id="91ce3-132">Analogamente ai profili PowerShell, i comandi hanno la precedenza sull'impostazione del profilo `startingDirectory`.</span><span class="sxs-lookup"><span data-stu-id="91ce3-132">Similar to PowerShell profiles, your commands there take precedence over the `startingDirectory` profile setting.</span></span>

<span data-ttu-id="91ce3-133">Lo scopo di `startingDirectory` è avviare una nuova istanza di Terminale Windows nella directory specificata.</span><span class="sxs-lookup"><span data-stu-id="91ce3-133">The purpose of `startingDirectory` is to launch a new Windows Terminal instance in the given directory.</span></span> <span data-ttu-id="91ce3-134">Se il terminale esegue qualsiasi codice che cambia la directory, potrebbe essere questa la causa del problema.</span><span class="sxs-lookup"><span data-stu-id="91ce3-134">If the terminal runs any code that changes its directory, that may be a good place to take a look.</span></span>

## <a name="ctrl-does-not-increase-the-font-size"></a><span data-ttu-id="91ce3-135">CTRL+= non aumenta le dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="91ce3-135">Ctrl+= does not increase the font size</span></span>

<span data-ttu-id="91ce3-136">Se usi un layout di tastiera tedesco, potresti riscontrare questo problema.</span><span class="sxs-lookup"><span data-stu-id="91ce3-136">If you are using a German keyboard layout, you may run into this problem.</span></span> <span data-ttu-id="91ce3-137">La combinazione <kbd>CTRL+=</kbd> viene deserializzata come <kbd>CTRL+MAIUSC+0</kbd> se il layout di tastiera principale è impostato sul tedesco.</span><span class="sxs-lookup"><span data-stu-id="91ce3-137"><kbd>ctrl+=</kbd> gets deserialized as <kbd>ctrl+shift+0</kbd> if your main keyboard layout is set to German.</span></span> <span data-ttu-id="91ce3-138">Si tratta del mapping corretto per le tastiere tedesche.</span><span class="sxs-lookup"><span data-stu-id="91ce3-138">This is the correct mapping for German keyboards.</span></span>

<span data-ttu-id="91ce3-139">Ancora più importante, l'app non riceve mai la sequenza di tasti <kbd>CTRL+MAIUSC+0</kbd>.</span><span class="sxs-lookup"><span data-stu-id="91ce3-139">More importantly, the app never receives the <kbd>ctrl+shift+0</kbd> keystroke.</span></span> <span data-ttu-id="91ce3-140">Il motivo è che la combinazione <kbd>CTRL+MAIUSC+0</kbd> è riservata da Windows se sono attivi più layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="91ce3-140">This is because <kbd>ctrl+shift+0</kbd> is reserved by Windows if you have multiple keyboard layouts active.</span></span>

<span data-ttu-id="91ce3-141">Se vuoi disabilitare questa funzionalità per il corretto funzionamento di `Ctrl+=`, segui le istruzioni su come cambiare i tasti di scelta rapida per sostituire il layout della tastiera in Windows 10 in questo [post di blog](https://winaero.com/blog/change-hotkeys-switch-keyboard-layout-windows-10/).</span><span class="sxs-lookup"><span data-stu-id="91ce3-141">If you would like to disable this feature in order for `Ctrl+=` to work properly, follow the instructions for "Change Hotkeys to Switch Keyboard Layout in Windows 10" in this [blog post](https://winaero.com/blog/change-hotkeys-switch-keyboard-layout-windows-10/).</span></span>

<span data-ttu-id="91ce3-142">Imposta l'opzione 'Cambia layout di tastiera' su 'Non assegnato' (o su una combinazione senza <kbd>CTRL+MAIUSC</kbd>), quindi seleziona **OK** e poi **Applica**.</span><span class="sxs-lookup"><span data-stu-id="91ce3-142">Change the 'Switch Keyboard Layout' option to 'Not Assigned' (or off of <kbd>ctrl+shift</kbd>), then select **OK** and then **Apply**.</span></span> <span data-ttu-id="91ce3-143">La combinazione di tasti <kbd>CTRL+MAIUSC+0</kbd> dovrebbe ora funzionare e viene passata al terminale.</span><span class="sxs-lookup"><span data-stu-id="91ce3-143"><kbd>ctrl+shift+0</kbd> should now work as a key binding and is passed through to the terminal.</span></span>

<span data-ttu-id="91ce3-144">Se al contrario usi questa funzionalità di tasti di scelta rapida per più lingue di input, puoi [configurare combinazioni di tasti personalizzate](./customize-settings/key-bindings.md) nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="91ce3-144">On the other hand, if you do use this hotkey feature for multiple input languages, you can [configure your own custom key binding](./customize-settings/key-bindings.md) in your settings.json file.</span></span>
