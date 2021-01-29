---
title: Impostazioni del profilo avanzato di Windows Terminal
description: Informazioni su come personalizzare le impostazioni avanzate del profilo nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 0019a96f80e73740d980c9c6e156cf50134f0945
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041971"
---
# <a name="advanced-profile-settings-in-windows-terminal"></a><span data-ttu-id="c120b-103">Impostazioni avanzate del profilo nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="c120b-103">Advanced profile settings in Windows Terminal</span></span>

<span data-ttu-id="c120b-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="c120b-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="c120b-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="c120b-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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
> <span data-ttu-id="c120b-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="c120b-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="c120b-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="c120b-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="suppress-title-changes"></a><span data-ttu-id="c120b-108">Non visualizzare modifiche al titolo</span><span class="sxs-lookup"><span data-stu-id="c120b-108">Suppress title changes</span></span>

<span data-ttu-id="c120b-109">Quando è impostata su `true`, `tabTitle` sostituisce il titolo predefinito della scheda. Tutti i messaggi di modifica del titolo dall'applicazione verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="c120b-109">When this is set to `true`, `tabTitle` overrides the default title of the tab and any title change messages from the application will be suppressed.</span></span> <span data-ttu-id="c120b-110">Se `tabTitle` non è impostata, verrà usata `name`.</span><span class="sxs-lookup"><span data-stu-id="c120b-110">If `tabTitle` isn't set, `name` will be used instead.</span></span> <span data-ttu-id="c120b-111">Quando è impostata su `false`, `tabTitle` si comporta normalmente.</span><span class="sxs-lookup"><span data-stu-id="c120b-111">When this is set to `false`, `tabTitle` behaves as normal.</span></span>

<span data-ttu-id="c120b-112">**Nome della proprietà:** `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="c120b-112">**Property name:** `suppressApplicationTitle`</span></span>

<span data-ttu-id="c120b-113">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-113">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-114">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c120b-114">**Accepts:** `true`, `false`</span></span>

<br />

___

## <a name="text-antialiasing"></a><span data-ttu-id="c120b-115">Anti-aliasing del testo</span><span class="sxs-lookup"><span data-stu-id="c120b-115">Text antialiasing</span></span>

<span data-ttu-id="c120b-116">Controlla la modalità di anti-aliasing del testo nel renderer.</span><span class="sxs-lookup"><span data-stu-id="c120b-116">This controls how text is antialiased in the renderer.</span></span> <span data-ttu-id="c120b-117">La modifica di questa impostazione richiede l'avvio di una nuova istanza del terminale.</span><span class="sxs-lookup"><span data-stu-id="c120b-117">Note that changing this setting will require starting a new terminal instance.</span></span>

![Terminale Windows - Anti-aliasing del testo](./../images/antialiasing-mode.gif)

<span data-ttu-id="c120b-119">**Nome della proprietà:** `antialiasingMode`</span><span class="sxs-lookup"><span data-stu-id="c120b-119">**Property name:** `antialiasingMode`</span></span>

<span data-ttu-id="c120b-120">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-120">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-121">**Accetta:** `"grayscale"`, `"cleartype"`, `"aliased"`</span><span class="sxs-lookup"><span data-stu-id="c120b-121">**Accepts:** `"grayscale"`, `"cleartype"`, `"aliased"`</span></span>

<span data-ttu-id="c120b-122">**Valore predefinito:** `"grayscale"`</span><span class="sxs-lookup"><span data-stu-id="c120b-122">**Default value:** `"grayscale"`</span></span>

<br />

___

## <a name="altgr-aliasing"></a><span data-ttu-id="c120b-123">Aliasing AltGr</span><span class="sxs-lookup"><span data-stu-id="c120b-123">AltGr aliasing</span></span>

<span data-ttu-id="c120b-124">Questa proprietà consente di controllare se Terminale Windows considererà <kbd>CTRL+ALT</kbd> come alias di <kbd>ALTGR</kbd>.</span><span class="sxs-lookup"><span data-stu-id="c120b-124">This allows you to control if Windows Terminal will treat <kbd>ctrl+alt</kbd> as an alias for <kbd>AltGr</kbd>.</span></span>

<span data-ttu-id="c120b-125">**Nome della proprietà:** `altGrAliasing`</span><span class="sxs-lookup"><span data-stu-id="c120b-125">**Property name:** `altGrAliasing`</span></span>

<span data-ttu-id="c120b-126">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-126">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-127">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c120b-127">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c120b-128">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="c120b-128">**Default value:** `true`</span></span>

<br />

___

## <a name="scroll-to-input-when-typing"></a><span data-ttu-id="c120b-129">Scorri fino all'input durante la digitazione</span><span class="sxs-lookup"><span data-stu-id="c120b-129">Scroll to input when typing</span></span>

<span data-ttu-id="c120b-130">Quando è impostata su `true`, la finestra scorre fino alla riga di input del comando durante la digitazione.</span><span class="sxs-lookup"><span data-stu-id="c120b-130">When this is set to `true`, the window will scroll to the command input line when typing.</span></span> <span data-ttu-id="c120b-131">Quando è impostata su `false`, lo scorrimento della finestra non è attivato quando inizi a digitare.</span><span class="sxs-lookup"><span data-stu-id="c120b-131">When it's set to `false`, the window will not scroll when you start typing.</span></span>

<span data-ttu-id="c120b-132">**Nome della proprietà:** `snapOnInput`</span><span class="sxs-lookup"><span data-stu-id="c120b-132">**Property name:** `snapOnInput`</span></span>

<span data-ttu-id="c120b-133">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-133">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-134">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c120b-134">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="c120b-135">**Valore predefinito:** `true`</span><span class="sxs-lookup"><span data-stu-id="c120b-135">**Default value:** `true`</span></span>

<br />

___

## <a name="history-size"></a><span data-ttu-id="c120b-136">Dimensioni della cronologia</span><span class="sxs-lookup"><span data-stu-id="c120b-136">History size</span></span>

<span data-ttu-id="c120b-137">Consente di impostare il numero di righe a cui è possibile passare scorrendo che precedono quelle visualizzate nella finestra.</span><span class="sxs-lookup"><span data-stu-id="c120b-137">This sets the number of lines above the ones displayed in the window you can scroll back to.</span></span>

<span data-ttu-id="c120b-138">**Nome della proprietà:** `historySize`</span><span class="sxs-lookup"><span data-stu-id="c120b-138">**Property name:** `historySize`</span></span>

<span data-ttu-id="c120b-139">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-139">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-140">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="c120b-140">**Accepts:** Integer</span></span>

<span data-ttu-id="c120b-141">**Valore predefinito:** `9001`</span><span class="sxs-lookup"><span data-stu-id="c120b-141">**Default value:** `9001`</span></span>

<br />

___

## <a name="profile-termination-behavior"></a><span data-ttu-id="c120b-142">Comportamento di terminazione del profilo</span><span class="sxs-lookup"><span data-stu-id="c120b-142">Profile termination behavior</span></span>

<span data-ttu-id="c120b-143">Consente di impostare la reazione del profilo alla chiusura o a un errore all'avvio.</span><span class="sxs-lookup"><span data-stu-id="c120b-143">This sets how the profile reacts to termination or failure to launch.</span></span> <span data-ttu-id="c120b-144">Con `"graceful"`, il profilo verrà chiuso quando viene digitato `exit` o quando il processo viene chiuso normalmente.</span><span class="sxs-lookup"><span data-stu-id="c120b-144">`"graceful"` will close the profile when `exit` is typed or when the process exits normally.</span></span> <span data-ttu-id="c120b-145">Con `"always"` il profilo verrà sempre chiuso, mentre con `"never"` non verrà mai chiuso.</span><span class="sxs-lookup"><span data-stu-id="c120b-145">`"always"` will always close the profile and `"never"` will never close the profile.</span></span> <span data-ttu-id="c120b-146">`true` e `false` vengono accettati come sinonimi rispettivamente per `"graceful"` e `"never"`.</span><span class="sxs-lookup"><span data-stu-id="c120b-146">`true` and `false` are accepted as synonyms for `"graceful"` and `"never"`, respectively.</span></span>

<span data-ttu-id="c120b-147">**Nome della proprietà:** `closeOnExit`</span><span class="sxs-lookup"><span data-stu-id="c120b-147">**Property name:** `closeOnExit`</span></span>

<span data-ttu-id="c120b-148">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-148">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-149">**Accetta:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="c120b-149">**Accepts:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span></span>

<span data-ttu-id="c120b-150">**Valore predefinito:** `"graceful"`</span><span class="sxs-lookup"><span data-stu-id="c120b-150">**Default value:** `"graceful"`</span></span>

<br />

___

## <a name="bell-notification-style"></a><span data-ttu-id="c120b-151">Stile notifica campanello</span><span class="sxs-lookup"><span data-stu-id="c120b-151">Bell notification style</span></span>

<span data-ttu-id="c120b-152">Controlla cosa accade quando l'applicazione emette un carattere BEL.</span><span class="sxs-lookup"><span data-stu-id="c120b-152">Controls what happens when the application emits a BEL character.</span></span> <span data-ttu-id="c120b-153">Quando è impostato su `"all"` , il terminale riprodurrà un suono e lampeggerà l'icona della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c120b-153">When set to `"all"`, the terminal will play a sound and flash the taskbar icon.</span></span>

<span data-ttu-id="c120b-154">**Nome della proprietà:** `bellStyle`</span><span class="sxs-lookup"><span data-stu-id="c120b-154">**Property name:** `bellStyle`</span></span>

<span data-ttu-id="c120b-155">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-155">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-156">**Accetta:** `"all"`, `"audible"`, `"visual"`, `"none"`</span><span class="sxs-lookup"><span data-stu-id="c120b-156">**Accepts:** `"all"`, `"audible"`, `"visual"`, `"none"`</span></span>

<span data-ttu-id="c120b-157">**Valore predefinito:** `"audible"`</span><span class="sxs-lookup"><span data-stu-id="c120b-157">**Default value:** `"audible"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c120b-158">Gli `"all"` `"visual"` stili di notifica e Bell sono disponibili solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="c120b-158">The `"all"` and `"visual"` bell notification styles are only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

<br />

___

## <a name="unique-identifier"></a><span data-ttu-id="c120b-159">Identificatore univoco</span><span class="sxs-lookup"><span data-stu-id="c120b-159">Unique identifier</span></span>

<span data-ttu-id="c120b-160">I profili possono usare un GUID come identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="c120b-160">Profiles can use a GUID as a unique identifier.</span></span> <span data-ttu-id="c120b-161">Per impostare un profilo come predefinito, è necessario un GUID per l'impostazione globale `defaultProfile`.</span><span class="sxs-lookup"><span data-stu-id="c120b-161">To make a profile your default profile, it needs a GUID for the `defaultProfile` global setting.</span></span>

<span data-ttu-id="c120b-162">**Nome della proprietà:** `guid`</span><span class="sxs-lookup"><span data-stu-id="c120b-162">**Property name:** `guid`</span></span>

<span data-ttu-id="c120b-163">**Obbligatoria:** Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="c120b-163">**Necessity:** Required</span></span>

<span data-ttu-id="c120b-164">**Accetta:** GUID in formato stringa del Registro di sistema: `"{00000000-0000-0000-0000-000000000000}"`</span><span class="sxs-lookup"><span data-stu-id="c120b-164">**Accepts:** GUID as a string in registry format: `"{00000000-0000-0000-0000-000000000000}"`</span></span>

<br />

___

## <a name="source"></a><span data-ttu-id="c120b-165">Origine</span><span class="sxs-lookup"><span data-stu-id="c120b-165">Source</span></span>

<span data-ttu-id="c120b-166">Archivia il nome del generatore di profili che ha originato il profilo.</span><span class="sxs-lookup"><span data-stu-id="c120b-166">This stores the name of the profile generator that originated the profile.</span></span> <span data-ttu-id="c120b-167">_Non esistono valori individuabili per questo campo._</span><span class="sxs-lookup"><span data-stu-id="c120b-167">_There are no discoverable values for this field._</span></span> <span data-ttu-id="c120b-168">Per altre informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c120b-168">For additional information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="c120b-169">**Nome della proprietà:** `source`</span><span class="sxs-lookup"><span data-stu-id="c120b-169">**Property name:** `source`</span></span>

<span data-ttu-id="c120b-170">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="c120b-170">**Necessity:** Optional</span></span>

<span data-ttu-id="c120b-171">**Accetta:** String</span><span class="sxs-lookup"><span data-stu-id="c120b-171">**Accepts:** String</span></span>

> [!NOTE]
> <span data-ttu-id="c120b-172">Questo campo deve essere omesso quando si dichiara un profilo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c120b-172">This field should be omitted when declaring a custom profile.</span></span> <span data-ttu-id="c120b-173">Viene usato dal terminale per connettere i profili generati automaticamente al file di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="c120b-173">It is used by Terminal to connect automatically generated profiles to your settings file.</span></span>
