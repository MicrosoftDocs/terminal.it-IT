---
title: Terminale Windows - Impostazioni globali
description: Informazioni su come personalizzare le impostazioni globali in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 3cbe4b2b99f8115ff4eeaab5f525de393d7e5eb1
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415956"
---
# <a name="global-settings-in-the-windows-terminal"></a><span data-ttu-id="63aaf-103">Impostazioni globali di Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="63aaf-103">Global settings in the Windows Terminal</span></span>

<span data-ttu-id="63aaf-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="63aaf-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="63aaf-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="63aaf-105">These should be placed at the root of your settings.json file.</span></span>

## <a name="default-profile"></a><span data-ttu-id="63aaf-106">Profilo predefinito</span><span class="sxs-lookup"><span data-stu-id="63aaf-106">Default profile</span></span>

<span data-ttu-id="63aaf-107">Imposta il profilo predefinito che viene aperto quando si digita <kbd>ctrl+shift+t</kbd>, si digita il tasto di scelta rapida assegnato a `newTab`, si esegue `wt new-tab` senza specificare un profilo o si fa clic sull'icona '+'.</span><span class="sxs-lookup"><span data-stu-id="63aaf-107">Set the default profile that opens by typing <kbd>ctrl+shift+t</kbd>, typing the key binding assigned to `newTab`, running `wt new-tab` without specifying a profile, or clicking the '+' icon.</span></span>

<span data-ttu-id="63aaf-108">**Nome della proprietà:** `defaultProfile`</span><span class="sxs-lookup"><span data-stu-id="63aaf-108">**Property name:** `defaultProfile`</span></span>

<span data-ttu-id="63aaf-109">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="63aaf-109">**Necessity:** Required</span></span>

<span data-ttu-id="63aaf-110">**Accetta:** GUID in formato stringa</span><span class="sxs-lookup"><span data-stu-id="63aaf-110">**Accepts:** GUID as a string</span></span>

<span data-ttu-id="63aaf-111">**Valore predefinito:** GUID di PowerShell</span><span class="sxs-lookup"><span data-stu-id="63aaf-111">**Default value:** PowerShell's GUID</span></span>

<br />

___

## <a name="disable-dynamic-profiles"></a><span data-ttu-id="63aaf-112">Disabilita i profili dinamici</span><span class="sxs-lookup"><span data-stu-id="63aaf-112">Disable dynamic profiles</span></span>

<span data-ttu-id="63aaf-113">Consente di impostare i generatori di profili dinamici da disabilitare, per evitare che aggiungano profili all'elenco di profili all'avvio.</span><span class="sxs-lookup"><span data-stu-id="63aaf-113">This sets which dynamic profile generators are disabled, preventing them from adding their profiles to the list of profiles on startup.</span></span> <span data-ttu-id="63aaf-114">Per informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="63aaf-114">For information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="63aaf-115">**Nome della proprietà:** `disabledProfileSources`</span><span class="sxs-lookup"><span data-stu-id="63aaf-115">**Property name:** `disabledProfileSources`</span></span>

<span data-ttu-id="63aaf-116">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-116">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-117">**Accetta:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` e/o `"Windows.Terminal.PowershellCore"` all'interno di una matrice</span><span class="sxs-lookup"><span data-stu-id="63aaf-117">**Accepts:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"`, and/or `"Windows.Terminal.PowershellCore"` inside an array</span></span>

<span data-ttu-id="63aaf-118">**Valore predefinito:** `[]`</span><span class="sxs-lookup"><span data-stu-id="63aaf-118">**Default value:** `[]`</span></span>

<br />

___

## <a name="darklight-theme"></a><span data-ttu-id="63aaf-119">Tema chiaro/scuro</span><span class="sxs-lookup"><span data-stu-id="63aaf-119">Dark/Light theme</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="63aaf-120">Consente di impostare il tema dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="63aaf-120">This sets the theme of the application.</span></span> <span data-ttu-id="63aaf-121">Con `"system"` viene usato lo stesso tema di Windows.</span><span class="sxs-lookup"><span data-stu-id="63aaf-121">`"system"` will use the same theme as Windows.</span></span>

<span data-ttu-id="63aaf-122">**Nome della proprietà:** `theme`</span><span class="sxs-lookup"><span data-stu-id="63aaf-122">**Property name:** `theme`</span></span>

<span data-ttu-id="63aaf-123">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-123">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-124">**Accetta:** `"system"`, `"dark"`, `"light"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-124">**Accepts:** `"system"`, `"dark"`, `"light"`</span></span>

<span data-ttu-id="63aaf-125">**Valore predefinito:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-125">**Default value:** `"system"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="63aaf-126">![Terminale Windows - Tema scuro](./../images/requested-themes.gif)
_Configurazione: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="63aaf-126">![Windows Terminal dark theme](./../images/requested-themes.gif)
_Configuration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a><span data-ttu-id="63aaf-127">Impostazioni per le schede</span><span class="sxs-lookup"><span data-stu-id="63aaf-127">Tab settings</span></span>

### <a name="always-show-tabs"></a><span data-ttu-id="63aaf-128">Mostra sempre le schede</span><span class="sxs-lookup"><span data-stu-id="63aaf-128">Always show tabs</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="63aaf-129">Quando è impostata su `true`, le schede vengono sempre visualizzate.</span><span class="sxs-lookup"><span data-stu-id="63aaf-129">When this is set to `true`, tabs are always displayed.</span></span> <span data-ttu-id="63aaf-130">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `true`, le schede vengono sempre visualizzate sotto la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="63aaf-130">When it's set to `false` and `showTabsInTitlebar` is set to `true`, tabs are always displayed underneath the title bar.</span></span> <span data-ttu-id="63aaf-131">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `false`, le schede vengono visualizzate solo se sono presenti più schede digitando <kbd>ctrl+shift+t</kbd> oppure digitando il tasto di scelta rapida assegnato a `newTab`.</span><span class="sxs-lookup"><span data-stu-id="63aaf-131">When this is set to `false` and `showTabsInTitlebar` is set to `false`, tabs only appear after more than one tab exists by typing <kbd>ctrl+shift+t</kbd> or by typing the key binding assigned to `newTab`.</span></span> <span data-ttu-id="63aaf-132">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="63aaf-132">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="63aaf-133">**Nome della proprietà:** `alwaysShowTabs`</span><span class="sxs-lookup"><span data-stu-id="63aaf-133">**Property name:** `alwaysShowTabs`</span></span>

<span data-ttu-id="63aaf-134">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-134">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-135">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-135">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="63aaf-136">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="63aaf-136">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Visualizza sempre le schede](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

### <a name="tab-width-mode"></a><span data-ttu-id="63aaf-138">Modalità larghezza schede</span><span class="sxs-lookup"><span data-stu-id="63aaf-138">Tab width mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="63aaf-139">Consente di impostare la larghezza delle schede.</span><span class="sxs-lookup"><span data-stu-id="63aaf-139">This sets the width of the tabs.</span></span> <span data-ttu-id="63aaf-140">Con `"equal"` tutte le schede hanno la stessa larghezza.</span><span class="sxs-lookup"><span data-stu-id="63aaf-140">`"equal"` makes each tab the same width.</span></span> <span data-ttu-id="63aaf-141">Con `"titleLength"` ogni scheda viene adattata alla lunghezza del titolo.</span><span class="sxs-lookup"><span data-stu-id="63aaf-141">`"titleLength"` sizes each tab to the length of its title.</span></span>

<span data-ttu-id="63aaf-142">**Nome della proprietà:** `tabWidthMode`</span><span class="sxs-lookup"><span data-stu-id="63aaf-142">**Property name:** `tabWidthMode`</span></span>

<span data-ttu-id="63aaf-143">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-143">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-144">**Accetta:** `"equal"`, `"titleLength"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-144">**Accepts:** `"equal"`, `"titleLength"`</span></span>

<span data-ttu-id="63aaf-145">**Valore predefinito:** `"equal"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-145">**Default value:** `"equal"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Modalità larghezza schede](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

### <a name="hide-close-all-tabs-popup"></a><span data-ttu-id="63aaf-147">Nascondi il popup di chiusura di tutte le schede</span><span class="sxs-lookup"><span data-stu-id="63aaf-147">Hide close all tabs popup</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="63aaf-148">Quando è impostata su `true`, alla chiusura di una finestra con più schede aperte _verrà_ richiesta una conferma.</span><span class="sxs-lookup"><span data-stu-id="63aaf-148">When this is set to `true`, closing a window with multiple tabs open _will_ require confirmation.</span></span> <span data-ttu-id="63aaf-149">Quando è impostata su `false`, alla chiusura di una finestra con più schede aperte _non verrà_ richiesta alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="63aaf-149">When it's set to `false`, closing a window with multiple tabs open _will not_ require confirmation.</span></span>

<span data-ttu-id="63aaf-150">**Nome della proprietà:** `confirmCloseAllTabs`</span><span class="sxs-lookup"><span data-stu-id="63aaf-150">**Property name:** `confirmCloseAllTabs`</span></span>

<span data-ttu-id="63aaf-151">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-151">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-152">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-152">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="63aaf-153">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="63aaf-153">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

<br />

___

## <a name="launch-settings"></a><span data-ttu-id="63aaf-155">Impostazioni per l'avvio</span><span class="sxs-lookup"><span data-stu-id="63aaf-155">Launch settings</span></span>

### <a name="launch-maximized"></a><span data-ttu-id="63aaf-156">Avvio a schermo intero</span><span class="sxs-lookup"><span data-stu-id="63aaf-156">Launch maximized</span></span>

<span data-ttu-id="63aaf-157">Consente di definire se il terminale verrà avviato a schermo intero in modo da occupare tutto lo spazio nella schermata o in una finestra.</span><span class="sxs-lookup"><span data-stu-id="63aaf-157">This defines whether the terminal will launch as maximized to fill the entire screen or in a window.</span></span>

<span data-ttu-id="63aaf-158">**Nome della proprietà:** `launchMode`</span><span class="sxs-lookup"><span data-stu-id="63aaf-158">**Property name:** `launchMode`</span></span>

<span data-ttu-id="63aaf-159">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-159">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-160">**Accetta:** `"default"`, `"maximized"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-160">**Accepts:** `"default"`, `"maximized"`</span></span>

<span data-ttu-id="63aaf-161">**Valore predefinito:** `"default"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-161">**Default value:** `"default"`</span></span>

### <a name="launch-position"></a><span data-ttu-id="63aaf-162">Posizione di avvio</span><span class="sxs-lookup"><span data-stu-id="63aaf-162">Launch position</span></span>

<span data-ttu-id="63aaf-163">Consente di impostare la posizione in pixel dell'angolo superiore sinistro della finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="63aaf-163">This sets the pixel position of the top left corner of the window upon first load.</span></span> <span data-ttu-id="63aaf-164">In un sistema con più schermi queste coordinate si riferiscono all'angolo superiore sinistro dello schermo principale.</span><span class="sxs-lookup"><span data-stu-id="63aaf-164">On a system with multiple displays, these coordinates are relative to the top left of the primary display.</span></span> <span data-ttu-id="63aaf-165">Se non viene specificata una coordinata X o Y, il terminale userà l'impostazione predefinita del sistema per tale valore.</span><span class="sxs-lookup"><span data-stu-id="63aaf-165">If an X or Y coordinate is not provided, the terminal will use the system default for that value.</span></span> <span data-ttu-id="63aaf-166">Se `launchMode` è impostata su `"maximized"`, la finestra aperta a schermo intero nel monitor specificato da tali coordinate.</span><span class="sxs-lookup"><span data-stu-id="63aaf-166">If `launchMode` is set to `"maximized"`, the window will be maximized on the monitor specified by those coordinates.</span></span>

<span data-ttu-id="63aaf-167">**Nome della proprietà:** `initialPosition`</span><span class="sxs-lookup"><span data-stu-id="63aaf-167">**Property name:** `initialPosition`</span></span>

<span data-ttu-id="63aaf-168">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-168">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-169">**Accetta:** coordinate nei formati stringa seguenti: `","`, `"#,#"`, `"#,"`, `",#"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-169">**Accepts:** Coordinates as a string in the following formats: `","`, `"#,#"`, `"#,"`, `",#"`</span></span>

<span data-ttu-id="63aaf-170">**Valore predefinito:** `","`</span><span class="sxs-lookup"><span data-stu-id="63aaf-170">**Default value:** `","`</span></span>

### <a name="columns-on-first-launch"></a><span data-ttu-id="63aaf-171">Colonne al primo avvio</span><span class="sxs-lookup"><span data-stu-id="63aaf-171">Columns on first launch</span></span>

<span data-ttu-id="63aaf-172">Numero di colonne di tipo carattere visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="63aaf-172">This is the number of character columns displayed in the window upon first load.</span></span> <span data-ttu-id="63aaf-173">Se `launchMode` è impostata su `"maximized"`, questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="63aaf-173">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="63aaf-174">**Nome della proprietà:** `initialCols`</span><span class="sxs-lookup"><span data-stu-id="63aaf-174">**Property name:** `initialCols`</span></span>

<span data-ttu-id="63aaf-175">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-175">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-176">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="63aaf-176">**Accepts:** Integer</span></span>

<span data-ttu-id="63aaf-177">**Valore predefinito:** `120`</span><span class="sxs-lookup"><span data-stu-id="63aaf-177">**Default value:** `120`</span></span>

### <a name="rows-on-first-launch"></a><span data-ttu-id="63aaf-178">Righe al primo avvio</span><span class="sxs-lookup"><span data-stu-id="63aaf-178">Rows on first launch</span></span>

<span data-ttu-id="63aaf-179">Numero di righe visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="63aaf-179">This is the number of rows displayed in the window upon first load.</span></span> <span data-ttu-id="63aaf-180">Se `launchMode` è impostata su `"maximized"`, questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="63aaf-180">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="63aaf-181">**Nome della proprietà:** `initialRows`</span><span class="sxs-lookup"><span data-stu-id="63aaf-181">**Property name:** `initialRows`</span></span>

<span data-ttu-id="63aaf-182">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-182">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-183">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="63aaf-183">**Accepts:** Integer</span></span>

<span data-ttu-id="63aaf-184">**Valore predefinito:** `30`</span><span class="sxs-lookup"><span data-stu-id="63aaf-184">**Default value:** `30`</span></span>

<br />

___

## <a name="title-bar-settings"></a><span data-ttu-id="63aaf-185">Impostazioni per la barra del titolo</span><span class="sxs-lookup"><span data-stu-id="63aaf-185">Title bar settings</span></span>

### <a name="showhide-the-title-bar"></a><span data-ttu-id="63aaf-186">Mostra/Nascondi la barra del titolo</span><span class="sxs-lookup"><span data-stu-id="63aaf-186">Show/Hide the title bar</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="63aaf-187">Quando è impostata su `true`, le schede vengono spostate nella barra del titolo e la barra del titolo scompare.</span><span class="sxs-lookup"><span data-stu-id="63aaf-187">When this is set to `true`, the tabs are moved into the title bar and the title bar disappears.</span></span> <span data-ttu-id="63aaf-188">Quando è impostata su `false`, la barra del titolo si trova sopra le schede.</span><span class="sxs-lookup"><span data-stu-id="63aaf-188">When it's set to `false`, the title bar sits above the tabs.</span></span> <span data-ttu-id="63aaf-189">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="63aaf-189">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="63aaf-190">**Nome della proprietà:** `showTabsInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="63aaf-190">**Property name:** `showTabsInTitlebar`</span></span>

<span data-ttu-id="63aaf-191">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-191">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-192">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-192">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="63aaf-193">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="63aaf-193">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Mostra le schede nella barra del titolo](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

### <a name="set-the-text-in-the-title-bar"></a><span data-ttu-id="63aaf-195">Imposta il testo nella barra del titolo</span><span class="sxs-lookup"><span data-stu-id="63aaf-195">Set the text in the title bar</span></span>

<span data-ttu-id="63aaf-196">Quando è impostata su `true`, la barra del titolo visualizza il titolo della scheda selezionata. Quando è impostata su `false`, la barra del titolo visualizza "Terminale Windows".</span><span class="sxs-lookup"><span data-stu-id="63aaf-196">When this is set to `true`, the title bar displays the title of the selected tab. When it's set to `false`, title bar displays "Windows Terminal".</span></span> <span data-ttu-id="63aaf-197">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="63aaf-197">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="63aaf-198">**Nome della proprietà:** `showTerminalTitleInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="63aaf-198">**Property name:** `showTerminalTitleInTitlebar`</span></span>

<span data-ttu-id="63aaf-199">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-199">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-200">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-200">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="63aaf-201">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="63aaf-201">**Default value:** `true`</span></span>

<br />

___

## <a name="selection-settings"></a><span data-ttu-id="63aaf-202">Impostazioni per le selezioni</span><span class="sxs-lookup"><span data-stu-id="63aaf-202">Selection settings</span></span>

### <a name="copy-after-selection-is-made"></a><span data-ttu-id="63aaf-203">Copia dopo che è stata effettuata la selezione</span><span class="sxs-lookup"><span data-stu-id="63aaf-203">Copy after selection is made</span></span>

<span data-ttu-id="63aaf-204">Quando è impostata su `true`, una selezione viene immediatamente copiata negli Appunti al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="63aaf-204">When this is set to `true`, a selection is immediately copied to your clipboard upon creation.</span></span> <span data-ttu-id="63aaf-205">In questo caso facendo clic con il pulsante destro del mouse, la selezione verrà sempre incollata.</span><span class="sxs-lookup"><span data-stu-id="63aaf-205">The right-click on your mouse will always paste in this case.</span></span> <span data-ttu-id="63aaf-206">Quando è impostata su `false`, la selezione viene mantenuta in attesa di altre azioni.</span><span class="sxs-lookup"><span data-stu-id="63aaf-206">When it's set to `false`, the selection persists and awaits further action.</span></span> <span data-ttu-id="63aaf-207">Facendo clic con il pulsante destro del mouse, la selezione verrà copiata.</span><span class="sxs-lookup"><span data-stu-id="63aaf-207">Using your mouse to right-click will copy the selection.</span></span>

<span data-ttu-id="63aaf-208">**Nome della proprietà:** `copyOnSelect`</span><span class="sxs-lookup"><span data-stu-id="63aaf-208">**Property name:** `copyOnSelect`</span></span>

<span data-ttu-id="63aaf-209">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-209">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-210">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-210">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="63aaf-211">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-211">**Default value:** `false`</span></span>

### <a name="copy-formatting"></a><span data-ttu-id="63aaf-212">Copia formattazione</span><span class="sxs-lookup"><span data-stu-id="63aaf-212">Copy formatting</span></span>

<span data-ttu-id="63aaf-213">Quando è impostata su `true`, negli Appunti vengono copiate anche la formattazione del colore e del carattere del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="63aaf-213">When this is set to `true`, the color and font formatting of selected text is also copied to your clipboard.</span></span> <span data-ttu-id="63aaf-214">Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale.</span><span class="sxs-lookup"><span data-stu-id="63aaf-214">When it's set to `false`, only plain text is copied to your clipboard.</span></span>

<span data-ttu-id="63aaf-215">**Nome della proprietà:** `copyFormatting`</span><span class="sxs-lookup"><span data-stu-id="63aaf-215">**Property name:** `copyFormatting`</span></span>

<span data-ttu-id="63aaf-216">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-216">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-217">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-217">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="63aaf-218">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-218">**Default value:** `false`</span></span>

### <a name="word-delimiters"></a><span data-ttu-id="63aaf-219">Delimitatori di parola</span><span class="sxs-lookup"><span data-stu-id="63aaf-219">Word delimiters</span></span>

<span data-ttu-id="63aaf-220">Determina i delimitatori di parola usati quando si fa doppio clic per selezionare.</span><span class="sxs-lookup"><span data-stu-id="63aaf-220">This determines the word delimiters used in a double-click selection.</span></span> <span data-ttu-id="63aaf-221">I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole.</span><span class="sxs-lookup"><span data-stu-id="63aaf-221">Word delimiters are characters that specify where the boundary is between two words.</span></span> <span data-ttu-id="63aaf-222">Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.</span><span class="sxs-lookup"><span data-stu-id="63aaf-222">The most common examples are spaces, semicolons, commas, and periods.</span></span>

<span data-ttu-id="63aaf-223">**Nome della proprietà:** `wordDelimiters`</span><span class="sxs-lookup"><span data-stu-id="63aaf-223">**Property name:** `wordDelimiters`</span></span>

<span data-ttu-id="63aaf-224">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-224">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-225">**Accetta:** caratteri in formato stringa</span><span class="sxs-lookup"><span data-stu-id="63aaf-225">**Accepts:** Characters as a string</span></span>

<span data-ttu-id="63aaf-226">**Valore predefinito:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span><span class="sxs-lookup"><span data-stu-id="63aaf-226">**Default value:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span></span><br><span data-ttu-id="63aaf-227">_(`│` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span><span class="sxs-lookup"><span data-stu-id="63aaf-227">_(`│` is `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span></span>

<br />

___

## <a name="scroll-speed"></a><span data-ttu-id="63aaf-228">Velocità di scorrimento</span><span class="sxs-lookup"><span data-stu-id="63aaf-228">Scroll speed</span></span>

<span data-ttu-id="63aaf-229">Numero di righe da scorrere per volta quando si usa la rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="63aaf-229">This is the number of rows to scroll at a time with the mouse wheel.</span></span> <span data-ttu-id="63aaf-230">Sostituisce l'impostazione di sistema se il valore è diverso da zero o `"system"`.</span><span class="sxs-lookup"><span data-stu-id="63aaf-230">This will override the system setting if the value is not zero or `"system"`.</span></span>

<span data-ttu-id="63aaf-231">**Nome della proprietà:** `rowsToScroll`</span><span class="sxs-lookup"><span data-stu-id="63aaf-231">**Property name:** `rowsToScroll`</span></span>

<span data-ttu-id="63aaf-232">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-232">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-233">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="63aaf-233">**Accepts:** Integer</span></span>

<span data-ttu-id="63aaf-234">**Valore predefinito:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="63aaf-234">**Default value:** `"system"`</span></span>

<br />

___

## <a name="window-resize-behavior"></a><span data-ttu-id="63aaf-235">Comportamento di ridimensionamento delle finestre</span><span class="sxs-lookup"><span data-stu-id="63aaf-235">Window resize behavior</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="63aaf-236">Quando è impostata su `true`, la finestra verrà allineata al limite del carattere più vicino quando viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="63aaf-236">When this is set to `true`, the window will snap to the nearest character boundary on resize.</span></span> <span data-ttu-id="63aaf-237">Quando è impostata su `false`, la finestra verrà ridimensionata senza vincoli.</span><span class="sxs-lookup"><span data-stu-id="63aaf-237">When it's set to `false`, the window will resize "smoothly".</span></span>

<span data-ttu-id="63aaf-238">**Nome della proprietà:** `snapToGridOnResize`</span><span class="sxs-lookup"><span data-stu-id="63aaf-238">**Property name:** `snapToGridOnResize`</span></span>

<span data-ttu-id="63aaf-239">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="63aaf-239">**Necessity:** Optional</span></span>

<span data-ttu-id="63aaf-240">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="63aaf-240">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="63aaf-241">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="63aaf-241">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Blocca sulla griglia al ridimensionamento](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::
