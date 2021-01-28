---
title: Azioni del terminale di Windows
description: Informazioni su come creare azioni personalizzate per il terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 1/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 050e6fc2bc9d541e49f3a36cc8b2180a4e374825
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "98980974"
---
# <a name="custom-actions-in-windows-terminal"></a><span data-ttu-id="21557-103">Azioni personalizzate nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="21557-103">Custom actions in Windows Terminal</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21557-104">A partire dalla versione 1,4 del terminale di Windows, la `keybindings` matrice è stata rinominata all' `actions` interno del settings.jssu file.</span><span class="sxs-lookup"><span data-stu-id="21557-104">As of Windows Terminal version 1.4, the `keybindings` array has been renamed to `actions` inside the settings.json file.</span></span> <span data-ttu-id="21557-105">Il supporto per la `keybindings` matrice esiste ancora per la compatibilità con le versioni precedenti, ma il terminale non verrà rinominato automaticamente all' `keybindings` interno del `actions` settings.jssu file.</span><span class="sxs-lookup"><span data-stu-id="21557-105">Support for the `keybindings` array still exists for backward compatibility, however the terminal will not automatically rename `keybindings` to `actions` inside your settings.json file.</span></span>

<span data-ttu-id="21557-106">È possibile creare azioni personalizzate all'interno del terminale di Windows che consentono di controllare la modalità di interazione con il terminale.</span><span class="sxs-lookup"><span data-stu-id="21557-106">You can create custom actions inside Windows Terminal that give you control of how you interact with the terminal.</span></span> <span data-ttu-id="21557-107">Queste azioni verranno aggiunte automaticamente al riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="21557-107">These actions will automatically be added to the command palette.</span></span>

## <a name="action-formats"></a><span data-ttu-id="21557-108">Formati di azione</span><span class="sxs-lookup"><span data-stu-id="21557-108">Action formats</span></span>

<span data-ttu-id="21557-109">Le azioni possono essere strutturate nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="21557-109">Actions can be structured in the following formats:</span></span>

### <a name="commands-without-arguments"></a><span data-ttu-id="21557-110">Comandi senza argomenti</span><span class="sxs-lookup"><span data-stu-id="21557-110">Commands without arguments</span></span>

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

<span data-ttu-id="21557-111">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>alt+f4</kbd> per chiudere la finestra del terminale:</span><span class="sxs-lookup"><span data-stu-id="21557-111">For example, this default setting uses the shortcut key <kbd>alt+f4</kbd> to close the terminal window:</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a><span data-ttu-id="21557-112">Comandi con argomenti</span><span class="sxs-lookup"><span data-stu-id="21557-112">Commands with arguments</span></span>

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

<span data-ttu-id="21557-113">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>ctrl+maiusc+1</kbd> per aprire una nuova scheda nel terminale in base al profilo elencato per primo nel menu a discesa (in genere verrà aperto il profilo PowerShell):</span><span class="sxs-lookup"><span data-stu-id="21557-113">For example, this default setting uses the shortcut key <kbd>ctrl+shift+1</kbd> to open a new tab in the terminal based on whichever profile is listed first in your dropdown menu (typically this will open the PowerShell profile):</span></span>

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="action-properties"></a><span data-ttu-id="21557-114">Proprietà delle azioni</span><span class="sxs-lookup"><span data-stu-id="21557-114">Action properties</span></span>

<span data-ttu-id="21557-115">Le azioni possono essere costruite usando le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="21557-115">Actions can be constructed using the following properties.</span></span>

### <a name="command"></a><span data-ttu-id="21557-116">Comando</span><span class="sxs-lookup"><span data-stu-id="21557-116">Command</span></span>

<span data-ttu-id="21557-117">Comando eseguito quando vengono premuti i tasti associati.</span><span class="sxs-lookup"><span data-stu-id="21557-117">This is the command executed when the associated keys are pressed.</span></span>

<span data-ttu-id="21557-118">**Nome della proprietà:** `command`</span><span class="sxs-lookup"><span data-stu-id="21557-118">**Property name:** `command`</span></span>

<span data-ttu-id="21557-119">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-119">**Necessity:** Required</span></span>

<span data-ttu-id="21557-120">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="21557-120">**Accepts:** String</span></span>

### <a name="keys"></a><span data-ttu-id="21557-121">Tasti</span><span class="sxs-lookup"><span data-stu-id="21557-121">Keys</span></span>

<span data-ttu-id="21557-122">Definisce le combinazioni di tasti usate per chiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="21557-122">This defines the key combinations used to call the command.</span></span> <span data-ttu-id="21557-123">Con la proprietà keys è possibile associare più modificatori a un unico tasto.</span><span class="sxs-lookup"><span data-stu-id="21557-123">Keys can have any number of modifiers with one key.</span></span> <span data-ttu-id="21557-124">I tasti e i modificatori accettati sono elencati [di seguito](#accepted-modifiers-and-keys).</span><span class="sxs-lookup"><span data-stu-id="21557-124">Accepted modifiers and keys are listed [below](#accepted-modifiers-and-keys).</span></span>

<span data-ttu-id="21557-125">Se l'azione non dispone di chiavi, verrà visualizzata nel riquadro comandi, ma non potrà essere richiamata con la tastiera.</span><span class="sxs-lookup"><span data-stu-id="21557-125">If the action does not have keys, it will appear in the command palette but cannot be invoked with the keyboard.</span></span>

<span data-ttu-id="21557-126">**Nome della proprietà:** `keys`</span><span class="sxs-lookup"><span data-stu-id="21557-126">**Property name:** `keys`</span></span>

<span data-ttu-id="21557-127">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-127">**Necessity:** Optional</span></span>

<span data-ttu-id="21557-128">**Accetta:** stringa o matrice[stringa]</span><span class="sxs-lookup"><span data-stu-id="21557-128">**Accepts:** String or array[string]</span></span>

### <a name="action"></a><span data-ttu-id="21557-129">Azione</span><span class="sxs-lookup"><span data-stu-id="21557-129">Action</span></span>

<span data-ttu-id="21557-130">Aggiunge funzionalità aggiuntive a determinati comandi.</span><span class="sxs-lookup"><span data-stu-id="21557-130">This adds additional functionality to certain commands.</span></span>

<span data-ttu-id="21557-131">**Nome della proprietà:** `action`</span><span class="sxs-lookup"><span data-stu-id="21557-131">**Property name:** `action`</span></span>

<span data-ttu-id="21557-132">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-132">**Necessity:** Optional</span></span>

<span data-ttu-id="21557-133">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="21557-133">**Accepts:** String</span></span>

### <a name="name"></a><span data-ttu-id="21557-134">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-134">Name</span></span>

<span data-ttu-id="21557-135">Questo consente di impostare il nome che verrà visualizzato nel riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="21557-135">This sets the name that will appear in the command palette.</span></span> <span data-ttu-id="21557-136">Se non ne viene specificato uno, il terminale tenterà di generare automaticamente un nome.</span><span class="sxs-lookup"><span data-stu-id="21557-136">If one isn't provided, the terminal will attempt to automatically generate a name.</span></span>

<span data-ttu-id="21557-137">**Nome della proprietà:** `name`</span><span class="sxs-lookup"><span data-stu-id="21557-137">**Property name:** `name`</span></span>

<span data-ttu-id="21557-138">**Necessità**: facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-138">**Necessity**: Optional</span></span>

<span data-ttu-id="21557-139">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="21557-139">**Accepts:** String</span></span>

### <a name="icon"></a><span data-ttu-id="21557-140">Icona</span><span class="sxs-lookup"><span data-stu-id="21557-140">Icon</span></span>

<span data-ttu-id="21557-141">Questa operazione consente di impostare l'icona visualizzata all'interno del riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="21557-141">This sets the icon that displays within the command palette.</span></span>

<span data-ttu-id="21557-142">**Nome della proprietà:** `icon`</span><span class="sxs-lookup"><span data-stu-id="21557-142">**Property name:** `icon`</span></span>

<span data-ttu-id="21557-143">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-143">**Necessity:** Optional</span></span>

<span data-ttu-id="21557-144">**Accetta:** Percorso del file sotto forma di stringa o emoji</span><span class="sxs-lookup"><span data-stu-id="21557-144">**Accepts:** File location as a string, or an emoji</span></span>

<br />

___

## <a name="accepted-modifiers-and-keys"></a><span data-ttu-id="21557-145">Tasti e modificatori accettati</span><span class="sxs-lookup"><span data-stu-id="21557-145">Accepted modifiers and keys</span></span>

### <a name="modifiers"></a><span data-ttu-id="21557-146">Modificatori</span><span class="sxs-lookup"><span data-stu-id="21557-146">Modifiers</span></span>

<span data-ttu-id="21557-147">`ctrl+`, `shift+`, `alt+`</span><span class="sxs-lookup"><span data-stu-id="21557-147">`ctrl+`, `shift+`, `alt+`</span></span>

> [!NOTE]
> <span data-ttu-id="21557-148">La `Windows` chiave non è supportata come modificatore.</span><span class="sxs-lookup"><span data-stu-id="21557-148">The `Windows` key is not supported as a modifier.</span></span>

### <a name="modifier-keys"></a><span data-ttu-id="21557-149">Tasti di modifica</span><span class="sxs-lookup"><span data-stu-id="21557-149">Modifier keys</span></span>

| <span data-ttu-id="21557-150">Type</span><span class="sxs-lookup"><span data-stu-id="21557-150">Type</span></span> | <span data-ttu-id="21557-151">Tasti</span><span class="sxs-lookup"><span data-stu-id="21557-151">Keys</span></span> |
| ---- | ---- |
| <span data-ttu-id="21557-152">Tasti funzione e alfanumerici</span><span class="sxs-lookup"><span data-stu-id="21557-152">Function and alphanumeric keys</span></span> | <span data-ttu-id="21557-153">`f1-f24`, `a-z`, `0-9`</span><span class="sxs-lookup"><span data-stu-id="21557-153">`f1-f24`, `a-z`, `0-9`</span></span> |
| <span data-ttu-id="21557-154">Simboli</span><span class="sxs-lookup"><span data-stu-id="21557-154">Symbols</span></span> | <span data-ttu-id="21557-155">``` ` ```, `plus`, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span><span class="sxs-lookup"><span data-stu-id="21557-155">``` ` ```, `plus`, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span></span> |
| <span data-ttu-id="21557-156">Tasti di direzione</span><span class="sxs-lookup"><span data-stu-id="21557-156">Arrow keys</span></span> | <span data-ttu-id="21557-157">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`</span><span class="sxs-lookup"><span data-stu-id="21557-157">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`</span></span> |
| <span data-ttu-id="21557-158">Tasti di azione</span><span class="sxs-lookup"><span data-stu-id="21557-158">Action keys</span></span> | <span data-ttu-id="21557-159">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`, `app`, `menu`</span><span class="sxs-lookup"><span data-stu-id="21557-159">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`, `app`, `menu`</span></span>  |
| <span data-ttu-id="21557-160">Tasti del tastierino numerico</span><span class="sxs-lookup"><span data-stu-id="21557-160">Numpad keys</span></span> | <span data-ttu-id="21557-161">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span><span class="sxs-lookup"><span data-stu-id="21557-161">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span></span> |

<span data-ttu-id="21557-162">**Nota:** `=` e `plus` sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="21557-162">**Note:** `=` and `plus` are equivalents.</span></span> <span data-ttu-id="21557-163">Il secondo non deve essere confuso con `numpad_plus` .</span><span class="sxs-lookup"><span data-stu-id="21557-163">The latter must not be confused with `numpad_plus`.</span></span>

___

## <a name="application-level-commands"></a><span data-ttu-id="21557-164">Comandi a livello di applicazione</span><span class="sxs-lookup"><span data-stu-id="21557-164">Application-level commands</span></span>

### <a name="close-window"></a><span data-ttu-id="21557-165">Chiudi finestra</span><span class="sxs-lookup"><span data-stu-id="21557-165">Close window</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="21557-166">Chiude la finestra corrente e tutte le relative schede.</span><span class="sxs-lookup"><span data-stu-id="21557-166">This closes the current window and all tabs within it.</span></span> <span data-ttu-id="21557-167">Se `confirmCloseAllTabs` è impostato su `true`, verrà visualizzata una finestra di dialogo per confermare la chiusura di tutte le schede.</span><span class="sxs-lookup"><span data-stu-id="21557-167">If `confirmCloseAllTabs` is set to `true`, a confirmation dialog will appear to ensure you'd like to close all your tabs.</span></span> <span data-ttu-id="21557-168">Ulteriori informazioni su questa impostazione sono disponibili nella [pagina aspetto](./appearance.md#show-close-all-tabs-popup).</span><span class="sxs-lookup"><span data-stu-id="21557-168">More information on this setting can be found on the [Appearance page](./appearance.md#show-close-all-tabs-popup).</span></span>

<span data-ttu-id="21557-169">**Nome del comando:** `closeWindow`</span><span class="sxs-lookup"><span data-stu-id="21557-169">**Command name:** `closeWindow`</span></span>

<span data-ttu-id="21557-170">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-170">**Default binding:**</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a><span data-ttu-id="21557-172">Trova</span><span class="sxs-lookup"><span data-stu-id="21557-172">Find</span></span>

<span data-ttu-id="21557-173">Apre la finestra di dialogo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="21557-173">This opens the search dialog box.</span></span> <span data-ttu-id="21557-174">Per altre informazioni sulla ricerca, vedi la [pagina relativa alla ricerca](./../search.md).</span><span class="sxs-lookup"><span data-stu-id="21557-174">More information on search can be found on the [Search page](./../search.md).</span></span>

<span data-ttu-id="21557-175">**Nome del comando:** `find`</span><span class="sxs-lookup"><span data-stu-id="21557-175">**Command name:** `find`</span></span>

<span data-ttu-id="21557-176">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-176">**Default binding:**</span></span>

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a><span data-ttu-id="21557-177">Apri menu a discesa</span><span class="sxs-lookup"><span data-stu-id="21557-177">Open the dropdown</span></span>

<span data-ttu-id="21557-178">Apre il menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="21557-178">This opens the dropdown menu.</span></span>

<span data-ttu-id="21557-179">**Nome del comando:** `openNewTabDropdown`</span><span class="sxs-lookup"><span data-stu-id="21557-179">**Command name:** `openNewTabDropdown`</span></span>

<span data-ttu-id="21557-180">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-180">**Default binding:**</span></span>

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-files"></a><span data-ttu-id="21557-181">Apri file di impostazioni</span><span class="sxs-lookup"><span data-stu-id="21557-181">Open settings files</span></span>

<span data-ttu-id="21557-182">Apre i file di impostazioni predefiniti o personalizzati.</span><span class="sxs-lookup"><span data-stu-id="21557-182">This opens either the default or custom settings files.</span></span> <span data-ttu-id="21557-183">Senza il campo `target` verrà aperto il file settings.json.</span><span class="sxs-lookup"><span data-stu-id="21557-183">Without the `target` field, this will open the settings.json file.</span></span>

<span data-ttu-id="21557-184">**Nome del comando:** `openSettings`</span><span class="sxs-lookup"><span data-stu-id="21557-184">**Command name:** `openSettings`</span></span>

<span data-ttu-id="21557-185">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-185">**Default binding:**</span></span>

```json
{ "command": "openSettings", "keys": "ctrl+," },
{ "command": { "action": "openSettings", "target": "defaultsFile" }, "keys": "ctrl+alt+," },
```

#### <a name="actions"></a><span data-ttu-id="21557-186">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-186">Actions</span></span>

| <span data-ttu-id="21557-187">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-187">Name</span></span> | <span data-ttu-id="21557-188">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-188">Necessity</span></span> | <span data-ttu-id="21557-189">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-189">Accepts</span></span> | <span data-ttu-id="21557-190">Description</span><span class="sxs-lookup"><span data-stu-id="21557-190">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `target` | <span data-ttu-id="21557-191">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-191">Optional</span></span> | <span data-ttu-id="21557-192">`"settingsFile"`, `"defaultsFile"`, `"settingsUI"`, `"allFiles"`</span><span class="sxs-lookup"><span data-stu-id="21557-192">`"settingsFile"`, `"defaultsFile"`, `"settingsUI"`, `"allFiles"`</span></span> | <span data-ttu-id="21557-193">Il file di impostazioni da aprire.</span><span class="sxs-lookup"><span data-stu-id="21557-193">The settings file to open.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="21557-194">Il `"settingsUI"` valore di `target` è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="21557-194">The `"settingsUI"` value for `target` is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="toggle-full-screen"></a><span data-ttu-id="21557-195">Attiva/Disattiva schermo intero</span><span class="sxs-lookup"><span data-stu-id="21557-195">Toggle full screen</span></span>

<span data-ttu-id="21557-196">Consente di passare dalla finestra a schermo intero a quella con dimensioni predefinite e viceversa.</span><span class="sxs-lookup"><span data-stu-id="21557-196">This allows you to switch between full screen and default window sizes.</span></span>

<span data-ttu-id="21557-197">**Nome del comando:** `toggleFullscreen`</span><span class="sxs-lookup"><span data-stu-id="21557-197">**Command name:** `toggleFullscreen`</span></span>

<span data-ttu-id="21557-198">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-198">**Default bindings:**</span></span>

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

### <a name="toggle-focus-mode"></a><span data-ttu-id="21557-199">Attiva/Nascondi modalità messa a fuoco</span><span class="sxs-lookup"><span data-stu-id="21557-199">Toggle focus mode</span></span>

<span data-ttu-id="21557-200">Questo consente di attivare la modalità messa a fuoco, che nasconde le schede e la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="21557-200">This allows you to enter "focus mode", which hides the tabs and title bar.</span></span>

<span data-ttu-id="21557-201">**Nome del comando:** `toggleFocusMode`</span><span class="sxs-lookup"><span data-stu-id="21557-201">**Command name:** `toggleFocusMode`</span></span>

<span data-ttu-id="21557-202">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-202">**Default bindings:**</span></span>

```json
{ "command": "toggleFocusMode" }
```

### <a name="toggle-always-on-top-mode"></a><span data-ttu-id="21557-203">Attiva/Nascondi sempre in modalità principale</span><span class="sxs-lookup"><span data-stu-id="21557-203">Toggle always on top mode</span></span>

<span data-ttu-id="21557-204">In questo modo è possibile impostare lo stato "always on top" della finestra.</span><span class="sxs-lookup"><span data-stu-id="21557-204">This allows you toggle the "always on top" state of the window.</span></span> <span data-ttu-id="21557-205">Quando si usa la modalità "always on top", la finestra verrà visualizzata nella parte superiore di tutte le altre finestre non in primo piano.</span><span class="sxs-lookup"><span data-stu-id="21557-205">When in "always on top" mode, the window will appear on top of all other non-topmost windows.</span></span>

<span data-ttu-id="21557-206">**Nome del comando:** `toggleAlwaysOnTop`</span><span class="sxs-lookup"><span data-stu-id="21557-206">**Command name:** `toggleAlwaysOnTop`</span></span>

<span data-ttu-id="21557-207">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-207">**Default bindings:**</span></span>

```json
{ "command": "toggleAlwaysOnTop" }
```

### <a name="send-input"></a><span data-ttu-id="21557-208">Invia input</span><span class="sxs-lookup"><span data-stu-id="21557-208">Send input</span></span>

<span data-ttu-id="21557-209">Inviare input di testo arbitrario alla Shell.</span><span class="sxs-lookup"><span data-stu-id="21557-209">Send arbitrary text input to the shell.</span></span>
<span data-ttu-id="21557-210">Ad esempio, l'input `"text\n"` scriverà "testo" seguito da una nuova riga nella shell.</span><span class="sxs-lookup"><span data-stu-id="21557-210">As an example the input `"text\n"` will write "text" followed by a newline to the shell.</span></span>

<span data-ttu-id="21557-211">È possibile usare le sequenze di escape ANSI, ma i codici `\x1b` di escape come devono essere scritti come `\u001b` .</span><span class="sxs-lookup"><span data-stu-id="21557-211">ANSI escape sequences may be used, but escape codes like `\x1b` must be written as `\u001b`.</span></span>
<span data-ttu-id="21557-212">Ad esempio `"\u001b[A"` , si comporterà come se fosse stato premuto il pulsante freccia su.</span><span class="sxs-lookup"><span data-stu-id="21557-212">For instance `"\u001b[A"` will behave as if the up arrow button had been pressed.</span></span>

<span data-ttu-id="21557-213">**Nome del comando:** `sendInput`</span><span class="sxs-lookup"><span data-stu-id="21557-213">**Command name:** `sendInput`</span></span>

<span data-ttu-id="21557-214">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-214">**Default bindings:**</span></span>

<span data-ttu-id="21557-215">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="21557-215">_This command is not currently bound in the default settings_.</span></span>

```json
{ "command": { "action": "sendInput", "input": "\u001b[A" }, "keys": "" }
```

#### <a name="actions"></a><span data-ttu-id="21557-216">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-216">Actions</span></span>

| <span data-ttu-id="21557-217">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-217">Name</span></span> | <span data-ttu-id="21557-218">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-218">Necessity</span></span> | <span data-ttu-id="21557-219">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-219">Accepts</span></span> | <span data-ttu-id="21557-220">Description</span><span class="sxs-lookup"><span data-stu-id="21557-220">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `input` | <span data-ttu-id="21557-221">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-221">Required</span></span> | <span data-ttu-id="21557-222">string</span><span class="sxs-lookup"><span data-stu-id="21557-222">String</span></span> | <span data-ttu-id="21557-223">Input di testo da inserire nella shell.</span><span class="sxs-lookup"><span data-stu-id="21557-223">The text input to feed into the shell.</span></span> |

<br />

___

## <a name="tab-management-commands"></a><span data-ttu-id="21557-224">Comandi per la gestione delle schede</span><span class="sxs-lookup"><span data-stu-id="21557-224">Tab management commands</span></span>

### <a name="close-tab"></a><span data-ttu-id="21557-225">Chiudi scheda</span><span class="sxs-lookup"><span data-stu-id="21557-225">Close tab</span></span>

<span data-ttu-id="21557-226">Chiude la scheda corrente.</span><span class="sxs-lookup"><span data-stu-id="21557-226">This closes the current tab.</span></span>

<span data-ttu-id="21557-227">**Nome del comando:** `closeTab`</span><span class="sxs-lookup"><span data-stu-id="21557-227">**Command name:** `closeTab`</span></span>

### <a name="close-all-other-tabs"></a><span data-ttu-id="21557-228">Chiudi tutte le altre schede</span><span class="sxs-lookup"><span data-stu-id="21557-228">Close all other tabs</span></span>

<span data-ttu-id="21557-229">In questo modo vengono chiuse tutte le schede ad eccezione di quella in corrispondenza di un indice.</span><span class="sxs-lookup"><span data-stu-id="21557-229">This closes all tabs except for the one at an index.</span></span> <span data-ttu-id="21557-230">Se non viene specificato alcun indice, usare l'indice della scheda con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="21557-230">If no index is provided, use the focused tab's index.</span></span>

<span data-ttu-id="21557-231">**Nome del comando:** `closeOtherTabs`</span><span class="sxs-lookup"><span data-stu-id="21557-231">**Command name:** `closeOtherTabs`</span></span>

<span data-ttu-id="21557-232">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-232">**Default binding:**</span></span>

```json
{ "command": "closeOtherTabs" }
```

#### <a name="actions"></a><span data-ttu-id="21557-233">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-233">Actions</span></span>

| <span data-ttu-id="21557-234">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-234">Name</span></span> | <span data-ttu-id="21557-235">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-235">Necessity</span></span> | <span data-ttu-id="21557-236">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-236">Accepts</span></span> | <span data-ttu-id="21557-237">Description</span><span class="sxs-lookup"><span data-stu-id="21557-237">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="21557-238">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-238">Optional</span></span> | <span data-ttu-id="21557-239">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-239">Integer</span></span> | <span data-ttu-id="21557-240">Posizione della scheda da mantenere aperta.</span><span class="sxs-lookup"><span data-stu-id="21557-240">Position of the tab to be kept open.</span></span> |

### <a name="close-tabs-after-index"></a><span data-ttu-id="21557-241">Chiudi tabulazioni dopo l'indice</span><span class="sxs-lookup"><span data-stu-id="21557-241">Close tabs after index</span></span>

<span data-ttu-id="21557-242">Questa operazione chiude le schede che seguono la scheda in corrispondenza di un indice.</span><span class="sxs-lookup"><span data-stu-id="21557-242">This closes the tabs following the tab at an index.</span></span> <span data-ttu-id="21557-243">Se non viene specificato alcun indice, usare l'indice della scheda con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="21557-243">If no index is provided, use the focused tab's index.</span></span>

<span data-ttu-id="21557-244">**Nome del comando:** `closeTabsAfter`</span><span class="sxs-lookup"><span data-stu-id="21557-244">**Command name:** `closeTabsAfter`</span></span>

<span data-ttu-id="21557-245">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-245">**Default binding:**</span></span>

```json
{ "command": "closeTabsAfter" }
```

#### <a name="actions"></a><span data-ttu-id="21557-246">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-246">Actions</span></span>

| <span data-ttu-id="21557-247">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-247">Name</span></span> | <span data-ttu-id="21557-248">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-248">Necessity</span></span> | <span data-ttu-id="21557-249">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-249">Accepts</span></span> | <span data-ttu-id="21557-250">Description</span><span class="sxs-lookup"><span data-stu-id="21557-250">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="21557-251">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-251">Optional</span></span> | <span data-ttu-id="21557-252">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-252">Integer</span></span> | <span data-ttu-id="21557-253">Posizione dell'ultima scheda da mantenere aperta.</span><span class="sxs-lookup"><span data-stu-id="21557-253">Position of the last tab to be kept open.</span></span> |

### <a name="duplicate-tab"></a><span data-ttu-id="21557-254">Duplica scheda</span><span class="sxs-lookup"><span data-stu-id="21557-254">Duplicate tab</span></span>

<span data-ttu-id="21557-255">Crea una copia della scheda corrente e la apre.</span><span class="sxs-lookup"><span data-stu-id="21557-255">This makes a copy of the current tab and opens it.</span></span>

<span data-ttu-id="21557-256">**Nome del comando:** `duplicateTab`</span><span class="sxs-lookup"><span data-stu-id="21557-256">**Command name:** `duplicateTab`</span></span>

<span data-ttu-id="21557-257">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-257">**Default binding:**</span></span>

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a><span data-ttu-id="21557-258">Nuova scheda</span><span class="sxs-lookup"><span data-stu-id="21557-258">New tab</span></span>

<span data-ttu-id="21557-259">Crea una nuova scheda. Se viene specificato senza argomenti, il profilo predefinito verrà aperto in una nuova scheda. Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="21557-259">This creates a new tab. Without any arguments, this will open the default profile in a new tab. If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="21557-260">**Nome del comando:** `newTab`</span><span class="sxs-lookup"><span data-stu-id="21557-260">**Command name:** `newTab`</span></span>

<span data-ttu-id="21557-261">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-261">**Default bindings:**</span></span>

```json
{ "command": "newTab", "keys": "ctrl+shift+t" },
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" },
{ "command": { "action": "newTab", "index": 1 }, "keys": "ctrl+shift+2" },
{ "command": { "action": "newTab", "index": 2 }, "keys": "ctrl+shift+3" },
{ "command": { "action": "newTab", "index": 3 }, "keys": "ctrl+shift+4" },
{ "command": { "action": "newTab", "index": 4 }, "keys": "ctrl+shift+5" },
{ "command": { "action": "newTab", "index": 5 }, "keys": "ctrl+shift+6" },
{ "command": { "action": "newTab", "index": 6 }, "keys": "ctrl+shift+7" },
{ "command": { "action": "newTab", "index": 7 }, "keys": "ctrl+shift+8" },
{ "command": { "action": "newTab", "index": 8 }, "keys": "ctrl+shift+9" }
```

#### <a name="actions"></a><span data-ttu-id="21557-262">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-262">Actions</span></span>

| <span data-ttu-id="21557-263">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-263">Name</span></span> | <span data-ttu-id="21557-264">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-264">Necessity</span></span> | <span data-ttu-id="21557-265">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-265">Accepts</span></span> | <span data-ttu-id="21557-266">Description</span><span class="sxs-lookup"><span data-stu-id="21557-266">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `commandline` | <span data-ttu-id="21557-267">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-267">Optional</span></span> | <span data-ttu-id="21557-268">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="21557-268">Executable file name as a string</span></span> | <span data-ttu-id="21557-269">Esegue l'eseguibile all'interno della scheda.</span><span class="sxs-lookup"><span data-stu-id="21557-269">Executable run within the tab.</span></span> |
| `startingDirectory` | <span data-ttu-id="21557-270">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-270">Optional</span></span> | <span data-ttu-id="21557-271">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="21557-271">Folder location as a string</span></span> | <span data-ttu-id="21557-272">Directory in cui verrà aperta la scheda.</span><span class="sxs-lookup"><span data-stu-id="21557-272">Directory in which the tab will open.</span></span> |
| `tabTitle` | <span data-ttu-id="21557-273">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-273">Optional</span></span> | <span data-ttu-id="21557-274">String</span><span class="sxs-lookup"><span data-stu-id="21557-274">String</span></span> | <span data-ttu-id="21557-275">Titolo della nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="21557-275">Title of the new tab.</span></span> |
| `index` | <span data-ttu-id="21557-276">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-276">Optional</span></span> | <span data-ttu-id="21557-277">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-277">Integer</span></span> | <span data-ttu-id="21557-278">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="21557-278">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="21557-279">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-279">Optional</span></span> | <span data-ttu-id="21557-280">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="21557-280">Profile's name or GUID as a string</span></span> | <span data-ttu-id="21557-281">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="21557-281">Profile that will open based on its GUID or name.</span></span> |

### <a name="open-next-tab"></a><span data-ttu-id="21557-282">Apri scheda successiva</span><span class="sxs-lookup"><span data-stu-id="21557-282">Open next tab</span></span>

<span data-ttu-id="21557-283">Apre la scheda a destra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="21557-283">This opens the tab to the right of the current one.</span></span>

<span data-ttu-id="21557-284">**Nome del comando:** `nextTab`</span><span class="sxs-lookup"><span data-stu-id="21557-284">**Command name:** `nextTab`</span></span>

<span data-ttu-id="21557-285">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-285">**Default binding:**</span></span>

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a><span data-ttu-id="21557-286">Apri scheda precedente</span><span class="sxs-lookup"><span data-stu-id="21557-286">Open previous tab</span></span>

<span data-ttu-id="21557-287">Apre la scheda a sinistra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="21557-287">This opens the tab to the left of the current one.</span></span>

<span data-ttu-id="21557-288">**Nome del comando:** `prevTab`</span><span class="sxs-lookup"><span data-stu-id="21557-288">**Command name:** `prevTab`</span></span>

<span data-ttu-id="21557-289">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-289">**Default binding:**</span></span>

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="tab-search"></a><span data-ttu-id="21557-290">Ricerca nella scheda</span><span class="sxs-lookup"><span data-stu-id="21557-290">Tab search</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="21557-291">Verrà visualizzata la casella di ricerca della scheda.</span><span class="sxs-lookup"><span data-stu-id="21557-291">This opens the tab search box.</span></span>

<span data-ttu-id="21557-292">**Nome del comando:** `tabSearch`</span><span class="sxs-lookup"><span data-stu-id="21557-292">**Command name:** `tabSearch`</span></span>

<span data-ttu-id="21557-293">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-293">**Default binding:**</span></span>

<span data-ttu-id="21557-294">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="21557-294">_This command is not currently bound in the default settings_.</span></span>

```json
{"command": "tabSearch", "keys": ""}
```

:::column-end:::
:::column span="":::
![Ricerca nella scheda terminale di Windows](./../images/tab-search.gif)

:::column-end:::
:::row-end:::

### <a name="open-a-specific-tab"></a><span data-ttu-id="21557-296">Apri una scheda specifica</span><span class="sxs-lookup"><span data-stu-id="21557-296">Open a specific tab</span></span>

<span data-ttu-id="21557-297">Apre una scheda specifica a seconda dell'indice.</span><span class="sxs-lookup"><span data-stu-id="21557-297">This opens a specific tab depending on the index.</span></span>

<span data-ttu-id="21557-298">**Nome del comando:** `switchToTab`</span><span class="sxs-lookup"><span data-stu-id="21557-298">**Command name:** `switchToTab`</span></span>

<span data-ttu-id="21557-299">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-299">**Default bindings:**</span></span>

```json
{ "command": { "action": "switchToTab", "index": 0 }, "keys": "ctrl+alt+1" },
{ "command": { "action": "switchToTab", "index": 1 }, "keys": "ctrl+alt+2" },
{ "command": { "action": "switchToTab", "index": 2 }, "keys": "ctrl+alt+3" },
{ "command": { "action": "switchToTab", "index": 3 }, "keys": "ctrl+alt+4" },
{ "command": { "action": "switchToTab", "index": 4 }, "keys": "ctrl+alt+5" },
{ "command": { "action": "switchToTab", "index": 5 }, "keys": "ctrl+alt+6" },
{ "command": { "action": "switchToTab", "index": 6 }, "keys": "ctrl+alt+7" },
{ "command": { "action": "switchToTab", "index": 7 }, "keys": "ctrl+alt+8" },
{ "command": { "action": "switchToTab", "index": 8 }, "keys": "ctrl+alt+9" }
```

#### <a name="actions"></a><span data-ttu-id="21557-300">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-300">Actions</span></span>

| <span data-ttu-id="21557-301">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-301">Name</span></span> | <span data-ttu-id="21557-302">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-302">Necessity</span></span> | <span data-ttu-id="21557-303">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-303">Accepts</span></span> | <span data-ttu-id="21557-304">Description</span><span class="sxs-lookup"><span data-stu-id="21557-304">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="21557-305">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-305">Required</span></span> | <span data-ttu-id="21557-306">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-306">Integer</span></span> | <span data-ttu-id="21557-307">Scheda che verrà aperta in base alla relativa posizione nella barra delle schede (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="21557-307">Tab that will open based on its position in the tab bar (starting at 0).</span></span> |

### <a name="rename-tab"></a><span data-ttu-id="21557-308">Rinomina scheda</span><span class="sxs-lookup"><span data-stu-id="21557-308">Rename tab</span></span>

<span data-ttu-id="21557-309">Questo comando può essere usato per rinominare una scheda in una stringa specifica.</span><span class="sxs-lookup"><span data-stu-id="21557-309">This command can be used to rename a tab to a specific string.</span></span>

<span data-ttu-id="21557-310">**Nome del comando:** `renameTab`</span><span class="sxs-lookup"><span data-stu-id="21557-310">**Command name:** `renameTab`</span></span>

<span data-ttu-id="21557-311">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-311">**Default binding:**</span></span>

<span data-ttu-id="21557-312">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="21557-312">_This command is not currently bound in the default settings_.</span></span>

```json
// Rename a tab to "Foo"
{ "command": { "action": "renameTab", "title": "Foo" }, "keys": "" }

// Reset the tab's name
{ "command": { "action": "renameTab", "title": null }, "keys": "" }
```

#### <a name="actions"></a><span data-ttu-id="21557-313">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-313">Actions</span></span>

| <span data-ttu-id="21557-314">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-314">Name</span></span> | <span data-ttu-id="21557-315">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-315">Necessity</span></span> | <span data-ttu-id="21557-316">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-316">Accepts</span></span> | <span data-ttu-id="21557-317">Description</span><span class="sxs-lookup"><span data-stu-id="21557-317">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `title` | <span data-ttu-id="21557-318">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-318">Optional</span></span> | <span data-ttu-id="21557-319">String</span><span class="sxs-lookup"><span data-stu-id="21557-319">String</span></span> | <span data-ttu-id="21557-320">Nuovo titolo da utilizzare per questa scheda. Se omesso, il comando ripristinerà nuovamente il titolo della scheda al valore originale.</span><span class="sxs-lookup"><span data-stu-id="21557-320">The new title to use for this tab. If omitted, this command will revert the tab title back to its original value.</span></span> |

### <a name="open-tab-rename-text-box"></a><span data-ttu-id="21557-321">Aprire la casella di testo Rinomina tabulazione</span><span class="sxs-lookup"><span data-stu-id="21557-321">Open tab rename text box</span></span>

<span data-ttu-id="21557-322">Questo comando modifica il titolo della scheda in un campo di testo che consente di modificare il titolo per la scheda corrente. Se si deseleziona il campo di testo, il titolo della scheda viene reimpostato sul valore predefinito per l'istanza corrente della shell.</span><span class="sxs-lookup"><span data-stu-id="21557-322">This command changes the tab title into a text field that lets you edit the title for the current tab. Clearing the text field will reset the tab title back to the default for the current shell instance.</span></span>

<span data-ttu-id="21557-323">**Nome del comando:** `openTabRenamer`</span><span class="sxs-lookup"><span data-stu-id="21557-323">**Command name:** `openTabRenamer`</span></span>

<span data-ttu-id="21557-324">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-324">**Default binding:**</span></span>

<span data-ttu-id="21557-325">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="21557-325">_This command is not currently bound in the default settings_.</span></span>

```json
{ "command": "openTabRenamer", "keys": "ctrl+alt+a" }
```

### <a name="change-tab-color"></a><span data-ttu-id="21557-326">Cambia colore scheda</span><span class="sxs-lookup"><span data-stu-id="21557-326">Change tab color</span></span>

<span data-ttu-id="21557-327">Questo comando può essere usato per modificare il colore di una scheda in un valore specifico.</span><span class="sxs-lookup"><span data-stu-id="21557-327">This command can be used to change the color of a tab to a specific value.</span></span>

<span data-ttu-id="21557-328">**Nome del comando:** `setTabColor`</span><span class="sxs-lookup"><span data-stu-id="21557-328">**Command name:** `setTabColor`</span></span>

<span data-ttu-id="21557-329">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-329">**Default binding:**</span></span>

<span data-ttu-id="21557-330">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="21557-330">_This command is not currently bound in the default settings_.</span></span>

```json
// Change the tab's color to a bright magenta
{ "command": { "action": "setTabColor", "color": "#ff00ff" }, "keys": "" }

// Reset the tab's color
{ "command": { "action": "setTabColor", "color": null }, "keys": "" }
```

#### <a name="actions"></a><span data-ttu-id="21557-331">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-331">Actions</span></span>

| <span data-ttu-id="21557-332">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-332">Name</span></span> | <span data-ttu-id="21557-333">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-333">Necessity</span></span> | <span data-ttu-id="21557-334">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-334">Accepts</span></span> | <span data-ttu-id="21557-335">Description</span><span class="sxs-lookup"><span data-stu-id="21557-335">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `color` | <span data-ttu-id="21557-336">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-336">Optional</span></span> | <span data-ttu-id="21557-337">Stringa, in formato esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="21557-337">String, in hex format: `"#rgb"` or `"#rrggbb"`</span></span> | <span data-ttu-id="21557-338">Nuovo colore da usare per questa scheda. Se omesso, il comando ripristinerà il colore della scheda al valore originale.</span><span class="sxs-lookup"><span data-stu-id="21557-338">The new color to use for this tab. If omitted, this command will revert the tab's color back to its original value.</span></span> |

### <a name="open-tab-color-picker"></a><span data-ttu-id="21557-339">Apri selezione colori scheda</span><span class="sxs-lookup"><span data-stu-id="21557-339">Open tab color picker</span></span>

<span data-ttu-id="21557-340">Questo comando può essere usato per aprire la selezione colori per la scheda attiva. La selezione colori può essere usata per impostare un colore per la scheda in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="21557-340">This command can be used to open the color picker for the active tab. The color picker can be used to set a color for the tab at runtime.</span></span>

<span data-ttu-id="21557-341">**Nome del comando:** `openTabColorPicker`</span><span class="sxs-lookup"><span data-stu-id="21557-341">**Command name:** `openTabColorPicker`</span></span>

<span data-ttu-id="21557-342">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-342">**Default binding:**</span></span>

```json
{ "command": "openTabColorPicker" }
```

### <a name="move-tab-preview"></a><span data-ttu-id="21557-343">Scheda Sposta ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="21557-343">Move tab ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="21557-344">Questo comando Sposta la scheda "indietro" e "Avanti", che equivale a "left" e "Right" nell'interfaccia utente da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="21557-344">This command moves the tab "backward" and "forward", which is equivalent to "left" and "right" in left-to-right UI.</span></span>

<span data-ttu-id="21557-345">**Nome del comando:** `moveTab`</span><span class="sxs-lookup"><span data-stu-id="21557-345">**Command name:** `moveTab`</span></span>

<span data-ttu-id="21557-346">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-346">**Default binding:**</span></span>

<span data-ttu-id="21557-347">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="21557-347">_This command is not currently bound in the default settings_.</span></span>

```json
// Move tab backward (left in LTR)
{ "command": { "action": "moveTab", "direction": "backward" }, "keys": "" }

// Move tab forward (right in LTR)
{ "command": { "action": "moveTab", "direction": "forward" }, "keys": "" }
```

#### <a name="actions"></a><span data-ttu-id="21557-348">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-348">Actions</span></span>

| <span data-ttu-id="21557-349">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-349">Name</span></span> | <span data-ttu-id="21557-350">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-350">Necessity</span></span> | <span data-ttu-id="21557-351">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-351">Accepts</span></span> | <span data-ttu-id="21557-352">Description</span><span class="sxs-lookup"><span data-stu-id="21557-352">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="21557-353">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-353">Required</span></span> | <span data-ttu-id="21557-354">`"backward"`, `"forward"`</span><span class="sxs-lookup"><span data-stu-id="21557-354">`"backward"`, `"forward"`</span></span> | <span data-ttu-id="21557-355">Direzione in cui la scheda viene spostata.</span><span class="sxs-lookup"><span data-stu-id="21557-355">Direction in which the tab will move.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="21557-356">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="21557-356">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

<br />

___

## <a name="pane-management-commands"></a><span data-ttu-id="21557-357">Comandi di gestione dei riquadri</span><span class="sxs-lookup"><span data-stu-id="21557-357">Pane management commands</span></span>

### <a name="close-pane"></a><span data-ttu-id="21557-358">Chiudi riquadro</span><span class="sxs-lookup"><span data-stu-id="21557-358">Close pane</span></span>

<span data-ttu-id="21557-359">Chiude il riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="21557-359">This closes the active pane.</span></span> <span data-ttu-id="21557-360">Se non sono presenti riquadri divisi, chiude la scheda corrente. Se è aperta una sola scheda, chiude la finestra.</span><span class="sxs-lookup"><span data-stu-id="21557-360">If there aren't any split panes, this will close the current tab. If there is only one tab open, this will close the window.</span></span>

<span data-ttu-id="21557-361">**Nome del comando:** `closePane`</span><span class="sxs-lookup"><span data-stu-id="21557-361">**Command name:** `closePane`</span></span>

<span data-ttu-id="21557-362">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-362">**Default binding:**</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a><span data-ttu-id="21557-363">Sposta stato attivo nel riquadro</span><span class="sxs-lookup"><span data-stu-id="21557-363">Move pane focus</span></span>

<span data-ttu-id="21557-364">Consente di spostare lo stato attivo in un altro riquadro a seconda della direzione.</span><span class="sxs-lookup"><span data-stu-id="21557-364">This changes focus to a different pane depending on the direction.</span></span> <span data-ttu-id="21557-365">Impostando `direction` su `"previous"` , lo stato attivo viene spostato sul riquadro usato più di recente.</span><span class="sxs-lookup"><span data-stu-id="21557-365">Setting the `direction` to `"previous"` will move focus to the most recently used pane.</span></span>

<span data-ttu-id="21557-366">**Nome del comando:** `moveFocus`</span><span class="sxs-lookup"><span data-stu-id="21557-366">**Command name:** `moveFocus`</span></span>

<span data-ttu-id="21557-367">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-367">**Default bindings:**</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" },
{ "command": { "action": "moveFocus", "direction": "previous" }, "keys": "ctrl+alt+left" }
```

#### <a name="actions"></a><span data-ttu-id="21557-368">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-368">Actions</span></span>

| <span data-ttu-id="21557-369">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-369">Name</span></span> | <span data-ttu-id="21557-370">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-370">Necessity</span></span> | <span data-ttu-id="21557-371">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-371">Accepts</span></span> | <span data-ttu-id="21557-372">Description</span><span class="sxs-lookup"><span data-stu-id="21557-372">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="21557-373">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-373">Required</span></span> | <span data-ttu-id="21557-374">`"left"`, `"right"`, `"up"`, `"down"`, `"previous"`</span><span class="sxs-lookup"><span data-stu-id="21557-374">`"left"`, `"right"`, `"up"`, `"down"`, `"previous"`</span></span> | <span data-ttu-id="21557-375">Direzione in cui viene spostato lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="21557-375">Direction in which the focus will move.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="21557-376">La `"previous"` direzione è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="21557-376">The `"previous"` direction is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="zoom-a-pane"></a><span data-ttu-id="21557-377">Ingrandire un riquadro</span><span class="sxs-lookup"><span data-stu-id="21557-377">Zoom a pane</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="21557-378">In questo modo si espande il riquadro con lo stato attivo per riempire l'intero contenuto della finestra.</span><span class="sxs-lookup"><span data-stu-id="21557-378">This expands the focused pane to fill the entire contents of the window.</span></span>

<span data-ttu-id="21557-379">**Nome del comando:** `togglePaneZoom`</span><span class="sxs-lookup"><span data-stu-id="21557-379">**Command name:** `togglePaneZoom`</span></span>

<span data-ttu-id="21557-380">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-380">**Default binding:**</span></span>

```json
{ "command": "togglePaneZoom" }
```

:::column-end:::
:::column span="":::
![Zoom del riquadro di attivazione/disconnessione del terminale di Windows](./../images/toggle-pane-zoom.gif)

:::column-end:::
:::row-end:::

### <a name="resize-a-pane"></a><span data-ttu-id="21557-382">Ridimensiona un riquadro</span><span class="sxs-lookup"><span data-stu-id="21557-382">Resize a pane</span></span>

<span data-ttu-id="21557-383">Modifica le dimensioni del riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="21557-383">This changes the size of the active pane.</span></span>

<span data-ttu-id="21557-384">**Nome del comando:** `resizePane`</span><span class="sxs-lookup"><span data-stu-id="21557-384">**Command name:** `resizePane`</span></span>

<span data-ttu-id="21557-385">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-385">**Default bindings:**</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="21557-386">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-386">Actions</span></span>

| <span data-ttu-id="21557-387">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-387">Name</span></span> | <span data-ttu-id="21557-388">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-388">Necessity</span></span> | <span data-ttu-id="21557-389">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-389">Accepts</span></span> | <span data-ttu-id="21557-390">Description</span><span class="sxs-lookup"><span data-stu-id="21557-390">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="21557-391">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-391">Required</span></span> | <span data-ttu-id="21557-392">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="21557-392">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="21557-393">Direzione in cui verranno modificate le dimensioni del riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-393">Direction in which the pane will be resized.</span></span> |

### <a name="split-a-pane"></a><span data-ttu-id="21557-394">Dividi un riquadro</span><span class="sxs-lookup"><span data-stu-id="21557-394">Split a pane</span></span>

<span data-ttu-id="21557-395">Divide a metà il riquadro attivo e ne apre un altro.</span><span class="sxs-lookup"><span data-stu-id="21557-395">This halves the size of the active pane and opens another.</span></span> <span data-ttu-id="21557-396">Se viene specificato senza argomenti, il profilo predefinito verrà aperto nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-396">Without any arguments, this will open the default profile in the new pane.</span></span> <span data-ttu-id="21557-397">Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="21557-397">If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="21557-398">**Nome del comando:** `splitPane`</span><span class="sxs-lookup"><span data-stu-id="21557-398">**Command name:** `splitPane`</span></span>

<span data-ttu-id="21557-399">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-399">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal" }, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical" }, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a><span data-ttu-id="21557-400">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-400">Actions</span></span>

| <span data-ttu-id="21557-401">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-401">Name</span></span> | <span data-ttu-id="21557-402">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-402">Necessity</span></span> | <span data-ttu-id="21557-403">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-403">Accepts</span></span> | <span data-ttu-id="21557-404">Description</span><span class="sxs-lookup"><span data-stu-id="21557-404">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `split` | <span data-ttu-id="21557-405">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-405">Required</span></span> | <span data-ttu-id="21557-406">`"vertical"`, `"horizontal"`, `"auto"`</span><span class="sxs-lookup"><span data-stu-id="21557-406">`"vertical"`, `"horizontal"`, `"auto"`</span></span> | <span data-ttu-id="21557-407">Modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-407">How the pane will split.</span></span> <span data-ttu-id="21557-408">Con `"auto"` il riquadro verrà diviso nella direzione che offre l'area con la superficie più estesa.</span><span class="sxs-lookup"><span data-stu-id="21557-408">`"auto"` will split in the direction that provides the most surface area.</span></span> |
| `commandline` | <span data-ttu-id="21557-409">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-409">Optional</span></span> | <span data-ttu-id="21557-410">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="21557-410">Executable file name as a string</span></span> | <span data-ttu-id="21557-411">Esegue l'eseguibile all'interno del riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-411">Executable run within the pane.</span></span> |
| `startingDirectory` | <span data-ttu-id="21557-412">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-412">Optional</span></span> | <span data-ttu-id="21557-413">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="21557-413">Folder location as a string</span></span> | <span data-ttu-id="21557-414">Directory in cui verrà aperto il riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-414">Directory in which the pane will open.</span></span> |
| `tabTitle` | <span data-ttu-id="21557-415">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-415">Optional</span></span> | <span data-ttu-id="21557-416">String</span><span class="sxs-lookup"><span data-stu-id="21557-416">String</span></span> | <span data-ttu-id="21557-417">Titolo della scheda quando lo stato attivo si trova nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-417">Title of the tab when the new pane is focused.</span></span> |
| `index` | <span data-ttu-id="21557-418">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-418">Optional</span></span> | <span data-ttu-id="21557-419">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-419">Integer</span></span> | <span data-ttu-id="21557-420">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="21557-420">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="21557-421">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-421">Optional</span></span> | <span data-ttu-id="21557-422">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="21557-422">Profile's name or GUID as a string</span></span> | <span data-ttu-id="21557-423">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="21557-423">Profile that will open based on its GUID or name.</span></span> |
| `splitMode` | <span data-ttu-id="21557-424">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-424">Optional</span></span> | `"duplicate"` | <span data-ttu-id="21557-425">Controlla la modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-425">Controls how the pane splits.</span></span> <span data-ttu-id="21557-426">Accetta solo `"duplicate"`, con cui il profilo del riquadro con lo stato attivo viene duplicato in un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="21557-426">Only accepts `"duplicate"`, which will duplicate the focused pane's profile into a new pane.</span></span> |
| `size` | <span data-ttu-id="21557-427">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-427">Optional</span></span> | <span data-ttu-id="21557-428">Float</span><span class="sxs-lookup"><span data-stu-id="21557-428">Float</span></span> | <span data-ttu-id="21557-429">Consente di specificare la dimensione del nuovo riquadro, come frazione della dimensione del riquadro corrente.</span><span class="sxs-lookup"><span data-stu-id="21557-429">Specify how large the new pane should be, as a fraction of the current pane's size.</span></span> <span data-ttu-id="21557-430">`1.0` è "all of the current pane" e `0.0` è "None of the parent".</span><span class="sxs-lookup"><span data-stu-id="21557-430">`1.0` would be "all of the current pane", and `0.0` is "None of the parent".</span></span> <span data-ttu-id="21557-431">Il valore predefinito è `0.5`.</span><span class="sxs-lookup"><span data-stu-id="21557-431">Defaults to `0.5`.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="21557-432">Il `size` parametro è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="21557-432">The `size` parameter is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

<br />

___

## <a name="clipboard-integration-commands"></a><span data-ttu-id="21557-433">Comandi di integrazione degli Appunti</span><span class="sxs-lookup"><span data-stu-id="21557-433">Clipboard integration commands</span></span>

### <a name="copy"></a><span data-ttu-id="21557-434">Copia</span><span class="sxs-lookup"><span data-stu-id="21557-434">Copy</span></span>

<span data-ttu-id="21557-435">Copia il contenuto del terminale selezionato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="21557-435">This copies the selected terminal content to your clipboard.</span></span>

<span data-ttu-id="21557-436">**Nome del comando:** `copy`</span><span class="sxs-lookup"><span data-stu-id="21557-436">**Command name:** `copy`</span></span>

<span data-ttu-id="21557-437">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-437">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="actions"></a><span data-ttu-id="21557-438">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-438">Actions</span></span>

| <span data-ttu-id="21557-439">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-439">Name</span></span> | <span data-ttu-id="21557-440">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-440">Necessity</span></span> | <span data-ttu-id="21557-441">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-441">Accepts</span></span> | <span data-ttu-id="21557-442">Description</span><span class="sxs-lookup"><span data-stu-id="21557-442">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `singleLine` | <span data-ttu-id="21557-443">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-443">Optional</span></span> | <span data-ttu-id="21557-444">`true`, `false`</span><span class="sxs-lookup"><span data-stu-id="21557-444">`true`, `false`</span></span> | <span data-ttu-id="21557-445">Quando è `true`, il contenuto copiato verrà copiato come una riga singola.</span><span class="sxs-lookup"><span data-stu-id="21557-445">When `true`, the copied content will be copied as a single line.</span></span> <span data-ttu-id="21557-446">Quando è `false`, i caratteri di nuova riga del testo selezionato vengono mantenuti.</span><span class="sxs-lookup"><span data-stu-id="21557-446">When `false`, newlines persist from the selected text.</span></span> |
| `copyFormatting` | <span data-ttu-id="21557-447">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-447">Optional</span></span> | <span data-ttu-id="21557-448">`true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"`</span><span class="sxs-lookup"><span data-stu-id="21557-448">`true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"`</span></span> | <span data-ttu-id="21557-449">Quando `true` , anche il colore e la formattazione dei caratteri del testo selezionato vengono copiati negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="21557-449">When `true`, the color and font formatting of the selected text is also copied to your clipboard.</span></span> <span data-ttu-id="21557-450">Quando `false` , solo il testo normale viene copiato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="21557-450">When `false`, only plain text is copied to your clipboard.</span></span> <span data-ttu-id="21557-451">È inoltre possibile specificare i formati che si desidera copiare.</span><span class="sxs-lookup"><span data-stu-id="21557-451">You can also specify which formats you would like to copy.</span></span> <span data-ttu-id="21557-452">Se `null` , il `"copyFormatting"` comportamento globale viene ereditato.</span><span class="sxs-lookup"><span data-stu-id="21557-452">When `null`, the global `"copyFormatting"` behavior is inherited.</span></span> |

### <a name="paste"></a><span data-ttu-id="21557-453">Incolla</span><span class="sxs-lookup"><span data-stu-id="21557-453">Paste</span></span>

<span data-ttu-id="21557-454">Inserisce il contenuto copiato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="21557-454">This inserts the content that was copied onto the clipboard.</span></span>

<span data-ttu-id="21557-455">**Nome del comando:** `paste`</span><span class="sxs-lookup"><span data-stu-id="21557-455">**Command name:** `paste`</span></span>

<span data-ttu-id="21557-456">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-456">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a><span data-ttu-id="21557-457">Comandi di scorrimento</span><span class="sxs-lookup"><span data-stu-id="21557-457">Scrollback commands</span></span>

### <a name="scroll-up"></a><span data-ttu-id="21557-458">Scorri verso l'alto</span><span class="sxs-lookup"><span data-stu-id="21557-458">Scroll up</span></span>

<span data-ttu-id="21557-459">Scorre lo schermo verso l'alto in base al numero di righe definito da `"rowsToScroll"` .</span><span class="sxs-lookup"><span data-stu-id="21557-459">This scrolls the screen up by the number of rows defined by `"rowsToScroll"`.</span></span> <span data-ttu-id="21557-460">Se `"rowsToScroll"` non viene specificato, scorrerà verso l'alto la quantità definita dall'impostazione predefinita del sistema, ovvero la stessa quantità di scorrimento del mouse.</span><span class="sxs-lookup"><span data-stu-id="21557-460">If `"rowsToScroll"` is not provided, it will scroll up the amount defined by the system default, which is the same amount as mouse scrolling.</span></span>

<span data-ttu-id="21557-461">**Nome del comando:** `scrollUp`</span><span class="sxs-lookup"><span data-stu-id="21557-461">**Command name:** `scrollUp`</span></span>

<span data-ttu-id="21557-462">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-462">**Default binding:**</span></span>

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="21557-463">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-463">Actions</span></span>

| <span data-ttu-id="21557-464">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-464">Name</span></span> | <span data-ttu-id="21557-465">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-465">Necessity</span></span> | <span data-ttu-id="21557-466">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-466">Accepts</span></span> | <span data-ttu-id="21557-467">Description</span><span class="sxs-lookup"><span data-stu-id="21557-467">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `rowsToScroll` | <span data-ttu-id="21557-468">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-468">Optional</span></span> | <span data-ttu-id="21557-469">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-469">Integer</span></span> | <span data-ttu-id="21557-470">Numero di righe da scorrere.</span><span class="sxs-lookup"><span data-stu-id="21557-470">The number of rows to scroll.</span></span> |

### <a name="scroll-down"></a><span data-ttu-id="21557-471">Scorri verso il basso</span><span class="sxs-lookup"><span data-stu-id="21557-471">Scroll down</span></span>

<span data-ttu-id="21557-472">Scorre lo schermo verso il basso in base al numero di righe definito da `"rowsToScroll"` .</span><span class="sxs-lookup"><span data-stu-id="21557-472">This scrolls the screen down by the number of rows defined by `"rowsToScroll"`.</span></span> <span data-ttu-id="21557-473">Se `"rowsToScroll"` non viene specificato, scorre verso il basso la quantità definita dall'impostazione predefinita del sistema, che corrisponde allo scorrimento del mouse.</span><span class="sxs-lookup"><span data-stu-id="21557-473">If `"rowsToScroll"` is not provided, it will scroll down the amount defined by the system default, which is the same amount as mouse scrolling.</span></span>

<span data-ttu-id="21557-474">**Nome del comando:** `scrollDown`</span><span class="sxs-lookup"><span data-stu-id="21557-474">**Command name:** `scrollDown`</span></span>

<span data-ttu-id="21557-475">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-475">**Default binding:**</span></span>

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

#### <a name="actions"></a><span data-ttu-id="21557-476">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-476">Actions</span></span>

| <span data-ttu-id="21557-477">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-477">Name</span></span> | <span data-ttu-id="21557-478">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-478">Necessity</span></span> | <span data-ttu-id="21557-479">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-479">Accepts</span></span> | <span data-ttu-id="21557-480">Description</span><span class="sxs-lookup"><span data-stu-id="21557-480">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `rowsToScroll` | <span data-ttu-id="21557-481">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="21557-481">Optional</span></span> | <span data-ttu-id="21557-482">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-482">Integer</span></span> | <span data-ttu-id="21557-483">Numero di righe da scorrere.</span><span class="sxs-lookup"><span data-stu-id="21557-483">The number of rows to scroll.</span></span> |

### <a name="scroll-up-a-whole-page"></a><span data-ttu-id="21557-484">Scorri verso l'alto di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="21557-484">Scroll up a whole page</span></span>

<span data-ttu-id="21557-485">Scorre lo schermo verso l'alto di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="21557-485">This scrolls the screen up by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="21557-486">**Nome del comando:** `scrollUpPage`</span><span class="sxs-lookup"><span data-stu-id="21557-486">**Command name:** `scrollUpPage`</span></span>

<span data-ttu-id="21557-487">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-487">**Default binding:**</span></span>

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a><span data-ttu-id="21557-488">Scorri verso il basso di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="21557-488">Scroll down a whole page</span></span>

<span data-ttu-id="21557-489">Scorre lo schermo verso il basso di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="21557-489">This scrolls the screen down by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="21557-490">**Nome del comando:** `scrollDownPage`</span><span class="sxs-lookup"><span data-stu-id="21557-490">**Command name:** `scrollDownPage`</span></span>

<span data-ttu-id="21557-491">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-491">**Default binding:**</span></span>

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

### <a name="scroll-to-the-earliest-history"></a><span data-ttu-id="21557-492">Scorri fino alla cronologia più antica</span><span class="sxs-lookup"><span data-stu-id="21557-492">Scroll to the earliest history</span></span>

<span data-ttu-id="21557-493">Scorre lo schermo verso l'alto nella parte superiore del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="21557-493">This scrolls the screen up to the top of the input buffer.</span></span>

<span data-ttu-id="21557-494">**Nome del comando:** `scrollToTop`</span><span class="sxs-lookup"><span data-stu-id="21557-494">**Command name:** `scrollToTop`</span></span>

<span data-ttu-id="21557-495">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-495">**Default binding:**</span></span>

```json
{ "command": "scrollToTop", "keys": "ctrl+shift+home" }
```

> [!IMPORTANT]
> <span data-ttu-id="21557-496">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="21557-496">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="scroll-to-the-latest-history"></a><span data-ttu-id="21557-497">Scorrere fino alla cronologia più recente</span><span class="sxs-lookup"><span data-stu-id="21557-497">Scroll to the latest history</span></span>

<span data-ttu-id="21557-498">Scorre lo schermo verso il basso fino alla fine del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="21557-498">This scrolls the screen down to the bottom of the input buffer.</span></span>

<span data-ttu-id="21557-499">**Nome del comando:** `scrollToBottom`</span><span class="sxs-lookup"><span data-stu-id="21557-499">**Command name:** `scrollToBottom`</span></span>

<span data-ttu-id="21557-500">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-500">**Default binding:**</span></span>

```json
{ "command": "scrollToBottom", "keys": "ctrl+shift+end" }
```

> [!IMPORTANT]
> <span data-ttu-id="21557-501">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="21557-501">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

<br />

___

## <a name="visual-adjustment-commands"></a><span data-ttu-id="21557-502">Comandi di regolazione della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="21557-502">Visual adjustment commands</span></span>

### <a name="adjust-font-size"></a><span data-ttu-id="21557-503">Regola dimensioni caratteri</span><span class="sxs-lookup"><span data-stu-id="21557-503">Adjust font size</span></span>

<span data-ttu-id="21557-504">Modifica le dimensioni del testo in base al numero di punti specificato.</span><span class="sxs-lookup"><span data-stu-id="21557-504">This changes the text size by a specified point amount.</span></span>

<span data-ttu-id="21557-505">**Nome del comando:** `adjustFontSize`</span><span class="sxs-lookup"><span data-stu-id="21557-505">**Command name:** `adjustFontSize`</span></span>

<span data-ttu-id="21557-506">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="21557-506">**Default bindings:**</span></span>

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a><span data-ttu-id="21557-507">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-507">Actions</span></span>

| <span data-ttu-id="21557-508">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-508">Name</span></span> | <span data-ttu-id="21557-509">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-509">Necessity</span></span> | <span data-ttu-id="21557-510">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-510">Accepts</span></span> | <span data-ttu-id="21557-511">Description</span><span class="sxs-lookup"><span data-stu-id="21557-511">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `delta` | <span data-ttu-id="21557-512">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-512">Required</span></span> | <span data-ttu-id="21557-513">Intero</span><span class="sxs-lookup"><span data-stu-id="21557-513">Integer</span></span> | <span data-ttu-id="21557-514">Modifiche applicate alle dimensioni per ogni chiamata del comando.</span><span class="sxs-lookup"><span data-stu-id="21557-514">Amount of size change per command invocation.</span></span> |

### <a name="reset-font-size"></a><span data-ttu-id="21557-515">Reimposta dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="21557-515">Reset font size</span></span>

<span data-ttu-id="21557-516">Reimposta le dimensioni del testo in base al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="21557-516">This resets the text size to the default value.</span></span>

<span data-ttu-id="21557-517">**Nome del comando:** `resetFontSize`</span><span class="sxs-lookup"><span data-stu-id="21557-517">**Command name:** `resetFontSize`</span></span>

<span data-ttu-id="21557-518">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-518">**Default binding:**</span></span>

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

### <a name="toggle-pixel-shader-effects"></a><span data-ttu-id="21557-519">Imposta/Nascondi pixel shader effetti</span><span class="sxs-lookup"><span data-stu-id="21557-519">Toggle pixel shader effects</span></span>

<span data-ttu-id="21557-520">Questo consente di attivare o disabilitare gli effetti pixel shader abilitati nel terminale.</span><span class="sxs-lookup"><span data-stu-id="21557-520">This toggles any pixel shader effects enabled in the terminal.</span></span> <span data-ttu-id="21557-521">Se l'utente ha specificato uno shader valido con `experimental.pixelShaderPath` , questa azione attiva o disattiva lo shader.</span><span class="sxs-lookup"><span data-stu-id="21557-521">If the user specified a valid shader with `experimental.pixelShaderPath`, this action will toggle that shader on/off.</span></span> <span data-ttu-id="21557-522">Verrà inoltre attivato il "effetto terminale retrò", che è abilitato con l'impostazione del profilo `experimental.retroTerminalEffect` .</span><span class="sxs-lookup"><span data-stu-id="21557-522">This will also toggle the "retro terminal effect", which is enabled with the profile setting `experimental.retroTerminalEffect`.</span></span>

<span data-ttu-id="21557-523">**Nome del comando:** `toggleShaderEffects`</span><span class="sxs-lookup"><span data-stu-id="21557-523">**Command name:** `toggleShaderEffects`</span></span>

<span data-ttu-id="21557-524">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="21557-524">**Default binding:**</span></span>

```json
{ "command": "toggleShaderEffects" }
```

> [!CAUTION]
> <span data-ttu-id="21557-525">L' `toggleRetroEffect` azione non è più disponibile nelle versioni 1,6 e successive.</span><span class="sxs-lookup"><span data-stu-id="21557-525">The `toggleRetroEffect` action is no longer available in versions 1.6 and later.</span></span> <span data-ttu-id="21557-526">Si consiglia di usare in `toggleShaderEffects` alternativa.</span><span class="sxs-lookup"><span data-stu-id="21557-526">It is recommended that you use `toggleShaderEffects` instead.</span></span>

### <a name="set-the-color-scheme"></a><span data-ttu-id="21557-527">Imposta la combinazione di colori</span><span class="sxs-lookup"><span data-stu-id="21557-527">Set the color scheme</span></span>

<span data-ttu-id="21557-528">Modifica la combinazione di colori attiva.</span><span class="sxs-lookup"><span data-stu-id="21557-528">Changes the active color scheme.</span></span>

<span data-ttu-id="21557-529">**Nome del comando:** `setColorScheme`</span><span class="sxs-lookup"><span data-stu-id="21557-529">**Command name:** `setColorScheme`</span></span>

#### <a name="actions"></a><span data-ttu-id="21557-530">Azioni</span><span class="sxs-lookup"><span data-stu-id="21557-530">Actions</span></span>

| <span data-ttu-id="21557-531">Nome</span><span class="sxs-lookup"><span data-stu-id="21557-531">Name</span></span> | <span data-ttu-id="21557-532">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-532">Necessity</span></span> | <span data-ttu-id="21557-533">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="21557-533">Accepts</span></span> | <span data-ttu-id="21557-534">Description</span><span class="sxs-lookup"><span data-stu-id="21557-534">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `colorScheme` | <span data-ttu-id="21557-535">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="21557-535">Required</span></span> | <span data-ttu-id="21557-536">string</span><span class="sxs-lookup"><span data-stu-id="21557-536">String</span></span> | <span data-ttu-id="21557-537">Oggetto `name` della combinazione di colori da applicare.</span><span class="sxs-lookup"><span data-stu-id="21557-537">The `name` of the color scheme to apply.</span></span> |

<span data-ttu-id="21557-538">**Associazione di esempio:**</span><span class="sxs-lookup"><span data-stu-id="21557-538">**Example binding:**</span></span>

```json
{ "command": { "action": "setColorScheme", "colorScheme": "Campbell" }, "keys": "" }
```

<br />

___

## <a name="unbind-keys"></a><span data-ttu-id="21557-539">Disassocia tasti</span><span class="sxs-lookup"><span data-stu-id="21557-539">Unbind keys</span></span>

<span data-ttu-id="21557-540">Annulla l'associazione dei tasti per tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="21557-540">This unbinds the associated keys from any command.</span></span>

<span data-ttu-id="21557-541">**Nome del comando:** `unbound`</span><span class="sxs-lookup"><span data-stu-id="21557-541">**Command name:** `unbound`</span></span>
