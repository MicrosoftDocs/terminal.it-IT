---
title: Impostazioni di avvio del terminale di Windows
description: Informazioni su come personalizzare le impostazioni di avvio nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 1a16946a0b43a4fadd8e68014a13e6f13a79ae1e
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041968"
---
# <a name="startup-settings-in-windows-terminal"></a><span data-ttu-id="96b32-103">Impostazioni di avvio nel terminale Windows</span><span class="sxs-lookup"><span data-stu-id="96b32-103">Startup settings in Windows Terminal</span></span>

<span data-ttu-id="96b32-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="96b32-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="96b32-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="96b32-105">These should be placed at the root of your settings.json file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96b32-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="96b32-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="96b32-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="96b32-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="default-profile"></a><span data-ttu-id="96b32-108">Profilo predefinito</span><span class="sxs-lookup"><span data-stu-id="96b32-108">Default profile</span></span>

<span data-ttu-id="96b32-109">Imposta il profilo predefinito che viene aperto quando si digita <kbd>ctrl+shift+t</kbd>, si digita il tasto di scelta rapida assegnato a `newTab`, si esegue `wt new-tab` senza specificare un profilo o si fa clic sull'icona '+'.</span><span class="sxs-lookup"><span data-stu-id="96b32-109">Set the default profile that opens by typing <kbd>ctrl+shift+t</kbd>, typing the key binding assigned to `newTab`, running `wt new-tab` without specifying a profile, or clicking the '+' icon.</span></span>

<span data-ttu-id="96b32-110">**Nome della proprietà:** `defaultProfile`</span><span class="sxs-lookup"><span data-stu-id="96b32-110">**Property name:** `defaultProfile`</span></span>

<span data-ttu-id="96b32-111">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="96b32-111">**Necessity:** Required</span></span>

<span data-ttu-id="96b32-112">**Accetta:** GUID o nome del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="96b32-112">**Accepts:** GUID or profile name as a string</span></span>

<span data-ttu-id="96b32-113">**Valore predefinito:** GUID di PowerShell</span><span class="sxs-lookup"><span data-stu-id="96b32-113">**Default value:** PowerShell's GUID</span></span>

<br />

___

## <a name="launch-on-machine-startup"></a><span data-ttu-id="96b32-114">Avvia all'avvio del computer</span><span class="sxs-lookup"><span data-stu-id="96b32-114">Launch on machine startup</span></span>

<span data-ttu-id="96b32-115">Se questa proprietà è impostata su `true`, abilita l'avvio di Terminale Windows all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="96b32-115">When set to `true`, this enables the launch of Windows Terminal at startup.</span></span> <span data-ttu-id="96b32-116">L'impostazione su `false` disabiliterà la voce dell'attività di avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="96b32-116">Setting this to `false` will disable the startup task entry.</span></span>

<span data-ttu-id="96b32-117">Nota: se la voce dell'attività di avvio del sistema di Terminale Windows viene disabilitata da criteri dell'organizzazione o da un'azione dell'utente, questa impostazione non avrà effetto.</span><span class="sxs-lookup"><span data-stu-id="96b32-117">Note: if the Windows Terminal startup task entry is disabled either by org policy or by user action this setting will have no effect.</span></span>

<span data-ttu-id="96b32-118">**Nome della proprietà:** `startOnUserLogin`</span><span class="sxs-lookup"><span data-stu-id="96b32-118">**Property name:** `startOnUserLogin`</span></span>

<span data-ttu-id="96b32-119">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="96b32-119">**Necessity:** Optional</span></span>

<span data-ttu-id="96b32-120">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="96b32-120">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="96b32-121">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="96b32-121">**Default value:** `false`</span></span>

<br />

___

## <a name="launch-mode"></a><span data-ttu-id="96b32-122">Modalità di avvio</span><span class="sxs-lookup"><span data-stu-id="96b32-122">Launch mode</span></span>

<span data-ttu-id="96b32-123">Definisce se il terminale verrà avviato come ingrandito, a schermo intero o in una finestra.</span><span class="sxs-lookup"><span data-stu-id="96b32-123">This defines whether the terminal will launch as maximized, full screen, or in a window.</span></span> <span data-ttu-id="96b32-124">L'impostazione di questa opzione su `focus` equivale all'avvio del terminale in `default` modalità, ma con la [modalità messa a fuoco](./actions.md#toggle-focus-mode) abilitata.</span><span class="sxs-lookup"><span data-stu-id="96b32-124">Setting this to `focus` is equivalent to launching the terminal in the `default` mode, but with [focus mode](./actions.md#toggle-focus-mode) enabled.</span></span> <span data-ttu-id="96b32-125">Analogamente, l'impostazione di questa opzione su comporterà `maximizedFocus` l'avvio del terminale in una finestra ingrandita con la modalità messa a fuoco abilitata.</span><span class="sxs-lookup"><span data-stu-id="96b32-125">Similarly, setting this to `maximizedFocus` will result in launching the terminal in a maximized window with focus mode enabled.</span></span>

<span data-ttu-id="96b32-126">**Nome della proprietà:** `launchMode`</span><span class="sxs-lookup"><span data-stu-id="96b32-126">**Property name:** `launchMode`</span></span>

<span data-ttu-id="96b32-127">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="96b32-127">**Necessity:** Optional</span></span>

<span data-ttu-id="96b32-128">**Accetta:** `"default"`, `"maximized"`, `"fullscreen"`, `"focus"`, `"maximizedFocus"`</span><span class="sxs-lookup"><span data-stu-id="96b32-128">**Accepts:** `"default"`, `"maximized"`, `"fullscreen"`, `"focus"`, `"maximizedFocus"`</span></span>

<span data-ttu-id="96b32-129">**Valore predefinito:** `"default"`</span><span class="sxs-lookup"><span data-stu-id="96b32-129">**Default value:** `"default"`</span></span>

<br />

___

## <a name="launch-size"></a><span data-ttu-id="96b32-130">Dimensioni all'avvio</span><span class="sxs-lookup"><span data-stu-id="96b32-130">Launch size</span></span>

### <a name="columns-on-first-launch"></a><span data-ttu-id="96b32-131">Colonne al primo avvio</span><span class="sxs-lookup"><span data-stu-id="96b32-131">Columns on first launch</span></span>

<span data-ttu-id="96b32-132">Numero di colonne di tipo carattere visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="96b32-132">This is the number of character columns displayed in the window upon first load.</span></span> <span data-ttu-id="96b32-133">Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="96b32-133">If `launchMode` is set to `"maximized"` or `"maximizedFocus"`, this property is ignored.</span></span>

<span data-ttu-id="96b32-134">**Nome della proprietà:** `initialCols`</span><span class="sxs-lookup"><span data-stu-id="96b32-134">**Property name:** `initialCols`</span></span>

<span data-ttu-id="96b32-135">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="96b32-135">**Necessity:** Optional</span></span>

<span data-ttu-id="96b32-136">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="96b32-136">**Accepts:** Integer</span></span>

<span data-ttu-id="96b32-137">**Valore predefinito:** `120`</span><span class="sxs-lookup"><span data-stu-id="96b32-137">**Default value:** `120`</span></span>

### <a name="rows-on-first-launch"></a><span data-ttu-id="96b32-138">Righe al primo avvio</span><span class="sxs-lookup"><span data-stu-id="96b32-138">Rows on first launch</span></span>

<span data-ttu-id="96b32-139">Numero di righe visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="96b32-139">This is the number of rows displayed in the window upon first load.</span></span> <span data-ttu-id="96b32-140">Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="96b32-140">If `launchMode` is set to `"maximized"` or `"maximizedFocus"`, this property is ignored.</span></span>

<span data-ttu-id="96b32-141">**Nome della proprietà:** `initialRows`</span><span class="sxs-lookup"><span data-stu-id="96b32-141">**Property name:** `initialRows`</span></span>

<span data-ttu-id="96b32-142">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="96b32-142">**Necessity:** Optional</span></span>

<span data-ttu-id="96b32-143">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="96b32-143">**Accepts:** Integer</span></span>

<span data-ttu-id="96b32-144">**Valore predefinito:** `30`</span><span class="sxs-lookup"><span data-stu-id="96b32-144">**Default value:** `30`</span></span>

<br />

___

## <a name="launch-position"></a><span data-ttu-id="96b32-145">Posizione di avvio</span><span class="sxs-lookup"><span data-stu-id="96b32-145">Launch position</span></span>

<span data-ttu-id="96b32-146">Consente di impostare la posizione in pixel dell'angolo superiore sinistro della finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="96b32-146">This sets the pixel position of the top left corner of the window upon first load.</span></span> <span data-ttu-id="96b32-147">In un sistema con più schermi queste coordinate si riferiscono all'angolo superiore sinistro dello schermo principale.</span><span class="sxs-lookup"><span data-stu-id="96b32-147">On a system with multiple displays, these coordinates are relative to the top left of the primary display.</span></span> <span data-ttu-id="96b32-148">Se non viene specificata una coordinata X o Y, il terminale userà l'impostazione predefinita del sistema per tale valore.</span><span class="sxs-lookup"><span data-stu-id="96b32-148">If an X or Y coordinate is not provided, the terminal will use the system default for that value.</span></span> <span data-ttu-id="96b32-149">Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , la finestra verrà ingrandita sul monitoraggio specificato da tali coordinate.</span><span class="sxs-lookup"><span data-stu-id="96b32-149">If `launchMode` is set to `"maximized"` or `"maximizedFocus"`, the window will be maximized on the monitor specified by those coordinates.</span></span>

<span data-ttu-id="96b32-150">**Nome della proprietà:** `initialPosition`</span><span class="sxs-lookup"><span data-stu-id="96b32-150">**Property name:** `initialPosition`</span></span>

<span data-ttu-id="96b32-151">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="96b32-151">**Necessity:** Optional</span></span>

<span data-ttu-id="96b32-152">**Accetta:** coordinate nei formati stringa seguenti: `","`, `"#,#"`, `"#,"`, `",#"`</span><span class="sxs-lookup"><span data-stu-id="96b32-152">**Accepts:** Coordinates as a string in the following formats: `","`, `"#,#"`, `"#,"`, `",#"`</span></span>

<span data-ttu-id="96b32-153">**Valore predefinito:** `","`</span><span class="sxs-lookup"><span data-stu-id="96b32-153">**Default value:** `","`</span></span>

<br />

___

## <a name="disable-dynamic-profiles"></a><span data-ttu-id="96b32-154">Disabilita i profili dinamici</span><span class="sxs-lookup"><span data-stu-id="96b32-154">Disable dynamic profiles</span></span>

<span data-ttu-id="96b32-155">Consente di impostare i generatori di profili dinamici da disabilitare, per evitare che aggiungano profili all'elenco di profili all'avvio.</span><span class="sxs-lookup"><span data-stu-id="96b32-155">This sets which dynamic profile generators are disabled, preventing them from adding their profiles to the list of profiles on startup.</span></span> <span data-ttu-id="96b32-156">Per informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="96b32-156">For information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="96b32-157">**Nome della proprietà:** `disabledProfileSources`</span><span class="sxs-lookup"><span data-stu-id="96b32-157">**Property name:** `disabledProfileSources`</span></span>

<span data-ttu-id="96b32-158">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="96b32-158">**Necessity:** Optional</span></span>

<span data-ttu-id="96b32-159">**Accetta:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` e/o `"Windows.Terminal.PowershellCore"` all'interno di una matrice</span><span class="sxs-lookup"><span data-stu-id="96b32-159">**Accepts:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"`, and/or `"Windows.Terminal.PowershellCore"` inside an array</span></span>

<span data-ttu-id="96b32-160">**Valore predefinito:** `[]`</span><span class="sxs-lookup"><span data-stu-id="96b32-160">**Default value:** `[]`</span></span>

<br />

___

## <a name="startup-actions-preview"></a><span data-ttu-id="96b32-161">Azioni di avvio ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="96b32-161">Startup actions ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="96b32-162">In questo modo viene impostato l'elenco di azioni da eseguire all'avvio, consentendo al terminale di avviarsi con un set personalizzato di schede e riquadri per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="96b32-162">This sets the list of actions to execute on startup, allowing the terminal to launch with a custom set of tabs and panes by default.</span></span> <span data-ttu-id="96b32-163">Queste azioni verranno applicate solo se non è stato fornito alcun argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="96b32-163">These actions will be applied only if no command line arguments were supplied.</span></span> <span data-ttu-id="96b32-164">L'elenco di azioni è rappresentato da una stringa con lo stesso formato dei comandi negli argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="96b32-164">The list of actions is represented by a string with the same format as commands in the command line arguments.</span></span> <span data-ttu-id="96b32-165">Per ulteriori informazioni sul formato dei comandi, visitare la [pagina argomenti della riga di comando](./../command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="96b32-165">For more information about the commands format, visit the [Command line arguments page](./../command-line-arguments.md).</span></span>

<span data-ttu-id="96b32-166">**Nome della proprietà:** `startupActions`</span><span class="sxs-lookup"><span data-stu-id="96b32-166">**Property name:** `startupActions`</span></span>

<span data-ttu-id="96b32-167">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="96b32-167">**Necessity:** Optional</span></span>

<span data-ttu-id="96b32-168">**Accetta:** Stringa che rappresenta un elenco di comandi da eseguire</span><span class="sxs-lookup"><span data-stu-id="96b32-168">**Accepts:** String representing a list of commands to run</span></span>

<span data-ttu-id="96b32-169">**Valore predefinito:** `""`</span><span class="sxs-lookup"><span data-stu-id="96b32-169">**Default value:** `""`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96b32-170">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="96b32-170">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>
