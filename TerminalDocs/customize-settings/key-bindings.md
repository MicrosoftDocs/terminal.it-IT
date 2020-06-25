---
title: Terminale Windows - Tasti di scelta rapida
description: Informazioni su come creare tasti di scelta rapida personalizzati per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 2716e3bfbbc290eb3f2bdce58d0de5c12ee3225d
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994294"
---
# <a name="custom-key-bindings-in-windows-terminal"></a><span data-ttu-id="308c4-103">Tasti di scelta rapida personalizzati in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="308c4-103">Custom key bindings in Windows Terminal</span></span>

<span data-ttu-id="308c4-104">In Terminale Windows è possibile creare tasti di scelta rapida personalizzati per controllare l'interazione con il terminale tramite la tastiera.</span><span class="sxs-lookup"><span data-stu-id="308c4-104">You can create custom key bindings (keyboard shortcuts) inside Windows Terminal that give you control of how you interact with the terminal using your keyboard.</span></span>

## <a name="key-binding-formats"></a><span data-ttu-id="308c4-105">Formati di tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="308c4-105">Key binding formats</span></span>

<span data-ttu-id="308c4-106">I tasti di scelta rapida possono essere strutturati nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="308c4-106">Key bindings can be structured in the following formats:</span></span>

### <a name="commands-without-arguments"></a><span data-ttu-id="308c4-107">Comandi senza argomenti</span><span class="sxs-lookup"><span data-stu-id="308c4-107">Commands without arguments</span></span>

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

<span data-ttu-id="308c4-108">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>alt+f4</kbd> per chiudere la finestra del terminale:</span><span class="sxs-lookup"><span data-stu-id="308c4-108">For example, this default setting uses the shortcut key <kbd>alt+f4</kbd> to close the terminal window:</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a><span data-ttu-id="308c4-109">Comandi con argomenti</span><span class="sxs-lookup"><span data-stu-id="308c4-109">Commands with arguments</span></span>

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

<span data-ttu-id="308c4-110">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>ctrl+maiusc+1</kbd> per aprire una nuova scheda nel terminale in base al profilo elencato per primo nel menu a discesa (in genere verrà aperto il profilo PowerShell):</span><span class="sxs-lookup"><span data-stu-id="308c4-110">For example, this default setting uses the shortcut key <kbd>ctrl+shift+1</kbd> to open a new tab in the terminal based on whichever profile is listed first in your dropdown menu (typically this will open the PowerShell profile):</span></span>

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="key-binding-properties"></a><span data-ttu-id="308c4-111">Proprietà dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="308c4-111">Key binding properties</span></span>

<span data-ttu-id="308c4-112">È possibile creare tasti di scelta rapida usando le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="308c4-112">Key bindings can be constructed using the following properties.</span></span>

### <a name="command"></a><span data-ttu-id="308c4-113">Comando</span><span class="sxs-lookup"><span data-stu-id="308c4-113">Command</span></span>

<span data-ttu-id="308c4-114">Comando eseguito quando vengono premuti i tasti associati.</span><span class="sxs-lookup"><span data-stu-id="308c4-114">This is the command executed when the associated keys are pressed.</span></span>

<span data-ttu-id="308c4-115">**Nome della proprietà:** `command`</span><span class="sxs-lookup"><span data-stu-id="308c4-115">**Property name:** `command`</span></span>

<span data-ttu-id="308c4-116">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-116">**Necessity:** Required</span></span>

<span data-ttu-id="308c4-117">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="308c4-117">**Accepts:** String</span></span>

### <a name="keys"></a><span data-ttu-id="308c4-118">Tasti</span><span class="sxs-lookup"><span data-stu-id="308c4-118">Keys</span></span>

<span data-ttu-id="308c4-119">Definisce le combinazioni di tasti usate per chiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="308c4-119">This defines the key combinations used to call the command.</span></span> <span data-ttu-id="308c4-120">Con la proprietà keys è possibile associare più modificatori a un unico tasto.</span><span class="sxs-lookup"><span data-stu-id="308c4-120">Keys can have any number of modifiers with one key.</span></span> <span data-ttu-id="308c4-121">I tasti e i modificatori accettati sono elencati [di seguito](#accepted-modifiers-and-keys).</span><span class="sxs-lookup"><span data-stu-id="308c4-121">Accepted modifiers and keys are listed [below](#accepted-modifiers-and-keys).</span></span>

<span data-ttu-id="308c4-122">**Nome della proprietà:** `keys`</span><span class="sxs-lookup"><span data-stu-id="308c4-122">**Property name:** `keys`</span></span>

<span data-ttu-id="308c4-123">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-123">**Necessity:** Required</span></span>

<span data-ttu-id="308c4-124">**Accetta:** stringa o matrice[stringa]</span><span class="sxs-lookup"><span data-stu-id="308c4-124">**Accepts:** String or array[string]</span></span>

### <a name="action"></a><span data-ttu-id="308c4-125">Azione</span><span class="sxs-lookup"><span data-stu-id="308c4-125">Action</span></span>

<span data-ttu-id="308c4-126">Aggiunge funzionalità aggiuntive a determinati comandi.</span><span class="sxs-lookup"><span data-stu-id="308c4-126">This adds additional functionality to certain commands.</span></span>

<span data-ttu-id="308c4-127">**Nome della proprietà:** `action`</span><span class="sxs-lookup"><span data-stu-id="308c4-127">**Property name:** `action`</span></span>

<span data-ttu-id="308c4-128">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-128">**Necessity:** Optional</span></span>

<span data-ttu-id="308c4-129">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="308c4-129">**Accepts:** String</span></span>

<br />

___

## <a name="accepted-modifiers-and-keys"></a><span data-ttu-id="308c4-130">Tasti e modificatori accettati</span><span class="sxs-lookup"><span data-stu-id="308c4-130">Accepted modifiers and keys</span></span>

### <a name="modifiers"></a><span data-ttu-id="308c4-131">Modificatori</span><span class="sxs-lookup"><span data-stu-id="308c4-131">Modifiers</span></span>

<span data-ttu-id="308c4-132">`ctrl+`, `shift+`, `alt+`</span><span class="sxs-lookup"><span data-stu-id="308c4-132">`ctrl+`, `shift+`, `alt+`</span></span>

### <a name="modifier-keys"></a><span data-ttu-id="308c4-133">Tasti di modifica</span><span class="sxs-lookup"><span data-stu-id="308c4-133">Modifier keys</span></span>

| <span data-ttu-id="308c4-134">Type</span><span class="sxs-lookup"><span data-stu-id="308c4-134">Type</span></span> | <span data-ttu-id="308c4-135">Tasti</span><span class="sxs-lookup"><span data-stu-id="308c4-135">Keys</span></span> |
| ---- | ---- |
| <span data-ttu-id="308c4-136">Tasti funzione e alfanumerici</span><span class="sxs-lookup"><span data-stu-id="308c4-136">Function and alphanumeric keys</span></span> | <span data-ttu-id="308c4-137">`f1-f24`, `a-z`, `0-9`</span><span class="sxs-lookup"><span data-stu-id="308c4-137">`f1-f24`, `a-z`, `0-9`</span></span> |
| <span data-ttu-id="308c4-138">Simboli</span><span class="sxs-lookup"><span data-stu-id="308c4-138">Symbols</span></span> | <span data-ttu-id="308c4-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span><span class="sxs-lookup"><span data-stu-id="308c4-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span></span> |
| <span data-ttu-id="308c4-140">Tasti di direzione</span><span class="sxs-lookup"><span data-stu-id="308c4-140">Arrow keys</span></span> | <span data-ttu-id="308c4-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span><span class="sxs-lookup"><span data-stu-id="308c4-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span></span> |
| <span data-ttu-id="308c4-142">Tasti di azione</span><span class="sxs-lookup"><span data-stu-id="308c4-142">Action keys</span></span> | <span data-ttu-id="308c4-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span><span class="sxs-lookup"><span data-stu-id="308c4-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span></span> |
| <span data-ttu-id="308c4-144">Tasti del tastierino numerico</span><span class="sxs-lookup"><span data-stu-id="308c4-144">Numpad keys</span></span> | <span data-ttu-id="308c4-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span><span class="sxs-lookup"><span data-stu-id="308c4-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span></span> |

<br />

___

## <a name="application-level-commands"></a><span data-ttu-id="308c4-146">Comandi a livello di applicazione</span><span class="sxs-lookup"><span data-stu-id="308c4-146">Application-level commands</span></span>

### <a name="close-window"></a><span data-ttu-id="308c4-147">Chiudi finestra</span><span class="sxs-lookup"><span data-stu-id="308c4-147">Close window</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="308c4-148">Chiude la finestra corrente e tutte le relative schede.</span><span class="sxs-lookup"><span data-stu-id="308c4-148">This closes the current window and all tabs within it.</span></span> <span data-ttu-id="308c4-149">Se `confirmCloseAllTabs` è impostato su `true`, verrà visualizzata una finestra di dialogo per confermare la chiusura di tutte le schede.</span><span class="sxs-lookup"><span data-stu-id="308c4-149">If `confirmCloseAllTabs` is set to `true`, a confirmation dialog will appear to ensure you'd like to close all your tabs.</span></span> <span data-ttu-id="308c4-150">Per altre informazioni su questa impostazione, vedi la [pagina delle impostazioni globali](./global-settings.md#hide-close-all-tabs-popup).</span><span class="sxs-lookup"><span data-stu-id="308c4-150">More information on this setting can be found on the [Global settings page](./global-settings.md#hide-close-all-tabs-popup).</span></span>

<span data-ttu-id="308c4-151">**Nome del comando:** `closeWindow`</span><span class="sxs-lookup"><span data-stu-id="308c4-151">**Command name:** `closeWindow`</span></span>

<span data-ttu-id="308c4-152">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-152">**Default binding:**</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a><span data-ttu-id="308c4-154">Trova</span><span class="sxs-lookup"><span data-stu-id="308c4-154">Find</span></span>

<span data-ttu-id="308c4-155">Apre la finestra di dialogo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="308c4-155">This opens the search dialog box.</span></span> <span data-ttu-id="308c4-156">Per altre informazioni sulla ricerca, vedi la [pagina relativa alla ricerca](./../search.md).</span><span class="sxs-lookup"><span data-stu-id="308c4-156">More information on search can be found on the [Search page](./../search.md).</span></span>

<span data-ttu-id="308c4-157">**Nome del comando:** `find`</span><span class="sxs-lookup"><span data-stu-id="308c4-157">**Command name:** `find`</span></span>

<span data-ttu-id="308c4-158">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-158">**Default binding:**</span></span>

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a><span data-ttu-id="308c4-159">Apri menu a discesa</span><span class="sxs-lookup"><span data-stu-id="308c4-159">Open the dropdown</span></span>

<span data-ttu-id="308c4-160">Apre il menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="308c4-160">This opens the dropdown menu.</span></span>

<span data-ttu-id="308c4-161">**Nome del comando:** `openNewTabDropdown`</span><span class="sxs-lookup"><span data-stu-id="308c4-161">**Command name:** `openNewTabDropdown`</span></span>

<span data-ttu-id="308c4-162">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-162">**Default binding:**</span></span>

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-files"></a><span data-ttu-id="308c4-163">Apri file di impostazioni</span><span class="sxs-lookup"><span data-stu-id="308c4-163">Open settings files</span></span>

<span data-ttu-id="308c4-164">Apre i file di impostazioni predefiniti o personalizzati.</span><span class="sxs-lookup"><span data-stu-id="308c4-164">This opens either the default or custom settings files.</span></span> <span data-ttu-id="308c4-165">Senza il campo `target` verrà aperto il file settings.json.</span><span class="sxs-lookup"><span data-stu-id="308c4-165">Without the `target` field, this will open the settings.json file.</span></span>

<span data-ttu-id="308c4-166">**Nome del comando:** `openSettings`</span><span class="sxs-lookup"><span data-stu-id="308c4-166">**Command name:** `openSettings`</span></span>

<span data-ttu-id="308c4-167">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-167">**Default binding:**</span></span>

```json
{ "command": "openSettings", "keys": "ctrl+," },
{ "command": { "action": "openSettings", "target": "defaultsFile" }, "keys": "ctrl+alt+," },
```

#### <a name="actions"></a><span data-ttu-id="308c4-168">Azioni</span><span class="sxs-lookup"><span data-stu-id="308c4-168">Actions</span></span>

| <span data-ttu-id="308c4-169">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-169">Name</span></span> | <span data-ttu-id="308c4-170">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-170">Necessity</span></span> | <span data-ttu-id="308c4-171">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-171">Accepts</span></span> | <span data-ttu-id="308c4-172">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-172">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `target` | <span data-ttu-id="308c4-173">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-173">Optional</span></span> | <span data-ttu-id="308c4-174">`"settingsFile"`, `"defaultsFile"`, `"allFiles"`</span><span class="sxs-lookup"><span data-stu-id="308c4-174">`"settingsFile"`, `"defaultsFile"`, `"allFiles"`</span></span> | <span data-ttu-id="308c4-175">Il file di impostazioni da aprire.</span><span class="sxs-lookup"><span data-stu-id="308c4-175">The settings file to open.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="308c4-176">Il campo `target` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="308c4-176">The `target` field is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="toggle-full-screen"></a><span data-ttu-id="308c4-177">Attiva/Disattiva schermo intero</span><span class="sxs-lookup"><span data-stu-id="308c4-177">Toggle full screen</span></span>

<span data-ttu-id="308c4-178">Consente di passare dalla finestra a schermo intero a quella con dimensioni predefinite e viceversa.</span><span class="sxs-lookup"><span data-stu-id="308c4-178">This allows you to switch between full screen and default window sizes.</span></span>

<span data-ttu-id="308c4-179">**Nome del comando:** `toggleFullscreen`</span><span class="sxs-lookup"><span data-stu-id="308c4-179">**Command name:** `toggleFullscreen`</span></span>

<span data-ttu-id="308c4-180">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-180">**Default bindings:**</span></span>

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

<br />

___

## <a name="tab-management-commands"></a><span data-ttu-id="308c4-181">Comandi per la gestione delle schede</span><span class="sxs-lookup"><span data-stu-id="308c4-181">Tab management commands</span></span>

### <a name="close-tab"></a><span data-ttu-id="308c4-182">Chiudi scheda</span><span class="sxs-lookup"><span data-stu-id="308c4-182">Close tab</span></span>

<span data-ttu-id="308c4-183">Chiude la scheda corrente.</span><span class="sxs-lookup"><span data-stu-id="308c4-183">This closes the current tab.</span></span>

<span data-ttu-id="308c4-184">**Nome del comando:** `closeTab`</span><span class="sxs-lookup"><span data-stu-id="308c4-184">**Command name:** `closeTab`</span></span>

### <a name="duplicate-tab"></a><span data-ttu-id="308c4-185">Duplica scheda</span><span class="sxs-lookup"><span data-stu-id="308c4-185">Duplicate tab</span></span>

<span data-ttu-id="308c4-186">Crea una copia della scheda corrente e la apre.</span><span class="sxs-lookup"><span data-stu-id="308c4-186">This makes a copy of the current tab and opens it.</span></span>

<span data-ttu-id="308c4-187">**Nome del comando:** `duplicateTab`</span><span class="sxs-lookup"><span data-stu-id="308c4-187">**Command name:** `duplicateTab`</span></span>

<span data-ttu-id="308c4-188">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-188">**Default binding:**</span></span>

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a><span data-ttu-id="308c4-189">Nuova scheda</span><span class="sxs-lookup"><span data-stu-id="308c4-189">New tab</span></span>

<span data-ttu-id="308c4-190">Crea una nuova scheda. Se viene specificato senza argomenti, il profilo predefinito verrà aperto in una nuova scheda. Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="308c4-190">This creates a new tab. Without any arguments, this will open the default profile in a new tab. If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="308c4-191">**Nome del comando:** `newTab`</span><span class="sxs-lookup"><span data-stu-id="308c4-191">**Command name:** `newTab`</span></span>

<span data-ttu-id="308c4-192">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-192">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="308c4-193">Azioni</span><span class="sxs-lookup"><span data-stu-id="308c4-193">Actions</span></span>

| <span data-ttu-id="308c4-194">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-194">Name</span></span> | <span data-ttu-id="308c4-195">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-195">Necessity</span></span> | <span data-ttu-id="308c4-196">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-196">Accepts</span></span> | <span data-ttu-id="308c4-197">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-197">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `commandLine` | <span data-ttu-id="308c4-198">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-198">Optional</span></span> | <span data-ttu-id="308c4-199">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="308c4-199">Executable file name as a string</span></span> | <span data-ttu-id="308c4-200">Esegue l'eseguibile all'interno della scheda.</span><span class="sxs-lookup"><span data-stu-id="308c4-200">Executable run within the tab.</span></span> |
| `startingDirectory` | <span data-ttu-id="308c4-201">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-201">Optional</span></span> | <span data-ttu-id="308c4-202">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="308c4-202">Folder location as a string</span></span> | <span data-ttu-id="308c4-203">Directory in cui verrà aperta la scheda.</span><span class="sxs-lookup"><span data-stu-id="308c4-203">Directory in which the tab will open.</span></span> |
| `tabTitle` | <span data-ttu-id="308c4-204">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-204">Optional</span></span> | <span data-ttu-id="308c4-205">String</span><span class="sxs-lookup"><span data-stu-id="308c4-205">String</span></span> | <span data-ttu-id="308c4-206">Titolo della nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="308c4-206">Title of the new tab.</span></span> |
| `index` | <span data-ttu-id="308c4-207">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-207">Optional</span></span> | <span data-ttu-id="308c4-208">Intero</span><span class="sxs-lookup"><span data-stu-id="308c4-208">Integer</span></span> | <span data-ttu-id="308c4-209">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="308c4-209">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="308c4-210">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-210">Optional</span></span> | <span data-ttu-id="308c4-211">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="308c4-211">Profile's name or GUID as a string</span></span> | <span data-ttu-id="308c4-212">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="308c4-212">Profile that will open based on its GUID or name.</span></span> |

### <a name="open-next-tab"></a><span data-ttu-id="308c4-213">Apri scheda successiva</span><span class="sxs-lookup"><span data-stu-id="308c4-213">Open next tab</span></span>

<span data-ttu-id="308c4-214">Apre la scheda a destra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="308c4-214">This opens the tab to the right of the current one.</span></span>

<span data-ttu-id="308c4-215">**Nome del comando:** `nextTab`</span><span class="sxs-lookup"><span data-stu-id="308c4-215">**Command name:** `nextTab`</span></span>

<span data-ttu-id="308c4-216">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-216">**Default binding:**</span></span>

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a><span data-ttu-id="308c4-217">Apri scheda precedente</span><span class="sxs-lookup"><span data-stu-id="308c4-217">Open previous tab</span></span>

<span data-ttu-id="308c4-218">Apre la scheda a sinistra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="308c4-218">This opens the tab to the left of the current one.</span></span>

<span data-ttu-id="308c4-219">**Nome del comando:** `prevTab`</span><span class="sxs-lookup"><span data-stu-id="308c4-219">**Command name:** `prevTab`</span></span>

<span data-ttu-id="308c4-220">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-220">**Default binding:**</span></span>

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="open-a-specific-tab"></a><span data-ttu-id="308c4-221">Apri una scheda specifica</span><span class="sxs-lookup"><span data-stu-id="308c4-221">Open a specific tab</span></span>

<span data-ttu-id="308c4-222">Apre una scheda specifica a seconda dell'indice.</span><span class="sxs-lookup"><span data-stu-id="308c4-222">This opens a specific tab depending on the index.</span></span>

<span data-ttu-id="308c4-223">**Nome del comando:** `switchToTab`</span><span class="sxs-lookup"><span data-stu-id="308c4-223">**Command name:** `switchToTab`</span></span>

<span data-ttu-id="308c4-224">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-224">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="308c4-225">Azioni</span><span class="sxs-lookup"><span data-stu-id="308c4-225">Actions</span></span>

| <span data-ttu-id="308c4-226">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-226">Name</span></span> | <span data-ttu-id="308c4-227">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-227">Necessity</span></span> | <span data-ttu-id="308c4-228">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-228">Accepts</span></span> | <span data-ttu-id="308c4-229">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-229">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="308c4-230">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-230">Required</span></span> | <span data-ttu-id="308c4-231">Intero</span><span class="sxs-lookup"><span data-stu-id="308c4-231">Integer</span></span> | <span data-ttu-id="308c4-232">Scheda che verrà aperta in base alla relativa posizione nella barra delle schede (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="308c4-232">Tab that will open based on its position in the tab bar (starting at 0).</span></span> |

<br />

___

## <a name="pane-management-commands"></a><span data-ttu-id="308c4-233">Comandi di gestione dei riquadri</span><span class="sxs-lookup"><span data-stu-id="308c4-233">Pane management commands</span></span>

### <a name="close-pane"></a><span data-ttu-id="308c4-234">Chiudi riquadro</span><span class="sxs-lookup"><span data-stu-id="308c4-234">Close pane</span></span>

<span data-ttu-id="308c4-235">Chiude il riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="308c4-235">This closes the active pane.</span></span> <span data-ttu-id="308c4-236">Se non sono presenti riquadri divisi, chiude la scheda corrente. Se è aperta una sola scheda, chiude la finestra.</span><span class="sxs-lookup"><span data-stu-id="308c4-236">If there aren't any split panes, this will close the current tab. If there is only one tab open, this will close the window.</span></span>

<span data-ttu-id="308c4-237">**Nome del comando:** `closePane`</span><span class="sxs-lookup"><span data-stu-id="308c4-237">**Command name:** `closePane`</span></span>

<span data-ttu-id="308c4-238">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-238">**Default binding:**</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a><span data-ttu-id="308c4-239">Sposta stato attivo nel riquadro</span><span class="sxs-lookup"><span data-stu-id="308c4-239">Move pane focus</span></span>

<span data-ttu-id="308c4-240">Consente di spostare lo stato attivo in un altro riquadro a seconda della direzione.</span><span class="sxs-lookup"><span data-stu-id="308c4-240">This changes focus to a different pane depending on the direction.</span></span>

<span data-ttu-id="308c4-241">**Nome del comando:** `moveFocus`</span><span class="sxs-lookup"><span data-stu-id="308c4-241">**Command name:** `moveFocus`</span></span>

<span data-ttu-id="308c4-242">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-242">**Default bindings:**</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

#### <a name="actions"></a><span data-ttu-id="308c4-243">Azioni</span><span class="sxs-lookup"><span data-stu-id="308c4-243">Actions</span></span>

| <span data-ttu-id="308c4-244">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-244">Name</span></span> | <span data-ttu-id="308c4-245">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-245">Necessity</span></span> | <span data-ttu-id="308c4-246">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-246">Accepts</span></span> | <span data-ttu-id="308c4-247">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-247">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="308c4-248">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-248">Required</span></span> | <span data-ttu-id="308c4-249">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="308c4-249">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="308c4-250">Direzione in cui viene spostato lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="308c4-250">Direction in which the focus will move.</span></span> |

### <a name="resize-a-pane"></a><span data-ttu-id="308c4-251">Ridimensiona un riquadro</span><span class="sxs-lookup"><span data-stu-id="308c4-251">Resize a pane</span></span>

<span data-ttu-id="308c4-252">Modifica le dimensioni del riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="308c4-252">This changes the size of the active pane.</span></span>

<span data-ttu-id="308c4-253">**Nome del comando:** `resizePane`</span><span class="sxs-lookup"><span data-stu-id="308c4-253">**Command name:** `resizePane`</span></span>

<span data-ttu-id="308c4-254">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-254">**Default bindings:**</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="308c4-255">Azioni</span><span class="sxs-lookup"><span data-stu-id="308c4-255">Actions</span></span>

| <span data-ttu-id="308c4-256">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-256">Name</span></span> | <span data-ttu-id="308c4-257">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-257">Necessity</span></span> | <span data-ttu-id="308c4-258">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-258">Accepts</span></span> | <span data-ttu-id="308c4-259">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-259">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="308c4-260">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-260">Required</span></span> | <span data-ttu-id="308c4-261">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="308c4-261">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="308c4-262">Direzione in cui verranno modificate le dimensioni del riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-262">Direction in which the pane will be resized.</span></span> |

### <a name="split-a-pane"></a><span data-ttu-id="308c4-263">Dividi un riquadro</span><span class="sxs-lookup"><span data-stu-id="308c4-263">Split a pane</span></span>

<span data-ttu-id="308c4-264">Divide a metà il riquadro attivo e ne apre un altro.</span><span class="sxs-lookup"><span data-stu-id="308c4-264">This halves the size of the active pane and opens another.</span></span> <span data-ttu-id="308c4-265">Se viene specificato senza argomenti, il profilo predefinito verrà aperto nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-265">Without any arguments, this will open the default profile in the new pane.</span></span> <span data-ttu-id="308c4-266">Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="308c4-266">If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="308c4-267">**Nome del comando:** `splitPane`</span><span class="sxs-lookup"><span data-stu-id="308c4-267">**Command name:** `splitPane`</span></span>

<span data-ttu-id="308c4-268">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-268">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal"}, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical"}, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a><span data-ttu-id="308c4-269">Azioni</span><span class="sxs-lookup"><span data-stu-id="308c4-269">Actions</span></span>

| <span data-ttu-id="308c4-270">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-270">Name</span></span> | <span data-ttu-id="308c4-271">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-271">Necessity</span></span> | <span data-ttu-id="308c4-272">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-272">Accepts</span></span> | <span data-ttu-id="308c4-273">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-273">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `split` | <span data-ttu-id="308c4-274">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-274">Required</span></span> | <span data-ttu-id="308c4-275">`"vertical"`, `"horizontal"`, `"auto"`</span><span class="sxs-lookup"><span data-stu-id="308c4-275">`"vertical"`, `"horizontal"`, `"auto"`</span></span> | <span data-ttu-id="308c4-276">Modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-276">How the pane will split.</span></span> <span data-ttu-id="308c4-277">Con `"auto"` il riquadro verrà diviso nella direzione che offre l'area con la superficie più estesa.</span><span class="sxs-lookup"><span data-stu-id="308c4-277">`"auto"` will split in the direction that provides the most surface area.</span></span> |
| `commandLine` | <span data-ttu-id="308c4-278">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-278">Optional</span></span> | <span data-ttu-id="308c4-279">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="308c4-279">Executable file name as a string</span></span> | <span data-ttu-id="308c4-280">Esegue l'eseguibile all'interno del riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-280">Executable run within the pane.</span></span> |
| `startingDirectory` | <span data-ttu-id="308c4-281">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-281">Optional</span></span> | <span data-ttu-id="308c4-282">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="308c4-282">Folder location as a string</span></span> | <span data-ttu-id="308c4-283">Directory in cui verrà aperto il riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-283">Directory in which the pane will open.</span></span> |
| `tabTitle` | <span data-ttu-id="308c4-284">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-284">Optional</span></span> | <span data-ttu-id="308c4-285">String</span><span class="sxs-lookup"><span data-stu-id="308c4-285">String</span></span> | <span data-ttu-id="308c4-286">Titolo della scheda quando lo stato attivo si trova nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-286">Title of the tab when the new pane is focused.</span></span> |
| `index` | <span data-ttu-id="308c4-287">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-287">Optional</span></span> | <span data-ttu-id="308c4-288">Intero</span><span class="sxs-lookup"><span data-stu-id="308c4-288">Integer</span></span> | <span data-ttu-id="308c4-289">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="308c4-289">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="308c4-290">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-290">Optional</span></span> | <span data-ttu-id="308c4-291">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="308c4-291">Profile's name or GUID as a string</span></span> | <span data-ttu-id="308c4-292">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="308c4-292">Profile that will open based on its GUID or name.</span></span> |
| `splitMode` | <span data-ttu-id="308c4-293">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-293">Optional</span></span> | `"duplicate"` | <span data-ttu-id="308c4-294">Controlla la modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-294">Controls how the pane splits.</span></span> <span data-ttu-id="308c4-295">Accetta solo `"duplicate"`, con cui il profilo del riquadro con lo stato attivo viene duplicato in un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="308c4-295">Only accepts `"duplicate"`, which will duplicate the focused pane's profile into a new pane.</span></span> |

<br />

___

## <a name="clipboard-integration-commands"></a><span data-ttu-id="308c4-296">Comandi di integrazione degli Appunti</span><span class="sxs-lookup"><span data-stu-id="308c4-296">Clipboard integration commands</span></span>

### <a name="copy"></a><span data-ttu-id="308c4-297">Copia</span><span class="sxs-lookup"><span data-stu-id="308c4-297">Copy</span></span>

<span data-ttu-id="308c4-298">Copia il contenuto del terminale selezionato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="308c4-298">This copies the selected terminal content to your clipboard.</span></span>

<span data-ttu-id="308c4-299">**Nome del comando:** `copy`</span><span class="sxs-lookup"><span data-stu-id="308c4-299">**Command name:** `copy`</span></span>

<span data-ttu-id="308c4-300">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-300">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="clipboard-actions"></a><span data-ttu-id="308c4-301">Azioni degli Appunti</span><span class="sxs-lookup"><span data-stu-id="308c4-301">Clipboard Actions</span></span>

| <span data-ttu-id="308c4-302">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-302">Name</span></span> | <span data-ttu-id="308c4-303">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-303">Necessity</span></span> | <span data-ttu-id="308c4-304">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-304">Accepts</span></span> | <span data-ttu-id="308c4-305">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-305">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `singleLine` | <span data-ttu-id="308c4-306">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="308c4-306">Optional</span></span> | <span data-ttu-id="308c4-307">`true`, `false`</span><span class="sxs-lookup"><span data-stu-id="308c4-307">`true`, `false`</span></span> | <span data-ttu-id="308c4-308">Quando è `true`, il contenuto copiato verrà copiato come una riga singola.</span><span class="sxs-lookup"><span data-stu-id="308c4-308">When `true`, the copied content will be copied as a single line.</span></span> <span data-ttu-id="308c4-309">Quando è `false`, i caratteri di nuova riga del testo selezionato vengono mantenuti.</span><span class="sxs-lookup"><span data-stu-id="308c4-309">When `false`, newlines persist from the selected text.</span></span> |

### <a name="paste"></a><span data-ttu-id="308c4-310">Incolla</span><span class="sxs-lookup"><span data-stu-id="308c4-310">Paste</span></span>

<span data-ttu-id="308c4-311">Inserisce il contenuto copiato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="308c4-311">This inserts the content that was copied onto the clipboard.</span></span>

<span data-ttu-id="308c4-312">**Nome del comando:** `paste`</span><span class="sxs-lookup"><span data-stu-id="308c4-312">**Command name:** `paste`</span></span>

<span data-ttu-id="308c4-313">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-313">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a><span data-ttu-id="308c4-314">Comandi di scorrimento</span><span class="sxs-lookup"><span data-stu-id="308c4-314">Scrollback commands</span></span>

### <a name="scroll-up"></a><span data-ttu-id="308c4-315">Scorri verso l'alto</span><span class="sxs-lookup"><span data-stu-id="308c4-315">Scroll up</span></span>

<span data-ttu-id="308c4-316">Scorre lo schermo verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="308c4-316">This scrolls the screen up.</span></span>

<span data-ttu-id="308c4-317">**Nome del comando:** `scrollUp`</span><span class="sxs-lookup"><span data-stu-id="308c4-317">**Command name:** `scrollUp`</span></span>

<span data-ttu-id="308c4-318">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-318">**Default binding:**</span></span>

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

### <a name="scroll-down"></a><span data-ttu-id="308c4-319">Scorri verso il basso</span><span class="sxs-lookup"><span data-stu-id="308c4-319">Scroll down</span></span>

<span data-ttu-id="308c4-320">Scorre lo schermo verso il basso.</span><span class="sxs-lookup"><span data-stu-id="308c4-320">This scrolls the screen down.</span></span>

<span data-ttu-id="308c4-321">**Nome del comando:** `scrollDown`</span><span class="sxs-lookup"><span data-stu-id="308c4-321">**Command name:** `scrollDown`</span></span>

<span data-ttu-id="308c4-322">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-322">**Default binding:**</span></span>

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

### <a name="scroll-up-a-whole-page"></a><span data-ttu-id="308c4-323">Scorri verso l'alto di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="308c4-323">Scroll up a whole page</span></span>

<span data-ttu-id="308c4-324">Scorre lo schermo verso l'alto di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="308c4-324">This scrolls the screen up by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="308c4-325">**Nome del comando:** `scrollUpPage`</span><span class="sxs-lookup"><span data-stu-id="308c4-325">**Command name:** `scrollUpPage`</span></span>

<span data-ttu-id="308c4-326">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-326">**Default binding:**</span></span>

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a><span data-ttu-id="308c4-327">Scorri verso il basso di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="308c4-327">Scroll down a whole page</span></span>

<span data-ttu-id="308c4-328">Scorre lo schermo verso il basso di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="308c4-328">This scrolls the screen down by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="308c4-329">**Nome del comando:** `scrollDownPage`</span><span class="sxs-lookup"><span data-stu-id="308c4-329">**Command name:** `scrollDownPage`</span></span>

<span data-ttu-id="308c4-330">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-330">**Default binding:**</span></span>

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

<br />

___

## <a name="visual-adjustment-commands"></a><span data-ttu-id="308c4-331">Comandi di regolazione della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="308c4-331">Visual adjustment commands</span></span>

### <a name="adjust-font-size"></a><span data-ttu-id="308c4-332">Regola dimensioni caratteri</span><span class="sxs-lookup"><span data-stu-id="308c4-332">Adjust font size</span></span>

<span data-ttu-id="308c4-333">Modifica le dimensioni del testo in base al numero di punti specificato.</span><span class="sxs-lookup"><span data-stu-id="308c4-333">This changes the text size by a specified point amount.</span></span>

<span data-ttu-id="308c4-334">**Nome del comando:** `adjustFontSize`</span><span class="sxs-lookup"><span data-stu-id="308c4-334">**Command name:** `adjustFontSize`</span></span>

<span data-ttu-id="308c4-335">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="308c4-335">**Default bindings:**</span></span>

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a><span data-ttu-id="308c4-336">Azioni</span><span class="sxs-lookup"><span data-stu-id="308c4-336">Actions</span></span>

| <span data-ttu-id="308c4-337">Nome</span><span class="sxs-lookup"><span data-stu-id="308c4-337">Name</span></span> | <span data-ttu-id="308c4-338">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-338">Necessity</span></span> | <span data-ttu-id="308c4-339">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="308c4-339">Accepts</span></span> | <span data-ttu-id="308c4-340">Description</span><span class="sxs-lookup"><span data-stu-id="308c4-340">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `delta` | <span data-ttu-id="308c4-341">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="308c4-341">Required</span></span> | <span data-ttu-id="308c4-342">Intero</span><span class="sxs-lookup"><span data-stu-id="308c4-342">Integer</span></span> | <span data-ttu-id="308c4-343">Modifiche applicate alle dimensioni per ogni chiamata del comando.</span><span class="sxs-lookup"><span data-stu-id="308c4-343">Amount of size change per command invocation.</span></span> |

### <a name="reset-font-size"></a><span data-ttu-id="308c4-344">Reimposta dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="308c4-344">Reset font size</span></span>

<span data-ttu-id="308c4-345">Reimposta le dimensioni del testo in base al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="308c4-345">This resets the text size to the default value.</span></span>

<span data-ttu-id="308c4-346">**Nome del comando:** `resetFontSize`</span><span class="sxs-lookup"><span data-stu-id="308c4-346">**Command name:** `resetFontSize`</span></span>

<span data-ttu-id="308c4-347">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="308c4-347">**Default binding:**</span></span>

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

<br />

___

## <a name="unbind-keys"></a><span data-ttu-id="308c4-348">Disassocia tasti</span><span class="sxs-lookup"><span data-stu-id="308c4-348">Unbind keys</span></span>

<span data-ttu-id="308c4-349">Annulla l'associazione dei tasti per tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="308c4-349">This unbinds the associated keys from any command.</span></span>

<span data-ttu-id="308c4-350">**Nome del comando:** `unbound`</span><span class="sxs-lookup"><span data-stu-id="308c4-350">**Command name:** `unbound`</span></span>
