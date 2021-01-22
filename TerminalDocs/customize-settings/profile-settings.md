---
title: Terminale Windows - Impostazioni del profilo
description: Informazioni su come personalizzare i singoli profili in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 11/11/2020
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 8715cc5af89784d1d58d408bdeb969e187f1a295
ms.sourcegitcommit: 9a2f9d152f65cdc8106fb9aad7fa69b01f3d05db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "94520280"
---
# <a name="profile-settings-in-windows-terminal"></a><span data-ttu-id="6550b-103">Impostazioni del profilo in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="6550b-103">Profile settings in Windows Terminal</span></span>

<span data-ttu-id="6550b-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="6550b-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="6550b-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="6550b-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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

## <a name="unique-identifier"></a><span data-ttu-id="6550b-106">Identificatore univoco</span><span class="sxs-lookup"><span data-stu-id="6550b-106">Unique identifier</span></span>

<span data-ttu-id="6550b-107">I profili possono usare un GUID come identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="6550b-107">Profiles can use a GUID as a unique identifier.</span></span> <span data-ttu-id="6550b-108">Per impostare un profilo come predefinito, è necessario un GUID per l'impostazione globale `defaultProfile`.</span><span class="sxs-lookup"><span data-stu-id="6550b-108">To make a profile your default profile, it needs a GUID for the `defaultProfile` global setting.</span></span>

<span data-ttu-id="6550b-109">**Nome della proprietà:** `guid`</span><span class="sxs-lookup"><span data-stu-id="6550b-109">**Property name:** `guid`</span></span>

<span data-ttu-id="6550b-110">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="6550b-110">**Necessity:** Required</span></span>

<span data-ttu-id="6550b-111">**Accetta:** GUID in formato stringa del Registro di sistema: `"{00000000-0000-0000-0000-000000000000}"`</span><span class="sxs-lookup"><span data-stu-id="6550b-111">**Accepts:** GUID as a string in registry format: `"{00000000-0000-0000-0000-000000000000}"`</span></span>

<br />

___

## <a name="executable-settings"></a><span data-ttu-id="6550b-112">Impostazioni per file eseguibili</span><span class="sxs-lookup"><span data-stu-id="6550b-112">Executable settings</span></span>

### <a name="command-line"></a><span data-ttu-id="6550b-113">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="6550b-113">Command line</span></span>

<span data-ttu-id="6550b-114">File eseguibile usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-114">This is the executable used in the profile.</span></span>

<span data-ttu-id="6550b-115">**Nome della proprietà:** `commandline`</span><span class="sxs-lookup"><span data-stu-id="6550b-115">**Property name:** `commandline`</span></span>

<span data-ttu-id="6550b-116">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-116">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-117">**Accetta:** nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="6550b-117">**Accepts:** Executable file name as a string</span></span>

<span data-ttu-id="6550b-118">**Valore predefinito:** `"cmd.exe"`</span><span class="sxs-lookup"><span data-stu-id="6550b-118">**Default value:** `"cmd.exe"`</span></span>

### <a name="source"></a><span data-ttu-id="6550b-119">Origine</span><span class="sxs-lookup"><span data-stu-id="6550b-119">Source</span></span>

<span data-ttu-id="6550b-120">Archivia il nome del generatore di profili che ha originato il profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-120">This stores the name of the profile generator that originated the profile.</span></span> <span data-ttu-id="6550b-121">_Non esistono valori individuabili per questo campo._</span><span class="sxs-lookup"><span data-stu-id="6550b-121">_There are no discoverable values for this field._</span></span> <span data-ttu-id="6550b-122">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6550b-122">For additional information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="6550b-123">**Nome della proprietà:** `source`</span><span class="sxs-lookup"><span data-stu-id="6550b-123">**Property name:** `source`</span></span>

<span data-ttu-id="6550b-124">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-124">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-125">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="6550b-125">**Accepts:** String</span></span>

### <a name="starting-directory"></a><span data-ttu-id="6550b-126">Directory iniziale</span><span class="sxs-lookup"><span data-stu-id="6550b-126">Starting directory</span></span>

<span data-ttu-id="6550b-127">Directory in cui viene avviata la shell quando viene caricata.</span><span class="sxs-lookup"><span data-stu-id="6550b-127">This is the directory the shell starts in when it is loaded.</span></span>

<span data-ttu-id="6550b-128">**Nome della proprietà:** `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="6550b-128">**Property name:** `startingDirectory`</span></span>

<span data-ttu-id="6550b-129">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-129">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-130">**Accetta:** percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="6550b-130">**Accepts:** Folder location as a string</span></span>

<span data-ttu-id="6550b-131">**Valore predefinito:** `"%USERPROFILE%"`</span><span class="sxs-lookup"><span data-stu-id="6550b-131">**Default value:** `"%USERPROFILE%"`</span></span>

<br />

> [!NOTE]
> <span data-ttu-id="6550b-132">Quando si imposta la directory iniziale a cui si aprono le distribuzioni WSL installate, è necessario usare il formato seguente: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"` , sostituendo con il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6550b-132">When setting the starting directory that your installed WSL distributions open to, you should use this format: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"`, replacing with the name of your distribution.</span></span> <span data-ttu-id="6550b-133">Ad esempio: `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.</span><span class="sxs-lookup"><span data-stu-id="6550b-133">For example, `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.</span></span>

> [!NOTE]
> <span data-ttu-id="6550b-134">L'omissione del valore startingDirectory in un profilo comporta...</span><span class="sxs-lookup"><span data-stu-id="6550b-134">Omitting the startingDirectory value in a profile results in...</span></span>
</br>
<span data-ttu-id="6550b-135">.. Se si esegue il terminale di Windows dal menu Start: C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="6550b-135">..if you run Windows Terminal from the Start menu: C:\windows\system32</span></span>
</br>
<span data-ttu-id="6550b-136">.. Se si esegue wt.exe dal menu Start: C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="6550b-136">..if you run wt.exe from the Start menu: C:\windows\system32</span></span>
</br>
<span data-ttu-id="6550b-137">.. Se si esegue wt.exe da Win + R:% USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="6550b-137">..if you run wt.exe from Win+R: %USERPROFILE%</span></span>
</br>
<span data-ttu-id="6550b-138">.. Se si esegue wt.exe dalla barra degli indirizzi di Explorer, ovvero qualunque sia la cartella esaminata.</span><span class="sxs-lookup"><span data-stu-id="6550b-138">..if you run wt.exe from the explorer address bar: whatever folder you were looking at.</span></span>
___

## <a name="dropdown-settings"></a><span data-ttu-id="6550b-139">Impostazioni per il menu a discesa</span><span class="sxs-lookup"><span data-stu-id="6550b-139">Dropdown settings</span></span>

<span data-ttu-id="6550b-140">![Terminale Windows - Menu a discesa](./../images/dropdown.png)
_Configurazione: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="6550b-140">![Windows Terminal dropdown](./../images/dropdown.png)
_Configuration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

### <a name="name"></a><span data-ttu-id="6550b-141">Nome</span><span class="sxs-lookup"><span data-stu-id="6550b-141">Name</span></span>

<span data-ttu-id="6550b-142">Nome del profilo che verrà visualizzato nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="6550b-142">This is the name of the profile that will be displayed in the dropdown menu.</span></span> <span data-ttu-id="6550b-143">Questo valore viene usato anche come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="6550b-143">This value is also used as the "title" to pass to the shell on startup.</span></span> <span data-ttu-id="6550b-144">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6550b-144">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="6550b-145">Per eseguire l'override di questo comportamento del titolo, usa `tabTitle`.</span><span class="sxs-lookup"><span data-stu-id="6550b-145">This "title" behavior can be overridden by using `tabTitle`.</span></span>

<span data-ttu-id="6550b-146">**Nome della proprietà:** `name`</span><span class="sxs-lookup"><span data-stu-id="6550b-146">**Property name:** `name`</span></span>

<span data-ttu-id="6550b-147">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="6550b-147">**Necessity:** Required</span></span>

<span data-ttu-id="6550b-148">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="6550b-148">**Accepts:** String</span></span>

### <a name="icon"></a><span data-ttu-id="6550b-149">Icona</span><span class="sxs-lookup"><span data-stu-id="6550b-149">Icon</span></span>

<span data-ttu-id="6550b-150">Questa operazione consente di impostare l'icona visualizzata all'interno della scheda, del menu a discesa, di JumpList e dello switcher di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="6550b-150">This sets the icon that displays within the tab, dropdown menu, jumplist, and tab switcher.</span></span>

<span data-ttu-id="6550b-151">**Nome della proprietà:** `icon`</span><span class="sxs-lookup"><span data-stu-id="6550b-151">**Property name:** `icon`</span></span>

<span data-ttu-id="6550b-152">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-152">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-153">**Accetta:** Percorso del file sotto forma di stringa o emoji</span><span class="sxs-lookup"><span data-stu-id="6550b-153">**Accepts:** File location as a string, or an emoji</span></span>

### <a name="hide-a-profile-from-the-dropdown"></a><span data-ttu-id="6550b-154">Nascondi un profilo nell'elenco a discesa</span><span class="sxs-lookup"><span data-stu-id="6550b-154">Hide a profile from the dropdown</span></span>

<span data-ttu-id="6550b-155">Se `hidden` è impostato su `true`, il profilo non verrà visualizzato nell'elenco dei profili.</span><span class="sxs-lookup"><span data-stu-id="6550b-155">If `hidden` is set to `true`, the profile will not appear in the list of profiles.</span></span> <span data-ttu-id="6550b-156">Può essere usata per nascondere i profili predefiniti e quelli generati dinamicamente, lasciandoli nel file settings.</span><span class="sxs-lookup"><span data-stu-id="6550b-156">This can be used to hide default profiles and dynamically generated profiles, while leaving them in your settings file.</span></span> <span data-ttu-id="6550b-157">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6550b-157">To learn more about dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="6550b-158">**Nome della proprietà:** `hidden`</span><span class="sxs-lookup"><span data-stu-id="6550b-158">**Property name:** `hidden`</span></span>

<span data-ttu-id="6550b-159">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-159">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-160">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-160">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="6550b-161">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-161">**Default value:** `false`</span></span>

<br />

___

## <a name="tab-title-settings"></a><span data-ttu-id="6550b-162">Impostazioni per i titoli delle schede</span><span class="sxs-lookup"><span data-stu-id="6550b-162">Tab title settings</span></span>

### <a name="custom-tab-title"></a><span data-ttu-id="6550b-163">Titolo scheda personalizzato</span><span class="sxs-lookup"><span data-stu-id="6550b-163">Custom tab title</span></span>

<span data-ttu-id="6550b-164">Se è impostata, sostituirà `name` come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="6550b-164">If set, this will replace the `name` as the title to pass to the shell on startup.</span></span> <span data-ttu-id="6550b-165">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6550b-165">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="6550b-166">Per informazioni su come impostare la shell come titolo, vedi l'[esercitazione relativa al titolo della scheda](./../tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="6550b-166">If you'd like to learn how to have the shell set your title, visit the [tab title tutorial](./../tutorials/tab-title.md).</span></span>

<span data-ttu-id="6550b-167">**Nome della proprietà:** `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="6550b-167">**Property name:** `tabTitle`</span></span>

<span data-ttu-id="6550b-168">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-168">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-169">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="6550b-169">**Accepts:** String</span></span>

### <a name="suppress-title-changes-from-the-shell"></a><span data-ttu-id="6550b-170">Non visualizzare le modifiche apportate al titolo dalla shell</span><span class="sxs-lookup"><span data-stu-id="6550b-170">Suppress title changes from the shell</span></span>

<span data-ttu-id="6550b-171">Quando è impostata su `true`, `tabTitle` sostituisce il titolo predefinito della scheda. Tutti i messaggi di modifica del titolo dall'applicazione verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="6550b-171">When this is set to `true`, `tabTitle` overrides the default title of the tab and any title change messages from the application will be suppressed.</span></span> <span data-ttu-id="6550b-172">Se `tabTitle` non è impostata, verrà usata `name`.</span><span class="sxs-lookup"><span data-stu-id="6550b-172">If `tabTitle` isn't set, `name` will be used instead.</span></span> <span data-ttu-id="6550b-173">Quando è impostata su `false`, `tabTitle` si comporta normalmente.</span><span class="sxs-lookup"><span data-stu-id="6550b-173">When this is set to `false`, `tabTitle` behaves as normal.</span></span>

<span data-ttu-id="6550b-174">**Nome della proprietà:** `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="6550b-174">**Property name:** `suppressApplicationTitle`</span></span>

<span data-ttu-id="6550b-175">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-175">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-176">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-176">**Accepts:** `true`, `false`</span></span>

<br />

___

## <a name="text-settings"></a><span data-ttu-id="6550b-177">Impostazioni per il testo</span><span class="sxs-lookup"><span data-stu-id="6550b-177">Text settings</span></span>

### <a name="font-face"></a><span data-ttu-id="6550b-178">Tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="6550b-178">Font face</span></span>

<span data-ttu-id="6550b-179">Nome del tipo di carattere usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-179">This is the name of the font face used in the profile.</span></span> <span data-ttu-id="6550b-180">Il terminale proverà ad eseguire il fallback a Consolas se non riesce a trovarlo o non è valido.</span><span class="sxs-lookup"><span data-stu-id="6550b-180">The terminal will try to fallback to Consolas if this can't be found or is invalid.</span></span> <span data-ttu-id="6550b-181">Per informazioni sulle altre varianti del tipo di carattere predefinito, Cascadia Mono, vedi la [tabella codici di Cascadia](./../cascadia-code.md).</span><span class="sxs-lookup"><span data-stu-id="6550b-181">To learn about the other variants of the default font, Cascadia Mono, visit the [Cascadia Code page](./../cascadia-code.md).</span></span>

<span data-ttu-id="6550b-182">**Nome della proprietà:** `fontFace`</span><span class="sxs-lookup"><span data-stu-id="6550b-182">**Property name:** `fontFace`</span></span>

<span data-ttu-id="6550b-183">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-183">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-184">**Accetta:** nome del tipo di carattere in formato stringa</span><span class="sxs-lookup"><span data-stu-id="6550b-184">**Accepts:** Font name as a string</span></span>

<span data-ttu-id="6550b-185">**Valore predefinito:** `"Cascadia Mono"`</span><span class="sxs-lookup"><span data-stu-id="6550b-185">**Default value:** `"Cascadia Mono"`</span></span>

### <a name="font-size"></a><span data-ttu-id="6550b-186">Dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="6550b-186">Font size</span></span>

<span data-ttu-id="6550b-187">Consente di impostare le dimensioni del carattere del profilo in punti.</span><span class="sxs-lookup"><span data-stu-id="6550b-187">This sets the profile's font size in points.</span></span>

<span data-ttu-id="6550b-188">**Nome della proprietà:** `fontSize`</span><span class="sxs-lookup"><span data-stu-id="6550b-188">**Property name:** `fontSize`</span></span>

<span data-ttu-id="6550b-189">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-189">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-190">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="6550b-190">**Accepts:** Integer</span></span>

<span data-ttu-id="6550b-191">**Valore predefinito:** `12`</span><span class="sxs-lookup"><span data-stu-id="6550b-191">**Default value:** `12`</span></span>

### <a name="font-weight"></a><span data-ttu-id="6550b-192">Peso carattere</span><span class="sxs-lookup"><span data-stu-id="6550b-192">Font weight</span></span>

<span data-ttu-id="6550b-193">Questa proprietà imposta lo spessore (tratti sottili o spessi) per il tipo di carattere del profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-193">This sets the weight (lightness or heaviness of the strokes) for the profile's font.</span></span>

<span data-ttu-id="6550b-194">**Nome della proprietà:** `fontWeight`</span><span class="sxs-lookup"><span data-stu-id="6550b-194">**Property name:** `fontWeight`</span></span>

<span data-ttu-id="6550b-195">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-195">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-196">**Accetta**  `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"` oppure un intero che corrisponde alla rappresentazione numerica dello spesso del tipo di carattere OpenType</span><span class="sxs-lookup"><span data-stu-id="6550b-196">**Accepts:** `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"`, or an integer corresponding to the numeric representation of the OpenType font weight</span></span>

<span data-ttu-id="6550b-197">**Valore predefinito:** `"normal"`</span><span class="sxs-lookup"><span data-stu-id="6550b-197">**Default value:** `"normal"`</span></span>

### <a name="padding"></a><span data-ttu-id="6550b-198">Spaziatura interna</span><span class="sxs-lookup"><span data-stu-id="6550b-198">Padding</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="6550b-199">Consente di impostare la spaziatura intorno al testo all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="6550b-199">This sets the padding around the text within the window.</span></span> <span data-ttu-id="6550b-200">Questo accetta tre formati diversi: `"#"` e imposta `#` la stessa spaziatura interna per tutti i lati, `"#, #"` imposta la stessa spaziatura interna per Left-Right e top-bottom e `"#, #, #, #"` imposta la spaziatura interna singolarmente per left, top, Right e Bottom.</span><span class="sxs-lookup"><span data-stu-id="6550b-200">This will accept three different formats: `"#"` and `#` set the same padding for all sides, `"#, #"` sets the same padding for left-right and top-bottom, and `"#, #, #, #"` sets the padding individually for left, top, right, and bottom.</span></span>

<span data-ttu-id="6550b-201">**Nome della proprietà:** `padding`</span><span class="sxs-lookup"><span data-stu-id="6550b-201">**Property name:** `padding`</span></span>

<span data-ttu-id="6550b-202">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-202">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-203">**Accetta:** Valori come stringa nei formati seguenti: `"#"` , `"#, #"` `"#, #, #, #"` o valore come Integer: `#`</span><span class="sxs-lookup"><span data-stu-id="6550b-203">**Accepts:** Values as a string in the following formats: `"#"`, `"#, #"`, `"#, #, #, #"` or value as an integer: `#`</span></span>

<span data-ttu-id="6550b-204">**Valore predefinito:** `"8, 8, 8, 8"`</span><span class="sxs-lookup"><span data-stu-id="6550b-204">**Default value:** `"8, 8, 8, 8"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Spaziatura interna](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="antialiasing-text"></a><span data-ttu-id="6550b-206">Anti-aliasing del testo</span><span class="sxs-lookup"><span data-stu-id="6550b-206">Antialiasing text</span></span>

<span data-ttu-id="6550b-207">Controlla la modalità di anti-aliasing del testo nel renderer.</span><span class="sxs-lookup"><span data-stu-id="6550b-207">This controls how text is antialiased in the renderer.</span></span> <span data-ttu-id="6550b-208">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="6550b-208">Note that changing this setting will require starting a new terminal instance.</span></span>

![Terminale Windows - Anti-aliasing del testo](./../images/antialiasing-mode.gif)

<span data-ttu-id="6550b-210">**Nome della proprietà:** `antialiasingMode`</span><span class="sxs-lookup"><span data-stu-id="6550b-210">**Property name:** `antialiasingMode`</span></span>

<span data-ttu-id="6550b-211">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-211">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-212">**Accetta:** `"grayscale"`, `"cleartype"`, `"aliased"`</span><span class="sxs-lookup"><span data-stu-id="6550b-212">**Accepts:** `"grayscale"`, `"cleartype"`, `"aliased"`</span></span>

<span data-ttu-id="6550b-213">**Valore predefinito:** `"grayscale"`</span><span class="sxs-lookup"><span data-stu-id="6550b-213">**Default value:** `"grayscale"`</span></span>

<br />

___

## <a name="cursor-settings"></a><span data-ttu-id="6550b-214">Impostazioni per il cursore</span><span class="sxs-lookup"><span data-stu-id="6550b-214">Cursor settings</span></span>

### <a name="cursor-shape"></a><span data-ttu-id="6550b-215">Forma del cursore</span><span class="sxs-lookup"><span data-stu-id="6550b-215">Cursor shape</span></span>

<span data-ttu-id="6550b-216">Consente di impostare la forma del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-216">This sets the cursor shape for the profile.</span></span> <span data-ttu-id="6550b-217">I cursori possibili sono i seguenti: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;)</span><span class="sxs-lookup"><span data-stu-id="6550b-217">The possible cursors are as follows: `"bar"` ( &#x2503; ), `"vintage"` ( &#x2583; ), `"underscore"` ( &#x2581; ), `"filledBox"` ( &#x2588; ), `"emptyBox"` ( &#x25AF; )</span></span>

<span data-ttu-id="6550b-218">**Nome della proprietà:** `cursorShape`</span><span class="sxs-lookup"><span data-stu-id="6550b-218">**Property name:** `cursorShape`</span></span>

<span data-ttu-id="6550b-219">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-219">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-220">**Accetta:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span><span class="sxs-lookup"><span data-stu-id="6550b-220">**Accepts:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span></span>

<span data-ttu-id="6550b-221">**Valore predefinito:** `"bar"`</span><span class="sxs-lookup"><span data-stu-id="6550b-221">**Default value:** `"bar"`</span></span>

### <a name="cursor-color"></a><span data-ttu-id="6550b-222">Colore del cursore</span><span class="sxs-lookup"><span data-stu-id="6550b-222">Cursor color</span></span>

<span data-ttu-id="6550b-223">Consente di impostare il colore del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-223">This sets the cursor color of the profile.</span></span> <span data-ttu-id="6550b-224">Sostituisce il valore di `cursorColor` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="6550b-224">This will override the `cursorColor` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="6550b-225">**Nome della proprietà:** `cursorColor`</span><span class="sxs-lookup"><span data-stu-id="6550b-225">**Property name:** `cursorColor`</span></span>

<span data-ttu-id="6550b-226">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-226">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-227">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="6550b-227">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="cursor-height"></a><span data-ttu-id="6550b-228">Altezza del cursore</span><span class="sxs-lookup"><span data-stu-id="6550b-228">Cursor height</span></span>

<span data-ttu-id="6550b-229">Consente di impostare l'altezza percentuale del cursore a partire dalla parte inferiore.</span><span class="sxs-lookup"><span data-stu-id="6550b-229">This sets the percentage height of the cursor starting from the bottom.</span></span> <span data-ttu-id="6550b-230">Funziona solo se `cursorShape` è impostata su `"vintage"`.</span><span class="sxs-lookup"><span data-stu-id="6550b-230">This will only work when `cursorShape` is set to `"vintage"`.</span></span>

<span data-ttu-id="6550b-231">**Nome della proprietà:** `cursorHeight`</span><span class="sxs-lookup"><span data-stu-id="6550b-231">**Property name:** `cursorHeight`</span></span>

<span data-ttu-id="6550b-232">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-232">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-233">**Accetta:** intero compreso tra 25-100</span><span class="sxs-lookup"><span data-stu-id="6550b-233">**Accepts:** Integer from 25-100</span></span>

<br />

___

## <a name="keyboard-settings"></a><span data-ttu-id="6550b-234">Impostazioni da tastiera</span><span class="sxs-lookup"><span data-stu-id="6550b-234">Keyboard settings</span></span>

### <a name="altgr-aliasing"></a><span data-ttu-id="6550b-235">Aliasing AltGr</span><span class="sxs-lookup"><span data-stu-id="6550b-235">AltGr aliasing</span></span>

<span data-ttu-id="6550b-236">Questa proprietà consente di controllare se Terminale Windows considererà <kbd>CTRL+ALT</kbd> come alias di <kbd>ALTGR</kbd>.</span><span class="sxs-lookup"><span data-stu-id="6550b-236">This allows you to control if Windows Terminal will treat <kbd>ctrl+alt</kbd> as an alias for <kbd>AltGr</kbd>.</span></span>

<span data-ttu-id="6550b-237">**Nome della proprietà:** `altGrAliasing`</span><span class="sxs-lookup"><span data-stu-id="6550b-237">**Property name:** `altGrAliasing`</span></span>

<span data-ttu-id="6550b-238">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-238">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-239">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-239">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="6550b-240">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="6550b-240">**Default value:** `true`</span></span>

<br />

___

## <a name="color-settings"></a><span data-ttu-id="6550b-241">Impostazioni per il colore</span><span class="sxs-lookup"><span data-stu-id="6550b-241">Color settings</span></span>

### <a name="color-scheme"></a><span data-ttu-id="6550b-242">Combinazione colori</span><span class="sxs-lookup"><span data-stu-id="6550b-242">Color scheme</span></span>

<span data-ttu-id="6550b-243">Nome della combinazione colori usata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-243">This is the name of the color scheme used in the profile.</span></span> <span data-ttu-id="6550b-244">Le combinazioni colori sono definite nell'oggetto `schemes`.</span><span class="sxs-lookup"><span data-stu-id="6550b-244">Color schemes are defined in the `schemes` object.</span></span> <span data-ttu-id="6550b-245">Per informazioni più dettagliate, vedi la [pagina Combinazioni colori](./color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="6550b-245">More detailed information can be found on the [Color schemes page](./color-schemes.md).</span></span>

<span data-ttu-id="6550b-246">**Nome della proprietà:** `colorScheme`</span><span class="sxs-lookup"><span data-stu-id="6550b-246">**Property name:** `colorScheme`</span></span>

<span data-ttu-id="6550b-247">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-247">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-248">**Accetta:** nome della combinazione colori in formato stringa</span><span class="sxs-lookup"><span data-stu-id="6550b-248">**Accepts:** Name of color scheme as a string</span></span>

<span data-ttu-id="6550b-249">**Valore predefinito:** `"Campbell"`</span><span class="sxs-lookup"><span data-stu-id="6550b-249">**Default value:** `"Campbell"`</span></span>

### <a name="tab-color"></a><span data-ttu-id="6550b-250">Colore delle schede</span><span class="sxs-lookup"><span data-stu-id="6550b-250">Tab color</span></span>

<span data-ttu-id="6550b-251">Viene impostato il colore della scheda del profilo. Se si utilizza la selezione colori scheda, questo colore verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="6550b-251">This sets the color of the profile's tab. Using the tab color picker will override this color.</span></span>

<span data-ttu-id="6550b-252">**Nome della proprietà:** `tabColor`</span><span class="sxs-lookup"><span data-stu-id="6550b-252">**Property name:** `tabColor`</span></span>

<span data-ttu-id="6550b-253">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-253">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-254">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="6550b-254">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="foreground-color"></a><span data-ttu-id="6550b-255">Colore primo piano</span><span class="sxs-lookup"><span data-stu-id="6550b-255">Foreground color</span></span>

<span data-ttu-id="6550b-256">Modifica il colore primo piano del profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-256">This changes the foreground color of the profile.</span></span> <span data-ttu-id="6550b-257">Sostituisce il valore di `foreground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="6550b-257">This overrides `foreground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="6550b-258">**Nome della proprietà:** `foreground`</span><span class="sxs-lookup"><span data-stu-id="6550b-258">**Property name:** `foreground`</span></span>

<span data-ttu-id="6550b-259">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-259">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-260">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="6550b-260">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="background-color"></a><span data-ttu-id="6550b-261">Colore di sfondo</span><span class="sxs-lookup"><span data-stu-id="6550b-261">Background color</span></span>

<span data-ttu-id="6550b-262">Modifica il colore di sfondo del profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-262">This changes the background color of the profile with this setting.</span></span> <span data-ttu-id="6550b-263">Sostituisce il valore di `background` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="6550b-263">This overrides `background` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="6550b-264">**Nome della proprietà:** `background`</span><span class="sxs-lookup"><span data-stu-id="6550b-264">**Property name:** `background`</span></span>

<span data-ttu-id="6550b-265">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-265">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-266">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="6550b-266">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="selection-background-color"></a><span data-ttu-id="6550b-267">Colore di sfondo della selezione</span><span class="sxs-lookup"><span data-stu-id="6550b-267">Selection background color</span></span>

<span data-ttu-id="6550b-268">Consente di impostare il colore di sfondo di una selezione nel profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-268">This sets the background color of a selection within the profile.</span></span> <span data-ttu-id="6550b-269">Sostituisce il valore di `selectionBackground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="6550b-269">This will override the `selectionBackground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="6550b-270">**Nome della proprietà:** `selectionBackground`</span><span class="sxs-lookup"><span data-stu-id="6550b-270">**Property name:** `selectionBackground`</span></span>

<span data-ttu-id="6550b-271">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-271">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-272">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="6550b-272">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

<br />

___

## <a name="acrylic-settings"></a><span data-ttu-id="6550b-273">Impostazioni per acrilico</span><span class="sxs-lookup"><span data-stu-id="6550b-273">Acrylic settings</span></span>

### <a name="enable-acrylic"></a><span data-ttu-id="6550b-274">Abilita acrilico</span><span class="sxs-lookup"><span data-stu-id="6550b-274">Enable acrylic</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="6550b-275">Quando è impostata su `true`, la finestra avrà uno sfondo acrilico.</span><span class="sxs-lookup"><span data-stu-id="6550b-275">When this is set to `true`, the window will have an acrylic background.</span></span> <span data-ttu-id="6550b-276">Quando è impostato su `false`, la finestra avrà uno sfondo normale e senza trame.</span><span class="sxs-lookup"><span data-stu-id="6550b-276">When it's set to `false`, the window will have a plain, untextured background.</span></span> <span data-ttu-id="6550b-277">A causa delle limitazioni del sistema operativo, la trasparenza si applica solo alle finestre con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="6550b-277">The transparency only applies to focused windows due to OS limitations.</span></span>

<span data-ttu-id="6550b-278">**Nome della proprietà:** `useAcrylic`</span><span class="sxs-lookup"><span data-stu-id="6550b-278">**Property name:** `useAcrylic`</span></span>

<span data-ttu-id="6550b-279">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-279">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-280">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-280">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="6550b-281">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-281">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Acrilico](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a><span data-ttu-id="6550b-283">Opacità acrilico</span><span class="sxs-lookup"><span data-stu-id="6550b-283">Acrylic opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="6550b-284">Quando `useAcrylic` è impostata su `true`, imposta la trasparenza della finestra per il profilo.</span><span class="sxs-lookup"><span data-stu-id="6550b-284">When `useAcrylic` is set to `true`, this sets the transparency of the window for the profile.</span></span> <span data-ttu-id="6550b-285">Accetta valori a virgola mobile compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="6550b-285">This accepts floating point values from 0-1.</span></span>

<span data-ttu-id="6550b-286">**Nome della proprietà:** `acrylicOpacity`</span><span class="sxs-lookup"><span data-stu-id="6550b-286">**Property name:** `acrylicOpacity`</span></span>

<span data-ttu-id="6550b-287">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-287">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-288">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="6550b-288">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="6550b-289">**Valore predefinito:** `0.5`</span><span class="sxs-lookup"><span data-stu-id="6550b-289">**Default value:** `0.5`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Opacità acrilico](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="background-image-settings"></a><span data-ttu-id="6550b-291">Impostazioni per immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="6550b-291">Background image settings</span></span>

### <a name="setting-the-background-image"></a><span data-ttu-id="6550b-292">Impostazione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="6550b-292">Setting the background image</span></span>

<span data-ttu-id="6550b-293">Consente di impostare il percorso del file dell'immagine da tracciare sullo sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="6550b-293">This sets the file location of the image to draw over the window background.</span></span> <span data-ttu-id="6550b-294">L'immagine di sfondo può essere un file con estensione jpg, png o gif.</span><span class="sxs-lookup"><span data-stu-id="6550b-294">The background image can be a .jpg, .png, or .gif file.</span></span> <span data-ttu-id="6550b-295">`"desktopWallpaper"` imposta l'immagine di sfondo sullo sfondo del desktop.</span><span class="sxs-lookup"><span data-stu-id="6550b-295">`"desktopWallpaper"` will set the background image to the desktop's wallpaper.</span></span>

<span data-ttu-id="6550b-296">**Nome della proprietà:** `backgroundImage`</span><span class="sxs-lookup"><span data-stu-id="6550b-296">**Property name:** `backgroundImage`</span></span>

<span data-ttu-id="6550b-297">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-297">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-298">**Accetta:** Percorso del file sotto forma di stringa o `"desktopWallpaper"`</span><span class="sxs-lookup"><span data-stu-id="6550b-298">**Accepts:** File location as a string or `"desktopWallpaper"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6550b-299">L'impostazione `"desktopWallpaper"` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="6550b-299">The `"desktopWallpaper"` setting is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="background-image-stretch-mode"></a><span data-ttu-id="6550b-300">Modalità di estensione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="6550b-300">Background image stretch mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="6550b-301">Consente di impostare la modalità di ridimensionamento dell'immagine di sfondo in modo che occupi tutto lo spazio della finestra.</span><span class="sxs-lookup"><span data-stu-id="6550b-301">This sets how the background image is resized to fill the window.</span></span>

<span data-ttu-id="6550b-302">**Nome della proprietà:** `backgroundImageStretchMode`</span><span class="sxs-lookup"><span data-stu-id="6550b-302">**Property name:** `backgroundImageStretchMode`</span></span>

<span data-ttu-id="6550b-303">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-303">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-304">**Accetta:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="6550b-304">**Accepts:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span></span>

<span data-ttu-id="6550b-305">**Valore predefinito:** `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="6550b-305">**Default value:** `"uniformToFill"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="6550b-306">![Terminale Windows - Modalità di estensione dell'immagine di sfondo](./../images/background-image-stretch-mode.gif)
 _[Origine dell'immagine di sfondo](https://wallpaperhub.app/wallpapers/6287)_</span><span class="sxs-lookup"><span data-stu-id="6550b-306">![Windows Terminal background image stretch mode](./../images/background-image-stretch-mode.gif)
_[Background image source](https://wallpaperhub.app/wallpapers/6287)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a><span data-ttu-id="6550b-307">Allineamento dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="6550b-307">Background image alignment</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="6550b-308">Consente di impostare la modalità di allineamento dell'immagine di sfondo ai bordi della finestra.</span><span class="sxs-lookup"><span data-stu-id="6550b-308">This sets how the background image aligns to the boundaries of the window.</span></span>

<span data-ttu-id="6550b-309">**Nome della proprietà:** `backgroundImageAlignment`</span><span class="sxs-lookup"><span data-stu-id="6550b-309">**Property name:** `backgroundImageAlignment`</span></span>

<span data-ttu-id="6550b-310">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-310">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-311">**Accetta:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span><span class="sxs-lookup"><span data-stu-id="6550b-311">**Accepts:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span></span>

<span data-ttu-id="6550b-312">**Valore predefinito:** `"center"`</span><span class="sxs-lookup"><span data-stu-id="6550b-312">**Default value:** `"center"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="6550b-313">![Terminale Windows - Allineamento dell'immagine di sfondo](./../images/background-image-alignment.gif)
 _[Origine dell'immagine di sfondo](https://design.ubuntu.com/brand/ubuntu-logo/)_</span><span class="sxs-lookup"><span data-stu-id="6550b-313">![Windows Terminal background image alignment](./../images/background-image-alignment.gif)
_[Background image source](https://design.ubuntu.com/brand/ubuntu-logo/)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a><span data-ttu-id="6550b-314">Opacità dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="6550b-314">Background image opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="6550b-315">Consente di impostare la trasparenza dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="6550b-315">This sets the transparency of the background image.</span></span>

:::column-end:::
:::row-end:::

<span data-ttu-id="6550b-316">**Nome della proprietà:** `backgroundImageOpacity`</span><span class="sxs-lookup"><span data-stu-id="6550b-316">**Property name:** `backgroundImageOpacity`</span></span>

<span data-ttu-id="6550b-317">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-317">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-318">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="6550b-318">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="6550b-319">**Valore predefinito:** `1.0`</span><span class="sxs-lookup"><span data-stu-id="6550b-319">**Default value:** `1.0`</span></span>

<br />

___

## <a name="scroll-settings"></a><span data-ttu-id="6550b-320">Impostazioni per lo scorrimento</span><span class="sxs-lookup"><span data-stu-id="6550b-320">Scroll settings</span></span>

### <a name="scrollbar-visibility"></a><span data-ttu-id="6550b-321">Visibilità della barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="6550b-321">Scrollbar visibility</span></span>

<span data-ttu-id="6550b-322">Consente di impostare la visibilità della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="6550b-322">This sets the visibility of the scrollbar.</span></span>

<span data-ttu-id="6550b-323">**Nome della proprietà:** `scrollbarState`</span><span class="sxs-lookup"><span data-stu-id="6550b-323">**Property name:** `scrollbarState`</span></span>

<span data-ttu-id="6550b-324">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-324">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-325">**Accetta:** `"visible"`, `"hidden"`</span><span class="sxs-lookup"><span data-stu-id="6550b-325">**Accepts:** `"visible"`, `"hidden"`</span></span>

### <a name="scroll-to-input-line-when-typing"></a><span data-ttu-id="6550b-326">Scorri fino alla riga di input durante la digitazione</span><span class="sxs-lookup"><span data-stu-id="6550b-326">Scroll to input line when typing</span></span>

<span data-ttu-id="6550b-327">Quando è impostata su `true`, la finestra scorre fino alla riga di input del comando durante la digitazione.</span><span class="sxs-lookup"><span data-stu-id="6550b-327">When this is set to `true`, the window will scroll to the command input line when typing.</span></span> <span data-ttu-id="6550b-328">Quando è impostata su `false`, lo scorrimento della finestra non è attivato quando inizi a digitare.</span><span class="sxs-lookup"><span data-stu-id="6550b-328">When it's set to `false`, the window will not scroll when you start typing.</span></span>

<span data-ttu-id="6550b-329">**Nome della proprietà:** `snapOnInput`</span><span class="sxs-lookup"><span data-stu-id="6550b-329">**Property name:** `snapOnInput`</span></span>

<span data-ttu-id="6550b-330">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-330">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-331">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-331">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="6550b-332">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="6550b-332">**Default value:** `true`</span></span>

### <a name="history-size"></a><span data-ttu-id="6550b-333">Dimensioni della cronologia</span><span class="sxs-lookup"><span data-stu-id="6550b-333">History size</span></span>

<span data-ttu-id="6550b-334">Consente di impostare il numero di righe a cui è possibile passare scorrendo che precedono quelle visualizzate nella finestra.</span><span class="sxs-lookup"><span data-stu-id="6550b-334">This sets the number of lines above the ones displayed in the window you can scroll back to.</span></span>

<span data-ttu-id="6550b-335">**Nome della proprietà:** `historySize`</span><span class="sxs-lookup"><span data-stu-id="6550b-335">**Property name:** `historySize`</span></span>

<span data-ttu-id="6550b-336">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-336">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-337">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="6550b-337">**Accepts:** Integer</span></span>

<span data-ttu-id="6550b-338">**Valore predefinito:** `9001`</span><span class="sxs-lookup"><span data-stu-id="6550b-338">**Default value:** `9001`</span></span>

<br />

___

## <a name="how-the-profile-closes-when-exiting"></a><span data-ttu-id="6550b-339">Modalità di chiusura del profilo all'uscita</span><span class="sxs-lookup"><span data-stu-id="6550b-339">How the profile closes when exiting</span></span>

<span data-ttu-id="6550b-340">Consente di impostare la reazione del profilo alla chiusura o a un errore all'avvio.</span><span class="sxs-lookup"><span data-stu-id="6550b-340">This sets how the profile reacts to termination or failure to launch.</span></span> <span data-ttu-id="6550b-341">Con `"graceful"`, il profilo verrà chiuso quando viene digitato `exit` o quando il processo viene chiuso normalmente.</span><span class="sxs-lookup"><span data-stu-id="6550b-341">`"graceful"` will close the profile when `exit` is typed or when the process exits normally.</span></span> <span data-ttu-id="6550b-342">Con `"always"` il profilo verrà sempre chiuso, mentre con `"never"` non verrà mai chiuso.</span><span class="sxs-lookup"><span data-stu-id="6550b-342">`"always"` will always close the profile and `"never"` will never close the profile.</span></span> <span data-ttu-id="6550b-343">`true` e `false` vengono accettati come sinonimi rispettivamente per `"graceful"` e `"never"`.</span><span class="sxs-lookup"><span data-stu-id="6550b-343">`true` and `false` are accepted as synonyms for `"graceful"` and `"never"`, respectively.</span></span>

<span data-ttu-id="6550b-344">**Nome della proprietà:** `closeOnExit`</span><span class="sxs-lookup"><span data-stu-id="6550b-344">**Property name:** `closeOnExit`</span></span>

<span data-ttu-id="6550b-345">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-345">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-346">**Accetta:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-346">**Accepts:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span></span>

<span data-ttu-id="6550b-347">**Valore predefinito:** `"graceful"`</span><span class="sxs-lookup"><span data-stu-id="6550b-347">**Default value:** `"graceful"`</span></span>

<br />

___

## <a name="bell-settings-preview"></a><span data-ttu-id="6550b-348">Impostazioni campanello ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="6550b-348">Bell settings ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="6550b-349">Controlla cosa accade quando l'applicazione emette un carattere BEL.</span><span class="sxs-lookup"><span data-stu-id="6550b-349">Controls what happens when the application emits a BEL character.</span></span> <span data-ttu-id="6550b-350">Quando è impostato su `"audible"` , il terminale risuonerà un suono.</span><span class="sxs-lookup"><span data-stu-id="6550b-350">When set to `"audible"`, the terminal will play a sound.</span></span> <span data-ttu-id="6550b-351">Quando è impostato su `"none"` , non viene eseguita alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="6550b-351">When set to `"none"`, nothing will happen.</span></span>

<span data-ttu-id="6550b-352">**Nome della proprietà:** `bellStyle`</span><span class="sxs-lookup"><span data-stu-id="6550b-352">**Property name:** `bellStyle`</span></span>

<span data-ttu-id="6550b-353">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-353">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-354">**Accetta:** `"audible"`, `"none"`</span><span class="sxs-lookup"><span data-stu-id="6550b-354">**Accepts:** `"audible"`, `"none"`</span></span>

<span data-ttu-id="6550b-355">**Valore predefinito:** `"audible"`</span><span class="sxs-lookup"><span data-stu-id="6550b-355">**Default value:** `"audible"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6550b-356">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="6550b-356">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

<br />

___

## <a name="retro-terminal-effects"></a><span data-ttu-id="6550b-357">Effetti per terminale retro</span><span class="sxs-lookup"><span data-stu-id="6550b-357">Retro terminal effects</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="6550b-358">Quando è impostata su `true`, il terminale emulerà un monitor CRT classico con linee di scansione e bordi di testo sfocati.</span><span class="sxs-lookup"><span data-stu-id="6550b-358">When this is set to `true`, the terminal will emulate a classic CRT display with scan lines and blurry text edges.</span></span> <span data-ttu-id="6550b-359">Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="6550b-359">This is an experimental feature and its continued existence is not guaranteed.</span></span>

<span data-ttu-id="6550b-360">**Nome della proprietà:** `experimental.retroTerminalEffect`</span><span class="sxs-lookup"><span data-stu-id="6550b-360">**Property name:** `experimental.retroTerminalEffect`</span></span>

<span data-ttu-id="6550b-361">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="6550b-361">**Necessity:** Optional</span></span>

<span data-ttu-id="6550b-362">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-362">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="6550b-363">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="6550b-363">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="6550b-364">![Terminale Windows - Effetto sperimentale per terminale retro](./../images/experimental-retro-terminal-effect.gif)
_Configurazione: [Prompt dei comandi retro](./../custom-terminal-gallery/retro-command-prompt.md)_</span><span class="sxs-lookup"><span data-stu-id="6550b-364">![Windows Terminal experimental retro terminal effect](./../images/experimental-retro-terminal-effect.gif)
_Configuration: [Retro Command Prompt](./../custom-terminal-gallery/retro-command-prompt.md)_</span></span>

:::column-end:::
:::row-end:::
