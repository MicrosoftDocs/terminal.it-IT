---
title: Risoluzione dei problemi di Terminale Windows
description: Informazioni sulle correzioni per i problemi comuni di Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 1/28/2021
ms.topic: overview
ms.localizationpriority: high
ms.openlocfilehash: f2c83f4ec4fc4596ce4a66764c49f73cc5d1fbf5
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "98981004"
---
# <a name="troubleshooting-in-windows-terminal"></a><span data-ttu-id="30984-103">Risoluzione dei problemi di Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="30984-103">Troubleshooting in Windows Terminal</span></span>

<span data-ttu-id="30984-104">Questa guida descrive alcuni errori e problemi comuni che possono verificarsi in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="30984-104">This guide addresses some of the common errors and obstacles you may encounter when using Windows Terminal.</span></span>

## <a name="open-the-settings-ui"></a><span data-ttu-id="30984-105">Aprire l'interfaccia utente delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="30984-105">Open the settings UI</span></span>

<span data-ttu-id="30984-106">Al momento, l'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="30984-106">At the moment, the settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="30984-107">Per aprire l'interfaccia utente delle impostazioni, è necessario aggiungere l' `"openSettings"` azione alla `"actions"` matrice per aprirla con il riquadro comandi o la tastiera.</span><span class="sxs-lookup"><span data-stu-id="30984-107">In order to open the settings UI, you will have to add the `"openSettings"` action to your `"actions"` array in order to open it with the command palette or keyboard.</span></span>

```
{ "command": { "action": "openSettings", "target": "settingsUI" }, "keys": "ctrl+shift+," },
```

## <a name="set-your-wsl-distribution-to-start-in-the-home--directory-when-launched"></a><span data-ttu-id="30984-108">Impostare la distribuzione di WSL in modo che venga avviata nella home directory `~`</span><span class="sxs-lookup"><span data-stu-id="30984-108">Set your WSL distribution to start in the home `~` directory when launched</span></span>

<span data-ttu-id="30984-109">Per impostazione predefinita, la directory `startingDirectory` di un profilo è `%USERPROFILE%` (`C:\Users\<YourUsername>`),</span><span class="sxs-lookup"><span data-stu-id="30984-109">By default, the `startingDirectory` of a profile is `%USERPROFILE%` (`C:\Users\<YourUsername>`).</span></span> <span data-ttu-id="30984-110">ovvero un percorso di Windows.</span><span class="sxs-lookup"><span data-stu-id="30984-110">This is a Windows path.</span></span> <span data-ttu-id="30984-111">Per WSL, tuttavia, è consigliabile usare invece il percorso della home directory WSL.</span><span class="sxs-lookup"><span data-stu-id="30984-111">For WSL, however, you may want to use the WSL home path instead.</span></span> <span data-ttu-id="30984-112">`startingDirectory` accetta solo un percorso di tipo Windows, quindi l'impostazione per l'avvio in una distribuzione WSL richiede un prefisso.</span><span class="sxs-lookup"><span data-stu-id="30984-112">`startingDirectory` only accepts a Windows-style path, so setting it to start within a WSL distribution requires a prefix.</span></span>

<span data-ttu-id="30984-113">A partire da Windows 10 versione 1903, puoi gestire i file system delle distribuzioni WSL usando il prefisso `\\wsl$\`.</span><span class="sxs-lookup"><span data-stu-id="30984-113">Beginning in Windows 10 version 1903, the file systems of WSL distributions can be addressed using the `\\wsl$\` prefix.</span></span> <span data-ttu-id="30984-114">Per qualsiasi distribuzione WSL con il nome `DistroName`, usa `\\wsl$\DistroName` come percorso di Windows che punta alla radice del file system della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="30984-114">For any WSL distribution with the name `DistroName`, use `\\wsl$\DistroName` as a Windows path that points to the root of that distribution's file system.</span></span>

<span data-ttu-id="30984-115">Ad esempio, l'impostazione seguente avvierà la distribuzione "Ubuntu-18.04" nel percorso file della home directory:</span><span class="sxs-lookup"><span data-stu-id="30984-115">For example, the following setting will launch the "Ubuntu-18.04" distribution in its home file path:</span></span>

```json
{
    "name": "Ubuntu-18.04",
    "commandline" : "wsl -d Ubuntu-18.04",
    "startingDirectory" : "//wsl$/Ubuntu-18.04/home/<Your Ubuntu Username>"
}
```

## <a name="setting-the-tab-title"></a><span data-ttu-id="30984-116">Impostazione del titolo della scheda</span><span class="sxs-lookup"><span data-stu-id="30984-116">Setting the tab title</span></span>

<span data-ttu-id="30984-117">Per fare in modo che il titolo della scheda venga impostato automaticamente dalla shell, [vedi questa esercitazione](./tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="30984-117">To have the shell automatically set your tab title, [visit the set the tab title tutorial](./tutorials/tab-title.md).</span></span> <span data-ttu-id="30984-118">Se vuoi impostare un titolo personalizzato per la scheda, apri il file settings.json e segui questa procedura:</span><span class="sxs-lookup"><span data-stu-id="30984-118">If you want to set your own tab title, open the settings.json file and follow these steps:</span></span>

1. <span data-ttu-id="30984-119">Nel profilo di una riga di comando a scelta aggiungi `"suppressApplicationTitle": true` per eliminare gli eventi di modifica del titolo che vengono inviati dalla shell.</span><span class="sxs-lookup"><span data-stu-id="30984-119">In the profile for the command line of your choice, add `"suppressApplicationTitle": true` to suppress any title change events that get sent from the shell.</span></span> <span data-ttu-id="30984-120">Se aggiungi *solo* questa impostazione al profilo, il titolo della scheda verrà impostato sul nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="30984-120">Adding *only* this setting to your profile will set the tab title to the name of your profile.</span></span>

2. <span data-ttu-id="30984-121">Se vuoi impostare un titolo di scheda personalizzato e non il nome del profilo, aggiungi `"tabTitle": "TITLE"`.</span><span class="sxs-lookup"><span data-stu-id="30984-121">If you want a custom tab title that is not the name of your profile, add `"tabTitle": "TITLE"`.</span></span> <span data-ttu-id="30984-122">Sostituisci "TITLE" con il titolo preferito per la scheda.</span><span class="sxs-lookup"><span data-stu-id="30984-122">Replacing "TITLE" with your preferred tab title.</span></span>

## <a name="command-line-arguments-in-powershell"></a><span data-ttu-id="30984-123">Argomenti della riga di comando in PowerShell</span><span class="sxs-lookup"><span data-stu-id="30984-123">Command line arguments in PowerShell</span></span>

<span data-ttu-id="30984-124">Per informazioni sul funzionamento degli argomenti della riga di comando in PowerShell, vedere la [pagina Argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="30984-124">Visit the [Command line arguments page](./command-line-arguments.md) to learn how command-line arguments operate in PowerShell.</span></span>

## <a name="command-line-arguments-in-wsl"></a><span data-ttu-id="30984-125">Argomenti della riga di comando in WSL</span><span class="sxs-lookup"><span data-stu-id="30984-125">Command line arguments in WSL</span></span>

<span data-ttu-id="30984-126">Per informazioni sul funzionamento degli argomenti della riga di comando in WSL, vedere la [pagina Argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="30984-126">Visit the [Command line arguments page](./command-line-arguments.md) to learn how command-line arguments operate in WSL.</span></span>

## <a name="problem-setting-startingdirectory"></a><span data-ttu-id="30984-127">Problema con l'impostazione di `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="30984-127">Problem setting `startingDirectory`</span></span>

<span data-ttu-id="30984-128">Se l'impostazione di `startingDirectory` viene ignorata nel profilo, verifica prima di tutto che la sintassi del file settings.json sia corretta.</span><span class="sxs-lookup"><span data-stu-id="30984-128">If the `startingDirectory` is being ignored in your profile, first check to make sure your settings.json's syntax is correct.</span></span> <span data-ttu-id="30984-129">Per semplificare la verifica della sintassi, `"$schema": "https://aka.ms/terminal-profiles-schema"` viene inserito automaticamente.</span><span class="sxs-lookup"><span data-stu-id="30984-129">To help you check this syntax, `"$schema": "https://aka.ms/terminal-profiles-schema"` is automatically injected.</span></span> <span data-ttu-id="30984-130">Alcune applicazioni, ad esempio [Visual Studio Code](https://code.visualstudio.com/download), possono usare lo schema inserito per convalidare il file JSON durante le modifiche.</span><span class="sxs-lookup"><span data-stu-id="30984-130">Some applications, like [Visual Studio Code](https://code.visualstudio.com/download), can use that injected schema to validate your json file as you make edits.</span></span>

<span data-ttu-id="30984-131">Se le impostazioni sono corrette, è possibile che sia in esecuzione uno script di avvio che imposta separatamente la directory iniziale del terminale.</span><span class="sxs-lookup"><span data-stu-id="30984-131">If your settings are correct, you may be running a startup script that sets the starting directory of your terminal separately.</span></span> <span data-ttu-id="30984-132">PowerShell, ad esempio, prevede un proprio concetto separato dei profili.</span><span class="sxs-lookup"><span data-stu-id="30984-132">For example, PowerShell has its own separate concept of profiles.</span></span> <span data-ttu-id="30984-133">Se cambi qui la directory iniziale, questa impostazione avrà la precedenza su quella definita in Terminale Windows.</span><span class="sxs-lookup"><span data-stu-id="30984-133">If you are changing your starting directory there, it will take precedence over the setting defined in Windows Terminal.</span></span>

<span data-ttu-id="30984-134">In alternativa, se esegui uno script usando l'impostazione del profilo `commandline`, è possibile che stia impostando qui la posizione.</span><span class="sxs-lookup"><span data-stu-id="30984-134">Alternatively, if you are running a script using the `commandline` profile setting, it may be that you are setting the location there.</span></span> <span data-ttu-id="30984-135">Analogamente ai profili PowerShell, i comandi hanno la precedenza sull'impostazione del profilo `startingDirectory`.</span><span class="sxs-lookup"><span data-stu-id="30984-135">Similar to PowerShell profiles, your commands there take precedence over the `startingDirectory` profile setting.</span></span>

<span data-ttu-id="30984-136">Lo scopo di `startingDirectory` è avviare una nuova istanza di Terminale Windows nella directory specificata.</span><span class="sxs-lookup"><span data-stu-id="30984-136">The purpose of `startingDirectory` is to launch a new Windows Terminal instance in the given directory.</span></span> <span data-ttu-id="30984-137">Se il terminale esegue qualsiasi codice che cambia la directory, potrebbe essere questa la causa del problema.</span><span class="sxs-lookup"><span data-stu-id="30984-137">If the terminal runs any code that changes its directory, that may be a good place to take a look.</span></span>

## <a name="ctrl-does-not-increase-the-font-size"></a><span data-ttu-id="30984-138">CTRL+= non aumenta le dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="30984-138">Ctrl+= does not increase the font size</span></span>

<span data-ttu-id="30984-139">Se usi un layout di tastiera tedesco, potresti riscontrare questo problema.</span><span class="sxs-lookup"><span data-stu-id="30984-139">If you are using a German keyboard layout, you may run into this problem.</span></span> <span data-ttu-id="30984-140">La combinazione <kbd>CTRL+=</kbd> viene deserializzata come <kbd>CTRL+MAIUSC+0</kbd> se il layout di tastiera principale è impostato sul tedesco.</span><span class="sxs-lookup"><span data-stu-id="30984-140"><kbd>ctrl+=</kbd> gets deserialized as <kbd>ctrl+shift+0</kbd> if your main keyboard layout is set to German.</span></span> <span data-ttu-id="30984-141">Si tratta del mapping corretto per le tastiere tedesche.</span><span class="sxs-lookup"><span data-stu-id="30984-141">This is the correct mapping for German keyboards.</span></span>

<span data-ttu-id="30984-142">Ancora più importante, l'app non riceve mai la sequenza di tasti <kbd>CTRL+MAIUSC+0</kbd>.</span><span class="sxs-lookup"><span data-stu-id="30984-142">More importantly, the app never receives the <kbd>ctrl+shift+0</kbd> keystroke.</span></span> <span data-ttu-id="30984-143">Il motivo è che la combinazione <kbd>CTRL+MAIUSC+0</kbd> è riservata da Windows se sono attivi più layout di tastiera.</span><span class="sxs-lookup"><span data-stu-id="30984-143">This is because <kbd>ctrl+shift+0</kbd> is reserved by Windows if you have multiple keyboard layouts active.</span></span>

<span data-ttu-id="30984-144">Se vuoi disabilitare questa funzionalità per il corretto funzionamento di `Ctrl+=`, segui le istruzioni su come cambiare i tasti di scelta rapida per sostituire il layout della tastiera in Windows 10 in questo [post di blog](https://winaero.com/blog/change-hotkeys-switch-keyboard-layout-windows-10/).</span><span class="sxs-lookup"><span data-stu-id="30984-144">If you would like to disable this feature in order for `Ctrl+=` to work properly, follow the instructions for "Change Hotkeys to Switch Keyboard Layout in Windows 10" in this [blog post](https://winaero.com/blog/change-hotkeys-switch-keyboard-layout-windows-10/).</span></span>

<span data-ttu-id="30984-145">Imposta l'opzione 'Cambia layout di tastiera' su 'Non assegnato' (o su una combinazione senza <kbd>CTRL+MAIUSC</kbd>), quindi seleziona **OK** e poi **Applica**.</span><span class="sxs-lookup"><span data-stu-id="30984-145">Change the 'Switch Keyboard Layout' option to 'Not Assigned' (or off of <kbd>ctrl+shift</kbd>), then select **OK** and then **Apply**.</span></span> <span data-ttu-id="30984-146">La combinazione di tasti <kbd>CTRL+MAIUSC+0</kbd> dovrebbe ora funzionare e viene passata al terminale.</span><span class="sxs-lookup"><span data-stu-id="30984-146"><kbd>ctrl+shift+0</kbd> should now work as a key binding and is passed through to the terminal.</span></span>

<span data-ttu-id="30984-147">Se al contrario usi questa funzionalità di tasti di scelta rapida per più lingue di input, puoi [configurare combinazioni di tasti personalizzate](./customize-settings/actions.md) nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="30984-147">On the other hand, if you do use this hotkey feature for multiple input languages, you can [configure your own custom key binding](./customize-settings/actions.md) in your settings.json file.</span></span>

## <a name="the-text-is-blurry"></a><span data-ttu-id="30984-148">Il testo è sfocato</span><span class="sxs-lookup"><span data-stu-id="30984-148">The text is blurry</span></span>

<span data-ttu-id="30984-149">Alcuni driver video e combinazioni di hardware non gestiscono lo scorrimento e/o le aree modificate senza sfocare i dati del frame precedente.</span><span class="sxs-lookup"><span data-stu-id="30984-149">Some display drivers and hardware combinations do not handle scroll and/or dirty regions without blurring the data from the previous frame.</span></span> <span data-ttu-id="30984-150">Per ovviare a questo problema, è possibile aggiungere una combinazione di [queste impostazioni di rendering globali](./customize-settings/rendering.md) per ridurre la pressione esercitata sull'hardware dal renderer di testo del terminale.</span><span class="sxs-lookup"><span data-stu-id="30984-150">To mitigate this problem, you can add a combination of [these global rendering settings](./customize-settings/rendering.md) to reduce the strain placed on your hardware caused by the terminal text renderer.</span></span>

## <a name="my-colors-look-strange-there-are-black-bars-on-my-screen"></a><span data-ttu-id="30984-151">I miei colori hanno un aspetto strano.</span><span class="sxs-lookup"><span data-stu-id="30984-151">My colors look strange!</span></span> <span data-ttu-id="30984-152">Sono presenti barre nere sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="30984-152">There are black bars on my screen!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30984-153">Si applica solo alla versione 1.2 + del terminale di Windows.</span><span class="sxs-lookup"><span data-stu-id="30984-153">This applies only to version 1.2+ of Windows Terminal.</span></span> <span data-ttu-id="30984-154">Se si verificano problemi di colore nel terminale di Windows 1,0 o 1,1 o problemi che non vengono acquisiti qui, inviare un bug.</span><span class="sxs-lookup"><span data-stu-id="30984-154">If you are seeing color issues in Windows Terminal 1.0 or 1.1, or issues that are not captured here, please file a bug.</span></span>

<span data-ttu-id="30984-155">Windows Terminal 1,2 e versioni successive hanno migliorato la conoscenza di determinate impostazioni dei colori dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="30984-155">Windows Terminal 1.2 and beyond has an improved understanding of certain application color settings.</span></span> <span data-ttu-id="30984-156">Grazie a questa migliore comprensione, è stato possibile rimuovere una serie di blocchi di compatibilità che hanno comportato un'esperienza utente insufficiente.</span><span class="sxs-lookup"><span data-stu-id="30984-156">Because of this improved understanding, we have been able to remove a number of compatibility blocks that resulted in a poor user experience.</span></span> <span data-ttu-id="30984-157">Sfortunatamente, c'è un numero ridotto di applicazioni che possono riscontrare problemi.</span><span class="sxs-lookup"><span data-stu-id="30984-157">Unfortunately, there is a small number of applications that may experience issues.</span></span>

<span data-ttu-id="30984-158">Questo elemento di risoluzione dei problemi verrà mantenuto aggiornato con l'elenco dei problemi noti e delle relative soluzioni alternative.</span><span class="sxs-lookup"><span data-stu-id="30984-158">We will keep this troubleshooting item up-to-date with the list of known issues and their workarounds.</span></span>

### <a name="black-lines-in-powershell-51-6x-70"></a><span data-ttu-id="30984-159">Righe nere in PowerShell (5,1, 6. x, 7,0)</span><span class="sxs-lookup"><span data-stu-id="30984-159">Black lines in PowerShell (5.1, 6.x, 7.0)</span></span>

<span data-ttu-id="30984-160">Quando il terminale è associato alla libreria di modifica della riga di PowerShell [PSReadline](https://www.powershellgallery.com/packages/PSReadLine), può creare linee nere sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="30984-160">Terminal, when coupled with PowerShell's line editing library [PSReadline](https://www.powershellgallery.com/packages/PSReadLine), may draw black lines across the screen.</span></span> <span data-ttu-id="30984-161">Queste aree non colorate si estendono sullo schermo oltre la richiesta, ovunque ci siano parametri del comando, stringhe o operatori.</span><span class="sxs-lookup"><span data-stu-id="30984-161">These miscolored regions will extend across the screen beyond your prompt wherever there are command parameters, strings or operators.</span></span>

<span data-ttu-id="30984-162">PSReadline versione **2.0.3** è stata rilasciata e contiene una correzione per questo problema.</span><span class="sxs-lookup"><span data-stu-id="30984-162">PSReadline version **2.0.3** has been released and contains a fix for this issue.</span></span> <span data-ttu-id="30984-163">Se si usa la versione provvisoria di PSReadline, si noti che una correzione non è ancora disponibile.</span><span class="sxs-lookup"><span data-stu-id="30984-163">If you are using the prerelease version of PSReadline, note that a fix is not yet available.</span></span>

<span data-ttu-id="30984-164">Per eseguire l'aggiornamento alla versione più recente di PSReadline, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="30984-164">To update to the newest version of PSReadline, please run the following command:</span></span>

```powershell
Update-Module PSReadline
```

## <a name="why-are-my-emojis-not-appearing-as-icons-in-the-jumplist"></a><span data-ttu-id="30984-165">Perché i emoji non vengono visualizzati come icone in JumpList?</span><span class="sxs-lookup"><span data-stu-id="30984-165">Why are my emojis not appearing as icons in the jumplist?</span></span>

<span data-ttu-id="30984-166">Solo le immagini collegate da un percorso di file possono essere sottoposte a rendering come icone del profilo nell'oggetto JumpList.</span><span class="sxs-lookup"><span data-stu-id="30984-166">Only images linked from a file location can be rendered as profile icons in the jumplist.</span></span> <span data-ttu-id="30984-167">Emoji non sono supportati per le icone JumpList.</span><span class="sxs-lookup"><span data-stu-id="30984-167">Emojis are not supported for jumplist icons.</span></span>

## <a name="technical-notes"></a><span data-ttu-id="30984-168">Note tecniche</span><span class="sxs-lookup"><span data-stu-id="30984-168">Technical Notes</span></span>

<span data-ttu-id="30984-169">Le applicazioni che usano la [ `GetConsoleScreenBufferInfo` famiglia di API](https://docs.microsoft.com/windows/console/getconsolescreenbufferinfoex) per recuperare i colori della console attiva in formato Win32 e quindi provare a trasformarle in sequenze VT multipiattaforma (ad esempio, trasformando `BACKGROUND_RED` in `\x1b[41m` ) potrebbero interferire con la capacità del terminale di rilevare il colore di sfondo che l'applicazione sta tentando di usare.</span><span class="sxs-lookup"><span data-stu-id="30984-169">Applications that use the [`GetConsoleScreenBufferInfo` family of APIs](https://docs.microsoft.com/windows/console/getconsolescreenbufferinfoex) to retrieve the active console colors in Win32 format and then attempt to transform them into cross-platform VT sequences (for example, by transforming `BACKGROUND_RED` to `\x1b[41m`) may interfere with Terminal's ability to detect what background color the application is attempting to use.</span></span>

<span data-ttu-id="30984-170">Gli sviluppatori di applicazioni sono invitati a scegliere le funzioni dell'API Windows _o_ le sequenze VT per la regolazione dei colori senza provare a combinarli.</span><span class="sxs-lookup"><span data-stu-id="30984-170">Application developers are encouraged to choose either Windows API functions _or_ VT sequences for adjusting colors and not attempt to mix them.</span></span>

### <a name="keyboard-service-warning"></a><span data-ttu-id="30984-171">Avviso servizio tastiera</span><span class="sxs-lookup"><span data-stu-id="30984-171">Keyboard service warning</span></span>

<span data-ttu-id="30984-172">A partire da Windows Terminal 1,5, il terminale visualizzerà un avviso se la tastiera touch e il servizio pannello grafia sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="30984-172">Starting in Windows Terminal 1.5, the Terminal will display a warning if the "Touch Keyboard and Handwriting Panel Service" is disabled.</span></span> <span data-ttu-id="30984-173">Questo servizio è necessario per il sistema operativo per indirizzare correttamente gli eventi di input all'applicazione Terminal (così come molte altre applicazioni in Windows).</span><span class="sxs-lookup"><span data-stu-id="30984-173">This service is needed by the operating system to properly route input events to the Terminal application (as well as many other applications on Windows).</span></span> <span data-ttu-id="30984-174">Se viene visualizzato questo avviso, è possibile eseguire la procedura seguente per abilitare nuovamente il servizio:</span><span class="sxs-lookup"><span data-stu-id="30984-174">If you see this warning, you can follow these steps to re-enable the service:</span></span>
1. <span data-ttu-id="30984-175">Nella finestra di dialogo Esegui eseguire `services.msc`</span><span class="sxs-lookup"><span data-stu-id="30984-175">In the run dialog, run `services.msc`</span></span>

  ![Services. msc nella finestra di dialogo Esegui](https://user-images.githubusercontent.com/18356694/97891741-c81eed00-1cf4-11eb-9d48-7b94fede5294.png)

2. <span data-ttu-id="30984-177">Trovare il servizio "Touch Keyboard and grafia Panel Service"</span><span class="sxs-lookup"><span data-stu-id="30984-177">Find the "Touch Keyboard and Handwriting Panel Service"</span></span>

  ![Toccare tastiera e servizio pannello grafia in Services. msc](https://user-images.githubusercontent.com/18356694/97891813-e1279e00-1cf4-11eb-91c8-69a5c6da6c3d.png)

3. <span data-ttu-id="30984-179">Apre "Properties" per questo servizio</span><span class="sxs-lookup"><span data-stu-id="30984-179">Open the "Properties" for this service</span></span>

  ![Proprietà del servizio](https://user-images.githubusercontent.com/18356694/97891923-03212080-1cf5-11eb-90cc-821a4fbf16ba.png)

4. <span data-ttu-id="30984-181">Modificare il "tipo di avvio" in "automatico"</span><span class="sxs-lookup"><span data-stu-id="30984-181">Change the "startup type" to "Automatic"</span></span>

  ![tipo di avvio del servizio](https://user-images.githubusercontent.com/18356694/97892043-25b33980-1cf5-11eb-8833-a2e65a306a79.png)

5. <span data-ttu-id="30984-183">Fare clic su "OK" e riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="30984-183">Hit "Ok", and restart the PC.</span></span>

<span data-ttu-id="30984-184">Dopo il riavvio del computer, il servizio dovrebbe avviarsi automaticamente e la finestra di dialogo non dovrebbe più essere visualizzata.</span><span class="sxs-lookup"><span data-stu-id="30984-184">After restarting the machine, the service should auto-start, and the dialog should no longer appear.</span></span>
