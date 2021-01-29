---
title: Impostazioni del profilo aspetto terminale Windows
description: Informazioni su come personalizzare le impostazioni del profilo aspetto nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 0257f6698e0a497e98b77f4b574560adea00b7e1
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041970"
---
# <a name="appearance-profile-settings-in-windows-terminal"></a><span data-ttu-id="4487e-103">Impostazioni del profilo aspetto nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="4487e-103">Appearance profile settings in Windows Terminal</span></span>

<span data-ttu-id="4487e-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="4487e-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="4487e-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="4487e-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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
> <span data-ttu-id="4487e-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="4487e-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="4487e-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="4487e-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="text"></a><span data-ttu-id="4487e-108">Testo</span><span class="sxs-lookup"><span data-stu-id="4487e-108">Text</span></span>

### <a name="color-scheme"></a><span data-ttu-id="4487e-109">Combinazione colori</span><span class="sxs-lookup"><span data-stu-id="4487e-109">Color scheme</span></span>

<span data-ttu-id="4487e-110">Nome della combinazione colori usata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-110">This is the name of the color scheme used in the profile.</span></span> <span data-ttu-id="4487e-111">Le combinazioni colori sono definite nell'oggetto `schemes`.</span><span class="sxs-lookup"><span data-stu-id="4487e-111">Color schemes are defined in the `schemes` object.</span></span> <span data-ttu-id="4487e-112">Per informazioni più dettagliate, vedi la [pagina Combinazioni colori](./color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="4487e-112">More detailed information can be found on the [Color schemes page](./color-schemes.md).</span></span>

<span data-ttu-id="4487e-113">**Nome della proprietà:** `colorScheme`</span><span class="sxs-lookup"><span data-stu-id="4487e-113">**Property name:** `colorScheme`</span></span>

<span data-ttu-id="4487e-114">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-114">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-115">**Accetta:** nome della combinazione colori in formato stringa</span><span class="sxs-lookup"><span data-stu-id="4487e-115">**Accepts:** Name of color scheme as a string</span></span>

<span data-ttu-id="4487e-116">**Valore predefinito:** `"Campbell"`</span><span class="sxs-lookup"><span data-stu-id="4487e-116">**Default value:** `"Campbell"`</span></span>

### <a name="font-face"></a><span data-ttu-id="4487e-117">Tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="4487e-117">Font face</span></span>

<span data-ttu-id="4487e-118">Nome del tipo di carattere usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-118">This is the name of the font face used in the profile.</span></span> <span data-ttu-id="4487e-119">Il terminale proverà ad eseguire il fallback a Consolas se non riesce a trovarlo o non è valido.</span><span class="sxs-lookup"><span data-stu-id="4487e-119">The terminal will try to fallback to Consolas if this can't be found or is invalid.</span></span> <span data-ttu-id="4487e-120">Per informazioni sulle altre varianti del tipo di carattere predefinito, Cascadia Mono, vedi la [tabella codici di Cascadia](./../cascadia-code.md).</span><span class="sxs-lookup"><span data-stu-id="4487e-120">To learn about the other variants of the default font, Cascadia Mono, visit the [Cascadia Code page](./../cascadia-code.md).</span></span>

<span data-ttu-id="4487e-121">**Nome della proprietà:** `fontFace`</span><span class="sxs-lookup"><span data-stu-id="4487e-121">**Property name:** `fontFace`</span></span>

<span data-ttu-id="4487e-122">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-122">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-123">**Accetta:** nome del tipo di carattere in formato stringa</span><span class="sxs-lookup"><span data-stu-id="4487e-123">**Accepts:** Font name as a string</span></span>

<span data-ttu-id="4487e-124">**Valore predefinito:** `"Cascadia Mono"`</span><span class="sxs-lookup"><span data-stu-id="4487e-124">**Default value:** `"Cascadia Mono"`</span></span>

### <a name="font-size"></a><span data-ttu-id="4487e-125">Dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="4487e-125">Font size</span></span>

<span data-ttu-id="4487e-126">Consente di impostare le dimensioni del carattere del profilo in punti.</span><span class="sxs-lookup"><span data-stu-id="4487e-126">This sets the profile's font size in points.</span></span>

<span data-ttu-id="4487e-127">**Nome della proprietà:** `fontSize`</span><span class="sxs-lookup"><span data-stu-id="4487e-127">**Property name:** `fontSize`</span></span>

<span data-ttu-id="4487e-128">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-128">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-129">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="4487e-129">**Accepts:** Integer</span></span>

<span data-ttu-id="4487e-130">**Valore predefinito:** `12`</span><span class="sxs-lookup"><span data-stu-id="4487e-130">**Default value:** `12`</span></span>

### <a name="font-weight"></a><span data-ttu-id="4487e-131">Peso carattere</span><span class="sxs-lookup"><span data-stu-id="4487e-131">Font weight</span></span>

<span data-ttu-id="4487e-132">Questa proprietà imposta lo spessore (tratti sottili o spessi) per il tipo di carattere del profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-132">This sets the weight (lightness or heaviness of the strokes) for the profile's font.</span></span>

<span data-ttu-id="4487e-133">**Nome della proprietà:** `fontWeight`</span><span class="sxs-lookup"><span data-stu-id="4487e-133">**Property name:** `fontWeight`</span></span>

<span data-ttu-id="4487e-134">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-134">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-135">**Accetta**  `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"` oppure un intero che corrisponde alla rappresentazione numerica dello spesso del tipo di carattere OpenType</span><span class="sxs-lookup"><span data-stu-id="4487e-135">**Accepts:** `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"`, or an integer corresponding to the numeric representation of the OpenType font weight</span></span>

<span data-ttu-id="4487e-136">**Valore predefinito:** `"normal"`</span><span class="sxs-lookup"><span data-stu-id="4487e-136">**Default value:** `"normal"`</span></span>

## <a name="retro-terminal-effects"></a><span data-ttu-id="4487e-137">Effetti per terminale retro</span><span class="sxs-lookup"><span data-stu-id="4487e-137">Retro terminal effects</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="4487e-138">Quando è impostata su `true`, il terminale emulerà un monitor CRT classico con linee di scansione e bordi di testo sfocati.</span><span class="sxs-lookup"><span data-stu-id="4487e-138">When this is set to `true`, the terminal will emulate a classic CRT display with scan lines and blurry text edges.</span></span> <span data-ttu-id="4487e-139">Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="4487e-139">This is an experimental feature and its continued existence is not guaranteed.</span></span>

<span data-ttu-id="4487e-140">Se `experimental.pixelShaderPath` è impostato, eseguirà l'override di questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="4487e-140">If `experimental.pixelShaderPath` is set, it will override this setting.</span></span>

<span data-ttu-id="4487e-141">**Nome della proprietà:** `experimental.retroTerminalEffect`</span><span class="sxs-lookup"><span data-stu-id="4487e-141">**Property name:** `experimental.retroTerminalEffect`</span></span>

<span data-ttu-id="4487e-142">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-142">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-143">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="4487e-143">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="4487e-144">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="4487e-144">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="4487e-145">![Terminale Windows - Effetto sperimentale per terminale retro](./../images/experimental-retro-terminal-effect.gif)
_Configurazione: [Prompt dei comandi retro](./../custom-terminal-gallery/retro-command-prompt.md)_</span><span class="sxs-lookup"><span data-stu-id="4487e-145">![Windows Terminal experimental retro terminal effect](./../images/experimental-retro-terminal-effect.gif)
_Configuration: [Retro Command Prompt](./../custom-terminal-gallery/retro-command-prompt.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="cursor"></a><span data-ttu-id="4487e-146">Cursore</span><span class="sxs-lookup"><span data-stu-id="4487e-146">Cursor</span></span>

### <a name="cursor-shape"></a><span data-ttu-id="4487e-147">Forma del cursore</span><span class="sxs-lookup"><span data-stu-id="4487e-147">Cursor shape</span></span>

<span data-ttu-id="4487e-148">Consente di impostare la forma del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-148">This sets the cursor shape for the profile.</span></span> <span data-ttu-id="4487e-149">I possibili cursori sono i seguenti: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;), `"doubleUnderscore"` (&#x2017;)</span><span class="sxs-lookup"><span data-stu-id="4487e-149">The possible cursors are as follows: `"bar"` ( &#x2503; ), `"vintage"` ( &#x2583; ), `"underscore"` ( &#x2581; ), `"filledBox"` ( &#x2588; ), `"emptyBox"` ( &#x25AF; ), `"doubleUnderscore"` ( &#x2017; )</span></span>

<span data-ttu-id="4487e-150">**Nome della proprietà:** `cursorShape`</span><span class="sxs-lookup"><span data-stu-id="4487e-150">**Property name:** `cursorShape`</span></span>

<span data-ttu-id="4487e-151">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-151">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-152">**Accetta:** `"bar"` , `"vintage"` , `"underscore"` , `"filledBox"` , `"emptyBox"` , `"doubleUnderscore"`</span><span class="sxs-lookup"><span data-stu-id="4487e-152">**Accepts:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`, `"doubleUnderscore"`</span></span>

<span data-ttu-id="4487e-153">**Valore predefinito:** `"bar"`</span><span class="sxs-lookup"><span data-stu-id="4487e-153">**Default value:** `"bar"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4487e-154">La `"doubleUnderscore"` forma del cursore è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="4487e-154">The `"doubleUnderscore"` cursor shape is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="cursor-height"></a><span data-ttu-id="4487e-155">Altezza del cursore</span><span class="sxs-lookup"><span data-stu-id="4487e-155">Cursor height</span></span>

<span data-ttu-id="4487e-156">Consente di impostare l'altezza percentuale del cursore a partire dalla parte inferiore.</span><span class="sxs-lookup"><span data-stu-id="4487e-156">This sets the percentage height of the cursor starting from the bottom.</span></span> <span data-ttu-id="4487e-157">Funziona solo se `cursorShape` è impostata su `"vintage"`.</span><span class="sxs-lookup"><span data-stu-id="4487e-157">This will only work when `cursorShape` is set to `"vintage"`.</span></span>

<span data-ttu-id="4487e-158">**Nome della proprietà:** `cursorHeight`</span><span class="sxs-lookup"><span data-stu-id="4487e-158">**Property name:** `cursorHeight`</span></span>

<span data-ttu-id="4487e-159">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-159">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-160">**Accetta:** intero compreso tra 25-100</span><span class="sxs-lookup"><span data-stu-id="4487e-160">**Accepts:** Integer from 25-100</span></span>

<br />

___

## <a name="background-image"></a><span data-ttu-id="4487e-161">Immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="4487e-161">Background image</span></span>

### <a name="background-image-path"></a><span data-ttu-id="4487e-162">Percorso dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="4487e-162">Background image path</span></span>

<span data-ttu-id="4487e-163">Consente di impostare il percorso del file dell'immagine da tracciare sullo sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="4487e-163">This sets the file location of the image to draw over the window background.</span></span> <span data-ttu-id="4487e-164">L'immagine di sfondo può essere un file con estensione jpg, png o gif.</span><span class="sxs-lookup"><span data-stu-id="4487e-164">The background image can be a .jpg, .png, or .gif file.</span></span> <span data-ttu-id="4487e-165">`"desktopWallpaper"` imposta l'immagine di sfondo sullo sfondo del desktop.</span><span class="sxs-lookup"><span data-stu-id="4487e-165">`"desktopWallpaper"` will set the background image to the desktop's wallpaper.</span></span>

<span data-ttu-id="4487e-166">**Nome della proprietà:** `backgroundImage`</span><span class="sxs-lookup"><span data-stu-id="4487e-166">**Property name:** `backgroundImage`</span></span>

<span data-ttu-id="4487e-167">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-167">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-168">**Accetta:** Percorso del file sotto forma di stringa o `"desktopWallpaper"`</span><span class="sxs-lookup"><span data-stu-id="4487e-168">**Accepts:** File location as a string or `"desktopWallpaper"`</span></span>

### <a name="background-image-stretch-mode"></a><span data-ttu-id="4487e-169">Modalità di estensione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="4487e-169">Background image stretch mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="4487e-170">Consente di impostare la modalità di ridimensionamento dell'immagine di sfondo in modo che occupi tutto lo spazio della finestra.</span><span class="sxs-lookup"><span data-stu-id="4487e-170">This sets how the background image is resized to fill the window.</span></span>

<span data-ttu-id="4487e-171">**Nome della proprietà:** `backgroundImageStretchMode`</span><span class="sxs-lookup"><span data-stu-id="4487e-171">**Property name:** `backgroundImageStretchMode`</span></span>

<span data-ttu-id="4487e-172">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-172">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-173">**Accetta:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="4487e-173">**Accepts:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span></span>

<span data-ttu-id="4487e-174">**Valore predefinito:** `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="4487e-174">**Default value:** `"uniformToFill"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="4487e-175">![Terminale Windows - Modalità di estensione dell'immagine di sfondo](./../images/background-image-stretch-mode.gif)
 _[Origine dell'immagine di sfondo](https://wallpaperhub.app/wallpapers/6287)_</span><span class="sxs-lookup"><span data-stu-id="4487e-175">![Windows Terminal background image stretch mode](./../images/background-image-stretch-mode.gif)
_[Background image source](https://wallpaperhub.app/wallpapers/6287)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a><span data-ttu-id="4487e-176">Allineamento dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="4487e-176">Background image alignment</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="4487e-177">Consente di impostare la modalità di allineamento dell'immagine di sfondo ai bordi della finestra.</span><span class="sxs-lookup"><span data-stu-id="4487e-177">This sets how the background image aligns to the boundaries of the window.</span></span>

<span data-ttu-id="4487e-178">**Nome della proprietà:** `backgroundImageAlignment`</span><span class="sxs-lookup"><span data-stu-id="4487e-178">**Property name:** `backgroundImageAlignment`</span></span>

<span data-ttu-id="4487e-179">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-179">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-180">**Accetta:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span><span class="sxs-lookup"><span data-stu-id="4487e-180">**Accepts:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span></span>

<span data-ttu-id="4487e-181">**Valore predefinito:** `"center"`</span><span class="sxs-lookup"><span data-stu-id="4487e-181">**Default value:** `"center"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="4487e-182">![Terminale Windows - Allineamento dell'immagine di sfondo](./../images/background-image-alignment.gif)
 _[Origine dell'immagine di sfondo](https://design.ubuntu.com/brand/ubuntu-logo/)_</span><span class="sxs-lookup"><span data-stu-id="4487e-182">![Windows Terminal background image alignment](./../images/background-image-alignment.gif)
_[Background image source](https://design.ubuntu.com/brand/ubuntu-logo/)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a><span data-ttu-id="4487e-183">Opacità dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="4487e-183">Background image opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="4487e-184">Consente di impostare la trasparenza dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="4487e-184">This sets the transparency of the background image.</span></span>

:::column-end:::
:::row-end:::

<span data-ttu-id="4487e-185">**Nome della proprietà:** `backgroundImageOpacity`</span><span class="sxs-lookup"><span data-stu-id="4487e-185">**Property name:** `backgroundImageOpacity`</span></span>

<span data-ttu-id="4487e-186">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-186">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-187">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="4487e-187">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="4487e-188">**Valore predefinito:** `1.0`</span><span class="sxs-lookup"><span data-stu-id="4487e-188">**Default value:** `1.0`</span></span>

<br />

___

## <a name="acrylic"></a><span data-ttu-id="4487e-189">Acrilico</span><span class="sxs-lookup"><span data-stu-id="4487e-189">Acrylic</span></span>

### <a name="enable-acrylic"></a><span data-ttu-id="4487e-190">Abilita acrilico</span><span class="sxs-lookup"><span data-stu-id="4487e-190">Enable acrylic</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="4487e-191">Quando è impostata su `true`, la finestra avrà uno sfondo acrilico.</span><span class="sxs-lookup"><span data-stu-id="4487e-191">When this is set to `true`, the window will have an acrylic background.</span></span> <span data-ttu-id="4487e-192">Quando è impostato su `false`, la finestra avrà uno sfondo normale e senza trame.</span><span class="sxs-lookup"><span data-stu-id="4487e-192">When it's set to `false`, the window will have a plain, untextured background.</span></span> <span data-ttu-id="4487e-193">A causa delle limitazioni del sistema operativo, la trasparenza si applica solo alle finestre con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="4487e-193">The transparency only applies to focused windows due to OS limitations.</span></span>

<span data-ttu-id="4487e-194">**Nome della proprietà:** `useAcrylic`</span><span class="sxs-lookup"><span data-stu-id="4487e-194">**Property name:** `useAcrylic`</span></span>

<span data-ttu-id="4487e-195">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-195">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-196">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="4487e-196">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="4487e-197">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="4487e-197">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Acrilico](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a><span data-ttu-id="4487e-199">Opacità acrilico</span><span class="sxs-lookup"><span data-stu-id="4487e-199">Acrylic opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="4487e-200">Quando `useAcrylic` è impostata su `true`, imposta la trasparenza della finestra per il profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-200">When `useAcrylic` is set to `true`, this sets the transparency of the window for the profile.</span></span> <span data-ttu-id="4487e-201">Accetta valori a virgola mobile compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="4487e-201">This accepts floating point values from 0-1.</span></span>

<span data-ttu-id="4487e-202">**Nome della proprietà:** `acrylicOpacity`</span><span class="sxs-lookup"><span data-stu-id="4487e-202">**Property name:** `acrylicOpacity`</span></span>

<span data-ttu-id="4487e-203">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-203">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-204">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="4487e-204">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="4487e-205">**Valore predefinito:** `0.5`</span><span class="sxs-lookup"><span data-stu-id="4487e-205">**Default value:** `0.5`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Opacità acrilico](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="window"></a><span data-ttu-id="4487e-207">Finestra</span><span class="sxs-lookup"><span data-stu-id="4487e-207">Window</span></span>

### <a name="padding"></a><span data-ttu-id="4487e-208">Spaziatura interna</span><span class="sxs-lookup"><span data-stu-id="4487e-208">Padding</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="4487e-209">Consente di impostare la spaziatura intorno al testo all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="4487e-209">This sets the padding around the text within the window.</span></span> <span data-ttu-id="4487e-210">Questo accetta tre formati diversi: `"#"` e imposta `#` la stessa spaziatura interna per tutti i lati, `"#, #"` imposta la stessa spaziatura interna per Left-Right e top-bottom e `"#, #, #, #"` imposta la spaziatura interna singolarmente per left, top, Right e Bottom.</span><span class="sxs-lookup"><span data-stu-id="4487e-210">This will accept three different formats: `"#"` and `#` set the same padding for all sides, `"#, #"` sets the same padding for left-right and top-bottom, and `"#, #, #, #"` sets the padding individually for left, top, right, and bottom.</span></span>

<span data-ttu-id="4487e-211">**Nome della proprietà:** `padding`</span><span class="sxs-lookup"><span data-stu-id="4487e-211">**Property name:** `padding`</span></span>

<span data-ttu-id="4487e-212">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-212">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-213">**Accetta:** Valori come stringa nei formati seguenti: `"#"` , `"#, #"` `"#, #, #, #"` o valore come Integer: `#`</span><span class="sxs-lookup"><span data-stu-id="4487e-213">**Accepts:** Values as a string in the following formats: `"#"`, `"#, #"`, `"#, #, #, #"` or value as an integer: `#`</span></span>

<span data-ttu-id="4487e-214">**Valore predefinito:** `"8, 8, 8, 8"`</span><span class="sxs-lookup"><span data-stu-id="4487e-214">**Default value:** `"8, 8, 8, 8"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Spaziatura interna](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="scrollbar-visibility"></a><span data-ttu-id="4487e-216">Visibilità della barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="4487e-216">Scrollbar visibility</span></span>

<span data-ttu-id="4487e-217">Consente di impostare la visibilità della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="4487e-217">This sets the visibility of the scrollbar.</span></span>

<span data-ttu-id="4487e-218">**Nome della proprietà:** `scrollbarState`</span><span class="sxs-lookup"><span data-stu-id="4487e-218">**Property name:** `scrollbarState`</span></span>

<span data-ttu-id="4487e-219">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-219">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-220">**Accetta:** `"visible"`, `"hidden"`</span><span class="sxs-lookup"><span data-stu-id="4487e-220">**Accepts:** `"visible"`, `"hidden"`</span></span>

<br />

___

## <a name="color-settings"></a><span data-ttu-id="4487e-221">Impostazioni per il colore</span><span class="sxs-lookup"><span data-stu-id="4487e-221">Color settings</span></span>

### <a name="tab-color"></a><span data-ttu-id="4487e-222">Colore delle schede</span><span class="sxs-lookup"><span data-stu-id="4487e-222">Tab color</span></span>

<span data-ttu-id="4487e-223">Viene impostato il colore della scheda del profilo. Se si utilizza la selezione colori scheda, questo colore verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="4487e-223">This sets the color of the profile's tab. Using the tab color picker will override this color.</span></span>

<span data-ttu-id="4487e-224">**Nome della proprietà:** `tabColor`</span><span class="sxs-lookup"><span data-stu-id="4487e-224">**Property name:** `tabColor`</span></span>

<span data-ttu-id="4487e-225">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-225">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-226">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="4487e-226">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="foreground-color"></a><span data-ttu-id="4487e-227">Colore primo piano</span><span class="sxs-lookup"><span data-stu-id="4487e-227">Foreground color</span></span>

<span data-ttu-id="4487e-228">Modifica il colore primo piano del profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-228">This changes the foreground color of the profile.</span></span> <span data-ttu-id="4487e-229">Sostituisce il valore di `foreground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="4487e-229">This overrides `foreground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="4487e-230">**Nome della proprietà:** `foreground`</span><span class="sxs-lookup"><span data-stu-id="4487e-230">**Property name:** `foreground`</span></span>

<span data-ttu-id="4487e-231">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-231">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-232">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="4487e-232">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="background-color"></a><span data-ttu-id="4487e-233">Colore di sfondo</span><span class="sxs-lookup"><span data-stu-id="4487e-233">Background color</span></span>

<span data-ttu-id="4487e-234">Modifica il colore di sfondo del profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-234">This changes the background color of the profile with this setting.</span></span> <span data-ttu-id="4487e-235">Sostituisce il valore di `background` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="4487e-235">This overrides `background` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="4487e-236">**Nome della proprietà:** `background`</span><span class="sxs-lookup"><span data-stu-id="4487e-236">**Property name:** `background`</span></span>

<span data-ttu-id="4487e-237">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-237">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-238">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="4487e-238">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="selection-background-color"></a><span data-ttu-id="4487e-239">Colore di sfondo della selezione</span><span class="sxs-lookup"><span data-stu-id="4487e-239">Selection background color</span></span>

<span data-ttu-id="4487e-240">Consente di impostare il colore di sfondo di una selezione nel profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-240">This sets the background color of a selection within the profile.</span></span> <span data-ttu-id="4487e-241">Sostituisce il valore di `selectionBackground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="4487e-241">This will override the `selectionBackground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="4487e-242">**Nome della proprietà:** `selectionBackground`</span><span class="sxs-lookup"><span data-stu-id="4487e-242">**Property name:** `selectionBackground`</span></span>

<span data-ttu-id="4487e-243">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-243">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-244">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="4487e-244">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="cursor-color"></a><span data-ttu-id="4487e-245">Colore del cursore</span><span class="sxs-lookup"><span data-stu-id="4487e-245">Cursor color</span></span>

<span data-ttu-id="4487e-246">Consente di impostare il colore del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="4487e-246">This sets the cursor color of the profile.</span></span> <span data-ttu-id="4487e-247">Sostituisce il valore di `cursorColor` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="4487e-247">This will override the `cursorColor` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="4487e-248">**Nome della proprietà:** `cursorColor`</span><span class="sxs-lookup"><span data-stu-id="4487e-248">**Property name:** `cursorColor`</span></span>

<span data-ttu-id="4487e-249">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-249">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-250">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="4487e-250">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

<br />

___

## <a name="pixel-shader-effects-preview"></a><span data-ttu-id="4487e-251">Effetti pixel shader ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="4487e-251">Pixel shader effects ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="4487e-252">Questa impostazione consente a un utente di specificare il percorso di un pixel shader personalizzato da usare con il contenuto del terminale.</span><span class="sxs-lookup"><span data-stu-id="4487e-252">This setting allows a user to specify the path to a custom pixel shader to use with the terminal content.</span></span> <span data-ttu-id="4487e-253">Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="4487e-253">This is an experimental feature and its continued existence is not guaranteed.</span></span> <span data-ttu-id="4487e-254">Per altri dettagli sulla creazione di pixel shader personalizzati per il terminale, vedere [questa documentazione](https://github.com/microsoft/terminal/blob/main/samples/PixelShaders/README.md).</span><span class="sxs-lookup"><span data-stu-id="4487e-254">For more details on authoring custom pixel shaders for the terminal, see [this documentation](https://github.com/microsoft/terminal/blob/main/samples/PixelShaders/README.md).</span></span>

<span data-ttu-id="4487e-255">Se impostato, l'impostazione verrà sostituita `experimental.retroTerminalEffect` .</span><span class="sxs-lookup"><span data-stu-id="4487e-255">If set, this will override the `experimental.retroTerminalEffect` setting.</span></span>

<span data-ttu-id="4487e-256">**Nome della proprietà:** `experimental.pixelShaderPath`</span><span class="sxs-lookup"><span data-stu-id="4487e-256">**Property name:** `experimental.pixelShaderPath`</span></span>

<span data-ttu-id="4487e-257">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="4487e-257">**Necessity:** Optional</span></span>

<span data-ttu-id="4487e-258">**Accetta:** Percorso di un `.hlsl` file shader sotto forma di stringa</span><span class="sxs-lookup"><span data-stu-id="4487e-258">**Accepts:** A path to an `.hlsl` shader file, as a string</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4487e-259">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="4487e-259">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>
