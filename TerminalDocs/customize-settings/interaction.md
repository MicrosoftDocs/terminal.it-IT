---
title: Impostazioni di interazione del terminale di Windows
description: Informazioni su come personalizzare le impostazioni di interazione nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: e16c093ad1a6b7efb058377840bf8d516ef0fb69
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041974"
---
# <a name="interaction-settings-in-windows-terminal"></a><span data-ttu-id="99813-103">Impostazioni di interazione nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="99813-103">Interaction settings in Windows Terminal</span></span>

<span data-ttu-id="99813-104">Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo.</span><span class="sxs-lookup"><span data-stu-id="99813-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="99813-105">Queste proprietà devono essere inserite nella radice del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="99813-105">These should be placed at the root of your settings.json file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99813-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="99813-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="99813-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="99813-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="automatically-copy-selection-to-clipboard"></a><span data-ttu-id="99813-108">Copia automaticamente selezione negli Appunti</span><span class="sxs-lookup"><span data-stu-id="99813-108">Automatically copy selection to clipboard</span></span>

<span data-ttu-id="99813-109">Quando è impostata su `true`, una selezione viene immediatamente copiata negli Appunti al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="99813-109">When this is set to `true`, a selection is immediately copied to your clipboard upon creation.</span></span> <span data-ttu-id="99813-110">In questo caso facendo clic con il pulsante destro del mouse, la selezione verrà sempre incollata.</span><span class="sxs-lookup"><span data-stu-id="99813-110">The right-click on your mouse will always paste in this case.</span></span> <span data-ttu-id="99813-111">Quando è impostata su `false`, la selezione viene mantenuta in attesa di altre azioni.</span><span class="sxs-lookup"><span data-stu-id="99813-111">When it's set to `false`, the selection persists and awaits further action.</span></span> <span data-ttu-id="99813-112">Facendo clic con il pulsante destro del mouse, la selezione verrà copiata.</span><span class="sxs-lookup"><span data-stu-id="99813-112">Using your mouse to right-click will copy the selection.</span></span>

<span data-ttu-id="99813-113">**Nome della proprietà:** `copyOnSelect`</span><span class="sxs-lookup"><span data-stu-id="99813-113">**Property name:** `copyOnSelect`</span></span>

<span data-ttu-id="99813-114">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-114">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-115">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="99813-115">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="99813-116">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="99813-116">**Default value:** `false`</span></span>

<br />

___

## <a name="text-format-when-copying"></a><span data-ttu-id="99813-117">Formato testo durante la copia</span><span class="sxs-lookup"><span data-stu-id="99813-117">Text format when copying</span></span>

<span data-ttu-id="99813-118">Quando è impostato su `true` , la formattazione del colore e del carattere del testo selezionato viene anche copiata negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="99813-118">When this is set to `true`, the color and font formatting of the selected text is also copied to your clipboard.</span></span> <span data-ttu-id="99813-119">Quando è impostato su `false`, negli Appunti viene copiato solo il testo normale.</span><span class="sxs-lookup"><span data-stu-id="99813-119">When it's set to `false`, only plain text is copied to your clipboard.</span></span> <span data-ttu-id="99813-120">È inoltre possibile specificare i formati che si desidera copiare.</span><span class="sxs-lookup"><span data-stu-id="99813-120">You can also specify which formats you would like to copy.</span></span>

<span data-ttu-id="99813-121">**Nome della proprietà:** `copyFormatting`</span><span class="sxs-lookup"><span data-stu-id="99813-121">**Property name:** `copyFormatting`</span></span>

<span data-ttu-id="99813-122">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-122">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-123">**Accetta:** `true` , `false` , `"all"` , `"none"` , `"html"` , `"rtf"`</span><span class="sxs-lookup"><span data-stu-id="99813-123">**Accepts:** `true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"`</span></span>

<span data-ttu-id="99813-124">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="99813-124">**Default value:** `false`</span></span>

<br />

___

## <a name="word-delimiters"></a><span data-ttu-id="99813-125">Delimitatori di parola</span><span class="sxs-lookup"><span data-stu-id="99813-125">Word delimiters</span></span>

<span data-ttu-id="99813-126">Determina i delimitatori di parola usati quando si fa doppio clic per selezionare.</span><span class="sxs-lookup"><span data-stu-id="99813-126">This determines the word delimiters used in a double-click selection.</span></span> <span data-ttu-id="99813-127">I delimitatori di parola sono caratteri che specificano la posizione del limite tra due parole.</span><span class="sxs-lookup"><span data-stu-id="99813-127">Word delimiters are characters that specify where the boundary is between two words.</span></span> <span data-ttu-id="99813-128">Gli esempi più comuni sono spazi, punti e virgola, virgole e punti.</span><span class="sxs-lookup"><span data-stu-id="99813-128">The most common examples are spaces, semicolons, commas, and periods.</span></span>

<span data-ttu-id="99813-129">**Nome della proprietà:** `wordDelimiters`</span><span class="sxs-lookup"><span data-stu-id="99813-129">**Property name:** `wordDelimiters`</span></span>

<span data-ttu-id="99813-130">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-130">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-131">**Accetta:** caratteri in formato stringa</span><span class="sxs-lookup"><span data-stu-id="99813-131">**Accepts:** Characters as a string</span></span>

<span data-ttu-id="99813-132">**Valore predefinito:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span><span class="sxs-lookup"><span data-stu-id="99813-132">**Default value:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span></span><br><span data-ttu-id="99813-133">_(`│` è `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span><span class="sxs-lookup"><span data-stu-id="99813-133">_(`│` is `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span></span>

<br />

___

## <a name="snap-window-resizing-to-character-grid"></a><span data-ttu-id="99813-134">Blocca la finestra di ridimensionamento in griglia caratteri</span><span class="sxs-lookup"><span data-stu-id="99813-134">Snap window resizing to character grid</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="99813-135">Quando è impostata su `true`, la finestra verrà allineata al limite del carattere più vicino quando viene ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="99813-135">When this is set to `true`, the window will snap to the nearest character boundary on resize.</span></span> <span data-ttu-id="99813-136">Quando è impostata su `false`, la finestra verrà ridimensionata senza vincoli.</span><span class="sxs-lookup"><span data-stu-id="99813-136">When it's set to `false`, the window will resize "smoothly".</span></span>

<span data-ttu-id="99813-137">**Nome della proprietà:** `snapToGridOnResize`</span><span class="sxs-lookup"><span data-stu-id="99813-137">**Property name:** `snapToGridOnResize`</span></span>

<span data-ttu-id="99813-138">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-138">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-139">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="99813-139">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="99813-140">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="99813-140">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Blocca sulla griglia al ridimensionamento](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a><span data-ttu-id="99813-142">Impostazioni per le schede</span><span class="sxs-lookup"><span data-stu-id="99813-142">Tab settings</span></span>

### <a name="tab-switcher-interface-style"></a><span data-ttu-id="99813-143">Stile dell'interfaccia Switcher di tabulazione</span><span class="sxs-lookup"><span data-stu-id="99813-143">Tab switcher interface style</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="99813-144">Quando è impostato su `true` o `"mru"` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda, con l'ordine di utilizzo più recente.</span><span class="sxs-lookup"><span data-stu-id="99813-144">When this is set to `true` or `"mru"`, the `nextTab` and `prevTab` commands will use the tab switcher UI, with most recently used ordering.</span></span> <span data-ttu-id="99813-145">Quando è impostato su `"inOrder"` , queste azioni cambieranno le schede nell'ordine corrente sulla barra della scheda.</span><span class="sxs-lookup"><span data-stu-id="99813-145">When set to `"inOrder"`, these actions will switch tabs in their current order in the tab bar.</span></span> <span data-ttu-id="99813-146">L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.</span><span class="sxs-lookup"><span data-stu-id="99813-146">The UI will show all the currently open tabs in a vertical list, navigable with the keyboard or mouse.</span></span>

<span data-ttu-id="99813-147">Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto.</span><span class="sxs-lookup"><span data-stu-id="99813-147">The tab switcher will open on the initial press of the actions for `nextTab` and `prevTab`, and will stay open as long as a modifier key is held down.</span></span> <span data-ttu-id="99813-148">Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="99813-148">When all modifier keys are released, the switcher will close and the highlighted tab will be focused.</span></span> <span data-ttu-id="99813-149"><kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.</span><span class="sxs-lookup"><span data-stu-id="99813-149"><kbd>tab</kbd>/<kbd>shift+tab</kbd>, the <kbd>up</kbd> and <kbd>down</kbd> arrow keys, and the `nextTab`/`prevTab` actions can be used to cycle through the switcher UI.</span></span>

<span data-ttu-id="99813-150">Per disabilitare lo switcher di tabulazione, è possibile impostare questa impostazione su `false` o su `"disabled"` .</span><span class="sxs-lookup"><span data-stu-id="99813-150">To disable the tab switcher, you can set this to `false` or `"disabled"`.</span></span>

<span data-ttu-id="99813-151">**Nome della proprietà:** `tabSwitcherMode`</span><span class="sxs-lookup"><span data-stu-id="99813-151">**Property name:** `tabSwitcherMode`</span></span>

<span data-ttu-id="99813-152">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-152">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-153">**Accetta:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`</span><span class="sxs-lookup"><span data-stu-id="99813-153">**Accepts:** `true`, `false`, `"mru"`, `"inOrder"`, `"disabled"`</span></span>

<span data-ttu-id="99813-154">**Valore predefinito:** `"inOrder"`</span><span class="sxs-lookup"><span data-stu-id="99813-154">**Default value:** `"inOrder"`</span></span>

:::column-end:::
:::column span="":::
![Switcher Scheda terminale Windows](./../images/tab-switcher.gif)

:::column-end:::
:::row-end:::

### <a name="enable-tab-switcher"></a><span data-ttu-id="99813-156">Abilita Switcher schede</span><span class="sxs-lookup"><span data-stu-id="99813-156">Enable tab switcher</span></span>

<span data-ttu-id="99813-157">Quando questa impostazione è impostata su `true` , i `nextTab` comandi e utilizzeranno `prevTab` l'interfaccia utente di selezione scheda.</span><span class="sxs-lookup"><span data-stu-id="99813-157">When this is set to `true`, the `nextTab` and `prevTab` commands will use the tab switcher UI.</span></span> <span data-ttu-id="99813-158">L'interfaccia utente mostrerà tutte le schede attualmente aperte in un elenco verticale, navigable con la tastiera o il mouse.</span><span class="sxs-lookup"><span data-stu-id="99813-158">The UI will show all the currently open tabs in a vertical list, navigable with the keyboard or mouse.</span></span>

<span data-ttu-id="99813-159">Il selettore di schede verrà aperto sulla pressione iniziale delle azioni per `nextTab` e `prevTab` e resterà aperto finché il tasto di modifica verrà mantenuto premuto.</span><span class="sxs-lookup"><span data-stu-id="99813-159">The tab switcher will open on the initial press of the actions for `nextTab` and `prevTab`, and will stay open as long as a modifier key is held down.</span></span> <span data-ttu-id="99813-160">Quando vengono rilasciati tutti i tasti di modifica, lo switcher si chiude e la scheda evidenziata verrà messa a fuoco.</span><span class="sxs-lookup"><span data-stu-id="99813-160">When all modifier keys are released, the switcher will close and the highlighted tab will be focused.</span></span> <span data-ttu-id="99813-161"><kbd>scheda</kbd> / <kbd>MAIUSC + TAB</kbd>, i tasti freccia <kbd>su</kbd> e <kbd>giù</kbd> e le `nextTab` / `prevTab` azioni possono essere usate per scorrere l'interfaccia utente di selezione.</span><span class="sxs-lookup"><span data-stu-id="99813-161"><kbd>tab</kbd>/<kbd>shift+tab</kbd>, the <kbd>up</kbd> and <kbd>down</kbd> arrow keys, and the `nextTab`/`prevTab` actions can be used to cycle through the switcher UI.</span></span>

<span data-ttu-id="99813-162">**Nome della proprietà:** `useTabSwitcher`</span><span class="sxs-lookup"><span data-stu-id="99813-162">**Property name:** `useTabSwitcher`</span></span>

<span data-ttu-id="99813-163">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-163">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-164">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="99813-164">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="99813-165">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="99813-165">**Default value:** `true`</span></span>

> [!CAUTION]
> <span data-ttu-id="99813-166">L' `"useTabSwitcher"` impostazione non è più disponibile nelle versioni 1,5 e successive.</span><span class="sxs-lookup"><span data-stu-id="99813-166">The `"useTabSwitcher"` setting is no longer available in versions 1.5 and later.</span></span> <span data-ttu-id="99813-167">Si consiglia di utilizzare `"tabSwitcherMode"` invece l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="99813-167">It is recommended that you use the `"tabSwitcherMode"` setting instead.</span></span>

<br />

___

## <a name="paste-warnings"></a><span data-ttu-id="99813-168">Avvisi incolla</span><span class="sxs-lookup"><span data-stu-id="99813-168">Paste warnings</span></span>

### <a name="warn-when-the-text-to-paste-is-very-large"></a><span data-ttu-id="99813-169">Avvisa quando il testo da incollare è molto grande</span><span class="sxs-lookup"><span data-stu-id="99813-169">Warn when the text to paste is very large</span></span>

<span data-ttu-id="99813-170">Quando è impostato su, quando si `true` tenta di incollare testo con più di 5 KiB di caratteri verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla.</span><span class="sxs-lookup"><span data-stu-id="99813-170">When this is set to `true`, trying to paste text with more than 5 KiB of characters will display a dialog asking you whether to continue or not with the paste.</span></span> <span data-ttu-id="99813-171">Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="99813-171">When it's set to `false`, the dialog is not shown and instead the text is pasted right away.</span></span> <span data-ttu-id="99813-172">Se spesso si fa clic con il pulsante destro del mouse sul terminale per errore dopo aver selezionato una grande quantità di testo, potrebbe essere utile evitare che il terminale non risponda mentre il programma connesso al terminale riceve il contenuto degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="99813-172">If you often right-click on the terminal by accident after having selected a lot of text, this might be useful to prevent the terminal from becoming unresponsive while the program connected to the terminal receives the clipboard's content.</span></span>

<span data-ttu-id="99813-173">**Nome della proprietà:** `largePasteWarning`</span><span class="sxs-lookup"><span data-stu-id="99813-173">**Property name:** `largePasteWarning`</span></span>

<span data-ttu-id="99813-174">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-174">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-175">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="99813-175">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="99813-176">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="99813-176">**Default value:** `true`</span></span>

### <a name="warn-when-the-text-to-paste-contains-multiple-lines"></a><span data-ttu-id="99813-177">Avvisa quando il testo da incollare contiene più righe</span><span class="sxs-lookup"><span data-stu-id="99813-177">Warn when the text to paste contains multiple lines</span></span>

<span data-ttu-id="99813-178">Quando è impostato su, quando si `true` tenta di incollare testo con più righe verrà visualizzata una finestra di dialogo in cui viene chiesto se continuare o meno con l'operazione Incolla.</span><span class="sxs-lookup"><span data-stu-id="99813-178">When this is set to `true`, trying to paste text with multiple lines will display a dialog asking you whether to continue or not with the paste.</span></span> <span data-ttu-id="99813-179">Quando è impostato su `false` , la finestra di dialogo non viene visualizzata e invece il testo viene incollato immediatamente.</span><span class="sxs-lookup"><span data-stu-id="99813-179">When it's set to `false`, the dialog is not shown and instead the text is pasted right away.</span></span> <span data-ttu-id="99813-180">Nella maggior parte delle shell, una riga corrisponde a un comando, quindi se si incolla il testo che contiene il carattere "nuova riga" in una shell, è possibile che uno o più comandi vengano eseguiti automaticamente al termine della copia, senza che sia necessario convalidare i comandi.</span><span class="sxs-lookup"><span data-stu-id="99813-180">In most shells, one line corresponds to one command so if you paste text that contains the "new line" character into a shell, one or more command(s) might be executed automatically upon paste, without you having time to validate the commands.</span></span> <span data-ttu-id="99813-181">Questa operazione può essere utile se si copiano e si incollano spesso comandi da siti Web non attendibili.</span><span class="sxs-lookup"><span data-stu-id="99813-181">This can be useful if you often copy and paste commands from untrusted websites.</span></span>

<span data-ttu-id="99813-182">**Nome della proprietà:** `multiLinePasteWarning`</span><span class="sxs-lookup"><span data-stu-id="99813-182">**Property name:** `multiLinePasteWarning`</span></span>

<span data-ttu-id="99813-183">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="99813-183">**Necessity:** Optional</span></span>

<span data-ttu-id="99813-184">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="99813-184">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="99813-185">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="99813-185">**Default value:** `true`</span></span>
