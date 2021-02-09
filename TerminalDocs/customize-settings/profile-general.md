---
title: Impostazioni del profilo generale di Windows Terminal
description: Informazioni su come personalizzare le impostazioni generali del profilo nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: e8eb635075e5ea87c35713762f95cc0a375fe4b4
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974872"
---
# <a name="general-profile-settings-in-windows-terminal"></a><span data-ttu-id="a8d1d-103">Impostazioni generali del profilo nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="a8d1d-103">General profile settings in Windows Terminal</span></span>

<span data-ttu-id="a8d1d-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="a8d1d-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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

> [!IMPORTANT]
> <span data-ttu-id="a8d1d-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="a8d1d-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="a8d1d-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="a8d1d-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="name"></a><span data-ttu-id="a8d1d-108">Nome</span><span class="sxs-lookup"><span data-stu-id="a8d1d-108">Name</span></span>

<span data-ttu-id="a8d1d-109">Nome del profilo che verrà visualizzato nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-109">This is the name of the profile that will be displayed in the dropdown menu.</span></span> <span data-ttu-id="a8d1d-110">Questo valore viene usato anche come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-110">This value is also used as the "title" to pass to the shell on startup.</span></span> <span data-ttu-id="a8d1d-111">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-111">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="a8d1d-112">Per eseguire l'override di questo comportamento del titolo, usa `tabTitle`.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-112">This "title" behavior can be overridden by using `tabTitle`.</span></span>

<span data-ttu-id="a8d1d-113">**Nome della proprietà:** `name`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-113">**Property name:** `name`</span></span>

<span data-ttu-id="a8d1d-114">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="a8d1d-114">**Necessity:** Required</span></span>

<span data-ttu-id="a8d1d-115">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="a8d1d-115">**Accepts:** String</span></span>

<br />

___

## <a name="command-line"></a><span data-ttu-id="a8d1d-116">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="a8d1d-116">Command line</span></span>

<span data-ttu-id="a8d1d-117">File eseguibile usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-117">This is the executable used in the profile.</span></span>

<span data-ttu-id="a8d1d-118">**Nome della proprietà:** `commandline`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-118">**Property name:** `commandline`</span></span>

<span data-ttu-id="a8d1d-119">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a8d1d-119">**Necessity:** Optional</span></span>

<span data-ttu-id="a8d1d-120">**Accetta:** nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="a8d1d-120">**Accepts:** Executable file name as a string</span></span>

<span data-ttu-id="a8d1d-121">**Valore predefinito:** `"cmd.exe"`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-121">**Default value:** `"cmd.exe"`</span></span>

<br />

___

## <a name="starting-directory"></a><span data-ttu-id="a8d1d-122">Directory iniziale</span><span class="sxs-lookup"><span data-stu-id="a8d1d-122">Starting directory</span></span>

<span data-ttu-id="a8d1d-123">Directory in cui viene avviata la shell quando viene caricata.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-123">This is the directory the shell starts in when it is loaded.</span></span>

<span data-ttu-id="a8d1d-124">**Nome della proprietà:** `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-124">**Property name:** `startingDirectory`</span></span>

<span data-ttu-id="a8d1d-125">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a8d1d-125">**Necessity:** Optional</span></span>

<span data-ttu-id="a8d1d-126">**Accetta:** percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="a8d1d-126">**Accepts:** Folder location as a string</span></span>

<span data-ttu-id="a8d1d-127">**Valore predefinito:** `"%USERPROFILE%"`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-127">**Default value:** `"%USERPROFILE%"`</span></span>

<span data-ttu-id="a8d1d-128">**Esempio:** Avviare il profilo di PowerShell nella cartella *GitHubRepos* della directory dei *documenti* individuando il profilo di powershell.exe e aggiungendo `"startingDirectory": "%USERPROFILE%/Documents/GitHubRepos",`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-128">**Example:** Start the PowerShell profile in the *GitHubRepos* folder of your *Documents* directory by finding the powershell.exe profile and adding `"startingDirectory": "%USERPROFILE%/Documents/GitHubRepos",`</span></span>

<span data-ttu-id="a8d1d-129">**Esempio con WSL:** Quando si imposta la directory iniziale per una [distribuzione Linux installata tramite WSL](https://docs.microsoft.com/windows/wsl/install-win10), usare il formato: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"` , sostituendo con i segnaposto con i nomi appropriati della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-129">**Example with WSL:** When setting the starting directory for a [Linux distribution installed via WSL](https://docs.microsoft.com/windows/wsl/install-win10), use the format: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"`, replacing with the placeholders with the proper names of your distribution.</span></span> <span data-ttu-id="a8d1d-130">Ad esempio: `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-130">For example, `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.</span></span>

<span data-ttu-id="a8d1d-131">**Comportamento predefinito:** Se il valore startingDirectory non è specificato, si otterranno risultati diversi a seconda della posizione in cui si avvia il terminale:</span><span class="sxs-lookup"><span data-stu-id="a8d1d-131">**Default behavior:** When the startingDirectory value is not specified, you will get different results depending on where you launch Terminal:</span></span>
- <span data-ttu-id="a8d1d-132">Se si esegue il terminale di Windows dal menu Start: C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="a8d1d-132">If you run Windows Terminal from the Start menu: C:\windows\system32</span></span>
- <span data-ttu-id="a8d1d-133">Se si esegue wt.exe dal menu Start: C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="a8d1d-133">If you run wt.exe from the Start menu: C:\windows\system32</span></span>
- <span data-ttu-id="a8d1d-134">Se si esegue wt.exe da Win + R:% USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="a8d1d-134">If you run wt.exe from Win+R: %USERPROFILE%</span></span>
- <span data-ttu-id="a8d1d-135">Se si esegue wt.exe dalla barra degli indirizzi di Explorer, ovvero qualunque sia la cartella esaminata.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-135">If you run wt.exe from the explorer address bar: whatever folder you were looking at.</span></span>

> [!NOTE]
> <span data-ttu-id="a8d1d-136">Le barre rovesciate devono essere precedute da un carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-136">Backslashes need to be escaped.</span></span> <span data-ttu-id="a8d1d-137">Ad esempio, `C:\Users\USERNAME\Documents` deve essere immesso come `C:\\Users\\USERNAME\\Documents` .</span><span class="sxs-lookup"><span data-stu-id="a8d1d-137">For example, `C:\Users\USERNAME\Documents` should be entered as `C:\\Users\\USERNAME\\Documents`.</span></span>

___

## <a name="icon"></a><span data-ttu-id="a8d1d-138">Icona</span><span class="sxs-lookup"><span data-stu-id="a8d1d-138">Icon</span></span>

<span data-ttu-id="a8d1d-139">Questa operazione consente di impostare l'icona visualizzata all'interno della scheda, del menu a discesa, di JumpList e dello switcher di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-139">This sets the icon that displays within the tab, dropdown menu, jumplist, and tab switcher.</span></span>

<span data-ttu-id="a8d1d-140">**Nome della proprietà:** `icon`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-140">**Property name:** `icon`</span></span>

<span data-ttu-id="a8d1d-141">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a8d1d-141">**Necessity:** Optional</span></span>

<span data-ttu-id="a8d1d-142">**Accetta:** Percorso del file sotto forma di stringa o emoji</span><span class="sxs-lookup"><span data-stu-id="a8d1d-142">**Accepts:** File location as a string, or an emoji</span></span>

<span data-ttu-id="a8d1d-143">**Esempio:**  Inserendo l'immagine dell'icona `ubuntu.ico` nella cartella `%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState` che si trova in, è possibile visualizzare l'icona aggiungendo questa riga al profilo nel settings.jsin: `"icon": "ms-appdata:///roaming/ubuntu.ico"` .</span><span class="sxs-lookup"><span data-stu-id="a8d1d-143">**Example:**  Placing the icon image `ubuntu.ico` in the folder located at `%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\RoamingState`, you can display the icon by adding this line to the profile in your settings.json: `"icon": "ms-appdata:///roaming/ubuntu.ico"`.</span></span>

<br>
___

## <a name="tab-title"></a><span data-ttu-id="a8d1d-144">Titolo scheda</span><span class="sxs-lookup"><span data-stu-id="a8d1d-144">Tab title</span></span>

<span data-ttu-id="a8d1d-145">Se è impostata, sostituirà `name` come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-145">If set, this will replace the `name` as the title to pass to the shell on startup.</span></span> <span data-ttu-id="a8d1d-146">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-146">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="a8d1d-147">Per informazioni su come impostare la shell come titolo, vedi l'[esercitazione relativa al titolo della scheda](./../tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="a8d1d-147">If you'd like to learn how to have the shell set your title, visit the [tab title tutorial](./../tutorials/tab-title.md).</span></span>

<span data-ttu-id="a8d1d-148">**Nome della proprietà:** `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-148">**Property name:** `tabTitle`</span></span>

<span data-ttu-id="a8d1d-149">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a8d1d-149">**Necessity:** Optional</span></span>

<span data-ttu-id="a8d1d-150">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="a8d1d-150">**Accepts:** String</span></span>

<br />

___

## <a name="hide-profile-from-dropdown"></a><span data-ttu-id="a8d1d-151">Nascondi profilo dall'elenco a discesa</span><span class="sxs-lookup"><span data-stu-id="a8d1d-151">Hide profile from dropdown</span></span>

<span data-ttu-id="a8d1d-152">Se `hidden` è impostato su `true`, il profilo non verrà visualizzato nell'elenco dei profili.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-152">If `hidden` is set to `true`, the profile will not appear in the list of profiles.</span></span> <span data-ttu-id="a8d1d-153">Può essere usata per nascondere i profili predefiniti e quelli generati dinamicamente, lasciandoli nel file settings.</span><span class="sxs-lookup"><span data-stu-id="a8d1d-153">This can be used to hide default profiles and dynamically generated profiles, while leaving them in your settings file.</span></span> <span data-ttu-id="a8d1d-154">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="a8d1d-154">To learn more about dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="a8d1d-155">**Nome della proprietà:** `hidden`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-155">**Property name:** `hidden`</span></span>

<span data-ttu-id="a8d1d-156">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="a8d1d-156">**Necessity:** Optional</span></span>

<span data-ttu-id="a8d1d-157">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-157">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="a8d1d-158">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="a8d1d-158">**Default value:** `false`</span></span>
