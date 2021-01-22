---
title: Terminale Windows - Impostazioni globali
description: Informazioni su come personalizzare le impostazioni globali in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 11/11/2020
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 2724cc52c5a612184a7a5fc3a09be4d3d2d6d232
ms.sourcegitcommit: 9a2f9d152f65cdc8106fb9aad7fa69b01f3d05db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "94520266"
---
# <a name="global-settings-in-windows-terminal"></a><span data-ttu-id="28930-103">Impostazioni globali di Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="28930-103">Global settings in Windows Terminal</span></span>

<span data-ttu-id="28930-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="28930-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="28930-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="28930-105">These should be placed at the root of your settings.json file.</span></span>

## <a name="default-profile"></a><span data-ttu-id="28930-106">Profilo predefinito</span><span class="sxs-lookup"><span data-stu-id="28930-106">Default profile</span></span>

<span data-ttu-id="28930-107">Imposta il profilo predefinito che viene aperto quando si digita <kbd>ctrl+shift+t</kbd>, si digita il tasto di scelta rapida assegnato a `newTab`, si esegue `wt new-tab` senza specificare un profilo o si fa clic sull'icona '+'.</span><span class="sxs-lookup"><span data-stu-id="28930-107">Set the default profile that opens by typing <kbd>ctrl+shift+t</kbd>, typing the key binding assigned to `newTab`, running `wt new-tab` without specifying a profile, or clicking the '+' icon.</span></span>

<span data-ttu-id="28930-108">**Nome della proprietà:** `defaultProfile`</span><span class="sxs-lookup"><span data-stu-id="28930-108">**Property name:** `defaultProfile`</span></span>

<span data-ttu-id="28930-109">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="28930-109">**Necessity:** Required</span></span>

<span data-ttu-id="28930-110">**Accetta:** GUID o nome del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="28930-110">**Accepts:** GUID or profile name as a string</span></span>

<span data-ttu-id="28930-111">**Valore predefinito:** GUID di PowerShell</span><span class="sxs-lookup"><span data-stu-id="28930-111">**Default value:** PowerShell's GUID</span></span>

<br />

___

## <a name="disable-dynamic-profiles"></a><span data-ttu-id="28930-112">Disabilita i profili dinamici</span><span class="sxs-lookup"><span data-stu-id="28930-112">Disable dynamic profiles</span></span>

<span data-ttu-id="28930-113">Consente di impostare i generatori di profili dinamici da disabilitare, per evitare che aggiungano profili all'elenco di profili all'avvio.</span><span class="sxs-lookup"><span data-stu-id="28930-113">This sets which dynamic profile generators are disabled, preventing them from adding their profiles to the list of profiles on startup.</span></span> <span data-ttu-id="28930-114">Per informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="28930-114">For information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="28930-115">**Nome della proprietà:** `disabledProfileSources`</span><span class="sxs-lookup"><span data-stu-id="28930-115">**Property name:** `disabledProfileSources`</span></span>

<span data-ttu-id="28930-116">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-116">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-117">**Accetta:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` e/o `"Windows.Terminal.PowershellCore"` all'interno di una matrice</span><span class="sxs-lookup"><span data-stu-id="28930-117">**Accepts:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"`, and/or `"Windows.Terminal.PowershellCore"` inside an array</span></span>

<span data-ttu-id="28930-118">**Valore predefinito:** `[]`</span><span class="sxs-lookup"><span data-stu-id="28930-118">**Default value:** `[]`</span></span>

<br />

___

## <a name="darklight-theme"></a><span data-ttu-id="28930-119">Tema chiaro/scuro</span><span class="sxs-lookup"><span data-stu-id="28930-119">Dark/Light theme</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="28930-120">Consente di impostare il tema dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="28930-120">This sets the theme of the application.</span></span> <span data-ttu-id="28930-121">Con `"system"` viene usato lo stesso tema di Windows.</span><span class="sxs-lookup"><span data-stu-id="28930-121">`"system"` will use the same theme as Windows.</span></span>

<span data-ttu-id="28930-122">**Nome della proprietà:** `theme`</span><span class="sxs-lookup"><span data-stu-id="28930-122">**Property name:** `theme`</span></span>

<span data-ttu-id="28930-123">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-123">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-124">**Accetta:** `"system"`, `"dark"`, `"light"`</span><span class="sxs-lookup"><span data-stu-id="28930-124">**Accepts:** `"system"`, `"dark"`, `"light"`</span></span>

<span data-ttu-id="28930-125">**Valore predefinito:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="28930-125">**Default value:** `"system"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="28930-126">![Terminale Windows - Tema scuro](./../images/requested-themes.gif)
_Configurazione: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="28930-126">![Windows Terminal dark theme](./../images/requested-themes.gif)
_Configuration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a><span data-ttu-id="28930-127">Impostazioni per le schede</span><span class="sxs-lookup"><span data-stu-id="28930-127">Tab settings</span></span>

### <a name="use-tab-switcher-experience-preview"></a><span data-ttu-id="28930-128">Usare l'esperienza di selezione scheda ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="28930-128">Use tab switcher experience ([Preview](https://aka.ms/terminal-preview))</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="28930-129">Quando è impostato su `true` o `"mru"` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda, con l'ordine di utilizzo più recente.</span><span class="sxs-lookup"><span data-stu-id="28930-129">When this is set to `true` or `"mru"`, the `nextTab` and `prevTab` commands will use the tab switcher UI, with most recently used ordering.</span></span> <span data-ttu-id="28930-130">Quando è impostato su `"inOrder"` , queste azioni cambieranno le schede nell'ordine corrente sulla barra della scheda.</span><span class="sxs-lookup"><span data-stu-id="28930-130">When set to `"inOrder"`, these actions will switch tabs in their current order in the tab bar.</span></span> <span data-ttu-id="28930-131">L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.</span><span class="sxs-lookup"><span data-stu-id="28930-131">The UI will show all the currently open tabs in a vertical list, navigable with the keyboard or mouse.</span></span>

<span data-ttu-id="28930-132">Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto.</span><span class="sxs-lookup"><span data-stu-id="28930-132">The tab switcher will open on the initial press of the actions for `nextTab` and `prevTab`, and will stay open as long as a modifier key is held down.</span></span> <span data-ttu-id="28930-133">Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="28930-133">When all modifier keys are released, the switcher will close and the highlighted tab will be focused.</span></span> <span data-ttu-id="28930-134"><kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.</span><span class="sxs-lookup"><span data-stu-id="28930-134"><kbd>tab</kbd>/<kbd>shift+tab</kbd>, the <kbd>up</kbd> and <kbd>down</kbd> arrow keys, and the `nextTab`/`prevTab` actions can be used to cycle through the switcher UI.</span></span>

<span data-ttu-id="28930-135">Per disabilitare lo switcher di tabulazione, è possibile impostare questa impostazione su `false` o su `"disabled"` .</span><span class="sxs-lookup"><span data-stu-id="28930-135">To disable the tab switcher, you can set this to `false` or `"disabled"`.</span></span>

<span data-ttu-id="28930-136">**Nome della proprietà:** `tabSwitcherMode`</span><span class="sxs-lookup"><span data-stu-id="28930-136">**Property name:** `tabSwitcherMode`</span></span>

<span data-ttu-id="28930-137">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-137">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-138">**Accetta:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`</span><span class="sxs-lookup"><span data-stu-id="28930-138">**Accepts:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`</span></span>

<span data-ttu-id="28930-139">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-139">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Switcher Scheda terminale Windows](./../images/tab-switcher.gif)

:::column-end:::
:::row-end:::

> [!IMPORTANT]
> <span data-ttu-id="28930-141">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="28930-141">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="enable-tab-switcher"></a><span data-ttu-id="28930-142">Abilita Switcher schede</span><span class="sxs-lookup"><span data-stu-id="28930-142">Enable tab switcher</span></span>

<span data-ttu-id="28930-143">Quando questa impostazione è impostata su `true` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda.</span><span class="sxs-lookup"><span data-stu-id="28930-143">When this is set to `true`, the `nextTab` and `prevTab` commands will use the tab switcher UI.</span></span> <span data-ttu-id="28930-144">L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.</span><span class="sxs-lookup"><span data-stu-id="28930-144">The UI will show all the currently open tabs in a vertical list, navigable with the keyboard or mouse.</span></span>

<span data-ttu-id="28930-145">Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto.</span><span class="sxs-lookup"><span data-stu-id="28930-145">The tab switcher will open on the initial press of the actions for `nextTab` and `prevTab`, and will stay open as long as a modifier key is held down.</span></span> <span data-ttu-id="28930-146">Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="28930-146">When all modifier keys are released, the switcher will close and the highlighted tab will be focused.</span></span> <span data-ttu-id="28930-147"><kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.</span><span class="sxs-lookup"><span data-stu-id="28930-147"><kbd>tab</kbd>/<kbd>shift+tab</kbd>, the <kbd>up</kbd> and <kbd>down</kbd> arrow keys, and the `nextTab`/`prevTab` actions can be used to cycle through the switcher UI.</span></span>

<span data-ttu-id="28930-148">**Nome della proprietà:** `useTabSwitcher`</span><span class="sxs-lookup"><span data-stu-id="28930-148">**Property name:** `useTabSwitcher`</span></span>

<span data-ttu-id="28930-149">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-149">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-150">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-150">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-151">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-151">**Default value:** `true`</span></span>

> [!CAUTION]
> <span data-ttu-id="28930-152">L' `"useTabSwitcher"` impostazione non è più disponibile nelle versioni 1,5 e successive.</span><span class="sxs-lookup"><span data-stu-id="28930-152">The `"useTabSwitcher"` setting is no longer available in versions 1.5 and later.</span></span> <span data-ttu-id="28930-153">Si consiglia di utilizzare `"tabSwitcherMode"` invece l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="28930-153">It is recommended that you use the `"tabSwitcherMode"` setting instead.</span></span>

### <a name="always-show-tabs"></a><span data-ttu-id="28930-154">Mostra sempre le schede</span><span class="sxs-lookup"><span data-stu-id="28930-154">Always show tabs</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="28930-155">Quando è impostata su `true`, le schede vengono sempre visualizzate.</span><span class="sxs-lookup"><span data-stu-id="28930-155">When this is set to `true`, tabs are always displayed.</span></span> <span data-ttu-id="28930-156">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `true`, le schede vengono sempre visualizzate sotto la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="28930-156">When it's set to `false` and `showTabsInTitlebar` is set to `true`, tabs are always displayed underneath the title bar.</span></span> <span data-ttu-id="28930-157">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `false`, le schede vengono visualizzate solo se sono presenti più schede digitando <kbd>ctrl+shift+t</kbd> oppure digitando il tasto di scelta rapida assegnato a `newTab`.</span><span class="sxs-lookup"><span data-stu-id="28930-157">When this is set to `false` and `showTabsInTitlebar` is set to `false`, tabs only appear after more than one tab exists by typing <kbd>ctrl+shift+t</kbd> or by typing the key binding assigned to `newTab`.</span></span> <span data-ttu-id="28930-158">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="28930-158">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="28930-159">**Nome della proprietà:** `alwaysShowTabs`</span><span class="sxs-lookup"><span data-stu-id="28930-159">**Property name:** `alwaysShowTabs`</span></span>

<span data-ttu-id="28930-160">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-160">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-161">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-161">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-162">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-162">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Visualizza sempre le schede](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

### <a name="tab-width-mode"></a><span data-ttu-id="28930-164">Modalità larghezza schede</span><span class="sxs-lookup"><span data-stu-id="28930-164">Tab width mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="28930-165">Consente di impostare la larghezza delle schede.</span><span class="sxs-lookup"><span data-stu-id="28930-165">This sets the width of the tabs.</span></span> <span data-ttu-id="28930-166">Con `"equal"` tutte le schede hanno la stessa larghezza.</span><span class="sxs-lookup"><span data-stu-id="28930-166">`"equal"` makes each tab the same width.</span></span> <span data-ttu-id="28930-167">Con `"titleLength"` ogni scheda viene adattata alla lunghezza del titolo.</span><span class="sxs-lookup"><span data-stu-id="28930-167">`"titleLength"` sizes each tab to the length of its title.</span></span> <span data-ttu-id="28930-168">`"compact"` comprime tutte le schede inattive fino alla larghezza dell'icona, lasciando alla scheda attiva più spazio per visualizzare il titolo completo.</span><span class="sxs-lookup"><span data-stu-id="28930-168">`"compact"` will shrink every inactive tab to the width of the icon, leaving the active tab more space to display its full title.</span></span>

<span data-ttu-id="28930-169">**Nome della proprietà:** `tabWidthMode`</span><span class="sxs-lookup"><span data-stu-id="28930-169">**Property name:** `tabWidthMode`</span></span>

<span data-ttu-id="28930-170">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-170">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-171">**Accetta:** `"equal"`, `"titleLength"`, `"compact"`</span><span class="sxs-lookup"><span data-stu-id="28930-171">**Accepts:** `"equal"`, `"titleLength"`, `"compact"`</span></span>

<span data-ttu-id="28930-172">**Valore predefinito:** `"equal"`</span><span class="sxs-lookup"><span data-stu-id="28930-172">**Default value:** `"equal"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Modalità larghezza schede](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

### <a name="hide-close-all-tabs-popup"></a><span data-ttu-id="28930-174">Nascondi il popup di chiusura di tutte le schede</span><span class="sxs-lookup"><span data-stu-id="28930-174">Hide close all tabs popup</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="28930-175">Quando è impostata su `true`, alla chiusura di una finestra con più schede aperte _verrà_ richiesta una conferma.</span><span class="sxs-lookup"><span data-stu-id="28930-175">When this is set to `true`, closing a window with multiple tabs open _will_ require confirmation.</span></span> <span data-ttu-id="28930-176">Quando è impostata su `false`, alla chiusura di una finestra con più schede aperte _non verrà_ richiesta alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="28930-176">When it's set to `false`, closing a window with multiple tabs open _will not_ require confirmation.</span></span>

<span data-ttu-id="28930-177">**Nome della proprietà:** `confirmCloseAllTabs`</span><span class="sxs-lookup"><span data-stu-id="28930-177">**Property name:** `confirmCloseAllTabs`</span></span>

<span data-ttu-id="28930-178">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-178">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-179">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-179">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-180">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-180">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

<br />

___

## <a name="launch-settings"></a><span data-ttu-id="28930-182">Impostazioni per l'avvio</span><span class="sxs-lookup"><span data-stu-id="28930-182">Launch settings</span></span>

### <a name="launch-on-startup"></a><span data-ttu-id="28930-183">Avvia all'avvio</span><span class="sxs-lookup"><span data-stu-id="28930-183">Launch on startup</span></span>

<span data-ttu-id="28930-184">Se questa proprietà è impostata su `true`, abilita l'avvio di Terminale Windows all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="28930-184">When set to `true`, this enables the launch of Windows Terminal at startup.</span></span> <span data-ttu-id="28930-185">L'impostazione su `false` disabiliterà la voce dell'attività di avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="28930-185">Setting this to `false` will disable the startup task entry.</span></span> <span data-ttu-id="28930-186">Nota: se la voce dell'attività di avvio del sistema di Terminale Windows viene disabilitata da criteri dell'organizzazione o da un'azione dell'utente, questa impostazione non avrà effetto.</span><span class="sxs-lookup"><span data-stu-id="28930-186">Note: if the Windows Terminal startup task entry is disabled either by org policy or by user action this setting will have no effect.</span></span>

<span data-ttu-id="28930-187">**Nome della proprietà:** `startOnUserLogin`</span><span class="sxs-lookup"><span data-stu-id="28930-187">**Property name:** `startOnUserLogin`</span></span>

<span data-ttu-id="28930-188">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-188">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-189">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-189">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-190">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="28930-190">**Default value:** `false`</span></span>

### <a name="launch-mode"></a><span data-ttu-id="28930-191">Modalità di avvio</span><span class="sxs-lookup"><span data-stu-id="28930-191">Launch mode</span></span>

<span data-ttu-id="28930-192">Definisce se il terminale verrà avviato come ingrandito, a schermo intero o in una finestra.</span><span class="sxs-lookup"><span data-stu-id="28930-192">This defines whether the terminal will launch as maximized, full screen, or in a window.</span></span> <span data-ttu-id="28930-193">L'impostazione di questa opzione su `focus` equivale all'avvio del terminale in `default` modalità, ma con la [modalità messa a fuoco](./actions.md#toggle-focus-mode) abilitata.</span><span class="sxs-lookup"><span data-stu-id="28930-193">Setting this to `focus` is equivalent to launching the terminal in the `default` mode, but with [focus mode](./actions.md#toggle-focus-mode) enabled.</span></span> <span data-ttu-id="28930-194">Analogamente, l'impostazione di questa opzione su comporterà `maximizedFocus` l'avvio del terminale in una finestra ingrandita con la modalità messa a fuoco abilitata.</span><span class="sxs-lookup"><span data-stu-id="28930-194">Similarly, setting this to `maximizedFocus` will result in launching the terminal in a maximized window with focus mode enabled.</span></span>

<span data-ttu-id="28930-195">**Nome della proprietà:** `launchMode`</span><span class="sxs-lookup"><span data-stu-id="28930-195">**Property name:** `launchMode`</span></span>

<span data-ttu-id="28930-196">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-196">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-197">**Accetta:** `"default"`, `"maximized"`, `"fullscreen"`, `"focus"`, `"maximizedFocus"`</span><span class="sxs-lookup"><span data-stu-id="28930-197">**Accepts:** `"default"`, `"maximized"`, `"fullscreen"`, `"focus"`, `"maximizedFocus"`</span></span>

<span data-ttu-id="28930-198">**Valore predefinito:** `"default"`</span><span class="sxs-lookup"><span data-stu-id="28930-198">**Default value:** `"default"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28930-199">Le `"focus"` `"maximizedFocus"` modalità e sono disponibili solo in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="28930-199">The `"focus"` and `"maximizedFocus"` modes are only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="launch-position"></a><span data-ttu-id="28930-200">Posizione di avvio</span><span class="sxs-lookup"><span data-stu-id="28930-200">Launch position</span></span>

<span data-ttu-id="28930-201">Consente di impostare la posizione in pixel dell'angolo superiore sinistro della finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="28930-201">This sets the pixel position of the top left corner of the window upon first load.</span></span> <span data-ttu-id="28930-202">In un sistema con più schermi queste coordinate si riferiscono all'angolo superiore sinistro dello schermo principale.</span><span class="sxs-lookup"><span data-stu-id="28930-202">On a system with multiple displays, these coordinates are relative to the top left of the primary display.</span></span> <span data-ttu-id="28930-203">Se non viene specificata una coordinata X o Y, il terminale userà l'impostazione predefinita del sistema per tale valore.</span><span class="sxs-lookup"><span data-stu-id="28930-203">If an X or Y coordinate is not provided, the terminal will use the system default for that value.</span></span> <span data-ttu-id="28930-204">Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , la finestra verrà ingrandita sul monitoraggio specificato da tali coordinate.</span><span class="sxs-lookup"><span data-stu-id="28930-204">If `launchMode` is set to `"maximized"` or `"maximizedFocus"`, the window will be maximized on the monitor specified by those coordinates.</span></span>

<span data-ttu-id="28930-205">**Nome della proprietà:** `initialPosition`</span><span class="sxs-lookup"><span data-stu-id="28930-205">**Property name:** `initialPosition`</span></span>

<span data-ttu-id="28930-206">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-206">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-207">**Accetta:** coordinate nei formati stringa seguenti: `","`, `"#,#"`, `"#,"`, `",#"`</span><span class="sxs-lookup"><span data-stu-id="28930-207">**Accepts:** Coordinates as a string in the following formats: `","`, `"#,#"`, `"#,"`, `",#"`</span></span>

<span data-ttu-id="28930-208">**Valore predefinito:** `","`</span><span class="sxs-lookup"><span data-stu-id="28930-208">**Default value:** `","`</span></span>

### <a name="columns-on-first-launch"></a><span data-ttu-id="28930-209">Colonne al primo avvio</span><span class="sxs-lookup"><span data-stu-id="28930-209">Columns on first launch</span></span>

<span data-ttu-id="28930-210">Numero di colonne di tipo carattere visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="28930-210">This is the number of character columns displayed in the window upon first load.</span></span> <span data-ttu-id="28930-211">Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="28930-211">If `launchMode` is set to `"maximized"` or `"maximizedFocus"`, this property is ignored.</span></span>

<span data-ttu-id="28930-212">**Nome della proprietà:** `initialCols`</span><span class="sxs-lookup"><span data-stu-id="28930-212">**Property name:** `initialCols`</span></span>

<span data-ttu-id="28930-213">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-213">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-214">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="28930-214">**Accepts:** Integer</span></span>

<span data-ttu-id="28930-215">**Valore predefinito:** `120`</span><span class="sxs-lookup"><span data-stu-id="28930-215">**Default value:** `120`</span></span>

### <a name="rows-on-first-launch"></a><span data-ttu-id="28930-216">Righe al primo avvio</span><span class="sxs-lookup"><span data-stu-id="28930-216">Rows on first launch</span></span>

<span data-ttu-id="28930-217">Numero di righe visualizzate nella finestra al primo caricamento.</span><span class="sxs-lookup"><span data-stu-id="28930-217">This is the number of rows displayed in the window upon first load.</span></span> <span data-ttu-id="28930-218">Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="28930-218">If `launchMode` is set to `"maximized"` or `"maximizedFocus"`, this property is ignored.</span></span>

<span data-ttu-id="28930-219">**Nome della proprietà:** `initialRows`</span><span class="sxs-lookup"><span data-stu-id="28930-219">**Property name:** `initialRows`</span></span>

<span data-ttu-id="28930-220">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-220">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-221">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="28930-221">**Accepts:** Integer</span></span>

<span data-ttu-id="28930-222">**Valore predefinito:** `30`</span><span class="sxs-lookup"><span data-stu-id="28930-222">**Default value:** `30`</span></span>

### <a name="always-on-top-mode"></a><span data-ttu-id="28930-223">Modalità sempre in primo piano</span><span class="sxs-lookup"><span data-stu-id="28930-223">Always on top mode</span></span>

<span data-ttu-id="28930-224">Quando è impostato su true, Windows Terminal viene avviato in tutte le altre finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="28930-224">When set to true, Windows Terminal windows will launch on top of all other windows on the desktop.</span></span> <span data-ttu-id="28930-225">Questo stato può anche essere attivato o disattivato con l' `toggleAlwaysOnTop` associazione di tasti.</span><span class="sxs-lookup"><span data-stu-id="28930-225">This state can also be toggled with the `toggleAlwaysOnTop` key binding.</span></span>

<span data-ttu-id="28930-226">**Nome della proprietà:** `alwaysOnTop`</span><span class="sxs-lookup"><span data-stu-id="28930-226">**Property name:** `alwaysOnTop`</span></span>

<span data-ttu-id="28930-227">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-227">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-228">**Accetta:**`true, false`</span><span class="sxs-lookup"><span data-stu-id="28930-228">**Accepts:** `true, false`</span></span>

<span data-ttu-id="28930-229">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="28930-229">**Default value:** `false`</span></span>

<br />

___

## <a name="title-bar-settings"></a><span data-ttu-id="28930-230">Impostazioni per la barra del titolo</span><span class="sxs-lookup"><span data-stu-id="28930-230">Title bar settings</span></span>

### <a name="showhide-the-title-bar"></a><span data-ttu-id="28930-231">Mostra/Nascondi la barra del titolo</span><span class="sxs-lookup"><span data-stu-id="28930-231">Show/Hide the title bar</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="28930-232">Quando è impostata su `true`, le schede vengono spostate nella barra del titolo e la barra del titolo scompare.</span><span class="sxs-lookup"><span data-stu-id="28930-232">When this is set to `true`, the tabs are moved into the title bar and the title bar disappears.</span></span> <span data-ttu-id="28930-233">Quando è impostata su `false`, la barra del titolo si trova sopra le schede.</span><span class="sxs-lookup"><span data-stu-id="28930-233">When it's set to `false`, the title bar sits above the tabs.</span></span> <span data-ttu-id="28930-234">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="28930-234">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="28930-235">**Nome della proprietà:** `showTabsInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="28930-235">**Property name:** `showTabsInTitlebar`</span></span>

<span data-ttu-id="28930-236">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-236">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-237">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-237">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-238">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-238">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Mostra le schede nella barra del titolo](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

### <a name="set-the-text-in-the-title-bar"></a><span data-ttu-id="28930-240">Imposta il testo nella barra del titolo</span><span class="sxs-lookup"><span data-stu-id="28930-240">Set the text in the title bar</span></span>

<span data-ttu-id="28930-241">Quando è impostata su `true`, la barra del titolo visualizza il titolo della scheda selezionata. Quando è impostata su `false`, la barra del titolo visualizza "Terminale Windows".</span><span class="sxs-lookup"><span data-stu-id="28930-241">When this is set to `true`, the title bar displays the title of the selected tab. When it's set to `false`, title bar displays "Windows Terminal".</span></span> <span data-ttu-id="28930-242">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="28930-242">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="28930-243">**Nome della proprietà:** `showTerminalTitleInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="28930-243">**Property name:** `showTerminalTitleInTitlebar`</span></span>

<span data-ttu-id="28930-244">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-244">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-245">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-245">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-246">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-246">**Default value:** `true`</span></span>

<br />

___

## <a name="selection-settings"></a><span data-ttu-id="28930-247">Impostazioni per le selezioni</span><span class="sxs-lookup"><span data-stu-id="28930-247">Selection settings</span></span>

### <a name="copy-after-selection-is-made"></a><span data-ttu-id="28930-248">Copia dopo che è stata effettuata la selezione</span><span class="sxs-lookup"><span data-stu-id="28930-248">Copy after selection is made</span></span>

<span data-ttu-id="28930-249">Quando è impostata su `true`, una selezione viene immediatamente copiata negli Appunti al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="28930-249">When this is set to `true`, a selection is immediately copied to your clipboard upon creation.</span></span> <span data-ttu-id="28930-250">In questo caso facendo clic con il pulsante destro del mouse, la selezione verrà sempre incollata.</span><span class="sxs-lookup"><span data-stu-id="28930-250">The right-click on your mouse will always paste in this case.</span></span> <span data-ttu-id="28930-251">Quando è impostata su `false`, la selezione viene mantenuta in attesa di altre azioni.</span><span class="sxs-lookup"><span data-stu-id="28930-251">When it's set to `false`, the selection persists and awaits further action.</span></span> <span data-ttu-id="28930-252">Facendo clic con il pulsante destro del mouse, la selezione verrà copiata.</span><span class="sxs-lookup"><span data-stu-id="28930-252">Using your mouse to right-click will copy the selection.</span></span>

<span data-ttu-id="28930-253">**Nome della proprietà:** `copyOnSelect`</span><span class="sxs-lookup"><span data-stu-id="28930-253">**Property name:** `copyOnSelect`</span></span>

<span data-ttu-id="28930-254">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-254">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-255">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-255">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-256">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="28930-256">**Default value:** `false`</span></span>

### <a name="copy-formatting"></a><span data-ttu-id="28930-257">Copia formattazione</span><span class="sxs-lookup"><span data-stu-id="28930-257">Copy formatting</span></span>

<span data-ttu-id="28930-258">Quando è impostato su `true` , la formattazione del colore e del carattere del testo selezionato viene anche copiata negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="28930-258">When this is set to `true`, the color and font formatting of the selected text is also copied to your clipboard.</span></span> <span data-ttu-id="28930-259">Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale.</span><span class="sxs-lookup"><span data-stu-id="28930-259">When it's set to `false`, only plain text is copied to your clipboard.</span></span> <span data-ttu-id="28930-260">È inoltre possibile specificare i formati che si desidera copiare.</span><span class="sxs-lookup"><span data-stu-id="28930-260">You can also specify which formats you would like to copy.</span></span>

<span data-ttu-id="28930-261">**Nome della proprietà:** `copyFormatting`</span><span class="sxs-lookup"><span data-stu-id="28930-261">**Property name:** `copyFormatting`</span></span>

<span data-ttu-id="28930-262">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-262">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-263">**Accetta:** `true` , `false` , `"all"` , `"none"` , `"html"` , `"rtf"`</span><span class="sxs-lookup"><span data-stu-id="28930-263">**Accepts:** `true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"`</span></span>

<span data-ttu-id="28930-264">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="28930-264">**Default value:** `false`</span></span>

### <a name="word-delimiters"></a><span data-ttu-id="28930-265">Delimitatori di parola</span><span class="sxs-lookup"><span data-stu-id="28930-265">Word delimiters</span></span>

<span data-ttu-id="28930-266">Determina i delimitatori di parola usati quando si fa doppio clic per selezionare.</span><span class="sxs-lookup"><span data-stu-id="28930-266">This determines the word delimiters used in a double-click selection.</span></span> <span data-ttu-id="28930-267">I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole.</span><span class="sxs-lookup"><span data-stu-id="28930-267">Word delimiters are characters that specify where the boundary is between two words.</span></span> <span data-ttu-id="28930-268">Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.</span><span class="sxs-lookup"><span data-stu-id="28930-268">The most common examples are spaces, semicolons, commas, and periods.</span></span>

<span data-ttu-id="28930-269">**Nome della proprietà:** `wordDelimiters`</span><span class="sxs-lookup"><span data-stu-id="28930-269">**Property name:** `wordDelimiters`</span></span>

<span data-ttu-id="28930-270">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-270">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-271">**Accetta:** caratteri in formato stringa</span><span class="sxs-lookup"><span data-stu-id="28930-271">**Accepts:** Characters as a string</span></span>

<span data-ttu-id="28930-272">**Valore predefinito:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span><span class="sxs-lookup"><span data-stu-id="28930-272">**Default value:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span></span><br><span data-ttu-id="28930-273">_(`│` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span><span class="sxs-lookup"><span data-stu-id="28930-273">_(`│` is `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span></span>

<br />

___

## <a name="paste-warnings"></a><span data-ttu-id="28930-274">Avvisi incolla</span><span class="sxs-lookup"><span data-stu-id="28930-274">Paste warnings</span></span>

### <a name="warn-when-the-text-to-paste-is-very-large"></a><span data-ttu-id="28930-275">Avvisa quando il testo da incollare è molto grande</span><span class="sxs-lookup"><span data-stu-id="28930-275">Warn when the text to paste is very large</span></span>

<span data-ttu-id="28930-276">Quando è impostato su, quando si `true` tenta di incollare testo con più di 5 KiB di caratteri verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla.</span><span class="sxs-lookup"><span data-stu-id="28930-276">When this is set to `true`, trying to paste text with more than 5 KiB of characters will display a dialog asking you whether to continue or not with the paste.</span></span> <span data-ttu-id="28930-277">Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="28930-277">When it's set to `false`, the dialog is not shown and instead the text is pasted right away.</span></span> <span data-ttu-id="28930-278">Se spesso si fa clic con il pulsante destro del mouse sul terminale per errore dopo aver selezionato una grande quantità di testo, potrebbe essere utile evitare che il terminale non risponda mentre il programma connesso al terminale riceve il contenuto degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="28930-278">If you often right-click on the terminal by accident after having selected a lot of text, this might be useful to prevent the terminal from becoming unresponsive while the program connected to the terminal receives the clipboard's content.</span></span>

<span data-ttu-id="28930-279">**Nome della proprietà:** `largePasteWarning`</span><span class="sxs-lookup"><span data-stu-id="28930-279">**Property name:** `largePasteWarning`</span></span>

<span data-ttu-id="28930-280">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-280">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-281">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-281">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-282">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-282">**Default value:** `true`</span></span>

### <a name="warn-when-the-text-to-paste-contains-multiple-lines"></a><span data-ttu-id="28930-283">Avvisa quando il testo da incollare contiene più righe</span><span class="sxs-lookup"><span data-stu-id="28930-283">Warn when the text to paste contains multiple lines</span></span>

<span data-ttu-id="28930-284">Quando è impostato su, quando si `true` tenta di incollare testo con più righe verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla.</span><span class="sxs-lookup"><span data-stu-id="28930-284">When this is set to `true`, trying to paste text with multiple lines will display a dialog asking you whether to continue or not with the paste.</span></span> <span data-ttu-id="28930-285">Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="28930-285">When it's set to `false`, the dialog is not shown and instead the text is pasted right away.</span></span> <span data-ttu-id="28930-286">Nella maggior parte delle shell, una riga corrisponde a un comando, quindi se si incolla il testo che contiene il carattere "nuova riga" in una shell, è possibile che uno o più comandi vengano eseguiti automaticamente al termine della copia, senza che sia necessario convalidare i comandi.</span><span class="sxs-lookup"><span data-stu-id="28930-286">In most shells, one line corresponds to one command so if you paste text that contains the "new line" character into a shell, one or more command(s) might be executed automatically upon paste, without you having time to validate the commands.</span></span> <span data-ttu-id="28930-287">Questa operazione può essere utile se si copiano e si incollano spesso comandi da siti Web non attendibili.</span><span class="sxs-lookup"><span data-stu-id="28930-287">This can be useful if you often copy and paste commands from untrusted websites.</span></span>

<span data-ttu-id="28930-288">**Nome della proprietà:** `multiLinePasteWarning`</span><span class="sxs-lookup"><span data-stu-id="28930-288">**Property name:** `multiLinePasteWarning`</span></span>

<span data-ttu-id="28930-289">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-289">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-290">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-290">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-291">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-291">**Default value:** `true`</span></span>

<br />

___

## <a name="disable-animations-preview"></a><span data-ttu-id="28930-292">Disabilita animazioni ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="28930-292">Disable animations ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="28930-293">In questo modo vengono disabilitate le animazioni visive nell'applicazione quando è impostato su `true` .</span><span class="sxs-lookup"><span data-stu-id="28930-293">This disables visual animations across the application when set to `true`.</span></span>

<span data-ttu-id="28930-294">**Nome della proprietà:** `disableAnimations`</span><span class="sxs-lookup"><span data-stu-id="28930-294">**Property name:** `disableAnimations`</span></span>

<span data-ttu-id="28930-295">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-295">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-296">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-296">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-297">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="28930-297">**Default value:** `false`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28930-298">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="28930-298">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

<br />

___

## <a name="window-resize-behavior"></a><span data-ttu-id="28930-299">Comportamento di ridimensionamento delle finestre</span><span class="sxs-lookup"><span data-stu-id="28930-299">Window resize behavior</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="28930-300">Quando è impostata su `true`, la finestra verrà allineata al limite del carattere più vicino quando viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="28930-300">When this is set to `true`, the window will snap to the nearest character boundary on resize.</span></span> <span data-ttu-id="28930-301">Quando è impostata su `false`, la finestra verrà ridimensionata senza vincoli.</span><span class="sxs-lookup"><span data-stu-id="28930-301">When it's set to `false`, the window will resize "smoothly".</span></span>

<span data-ttu-id="28930-302">**Nome della proprietà:** `snapToGridOnResize`</span><span class="sxs-lookup"><span data-stu-id="28930-302">**Property name:** `snapToGridOnResize`</span></span>

<span data-ttu-id="28930-303">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-303">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-304">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-304">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-305">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="28930-305">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Blocca sulla griglia al ridimensionamento](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="rendering-settings"></a><span data-ttu-id="28930-307">Impostazioni di rendering</span><span class="sxs-lookup"><span data-stu-id="28930-307">Rendering settings</span></span>

<span data-ttu-id="28930-308">Per cambiare le impostazioni di rendering, vedere le informazioni aggiuntive disponibili nella [pagina sulla risoluzione dei problemi](./../troubleshooting.md#the-text-is-blurry) per assistenza.</span><span class="sxs-lookup"><span data-stu-id="28930-308">If you are thinking about changing the rendering settings, additional information is provided on the [Troubleshooting page](./../troubleshooting.md#the-text-is-blurry) to help guide you.</span></span>

### <a name="screen-redrawing"></a><span data-ttu-id="28930-309">Ridisegno dello schermo</span><span class="sxs-lookup"><span data-stu-id="28930-309">Screen redrawing</span></span>

<span data-ttu-id="28930-310">Se questa proprietà è impostata su `true`, il terminale ridisegnerà ogni frame dello schermo.</span><span class="sxs-lookup"><span data-stu-id="28930-310">When this set to `true`, the terminal will redraw the entire screen each frame.</span></span> <span data-ttu-id="28930-311">Se è impostata su `false`, verrà eseguito solo il rendering degli aggiornamenti dello schermo tra frame.</span><span class="sxs-lookup"><span data-stu-id="28930-311">When set to `false`, it will render only the updates to the screen between frames.</span></span>

<span data-ttu-id="28930-312">**Nome della proprietà:** `experimental.rendering.forceFullRepaint`</span><span class="sxs-lookup"><span data-stu-id="28930-312">**Property name:** `experimental.rendering.forceFullRepaint`</span></span>

<span data-ttu-id="28930-313">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-313">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-314">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-314">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-315">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="28930-315">**Default value:** `false`</span></span>

### <a name="software-rendering"></a><span data-ttu-id="28930-316">Rendering del software</span><span class="sxs-lookup"><span data-stu-id="28930-316">Software rendering</span></span>

<span data-ttu-id="28930-317">Se questa proprietà è impostata su `true`, il terminale userà il renderer software, ossia</span><span class="sxs-lookup"><span data-stu-id="28930-317">When this is set to `true`, the terminal will use the software renderer (a.k.a.</span></span> <span data-ttu-id="28930-318">WARP, invece di quello hardware.</span><span class="sxs-lookup"><span data-stu-id="28930-318">WARP) instead of the hardware one.</span></span>

<span data-ttu-id="28930-319">**Nome della proprietà:** `experimental.rendering.software`</span><span class="sxs-lookup"><span data-stu-id="28930-319">**Property name:** `experimental.rendering.software`</span></span>

<span data-ttu-id="28930-320">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="28930-320">**Necessity:** Optional</span></span>

<span data-ttu-id="28930-321">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="28930-321">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="28930-322">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="28930-322">**Default value:** `false`</span></span>
