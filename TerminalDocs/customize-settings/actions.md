---
title: Azioni del terminale di Windows
description: Informazioni su come creare azioni personalizzate per il terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 11/11/2020
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 31ba6ab95ffc9c55808cb85ba97651dff19076d2
ms.sourcegitcommit: 9a2f9d152f65cdc8106fb9aad7fa69b01f3d05db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "94520283"
---
# <a name="custom-actions-in-windows-terminal"></a><span data-ttu-id="f9b67-103">Azioni personalizzate nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="f9b67-103">Custom actions in Windows Terminal</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9b67-104">A partire dalla versione 1,4 del terminale di Windows, la `keybindings` matrice è stata rinominata all' `actions` interno del settings.jssu file.</span><span class="sxs-lookup"><span data-stu-id="f9b67-104">As of Windows Terminal version 1.4, the `keybindings` array has been renamed to `actions` inside the settings.json file.</span></span> <span data-ttu-id="f9b67-105">Il supporto per la `keybindings` matrice esiste ancora per la compatibilità con le versioni precedenti, ma il terminale non verrà rinominato automaticamente all' `keybindings` interno del `actions` settings.jssu file.</span><span class="sxs-lookup"><span data-stu-id="f9b67-105">Support for the `keybindings` array still exists for backward compatibility, however the terminal will not automatically rename `keybindings` to `actions` inside your settings.json file.</span></span>

<span data-ttu-id="f9b67-106">È possibile creare azioni personalizzate all'interno del terminale di Windows che consentono di controllare la modalità di interazione con il terminale.</span><span class="sxs-lookup"><span data-stu-id="f9b67-106">You can create custom actions inside Windows Terminal that give you control of how you interact with the terminal.</span></span> <span data-ttu-id="f9b67-107">Queste azioni verranno aggiunte automaticamente al riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="f9b67-107">These actions will automatically be added to the command palette.</span></span>

## <a name="action-formats"></a><span data-ttu-id="f9b67-108">Formati di azione</span><span class="sxs-lookup"><span data-stu-id="f9b67-108">Action formats</span></span>

<span data-ttu-id="f9b67-109">Le azioni possono essere strutturate nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9b67-109">Actions can be structured in the following formats:</span></span>

### <a name="commands-without-arguments"></a><span data-ttu-id="f9b67-110">Comandi senza argomenti</span><span class="sxs-lookup"><span data-stu-id="f9b67-110">Commands without arguments</span></span>

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

<span data-ttu-id="f9b67-111">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>alt+f4</kbd> per chiudere la finestra del terminale:</span><span class="sxs-lookup"><span data-stu-id="f9b67-111">For example, this default setting uses the shortcut key <kbd>alt+f4</kbd> to close the terminal window:</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a><span data-ttu-id="f9b67-112">Comandi con argomenti</span><span class="sxs-lookup"><span data-stu-id="f9b67-112">Commands with arguments</span></span>

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

<span data-ttu-id="f9b67-113">Questa impostazione predefinita, ad esempio, usa il tasto di scelta rapida <kbd>ctrl+maiusc+1</kbd> per aprire una nuova scheda nel terminale in base al profilo elencato per primo nel menu a discesa (in genere verrà aperto il profilo PowerShell):</span><span class="sxs-lookup"><span data-stu-id="f9b67-113">For example, this default setting uses the shortcut key <kbd>ctrl+shift+1</kbd> to open a new tab in the terminal based on whichever profile is listed first in your dropdown menu (typically this will open the PowerShell profile):</span></span>

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="action-properties"></a><span data-ttu-id="f9b67-114">Proprietà delle azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-114">Action properties</span></span>

<span data-ttu-id="f9b67-115">Le azioni possono essere costruite usando le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="f9b67-115">Actions can be constructed using the following properties.</span></span>

### <a name="command"></a><span data-ttu-id="f9b67-116">Comando</span><span class="sxs-lookup"><span data-stu-id="f9b67-116">Command</span></span>

<span data-ttu-id="f9b67-117">Comando eseguito quando vengono premuti i tasti associati.</span><span class="sxs-lookup"><span data-stu-id="f9b67-117">This is the command executed when the associated keys are pressed.</span></span>

<span data-ttu-id="f9b67-118">**Nome della proprietà:** `command`</span><span class="sxs-lookup"><span data-stu-id="f9b67-118">**Property name:** `command`</span></span>

<span data-ttu-id="f9b67-119">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-119">**Necessity:** Required</span></span>

<span data-ttu-id="f9b67-120">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="f9b67-120">**Accepts:** String</span></span>

### <a name="keys"></a><span data-ttu-id="f9b67-121">Tasti</span><span class="sxs-lookup"><span data-stu-id="f9b67-121">Keys</span></span>

<span data-ttu-id="f9b67-122">Definisce le combinazioni di tasti usate per chiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="f9b67-122">This defines the key combinations used to call the command.</span></span> <span data-ttu-id="f9b67-123">Con la proprietà keys è possibile associare più modificatori a un unico tasto.</span><span class="sxs-lookup"><span data-stu-id="f9b67-123">Keys can have any number of modifiers with one key.</span></span> <span data-ttu-id="f9b67-124">I tasti e i modificatori accettati sono elencati [di seguito](#accepted-modifiers-and-keys).</span><span class="sxs-lookup"><span data-stu-id="f9b67-124">Accepted modifiers and keys are listed [below](#accepted-modifiers-and-keys).</span></span>

<span data-ttu-id="f9b67-125">Se l'azione non dispone di chiavi, verrà visualizzata nel riquadro comandi, ma non potrà essere richiamata con la tastiera.</span><span class="sxs-lookup"><span data-stu-id="f9b67-125">If the action does not have keys, it will appear in the command palette but cannot be invoked with the keyboard.</span></span>

<span data-ttu-id="f9b67-126">**Nome della proprietà:** `keys`</span><span class="sxs-lookup"><span data-stu-id="f9b67-126">**Property name:** `keys`</span></span>

<span data-ttu-id="f9b67-127">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-127">**Necessity:** Optional</span></span>

<span data-ttu-id="f9b67-128">**Accetta:** stringa o matrice[stringa]</span><span class="sxs-lookup"><span data-stu-id="f9b67-128">**Accepts:** String or array[string]</span></span>

### <a name="action"></a><span data-ttu-id="f9b67-129">Azione</span><span class="sxs-lookup"><span data-stu-id="f9b67-129">Action</span></span>

<span data-ttu-id="f9b67-130">Aggiunge funzionalità aggiuntive a determinati comandi.</span><span class="sxs-lookup"><span data-stu-id="f9b67-130">This adds additional functionality to certain commands.</span></span>

<span data-ttu-id="f9b67-131">**Nome della proprietà:** `action`</span><span class="sxs-lookup"><span data-stu-id="f9b67-131">**Property name:** `action`</span></span>

<span data-ttu-id="f9b67-132">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-132">**Necessity:** Optional</span></span>

<span data-ttu-id="f9b67-133">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="f9b67-133">**Accepts:** String</span></span>

### <a name="name"></a><span data-ttu-id="f9b67-134">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-134">Name</span></span>

<span data-ttu-id="f9b67-135">Questo consente di impostare il nome che verrà visualizzato nel riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="f9b67-135">This sets the name that will appear in the command palette.</span></span> <span data-ttu-id="f9b67-136">Se non ne viene specificato uno, il terminale tenterà di generare automaticamente un nome.</span><span class="sxs-lookup"><span data-stu-id="f9b67-136">If one isn't provided, the terminal will attempt to automatically generate a name.</span></span>

<span data-ttu-id="f9b67-137">**Nome della proprietà:** `name`</span><span class="sxs-lookup"><span data-stu-id="f9b67-137">**Property name:** `name`</span></span>

<span data-ttu-id="f9b67-138">**Necessità**: facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-138">**Necessity**: Optional</span></span>

<span data-ttu-id="f9b67-139">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="f9b67-139">**Accepts:** String</span></span>

### <a name="icon"></a><span data-ttu-id="f9b67-140">Icona</span><span class="sxs-lookup"><span data-stu-id="f9b67-140">Icon</span></span>

<span data-ttu-id="f9b67-141">Questa operazione consente di impostare l'icona visualizzata all'interno del riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="f9b67-141">This sets the icon that displays within the command palette.</span></span>

<span data-ttu-id="f9b67-142">**Nome della proprietà:** `icon`</span><span class="sxs-lookup"><span data-stu-id="f9b67-142">**Property name:** `icon`</span></span>

<span data-ttu-id="f9b67-143">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-143">**Necessity:** Optional</span></span>

<span data-ttu-id="f9b67-144">**Accetta:** Percorso del file sotto forma di stringa o emoji</span><span class="sxs-lookup"><span data-stu-id="f9b67-144">**Accepts:** File location as a string, or an emoji</span></span>

<br />

___

## <a name="accepted-modifiers-and-keys"></a><span data-ttu-id="f9b67-145">Tasti e modificatori accettati</span><span class="sxs-lookup"><span data-stu-id="f9b67-145">Accepted modifiers and keys</span></span>

### <a name="modifiers"></a><span data-ttu-id="f9b67-146">Modificatori</span><span class="sxs-lookup"><span data-stu-id="f9b67-146">Modifiers</span></span>

<span data-ttu-id="f9b67-147">`ctrl+`, `shift+`, `alt+`</span><span class="sxs-lookup"><span data-stu-id="f9b67-147">`ctrl+`, `shift+`, `alt+`</span></span>

> [!NOTE]
> <span data-ttu-id="f9b67-148">La `Windows` chiave non è supportata come modificatore.</span><span class="sxs-lookup"><span data-stu-id="f9b67-148">The `Windows` key is not supported as a modifier.</span></span> 

### <a name="modifier-keys"></a><span data-ttu-id="f9b67-149">Tasti di modifica</span><span class="sxs-lookup"><span data-stu-id="f9b67-149">Modifier keys</span></span>

| <span data-ttu-id="f9b67-150">Type</span><span class="sxs-lookup"><span data-stu-id="f9b67-150">Type</span></span> | <span data-ttu-id="f9b67-151">Tasti</span><span class="sxs-lookup"><span data-stu-id="f9b67-151">Keys</span></span> |
| ---- | ---- |
| <span data-ttu-id="f9b67-152">Tasti funzione e alfanumerici</span><span class="sxs-lookup"><span data-stu-id="f9b67-152">Function and alphanumeric keys</span></span> | <span data-ttu-id="f9b67-153">`f1-f24`, `a-z`, `0-9`</span><span class="sxs-lookup"><span data-stu-id="f9b67-153">`f1-f24`, `a-z`, `0-9`</span></span> |
| <span data-ttu-id="f9b67-154">Simboli</span><span class="sxs-lookup"><span data-stu-id="f9b67-154">Symbols</span></span> | <span data-ttu-id="f9b67-155">``` ` ```, `plus`, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span><span class="sxs-lookup"><span data-stu-id="f9b67-155">``` ` ```, `plus`, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span></span> |
| <span data-ttu-id="f9b67-156">Tasti di direzione</span><span class="sxs-lookup"><span data-stu-id="f9b67-156">Arrow keys</span></span> | <span data-ttu-id="f9b67-157">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`</span><span class="sxs-lookup"><span data-stu-id="f9b67-157">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`</span></span> |
| <span data-ttu-id="f9b67-158">Tasti di azione</span><span class="sxs-lookup"><span data-stu-id="f9b67-158">Action keys</span></span> | <span data-ttu-id="f9b67-159">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`, `app`, `menu`</span><span class="sxs-lookup"><span data-stu-id="f9b67-159">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`, `app`, `menu`</span></span>  |
| <span data-ttu-id="f9b67-160">Tasti del tastierino numerico</span><span class="sxs-lookup"><span data-stu-id="f9b67-160">Numpad keys</span></span> | <span data-ttu-id="f9b67-161">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span><span class="sxs-lookup"><span data-stu-id="f9b67-161">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span></span> |

<span data-ttu-id="f9b67-162">**Nota:** `=` e `plus` sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f9b67-162">**Note:** `=` and `plus` are equivalents.</span></span> <span data-ttu-id="f9b67-163">Il secondo non deve essere confuso con `numpad_plus` .</span><span class="sxs-lookup"><span data-stu-id="f9b67-163">The latter must not be confused with `numpad_plus`.</span></span>

___

## <a name="application-level-commands"></a><span data-ttu-id="f9b67-164">Comandi a livello di applicazione</span><span class="sxs-lookup"><span data-stu-id="f9b67-164">Application-level commands</span></span>

### <a name="close-window"></a><span data-ttu-id="f9b67-165">Chiudi finestra</span><span class="sxs-lookup"><span data-stu-id="f9b67-165">Close window</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="f9b67-166">Chiude la finestra corrente e tutte le relative schede.</span><span class="sxs-lookup"><span data-stu-id="f9b67-166">This closes the current window and all tabs within it.</span></span> <span data-ttu-id="f9b67-167">Se `confirmCloseAllTabs` è impostato su `true`, verrà visualizzata una finestra di dialogo per confermare la chiusura di tutte le schede.</span><span class="sxs-lookup"><span data-stu-id="f9b67-167">If `confirmCloseAllTabs` is set to `true`, a confirmation dialog will appear to ensure you'd like to close all your tabs.</span></span> <span data-ttu-id="f9b67-168">Per altre informazioni su questa impostazione, vedi la [pagina delle impostazioni globali](./global-settings.md#hide-close-all-tabs-popup).</span><span class="sxs-lookup"><span data-stu-id="f9b67-168">More information on this setting can be found on the [Global settings page](./global-settings.md#hide-close-all-tabs-popup).</span></span>

<span data-ttu-id="f9b67-169">**Nome del comando:** `closeWindow`</span><span class="sxs-lookup"><span data-stu-id="f9b67-169">**Command name:** `closeWindow`</span></span>

<span data-ttu-id="f9b67-170">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-170">**Default binding:**</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Terminale Windows - Conferma chiusura di tutte le schede](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a><span data-ttu-id="f9b67-172">Trova</span><span class="sxs-lookup"><span data-stu-id="f9b67-172">Find</span></span>

<span data-ttu-id="f9b67-173">Apre la finestra di dialogo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="f9b67-173">This opens the search dialog box.</span></span> <span data-ttu-id="f9b67-174">Per altre informazioni sulla ricerca, vedi la [pagina relativa alla ricerca](./../search.md).</span><span class="sxs-lookup"><span data-stu-id="f9b67-174">More information on search can be found on the [Search page](./../search.md).</span></span>

<span data-ttu-id="f9b67-175">**Nome del comando:** `find`</span><span class="sxs-lookup"><span data-stu-id="f9b67-175">**Command name:** `find`</span></span>

<span data-ttu-id="f9b67-176">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-176">**Default binding:**</span></span>

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a><span data-ttu-id="f9b67-177">Apri menu a discesa</span><span class="sxs-lookup"><span data-stu-id="f9b67-177">Open the dropdown</span></span>

<span data-ttu-id="f9b67-178">Apre il menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="f9b67-178">This opens the dropdown menu.</span></span>

<span data-ttu-id="f9b67-179">**Nome del comando:** `openNewTabDropdown`</span><span class="sxs-lookup"><span data-stu-id="f9b67-179">**Command name:** `openNewTabDropdown`</span></span>

<span data-ttu-id="f9b67-180">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-180">**Default binding:**</span></span>

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-files"></a><span data-ttu-id="f9b67-181">Apri file di impostazioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-181">Open settings files</span></span>

<span data-ttu-id="f9b67-182">Apre i file di impostazioni predefiniti o personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f9b67-182">This opens either the default or custom settings files.</span></span> <span data-ttu-id="f9b67-183">Senza il campo `target` verrà aperto il file settings.json.</span><span class="sxs-lookup"><span data-stu-id="f9b67-183">Without the `target` field, this will open the settings.json file.</span></span>

<span data-ttu-id="f9b67-184">**Nome del comando:** `openSettings`</span><span class="sxs-lookup"><span data-stu-id="f9b67-184">**Command name:** `openSettings`</span></span>

<span data-ttu-id="f9b67-185">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-185">**Default binding:**</span></span>

```json
{ "command": "openSettings", "keys": "ctrl+," },
{ "command": { "action": "openSettings", "target": "defaultsFile" }, "keys": "ctrl+alt+," },
```

#### <a name="actions"></a><span data-ttu-id="f9b67-186">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-186">Actions</span></span>

| <span data-ttu-id="f9b67-187">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-187">Name</span></span> | <span data-ttu-id="f9b67-188">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-188">Necessity</span></span> | <span data-ttu-id="f9b67-189">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-189">Accepts</span></span> | <span data-ttu-id="f9b67-190">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-190">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `target` | <span data-ttu-id="f9b67-191">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-191">Optional</span></span> | <span data-ttu-id="f9b67-192">`"settingsFile"`, `"defaultsFile"`, `"allFiles"`</span><span class="sxs-lookup"><span data-stu-id="f9b67-192">`"settingsFile"`, `"defaultsFile"`, `"allFiles"`</span></span> | <span data-ttu-id="f9b67-193">Il file di impostazioni da aprire.</span><span class="sxs-lookup"><span data-stu-id="f9b67-193">The settings file to open.</span></span> |

### <a name="toggle-full-screen"></a><span data-ttu-id="f9b67-194">Attiva/Disattiva schermo intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-194">Toggle full screen</span></span>

<span data-ttu-id="f9b67-195">Consente di passare dalla finestra a schermo intero a quella con dimensioni predefinite e viceversa.</span><span class="sxs-lookup"><span data-stu-id="f9b67-195">This allows you to switch between full screen and default window sizes.</span></span>

<span data-ttu-id="f9b67-196">**Nome del comando:** `toggleFullscreen`</span><span class="sxs-lookup"><span data-stu-id="f9b67-196">**Command name:** `toggleFullscreen`</span></span>

<span data-ttu-id="f9b67-197">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-197">**Default bindings:**</span></span>

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

### <a name="toggle-focus-mode"></a><span data-ttu-id="f9b67-198">Attiva/Nascondi modalità messa a fuoco</span><span class="sxs-lookup"><span data-stu-id="f9b67-198">Toggle focus mode</span></span>

<span data-ttu-id="f9b67-199">Questo consente di attivare la modalità messa a fuoco, che nasconde le schede e la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="f9b67-199">This allows you to enter "focus mode", which hides the tabs and title bar.</span></span>

<span data-ttu-id="f9b67-200">**Nome del comando:** `toggleFocusMode`</span><span class="sxs-lookup"><span data-stu-id="f9b67-200">**Command name:** `toggleFocusMode`</span></span>

<span data-ttu-id="f9b67-201">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-201">**Default bindings:**</span></span>

```json
{ "command": "toggleFocusMode" }
```

### <a name="toggle-always-on-top-mode"></a><span data-ttu-id="f9b67-202">Attiva/Nascondi sempre in modalità principale</span><span class="sxs-lookup"><span data-stu-id="f9b67-202">Toggle always on top mode</span></span>

<span data-ttu-id="f9b67-203">In questo modo è possibile impostare lo stato "always on top" della finestra.</span><span class="sxs-lookup"><span data-stu-id="f9b67-203">This allows you toggle the "always on top" state of the window.</span></span> <span data-ttu-id="f9b67-204">Quando si usa la modalità "always on top", la finestra verrà visualizzata nella parte superiore di tutte le altre finestre non in primo piano.</span><span class="sxs-lookup"><span data-stu-id="f9b67-204">When in "always on top" mode, the window will appear on top of all other non-topmost windows.</span></span>

<span data-ttu-id="f9b67-205">**Nome del comando:** `toggleAlwaysOnTop`</span><span class="sxs-lookup"><span data-stu-id="f9b67-205">**Command name:** `toggleAlwaysOnTop`</span></span>

<span data-ttu-id="f9b67-206">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-206">**Default bindings:**</span></span>

```json
{ "command": "toggleAlwaysOnTop" }
```

### <a name="send-input"></a><span data-ttu-id="f9b67-207">Invia input</span><span class="sxs-lookup"><span data-stu-id="f9b67-207">Send input</span></span>

<span data-ttu-id="f9b67-208">Inviare input di testo arbitrario alla Shell.</span><span class="sxs-lookup"><span data-stu-id="f9b67-208">Send arbitrary text input to the shell.</span></span>
<span data-ttu-id="f9b67-209">Ad esempio, l'input `"text\n"` scriverà "testo" seguito da una nuova riga nella shell.</span><span class="sxs-lookup"><span data-stu-id="f9b67-209">As an example the input `"text\n"` will write "text" followed by a newline to the shell.</span></span>

<span data-ttu-id="f9b67-210">È possibile usare le sequenze di escape ANSI, ma i codici `\x1b` di escape come devono essere scritti come `\u001b` .</span><span class="sxs-lookup"><span data-stu-id="f9b67-210">ANSI escape sequences may be used, but escape codes like `\x1b` must be written as `\u001b`.</span></span>
<span data-ttu-id="f9b67-211">Ad esempio `"\u001b[A"` , si comporterà come se fosse stato premuto il pulsante freccia su.</span><span class="sxs-lookup"><span data-stu-id="f9b67-211">For instance `"\u001b[A"` will behave as if the up arrow button had been pressed.</span></span>

<span data-ttu-id="f9b67-212">**Nome del comando:** `sendInput`</span><span class="sxs-lookup"><span data-stu-id="f9b67-212">**Command name:** `sendInput`</span></span>

<span data-ttu-id="f9b67-213">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-213">**Default bindings:**</span></span>

<span data-ttu-id="f9b67-214">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="f9b67-214">_This command is not currently bound in the default settings_.</span></span>

```json
{ "command": { "action": "sendInput", "input": "\u001b[A" }, "keys": "" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-215">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-215">Actions</span></span>

| <span data-ttu-id="f9b67-216">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-216">Name</span></span> | <span data-ttu-id="f9b67-217">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-217">Necessity</span></span> | <span data-ttu-id="f9b67-218">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-218">Accepts</span></span> | <span data-ttu-id="f9b67-219">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-219">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `input` | <span data-ttu-id="f9b67-220">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-220">Required</span></span> | <span data-ttu-id="f9b67-221">string</span><span class="sxs-lookup"><span data-stu-id="f9b67-221">String</span></span> | <span data-ttu-id="f9b67-222">Input di testo da inserire nella shell.</span><span class="sxs-lookup"><span data-stu-id="f9b67-222">The text input to feed into the shell.</span></span> |

<br />

___

## <a name="tab-management-commands"></a><span data-ttu-id="f9b67-223">Comandi per la gestione delle schede</span><span class="sxs-lookup"><span data-stu-id="f9b67-223">Tab management commands</span></span>

### <a name="close-tab"></a><span data-ttu-id="f9b67-224">Chiudi scheda</span><span class="sxs-lookup"><span data-stu-id="f9b67-224">Close tab</span></span>

<span data-ttu-id="f9b67-225">Chiude la scheda corrente.</span><span class="sxs-lookup"><span data-stu-id="f9b67-225">This closes the current tab.</span></span>

<span data-ttu-id="f9b67-226">**Nome del comando:** `closeTab`</span><span class="sxs-lookup"><span data-stu-id="f9b67-226">**Command name:** `closeTab`</span></span>

### <a name="close-all-other-tabs"></a><span data-ttu-id="f9b67-227">Chiudi tutte le altre schede</span><span class="sxs-lookup"><span data-stu-id="f9b67-227">Close all other tabs</span></span>

<span data-ttu-id="f9b67-228">In questo modo vengono chiuse tutte le schede ad eccezione di quella in corrispondenza di un indice.</span><span class="sxs-lookup"><span data-stu-id="f9b67-228">This closes all tabs except for the one at an index.</span></span> <span data-ttu-id="f9b67-229">Se non viene specificato alcun indice, usare l'indice della scheda con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f9b67-229">If no index is provided, use the focused tab's index.</span></span>

<span data-ttu-id="f9b67-230">**Nome del comando:** `closeOtherTabs`</span><span class="sxs-lookup"><span data-stu-id="f9b67-230">**Command name:** `closeOtherTabs`</span></span>

<span data-ttu-id="f9b67-231">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-231">**Default binding:**</span></span>

```json
{ "command": "closeOtherTabs" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-232">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-232">Actions</span></span>

| <span data-ttu-id="f9b67-233">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-233">Name</span></span> | <span data-ttu-id="f9b67-234">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-234">Necessity</span></span> | <span data-ttu-id="f9b67-235">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-235">Accepts</span></span> | <span data-ttu-id="f9b67-236">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-236">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="f9b67-237">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-237">Optional</span></span> | <span data-ttu-id="f9b67-238">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-238">Integer</span></span> | <span data-ttu-id="f9b67-239">Posizione della scheda da mantenere aperta.</span><span class="sxs-lookup"><span data-stu-id="f9b67-239">Position of the tab to be kept open.</span></span> |

### <a name="close-tabs-after-index"></a><span data-ttu-id="f9b67-240">Chiudi tabulazioni dopo l'indice</span><span class="sxs-lookup"><span data-stu-id="f9b67-240">Close tabs after index</span></span>

<span data-ttu-id="f9b67-241">Questa operazione chiude le schede che seguono la scheda in corrispondenza di un indice.</span><span class="sxs-lookup"><span data-stu-id="f9b67-241">This closes the tabs following the tab at an index.</span></span> <span data-ttu-id="f9b67-242">Se non viene specificato alcun indice, usare l'indice della scheda con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f9b67-242">If no index is provided, use the focused tab's index.</span></span>

<span data-ttu-id="f9b67-243">**Nome del comando:** `closeTabsAfter`</span><span class="sxs-lookup"><span data-stu-id="f9b67-243">**Command name:** `closeTabsAfter`</span></span>

<span data-ttu-id="f9b67-244">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-244">**Default binding:**</span></span>

```json
{ "command": "closeTabsAfter" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-245">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-245">Actions</span></span>

| <span data-ttu-id="f9b67-246">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-246">Name</span></span> | <span data-ttu-id="f9b67-247">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-247">Necessity</span></span> | <span data-ttu-id="f9b67-248">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-248">Accepts</span></span> | <span data-ttu-id="f9b67-249">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-249">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="f9b67-250">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-250">Optional</span></span> | <span data-ttu-id="f9b67-251">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-251">Integer</span></span> | <span data-ttu-id="f9b67-252">Posizione dell'ultima scheda da mantenere aperta.</span><span class="sxs-lookup"><span data-stu-id="f9b67-252">Position of the last tab to be kept open.</span></span> |

### <a name="duplicate-tab"></a><span data-ttu-id="f9b67-253">Duplica scheda</span><span class="sxs-lookup"><span data-stu-id="f9b67-253">Duplicate tab</span></span>

<span data-ttu-id="f9b67-254">Crea una copia della scheda corrente e la apre.</span><span class="sxs-lookup"><span data-stu-id="f9b67-254">This makes a copy of the current tab and opens it.</span></span>

<span data-ttu-id="f9b67-255">**Nome del comando:** `duplicateTab`</span><span class="sxs-lookup"><span data-stu-id="f9b67-255">**Command name:** `duplicateTab`</span></span>

<span data-ttu-id="f9b67-256">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-256">**Default binding:**</span></span>

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a><span data-ttu-id="f9b67-257">Nuova scheda</span><span class="sxs-lookup"><span data-stu-id="f9b67-257">New tab</span></span>

<span data-ttu-id="f9b67-258">Crea una nuova scheda. Se viene specificato senza argomenti, il profilo predefinito verrà aperto in una nuova scheda. Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="f9b67-258">This creates a new tab. Without any arguments, this will open the default profile in a new tab. If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="f9b67-259">**Nome del comando:** `newTab`</span><span class="sxs-lookup"><span data-stu-id="f9b67-259">**Command name:** `newTab`</span></span>

<span data-ttu-id="f9b67-260">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-260">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="f9b67-261">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-261">Actions</span></span>

| <span data-ttu-id="f9b67-262">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-262">Name</span></span> | <span data-ttu-id="f9b67-263">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-263">Necessity</span></span> | <span data-ttu-id="f9b67-264">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-264">Accepts</span></span> | <span data-ttu-id="f9b67-265">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-265">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `commandline` | <span data-ttu-id="f9b67-266">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-266">Optional</span></span> | <span data-ttu-id="f9b67-267">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="f9b67-267">Executable file name as a string</span></span> | <span data-ttu-id="f9b67-268">Esegue l'eseguibile all'interno della scheda.</span><span class="sxs-lookup"><span data-stu-id="f9b67-268">Executable run within the tab.</span></span> |
| `startingDirectory` | <span data-ttu-id="f9b67-269">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-269">Optional</span></span> | <span data-ttu-id="f9b67-270">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="f9b67-270">Folder location as a string</span></span> | <span data-ttu-id="f9b67-271">Directory in cui verrà aperta la scheda.</span><span class="sxs-lookup"><span data-stu-id="f9b67-271">Directory in which the tab will open.</span></span> |
| `tabTitle` | <span data-ttu-id="f9b67-272">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-272">Optional</span></span> | <span data-ttu-id="f9b67-273">String</span><span class="sxs-lookup"><span data-stu-id="f9b67-273">String</span></span> | <span data-ttu-id="f9b67-274">Titolo della nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="f9b67-274">Title of the new tab.</span></span> |
| `index` | <span data-ttu-id="f9b67-275">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-275">Optional</span></span> | <span data-ttu-id="f9b67-276">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-276">Integer</span></span> | <span data-ttu-id="f9b67-277">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="f9b67-277">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="f9b67-278">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-278">Optional</span></span> | <span data-ttu-id="f9b67-279">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="f9b67-279">Profile's name or GUID as a string</span></span> | <span data-ttu-id="f9b67-280">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="f9b67-280">Profile that will open based on its GUID or name.</span></span> |

### <a name="open-next-tab"></a><span data-ttu-id="f9b67-281">Apri scheda successiva</span><span class="sxs-lookup"><span data-stu-id="f9b67-281">Open next tab</span></span>

<span data-ttu-id="f9b67-282">Apre la scheda a destra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="f9b67-282">This opens the tab to the right of the current one.</span></span>

<span data-ttu-id="f9b67-283">**Nome del comando:** `nextTab`</span><span class="sxs-lookup"><span data-stu-id="f9b67-283">**Command name:** `nextTab`</span></span>

<span data-ttu-id="f9b67-284">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-284">**Default binding:**</span></span>

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a><span data-ttu-id="f9b67-285">Apri scheda precedente</span><span class="sxs-lookup"><span data-stu-id="f9b67-285">Open previous tab</span></span>

<span data-ttu-id="f9b67-286">Apre la scheda a sinistra di quella corrente.</span><span class="sxs-lookup"><span data-stu-id="f9b67-286">This opens the tab to the left of the current one.</span></span>

<span data-ttu-id="f9b67-287">**Nome del comando:** `prevTab`</span><span class="sxs-lookup"><span data-stu-id="f9b67-287">**Command name:** `prevTab`</span></span>

<span data-ttu-id="f9b67-288">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-288">**Default binding:**</span></span>

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="tab-search"></a><span data-ttu-id="f9b67-289">Ricerca nella scheda</span><span class="sxs-lookup"><span data-stu-id="f9b67-289">Tab search</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="f9b67-290">Verrà visualizzata la casella di ricerca della scheda.</span><span class="sxs-lookup"><span data-stu-id="f9b67-290">This opens the tab search box.</span></span>

<span data-ttu-id="f9b67-291">**Nome del comando:** `tabSearch`</span><span class="sxs-lookup"><span data-stu-id="f9b67-291">**Command name:** `tabSearch`</span></span>

<span data-ttu-id="f9b67-292">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-292">**Default binding:**</span></span>

<span data-ttu-id="f9b67-293">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="f9b67-293">_This command is not currently bound in the default settings_.</span></span>

```json
{"command": "tabSearch", "keys": ""}
```

:::column-end:::
:::column span="":::
![Ricerca nella scheda terminale di Windows](./../images/tab-search.gif)

:::column-end:::
:::row-end:::

### <a name="open-a-specific-tab"></a><span data-ttu-id="f9b67-295">Apri una scheda specifica</span><span class="sxs-lookup"><span data-stu-id="f9b67-295">Open a specific tab</span></span>

<span data-ttu-id="f9b67-296">Apre una scheda specifica a seconda dell'indice.</span><span class="sxs-lookup"><span data-stu-id="f9b67-296">This opens a specific tab depending on the index.</span></span>

<span data-ttu-id="f9b67-297">**Nome del comando:** `switchToTab`</span><span class="sxs-lookup"><span data-stu-id="f9b67-297">**Command name:** `switchToTab`</span></span>

<span data-ttu-id="f9b67-298">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-298">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="f9b67-299">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-299">Actions</span></span>

| <span data-ttu-id="f9b67-300">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-300">Name</span></span> | <span data-ttu-id="f9b67-301">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-301">Necessity</span></span> | <span data-ttu-id="f9b67-302">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-302">Accepts</span></span> | <span data-ttu-id="f9b67-303">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-303">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="f9b67-304">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-304">Required</span></span> | <span data-ttu-id="f9b67-305">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-305">Integer</span></span> | <span data-ttu-id="f9b67-306">Scheda che verrà aperta in base alla relativa posizione nella barra delle schede (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="f9b67-306">Tab that will open based on its position in the tab bar (starting at 0).</span></span> |

### <a name="rename-tab"></a><span data-ttu-id="f9b67-307">Rinomina scheda</span><span class="sxs-lookup"><span data-stu-id="f9b67-307">Rename tab</span></span>

<span data-ttu-id="f9b67-308">Questo comando può essere usato per rinominare una scheda in una stringa specifica.</span><span class="sxs-lookup"><span data-stu-id="f9b67-308">This command can be used to rename a tab to a specific string.</span></span>

<span data-ttu-id="f9b67-309">**Nome del comando:** `renameTab`</span><span class="sxs-lookup"><span data-stu-id="f9b67-309">**Command name:** `renameTab`</span></span>

<span data-ttu-id="f9b67-310">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-310">**Default binding:**</span></span>

<span data-ttu-id="f9b67-311">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="f9b67-311">_This command is not currently bound in the default settings_.</span></span>

```json
// Rename a tab to "Foo"
{ "command": { "action": "renameTab", "title": "Foo" }, "keys": "" }

// Reset the tab's name
{ "command": { "action": "renameTab", "title": null }, "keys": "" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-312">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-312">Actions</span></span>

| <span data-ttu-id="f9b67-313">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-313">Name</span></span> | <span data-ttu-id="f9b67-314">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-314">Necessity</span></span> | <span data-ttu-id="f9b67-315">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-315">Accepts</span></span> | <span data-ttu-id="f9b67-316">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-316">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `title` | <span data-ttu-id="f9b67-317">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-317">Optional</span></span> | <span data-ttu-id="f9b67-318">String</span><span class="sxs-lookup"><span data-stu-id="f9b67-318">String</span></span> | <span data-ttu-id="f9b67-319">Nuovo titolo da utilizzare per questa scheda. Se omesso, il comando ripristinerà nuovamente il titolo della scheda al valore originale.</span><span class="sxs-lookup"><span data-stu-id="f9b67-319">The new title to use for this tab. If omitted, this command will revert the tab title back to its original value.</span></span> |

### <a name="open-tab-rename-text-box-preview"></a><span data-ttu-id="f9b67-320">Apri ridenominazione tabulazione casella di testo ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="f9b67-320">Open tab rename text box ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="f9b67-321">Questo comando modifica il titolo della scheda in un campo di testo che consente di modificare il titolo per la scheda corrente. Se si deseleziona il campo di testo, il titolo della scheda viene reimpostato sul valore predefinito per l'istanza corrente della shell.</span><span class="sxs-lookup"><span data-stu-id="f9b67-321">This command changes the tab title into a text field that lets you edit the title for the current tab. Clearing the text field will reset the tab title back to the default for the current shell instance.</span></span>

<span data-ttu-id="f9b67-322">**Nome del comando:** `openTabRenamer`</span><span class="sxs-lookup"><span data-stu-id="f9b67-322">**Command name:** `openTabRenamer`</span></span>

<span data-ttu-id="f9b67-323">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-323">**Default binding:**</span></span>

<span data-ttu-id="f9b67-324">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="f9b67-324">_This command is not currently bound in the default settings_.</span></span>

```json
{ "command": "openTabRenamer", "keys": "ctrl+alt+a" }
```

> [!IMPORTANT]
> <span data-ttu-id="f9b67-325">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="f9b67-325">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="change-tab-color"></a><span data-ttu-id="f9b67-326">Cambia colore scheda</span><span class="sxs-lookup"><span data-stu-id="f9b67-326">Change tab color</span></span>

<span data-ttu-id="f9b67-327">Questo comando può essere usato per modificare il colore di una scheda in un valore specifico.</span><span class="sxs-lookup"><span data-stu-id="f9b67-327">This command can be used to change the color of a tab to a specific value.</span></span>

<span data-ttu-id="f9b67-328">**Nome del comando:** `setTabColor`</span><span class="sxs-lookup"><span data-stu-id="f9b67-328">**Command name:** `setTabColor`</span></span>

<span data-ttu-id="f9b67-329">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-329">**Default binding:**</span></span>

<span data-ttu-id="f9b67-330">_Questo comando non è attualmente associato alle impostazioni predefinite_.</span><span class="sxs-lookup"><span data-stu-id="f9b67-330">_This command is not currently bound in the default settings_.</span></span>

```json
// Change the tab's color to a bright magenta
{ "command": { "action": "setTabColor", "color": "#ff00ff" }, "keys": "" }

// Reset the tab's color
{ "command": { "action": "setTabColor", "color": null }, "keys": "" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-331">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-331">Actions</span></span>

| <span data-ttu-id="f9b67-332">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-332">Name</span></span> | <span data-ttu-id="f9b67-333">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-333">Necessity</span></span> | <span data-ttu-id="f9b67-334">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-334">Accepts</span></span> | <span data-ttu-id="f9b67-335">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-335">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `color` | <span data-ttu-id="f9b67-336">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-336">Optional</span></span> | <span data-ttu-id="f9b67-337">Stringa, in formato esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="f9b67-337">String, in hex format: `"#rgb"` or `"#rrggbb"`</span></span> | <span data-ttu-id="f9b67-338">Nuovo colore da usare per questa scheda. Se omesso, il comando ripristinerà il colore della scheda al valore originale.</span><span class="sxs-lookup"><span data-stu-id="f9b67-338">The new color to use for this tab. If omitted, this command will revert the tab's color back to its original value.</span></span> |

### <a name="open-tab-color-picker"></a><span data-ttu-id="f9b67-339">Apri selezione colori scheda</span><span class="sxs-lookup"><span data-stu-id="f9b67-339">Open tab color picker</span></span>

<span data-ttu-id="f9b67-340">Questo comando può essere usato per aprire la selezione colori per la scheda attiva. La selezione colori può essere usata per impostare un colore per la scheda in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f9b67-340">This command can be used to open the color picker for the active tab. The color picker can be used to set a color for the tab at runtime.</span></span>

<span data-ttu-id="f9b67-341">**Nome del comando:** `openTabColorPicker`</span><span class="sxs-lookup"><span data-stu-id="f9b67-341">**Command name:** `openTabColorPicker`</span></span>

<span data-ttu-id="f9b67-342">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-342">**Default binding:**</span></span>

```json
{ "command": "openTabColorPicker" }
```

<br />

___

## <a name="pane-management-commands"></a><span data-ttu-id="f9b67-343">Comandi di gestione dei riquadri</span><span class="sxs-lookup"><span data-stu-id="f9b67-343">Pane management commands</span></span>

### <a name="close-pane"></a><span data-ttu-id="f9b67-344">Chiudi riquadro</span><span class="sxs-lookup"><span data-stu-id="f9b67-344">Close pane</span></span>

<span data-ttu-id="f9b67-345">Chiude il riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="f9b67-345">This closes the active pane.</span></span> <span data-ttu-id="f9b67-346">Se non sono presenti riquadri divisi, chiude la scheda corrente. Se è aperta una sola scheda, chiude la finestra.</span><span class="sxs-lookup"><span data-stu-id="f9b67-346">If there aren't any split panes, this will close the current tab. If there is only one tab open, this will close the window.</span></span>

<span data-ttu-id="f9b67-347">**Nome del comando:** `closePane`</span><span class="sxs-lookup"><span data-stu-id="f9b67-347">**Command name:** `closePane`</span></span>

<span data-ttu-id="f9b67-348">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-348">**Default binding:**</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a><span data-ttu-id="f9b67-349">Sposta stato attivo nel riquadro</span><span class="sxs-lookup"><span data-stu-id="f9b67-349">Move pane focus</span></span>

<span data-ttu-id="f9b67-350">Consente di spostare lo stato attivo in un altro riquadro a seconda della direzione.</span><span class="sxs-lookup"><span data-stu-id="f9b67-350">This changes focus to a different pane depending on the direction.</span></span>

<span data-ttu-id="f9b67-351">**Nome del comando:** `moveFocus`</span><span class="sxs-lookup"><span data-stu-id="f9b67-351">**Command name:** `moveFocus`</span></span>

<span data-ttu-id="f9b67-352">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-352">**Default bindings:**</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-353">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-353">Actions</span></span>

| <span data-ttu-id="f9b67-354">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-354">Name</span></span> | <span data-ttu-id="f9b67-355">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-355">Necessity</span></span> | <span data-ttu-id="f9b67-356">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-356">Accepts</span></span> | <span data-ttu-id="f9b67-357">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-357">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="f9b67-358">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-358">Required</span></span> | <span data-ttu-id="f9b67-359">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="f9b67-359">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="f9b67-360">Direzione in cui viene spostato lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="f9b67-360">Direction in which the focus will move.</span></span> |

### <a name="zoom-a-pane-preview"></a><span data-ttu-id="f9b67-361">Zoom di un riquadro ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="f9b67-361">Zoom a pane ([Preview](https://aka.ms/terminal-preview))</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="f9b67-362">In questo modo si espande il riquadro con lo stato attivo per riempire l'intero contenuto della finestra.</span><span class="sxs-lookup"><span data-stu-id="f9b67-362">This expands the focused pane to fill the entire contents of the window.</span></span>

<span data-ttu-id="f9b67-363">**Nome del comando:** `togglePaneZoom`</span><span class="sxs-lookup"><span data-stu-id="f9b67-363">**Command name:** `togglePaneZoom`</span></span>

<span data-ttu-id="f9b67-364">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-364">**Default binding:**</span></span>

```json
{ "command": "togglePaneZoom" }
```

:::column-end:::
:::column span="":::
![Zoom del riquadro di attivazione/disconnessione del terminale di Windows](./../images/toggle-pane-zoom.gif)

:::column-end:::
:::row-end:::

> [!IMPORTANT]
> <span data-ttu-id="f9b67-366">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="f9b67-366">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="resize-a-pane"></a><span data-ttu-id="f9b67-367">Ridimensiona un riquadro</span><span class="sxs-lookup"><span data-stu-id="f9b67-367">Resize a pane</span></span>

<span data-ttu-id="f9b67-368">Modifica le dimensioni del riquadro attivo.</span><span class="sxs-lookup"><span data-stu-id="f9b67-368">This changes the size of the active pane.</span></span>

<span data-ttu-id="f9b67-369">**Nome del comando:** `resizePane`</span><span class="sxs-lookup"><span data-stu-id="f9b67-369">**Command name:** `resizePane`</span></span>

<span data-ttu-id="f9b67-370">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-370">**Default bindings:**</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-371">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-371">Actions</span></span>

| <span data-ttu-id="f9b67-372">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-372">Name</span></span> | <span data-ttu-id="f9b67-373">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-373">Necessity</span></span> | <span data-ttu-id="f9b67-374">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-374">Accepts</span></span> | <span data-ttu-id="f9b67-375">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-375">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="f9b67-376">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-376">Required</span></span> | <span data-ttu-id="f9b67-377">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="f9b67-377">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="f9b67-378">Direzione in cui verranno modificate le dimensioni del riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-378">Direction in which the pane will be resized.</span></span> |

### <a name="split-a-pane"></a><span data-ttu-id="f9b67-379">Dividi un riquadro</span><span class="sxs-lookup"><span data-stu-id="f9b67-379">Split a pane</span></span>

<span data-ttu-id="f9b67-380">Divide a metà il riquadro attivo e ne apre un altro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-380">This halves the size of the active pane and opens another.</span></span> <span data-ttu-id="f9b67-381">Se viene specificato senza argomenti, il profilo predefinito verrà aperto nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-381">Without any arguments, this will open the default profile in the new pane.</span></span> <span data-ttu-id="f9b67-382">Se non viene specificata un'azione, verrà usata l'impostazione equivalente del profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="f9b67-382">If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="f9b67-383">**Nome del comando:** `splitPane`</span><span class="sxs-lookup"><span data-stu-id="f9b67-383">**Command name:** `splitPane`</span></span>

<span data-ttu-id="f9b67-384">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-384">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal"}, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical"}, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-385">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-385">Actions</span></span>

| <span data-ttu-id="f9b67-386">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-386">Name</span></span> | <span data-ttu-id="f9b67-387">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-387">Necessity</span></span> | <span data-ttu-id="f9b67-388">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-388">Accepts</span></span> | <span data-ttu-id="f9b67-389">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-389">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `split` | <span data-ttu-id="f9b67-390">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-390">Required</span></span> | <span data-ttu-id="f9b67-391">`"vertical"`, `"horizontal"`, `"auto"`</span><span class="sxs-lookup"><span data-stu-id="f9b67-391">`"vertical"`, `"horizontal"`, `"auto"`</span></span> | <span data-ttu-id="f9b67-392">Modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-392">How the pane will split.</span></span> <span data-ttu-id="f9b67-393">Con `"auto"` il riquadro verrà diviso nella direzione che offre l'area con la superficie più estesa.</span><span class="sxs-lookup"><span data-stu-id="f9b67-393">`"auto"` will split in the direction that provides the most surface area.</span></span> |
| `commandline` | <span data-ttu-id="f9b67-394">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-394">Optional</span></span> | <span data-ttu-id="f9b67-395">Nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="f9b67-395">Executable file name as a string</span></span> | <span data-ttu-id="f9b67-396">Esegue l'eseguibile all'interno del riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-396">Executable run within the pane.</span></span> |
| `startingDirectory` | <span data-ttu-id="f9b67-397">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-397">Optional</span></span> | <span data-ttu-id="f9b67-398">Percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="f9b67-398">Folder location as a string</span></span> | <span data-ttu-id="f9b67-399">Directory in cui verrà aperto il riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-399">Directory in which the pane will open.</span></span> |
| `tabTitle` | <span data-ttu-id="f9b67-400">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-400">Optional</span></span> | <span data-ttu-id="f9b67-401">String</span><span class="sxs-lookup"><span data-stu-id="f9b67-401">String</span></span> | <span data-ttu-id="f9b67-402">Titolo della scheda quando lo stato attivo si trova nel nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-402">Title of the tab when the new pane is focused.</span></span> |
| `index` | <span data-ttu-id="f9b67-403">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-403">Optional</span></span> | <span data-ttu-id="f9b67-404">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-404">Integer</span></span> | <span data-ttu-id="f9b67-405">Profilo che verrà aperto in base alla relativa posizione nel menu a discesa (a partire da 0).</span><span class="sxs-lookup"><span data-stu-id="f9b67-405">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="f9b67-406">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-406">Optional</span></span> | <span data-ttu-id="f9b67-407">Nome o GUID del profilo in formato stringa</span><span class="sxs-lookup"><span data-stu-id="f9b67-407">Profile's name or GUID as a string</span></span> | <span data-ttu-id="f9b67-408">Profilo che verrà aperto in base al relativo nome o GUID.</span><span class="sxs-lookup"><span data-stu-id="f9b67-408">Profile that will open based on its GUID or name.</span></span> |
| `splitMode` | <span data-ttu-id="f9b67-409">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-409">Optional</span></span> | `"duplicate"` | <span data-ttu-id="f9b67-410">Controlla la modalità di divisione del riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-410">Controls how the pane splits.</span></span> <span data-ttu-id="f9b67-411">Accetta solo `"duplicate"`, con cui il profilo del riquadro con lo stato attivo viene duplicato in un nuovo riquadro.</span><span class="sxs-lookup"><span data-stu-id="f9b67-411">Only accepts `"duplicate"`, which will duplicate the focused pane's profile into a new pane.</span></span> |

<br />

___

## <a name="clipboard-integration-commands"></a><span data-ttu-id="f9b67-412">Comandi di integrazione degli Appunti</span><span class="sxs-lookup"><span data-stu-id="f9b67-412">Clipboard integration commands</span></span>

### <a name="copy"></a><span data-ttu-id="f9b67-413">Copia</span><span class="sxs-lookup"><span data-stu-id="f9b67-413">Copy</span></span>

<span data-ttu-id="f9b67-414">Copia il contenuto del terminale selezionato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="f9b67-414">This copies the selected terminal content to your clipboard.</span></span>

<span data-ttu-id="f9b67-415">**Nome del comando:** `copy`</span><span class="sxs-lookup"><span data-stu-id="f9b67-415">**Command name:** `copy`</span></span>

<span data-ttu-id="f9b67-416">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-416">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-417">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-417">Actions</span></span>

| <span data-ttu-id="f9b67-418">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-418">Name</span></span> | <span data-ttu-id="f9b67-419">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-419">Necessity</span></span> | <span data-ttu-id="f9b67-420">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-420">Accepts</span></span> | <span data-ttu-id="f9b67-421">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-421">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `singleLine` | <span data-ttu-id="f9b67-422">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-422">Optional</span></span> | <span data-ttu-id="f9b67-423">`true`, `false`</span><span class="sxs-lookup"><span data-stu-id="f9b67-423">`true`, `false`</span></span> | <span data-ttu-id="f9b67-424">Quando è `true`, il contenuto copiato verrà copiato come una riga singola.</span><span class="sxs-lookup"><span data-stu-id="f9b67-424">When `true`, the copied content will be copied as a single line.</span></span> <span data-ttu-id="f9b67-425">Quando è `false`, i caratteri di nuova riga del testo selezionato vengono mantenuti.</span><span class="sxs-lookup"><span data-stu-id="f9b67-425">When `false`, newlines persist from the selected text.</span></span> |
| `copyFormatting` | <span data-ttu-id="f9b67-426">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-426">Optional</span></span> | <span data-ttu-id="f9b67-427">`true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"`</span><span class="sxs-lookup"><span data-stu-id="f9b67-427">`true`, `false`, `"all"`, `"none"`, `"html"`, `"rtf"`</span></span> | <span data-ttu-id="f9b67-428">Quando `true` , anche il colore e la formattazione dei caratteri del testo selezionato vengono copiati negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="f9b67-428">When `true`, the color and font formatting of the selected text is also copied to your clipboard.</span></span> <span data-ttu-id="f9b67-429">Quando `false` , solo il testo normale viene copiato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="f9b67-429">When `false`, only plain text is copied to your clipboard.</span></span> <span data-ttu-id="f9b67-430">È inoltre possibile specificare i formati che si desidera copiare.</span><span class="sxs-lookup"><span data-stu-id="f9b67-430">You can also specify which formats you would like to copy.</span></span> <span data-ttu-id="f9b67-431">Se `null` , il `"copyFormatting"` comportamento globale viene ereditato.</span><span class="sxs-lookup"><span data-stu-id="f9b67-431">When `null`, the global `"copyFormatting"` behavior is inherited.</span></span> |

### <a name="paste"></a><span data-ttu-id="f9b67-432">Incolla</span><span class="sxs-lookup"><span data-stu-id="f9b67-432">Paste</span></span>

<span data-ttu-id="f9b67-433">Inserisce il contenuto copiato negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="f9b67-433">This inserts the content that was copied onto the clipboard.</span></span>

<span data-ttu-id="f9b67-434">**Nome del comando:** `paste`</span><span class="sxs-lookup"><span data-stu-id="f9b67-434">**Command name:** `paste`</span></span>

<span data-ttu-id="f9b67-435">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-435">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a><span data-ttu-id="f9b67-436">Comandi di scorrimento</span><span class="sxs-lookup"><span data-stu-id="f9b67-436">Scrollback commands</span></span>

### <a name="scroll-up"></a><span data-ttu-id="f9b67-437">Scorri verso l'alto</span><span class="sxs-lookup"><span data-stu-id="f9b67-437">Scroll up</span></span>

<span data-ttu-id="f9b67-438">Scorre lo schermo verso l'alto in base al numero di righe definito da `"rowsToScroll"` .</span><span class="sxs-lookup"><span data-stu-id="f9b67-438">This scrolls the screen up by the number of rows defined by `"rowsToScroll"`.</span></span> <span data-ttu-id="f9b67-439">Se `"rowsToScroll"` non viene specificato, scorrerà verso l'alto la quantità definita dall'impostazione predefinita del sistema, ovvero la stessa quantità di scorrimento del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9b67-439">If `"rowsToScroll"` is not provided, it will scroll up the amount defined by the system default, which is the same amount as mouse scrolling.</span></span>

<span data-ttu-id="f9b67-440">**Nome del comando:** `scrollUp`</span><span class="sxs-lookup"><span data-stu-id="f9b67-440">**Command name:** `scrollUp`</span></span>

<span data-ttu-id="f9b67-441">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-441">**Default binding:**</span></span>

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-442">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-442">Actions</span></span>

| <span data-ttu-id="f9b67-443">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-443">Name</span></span> | <span data-ttu-id="f9b67-444">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-444">Necessity</span></span> | <span data-ttu-id="f9b67-445">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-445">Accepts</span></span> | <span data-ttu-id="f9b67-446">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-446">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `rowsToScroll` | <span data-ttu-id="f9b67-447">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-447">Optional</span></span> | <span data-ttu-id="f9b67-448">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-448">Integer</span></span> | <span data-ttu-id="f9b67-449">Numero di righe da scorrere.</span><span class="sxs-lookup"><span data-stu-id="f9b67-449">The number of rows to scroll.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="f9b67-450">L' `"rowsToScroll"` azione è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="f9b67-450">The `"rowsToScroll"` action is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="scroll-down"></a><span data-ttu-id="f9b67-451">Scorri verso il basso</span><span class="sxs-lookup"><span data-stu-id="f9b67-451">Scroll down</span></span>

<span data-ttu-id="f9b67-452">Scorre lo schermo verso il basso in base al numero di righe definito da `"rowsToScroll"` .</span><span class="sxs-lookup"><span data-stu-id="f9b67-452">This scrolls the screen down by the number of rows defined by `"rowsToScroll"`.</span></span> <span data-ttu-id="f9b67-453">Se `"rowsToScroll"` non viene specificato, scorre verso il basso la quantità definita dall'impostazione predefinita del sistema, che corrisponde allo scorrimento del mouse.</span><span class="sxs-lookup"><span data-stu-id="f9b67-453">If `"rowsToScroll"` is not provided, it will scroll down the amount defined by the system default, which is the same amount as mouse scrolling.</span></span>

<span data-ttu-id="f9b67-454">**Nome del comando:** `scrollDown`</span><span class="sxs-lookup"><span data-stu-id="f9b67-454">**Command name:** `scrollDown`</span></span>

<span data-ttu-id="f9b67-455">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-455">**Default binding:**</span></span>

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-456">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-456">Actions</span></span>

| <span data-ttu-id="f9b67-457">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-457">Name</span></span> | <span data-ttu-id="f9b67-458">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-458">Necessity</span></span> | <span data-ttu-id="f9b67-459">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-459">Accepts</span></span> | <span data-ttu-id="f9b67-460">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-460">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `rowsToScroll` | <span data-ttu-id="f9b67-461">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="f9b67-461">Optional</span></span> | <span data-ttu-id="f9b67-462">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-462">Integer</span></span> | <span data-ttu-id="f9b67-463">Numero di righe da scorrere.</span><span class="sxs-lookup"><span data-stu-id="f9b67-463">The number of rows to scroll.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="f9b67-464">L' `"rowsToScroll"` azione è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="f9b67-464">The `"rowsToScroll"` action is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="scroll-up-a-whole-page"></a><span data-ttu-id="f9b67-465">Scorri verso l'alto di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="f9b67-465">Scroll up a whole page</span></span>

<span data-ttu-id="f9b67-466">Scorre lo schermo verso l'alto di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="f9b67-466">This scrolls the screen up by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="f9b67-467">**Nome del comando:** `scrollUpPage`</span><span class="sxs-lookup"><span data-stu-id="f9b67-467">**Command name:** `scrollUpPage`</span></span>

<span data-ttu-id="f9b67-468">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-468">**Default binding:**</span></span>

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a><span data-ttu-id="f9b67-469">Scorri verso il basso di una pagina intera</span><span class="sxs-lookup"><span data-stu-id="f9b67-469">Scroll down a whole page</span></span>

<span data-ttu-id="f9b67-470">Scorre lo schermo verso il basso di una pagina intera, che corrisponde all'altezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="f9b67-470">This scrolls the screen down by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="f9b67-471">**Nome del comando:** `scrollDownPage`</span><span class="sxs-lookup"><span data-stu-id="f9b67-471">**Command name:** `scrollDownPage`</span></span>

<span data-ttu-id="f9b67-472">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-472">**Default binding:**</span></span>

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

<br />

___

## <a name="visual-adjustment-commands"></a><span data-ttu-id="f9b67-473">Comandi di regolazione della visualizzazione</span><span class="sxs-lookup"><span data-stu-id="f9b67-473">Visual adjustment commands</span></span>

### <a name="adjust-font-size"></a><span data-ttu-id="f9b67-474">Regola dimensioni caratteri</span><span class="sxs-lookup"><span data-stu-id="f9b67-474">Adjust font size</span></span>

<span data-ttu-id="f9b67-475">Modifica le dimensioni del testo in base al numero di punti specificato.</span><span class="sxs-lookup"><span data-stu-id="f9b67-475">This changes the text size by a specified point amount.</span></span>

<span data-ttu-id="f9b67-476">**Nome del comando:** `adjustFontSize`</span><span class="sxs-lookup"><span data-stu-id="f9b67-476">**Command name:** `adjustFontSize`</span></span>

<span data-ttu-id="f9b67-477">**Associazioni predefinite:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-477">**Default bindings:**</span></span>

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a><span data-ttu-id="f9b67-478">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-478">Actions</span></span>

| <span data-ttu-id="f9b67-479">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-479">Name</span></span> | <span data-ttu-id="f9b67-480">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-480">Necessity</span></span> | <span data-ttu-id="f9b67-481">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-481">Accepts</span></span> | <span data-ttu-id="f9b67-482">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-482">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `delta` | <span data-ttu-id="f9b67-483">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-483">Required</span></span> | <span data-ttu-id="f9b67-484">Intero</span><span class="sxs-lookup"><span data-stu-id="f9b67-484">Integer</span></span> | <span data-ttu-id="f9b67-485">Modifiche applicate alle dimensioni per ogni chiamata del comando.</span><span class="sxs-lookup"><span data-stu-id="f9b67-485">Amount of size change per command invocation.</span></span> |

### <a name="reset-font-size"></a><span data-ttu-id="f9b67-486">Reimposta dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="f9b67-486">Reset font size</span></span>

<span data-ttu-id="f9b67-487">Reimposta le dimensioni del testo in base al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f9b67-487">This resets the text size to the default value.</span></span>

<span data-ttu-id="f9b67-488">**Nome del comando:** `resetFontSize`</span><span class="sxs-lookup"><span data-stu-id="f9b67-488">**Command name:** `resetFontSize`</span></span>

<span data-ttu-id="f9b67-489">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-489">**Default binding:**</span></span>

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

### <a name="toggle-retro-terminal-effects"></a><span data-ttu-id="f9b67-490">Imposta/Rimuovi effetti terminali retro</span><span class="sxs-lookup"><span data-stu-id="f9b67-490">Toggle retro terminal effects</span></span>

<span data-ttu-id="f9b67-491">Questo consente di attivare o disabilitare il "effetto terminale retrò", che è abilitato con l'impostazione del profilo `experimental.retroTerminalEffect` .</span><span class="sxs-lookup"><span data-stu-id="f9b67-491">This toggles the "retro terminal effect", which is enabled with the profile setting `experimental.retroTerminalEffect`.</span></span>

<span data-ttu-id="f9b67-492">**Nome del comando:** `toggleRetroEffect`</span><span class="sxs-lookup"><span data-stu-id="f9b67-492">**Command name:** `toggleRetroEffect`</span></span>

<span data-ttu-id="f9b67-493">**Associazione predefinita:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-493">**Default binding:**</span></span>

```json
{ "command": "toggleRetroEffect" }
```

### <a name="set-the-color-scheme"></a><span data-ttu-id="f9b67-494">Imposta la combinazione di colori</span><span class="sxs-lookup"><span data-stu-id="f9b67-494">Set the color scheme</span></span>

<span data-ttu-id="f9b67-495">Modifica la combinazione di colori attiva.</span><span class="sxs-lookup"><span data-stu-id="f9b67-495">Changes the active color scheme.</span></span>

<span data-ttu-id="f9b67-496">**Nome del comando:** `setColorScheme`</span><span class="sxs-lookup"><span data-stu-id="f9b67-496">**Command name:** `setColorScheme`</span></span>

#### <a name="actions"></a><span data-ttu-id="f9b67-497">Azioni</span><span class="sxs-lookup"><span data-stu-id="f9b67-497">Actions</span></span>

| <span data-ttu-id="f9b67-498">Nome</span><span class="sxs-lookup"><span data-stu-id="f9b67-498">Name</span></span> | <span data-ttu-id="f9b67-499">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-499">Necessity</span></span> | <span data-ttu-id="f9b67-500">Tipo accettato</span><span class="sxs-lookup"><span data-stu-id="f9b67-500">Accepts</span></span> | <span data-ttu-id="f9b67-501">Description</span><span class="sxs-lookup"><span data-stu-id="f9b67-501">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `colorScheme` | <span data-ttu-id="f9b67-502">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="f9b67-502">Required</span></span> | <span data-ttu-id="f9b67-503">string</span><span class="sxs-lookup"><span data-stu-id="f9b67-503">String</span></span> | <span data-ttu-id="f9b67-504">Oggetto `name` della combinazione di colori da applicare.</span><span class="sxs-lookup"><span data-stu-id="f9b67-504">The `name` of the color scheme to apply.</span></span> |

<span data-ttu-id="f9b67-505">**Associazione di esempio:**</span><span class="sxs-lookup"><span data-stu-id="f9b67-505">**Example binding:**</span></span>

```json
{ "command": { "action": "setColorScheme", "colorScheme": "Campbell" }, "keys": "" }
```

<br />

___

## <a name="unbind-keys"></a><span data-ttu-id="f9b67-506">Disassocia tasti</span><span class="sxs-lookup"><span data-stu-id="f9b67-506">Unbind keys</span></span>

<span data-ttu-id="f9b67-507">Annulla l'associazione dei tasti per tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="f9b67-507">This unbinds the associated keys from any command.</span></span>

<span data-ttu-id="f9b67-508">**Nome del comando:** `unbound`</span><span class="sxs-lookup"><span data-stu-id="f9b67-508">**Command name:** `unbound`</span></span>
