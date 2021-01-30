---
title: Impostazioni del profilo generale di Windows Terminal
description: Informazioni su come personalizzare le impostazioni generali del profilo nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: ce5b495df7048b2bff549b75f260df8e50b7ce74
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041969"
---
# <a name="general-profile-settings-in-windows-terminal"></a><span data-ttu-id="ba0a9-103">Impostazioni generali del profilo nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="ba0a9-103">General profile settings in Windows Terminal</span></span>

<span data-ttu-id="ba0a9-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="ba0a9-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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
> <span data-ttu-id="ba0a9-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="ba0a9-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="ba0a9-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="ba0a9-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="name"></a><span data-ttu-id="ba0a9-108">Nome</span><span class="sxs-lookup"><span data-stu-id="ba0a9-108">Name</span></span>

<span data-ttu-id="ba0a9-109">Nome del profilo che verrà visualizzato nel menu a discesa.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-109">This is the name of the profile that will be displayed in the dropdown menu.</span></span> <span data-ttu-id="ba0a9-110">Questo valore viene usato anche come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-110">This value is also used as the "title" to pass to the shell on startup.</span></span> <span data-ttu-id="ba0a9-111">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-111">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="ba0a9-112">Per eseguire l'override di questo comportamento del titolo, usa `tabTitle`.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-112">This "title" behavior can be overridden by using `tabTitle`.</span></span>

<span data-ttu-id="ba0a9-113">**Nome della proprietà:** `name`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-113">**Property name:** `name`</span></span>

<span data-ttu-id="ba0a9-114">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="ba0a9-114">**Necessity:** Required</span></span>

<span data-ttu-id="ba0a9-115">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="ba0a9-115">**Accepts:** String</span></span>

<br />

___

## <a name="command-line"></a><span data-ttu-id="ba0a9-116">Riga di comando</span><span class="sxs-lookup"><span data-stu-id="ba0a9-116">Command line</span></span>

<span data-ttu-id="ba0a9-117">File eseguibile usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-117">This is the executable used in the profile.</span></span>

<span data-ttu-id="ba0a9-118">**Nome della proprietà:** `commandline`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-118">**Property name:** `commandline`</span></span>

<span data-ttu-id="ba0a9-119">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="ba0a9-119">**Necessity:** Optional</span></span>

<span data-ttu-id="ba0a9-120">**Accetta:** nome del file eseguibile in formato stringa</span><span class="sxs-lookup"><span data-stu-id="ba0a9-120">**Accepts:** Executable file name as a string</span></span>

<span data-ttu-id="ba0a9-121">**Valore predefinito:** `"cmd.exe"`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-121">**Default value:** `"cmd.exe"`</span></span>

<br />

___

## <a name="starting-directory"></a><span data-ttu-id="ba0a9-122">Directory iniziale</span><span class="sxs-lookup"><span data-stu-id="ba0a9-122">Starting directory</span></span>

<span data-ttu-id="ba0a9-123">Directory in cui viene avviata la shell quando viene caricata.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-123">This is the directory the shell starts in when it is loaded.</span></span>

<span data-ttu-id="ba0a9-124">**Nome della proprietà:** `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-124">**Property name:** `startingDirectory`</span></span>

<span data-ttu-id="ba0a9-125">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="ba0a9-125">**Necessity:** Optional</span></span>

<span data-ttu-id="ba0a9-126">**Accetta:** percorso della cartella in formato stringa</span><span class="sxs-lookup"><span data-stu-id="ba0a9-126">**Accepts:** Folder location as a string</span></span>

<span data-ttu-id="ba0a9-127">**Valore predefinito:** `"%USERPROFILE%"`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-127">**Default value:** `"%USERPROFILE%"`</span></span>

<br />

> [!NOTE]
> <span data-ttu-id="ba0a9-128">Quando si imposta la directory iniziale a cui si aprono le distribuzioni WSL installate, è necessario usare il formato seguente: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"` , sostituendo con il nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-128">When setting the starting directory that your installed WSL distributions open to, you should use this format: `"startingDirectory": "\\\\wsl$\\DISTRO NAME\\home\\USERNAME"`, replacing with the name of your distribution.</span></span> <span data-ttu-id="ba0a9-129">Ad esempio: `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-129">For example, `"startingDirectory": "\\\\wsl$\\Ubuntu-20.04\\home\\user1"`.</span></span>

> [!NOTE]
> <span data-ttu-id="ba0a9-130">L'omissione del valore startingDirectory in un profilo comporta...</span><span class="sxs-lookup"><span data-stu-id="ba0a9-130">Omitting the startingDirectory value in a profile results in...</span></span>
</br>
<span data-ttu-id="ba0a9-131">.. Se si esegue il terminale di Windows dal menu Start: C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="ba0a9-131">..if you run Windows Terminal from the Start menu: C:\windows\system32</span></span>
</br>
<span data-ttu-id="ba0a9-132">.. Se si esegue wt.exe dal menu Start: C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="ba0a9-132">..if you run wt.exe from the Start menu: C:\windows\system32</span></span>
</br>
<span data-ttu-id="ba0a9-133">.. Se si esegue wt.exe da Win + R:% USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="ba0a9-133">..if you run wt.exe from Win+R: %USERPROFILE%</span></span>
</br>
<span data-ttu-id="ba0a9-134">.. Se si esegue wt.exe dalla barra degli indirizzi di Explorer, ovvero qualunque sia la cartella esaminata.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-134">..if you run wt.exe from the explorer address bar: whatever folder you were looking at.</span></span>
___

## <a name="icon"></a><span data-ttu-id="ba0a9-135">Icona</span><span class="sxs-lookup"><span data-stu-id="ba0a9-135">Icon</span></span>

<span data-ttu-id="ba0a9-136">Questa operazione consente di impostare l'icona visualizzata all'interno della scheda, del menu a discesa, di JumpList e dello switcher di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-136">This sets the icon that displays within the tab, dropdown menu, jumplist, and tab switcher.</span></span>

<span data-ttu-id="ba0a9-137">**Nome della proprietà:** `icon`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-137">**Property name:** `icon`</span></span>

<span data-ttu-id="ba0a9-138">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="ba0a9-138">**Necessity:** Optional</span></span>

<span data-ttu-id="ba0a9-139">**Accetta:** Percorso del file sotto forma di stringa o emoji</span><span class="sxs-lookup"><span data-stu-id="ba0a9-139">**Accepts:** File location as a string, or an emoji</span></span>

<br />

___

## <a name="tab-title"></a><span data-ttu-id="ba0a9-140">Titolo scheda</span><span class="sxs-lookup"><span data-stu-id="ba0a9-140">Tab title</span></span>

<span data-ttu-id="ba0a9-141">Se è impostata, sostituirà `name` come titolo da passare alla shell all'avvio.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-141">If set, this will replace the `name` as the title to pass to the shell on startup.</span></span> <span data-ttu-id="ba0a9-142">Alcune shell, ad esempio `bash`, possono scegliere di ignorare questo valore iniziale, mentre altre (`Command Prompt`, `PowerShell`) possono usare questo valore per tutta la durata dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-142">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="ba0a9-143">Per informazioni su come impostare la shell come titolo, vedi l'[esercitazione relativa al titolo della scheda](./../tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="ba0a9-143">If you'd like to learn how to have the shell set your title, visit the [tab title tutorial](./../tutorials/tab-title.md).</span></span>

<span data-ttu-id="ba0a9-144">**Nome della proprietà:** `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-144">**Property name:** `tabTitle`</span></span>

<span data-ttu-id="ba0a9-145">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="ba0a9-145">**Necessity:** Optional</span></span>

<span data-ttu-id="ba0a9-146">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="ba0a9-146">**Accepts:** String</span></span>

<br />

___

## <a name="hide-profile-from-dropdown"></a><span data-ttu-id="ba0a9-147">Nascondi profilo dall'elenco a discesa</span><span class="sxs-lookup"><span data-stu-id="ba0a9-147">Hide profile from dropdown</span></span>

<span data-ttu-id="ba0a9-148">Se `hidden` è impostato su `true`, il profilo non verrà visualizzato nell'elenco dei profili.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-148">If `hidden` is set to `true`, the profile will not appear in the list of profiles.</span></span> <span data-ttu-id="ba0a9-149">Può essere usata per nascondere i profili predefiniti e quelli generati dinamicamente, lasciandoli nel file settings.</span><span class="sxs-lookup"><span data-stu-id="ba0a9-149">This can be used to hide default profiles and dynamically generated profiles, while leaving them in your settings file.</span></span> <span data-ttu-id="ba0a9-150">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ba0a9-150">To learn more about dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="ba0a9-151">**Nome della proprietà:** `hidden`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-151">**Property name:** `hidden`</span></span>

<span data-ttu-id="ba0a9-152">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="ba0a9-152">**Necessity:** Optional</span></span>

<span data-ttu-id="ba0a9-153">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-153">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="ba0a9-154">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="ba0a9-154">**Default value:** `false`</span></span>
