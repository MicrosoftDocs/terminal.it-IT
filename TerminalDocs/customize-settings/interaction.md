---
title: Impostazioni di interazione del terminale di Windows
description: Informazioni su come personalizzare le impostazioni di interazione nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 6eb6b0383f35de7406bde9f454ec60b498a9019c
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974942"
---
# <a name="interaction-settings-in-windows-terminal"></a><span data-ttu-id="36748-103">Impostazioni di interazione nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="36748-103">Interaction settings in Windows Terminal</span></span>

<span data-ttu-id="36748-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="36748-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="36748-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="36748-105">These should be placed at the root of your settings.json file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36748-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="36748-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="36748-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="36748-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="automatically-copy-selection-to-clipboard"></a><span data-ttu-id="36748-108">Copia automaticamente selezione negli Appunti</span><span class="sxs-lookup"><span data-stu-id="36748-108">Automatically copy selection to clipboard</span></span>

<span data-ttu-id="36748-109">Quando è impostata su `true`, una selezione viene immediatamente copiata negli Appunti al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="36748-109">When this is set to `true`, a selection is immediately copied to your clipboard upon creation.</span></span> <span data-ttu-id="36748-110">In questo caso facendo clic con il pulsante destro del mouse, la selezione verrà sempre incollata.</span><span class="sxs-lookup"><span data-stu-id="36748-110">The right-click on your mouse will always paste in this case.</span></span> <span data-ttu-id="36748-111">Quando è impostata su `false`, la selezione viene mantenuta in attesa di altre azioni.</span><span class="sxs-lookup"><span data-stu-id="36748-111">When it's set to `false`, the selection persists and awaits further action.</span></span> <span data-ttu-id="36748-112">Facendo clic con il pulsante destro del mouse, la selezione verrà copiata.</span><span class="sxs-lookup"><span data-stu-id="36748-112">Using your mouse to right-click will copy the selection.</span></span>

<span data-ttu-id="36748-113">**Nome della proprietà:** `copyOnSelect`</span><span class="sxs-lookup"><span data-stu-id="36748-113">**Property name:** `copyOnSelect`</span></span>

<span data-ttu-id="36748-114">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-114">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-115">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="36748-115">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="36748-116">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="36748-116">**Default value:** `false`</span></span>

<br />

___

## <a name="text-format-when-copying"></a><span data-ttu-id="36748-117">Formato testo durante la copia</span><span class="sxs-lookup"><span data-stu-id="36748-117">Text format when copying</span></span>

<span data-ttu-id="36748-118">Quando è impostato su `true` , la formattazione del colore e del carattere del testo selezionato viene anche copiata negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="36748-118">When this is set to `true`, the color and font formatting of the selected text is also copied to your clipboard.</span></span> <span data-ttu-id="36748-119">Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale.</span><span class="sxs-lookup"><span data-stu-id="36748-119">When it's set to `false`, only plain text is copied to your clipboard.</span></span> <span data-ttu-id="36748-120">È inoltre possibile specificare i formati che si desidera copiare.</span><span class="sxs-lookup"><span data-stu-id="36748-120">You can also specify which formats you would like to copy.</span></span>

<span data-ttu-id="36748-121">**Nome della proprietà:** `copyFormatting`</span><span class="sxs-lookup"><span data-stu-id="36748-121">**Property name:** `copyFormatting`</span></span>

<span data-ttu-id="36748-122">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-122">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-123">**Accetta:** `true` , `false` , `"all"` , `"none"` , `"html"` , `"rtf"`</span><span class="sxs-lookup"><span data-stu-id="36748-123">**Accepts:** `true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"`</span></span>

<span data-ttu-id="36748-124">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="36748-124">**Default value:** `false`</span></span>

<br />

___

## <a name="word-delimiters"></a><span data-ttu-id="36748-125">Delimitatori di parola</span><span class="sxs-lookup"><span data-stu-id="36748-125">Word delimiters</span></span>

<span data-ttu-id="36748-126">Determina i delimitatori di parola usati quando si fa doppio clic per selezionare.</span><span class="sxs-lookup"><span data-stu-id="36748-126">This determines the word delimiters used in a double-click selection.</span></span> <span data-ttu-id="36748-127">I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole.</span><span class="sxs-lookup"><span data-stu-id="36748-127">Word delimiters are characters that specify where the boundary is between two words.</span></span> <span data-ttu-id="36748-128">Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.</span><span class="sxs-lookup"><span data-stu-id="36748-128">The most common examples are spaces, semicolons, commas, and periods.</span></span>

<span data-ttu-id="36748-129">**Nome della proprietà:** `wordDelimiters`</span><span class="sxs-lookup"><span data-stu-id="36748-129">**Property name:** `wordDelimiters`</span></span>

<span data-ttu-id="36748-130">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-130">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-131">**Accetta:** caratteri in formato stringa</span><span class="sxs-lookup"><span data-stu-id="36748-131">**Accepts:** Characters as a string</span></span>

<span data-ttu-id="36748-132">**Valore predefinito:**</span><span class="sxs-lookup"><span data-stu-id="36748-132">**Default value:**</span></span> 
<code>&nbsp;&#x2f;&#x5c;&#x5c;&#x28;&#x29;&#x5c;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code>
<br><span data-ttu-id="36748-133">
_(`│\` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span><span class="sxs-lookup"><span data-stu-id="36748-133">
_(`│\` is `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36748-134">I caratteri seguenti devono essere preceduti da una barra rovesciata `\` : `"`</span><span class="sxs-lookup"><span data-stu-id="36748-134">The following characters must be escaped with a backslash : `\`, `"`</span></span>

___

## <a name="snap-window-resizing-to-character-grid"></a><span data-ttu-id="36748-135">Blocca la finestra di ridimensionamento in griglia caratteri</span><span class="sxs-lookup"><span data-stu-id="36748-135">Snap window resizing to character grid</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="36748-136">Quando è impostata su `true`, la finestra verrà allineata al limite del carattere più vicino quando viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="36748-136">When this is set to `true`, the window will snap to the nearest character boundary on resize.</span></span> <span data-ttu-id="36748-137">Quando è impostata su `false`, la finestra verrà ridimensionata senza vincoli.</span><span class="sxs-lookup"><span data-stu-id="36748-137">When it's set to `false`, the window will resize "smoothly".</span></span>

<span data-ttu-id="36748-138">**Nome della proprietà:** `snapToGridOnResize`</span><span class="sxs-lookup"><span data-stu-id="36748-138">**Property name:** `snapToGridOnResize`</span></span>

<span data-ttu-id="36748-139">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-139">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-140">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="36748-140">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="36748-141">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="36748-141">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Blocca sulla griglia al ridimensionamento](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a><span data-ttu-id="36748-143">Impostazioni per le schede</span><span class="sxs-lookup"><span data-stu-id="36748-143">Tab settings</span></span>

### <a name="tab-switcher-interface-style"></a><span data-ttu-id="36748-144">Stile dell'interfaccia Switcher di tabulazione</span><span class="sxs-lookup"><span data-stu-id="36748-144">Tab switcher interface style</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="36748-145">Quando è impostato su `true` o `"mru"` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda, con l'ordine di utilizzo più recente.</span><span class="sxs-lookup"><span data-stu-id="36748-145">When this is set to `true` or `"mru"`, the `nextTab` and `prevTab` commands will use the tab switcher UI, with most recently used ordering.</span></span> <span data-ttu-id="36748-146">Quando è impostato su `"inOrder"` , queste azioni cambieranno le schede nell'ordine corrente sulla barra della scheda.</span><span class="sxs-lookup"><span data-stu-id="36748-146">When set to `"inOrder"`, these actions will switch tabs in their current order in the tab bar.</span></span> <span data-ttu-id="36748-147">L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.</span><span class="sxs-lookup"><span data-stu-id="36748-147">The UI will show all the currently open tabs in a vertical list, navigable with the keyboard or mouse.</span></span>

<span data-ttu-id="36748-148">Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto.</span><span class="sxs-lookup"><span data-stu-id="36748-148">The tab switcher will open on the initial press of the actions for `nextTab` and `prevTab`, and will stay open as long as a modifier key is held down.</span></span> <span data-ttu-id="36748-149">Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="36748-149">When all modifier keys are released, the switcher will close and the highlighted tab will be focused.</span></span> <span data-ttu-id="36748-150"><kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.</span><span class="sxs-lookup"><span data-stu-id="36748-150"><kbd>tab</kbd>/<kbd>shift+tab</kbd>, the <kbd>up</kbd> and <kbd>down</kbd> arrow keys, and the `nextTab`/`prevTab` actions can be used to cycle through the switcher UI.</span></span>

<span data-ttu-id="36748-151">Per disabilitare lo switcher di tabulazione, è possibile impostare questa impostazione su `false` o su `"disabled"` .</span><span class="sxs-lookup"><span data-stu-id="36748-151">To disable the tab switcher, you can set this to `false` or `"disabled"`.</span></span>

<span data-ttu-id="36748-152">**Nome della proprietà:** `tabSwitcherMode`</span><span class="sxs-lookup"><span data-stu-id="36748-152">**Property name:** `tabSwitcherMode`</span></span>

<span data-ttu-id="36748-153">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-153">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-154">**Accetta:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`</span><span class="sxs-lookup"><span data-stu-id="36748-154">**Accepts:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`</span></span>

<span data-ttu-id="36748-155">**Valore predefinito:** `"inOrder"`</span><span class="sxs-lookup"><span data-stu-id="36748-155">**Default value:** `"inOrder"`</span></span>

:::column-end:::
:::column span="":::
![Switcher Scheda terminale Windows](./../images/tab-switcher.gif)

:::column-end:::
:::row-end:::

### <a name="enable-tab-switcher"></a><span data-ttu-id="36748-157">Abilita Switcher schede</span><span class="sxs-lookup"><span data-stu-id="36748-157">Enable tab switcher</span></span>

<span data-ttu-id="36748-158">Quando questa impostazione è impostata su `true` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda.</span><span class="sxs-lookup"><span data-stu-id="36748-158">When this is set to `true`, the `nextTab` and `prevTab` commands will use the tab switcher UI.</span></span> <span data-ttu-id="36748-159">L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.</span><span class="sxs-lookup"><span data-stu-id="36748-159">The UI will show all the currently open tabs in a vertical list, navigable with the keyboard or mouse.</span></span>

<span data-ttu-id="36748-160">Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto.</span><span class="sxs-lookup"><span data-stu-id="36748-160">The tab switcher will open on the initial press of the actions for `nextTab` and `prevTab`, and will stay open as long as a modifier key is held down.</span></span> <span data-ttu-id="36748-161">Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="36748-161">When all modifier keys are released, the switcher will close and the highlighted tab will be focused.</span></span> <span data-ttu-id="36748-162"><kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.</span><span class="sxs-lookup"><span data-stu-id="36748-162"><kbd>tab</kbd>/<kbd>shift+tab</kbd>, the <kbd>up</kbd> and <kbd>down</kbd> arrow keys, and the `nextTab`/`prevTab` actions can be used to cycle through the switcher UI.</span></span>

<span data-ttu-id="36748-163">**Nome della proprietà:** `useTabSwitcher`</span><span class="sxs-lookup"><span data-stu-id="36748-163">**Property name:** `useTabSwitcher`</span></span>

<span data-ttu-id="36748-164">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-164">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-165">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="36748-165">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="36748-166">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="36748-166">**Default value:** `true`</span></span>

> [!CAUTION]
> <span data-ttu-id="36748-167">L' `"useTabSwitcher"` impostazione non è più disponibile nelle versioni 1,5 e successive.</span><span class="sxs-lookup"><span data-stu-id="36748-167">The `"useTabSwitcher"` setting is no longer available in versions 1.5 and later.</span></span> <span data-ttu-id="36748-168">Si consiglia di utilizzare `"tabSwitcherMode"` invece l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="36748-168">It is recommended that you use the `"tabSwitcherMode"` setting instead.</span></span>

<br />

___

## <a name="paste-warnings"></a><span data-ttu-id="36748-169">Avvisi incolla</span><span class="sxs-lookup"><span data-stu-id="36748-169">Paste warnings</span></span>

### <a name="warn-when-the-text-to-paste-is-very-large"></a><span data-ttu-id="36748-170">Avvisa quando il testo da incollare è molto grande</span><span class="sxs-lookup"><span data-stu-id="36748-170">Warn when the text to paste is very large</span></span>

<span data-ttu-id="36748-171">Quando è impostato su, quando si `true` tenta di incollare testo con più di 5 KiB di caratteri verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla.</span><span class="sxs-lookup"><span data-stu-id="36748-171">When this is set to `true`, trying to paste text with more than 5 KiB of characters will display a dialog asking you whether to continue or not with the paste.</span></span> <span data-ttu-id="36748-172">Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="36748-172">When it's set to `false`, the dialog is not shown and instead the text is pasted right away.</span></span> <span data-ttu-id="36748-173">Se spesso si fa clic con il pulsante destro del mouse sul terminale per errore dopo aver selezionato una grande quantità di testo, potrebbe essere utile evitare che il terminale non risponda mentre il programma connesso al terminale riceve il contenuto degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="36748-173">If you often right-click on the terminal by accident after having selected a lot of text, this might be useful to prevent the terminal from becoming unresponsive while the program connected to the terminal receives the clipboard's content.</span></span>

<span data-ttu-id="36748-174">**Nome della proprietà:** `largePasteWarning`</span><span class="sxs-lookup"><span data-stu-id="36748-174">**Property name:** `largePasteWarning`</span></span>

<span data-ttu-id="36748-175">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-175">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-176">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="36748-176">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="36748-177">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="36748-177">**Default value:** `true`</span></span>

### <a name="warn-when-the-text-to-paste-contains-multiple-lines"></a><span data-ttu-id="36748-178">Avvisa quando il testo da incollare contiene più righe</span><span class="sxs-lookup"><span data-stu-id="36748-178">Warn when the text to paste contains multiple lines</span></span>

<span data-ttu-id="36748-179">Quando è impostato su, quando si `true` tenta di incollare testo con più righe verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla.</span><span class="sxs-lookup"><span data-stu-id="36748-179">When this is set to `true`, trying to paste text with multiple lines will display a dialog asking you whether to continue or not with the paste.</span></span> <span data-ttu-id="36748-180">Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="36748-180">When it's set to `false`, the dialog is not shown and instead the text is pasted right away.</span></span> <span data-ttu-id="36748-181">Nella maggior parte delle shell, una riga corrisponde a un comando, quindi se si incolla il testo che contiene il carattere "nuova riga" in una shell, è possibile che uno o più comandi vengano eseguiti automaticamente al termine della copia, senza che sia necessario convalidare i comandi.</span><span class="sxs-lookup"><span data-stu-id="36748-181">In most shells, one line corresponds to one command so if you paste text that contains the "new line" character into a shell, one or more command(s) might be executed automatically upon paste, without you having time to validate the commands.</span></span> <span data-ttu-id="36748-182">Questa operazione può essere utile se si copiano e si incollano spesso comandi da siti Web non attendibili.</span><span class="sxs-lookup"><span data-stu-id="36748-182">This can be useful if you often copy and paste commands from untrusted websites.</span></span>

<span data-ttu-id="36748-183">**Nome della proprietà:** `multiLinePasteWarning`</span><span class="sxs-lookup"><span data-stu-id="36748-183">**Property name:** `multiLinePasteWarning`</span></span>

<span data-ttu-id="36748-184">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="36748-184">**Necessity:** Optional</span></span>

<span data-ttu-id="36748-185">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="36748-185">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="36748-186">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="36748-186">**Default value:** `true`</span></span>
