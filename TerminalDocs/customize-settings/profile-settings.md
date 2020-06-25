---
title: Terminale Windows - Impostazioni del profilo
description: Informazioni su come personalizzare i singoli profili in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: ad7121f9cd6583562c03bf0e35d2928f46fe5d91
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994385"
---
# <a name="profile-settings-in-windows-terminal"></a><span data-ttu-id="46cfd-103">Impostazioni del profilo in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="46cfd-103">Profile settings in Windows Terminal</span></span>

<span data-ttu-id="46cfd-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="46cfd-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="46cfd-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="46cfd-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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

## <a name="unique-identifier"></a><span data-ttu-id="46cfd-106">Identificatore univoco</span><span class="sxs-lookup"><span data-stu-id="46cfd-106">Unique identifier</span></span>

<span data-ttu-id="46cfd-107">I profili possono usare un GUID come identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="46cfd-107">Profiles can use a GUID as a unique identifier.</span></span> <span data-ttu-id="46cfd-108">Per impostare un profilo come predefinito, è necessario un GUID per l'impostazione globale `defaultProfile`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-108">To make a profile your default profile, it needs a GUID for the `defaultProfile` global setting.</span></span>

<span data-ttu-id="46cfd-109">**Nome della proprietà:** `guid`</span><span class="sxs-lookup"><span data-stu-id="46cfd-109">**Property name:** `guid`</span></span>

<span data-ttu-id="46cfd-110">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="46cfd-110">**Necessity:** Required</span></span>

<span data-ttu-id="46cfd-111">**Accetta:** GUID in formato stringa del Registro di sistema: `"{00000000-0000-0000-0000-000000000000}"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-111">**Accepts:** GUID as a string in registry format: `"{00000000-0000-0000-0000-000000000000}"`</span></span>

<br />

___

## <a name="executable-settings"></a><span data-ttu-id="46cfd-112">Impostazioni per file eseguibili</span><span class="sxs-lookup"><span data-stu-id="46cfd-112">Executable settings</span></span>

### <a name="command-line"></a><span data-ttu-id="46cfd-113">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="46cfd-113">Command line</span></span>

<span data-ttu-id="46cfd-114">File eseguibile usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-114">This is the executable used in the profile.</span></span>

<span data-ttu-id="46cfd-115">**Nome della proprietà:** `commandline`</span><span class="sxs-lookup"><span data-stu-id="46cfd-115">**Property name:** `commandline`</span></span>

<span data-ttu-id="46cfd-116">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-116">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-117">**Accetta:** nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="46cfd-117">**Accepts:** Executable file name as a string</span></span>

<span data-ttu-id="46cfd-118">**Valore predefinito:** `"cmd.exe"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-118">**Default value:** `"cmd.exe"`</span></span>

### <a name="source"></a><span data-ttu-id="46cfd-119">Origine</span><span class="sxs-lookup"><span data-stu-id="46cfd-119">Source</span></span>

<span data-ttu-id="46cfd-120">Archivia il nome del generatore di profili che ha originato il profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-120">This stores the name of the profile generator that originated the profile.</span></span> <span data-ttu-id="46cfd-121">_Non esistono valori individuabili per questo campo._</span><span class="sxs-lookup"><span data-stu-id="46cfd-121">_There are no discoverable values for this field._</span></span> <span data-ttu-id="46cfd-122">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="46cfd-122">For additional information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="46cfd-123">**Nome della proprietà:** `source`</span><span class="sxs-lookup"><span data-stu-id="46cfd-123">**Property name:** `source`</span></span>

<span data-ttu-id="46cfd-124">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-124">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-125">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="46cfd-125">**Accepts:** String</span></span>

### <a name="starting-directory"></a><span data-ttu-id="46cfd-126">Directory iniziale</span><span class="sxs-lookup"><span data-stu-id="46cfd-126">Starting directory</span></span>

<span data-ttu-id="46cfd-127">Directory in cui viene avviata la shell quando viene caricata.</span><span class="sxs-lookup"><span data-stu-id="46cfd-127">This is the directory the shell starts in when it is loaded.</span></span>

<span data-ttu-id="46cfd-128">**Nome della proprietà:** `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="46cfd-128">**Property name:** `startingDirectory`</span></span>

<span data-ttu-id="46cfd-129">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-129">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-130">**Accetta:** percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="46cfd-130">**Accepts:** Folder location as a string</span></span>

<span data-ttu-id="46cfd-131">**Valore predefinito:** `"%USERPROFILE%"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-131">**Default value:** `"%USERPROFILE%"`</span></span>

<br />

> [!NOTE]
> <span data-ttu-id="46cfd-132">Quando si imposta la directory iniziale in cui si aprono le distribuzioni WSL installate, è consigliabile usare il formato "startingDirectory": "//wsl$/<distro name>", sostituendo il segnaposto con il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="46cfd-132">When setting the starting directory that your installed WSL distributions open to, you should use this format: "startingDirectory": "//wsl$/<distro name>", replacing with the name of your distribution.</span></span> <span data-ttu-id="46cfd-133">Ad esempio, "startingDirectory": "//wsl$/Ubuntu-20.04".</span><span class="sxs-lookup"><span data-stu-id="46cfd-133">For example, "startingDirectory": "//wsl$/Ubuntu-20.04".</span></span>

___

## <a name="dropdown-settings"></a><span data-ttu-id="46cfd-134">Impostazioni per il menu a discesa</span><span class="sxs-lookup"><span data-stu-id="46cfd-134">Dropdown settings</span></span>

<span data-ttu-id="46cfd-135">![Terminale Windows - Menu a discesa](./../images/dropdown.png)
_Configurazione: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="46cfd-135">![Windows Terminal dropdown](./../images/dropdown.png)
_Configuration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

### <a name="name"></a><span data-ttu-id="46cfd-136">Nome</span><span class="sxs-lookup"><span data-stu-id="46cfd-136">Name</span></span>

<span data-ttu-id="46cfd-137">Nome del profilo che verrà visualizzato nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="46cfd-137">This is the name of the profile that will be displayed in the dropdown menu.</span></span> <span data-ttu-id="46cfd-138">Questo valore viene usato anche come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="46cfd-138">This value is also used as the "title" to pass to the shell on startup.</span></span> <span data-ttu-id="46cfd-139">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46cfd-139">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="46cfd-140">Per eseguire l'override di questo comportamento del titolo, usa `tabTitle`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-140">This "title" behavior can be overridden by using `tabTitle`.</span></span>

<span data-ttu-id="46cfd-141">**Nome della proprietà:** `name`</span><span class="sxs-lookup"><span data-stu-id="46cfd-141">**Property name:** `name`</span></span>

<span data-ttu-id="46cfd-142">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="46cfd-142">**Necessity:** Required</span></span>

<span data-ttu-id="46cfd-143">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="46cfd-143">**Accepts:** String</span></span>

### <a name="icon"></a><span data-ttu-id="46cfd-144">Icona</span><span class="sxs-lookup"><span data-stu-id="46cfd-144">Icon</span></span>

<span data-ttu-id="46cfd-145">Consente di impostare l'icona visualizzata all'interno della scheda e nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="46cfd-145">This sets the icon that displays within the tab and the dropdown menu.</span></span>

<span data-ttu-id="46cfd-146">**Nome della proprietà:** `icon`</span><span class="sxs-lookup"><span data-stu-id="46cfd-146">**Property name:** `icon`</span></span>

<span data-ttu-id="46cfd-147">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-147">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-148">**Accetta:** percorso del file in formato stringa</span><span class="sxs-lookup"><span data-stu-id="46cfd-148">**Accepts:** File location as a string</span></span>

### <a name="hide-a-profile-from-the-dropdown"></a><span data-ttu-id="46cfd-149">Nascondi un profilo nell'elenco a discesa</span><span class="sxs-lookup"><span data-stu-id="46cfd-149">Hide a profile from the dropdown</span></span>

<span data-ttu-id="46cfd-150">Se `hidden` è impostato su `true`, il profilo non verrà visualizzato nell'elenco dei profili.</span><span class="sxs-lookup"><span data-stu-id="46cfd-150">If `hidden` is set to `true`, the profile will not appear in the list of profiles.</span></span> <span data-ttu-id="46cfd-151">Può essere usata per nascondere i profili predefiniti e quelli generati dinamicamente, lasciandoli nel file settings.</span><span class="sxs-lookup"><span data-stu-id="46cfd-151">This can be used to hide default profiles and dynamically generated profiles, while leaving them in your settings file.</span></span> <span data-ttu-id="46cfd-152">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="46cfd-152">To learn more about dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="46cfd-153">**Nome della proprietà:** `hidden`</span><span class="sxs-lookup"><span data-stu-id="46cfd-153">**Property name:** `hidden`</span></span>

<span data-ttu-id="46cfd-154">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-154">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-155">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-155">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="46cfd-156">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-156">**Default value:** `false`</span></span>

<br />

___

## <a name="tab-title-settings"></a><span data-ttu-id="46cfd-157">Impostazioni per i titoli delle schede</span><span class="sxs-lookup"><span data-stu-id="46cfd-157">Tab title settings</span></span>

### <a name="custom-tab-title"></a><span data-ttu-id="46cfd-158">Titolo scheda personalizzato</span><span class="sxs-lookup"><span data-stu-id="46cfd-158">Custom tab title</span></span>

<span data-ttu-id="46cfd-159">Se è impostata, sostituirà `name` come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="46cfd-159">If set, this will replace the `name` as the title to pass to the shell on startup.</span></span> <span data-ttu-id="46cfd-160">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="46cfd-160">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="46cfd-161">Per informazioni su come impostare la shell come titolo, vedi l'[esercitazione relativa al titolo della scheda](./../tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="46cfd-161">If you'd like to learn how to have the shell set your title, visit the [tab title tutorial](./../tutorials/tab-title.md).</span></span>

<span data-ttu-id="46cfd-162">**Nome della proprietà:** `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="46cfd-162">**Property name:** `tabTitle`</span></span>

<span data-ttu-id="46cfd-163">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-163">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-164">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="46cfd-164">**Accepts:** String</span></span>

### <a name="suppress-title-changes-from-the-shell"></a><span data-ttu-id="46cfd-165">Non visualizzare le modifiche apportate al titolo dalla shell</span><span class="sxs-lookup"><span data-stu-id="46cfd-165">Suppress title changes from the shell</span></span>

<span data-ttu-id="46cfd-166">Quando è impostata su `true`, `tabTitle` sostituisce il titolo predefinito della scheda. Tutti i messaggi di modifica del titolo dall'applicazione verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="46cfd-166">When this is set to `true`, `tabTitle` overrides the default title of the tab and any title change messages from the application will be suppressed.</span></span> <span data-ttu-id="46cfd-167">Se `tabTitle` non è impostata, verrà usata `name`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-167">If `tabTitle` isn't set, `name` will be used instead.</span></span> <span data-ttu-id="46cfd-168">Quando è impostata su `false`, `tabTitle` si comporta normalmente.</span><span class="sxs-lookup"><span data-stu-id="46cfd-168">When this is set to `false`, `tabTitle` behaves as normal.</span></span>

<span data-ttu-id="46cfd-169">**Nome della proprietà:** `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="46cfd-169">**Property name:** `suppressApplicationTitle`</span></span>

<span data-ttu-id="46cfd-170">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-170">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-171">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-171">**Accepts:** `true`, `false`</span></span>

<br />

___

## <a name="text-settings"></a><span data-ttu-id="46cfd-172">Impostazioni per il testo</span><span class="sxs-lookup"><span data-stu-id="46cfd-172">Text settings</span></span>

### <a name="font-face"></a><span data-ttu-id="46cfd-173">Tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="46cfd-173">Font face</span></span>

<span data-ttu-id="46cfd-174">Nome del tipo di carattere usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-174">This is the name of the font face used in the profile.</span></span> <span data-ttu-id="46cfd-175">Il terminale proverà ad eseguire il fallback a Consolas se non riesce a trovarlo o non è valido.</span><span class="sxs-lookup"><span data-stu-id="46cfd-175">The terminal will try to fallback to Consolas if this can't be found or is invalid.</span></span> <span data-ttu-id="46cfd-176">Per informazioni sulle altre varianti del tipo di carattere predefinito, Cascadia Mono, vedi la [tabella codici di Cascadia](./../cascadia-code.md).</span><span class="sxs-lookup"><span data-stu-id="46cfd-176">To learn about the other variants of the default font, Cascadia Mono, visit the [Cascadia Code page](./../cascadia-code.md).</span></span>

<span data-ttu-id="46cfd-177">**Nome della proprietà:** `fontFace`</span><span class="sxs-lookup"><span data-stu-id="46cfd-177">**Property name:** `fontFace`</span></span>

<span data-ttu-id="46cfd-178">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-178">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-179">**Accetta:** nome del tipo di carattere in formato stringa</span><span class="sxs-lookup"><span data-stu-id="46cfd-179">**Accepts:** Font name as a string</span></span>

<span data-ttu-id="46cfd-180">**Valore predefinito:** `"Cascadia Mono"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-180">**Default value:** `"Cascadia Mono"`</span></span>

### <a name="font-size"></a><span data-ttu-id="46cfd-181">Dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="46cfd-181">Font size</span></span>

<span data-ttu-id="46cfd-182">Consente di impostare le dimensioni del carattere del profilo in punti.</span><span class="sxs-lookup"><span data-stu-id="46cfd-182">This sets the profile's font size in points.</span></span>

<span data-ttu-id="46cfd-183">**Nome della proprietà:** `fontSize`</span><span class="sxs-lookup"><span data-stu-id="46cfd-183">**Property name:** `fontSize`</span></span>

<span data-ttu-id="46cfd-184">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-184">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-185">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="46cfd-185">**Accepts:** Integer</span></span>

<span data-ttu-id="46cfd-186">**Valore predefinito:** `12`</span><span class="sxs-lookup"><span data-stu-id="46cfd-186">**Default value:** `12`</span></span>

### <a name="font-weight-preview"></a><span data-ttu-id="46cfd-187">Spessore dei caratteri ([anteprima](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="46cfd-187">Font weight ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="46cfd-188">Questa proprietà imposta lo spessore (tratti sottili o spessi) per il tipo di carattere del profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-188">This sets the weight (lightness or heaviness of the strokes) for the profile's font.</span></span>

<span data-ttu-id="46cfd-189">**Nome della proprietà:** `fontWeight`</span><span class="sxs-lookup"><span data-stu-id="46cfd-189">**Property name:** `fontWeight`</span></span>

<span data-ttu-id="46cfd-190">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-190">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-191">**Accetta**  `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"` oppure un intero che corrisponde alla rappresentazione numerica dello spesso del tipo di carattere OpenType</span><span class="sxs-lookup"><span data-stu-id="46cfd-191">**Accepts:** `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"`, or an integer corresponding to the numeric representation of the OpenType font weight</span></span>

<span data-ttu-id="46cfd-192">**Valore predefinito:** `"normal"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-192">**Default value:** `"normal"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46cfd-193">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="46cfd-193">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="padding"></a><span data-ttu-id="46cfd-194">Spaziatura interna</span><span class="sxs-lookup"><span data-stu-id="46cfd-194">Padding</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="46cfd-195">Consente di impostare la spaziatura intorno al testo all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="46cfd-195">This sets the padding around the text within the window.</span></span> <span data-ttu-id="46cfd-196">Vengono accettati tre diversi formati: `"#"` imposta la stessa spaziatura interna su tutti i lati, `"#, #"` imposta la stessa spaziatura interna per left-right e top-bottom, mentre `"#, #, #, #"` imposta la spaziatura interna singolarmente per left, top, right e bottom.</span><span class="sxs-lookup"><span data-stu-id="46cfd-196">This will accept three different formats: `"#"` sets the same padding for all sides, `"#, #"` sets the same padding for left-right and top-bottom, and `"#, #, #, #"` sets the padding individually for left, top, right, and bottom.</span></span>

<span data-ttu-id="46cfd-197">**Nome della proprietà:** `padding`</span><span class="sxs-lookup"><span data-stu-id="46cfd-197">**Property name:** `padding`</span></span>

<span data-ttu-id="46cfd-198">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-198">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-199">**Accetta:** valori nei formati stringa seguenti: `"#"`, `"#, #"`, `"#, #, #, #"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-199">**Accepts:** Values as a string in the following formats: `"#"`, `"#, #"`, `"#, #, #, #"`</span></span>

<span data-ttu-id="46cfd-200">**Valore predefinito:** `"8, 8, 8, 8"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-200">**Default value:** `"8, 8, 8, 8"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Spaziatura interna](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="antialiasing-text"></a><span data-ttu-id="46cfd-202">Anti-aliasing del testo</span><span class="sxs-lookup"><span data-stu-id="46cfd-202">Antialiasing text</span></span>

<span data-ttu-id="46cfd-203">Controlla la modalità di anti-aliasing del testo nel renderer.</span><span class="sxs-lookup"><span data-stu-id="46cfd-203">This controls how text is antialiased in the renderer.</span></span> <span data-ttu-id="46cfd-204">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="46cfd-204">Note that changing this setting will require starting a new terminal instance.</span></span>

![Terminale Windows - Anti-aliasing del testo](./../images/antialiasing-mode.gif)

<span data-ttu-id="46cfd-206">**Nome della proprietà:** `antialiasingMode`</span><span class="sxs-lookup"><span data-stu-id="46cfd-206">**Property name:** `antialiasingMode`</span></span>

<span data-ttu-id="46cfd-207">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-207">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-208">**Accetta:** `"grayscale"`, `"cleartype"`, `"aliased"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-208">**Accepts:** `"grayscale"`, `"cleartype"`, `"aliased"`</span></span>

<span data-ttu-id="46cfd-209">**Valore predefinito:** `"grayscale"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-209">**Default value:** `"grayscale"`</span></span>

<br />

___

## <a name="cursor-settings"></a><span data-ttu-id="46cfd-210">Impostazioni per il cursore</span><span class="sxs-lookup"><span data-stu-id="46cfd-210">Cursor settings</span></span>

### <a name="cursor-shape"></a><span data-ttu-id="46cfd-211">Forma del cursore</span><span class="sxs-lookup"><span data-stu-id="46cfd-211">Cursor shape</span></span>

<span data-ttu-id="46cfd-212">Consente di impostare la forma del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-212">This sets the cursor shape for the profile.</span></span> <span data-ttu-id="46cfd-213">I cursori possibili sono i seguenti: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;)</span><span class="sxs-lookup"><span data-stu-id="46cfd-213">The possible cursors are as follows: `"bar"` ( &#x2503; ), `"vintage"` ( &#x2583; ), `"underscore"` ( &#x2581; ), `"filledBox"` ( &#x2588; ), `"emptyBox"` ( &#x25AF; )</span></span>

<span data-ttu-id="46cfd-214">**Nome della proprietà:** `cursorShape`</span><span class="sxs-lookup"><span data-stu-id="46cfd-214">**Property name:** `cursorShape`</span></span>

<span data-ttu-id="46cfd-215">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-215">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-216">**Accetta:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-216">**Accepts:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span></span>

<span data-ttu-id="46cfd-217">**Valore predefinito:** `"bar"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-217">**Default value:** `"bar"`</span></span>

### <a name="cursor-color"></a><span data-ttu-id="46cfd-218">Colore del cursore</span><span class="sxs-lookup"><span data-stu-id="46cfd-218">Cursor color</span></span>

<span data-ttu-id="46cfd-219">Consente di impostare il colore del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-219">This sets the cursor color of the profile.</span></span> <span data-ttu-id="46cfd-220">Sostituisce il valore di `cursorColor` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-220">This will override the `cursorColor` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="46cfd-221">**Nome della proprietà:** `cursorColor`</span><span class="sxs-lookup"><span data-stu-id="46cfd-221">**Property name:** `cursorColor`</span></span>

<span data-ttu-id="46cfd-222">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-222">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-223">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-223">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="cursor-height"></a><span data-ttu-id="46cfd-224">Altezza del cursore</span><span class="sxs-lookup"><span data-stu-id="46cfd-224">Cursor height</span></span>

<span data-ttu-id="46cfd-225">Consente di impostare l'altezza percentuale del cursore a partire dalla parte inferiore.</span><span class="sxs-lookup"><span data-stu-id="46cfd-225">This sets the percentage height of the cursor starting from the bottom.</span></span> <span data-ttu-id="46cfd-226">Funziona solo se `cursorShape` è impostata su `"vintage"`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-226">This will only work when `cursorShape` is set to `"vintage"`.</span></span>

<span data-ttu-id="46cfd-227">**Nome della proprietà:** `cursorHeight`</span><span class="sxs-lookup"><span data-stu-id="46cfd-227">**Property name:** `cursorHeight`</span></span>

<span data-ttu-id="46cfd-228">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-228">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-229">**Accetta:** intero compreso tra 25-100</span><span class="sxs-lookup"><span data-stu-id="46cfd-229">**Accepts:** Integer from 25-100</span></span>

<br />

___

## <a name="keyboard-settings"></a><span data-ttu-id="46cfd-230">Impostazioni da tastiera</span><span class="sxs-lookup"><span data-stu-id="46cfd-230">Keyboard settings</span></span>

### <a name="altgr-aliasing-preview"></a><span data-ttu-id="46cfd-231">Aliasing di ALTGR ([anteprima](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="46cfd-231">AltGr aliasing ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="46cfd-232">Questa proprietà consente di controllare se Terminale Windows considererà <kbd>CTRL+ALT</kbd> come alias di <kbd>ALTGR</kbd>.</span><span class="sxs-lookup"><span data-stu-id="46cfd-232">This allows you to control if Windows Terminal will treat <kbd>ctrl+alt</kbd> as an alias for <kbd>AltGr</kbd>.</span></span>

<span data-ttu-id="46cfd-233">**Nome della proprietà:** `altGrAliasing`</span><span class="sxs-lookup"><span data-stu-id="46cfd-233">**Property name:** `altGrAliasing`</span></span>

<span data-ttu-id="46cfd-234">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-234">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-235">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-235">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="46cfd-236">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="46cfd-236">**Default value:** `true`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46cfd-237">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="46cfd-237">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

<br />

___

## <a name="color-settings"></a><span data-ttu-id="46cfd-238">Impostazioni per il colore</span><span class="sxs-lookup"><span data-stu-id="46cfd-238">Color settings</span></span>

### <a name="color-scheme"></a><span data-ttu-id="46cfd-239">Combinazione colori</span><span class="sxs-lookup"><span data-stu-id="46cfd-239">Color scheme</span></span>

<span data-ttu-id="46cfd-240">Nome della combinazione colori usata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-240">This is the name of the color scheme used in the profile.</span></span> <span data-ttu-id="46cfd-241">Le combinazioni colori sono definite nell'oggetto `schemes`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-241">Color schemes are defined in the `schemes` object.</span></span> <span data-ttu-id="46cfd-242">Per informazioni più dettagliate, vedi la [pagina Combinazioni colori](./color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="46cfd-242">More detailed information can be found on the [Color schemes page](./color-schemes.md).</span></span>

<span data-ttu-id="46cfd-243">**Nome della proprietà:** `colorScheme`</span><span class="sxs-lookup"><span data-stu-id="46cfd-243">**Property name:** `colorScheme`</span></span>

<span data-ttu-id="46cfd-244">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-244">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-245">**Accetta:** nome della combinazione colori in formato stringa</span><span class="sxs-lookup"><span data-stu-id="46cfd-245">**Accepts:** Name of color scheme as a string</span></span>

<span data-ttu-id="46cfd-246">**Valore predefinito:** `"Campbell"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-246">**Default value:** `"Campbell"`</span></span>

### <a name="foreground-color"></a><span data-ttu-id="46cfd-247">Colore primo piano</span><span class="sxs-lookup"><span data-stu-id="46cfd-247">Foreground color</span></span>

<span data-ttu-id="46cfd-248">Modifica il colore primo piano del profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-248">This changes the foreground color of the profile.</span></span> <span data-ttu-id="46cfd-249">Sostituisce il valore di `foreground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-249">This overrides `foreground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="46cfd-250">**Nome della proprietà:** `foreground`</span><span class="sxs-lookup"><span data-stu-id="46cfd-250">**Property name:** `foreground`</span></span>

<span data-ttu-id="46cfd-251">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-251">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-252">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-252">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="background-color"></a><span data-ttu-id="46cfd-253">Colore di sfondo</span><span class="sxs-lookup"><span data-stu-id="46cfd-253">Background color</span></span>

<span data-ttu-id="46cfd-254">Modifica il colore di sfondo del profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-254">This changes the background color of the profile with this setting.</span></span> <span data-ttu-id="46cfd-255">Sostituisce il valore di `background` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-255">This overrides `background` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="46cfd-256">**Nome della proprietà:** `background`</span><span class="sxs-lookup"><span data-stu-id="46cfd-256">**Property name:** `background`</span></span>

<span data-ttu-id="46cfd-257">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-257">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-258">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-258">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="selection-background-color"></a><span data-ttu-id="46cfd-259">Colore di sfondo della selezione</span><span class="sxs-lookup"><span data-stu-id="46cfd-259">Selection background color</span></span>

<span data-ttu-id="46cfd-260">Consente di impostare il colore di sfondo di una selezione nel profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-260">This sets the background color of a selection within the profile.</span></span> <span data-ttu-id="46cfd-261">Sostituisce il valore di `selectionBackground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-261">This will override the `selectionBackground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="46cfd-262">**Nome della proprietà:** `selectionBackground`</span><span class="sxs-lookup"><span data-stu-id="46cfd-262">**Property name:** `selectionBackground`</span></span>

<span data-ttu-id="46cfd-263">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-263">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-264">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-264">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

<br />

___

## <a name="acrylic-settings"></a><span data-ttu-id="46cfd-265">Impostazioni per acrilico</span><span class="sxs-lookup"><span data-stu-id="46cfd-265">Acrylic settings</span></span>

### <a name="enable-acrylic"></a><span data-ttu-id="46cfd-266">Abilita acrilico</span><span class="sxs-lookup"><span data-stu-id="46cfd-266">Enable acrylic</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="46cfd-267">Quando è impostata su `true`, la finestra avrà uno sfondo acrilico.</span><span class="sxs-lookup"><span data-stu-id="46cfd-267">When this is set to `true`, the window will have an acrylic background.</span></span> <span data-ttu-id="46cfd-268">Quando è impostato su `false`, la finestra avrà uno sfondo normale e senza trame.</span><span class="sxs-lookup"><span data-stu-id="46cfd-268">When it's set to `false`, the window will have a plain, untextured background.</span></span> <span data-ttu-id="46cfd-269">A causa delle limitazioni del sistema operativo, la trasparenza si applica solo alle finestre con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-269">The transparency only applies to focused windows due to OS limitations.</span></span>

<span data-ttu-id="46cfd-270">**Nome della proprietà:** `useAcrylic`</span><span class="sxs-lookup"><span data-stu-id="46cfd-270">**Property name:** `useAcrylic`</span></span>

<span data-ttu-id="46cfd-271">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-271">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-272">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-272">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="46cfd-273">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-273">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Acrilico](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a><span data-ttu-id="46cfd-275">Opacità acrilico</span><span class="sxs-lookup"><span data-stu-id="46cfd-275">Acrylic opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="46cfd-276">Quando `useAcrylic` è impostata su `true`, imposta la trasparenza della finestra per il profilo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-276">When `useAcrylic` is set to `true`, this sets the transparency of the window for the profile.</span></span> <span data-ttu-id="46cfd-277">Accetta valori a virgola mobile compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="46cfd-277">This accepts floating point values from 0-1.</span></span>

<span data-ttu-id="46cfd-278">**Nome della proprietà:** `acrylicOpacity`</span><span class="sxs-lookup"><span data-stu-id="46cfd-278">**Property name:** `acrylicOpacity`</span></span>

<span data-ttu-id="46cfd-279">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-279">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-280">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="46cfd-280">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="46cfd-281">**Valore predefinito:** `0.5`</span><span class="sxs-lookup"><span data-stu-id="46cfd-281">**Default value:** `0.5`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Opacità acrilico](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="background-image-settings"></a><span data-ttu-id="46cfd-283">Impostazioni per immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="46cfd-283">Background image settings</span></span>

### <a name="setting-the-background-image"></a><span data-ttu-id="46cfd-284">Impostazione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="46cfd-284">Setting the background image</span></span>

<span data-ttu-id="46cfd-285">Consente di impostare il percorso del file dell'immagine da tracciare sullo sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="46cfd-285">This sets the file location of the image to draw over the window background.</span></span> <span data-ttu-id="46cfd-286">L'immagine di sfondo può essere un file con estensione jpg, png o gif.</span><span class="sxs-lookup"><span data-stu-id="46cfd-286">The background image can be a .jpg, .png, or .gif file.</span></span>

<span data-ttu-id="46cfd-287">**Nome della proprietà:** `backgroundImage`</span><span class="sxs-lookup"><span data-stu-id="46cfd-287">**Property name:** `backgroundImage`</span></span>

<span data-ttu-id="46cfd-288">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-288">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-289">**Accetta:** percorso del file in formato stringa</span><span class="sxs-lookup"><span data-stu-id="46cfd-289">**Accepts:** File location as a string</span></span>

### <a name="background-image-stretch-mode"></a><span data-ttu-id="46cfd-290">Modalità di estensione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="46cfd-290">Background image stretch mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="46cfd-291">Consente di impostare la modalità di ridimensionamento dell'immagine di sfondo in modo che occupi tutto lo spazio della finestra.</span><span class="sxs-lookup"><span data-stu-id="46cfd-291">This sets how the background image is resized to fill the window.</span></span>

<span data-ttu-id="46cfd-292">**Nome della proprietà:** `backgroundImageStretchMode`</span><span class="sxs-lookup"><span data-stu-id="46cfd-292">**Property name:** `backgroundImageStretchMode`</span></span>

<span data-ttu-id="46cfd-293">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-293">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-294">**Accetta:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-294">**Accepts:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span></span>

<span data-ttu-id="46cfd-295">**Valore predefinito:** `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-295">**Default value:** `"uniformToFill"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="46cfd-296">![Terminale Windows - Modalità di estensione dell'immagine di sfondo](./../images/background-image-stretch-mode.gif)
 _[Origine dell'immagine di sfondo](https://wallpaperhub.app/wallpapers/6287)_</span><span class="sxs-lookup"><span data-stu-id="46cfd-296">![Windows Terminal background image stretch mode](./../images/background-image-stretch-mode.gif)
_[Background image source](https://wallpaperhub.app/wallpapers/6287)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a><span data-ttu-id="46cfd-297">Allineamento dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="46cfd-297">Background image alignment</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="46cfd-298">Consente di impostare la modalità di allineamento dell'immagine di sfondo ai bordi della finestra.</span><span class="sxs-lookup"><span data-stu-id="46cfd-298">This sets how the background image aligns to the boundaries of the window.</span></span>

<span data-ttu-id="46cfd-299">**Nome della proprietà:** `backgroundImageAlignment`</span><span class="sxs-lookup"><span data-stu-id="46cfd-299">**Property name:** `backgroundImageAlignment`</span></span>

<span data-ttu-id="46cfd-300">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-300">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-301">**Accetta:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-301">**Accepts:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span></span>

<span data-ttu-id="46cfd-302">**Valore predefinito:** `"center"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-302">**Default value:** `"center"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="46cfd-303">![Terminale Windows - Allineamento dell'immagine di sfondo](./../images/background-image-alignment.gif)
 _[Origine dell'immagine di sfondo](https://design.ubuntu.com/brand/ubuntu-logo/)_</span><span class="sxs-lookup"><span data-stu-id="46cfd-303">![Windows Terminal background image alignment](./../images/background-image-alignment.gif)
_[Background image source](https://design.ubuntu.com/brand/ubuntu-logo/)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a><span data-ttu-id="46cfd-304">Opacità dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="46cfd-304">Background image opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="46cfd-305">Consente di impostare la trasparenza dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="46cfd-305">This sets the transparency of the background image.</span></span>

:::column-end:::
:::row-end:::

<span data-ttu-id="46cfd-306">**Nome della proprietà:** `backgroundImageOpacity`</span><span class="sxs-lookup"><span data-stu-id="46cfd-306">**Property name:** `backgroundImageOpacity`</span></span>

<span data-ttu-id="46cfd-307">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-307">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-308">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="46cfd-308">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="46cfd-309">**Valore predefinito:** `1.0`</span><span class="sxs-lookup"><span data-stu-id="46cfd-309">**Default value:** `1.0`</span></span>

<br />

___

## <a name="scroll-settings"></a><span data-ttu-id="46cfd-310">Impostazioni per lo scorrimento</span><span class="sxs-lookup"><span data-stu-id="46cfd-310">Scroll settings</span></span>

### <a name="scrollbar-visibility"></a><span data-ttu-id="46cfd-311">Visibilità della barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="46cfd-311">Scrollbar visibility</span></span>

<span data-ttu-id="46cfd-312">Consente di impostare la visibilità della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="46cfd-312">This sets the visibility of the scrollbar.</span></span>

<span data-ttu-id="46cfd-313">**Nome della proprietà:** `scrollbarState`</span><span class="sxs-lookup"><span data-stu-id="46cfd-313">**Property name:** `scrollbarState`</span></span>

<span data-ttu-id="46cfd-314">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-314">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-315">**Accetta:** `"visible"`, `"hidden"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-315">**Accepts:** `"visible"`, `"hidden"`</span></span>

### <a name="scroll-to-input-line-when-typing"></a><span data-ttu-id="46cfd-316">Scorri fino alla riga di input durante la digitazione</span><span class="sxs-lookup"><span data-stu-id="46cfd-316">Scroll to input line when typing</span></span>

<span data-ttu-id="46cfd-317">Quando è impostata su `true`, la finestra scorre fino alla riga di input del comando durante la digitazione.</span><span class="sxs-lookup"><span data-stu-id="46cfd-317">When this is set to `true`, the window will scroll to the command input line when typing.</span></span> <span data-ttu-id="46cfd-318">Quando è impostata su `false`, lo scorrimento della finestra non è attivato quando inizi a digitare.</span><span class="sxs-lookup"><span data-stu-id="46cfd-318">When it's set to `false`, the window will not scroll when you start typing.</span></span>

<span data-ttu-id="46cfd-319">**Nome della proprietà:** `snapOnInput`</span><span class="sxs-lookup"><span data-stu-id="46cfd-319">**Property name:** `snapOnInput`</span></span>

<span data-ttu-id="46cfd-320">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-320">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-321">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-321">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="46cfd-322">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="46cfd-322">**Default value:** `true`</span></span>

### <a name="history-size"></a><span data-ttu-id="46cfd-323">Dimensioni della cronologia</span><span class="sxs-lookup"><span data-stu-id="46cfd-323">History size</span></span>

<span data-ttu-id="46cfd-324">Consente di impostare il numero di righe a cui è possibile passare scorrendo che precedono quelle visualizzate nella finestra.</span><span class="sxs-lookup"><span data-stu-id="46cfd-324">This sets the number of lines above the ones displayed in the window you can scroll back to.</span></span>

<span data-ttu-id="46cfd-325">**Nome della proprietà:** `historySize`</span><span class="sxs-lookup"><span data-stu-id="46cfd-325">**Property name:** `historySize`</span></span>

<span data-ttu-id="46cfd-326">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-326">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-327">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="46cfd-327">**Accepts:** Integer</span></span>

<span data-ttu-id="46cfd-328">**Valore predefinito:** `9001`</span><span class="sxs-lookup"><span data-stu-id="46cfd-328">**Default value:** `9001`</span></span>

<br />

___

## <a name="how-the-profile-closes-when-exiting"></a><span data-ttu-id="46cfd-329">Modalità di chiusura del profilo all'uscita</span><span class="sxs-lookup"><span data-stu-id="46cfd-329">How the profile closes when exiting</span></span>

<span data-ttu-id="46cfd-330">Consente di impostare la reazione del profilo alla chiusura o a un errore all'avvio.</span><span class="sxs-lookup"><span data-stu-id="46cfd-330">This sets how the profile reacts to termination or failure to launch.</span></span> <span data-ttu-id="46cfd-331">Con `"graceful"`, il profilo verrà chiuso quando viene digitato `exit` o quando il processo viene chiuso normalmente.</span><span class="sxs-lookup"><span data-stu-id="46cfd-331">`"graceful"` will close the profile when `exit` is typed or when the process exits normally.</span></span> <span data-ttu-id="46cfd-332">Con `"always"` il profilo verrà sempre chiuso, mentre con `"never"` non verrà mai chiuso.</span><span class="sxs-lookup"><span data-stu-id="46cfd-332">`"always"` will always close the profile and `"never"` will never close the profile.</span></span> <span data-ttu-id="46cfd-333">`true` e `false` vengono accettati come sinonimi rispettivamente per `"graceful"` e `"never"`.</span><span class="sxs-lookup"><span data-stu-id="46cfd-333">`true` and `false` are accepted as synonyms for `"graceful"` and `"never"`, respectively.</span></span>

<span data-ttu-id="46cfd-334">**Nome della proprietà:** `closeOnExit`</span><span class="sxs-lookup"><span data-stu-id="46cfd-334">**Property name:** `closeOnExit`</span></span>

<span data-ttu-id="46cfd-335">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-335">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-336">**Accetta:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-336">**Accepts:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span></span>

<span data-ttu-id="46cfd-337">**Valore predefinito:** `"graceful"`</span><span class="sxs-lookup"><span data-stu-id="46cfd-337">**Default value:** `"graceful"`</span></span>

<br />

___

## <a name="retro-terminal-effects"></a><span data-ttu-id="46cfd-338">Effetti per terminale retro</span><span class="sxs-lookup"><span data-stu-id="46cfd-338">Retro terminal effects</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="46cfd-339">Quando è impostata su `true`, il terminale emulerà un monitor CRT classico con linee di scansione e bordi di testo sfocati.</span><span class="sxs-lookup"><span data-stu-id="46cfd-339">When this is set to `true`, the terminal will emulate a classic CRT display with scan lines and blurry text edges.</span></span> <span data-ttu-id="46cfd-340">Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="46cfd-340">This is an experimental feature and its continued existence is not guaranteed.</span></span>

<span data-ttu-id="46cfd-341">**Nome della proprietà:** `experimental.retroTerminalEffect`</span><span class="sxs-lookup"><span data-stu-id="46cfd-341">**Property name:** `experimental.retroTerminalEffect`</span></span>

<span data-ttu-id="46cfd-342">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="46cfd-342">**Necessity:** Optional</span></span>

<span data-ttu-id="46cfd-343">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-343">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="46cfd-344">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="46cfd-344">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="46cfd-345">![Terminale Windows - Effetto sperimentale per terminale retro](./../images/experimental-retro-terminal-effect.gif)
_Configurazione: [Prompt dei comandi retro](./../custom-terminal-gallery/retro-command-prompt.md)_</span><span class="sxs-lookup"><span data-stu-id="46cfd-345">![Windows Terminal experimental retro terminal effect](./../images/experimental-retro-terminal-effect.gif)
_Configuration: [Retro Command Prompt](./../custom-terminal-gallery/retro-command-prompt.md)_</span></span>

:::column-end:::
:::row-end:::
