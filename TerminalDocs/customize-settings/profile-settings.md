---
title: Terminale Windows - Impostazioni del profilo
description: Informazioni su come personalizzare i singoli profili in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 309fb40736718df7d1670a7376806b70ef0e35fe
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416086"
---
# <a name="profile-settings-in-the-windows-terminal"></a><span data-ttu-id="39840-103">Impostazioni del profilo in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="39840-103">Profile settings in the Windows Terminal</span></span>

<span data-ttu-id="39840-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="39840-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="39840-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="39840-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

```json
"defaults":
{
    // SETTINGS TO APPLY TO ALL PROFILES
},
"list":
[
    // PROFILE OBJECTS
]
```

## <a name="unique-identifier"></a><span data-ttu-id="39840-106">Identificatore univoco</span><span class="sxs-lookup"><span data-stu-id="39840-106">Unique identifier</span></span>

<span data-ttu-id="39840-107">I profili possono usare un GUID come identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="39840-107">Profiles can use a GUID as a unique identifier.</span></span> <span data-ttu-id="39840-108">Per impostare un profilo come predefinito, è necessario un GUID per l'impostazione globale `defaultProfile`.</span><span class="sxs-lookup"><span data-stu-id="39840-108">To make a profile your default profile, it needs a GUID for the `defaultProfile` global setting.</span></span>

<span data-ttu-id="39840-109">**Nome della proprietà:** `guid`</span><span class="sxs-lookup"><span data-stu-id="39840-109">**Property name:** `guid`</span></span>

<span data-ttu-id="39840-110">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="39840-110">**Necessity:** Required</span></span>

<span data-ttu-id="39840-111">**Accetta:** GUID in formato stringa del Registro di sistema: `"{00000000-0000-0000-0000-000000000000}"`</span><span class="sxs-lookup"><span data-stu-id="39840-111">**Accepts:** GUID as a string in registry format: `"{00000000-0000-0000-0000-000000000000}"`</span></span>

<br />

___

## <a name="executable-settings"></a><span data-ttu-id="39840-112">Impostazioni per file eseguibili</span><span class="sxs-lookup"><span data-stu-id="39840-112">Executable settings</span></span>

### <a name="command-line"></a><span data-ttu-id="39840-113">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="39840-113">Command line</span></span>

<span data-ttu-id="39840-114">File eseguibile usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-114">This is the executable used in the profile.</span></span>

<span data-ttu-id="39840-115">**Nome della proprietà:** `commandline`</span><span class="sxs-lookup"><span data-stu-id="39840-115">**Property name:** `commandline`</span></span>

<span data-ttu-id="39840-116">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-116">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-117">**Accetta:** nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="39840-117">**Accepts:** Executable file name as a string</span></span>

<span data-ttu-id="39840-118">**Valore predefinito:** `"cmd.exe"`</span><span class="sxs-lookup"><span data-stu-id="39840-118">**Default value:** `"cmd.exe"`</span></span>

### <a name="source"></a><span data-ttu-id="39840-119">Origine</span><span class="sxs-lookup"><span data-stu-id="39840-119">Source</span></span>

<span data-ttu-id="39840-120">Archivia il nome del generatore di profili che ha originato il profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-120">This stores the name of the profile generator that originated the profile.</span></span> <span data-ttu-id="39840-121">_Non esistono valori individuabili per questo campo._</span><span class="sxs-lookup"><span data-stu-id="39840-121">_There are no discoverable values for this field._</span></span> <span data-ttu-id="39840-122">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="39840-122">For additional information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="39840-123">**Nome della proprietà:** `source`</span><span class="sxs-lookup"><span data-stu-id="39840-123">**Property name:** `source`</span></span>

<span data-ttu-id="39840-124">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-124">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-125">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="39840-125">**Accepts:** String</span></span>

### <a name="starting-directory"></a><span data-ttu-id="39840-126">Directory iniziale</span><span class="sxs-lookup"><span data-stu-id="39840-126">Starting directory</span></span>

<span data-ttu-id="39840-127">Directory in cui viene avviata la shell quando viene caricata.</span><span class="sxs-lookup"><span data-stu-id="39840-127">This is the directory the shell starts in when it is loaded.</span></span>

<span data-ttu-id="39840-128">**Nome della proprietà:** `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="39840-128">**Property name:** `startingDirectory`</span></span>

<span data-ttu-id="39840-129">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-129">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-130">**Accetta:** percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="39840-130">**Accepts:** Folder location as a string</span></span>

<span data-ttu-id="39840-131">**Valore predefinito:** `"%USERPROFILE%"`</span><span class="sxs-lookup"><span data-stu-id="39840-131">**Default value:** `"%USERPROFILE%"`</span></span>

<br />

___

## <a name="dropdown-settings"></a><span data-ttu-id="39840-132">Impostazioni per il menu a discesa</span><span class="sxs-lookup"><span data-stu-id="39840-132">Dropdown settings</span></span>

<span data-ttu-id="39840-133">![Terminale Windows - Menu a discesa](./../images/dropdown.png)
_Configurazione: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="39840-133">![Windows Terminal dropdown](./../images/dropdown.png)
_Configuration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

### <a name="name"></a><span data-ttu-id="39840-134">Nome</span><span class="sxs-lookup"><span data-stu-id="39840-134">Name</span></span>

<span data-ttu-id="39840-135">Nome del profilo che verrà visualizzato nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="39840-135">This is the name of the profile that will be displayed in the dropdown menu.</span></span> <span data-ttu-id="39840-136">Questo valore viene usato anche come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="39840-136">This value is also used as the "title" to pass to the shell on startup.</span></span> <span data-ttu-id="39840-137">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="39840-137">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="39840-138">Per eseguire l'override di questo comportamento del titolo, usa `tabTitle`.</span><span class="sxs-lookup"><span data-stu-id="39840-138">This "title" behavior can be overridden by using `tabTitle`.</span></span>

<span data-ttu-id="39840-139">**Nome della proprietà:** `name`</span><span class="sxs-lookup"><span data-stu-id="39840-139">**Property name:** `name`</span></span>

<span data-ttu-id="39840-140">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="39840-140">**Necessity:** Required</span></span>

<span data-ttu-id="39840-141">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="39840-141">**Accepts:** String</span></span>

### <a name="icon"></a><span data-ttu-id="39840-142">Icona</span><span class="sxs-lookup"><span data-stu-id="39840-142">Icon</span></span>

<span data-ttu-id="39840-143">Consente di impostare l'icona visualizzata all'interno della scheda e nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="39840-143">This sets the icon that displays within the tab and the dropdown menu.</span></span>

<span data-ttu-id="39840-144">**Nome della proprietà:** `icon`</span><span class="sxs-lookup"><span data-stu-id="39840-144">**Property name:** `icon`</span></span>

<span data-ttu-id="39840-145">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-145">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-146">**Accetta:** percorso del file in formato stringa</span><span class="sxs-lookup"><span data-stu-id="39840-146">**Accepts:** File location as a string</span></span>

### <a name="hide-a-profile-from-the-dropdown"></a><span data-ttu-id="39840-147">Nascondi un profilo nell'elenco a discesa</span><span class="sxs-lookup"><span data-stu-id="39840-147">Hide a profile from the dropdown</span></span>

<span data-ttu-id="39840-148">Se `hidden` è impostato su `true`, il profilo non verrà visualizzato nell'elenco dei profili.</span><span class="sxs-lookup"><span data-stu-id="39840-148">If `hidden` is set to `true`, the profile will not appear in the list of profiles.</span></span> <span data-ttu-id="39840-149">Può essere usata per nascondere i profili predefiniti e quelli generati dinamicamente, lasciandoli nel file settings.</span><span class="sxs-lookup"><span data-stu-id="39840-149">This can be used to hide default profiles and dynamically generated profiles, while leaving them in your settings file.</span></span> <span data-ttu-id="39840-150">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="39840-150">To learn more about dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="39840-151">**Nome della proprietà:** `hidden`</span><span class="sxs-lookup"><span data-stu-id="39840-151">**Property name:** `hidden`</span></span>

<span data-ttu-id="39840-152">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-152">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-153">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="39840-153">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="39840-154">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="39840-154">**Default value:** `false`</span></span>

<br />

___

## <a name="tab-title-settings"></a><span data-ttu-id="39840-155">Impostazioni per i titoli delle schede</span><span class="sxs-lookup"><span data-stu-id="39840-155">Tab title settings</span></span>

### <a name="custom-tab-title"></a><span data-ttu-id="39840-156">Titolo scheda personalizzato</span><span class="sxs-lookup"><span data-stu-id="39840-156">Custom tab title</span></span>

<span data-ttu-id="39840-157">Se è impostata, sostituirà `name` come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="39840-157">If set, this will replace the `name` as the title to pass to the shell on startup.</span></span> <span data-ttu-id="39840-158">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="39840-158">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="39840-159">Per informazioni su come impostare la shell come titolo, vedi l'[esercitazione relativa al titolo della scheda](./../tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="39840-159">If you'd like to learn how to have the shell set your title, visit the [tab title tutorial](./../tutorials/tab-title.md).</span></span>

<span data-ttu-id="39840-160">**Nome della proprietà:** `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="39840-160">**Property name:** `tabTitle`</span></span>

<span data-ttu-id="39840-161">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-161">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-162">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="39840-162">**Accepts:** String</span></span>

### <a name="suppress-title-changes-from-the-shell"></a><span data-ttu-id="39840-163">Non visualizzare le modifiche apportate al titolo dalla shell</span><span class="sxs-lookup"><span data-stu-id="39840-163">Suppress title changes from the shell</span></span>

<span data-ttu-id="39840-164">Quando è impostata su `true`, `tabTitle` sostituisce il titolo predefinito della scheda. Tutti i messaggi di modifica del titolo dall'applicazione verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="39840-164">When this is set to `true`, `tabTitle` overrides the default title of the tab and any title change messages from the application will be suppressed.</span></span> <span data-ttu-id="39840-165">Se `tabTitle` non è impostata, verrà usata `name`.</span><span class="sxs-lookup"><span data-stu-id="39840-165">If `tabTitle` isn't set, `name` will be used instead.</span></span> <span data-ttu-id="39840-166">Quando è impostata su `false`, `tabTitle` si comporta normalmente.</span><span class="sxs-lookup"><span data-stu-id="39840-166">When this is set to `false`, `tabTitle` behaves as normal.</span></span>

<span data-ttu-id="39840-167">**Nome della proprietà:** `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="39840-167">**Property name:** `suppressApplicationTitle`</span></span>

<span data-ttu-id="39840-168">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-168">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-169">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="39840-169">**Accepts:** `true`, `false`</span></span>

<br />

___

## <a name="text-settings"></a><span data-ttu-id="39840-170">Impostazioni per il testo</span><span class="sxs-lookup"><span data-stu-id="39840-170">Text settings</span></span>

### <a name="font-face"></a><span data-ttu-id="39840-171">Tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="39840-171">Font face</span></span>

<span data-ttu-id="39840-172">Nome del tipo di carattere usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-172">This is the name of the font face used in the profile.</span></span> <span data-ttu-id="39840-173">Il terminale proverà ad eseguire il fallback a Consolas se non riesce a trovarlo o non è valido.</span><span class="sxs-lookup"><span data-stu-id="39840-173">The terminal will try to fallback to Consolas if this can't be found or is invalid.</span></span> <span data-ttu-id="39840-174">Per informazioni sulle altre varianti del tipo di carattere predefinito, Cascadia Mono, vedi la [tabella codici di Cascadia](./../cascadia-code.md).</span><span class="sxs-lookup"><span data-stu-id="39840-174">To learn about the other variants of the default font, Cascadia Mono, visit the [Cascadia Code page](./../cascadia-code.md).</span></span>

<span data-ttu-id="39840-175">**Nome della proprietà:** `fontFace`</span><span class="sxs-lookup"><span data-stu-id="39840-175">**Property name:** `fontFace`</span></span>

<span data-ttu-id="39840-176">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-176">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-177">**Accetta:** nome del tipo di carattere in formato stringa</span><span class="sxs-lookup"><span data-stu-id="39840-177">**Accepts:** Font name as a string</span></span>

<span data-ttu-id="39840-178">**Valore predefinito:** `"Cascadia Mono"`</span><span class="sxs-lookup"><span data-stu-id="39840-178">**Default value:** `"Cascadia Mono"`</span></span>

### <a name="font-size"></a><span data-ttu-id="39840-179">Dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="39840-179">Font size</span></span>

<span data-ttu-id="39840-180">Consente di impostare le dimensioni del carattere del profilo in punti.</span><span class="sxs-lookup"><span data-stu-id="39840-180">This sets the profile's font size in points.</span></span>

<span data-ttu-id="39840-181">**Nome della proprietà:** `fontSize`</span><span class="sxs-lookup"><span data-stu-id="39840-181">**Property name:** `fontSize`</span></span>

<span data-ttu-id="39840-182">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-182">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-183">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="39840-183">**Accepts:** Integer</span></span>

<span data-ttu-id="39840-184">**Valore predefinito:** `12`</span><span class="sxs-lookup"><span data-stu-id="39840-184">**Default value:** `12`</span></span>

### <a name="padding"></a><span data-ttu-id="39840-185">Spaziatura interna</span><span class="sxs-lookup"><span data-stu-id="39840-185">Padding</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="39840-186">Consente di impostare la spaziatura intorno al testo all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="39840-186">This sets the padding around the text within the window.</span></span> <span data-ttu-id="39840-187">Vengono accettati tre diversi formati: `"#"` imposta la stessa spaziatura interna su tutti i lati, `"#, #"` imposta la stessa spaziatura interna per left-right e top-bottom, mentre `"#, #, #, #"` imposta la spaziatura interna singolarmente per left, top, right e bottom.</span><span class="sxs-lookup"><span data-stu-id="39840-187">This will accept three different formats: `"#"` sets the same padding for all sides, `"#, #"` sets the same padding for left-right and top-bottom, and `"#, #, #, #"` sets the padding individually for left, top, right, and bottom.</span></span>

<span data-ttu-id="39840-188">**Nome della proprietà:** `padding`</span><span class="sxs-lookup"><span data-stu-id="39840-188">**Property name:** `padding`</span></span>

<span data-ttu-id="39840-189">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-189">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-190">**Accetta:** valori nei formati stringa seguenti: `"#"`, `"#, #"`, `"#, #, #, #"`</span><span class="sxs-lookup"><span data-stu-id="39840-190">**Accepts:** Values as a string in the following formats: `"#"`, `"#, #"`, `"#, #, #, #"`</span></span>

<span data-ttu-id="39840-191">**Valore predefinito:** `"8, 8, 8, 8"`</span><span class="sxs-lookup"><span data-stu-id="39840-191">**Default value:** `"8, 8, 8, 8"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Spaziatura interna](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="antialiasing-text"></a><span data-ttu-id="39840-193">Anti-aliasing del testo</span><span class="sxs-lookup"><span data-stu-id="39840-193">Antialiasing text</span></span>

<span data-ttu-id="39840-194">Controlla la modalità di anti-aliasing del testo nel renderer.</span><span class="sxs-lookup"><span data-stu-id="39840-194">This controls how text is antialiased in the renderer.</span></span> <span data-ttu-id="39840-195">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="39840-195">Note that changing this setting will require starting a new terminal instance.</span></span>

![Terminale Windows - Anti-aliasing del testo](./../images/antialiasing-mode.gif)

<span data-ttu-id="39840-197">**Nome della proprietà:** `antialiasingMode`</span><span class="sxs-lookup"><span data-stu-id="39840-197">**Property name:** `antialiasingMode`</span></span>

<span data-ttu-id="39840-198">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-198">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-199">**Accetta:** `"grayscale"`, `"cleartype"`, `"aliased"`</span><span class="sxs-lookup"><span data-stu-id="39840-199">**Accepts:** `"grayscale"`, `"cleartype"`, `"aliased"`</span></span>

<span data-ttu-id="39840-200">**Valore predefinito:** `"grayscale"`</span><span class="sxs-lookup"><span data-stu-id="39840-200">**Default value:** `"grayscale"`</span></span>

<br />

___

## <a name="cursor-settings"></a><span data-ttu-id="39840-201">Impostazioni per il cursore</span><span class="sxs-lookup"><span data-stu-id="39840-201">Cursor settings</span></span>

### <a name="cursor-shape"></a><span data-ttu-id="39840-202">Forma del cursore</span><span class="sxs-lookup"><span data-stu-id="39840-202">Cursor shape</span></span>

<span data-ttu-id="39840-203">Consente di impostare la forma del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-203">This sets the cursor shape for the profile.</span></span> <span data-ttu-id="39840-204">I cursori possibili sono i seguenti: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;)</span><span class="sxs-lookup"><span data-stu-id="39840-204">The possible cursors are as follows: `"bar"` ( &#x2503; ), `"vintage"` ( &#x2583; ), `"underscore"` ( &#x2581; ), `"filledBox"` ( &#x2588; ), `"emptyBox"` ( &#x25AF; )</span></span>

<span data-ttu-id="39840-205">**Nome della proprietà:** `cursorShape`</span><span class="sxs-lookup"><span data-stu-id="39840-205">**Property name:** `cursorShape`</span></span>

<span data-ttu-id="39840-206">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-206">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-207">**Accetta:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span><span class="sxs-lookup"><span data-stu-id="39840-207">**Accepts:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span></span>

<span data-ttu-id="39840-208">**Valore predefinito:** `"bar"`</span><span class="sxs-lookup"><span data-stu-id="39840-208">**Default value:** `"bar"`</span></span>

### <a name="cursor-color"></a><span data-ttu-id="39840-209">Colore del cursore</span><span class="sxs-lookup"><span data-stu-id="39840-209">Cursor color</span></span>

<span data-ttu-id="39840-210">Consente di impostare il colore del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-210">This sets the cursor color of the profile.</span></span> <span data-ttu-id="39840-211">Sostituisce il valore di `cursorColor` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="39840-211">This will override the `cursorColor` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="39840-212">**Nome della proprietà:** `cursorColor`</span><span class="sxs-lookup"><span data-stu-id="39840-212">**Property name:** `cursorColor`</span></span>

<span data-ttu-id="39840-213">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-213">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-214">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="39840-214">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="cursor-height"></a><span data-ttu-id="39840-215">Altezza del cursore</span><span class="sxs-lookup"><span data-stu-id="39840-215">Cursor height</span></span>

<span data-ttu-id="39840-216">Consente di impostare l'altezza percentuale del cursore a partire dalla parte inferiore.</span><span class="sxs-lookup"><span data-stu-id="39840-216">This sets the percentage height of the cursor starting from the bottom.</span></span> <span data-ttu-id="39840-217">Funziona solo se `cursorShape` è impostata su `"vintage"`.</span><span class="sxs-lookup"><span data-stu-id="39840-217">This will only work when `cursorShape` is set to `"vintage"`.</span></span>

<span data-ttu-id="39840-218">**Nome della proprietà:** `cursorHeight`</span><span class="sxs-lookup"><span data-stu-id="39840-218">**Property name:** `cursorHeight`</span></span>

<span data-ttu-id="39840-219">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-219">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-220">**Accetta:** intero compreso tra 25-100</span><span class="sxs-lookup"><span data-stu-id="39840-220">**Accepts:** Integer from 25-100</span></span>

<br />

___

## <a name="color-settings"></a><span data-ttu-id="39840-221">Impostazioni per il colore</span><span class="sxs-lookup"><span data-stu-id="39840-221">Color settings</span></span>

### <a name="color-scheme"></a><span data-ttu-id="39840-222">Combinazione colori</span><span class="sxs-lookup"><span data-stu-id="39840-222">Color scheme</span></span>

<span data-ttu-id="39840-223">Nome della combinazione colori usata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-223">This is the name of the color scheme used in the profile.</span></span> <span data-ttu-id="39840-224">Le combinazioni colori sono definite nell'oggetto `schemes`.</span><span class="sxs-lookup"><span data-stu-id="39840-224">Color schemes are defined in the `schemes` object.</span></span> <span data-ttu-id="39840-225">Per informazioni più dettagliate, vedi la [pagina Combinazioni colori](./color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="39840-225">More detailed information can be found on the [Color schemes page](./color-schemes.md).</span></span>

<span data-ttu-id="39840-226">**Nome della proprietà:** `colorScheme`</span><span class="sxs-lookup"><span data-stu-id="39840-226">**Property name:** `colorScheme`</span></span>

<span data-ttu-id="39840-227">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-227">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-228">**Accetta:** nome della combinazione colori in formato stringa</span><span class="sxs-lookup"><span data-stu-id="39840-228">**Accepts:** Name of color scheme as a string</span></span>

<span data-ttu-id="39840-229">**Valore predefinito:** `"Campbell"`</span><span class="sxs-lookup"><span data-stu-id="39840-229">**Default value:** `"Campbell"`</span></span>

### <a name="foreground-color"></a><span data-ttu-id="39840-230">Colore primo piano</span><span class="sxs-lookup"><span data-stu-id="39840-230">Foreground color</span></span>

<span data-ttu-id="39840-231">Modifica il colore primo piano del profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-231">This changes the foreground color of the profile.</span></span> <span data-ttu-id="39840-232">Sostituisce il valore di `foreground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="39840-232">This overrides `foreground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="39840-233">**Nome della proprietà:** `foreground`</span><span class="sxs-lookup"><span data-stu-id="39840-233">**Property name:** `foreground`</span></span>

<span data-ttu-id="39840-234">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-234">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-235">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="39840-235">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="background-color"></a><span data-ttu-id="39840-236">Colore di sfondo</span><span class="sxs-lookup"><span data-stu-id="39840-236">Background color</span></span>

<span data-ttu-id="39840-237">Modifica il colore di sfondo del profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-237">This changes the background color of the profile with this setting.</span></span> <span data-ttu-id="39840-238">Sostituisce il valore di `background` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="39840-238">This overrides `background` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="39840-239">**Nome della proprietà:** `background`</span><span class="sxs-lookup"><span data-stu-id="39840-239">**Property name:** `background`</span></span>

<span data-ttu-id="39840-240">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-240">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-241">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="39840-241">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="selection-background-color"></a><span data-ttu-id="39840-242">Colore di sfondo della selezione</span><span class="sxs-lookup"><span data-stu-id="39840-242">Selection background color</span></span>

<span data-ttu-id="39840-243">Consente di impostare il colore di sfondo di una selezione nel profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-243">This sets the background color of a selection within the profile.</span></span> <span data-ttu-id="39840-244">Sostituisce il valore di `selectionBackground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="39840-244">This will override the `selectionBackground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="39840-245">**Nome della proprietà:** `selectionBackground`</span><span class="sxs-lookup"><span data-stu-id="39840-245">**Property name:** `selectionBackground`</span></span>

<span data-ttu-id="39840-246">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-246">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-247">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="39840-247">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

<br />

___

## <a name="acrylic-settings"></a><span data-ttu-id="39840-248">Impostazioni per acrilico</span><span class="sxs-lookup"><span data-stu-id="39840-248">Acrylic settings</span></span>

### <a name="enable-acrylic"></a><span data-ttu-id="39840-249">Abilita acrilico</span><span class="sxs-lookup"><span data-stu-id="39840-249">Enable acrylic</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="39840-250">Quando è impostata su `true`, la finestra avrà uno sfondo acrilico.</span><span class="sxs-lookup"><span data-stu-id="39840-250">When this is set to `true`, the window will have an acrylic background.</span></span> <span data-ttu-id="39840-251">Quando è impostato su `false`, la finestra avrà uno sfondo normale e senza trame.</span><span class="sxs-lookup"><span data-stu-id="39840-251">When it's set to `false`, the window will have a plain, untextured background.</span></span> <span data-ttu-id="39840-252">A causa delle limitazioni del sistema operativo, la trasparenza si applica solo alle finestre con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="39840-252">The transparency only applies to focused windows due to OS limitations.</span></span>

<span data-ttu-id="39840-253">**Nome della proprietà:** `useAcrylic`</span><span class="sxs-lookup"><span data-stu-id="39840-253">**Property name:** `useAcrylic`</span></span>

<span data-ttu-id="39840-254">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-254">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-255">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="39840-255">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="39840-256">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="39840-256">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Acrilico](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a><span data-ttu-id="39840-258">Opacità acrilico</span><span class="sxs-lookup"><span data-stu-id="39840-258">Acrylic opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="39840-259">Quando `useAcrylic` è impostata su `true`, imposta la trasparenza della finestra per il profilo.</span><span class="sxs-lookup"><span data-stu-id="39840-259">When `useAcrylic` is set to `true`, this sets the transparency of the window for the profile.</span></span> <span data-ttu-id="39840-260">Accetta valori a virgola mobile compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="39840-260">This accepts floating point values from 0-1.</span></span>

<span data-ttu-id="39840-261">**Nome della proprietà:** `acrylicOpacity`</span><span class="sxs-lookup"><span data-stu-id="39840-261">**Property name:** `acrylicOpacity`</span></span>

<span data-ttu-id="39840-262">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-262">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-263">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="39840-263">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="39840-264">**Valore predefinito:** `0.5`</span><span class="sxs-lookup"><span data-stu-id="39840-264">**Default value:** `0.5`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Opacità acrilico](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="background-image-settings"></a><span data-ttu-id="39840-266">Impostazioni per immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="39840-266">Background image settings</span></span>

### <a name="setting-the-background-image"></a><span data-ttu-id="39840-267">Impostazione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="39840-267">Setting the background image</span></span>

<span data-ttu-id="39840-268">Consente di impostare il percorso del file dell'immagine da tracciare sullo sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="39840-268">This sets the file location of the image to draw over the window background.</span></span> <span data-ttu-id="39840-269">L'immagine di sfondo può essere un file con estensione jpg, png o gif.</span><span class="sxs-lookup"><span data-stu-id="39840-269">The background image can be a .jpg, .png, or .gif file.</span></span>

<span data-ttu-id="39840-270">**Nome della proprietà:** `backgroundImage`</span><span class="sxs-lookup"><span data-stu-id="39840-270">**Property name:** `backgroundImage`</span></span>

<span data-ttu-id="39840-271">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-271">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-272">**Accetta:** percorso del file in formato stringa</span><span class="sxs-lookup"><span data-stu-id="39840-272">**Accepts:** File location as a string</span></span>

### <a name="background-image-stretch-mode"></a><span data-ttu-id="39840-273">Modalità di estensione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="39840-273">Background image stretch mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="39840-274">Consente di impostare la modalità di ridimensionamento dell'immagine di sfondo in modo che occupi tutto lo spazio della finestra.</span><span class="sxs-lookup"><span data-stu-id="39840-274">This sets how the background image is resized to fill the window.</span></span>

<span data-ttu-id="39840-275">**Nome della proprietà:** `backgroundImageStretchMode`</span><span class="sxs-lookup"><span data-stu-id="39840-275">**Property name:** `backgroundImageStretchMode`</span></span>

<span data-ttu-id="39840-276">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-276">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-277">**Accetta:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="39840-277">**Accepts:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span></span>

<span data-ttu-id="39840-278">**Valore predefinito:** `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="39840-278">**Default value:** `"uniformToFill"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="39840-279">![Terminale Windows - Modalità di estensione dell'immagine di sfondo](./../images/background-image-stretch-mode.gif)
 _[Origine dell'immagine di sfondo](https://wallpaperhub.app/wallpapers/6287)_</span><span class="sxs-lookup"><span data-stu-id="39840-279">![Windows Terminal background image stretch mode](./../images/background-image-stretch-mode.gif)
_[Background image source](https://wallpaperhub.app/wallpapers/6287)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a><span data-ttu-id="39840-280">Allineamento dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="39840-280">Background image alignment</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="39840-281">Consente di impostare la modalità di allineamento dell'immagine di sfondo ai bordi della finestra.</span><span class="sxs-lookup"><span data-stu-id="39840-281">This sets how the background image aligns to the boundaries of the window.</span></span>

<span data-ttu-id="39840-282">**Nome della proprietà:** `backgroundImageAlignment`</span><span class="sxs-lookup"><span data-stu-id="39840-282">**Property name:** `backgroundImageAlignment`</span></span>

<span data-ttu-id="39840-283">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-283">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-284">**Accetta:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span><span class="sxs-lookup"><span data-stu-id="39840-284">**Accepts:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span></span>

<span data-ttu-id="39840-285">**Valore predefinito:** `"center"`</span><span class="sxs-lookup"><span data-stu-id="39840-285">**Default value:** `"center"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="39840-286">![Terminale Windows - Allineamento dell'immagine di sfondo](./../images/background-image-alignment.gif)
 _[Origine dell'immagine di sfondo](https://design.ubuntu.com/brand/ubuntu-logo/)_</span><span class="sxs-lookup"><span data-stu-id="39840-286">![Windows Terminal background image alignment](./../images/background-image-alignment.gif)
_[Background image source](https://design.ubuntu.com/brand/ubuntu-logo/)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a><span data-ttu-id="39840-287">Opacità dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="39840-287">Background image opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="39840-288">Consente di impostare la trasparenza dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="39840-288">This sets the transparency of the background image.</span></span>

:::column-end:::
:::row-end:::

<span data-ttu-id="39840-289">**Nome della proprietà:** `backgroundImageOpacity`</span><span class="sxs-lookup"><span data-stu-id="39840-289">**Property name:** `backgroundImageOpacity`</span></span>

<span data-ttu-id="39840-290">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-290">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-291">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="39840-291">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="39840-292">**Valore predefinito:** `1.0`</span><span class="sxs-lookup"><span data-stu-id="39840-292">**Default value:** `1.0`</span></span>

<br />

___

## <a name="scroll-settings"></a><span data-ttu-id="39840-293">Impostazioni per lo scorrimento</span><span class="sxs-lookup"><span data-stu-id="39840-293">Scroll settings</span></span>

### <a name="scrollbar-visibility"></a><span data-ttu-id="39840-294">Visibilità della barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="39840-294">Scrollbar visibility</span></span>

<span data-ttu-id="39840-295">Consente di impostare la visibilità della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="39840-295">This sets the visibility of the scrollbar.</span></span>

<span data-ttu-id="39840-296">**Nome della proprietà:** `scrollbarState`</span><span class="sxs-lookup"><span data-stu-id="39840-296">**Property name:** `scrollbarState`</span></span>

<span data-ttu-id="39840-297">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-297">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-298">**Accetta:** `"visible"`, `"hidden"`</span><span class="sxs-lookup"><span data-stu-id="39840-298">**Accepts:** `"visible"`, `"hidden"`</span></span>

### <a name="scroll-to-input-line-when-typing"></a><span data-ttu-id="39840-299">Scorri fino alla riga di input durante la digitazione</span><span class="sxs-lookup"><span data-stu-id="39840-299">Scroll to input line when typing</span></span>

<span data-ttu-id="39840-300">Quando è impostata su `true`, la finestra scorre fino alla riga di input del comando durante la digitazione.</span><span class="sxs-lookup"><span data-stu-id="39840-300">When this is set to `true`, the window will scroll to the command input line when typing.</span></span> <span data-ttu-id="39840-301">Quando è impostata su `false`, lo scorrimento della finestra non è attivato quando inizi a digitare.</span><span class="sxs-lookup"><span data-stu-id="39840-301">When it's set to `false`, the window will not scroll when you start typing.</span></span>

<span data-ttu-id="39840-302">**Nome della proprietà:** `snapOnInput`</span><span class="sxs-lookup"><span data-stu-id="39840-302">**Property name:** `snapOnInput`</span></span>

<span data-ttu-id="39840-303">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-303">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-304">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="39840-304">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="39840-305">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="39840-305">**Default value:** `true`</span></span>

### <a name="history-size"></a><span data-ttu-id="39840-306">Dimensioni della cronologia</span><span class="sxs-lookup"><span data-stu-id="39840-306">History size</span></span>

<span data-ttu-id="39840-307">Consente di impostare il numero di righe a cui è possibile passare scorrendo che precedono quelle visualizzate nella finestra.</span><span class="sxs-lookup"><span data-stu-id="39840-307">This sets the number of lines above the ones displayed in the window you can scroll back to.</span></span>

<span data-ttu-id="39840-308">**Nome della proprietà:** `historySize`</span><span class="sxs-lookup"><span data-stu-id="39840-308">**Property name:** `historySize`</span></span>

<span data-ttu-id="39840-309">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-309">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-310">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="39840-310">**Accepts:** Integer</span></span>

<span data-ttu-id="39840-311">**Valore predefinito:** `9001`</span><span class="sxs-lookup"><span data-stu-id="39840-311">**Default value:** `9001`</span></span>

<br />

___

## <a name="how-the-profile-closes-when-exiting"></a><span data-ttu-id="39840-312">Modalità di chiusura del profilo all'uscita</span><span class="sxs-lookup"><span data-stu-id="39840-312">How the profile closes when exiting</span></span>

<span data-ttu-id="39840-313">Consente di impostare la reazione del profilo alla chiusura o a un errore all'avvio.</span><span class="sxs-lookup"><span data-stu-id="39840-313">This sets how the profile reacts to termination or failure to launch.</span></span> <span data-ttu-id="39840-314">Con `"graceful"`, il profilo verrà chiuso quando viene digitato `exit` o quando il processo viene chiuso normalmente.</span><span class="sxs-lookup"><span data-stu-id="39840-314">`"graceful"` will close the profile when `exit` is typed or when the process exits normally.</span></span> <span data-ttu-id="39840-315">Con `"always"` il profilo verrà sempre chiuso, mentre con `"never"` non verrà mai chiuso.</span><span class="sxs-lookup"><span data-stu-id="39840-315">`"always"` will always close the profile and `"never"` will never close the profile.</span></span> <span data-ttu-id="39840-316">`true` e `false` vengono accettati come sinonimi rispettivamente per `"graceful"` e `"never"`.</span><span class="sxs-lookup"><span data-stu-id="39840-316">`true` and `false` are accepted as synonyms for `"graceful"` and `"never"`, respectively.</span></span>

<span data-ttu-id="39840-317">**Nome della proprietà:** `closeOnExit`</span><span class="sxs-lookup"><span data-stu-id="39840-317">**Property name:** `closeOnExit`</span></span>

<span data-ttu-id="39840-318">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-318">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-319">**Accetta:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="39840-319">**Accepts:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span></span>

<span data-ttu-id="39840-320">**Valore predefinito:** `"graceful"`</span><span class="sxs-lookup"><span data-stu-id="39840-320">**Default value:** `"graceful"`</span></span>

<br />

___

## <a name="retro-terminal-effects"></a><span data-ttu-id="39840-321">Effetti per terminale retro</span><span class="sxs-lookup"><span data-stu-id="39840-321">Retro terminal effects</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="39840-322">Quando è impostata su `true`, il terminale emulerà un monitor CRT classico con linee di scansione e bordi di testo sfocati.</span><span class="sxs-lookup"><span data-stu-id="39840-322">When this is set to `true`, the terminal will emulate a classic CRT display with scan lines and blurry text edges.</span></span> <span data-ttu-id="39840-323">Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="39840-323">This is an experimental feature and its continued existence is not guaranteed.</span></span>

<span data-ttu-id="39840-324">**Nome della proprietà:** `experimental.retroTerminalEffect`</span><span class="sxs-lookup"><span data-stu-id="39840-324">**Property name:** `experimental.retroTerminalEffect`</span></span>

<span data-ttu-id="39840-325">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="39840-325">**Necessity:** Optional</span></span>

<span data-ttu-id="39840-326">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="39840-326">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="39840-327">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="39840-327">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="39840-328">![Terminale Windows - Effetto sperimentale per terminale retro](./../images/experimental-retro-terminal-effect.gif)
_Configurazione: [Prompt dei comandi retro](./../custom-terminal-gallery/retro-command-prompt.md)_</span><span class="sxs-lookup"><span data-stu-id="39840-328">![Windows Terminal experimental retro terminal effect](./../images/experimental-retro-terminal-effect.gif)
_Configuration: [Retro Command Prompt](./../custom-terminal-gallery/retro-command-prompt.md)_</span></span>

:::column-end:::
:::row-end:::
