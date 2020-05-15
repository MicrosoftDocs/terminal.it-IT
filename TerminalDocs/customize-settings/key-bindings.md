---
title: Terminale Windows - Tasti di scelta rapida
description: Informazioni su come creare tasti di scelta rapida personalizzati per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 76bf91f8d7c2b49c2dc6bcf0c83640b57b2acd01
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415966"
---
# <a name="custom-key-bindings-in-windows-terminal"></a><span data-ttu-id="b3fcc-103">Tasti di scelta rapida personalizzati in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="b3fcc-103">Custom key bindings in Windows Terminal</span></span>

<span data-ttu-id="b3fcc-104">In Terminale Windows puoi creare tasti di scelta rapida personalizzati per controllare l'interazione con il terminale tramite la tastiera.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-104">You can create custom key bindings (keyboard shortcuts) inside the Windows Terminal that give you control of how you interact with the terminal using your keyboard.</span></span>

## <a name="key-binding-formats"></a><span data-ttu-id="b3fcc-105">Formati di tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="b3fcc-105">Key binding formats</span></span>

<span data-ttu-id="b3fcc-106">I tasti di scelta rapida possono essere strutturati nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3fcc-106">Key bindings can be structured in the following formats:</span></span>

### <a name="commands-without-arguments"></a><span data-ttu-id="b3fcc-107">Comandi senza argomenti</span><span class="sxs-lookup"><span data-stu-id="b3fcc-107">Commands without arguments</span></span>

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

<span data-ttu-id="b3fcc-108">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>alt+f4</kbd> per chiudere la finestra del terminale:</span><span class="sxs-lookup"><span data-stu-id="b3fcc-108">For example, this default setting uses the shortcut key <kbd>alt+f4</kbd> to close the terminal window:</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a><span data-ttu-id="b3fcc-109">Comandi con argomenti</span><span class="sxs-lookup"><span data-stu-id="b3fcc-109">Commands with arguments</span></span>

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

<span data-ttu-id="b3fcc-110">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>ctrl+maiusc+1</kbd> per aprire una nuova scheda nel terminale in base al profilo elencato per primo nel menu a discesa (in genere verrà aperto il profilo PowerShell):</span><span class="sxs-lookup"><span data-stu-id="b3fcc-110">For example, this default setting uses the shortcut key <kbd>ctrl+shift+1</kbd> to open a new tab in the terminal based on whichever profile is listed first in your dropdown menu (typically this will open the PowerShell profile):</span></span>

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="key-binding-properties"></a><span data-ttu-id="b3fcc-111">Proprietà dei tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="b3fcc-111">Key binding properties</span></span>

<span data-ttu-id="b3fcc-112">È possibile creare tasti di scelta rapida usando le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-112">Key bindings can be constructed using the following properties.</span></span>

### <a name="command"></a><span data-ttu-id="b3fcc-113">Comando</span><span class="sxs-lookup"><span data-stu-id="b3fcc-113">Command</span></span>

<span data-ttu-id="b3fcc-114">Comando eseguito quando vengono premuti i tasti associati.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-114">This is the command executed when the associated keys are pressed.</span></span>

<span data-ttu-id="b3fcc-115">**Nome della proprietà:** `command`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-115">**Property name:** `command`</span></span>

<span data-ttu-id="b3fcc-116">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-116">**Necessity:** Required</span></span>

<span data-ttu-id="b3fcc-117">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="b3fcc-117">**Accepts:** String</span></span>

### <a name="keys"></a><span data-ttu-id="b3fcc-118">Tasti</span><span class="sxs-lookup"><span data-stu-id="b3fcc-118">Keys</span></span>

<span data-ttu-id="b3fcc-119">Definisce le combinazioni di tasti usate per chiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-119">This defines the key combinations used to call the command.</span></span> <span data-ttu-id="b3fcc-120">Con la proprietà keys è possibile associare più modificatori a un unico tasto.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-120">Keys can have any number of modifiers with one key.</span></span> <span data-ttu-id="b3fcc-121">I tasti e i modificatori accettati sono elencati [di seguito](#accepted-modifiers-and-keys).</span><span class="sxs-lookup"><span data-stu-id="b3fcc-121">Accepted modifiers and keys are listed [below](#accepted-modifiers-and-keys).</span></span>

<span data-ttu-id="b3fcc-122">**Nome della proprietà:** `keys`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-122">**Property name:** `keys`</span></span>

<span data-ttu-id="b3fcc-123">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-123">**Necessity:** Required</span></span>

<span data-ttu-id="b3fcc-124">**Accetta:** stringa o matrice[stringa]</span><span class="sxs-lookup"><span data-stu-id="b3fcc-124">**Accepts:** String or array[string]</span></span>

### <a name="action"></a><span data-ttu-id="b3fcc-125">Azione</span><span class="sxs-lookup"><span data-stu-id="b3fcc-125">Action</span></span>

<span data-ttu-id="b3fcc-126">Aggiunge funzionalità aggiuntive a determinati comandi.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-126">This adds additional functionality to certain commands.</span></span>

<span data-ttu-id="b3fcc-127">**Nome della proprietà:** `action`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-127">**Property name:** `action`</span></span>

<span data-ttu-id="b3fcc-128">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-128">**Necessity:** Optional</span></span>

<span data-ttu-id="b3fcc-129">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="b3fcc-129">**Accepts:** String</span></span>

<br />

___

## <a name="accepted-modifiers-and-keys"></a><span data-ttu-id="b3fcc-130">Tasti e modificatori accettati</span><span class="sxs-lookup"><span data-stu-id="b3fcc-130">Accepted modifiers and keys</span></span>

### <a name="modifiers"></a><span data-ttu-id="b3fcc-131">Modificatori</span><span class="sxs-lookup"><span data-stu-id="b3fcc-131">Modifiers</span></span>

<span data-ttu-id="b3fcc-132">`ctrl+`, `shift+`, `alt+`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-132">`ctrl+`, `shift+`, `alt+`</span></span>

### <a name="modifier-keys"></a><span data-ttu-id="b3fcc-133">Tasti di modifica</span><span class="sxs-lookup"><span data-stu-id="b3fcc-133">Modifier keys</span></span>

| <span data-ttu-id="b3fcc-134">Type</span><span class="sxs-lookup"><span data-stu-id="b3fcc-134">Type</span></span> | <span data-ttu-id="b3fcc-135">Tasti</span><span class="sxs-lookup"><span data-stu-id="b3fcc-135">Keys</span></span> |
| ---- | ---- |
| <span data-ttu-id="b3fcc-136">Tasti funzione e alfanumerici</span><span class="sxs-lookup"><span data-stu-id="b3fcc-136">Function and alphanumeric keys</span></span> | <span data-ttu-id="b3fcc-137">`f1-f24`, `a-z`, `0-9`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-137">`f1-f24`, `a-z`, `0-9`</span></span> |
| <span data-ttu-id="b3fcc-138">Simboli</span><span class="sxs-lookup"><span data-stu-id="b3fcc-138">Symbols</span></span> | <span data-ttu-id="b3fcc-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span></span> |
| <span data-ttu-id="b3fcc-140">Tasti di direzione</span><span class="sxs-lookup"><span data-stu-id="b3fcc-140">Arrow keys</span></span> | <span data-ttu-id="b3fcc-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span></span> |
| <span data-ttu-id="b3fcc-142">Tasti di azione</span><span class="sxs-lookup"><span data-stu-id="b3fcc-142">Action keys</span></span> | <span data-ttu-id="b3fcc-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span></span> |
| <span data-ttu-id="b3fcc-144">Tasti del tastierino numerico</span><span class="sxs-lookup"><span data-stu-id="b3fcc-144">Numpad keys</span></span> | <span data-ttu-id="b3fcc-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span></span> |

<br />

___

## <a name="application-level-commands"></a><span data-ttu-id="b3fcc-146">Comandi a livello di applicazione</span><span class="sxs-lookup"><span data-stu-id="b3fcc-146">Application-level commands</span></span>

### <a name="close-window"></a><span data-ttu-id="b3fcc-147">Chiudi finestra</span><span class="sxs-lookup"><span data-stu-id="b3fcc-147">Close window</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="b3fcc-148">Chiude la finestra corrente e tutte le relative schede.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-148">This closes the current window and all tabs within it.</span></span> <span data-ttu-id="b3fcc-149">Se `confirmCloseAllTabs` è impostato su `true`, verrà visualizzata una finestra di dialogo per confermare la chiusura di tutte le schede.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-149">If `confirmCloseAllTabs` is set to `true`, a confirmation dialog will appear to ensure you'd like to close all your tabs.</span></span> <span data-ttu-id="b3fcc-150">Per altre informazioni su questa impostazione, vedi la [pagina delle impostazioni globali](./global-settings.md#hide-close-all-tabs-popup).</span><span class="sxs-lookup"><span data-stu-id="b3fcc-150">More information on this setting can be found on the [Global settings page](./global-settings.md#hide-close-all-tabs-popup).</span></span>

<span data-ttu-id="b3fcc-151">**Nome del comando:** `closeWindow`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-151">**Command name:** `closeWindow`</span></span>

<span data-ttu-id="b3fcc-152">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-152">**Default binding:**</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a><span data-ttu-id="b3fcc-154">Trova</span><span class="sxs-lookup"><span data-stu-id="b3fcc-154">Find</span></span>

<span data-ttu-id="b3fcc-155">Apre la finestra di dialogo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-155">This opens the search dialog box.</span></span> <span data-ttu-id="b3fcc-156">Per altre informazioni sulla ricerca, vedi la [pagina relativa alla ricerca](./../search.md).</span><span class="sxs-lookup"><span data-stu-id="b3fcc-156">More information on search can be found on the [Search page](./../search.md).</span></span>

<span data-ttu-id="b3fcc-157">**Nome del comando:** `find`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-157">**Command name:** `find`</span></span>

<span data-ttu-id="b3fcc-158">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-158">**Default binding:**</span></span>

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a><span data-ttu-id="b3fcc-159">Apri menu a discesa</span><span class="sxs-lookup"><span data-stu-id="b3fcc-159">Open the dropdown</span></span>

<span data-ttu-id="b3fcc-160">Apre il menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-160">This opens the dropdown menu.</span></span>

<span data-ttu-id="b3fcc-161">**Nome del comando:** `openNewTabDropdown`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-161">**Command name:** `openNewTabDropdown`</span></span>

<span data-ttu-id="b3fcc-162">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-162">**Default binding:**</span></span>

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-file"></a><span data-ttu-id="b3fcc-163">Apri file di impostazioni</span><span class="sxs-lookup"><span data-stu-id="b3fcc-163">Open settings file</span></span>

<span data-ttu-id="b3fcc-164">Apre il file settings.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-164">This opens the settings file.</span></span>

<span data-ttu-id="b3fcc-165">**Nome del comando:** `openSettings`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-165">**Command name:** `openSettings`</span></span>

<span data-ttu-id="b3fcc-166">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-166">**Default binding:**</span></span>

```json
{ "command": "openSettings", "keys": "ctrl+," }
```

### <a name="toggle-full-screen"></a><span data-ttu-id="b3fcc-167">Attiva/Disattiva schermo intero</span><span class="sxs-lookup"><span data-stu-id="b3fcc-167">Toggle full screen</span></span>

<span data-ttu-id="b3fcc-168">Consente di passare dalla finestra a schermo intero a quella con dimensioni predefinite e viceversa.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-168">This allows you to switch between full screen and default window sizes.</span></span>

<span data-ttu-id="b3fcc-169">**Nome del comando:** `toggleFullscreen`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-169">**Command name:** `toggleFullscreen`</span></span>

<span data-ttu-id="b3fcc-170">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-170">**Default bindings:**</span></span>

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

<br />

___

## <a name="tab-management-commands"></a><span data-ttu-id="b3fcc-171">Comandi per la gestione delle schede</span><span class="sxs-lookup"><span data-stu-id="b3fcc-171">Tab management commands</span></span>

### <a name="close-tab"></a><span data-ttu-id="b3fcc-172">Chiudi scheda</span><span class="sxs-lookup"><span data-stu-id="b3fcc-172">Close tab</span></span>

<span data-ttu-id="b3fcc-173">Chiude la scheda corrente.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-173">This closes the current tab.</span></span>

<span data-ttu-id="b3fcc-174">**Nome del comando:** `closeTab`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-174">**Command name:** `closeTab`</span></span>

### <a name="duplicate-tab"></a><span data-ttu-id="b3fcc-175">Duplica scheda</span><span class="sxs-lookup"><span data-stu-id="b3fcc-175">Duplicate tab</span></span>

<span data-ttu-id="b3fcc-176">Crea una copia della scheda corrente e la apre.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-176">This makes a copy of the current tab and opens it.</span></span>

<span data-ttu-id="b3fcc-177">**Nome del comando:** `duplicateTab`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-177">**Command name:** `duplicateTab`</span></span>

<span data-ttu-id="b3fcc-178">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-178">**Default binding:**</span></span>

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a><span data-ttu-id="b3fcc-179">Nuova scheda</span><span class="sxs-lookup"><span data-stu-id="b3fcc-179">New tab</span></span>

<span data-ttu-id="b3fcc-180">Crea una nuova scheda. Se viene specificato senza argomenti, il profilo predefinito verrà aperto in una nuova scheda. Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-180">This creates a new tab. Without any arguments, this will open the default profile in a new tab. If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="b3fcc-181">**Nome del comando:** `newTab`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-181">**Command name:** `newTab`</span></span>

<span data-ttu-id="b3fcc-182">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-182">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="b3fcc-183">Azioni</span><span class="sxs-lookup"><span data-stu-id="b3fcc-183">Actions</span></span>

| <span data-ttu-id="b3fcc-184">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fcc-184">Name</span></span> | <span data-ttu-id="b3fcc-185">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-185">Necessity</span></span> | <span data-ttu-id="b3fcc-186">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="b3fcc-186">Accepts</span></span> | <span data-ttu-id="b3fcc-187">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcc-187">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `commandLine` | <span data-ttu-id="b3fcc-188">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-188">Optional</span></span> | <span data-ttu-id="b3fcc-189">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="b3fcc-189">Executable file name as a string</span></span> | <span data-ttu-id="b3fcc-190">Esegue l'eseguibile all'interno della scheda.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-190">Executable run within the tab.</span></span> |
| `startingDirectory` | <span data-ttu-id="b3fcc-191">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-191">Optional</span></span> | <span data-ttu-id="b3fcc-192">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="b3fcc-192">Folder location as a string</span></span> | <span data-ttu-id="b3fcc-193">Directory in cui verrà aperta la scheda.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-193">Directory in which the tab will open.</span></span> |
| `tabTitle` | <span data-ttu-id="b3fcc-194">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-194">Optional</span></span> | <span data-ttu-id="b3fcc-195">String</span><span class="sxs-lookup"><span data-stu-id="b3fcc-195">String</span></span> | <span data-ttu-id="b3fcc-196">Titolo della nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-196">Title of the new tab.</span></span> |
| `index` | <span data-ttu-id="b3fcc-197">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-197">Optional</span></span> | <span data-ttu-id="b3fcc-198">Intero</span><span class="sxs-lookup"><span data-stu-id="b3fcc-198">Integer</span></span> | <span data-ttu-id="b3fcc-199">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="b3fcc-199">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="b3fcc-200">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-200">Optional</span></span> | <span data-ttu-id="b3fcc-201">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="b3fcc-201">Profile's name or GUID as a string</span></span> | <span data-ttu-id="b3fcc-202">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-202">Profile that will open based on its GUID or name.</span></span> |

### <a name="open-next-tab"></a><span data-ttu-id="b3fcc-203">Apri scheda successiva</span><span class="sxs-lookup"><span data-stu-id="b3fcc-203">Open next tab</span></span>

<span data-ttu-id="b3fcc-204">Apre la scheda a destra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-204">This opens the tab to the right of the current one.</span></span>

<span data-ttu-id="b3fcc-205">**Nome del comando:** `nextTab`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-205">**Command name:** `nextTab`</span></span>

<span data-ttu-id="b3fcc-206">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-206">**Default binding:**</span></span>

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a><span data-ttu-id="b3fcc-207">Apri scheda precedente</span><span class="sxs-lookup"><span data-stu-id="b3fcc-207">Open previous tab</span></span>

<span data-ttu-id="b3fcc-208">Apre la scheda a sinistra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-208">This opens the tab to the left of the current one.</span></span>

<span data-ttu-id="b3fcc-209">**Nome del comando:** `prevTab`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-209">**Command name:** `prevTab`</span></span>

<span data-ttu-id="b3fcc-210">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-210">**Default binding:**</span></span>

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="open-a-specific-tab"></a><span data-ttu-id="b3fcc-211">Apri una scheda specifica</span><span class="sxs-lookup"><span data-stu-id="b3fcc-211">Open a specific tab</span></span>

<span data-ttu-id="b3fcc-212">Apre una scheda specifica a seconda dell'indice.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-212">This opens a specific tab depending on the index.</span></span>

<span data-ttu-id="b3fcc-213">**Nome del comando:** `switchToTab`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-213">**Command name:** `switchToTab`</span></span>

<span data-ttu-id="b3fcc-214">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-214">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="b3fcc-215">Azioni</span><span class="sxs-lookup"><span data-stu-id="b3fcc-215">Actions</span></span>

| <span data-ttu-id="b3fcc-216">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fcc-216">Name</span></span> | <span data-ttu-id="b3fcc-217">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-217">Necessity</span></span> | <span data-ttu-id="b3fcc-218">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="b3fcc-218">Accepts</span></span> | <span data-ttu-id="b3fcc-219">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcc-219">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="b3fcc-220">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-220">Required</span></span> | <span data-ttu-id="b3fcc-221">Intero</span><span class="sxs-lookup"><span data-stu-id="b3fcc-221">Integer</span></span> | <span data-ttu-id="b3fcc-222">Scheda che verrà aperta in base alla relativa posizione nella barra delle schede (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="b3fcc-222">Tab that will open based on its position in the tab bar (starting at 0).</span></span> |

<br />

___

## <a name="pane-management-commands"></a><span data-ttu-id="b3fcc-223">Comandi di gestione dei riquadri</span><span class="sxs-lookup"><span data-stu-id="b3fcc-223">Pane management commands</span></span>

### <a name="close-pane"></a><span data-ttu-id="b3fcc-224">Chiudi riquadro</span><span class="sxs-lookup"><span data-stu-id="b3fcc-224">Close pane</span></span>

<span data-ttu-id="b3fcc-225">Chiude il riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-225">This closes the active pane.</span></span> <span data-ttu-id="b3fcc-226">Se non sono presenti riquadri divisi, chiude la scheda corrente. Se è aperta una sola scheda, chiude la finestra.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-226">If there aren't any split panes, this will close the current tab. If there is only one tab open, this will close the window.</span></span>

<span data-ttu-id="b3fcc-227">**Nome del comando:** `closePane`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-227">**Command name:** `closePane`</span></span>

<span data-ttu-id="b3fcc-228">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-228">**Default binding:**</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a><span data-ttu-id="b3fcc-229">Sposta stato attivo nel riquadro</span><span class="sxs-lookup"><span data-stu-id="b3fcc-229">Move pane focus</span></span>

<span data-ttu-id="b3fcc-230">Consente di spostare lo stato attivo in un altro riquadro a seconda della direzione.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-230">This changes focus to a different pane depending on the direction.</span></span>

<span data-ttu-id="b3fcc-231">**Nome del comando:** `moveFocus`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-231">**Command name:** `moveFocus`</span></span>

<span data-ttu-id="b3fcc-232">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-232">**Default bindings:**</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

#### <a name="actions"></a><span data-ttu-id="b3fcc-233">Azioni</span><span class="sxs-lookup"><span data-stu-id="b3fcc-233">Actions</span></span>

| <span data-ttu-id="b3fcc-234">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fcc-234">Name</span></span> | <span data-ttu-id="b3fcc-235">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-235">Necessity</span></span> | <span data-ttu-id="b3fcc-236">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="b3fcc-236">Accepts</span></span> | <span data-ttu-id="b3fcc-237">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcc-237">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="b3fcc-238">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-238">Required</span></span> | <span data-ttu-id="b3fcc-239">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-239">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="b3fcc-240">Direzione in cui viene spostato lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-240">Direction in which the focus will move.</span></span> |

### <a name="resize-a-pane"></a><span data-ttu-id="b3fcc-241">Ridimensiona un riquadro</span><span class="sxs-lookup"><span data-stu-id="b3fcc-241">Resize a pane</span></span>

<span data-ttu-id="b3fcc-242">Modifica le dimensioni del riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-242">This changes the size of the active pane.</span></span>

<span data-ttu-id="b3fcc-243">**Nome del comando:** `resizePane`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-243">**Command name:** `resizePane`</span></span>

<span data-ttu-id="b3fcc-244">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-244">**Default bindings:**</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="b3fcc-245">Azioni</span><span class="sxs-lookup"><span data-stu-id="b3fcc-245">Actions</span></span>

| <span data-ttu-id="b3fcc-246">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fcc-246">Name</span></span> | <span data-ttu-id="b3fcc-247">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-247">Necessity</span></span> | <span data-ttu-id="b3fcc-248">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="b3fcc-248">Accepts</span></span> | <span data-ttu-id="b3fcc-249">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcc-249">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="b3fcc-250">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-250">Required</span></span> | <span data-ttu-id="b3fcc-251">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-251">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="b3fcc-252">Direzione in cui verranno modificate le dimensioni del riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-252">Direction in which the pane will be resized.</span></span> |

### <a name="split-a-pane"></a><span data-ttu-id="b3fcc-253">Dividi un riquadro</span><span class="sxs-lookup"><span data-stu-id="b3fcc-253">Split a pane</span></span>

<span data-ttu-id="b3fcc-254">Divide a metà il riquadro attivo e ne apre un altro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-254">This halves the size of the active pane and opens another.</span></span> <span data-ttu-id="b3fcc-255">Se viene specificato senza argomenti, il profilo predefinito verrà aperto nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-255">Without any arguments, this will open the default profile in the new pane.</span></span> <span data-ttu-id="b3fcc-256">Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-256">If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="b3fcc-257">**Nome del comando:** `splitPane`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-257">**Command name:** `splitPane`</span></span>

<span data-ttu-id="b3fcc-258">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-258">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal"}, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical"}, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a><span data-ttu-id="b3fcc-259">Azioni</span><span class="sxs-lookup"><span data-stu-id="b3fcc-259">Actions</span></span>

| <span data-ttu-id="b3fcc-260">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fcc-260">Name</span></span> | <span data-ttu-id="b3fcc-261">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-261">Necessity</span></span> | <span data-ttu-id="b3fcc-262">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="b3fcc-262">Accepts</span></span> | <span data-ttu-id="b3fcc-263">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcc-263">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `split` | <span data-ttu-id="b3fcc-264">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-264">Required</span></span> | <span data-ttu-id="b3fcc-265">`"vertical"`, `"horizontal"`, `"auto"`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-265">`"vertical"`, `"horizontal"`, `"auto"`</span></span> | <span data-ttu-id="b3fcc-266">Modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-266">How the pane will split.</span></span> <span data-ttu-id="b3fcc-267">Con `"auto"` il riquadro verrà diviso nella direzione che offre l'area con la superficie più estesa.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-267">`"auto"` will split in the direction that provides the most surface area.</span></span> |
| `commandLine` | <span data-ttu-id="b3fcc-268">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-268">Optional</span></span> | <span data-ttu-id="b3fcc-269">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="b3fcc-269">Executable file name as a string</span></span> | <span data-ttu-id="b3fcc-270">Esegue l'eseguibile all'interno del riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-270">Executable run within the pane.</span></span> |
| `startingDirectory` | <span data-ttu-id="b3fcc-271">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-271">Optional</span></span> | <span data-ttu-id="b3fcc-272">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="b3fcc-272">Folder location as a string</span></span> | <span data-ttu-id="b3fcc-273">Directory in cui verrà aperto il riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-273">Directory in which the pane will open.</span></span> |
| `tabTitle` | <span data-ttu-id="b3fcc-274">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-274">Optional</span></span> | <span data-ttu-id="b3fcc-275">String</span><span class="sxs-lookup"><span data-stu-id="b3fcc-275">String</span></span> | <span data-ttu-id="b3fcc-276">Titolo della scheda quando lo stato attivo si trova nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-276">Title of the tab when the new pane is focused.</span></span> |
| `index` | <span data-ttu-id="b3fcc-277">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-277">Optional</span></span> | <span data-ttu-id="b3fcc-278">Intero</span><span class="sxs-lookup"><span data-stu-id="b3fcc-278">Integer</span></span> | <span data-ttu-id="b3fcc-279">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="b3fcc-279">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="b3fcc-280">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-280">Optional</span></span> | <span data-ttu-id="b3fcc-281">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="b3fcc-281">Profile's name or GUID as a string</span></span> | <span data-ttu-id="b3fcc-282">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-282">Profile that will open based on its GUID or name.</span></span> |
| `splitMode` | <span data-ttu-id="b3fcc-283">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-283">Optional</span></span> | `"duplicate"` | <span data-ttu-id="b3fcc-284">Controlla la modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-284">Controls how the pane splits.</span></span> <span data-ttu-id="b3fcc-285">Accetta solo `"duplicate"`, con cui il profilo del riquadro con lo stato attivo viene duplicato in un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-285">Only accepts `"duplicate"`, which will duplicate the focused pane's profile into a new pane.</span></span> |

<br />

___

## <a name="clipboard-integration-commands"></a><span data-ttu-id="b3fcc-286">Comandi di integrazione degli Appunti</span><span class="sxs-lookup"><span data-stu-id="b3fcc-286">Clipboard integration commands</span></span>

### <a name="copy"></a><span data-ttu-id="b3fcc-287">Copia</span><span class="sxs-lookup"><span data-stu-id="b3fcc-287">Copy</span></span>

<span data-ttu-id="b3fcc-288">Copia il contenuto del terminale selezionato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-288">This copies the selected terminal content to your clipboard.</span></span>

<span data-ttu-id="b3fcc-289">**Nome del comando:** `copy`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-289">**Command name:** `copy`</span></span>

<span data-ttu-id="b3fcc-290">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-290">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="clipboard-actions"></a><span data-ttu-id="b3fcc-291">Azioni degli Appunti</span><span class="sxs-lookup"><span data-stu-id="b3fcc-291">Clipboard Actions</span></span>

| <span data-ttu-id="b3fcc-292">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fcc-292">Name</span></span> | <span data-ttu-id="b3fcc-293">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-293">Necessity</span></span> | <span data-ttu-id="b3fcc-294">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="b3fcc-294">Accepts</span></span> | <span data-ttu-id="b3fcc-295">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcc-295">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `singleLine` | <span data-ttu-id="b3fcc-296">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="b3fcc-296">Optional</span></span> | <span data-ttu-id="b3fcc-297">`true`, `false`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-297">`true`, `false`</span></span> | <span data-ttu-id="b3fcc-298">Quando è `true`, il contenuto copiato verrà copiato come una riga singola.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-298">When `true`, the copied content will be copied as a single line.</span></span> <span data-ttu-id="b3fcc-299">Quando è `false`, i caratteri di nuova riga del testo selezionato vengono mantenuti.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-299">When `false`, newlines persist from the selected text.</span></span> |

### <a name="paste"></a><span data-ttu-id="b3fcc-300">Incolla</span><span class="sxs-lookup"><span data-stu-id="b3fcc-300">Paste</span></span>

<span data-ttu-id="b3fcc-301">Inserisce il contenuto copiato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-301">This inserts the content that was copied onto the clipboard.</span></span>

<span data-ttu-id="b3fcc-302">**Nome del comando:** `paste`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-302">**Command name:** `paste`</span></span>

<span data-ttu-id="b3fcc-303">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-303">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a><span data-ttu-id="b3fcc-304">Comandi di scorrimento</span><span class="sxs-lookup"><span data-stu-id="b3fcc-304">Scrollback commands</span></span>

### <a name="scroll-up"></a><span data-ttu-id="b3fcc-305">Scorri verso l'alto</span><span class="sxs-lookup"><span data-stu-id="b3fcc-305">Scroll up</span></span>

<span data-ttu-id="b3fcc-306">Scorre lo schermo verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-306">This scrolls the screen up.</span></span>

<span data-ttu-id="b3fcc-307">**Nome del comando:** `scrollUp`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-307">**Command name:** `scrollUp`</span></span>

<span data-ttu-id="b3fcc-308">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-308">**Default binding:**</span></span>

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

### <a name="scroll-down"></a><span data-ttu-id="b3fcc-309">Scorri verso il basso</span><span class="sxs-lookup"><span data-stu-id="b3fcc-309">Scroll down</span></span>

<span data-ttu-id="b3fcc-310">Scorre lo schermo verso il basso.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-310">This scrolls the screen down.</span></span>

<span data-ttu-id="b3fcc-311">**Nome del comando:** `scrollDown`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-311">**Command name:** `scrollDown`</span></span>

<span data-ttu-id="b3fcc-312">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-312">**Default binding:**</span></span>

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

### <a name="scroll-up-a-whole-page"></a><span data-ttu-id="b3fcc-313">Scorri verso l'alto di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="b3fcc-313">Scroll up a whole page</span></span>

<span data-ttu-id="b3fcc-314">Scorre lo schermo verso l'alto di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-314">This scrolls the screen up by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="b3fcc-315">**Nome del comando:** `scrollUpPage`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-315">**Command name:** `scrollUpPage`</span></span>

<span data-ttu-id="b3fcc-316">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-316">**Default binding:**</span></span>

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a><span data-ttu-id="b3fcc-317">Scorri verso il basso di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="b3fcc-317">Scroll down a whole page</span></span>

<span data-ttu-id="b3fcc-318">Scorre lo schermo verso il basso di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-318">This scrolls the screen down by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="b3fcc-319">**Nome del comando:** `scrollDownPage`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-319">**Command name:** `scrollDownPage`</span></span>

<span data-ttu-id="b3fcc-320">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-320">**Default binding:**</span></span>

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

<br />

___

## <a name="visual-adjustment-commands"></a><span data-ttu-id="b3fcc-321">Comandi di regolazione della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="b3fcc-321">Visual adjustment commands</span></span>

### <a name="adjust-font-size"></a><span data-ttu-id="b3fcc-322">Regola dimensioni caratteri</span><span class="sxs-lookup"><span data-stu-id="b3fcc-322">Adjust font size</span></span>

<span data-ttu-id="b3fcc-323">Modifica le dimensioni del testo in base al numero di punti specificato.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-323">This changes the text size by a specified point amount.</span></span>

<span data-ttu-id="b3fcc-324">**Nome del comando:** `adjustFontSize`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-324">**Command name:** `adjustFontSize`</span></span>

<span data-ttu-id="b3fcc-325">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-325">**Default bindings:**</span></span>

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a><span data-ttu-id="b3fcc-326">Azioni</span><span class="sxs-lookup"><span data-stu-id="b3fcc-326">Actions</span></span>

| <span data-ttu-id="b3fcc-327">Nome</span><span class="sxs-lookup"><span data-stu-id="b3fcc-327">Name</span></span> | <span data-ttu-id="b3fcc-328">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-328">Necessity</span></span> | <span data-ttu-id="b3fcc-329">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="b3fcc-329">Accepts</span></span> | <span data-ttu-id="b3fcc-330">Description</span><span class="sxs-lookup"><span data-stu-id="b3fcc-330">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `delta` | <span data-ttu-id="b3fcc-331">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="b3fcc-331">Required</span></span> | <span data-ttu-id="b3fcc-332">Intero</span><span class="sxs-lookup"><span data-stu-id="b3fcc-332">Integer</span></span> | <span data-ttu-id="b3fcc-333">Modifiche applicate alle dimensioni per ogni chiamata del comando.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-333">Amount of size change per command invocation.</span></span> |

### <a name="reset-font-size"></a><span data-ttu-id="b3fcc-334">Reimposta dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="b3fcc-334">Reset font size</span></span>

<span data-ttu-id="b3fcc-335">Reimposta le dimensioni del testo in base al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-335">This resets the text size to the default value.</span></span>

<span data-ttu-id="b3fcc-336">**Nome del comando:** `resetFontSize`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-336">**Command name:** `resetFontSize`</span></span>

<span data-ttu-id="b3fcc-337">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="b3fcc-337">**Default binding:**</span></span>

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

<br />

___

## <a name="unbind-keys"></a><span data-ttu-id="b3fcc-338">Disassocia tasti</span><span class="sxs-lookup"><span data-stu-id="b3fcc-338">Unbind keys</span></span>

<span data-ttu-id="b3fcc-339">Annulla l'associazione dei tasti per tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="b3fcc-339">This unbinds the associated keys from any command.</span></span>

<span data-ttu-id="b3fcc-340">**Nome del comando:** `unbound`</span><span class="sxs-lookup"><span data-stu-id="b3fcc-340">**Command name:** `unbound`</span></span>
