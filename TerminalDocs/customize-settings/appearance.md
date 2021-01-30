---
title: Impostazioni aspetto terminale Windows
description: Informazioni su come personalizzare le impostazioni di aspetto nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 0393cecf59a9b0dd1dce4aecf7fe11df1b5a4a63
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041978"
---
# <a name="appearance-settings-in-windows-terminal"></a><span data-ttu-id="a0bc9-103">Impostazioni aspetto nel terminale Windows</span><span class="sxs-lookup"><span data-stu-id="a0bc9-103">Appearance settings in Windows Terminal</span></span>

<span data-ttu-id="a0bc9-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="a0bc9-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-105">These should be placed at the root of your settings.json file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0bc9-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="a0bc9-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="a0bc9-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="a0bc9-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="theme"></a><span data-ttu-id="a0bc9-108">Tema</span><span class="sxs-lookup"><span data-stu-id="a0bc9-108">Theme</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="a0bc9-109">Consente di impostare il tema dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-109">This sets the theme of the application.</span></span> <span data-ttu-id="a0bc9-110">Con `"system"` viene usato lo stesso tema di Windows.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-110">`"system"` will use the same theme as Windows.</span></span>

<span data-ttu-id="a0bc9-111">**Nome della proprietà:** `theme`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-111">**Property name:** `theme`</span></span>

<span data-ttu-id="a0bc9-112">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-112">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-113">**Accetta:** `"system"`, `"dark"`, `"light"`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-113">**Accepts:** `"system"`, `"dark"`, `"light"`</span></span>

<span data-ttu-id="a0bc9-114">**Valore predefinito:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-114">**Default value:** `"system"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="a0bc9-115">![Terminale Windows - Tema scuro](./../images/requested-themes.gif)
_Configurazione: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="a0bc9-115">![Windows Terminal dark theme](./../images/requested-themes.gif)
_Configuration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="always-show-tabs"></a><span data-ttu-id="a0bc9-116">Mostra sempre le schede</span><span class="sxs-lookup"><span data-stu-id="a0bc9-116">Always show tabs</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="a0bc9-117">Quando è impostata su `true`, le schede vengono sempre visualizzate.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-117">When this is set to `true`, tabs are always displayed.</span></span> <span data-ttu-id="a0bc9-118">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `true`, le schede vengono sempre visualizzate sotto la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-118">When it's set to `false` and `showTabsInTitlebar` is set to `true`, tabs are always displayed underneath the title bar.</span></span> <span data-ttu-id="a0bc9-119">Quando è impostata su `false` e `showTabsInTitlebar` è impostata su `false`, le schede vengono visualizzate solo se sono presenti più schede digitando <kbd>ctrl+shift+t</kbd> oppure digitando il tasto di scelta rapida assegnato a `newTab`.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-119">When this is set to `false` and `showTabsInTitlebar` is set to `false`, tabs only appear after more than one tab exists by typing <kbd>ctrl+shift+t</kbd> or by typing the key binding assigned to `newTab`.</span></span> <span data-ttu-id="a0bc9-120">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-120">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="a0bc9-121">**Nome della proprietà:** `alwaysShowTabs`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-121">**Property name:** `alwaysShowTabs`</span></span>

<span data-ttu-id="a0bc9-122">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-122">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-123">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-123">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="a0bc9-124">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-124">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Visualizza sempre le schede](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="hide-the-title-bar"></a><span data-ttu-id="a0bc9-126">Nascondi la barra del titolo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-126">Hide the title bar</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="a0bc9-127">Quando è impostata su `true`, le schede vengono spostate nella barra del titolo e la barra del titolo scompare.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-127">When this is set to `true`, the tabs are moved into the title bar and the title bar disappears.</span></span> <span data-ttu-id="a0bc9-128">Quando è impostata su `false`, la barra del titolo si trova sopra le schede.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-128">When it's set to `false`, the title bar sits above the tabs.</span></span> <span data-ttu-id="a0bc9-129">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-129">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="a0bc9-130">**Nome della proprietà:** `showTabsInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-130">**Property name:** `showTabsInTitlebar`</span></span>

<span data-ttu-id="a0bc9-131">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-131">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-132">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-132">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="a0bc9-133">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-133">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Mostra le schede nella barra del titolo](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="use-active-terminal-title-as-application-title"></a><span data-ttu-id="a0bc9-135">USA titolo del terminale attivo come titolo dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="a0bc9-135">Use active terminal title as application title</span></span>

<span data-ttu-id="a0bc9-136">Quando è impostata su `true`, la barra del titolo visualizza il titolo della scheda selezionata. Quando è impostata su `false`, la barra del titolo visualizza "Terminale Windows".</span><span class="sxs-lookup"><span data-stu-id="a0bc9-136">When this is set to `true`, the title bar displays the title of the selected tab. When it's set to `false`, title bar displays "Windows Terminal".</span></span> <span data-ttu-id="a0bc9-137">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-137">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="a0bc9-138">**Nome della proprietà:** `showTerminalTitleInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-138">**Property name:** `showTerminalTitleInTitlebar`</span></span>

<span data-ttu-id="a0bc9-139">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-139">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-140">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-140">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="a0bc9-141">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-141">**Default value:** `true`</span></span>

<br />

___

## <a name="always-on-top-mode"></a><span data-ttu-id="a0bc9-142">Modalità sempre in primo piano</span><span class="sxs-lookup"><span data-stu-id="a0bc9-142">Always on top mode</span></span>

<span data-ttu-id="a0bc9-143">Quando è impostato su true, Windows Terminal viene avviato in tutte le altre finestre sul desktop.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-143">When set to true, Windows Terminal windows will launch on top of all other windows on the desktop.</span></span> <span data-ttu-id="a0bc9-144">Questo stato può anche essere attivato o disattivato con l' `toggleAlwaysOnTop` associazione di tasti.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-144">This state can also be toggled with the `toggleAlwaysOnTop` key binding.</span></span>

<span data-ttu-id="a0bc9-145">**Nome della proprietà:** `alwaysOnTop`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-145">**Property name:** `alwaysOnTop`</span></span>

<span data-ttu-id="a0bc9-146">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-146">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-147">**Accetta:**`true, false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-147">**Accepts:** `true, false`</span></span>

<span data-ttu-id="a0bc9-148">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-148">**Default value:** `false`</span></span>

<br />

___

## <a name="tab-width-mode"></a><span data-ttu-id="a0bc9-149">Modalità larghezza schede</span><span class="sxs-lookup"><span data-stu-id="a0bc9-149">Tab width mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="a0bc9-150">Consente di impostare la larghezza delle schede.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-150">This sets the width of the tabs.</span></span> <span data-ttu-id="a0bc9-151">Con `"equal"` tutte le schede hanno la stessa larghezza.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-151">`"equal"` makes each tab the same width.</span></span> <span data-ttu-id="a0bc9-152">Con `"titleLength"` ogni scheda viene adattata alla lunghezza del titolo.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-152">`"titleLength"` sizes each tab to the length of its title.</span></span> <span data-ttu-id="a0bc9-153">`"compact"` comprime tutte le schede inattive fino alla larghezza dell'icona, lasciando alla scheda attiva più spazio per visualizzare il titolo completo.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-153">`"compact"` will shrink every inactive tab to the width of the icon, leaving the active tab more space to display its full title.</span></span>

<span data-ttu-id="a0bc9-154">**Nome della proprietà:** `tabWidthMode`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-154">**Property name:** `tabWidthMode`</span></span>

<span data-ttu-id="a0bc9-155">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-155">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-156">**Accetta:** `"equal"`, `"titleLength"`, `"compact"`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-156">**Accepts:** `"equal"`, `"titleLength"`, `"compact"`</span></span>

<span data-ttu-id="a0bc9-157">**Valore predefinito:** `"equal"`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-157">**Default value:** `"equal"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Modalità larghezza schede](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="disable-pane-animations"></a><span data-ttu-id="a0bc9-159">Disabilita animazioni del riquadro</span><span class="sxs-lookup"><span data-stu-id="a0bc9-159">Disable pane animations</span></span>

<span data-ttu-id="a0bc9-160">In questo modo vengono disabilitate le animazioni visive nell'applicazione quando è impostato su `true` .</span><span class="sxs-lookup"><span data-stu-id="a0bc9-160">This disables visual animations across the application when set to `true`.</span></span>

<span data-ttu-id="a0bc9-161">**Nome della proprietà:** `disableAnimations`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-161">**Property name:** `disableAnimations`</span></span>

<span data-ttu-id="a0bc9-162">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-162">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-163">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-163">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="a0bc9-164">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-164">**Default value:** `false`</span></span>

<br />

___

## <a name="show-close-all-tabs-popup"></a><span data-ttu-id="a0bc9-165">Mostra finestra di chiusura di tutte le schede popup</span><span class="sxs-lookup"><span data-stu-id="a0bc9-165">Show close all tabs popup</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="a0bc9-166">Quando è impostata su `true`, alla chiusura di una finestra con più schede aperte _verrà_ richiesta una conferma.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-166">When this is set to `true`, closing a window with multiple tabs open _will_ require confirmation.</span></span> <span data-ttu-id="a0bc9-167">Quando è impostata su `false`, alla chiusura di una finestra con più schede aperte _non verrà_ richiesta alcuna conferma.</span><span class="sxs-lookup"><span data-stu-id="a0bc9-167">When it's set to `false`, closing a window with multiple tabs open _will not_ require confirmation.</span></span>

<span data-ttu-id="a0bc9-168">**Nome della proprietà:** `confirmCloseAllTabs`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-168">**Property name:** `confirmCloseAllTabs`</span></span>

<span data-ttu-id="a0bc9-169">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a0bc9-169">**Necessity:** Optional</span></span>

<span data-ttu-id="a0bc9-170">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-170">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="a0bc9-171">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="a0bc9-171">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::
