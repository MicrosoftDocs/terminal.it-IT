---
title: Terminale Windows - Impostazioni globali
description: Informazioni su come personalizzare le impostazioni globali in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: ba3197bb8b9466d37c01432b60314a7a00227898
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994310"
---
# <a name="global-settings-in-windows-terminal"></a><span data-ttu-id="c42ab-103">Impostazioni globali di Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="c42ab-103">Global settings in Windows Terminal</span></span>

<span data-ttu-id="c42ab-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="c42ab-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="c42ab-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="c42ab-105">These should be placed at the root of your settings.json file.</span></span>

## <a name="default-profile"></a><span data-ttu-id="c42ab-106">Profilo predefinito</span><span class="sxs-lookup"><span data-stu-id="c42ab-106">Default profile</span></span>

<span data-ttu-id="c42ab-107">Imposta il profilo predefinito che viene aperto quando si digita <kbd>ctrl+shift+t</kbd>, si digita il tasto di scelta rapida assegnato a `newTab`, si esegue `wt new-tab` senza specificare un profilo o si fa clic sull'icona '+'.</span><span class="sxs-lookup"><span data-stu-id="c42ab-107">Set the default profile that opens by typing <kbd>ctrl+shift+t</kbd>, typing the key binding assigned to `newTab`, running `wt new-tab` without specifying a profile, or clicking the '+' icon.</span></span>

<span data-ttu-id="c42ab-108">**Nome della proprietà:** `defaultProfile`</span><span class="sxs-lookup"><span data-stu-id="c42ab-108">**Property name:** `defaultProfile`</span></span>

<span data-ttu-id="c42ab-109">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="c42ab-109">**Necessity:** Required</span></span>

<span data-ttu-id="c42ab-110">**Accetta:** GUID o nome del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="c42ab-110">**Accepts:** GUID or profile name as a string</span></span>

<span data-ttu-id="c42ab-111">**Valore predefinito:** GUID di PowerShell</span><span class="sxs-lookup"><span data-stu-id="c42ab-111">**Default value:** PowerShell's GUID</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c42ab-112">L'uso del nome del profilo per `defaultProfile` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="c42ab-112">Using the profile name for `defaultProfile` is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

<br />

___

## <a name="disable-dynamic-profiles"></a><span data-ttu-id="c42ab-113">Disabilita i profili dinamici</span><span class="sxs-lookup"><span data-stu-id="c42ab-113">Disable dynamic profiles</span></span>

<span data-ttu-id="c42ab-114">Consente di impostare i generatori di profili dinamici da disabilitare, per evitare che aggiungano profili all'elenco di profili all'avvio.</span><span class="sxs-lookup"><span data-stu-id="c42ab-114">This sets which dynamic profile generators are disabled, preventing them from adding their profiles to the list of profiles on startup.</span></span> <span data-ttu-id="c42ab-115">Per informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c42ab-115">For information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="c42ab-116">**Nome della proprietà:** `disabledProfileSources`</span><span class="sxs-lookup"><span data-stu-id="c42ab-116">**Property name:** `disabledProfileSources`</span></span>

<span data-ttu-id="c42ab-117">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-117">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-118">**Accetta:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` e/o `"Windows.Terminal.PowershellCore"` all'interno di una matrice</span><span class="sxs-lookup"><span data-stu-id="c42ab-118">**Accepts:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"`, and/or `"Windows.Terminal.PowershellCore"` inside an array</span></span>

<span data-ttu-id="c42ab-119">**Valore predefinito:** `[]`</span><span class="sxs-lookup"><span data-stu-id="c42ab-119">**Default value:** `[]`</span></span>

<br />

___

## <a name="darklight-theme"></a><span data-ttu-id="c42ab-120">Tema chiaro/scuro</span><span class="sxs-lookup"><span data-stu-id="c42ab-120">Dark/Light theme</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="c42ab-121">Consente di impostare il tema dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c42ab-121">This sets the theme of the application.</span></span> <span data-ttu-id="c42ab-122">Con `"system"` viene usato lo stesso tema di Windows.</span><span class="sxs-lookup"><span data-stu-id="c42ab-122">`"system"` will use the same theme as Windows.</span></span>

<span data-ttu-id="c42ab-123">**Nome della proprietà:** `theme`</span><span class="sxs-lookup"><span data-stu-id="c42ab-123">**Property name:** `theme`</span></span>

<span data-ttu-id="c42ab-124">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-124">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-125">**Accetta:** `"system"`, `"dark"`, `"light"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-125">**Accepts:** `"system"`, `"dark"`, `"light"`</span></span>

<span data-ttu-id="c42ab-126">**Valore predefinito:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-126">**Default value:** `"system"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="c42ab-127">![Terminale Windows - Tema scuro](./../images/requested-themes.gif)
_Configurazione: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="c42ab-127">![Windows Terminal dark theme](./../images/requested-themes.gif)
_Configuration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a><span data-ttu-id="c42ab-128">Impostazioni per le schede</span><span class="sxs-lookup"><span data-stu-id="c42ab-128">Tab settings</span></span>

### <a name="always-show-tabs"></a><span data-ttu-id="c42ab-129">Mostra sempre le schede</span><span class="sxs-lookup"><span data-stu-id="c42ab-129">Always show tabs</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="c42ab-130">Quando è impostata su `true`, le schede vengono sempre visualizzate.</span><span class="sxs-lookup"><span data-stu-id="c42ab-130">When this is set to `true`, tabs are always displayed.</span></span> <span data-ttu-id="c42ab-131">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `true`, le schede vengono sempre visualizzate sotto la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="c42ab-131">When it's set to `false` and `showTabsInTitlebar` is set to `true`, tabs are always displayed underneath the title bar.</span></span> <span data-ttu-id="c42ab-132">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `false`, le schede vengono visualizzate solo se sono presenti più schede digitando <kbd>ctrl+shift+t</kbd> oppure digitando il tasto di scelta rapida assegnato a `newTab`.</span><span class="sxs-lookup"><span data-stu-id="c42ab-132">When this is set to `false` and `showTabsInTitlebar` is set to `false`, tabs only appear after more than one tab exists by typing <kbd>ctrl+shift+t</kbd> or by typing the key binding assigned to `newTab`.</span></span> <span data-ttu-id="c42ab-133">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="c42ab-133">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="c42ab-134">**Nome della proprietà:** `alwaysShowTabs`</span><span class="sxs-lookup"><span data-stu-id="c42ab-134">**Property name:** `alwaysShowTabs`</span></span>

<span data-ttu-id="c42ab-135">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-135">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-136">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-136">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-137">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="c42ab-137">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Visualizza sempre le schede](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

### <a name="tab-width-mode"></a><span data-ttu-id="c42ab-139">Modalità larghezza schede</span><span class="sxs-lookup"><span data-stu-id="c42ab-139">Tab width mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="c42ab-140">Consente di impostare la larghezza delle schede.</span><span class="sxs-lookup"><span data-stu-id="c42ab-140">This sets the width of the tabs.</span></span> <span data-ttu-id="c42ab-141">Con `"equal"` tutte le schede hanno la stessa larghezza.</span><span class="sxs-lookup"><span data-stu-id="c42ab-141">`"equal"` makes each tab the same width.</span></span> <span data-ttu-id="c42ab-142">Con `"titleLength"` ogni scheda viene adattata alla lunghezza del titolo.</span><span class="sxs-lookup"><span data-stu-id="c42ab-142">`"titleLength"` sizes each tab to the length of its title.</span></span> <span data-ttu-id="c42ab-143">`"compact"` comprime tutte le schede inattive fino alla larghezza dell'icona, lasciando alla scheda attiva più spazio per visualizzare il titolo completo.</span><span class="sxs-lookup"><span data-stu-id="c42ab-143">`"compact"` will shrink every inactive tab to the width of the icon, leaving the active tab more space to display its full title.</span></span>

<span data-ttu-id="c42ab-144">**Nome della proprietà:** `tabWidthMode`</span><span class="sxs-lookup"><span data-stu-id="c42ab-144">**Property name:** `tabWidthMode`</span></span>

<span data-ttu-id="c42ab-145">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-145">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-146">**Accetta:** `"equal"`, `"titleLength"`, `"compact"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-146">**Accepts:** `"equal"`, `"titleLength"`, `"compact"`</span></span>

<span data-ttu-id="c42ab-147">**Valore predefinito:** `"equal"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-147">**Default value:** `"equal"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Modalità larghezza schede](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

> [!IMPORTANT]
> <span data-ttu-id="c42ab-149">L'impostazione `"compact"` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="c42ab-149">The `"compact"` setting is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="hide-close-all-tabs-popup"></a><span data-ttu-id="c42ab-150">Nascondi il popup di chiusura di tutte le schede</span><span class="sxs-lookup"><span data-stu-id="c42ab-150">Hide close all tabs popup</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="c42ab-151">Quando è impostata su `true`, alla chiusura di una finestra con più schede aperte _verrà_ richiesta una conferma.</span><span class="sxs-lookup"><span data-stu-id="c42ab-151">When this is set to `true`, closing a window with multiple tabs open _will_ require confirmation.</span></span> <span data-ttu-id="c42ab-152">Quando è impostata su `false`, alla chiusura di una finestra con più schede aperte _non verrà_ richiesta alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="c42ab-152">When it's set to `false`, closing a window with multiple tabs open _will not_ require confirmation.</span></span>

<span data-ttu-id="c42ab-153">**Nome della proprietà:** `confirmCloseAllTabs`</span><span class="sxs-lookup"><span data-stu-id="c42ab-153">**Property name:** `confirmCloseAllTabs`</span></span>

<span data-ttu-id="c42ab-154">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-154">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-155">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-155">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-156">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="c42ab-156">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

<br />

___

## <a name="launch-settings"></a><span data-ttu-id="c42ab-158">Impostazioni per l'avvio</span><span class="sxs-lookup"><span data-stu-id="c42ab-158">Launch settings</span></span>

### <a name="launch-on-startup-preview"></a><span data-ttu-id="c42ab-159">Avvio all'avvio del sistema ([anteprima](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="c42ab-159">Launch on startup ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="c42ab-160">Se questa proprietà è impostata su `true`, abilita l'avvio di Terminale Windows all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="c42ab-160">When set to `true`, this enables the launch of Windows Terminal at startup.</span></span> <span data-ttu-id="c42ab-161">L'impostazione su `false` disabiliterà la voce dell'attività di avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="c42ab-161">Setting this to `false` will disable the startup task entry.</span></span> <span data-ttu-id="c42ab-162">Nota: se la voce dell'attività di avvio del sistema di Terminale Windows viene disabilitata da criteri dell'organizzazione o da un'azione dell'utente, questa impostazione non avrà effetto.</span><span class="sxs-lookup"><span data-stu-id="c42ab-162">Note: if the Windows Terminal startup task entry is disabled either by org policy or by user action this setting will have no effect.</span></span>

<span data-ttu-id="c42ab-163">**Nome della proprietà:** `startOnUserLogin`</span><span class="sxs-lookup"><span data-stu-id="c42ab-163">**Property name:** `startOnUserLogin`</span></span>

<span data-ttu-id="c42ab-164">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-164">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-165">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-165">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-166">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-166">**Default value:** `false`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c42ab-167">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="c42ab-167">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="launch-size"></a><span data-ttu-id="c42ab-168">Dimensioni all'avvio</span><span class="sxs-lookup"><span data-stu-id="c42ab-168">Launch size</span></span>

<span data-ttu-id="c42ab-169">Definisce se il terminale verrà avviato con dimensioni ingrandite, a schermo intero o in una finestra.</span><span class="sxs-lookup"><span data-stu-id="c42ab-169">This defines whether the terminal will launch as maximized, fullscreen, or in a window.</span></span>

<span data-ttu-id="c42ab-170">**Nome della proprietà:** `launchMode`</span><span class="sxs-lookup"><span data-stu-id="c42ab-170">**Property name:** `launchMode`</span></span>

<span data-ttu-id="c42ab-171">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-171">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-172">**Accetta:** `"default"`, `"maximized"`, `"fullscreen"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-172">**Accepts:** `"default"`, `"maximized"`, `"fullscreen"`</span></span>

<span data-ttu-id="c42ab-173">**Valore predefinito:** `"default"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-173">**Default value:** `"default"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c42ab-174">L'impostazione `"fullscreen"` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="c42ab-174">The `"fullscreen"` setting is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="launch-position"></a><span data-ttu-id="c42ab-175">Posizione di avvio</span><span class="sxs-lookup"><span data-stu-id="c42ab-175">Launch position</span></span>

<span data-ttu-id="c42ab-176">Consente di impostare la posizione in pixel dell'angolo superiore sinistro della finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="c42ab-176">This sets the pixel position of the top left corner of the window upon first load.</span></span> <span data-ttu-id="c42ab-177">In un sistema con più schermi queste coordinate si riferiscono all'angolo superiore sinistro dello schermo principale.</span><span class="sxs-lookup"><span data-stu-id="c42ab-177">On a system with multiple displays, these coordinates are relative to the top left of the primary display.</span></span> <span data-ttu-id="c42ab-178">Se non viene specificata una coordinata X o Y, il terminale userà l'impostazione predefinita del sistema per tale valore.</span><span class="sxs-lookup"><span data-stu-id="c42ab-178">If an X or Y coordinate is not provided, the terminal will use the system default for that value.</span></span> <span data-ttu-id="c42ab-179">Se `launchMode` è impostata su `"maximized"`, la finestra aperta a schermo intero nel monitor specificato da tali coordinate.</span><span class="sxs-lookup"><span data-stu-id="c42ab-179">If `launchMode` is set to `"maximized"`, the window will be maximized on the monitor specified by those coordinates.</span></span>

<span data-ttu-id="c42ab-180">**Nome della proprietà:** `initialPosition`</span><span class="sxs-lookup"><span data-stu-id="c42ab-180">**Property name:** `initialPosition`</span></span>

<span data-ttu-id="c42ab-181">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-181">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-182">**Accetta:** coordinate nei formati stringa seguenti: `","`, `"#,#"`, `"#,"`, `",#"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-182">**Accepts:** Coordinates as a string in the following formats: `","`, `"#,#"`, `"#,"`, `",#"`</span></span>

<span data-ttu-id="c42ab-183">**Valore predefinito:** `","`</span><span class="sxs-lookup"><span data-stu-id="c42ab-183">**Default value:** `","`</span></span>

### <a name="columns-on-first-launch"></a><span data-ttu-id="c42ab-184">Colonne al primo avvio</span><span class="sxs-lookup"><span data-stu-id="c42ab-184">Columns on first launch</span></span>

<span data-ttu-id="c42ab-185">Numero di colonne di tipo carattere visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="c42ab-185">This is the number of character columns displayed in the window upon first load.</span></span> <span data-ttu-id="c42ab-186">Se `launchMode` è impostata su `"maximized"`, questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="c42ab-186">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="c42ab-187">**Nome della proprietà:** `initialCols`</span><span class="sxs-lookup"><span data-stu-id="c42ab-187">**Property name:** `initialCols`</span></span>

<span data-ttu-id="c42ab-188">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-188">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-189">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="c42ab-189">**Accepts:** Integer</span></span>

<span data-ttu-id="c42ab-190">**Valore predefinito:** `120`</span><span class="sxs-lookup"><span data-stu-id="c42ab-190">**Default value:** `120`</span></span>

### <a name="rows-on-first-launch"></a><span data-ttu-id="c42ab-191">Righe al primo avvio</span><span class="sxs-lookup"><span data-stu-id="c42ab-191">Rows on first launch</span></span>

<span data-ttu-id="c42ab-192">Numero di righe visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="c42ab-192">This is the number of rows displayed in the window upon first load.</span></span> <span data-ttu-id="c42ab-193">Se `launchMode` è impostata su `"maximized"`, questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="c42ab-193">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="c42ab-194">**Nome della proprietà:** `initialRows`</span><span class="sxs-lookup"><span data-stu-id="c42ab-194">**Property name:** `initialRows`</span></span>

<span data-ttu-id="c42ab-195">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-195">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-196">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="c42ab-196">**Accepts:** Integer</span></span>

<span data-ttu-id="c42ab-197">**Valore predefinito:** `30`</span><span class="sxs-lookup"><span data-stu-id="c42ab-197">**Default value:** `30`</span></span>

<br />

___

## <a name="title-bar-settings"></a><span data-ttu-id="c42ab-198">Impostazioni per la barra del titolo</span><span class="sxs-lookup"><span data-stu-id="c42ab-198">Title bar settings</span></span>

### <a name="showhide-the-title-bar"></a><span data-ttu-id="c42ab-199">Mostra/Nascondi la barra del titolo</span><span class="sxs-lookup"><span data-stu-id="c42ab-199">Show/Hide the title bar</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="c42ab-200">Quando è impostata su `true`, le schede vengono spostate nella barra del titolo e la barra del titolo scompare.</span><span class="sxs-lookup"><span data-stu-id="c42ab-200">When this is set to `true`, the tabs are moved into the title bar and the title bar disappears.</span></span> <span data-ttu-id="c42ab-201">Quando è impostata su `false`, la barra del titolo si trova sopra le schede.</span><span class="sxs-lookup"><span data-stu-id="c42ab-201">When it's set to `false`, the title bar sits above the tabs.</span></span> <span data-ttu-id="c42ab-202">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="c42ab-202">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="c42ab-203">**Nome della proprietà:** `showTabsInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="c42ab-203">**Property name:** `showTabsInTitlebar`</span></span>

<span data-ttu-id="c42ab-204">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-204">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-205">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-205">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-206">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="c42ab-206">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Mostra le schede nella barra del titolo](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

### <a name="set-the-text-in-the-title-bar"></a><span data-ttu-id="c42ab-208">Imposta il testo nella barra del titolo</span><span class="sxs-lookup"><span data-stu-id="c42ab-208">Set the text in the title bar</span></span>

<span data-ttu-id="c42ab-209">Quando è impostata su `true`, la barra del titolo visualizza il titolo della scheda selezionata. Quando è impostata su `false`, la barra del titolo visualizza "Terminale Windows".</span><span class="sxs-lookup"><span data-stu-id="c42ab-209">When this is set to `true`, the title bar displays the title of the selected tab. When it's set to `false`, title bar displays "Windows Terminal".</span></span> <span data-ttu-id="c42ab-210">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="c42ab-210">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="c42ab-211">**Nome della proprietà:** `showTerminalTitleInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="c42ab-211">**Property name:** `showTerminalTitleInTitlebar`</span></span>

<span data-ttu-id="c42ab-212">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-212">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-213">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-213">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-214">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="c42ab-214">**Default value:** `true`</span></span>

<br />

___

## <a name="selection-settings"></a><span data-ttu-id="c42ab-215">Impostazioni per le selezioni</span><span class="sxs-lookup"><span data-stu-id="c42ab-215">Selection settings</span></span>

### <a name="copy-after-selection-is-made"></a><span data-ttu-id="c42ab-216">Copia dopo che è stata effettuata la selezione</span><span class="sxs-lookup"><span data-stu-id="c42ab-216">Copy after selection is made</span></span>

<span data-ttu-id="c42ab-217">Quando è impostata su `true`, una selezione viene immediatamente copiata negli Appunti al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="c42ab-217">When this is set to `true`, a selection is immediately copied to your clipboard upon creation.</span></span> <span data-ttu-id="c42ab-218">In questo caso facendo clic con il pulsante destro del mouse, la selezione verrà sempre incollata.</span><span class="sxs-lookup"><span data-stu-id="c42ab-218">The right-click on your mouse will always paste in this case.</span></span> <span data-ttu-id="c42ab-219">Quando è impostata su `false`, la selezione viene mantenuta in attesa di altre azioni.</span><span class="sxs-lookup"><span data-stu-id="c42ab-219">When it's set to `false`, the selection persists and awaits further action.</span></span> <span data-ttu-id="c42ab-220">Facendo clic con il pulsante destro del mouse, la selezione verrà copiata.</span><span class="sxs-lookup"><span data-stu-id="c42ab-220">Using your mouse to right-click will copy the selection.</span></span>

<span data-ttu-id="c42ab-221">**Nome della proprietà:** `copyOnSelect`</span><span class="sxs-lookup"><span data-stu-id="c42ab-221">**Property name:** `copyOnSelect`</span></span>

<span data-ttu-id="c42ab-222">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-222">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-223">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-223">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-224">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-224">**Default value:** `false`</span></span>

### <a name="copy-formatting"></a><span data-ttu-id="c42ab-225">Copia formattazione</span><span class="sxs-lookup"><span data-stu-id="c42ab-225">Copy formatting</span></span>

<span data-ttu-id="c42ab-226">Quando è impostata su `true`, negli Appunti vengono copiate anche la formattazione del colore e del carattere del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="c42ab-226">When this is set to `true`, the color and font formatting of selected text is also copied to your clipboard.</span></span> <span data-ttu-id="c42ab-227">Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale.</span><span class="sxs-lookup"><span data-stu-id="c42ab-227">When it's set to `false`, only plain text is copied to your clipboard.</span></span>

<span data-ttu-id="c42ab-228">**Nome della proprietà:** `copyFormatting`</span><span class="sxs-lookup"><span data-stu-id="c42ab-228">**Property name:** `copyFormatting`</span></span>

<span data-ttu-id="c42ab-229">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-229">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-230">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-230">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-231">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-231">**Default value:** `false`</span></span>

### <a name="word-delimiters"></a><span data-ttu-id="c42ab-232">Delimitatori di parola</span><span class="sxs-lookup"><span data-stu-id="c42ab-232">Word delimiters</span></span>

<span data-ttu-id="c42ab-233">Determina i delimitatori di parola usati quando si fa doppio clic per selezionare.</span><span class="sxs-lookup"><span data-stu-id="c42ab-233">This determines the word delimiters used in a double-click selection.</span></span> <span data-ttu-id="c42ab-234">I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole.</span><span class="sxs-lookup"><span data-stu-id="c42ab-234">Word delimiters are characters that specify where the boundary is between two words.</span></span> <span data-ttu-id="c42ab-235">Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.</span><span class="sxs-lookup"><span data-stu-id="c42ab-235">The most common examples are spaces, semicolons, commas, and periods.</span></span>

<span data-ttu-id="c42ab-236">**Nome della proprietà:** `wordDelimiters`</span><span class="sxs-lookup"><span data-stu-id="c42ab-236">**Property name:** `wordDelimiters`</span></span>

<span data-ttu-id="c42ab-237">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-237">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-238">**Accetta:** caratteri in formato stringa</span><span class="sxs-lookup"><span data-stu-id="c42ab-238">**Accepts:** Characters as a string</span></span>

<span data-ttu-id="c42ab-239">**Valore predefinito:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span><span class="sxs-lookup"><span data-stu-id="c42ab-239">**Default value:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span></span><br><span data-ttu-id="c42ab-240">_(`│` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span><span class="sxs-lookup"><span data-stu-id="c42ab-240">_(`│` is `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span></span>

<br />

___

## <a name="scroll-speed"></a><span data-ttu-id="c42ab-241">Velocità di scorrimento</span><span class="sxs-lookup"><span data-stu-id="c42ab-241">Scroll speed</span></span>

<span data-ttu-id="c42ab-242">Numero di righe da scorrere per volta quando si usa la rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="c42ab-242">This is the number of rows to scroll at a time with the mouse wheel.</span></span> <span data-ttu-id="c42ab-243">Sostituisce l'impostazione di sistema se il valore è diverso da zero o `"system"`.</span><span class="sxs-lookup"><span data-stu-id="c42ab-243">This will override the system setting if the value is not zero or `"system"`.</span></span>

<span data-ttu-id="c42ab-244">**Nome della proprietà:** `rowsToScroll`</span><span class="sxs-lookup"><span data-stu-id="c42ab-244">**Property name:** `rowsToScroll`</span></span>

<span data-ttu-id="c42ab-245">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-245">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-246">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="c42ab-246">**Accepts:** Integer</span></span>

<span data-ttu-id="c42ab-247">**Valore predefinito:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="c42ab-247">**Default value:** `"system"`</span></span>

<br />

___

## <a name="window-resize-behavior"></a><span data-ttu-id="c42ab-248">Comportamento di ridimensionamento delle finestre</span><span class="sxs-lookup"><span data-stu-id="c42ab-248">Window resize behavior</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="c42ab-249">Quando è impostata su `true`, la finestra verrà allineata al limite del carattere più vicino quando viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="c42ab-249">When this is set to `true`, the window will snap to the nearest character boundary on resize.</span></span> <span data-ttu-id="c42ab-250">Quando è impostata su `false`, la finestra verrà ridimensionata senza vincoli.</span><span class="sxs-lookup"><span data-stu-id="c42ab-250">When it's set to `false`, the window will resize "smoothly".</span></span>

<span data-ttu-id="c42ab-251">**Nome della proprietà:** `snapToGridOnResize`</span><span class="sxs-lookup"><span data-stu-id="c42ab-251">**Property name:** `snapToGridOnResize`</span></span>

<span data-ttu-id="c42ab-252">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-252">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-253">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-253">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-254">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="c42ab-254">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Blocca sulla griglia al ridimensionamento](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="rendering-settings"></a><span data-ttu-id="c42ab-256">Impostazioni di rendering</span><span class="sxs-lookup"><span data-stu-id="c42ab-256">Rendering settings</span></span>

<span data-ttu-id="c42ab-257">Per cambiare le impostazioni di rendering, vedere le informazioni aggiuntive disponibili nella [pagina sulla risoluzione dei problemi](./../troubleshooting.md#the-text-is-blurry) per assistenza.</span><span class="sxs-lookup"><span data-stu-id="c42ab-257">If you are thinking about changing the rendering settings, additional information is provided on the [Troubleshooting page](./../troubleshooting.md#the-text-is-blurry) to help guide you.</span></span>

### <a name="screen-redrawing"></a><span data-ttu-id="c42ab-258">Ridisegno dello schermo</span><span class="sxs-lookup"><span data-stu-id="c42ab-258">Screen redrawing</span></span>

<span data-ttu-id="c42ab-259">Se questa proprietà è impostata su `true`, il terminale ridisegnerà ogni frame dello schermo.</span><span class="sxs-lookup"><span data-stu-id="c42ab-259">When this set to `true`, the terminal will redraw the entire screen each frame.</span></span> <span data-ttu-id="c42ab-260">Se è impostata su `false`, verrà eseguito solo il rendering degli aggiornamenti dello schermo tra frame.</span><span class="sxs-lookup"><span data-stu-id="c42ab-260">When set to `false`, it will render only the updates to the screen between frames.</span></span>

<span data-ttu-id="c42ab-261">**Nome della proprietà:** `experimental.rendering.forceFullRepaint`</span><span class="sxs-lookup"><span data-stu-id="c42ab-261">**Property name:** `experimental.rendering.forceFullRepaint`</span></span>

<span data-ttu-id="c42ab-262">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-262">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-263">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-263">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-264">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-264">**Default value:** `false`</span></span>

### <a name="software-rendering"></a><span data-ttu-id="c42ab-265">Rendering del software</span><span class="sxs-lookup"><span data-stu-id="c42ab-265">Software rendering</span></span>

<span data-ttu-id="c42ab-266">Se questa proprietà è impostata su `true`, il terminale userà il renderer software, ossia</span><span class="sxs-lookup"><span data-stu-id="c42ab-266">When this is set to `true`, the terminal will use the software renderer (a.k.a.</span></span> <span data-ttu-id="c42ab-267">WARP, invece di quello hardware.</span><span class="sxs-lookup"><span data-stu-id="c42ab-267">WARP) instead of the hardware one.</span></span>

<span data-ttu-id="c42ab-268">**Nome della proprietà:** `experimental.rendering.software`</span><span class="sxs-lookup"><span data-stu-id="c42ab-268">**Property name:** `experimental.rendering.software`</span></span>

<span data-ttu-id="c42ab-269">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c42ab-269">**Necessity:** Optional</span></span>

<span data-ttu-id="c42ab-270">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-270">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c42ab-271">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="c42ab-271">**Default value:** `false`</span></span>
