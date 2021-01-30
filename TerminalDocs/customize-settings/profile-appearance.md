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
# <a name="appearance-profile-settings-in-windows-terminal"></a><span data-ttu-id="71981-103">Impostazioni del profilo aspetto nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="71981-103">Appearance profile settings in Windows Terminal</span></span>

<span data-ttu-id="71981-104">Le impostazioni elencate di seguito sono specifiche dei singoli profili univoci.</span><span class="sxs-lookup"><span data-stu-id="71981-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="71981-105">Se vuoi applicare un'impostazione a tutti i profili, puoi aggiungerla alla sezione `defaults` prima dell'elenco dei profili nel file settings.json.</span><span class="sxs-lookup"><span data-stu-id="71981-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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
> <span data-ttu-id="71981-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="71981-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="71981-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="71981-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="text"></a><span data-ttu-id="71981-108">Testo</span><span class="sxs-lookup"><span data-stu-id="71981-108">Text</span></span>

### <a name="color-scheme"></a><span data-ttu-id="71981-109">Combinazione colori</span><span class="sxs-lookup"><span data-stu-id="71981-109">Color scheme</span></span>

<span data-ttu-id="71981-110">Nome della combinazione colori usata nel profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-110">This is the name of the color scheme used in the profile.</span></span> <span data-ttu-id="71981-111">Le combinazioni colori sono definite nell'oggetto `schemes`.</span><span class="sxs-lookup"><span data-stu-id="71981-111">Color schemes are defined in the `schemes` object.</span></span> <span data-ttu-id="71981-112">Per informazioni più dettagliate, vedi la [pagina Combinazioni colori](./color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="71981-112">More detailed information can be found on the [Color schemes page](./color-schemes.md).</span></span>

<span data-ttu-id="71981-113">**Nome della proprietà:** `colorScheme`</span><span class="sxs-lookup"><span data-stu-id="71981-113">**Property name:** `colorScheme`</span></span>

<span data-ttu-id="71981-114">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-114">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-115">**Accetta:** nome della combinazione colori in formato stringa</span><span class="sxs-lookup"><span data-stu-id="71981-115">**Accepts:** Name of color scheme as a string</span></span>

<span data-ttu-id="71981-116">**Valore predefinito:** `"Campbell"`</span><span class="sxs-lookup"><span data-stu-id="71981-116">**Default value:** `"Campbell"`</span></span>

### <a name="font-face"></a><span data-ttu-id="71981-117">Tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="71981-117">Font face</span></span>

<span data-ttu-id="71981-118">Nome del tipo di carattere usato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-118">This is the name of the font face used in the profile.</span></span> <span data-ttu-id="71981-119">Il terminale proverà ad eseguire il fallback a Consolas se non riesce a trovarlo o non è valido.</span><span class="sxs-lookup"><span data-stu-id="71981-119">The terminal will try to fallback to Consolas if this can't be found or is invalid.</span></span> <span data-ttu-id="71981-120">Per informazioni sulle altre varianti del tipo di carattere predefinito, Cascadia Mono, vedi la [tabella codici di Cascadia](./../cascadia-code.md).</span><span class="sxs-lookup"><span data-stu-id="71981-120">To learn about the other variants of the default font, Cascadia Mono, visit the [Cascadia Code page](./../cascadia-code.md).</span></span>

<span data-ttu-id="71981-121">**Nome della proprietà:** `fontFace`</span><span class="sxs-lookup"><span data-stu-id="71981-121">**Property name:** `fontFace`</span></span>

<span data-ttu-id="71981-122">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-122">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-123">**Accetta:** nome del tipo di carattere in formato stringa</span><span class="sxs-lookup"><span data-stu-id="71981-123">**Accepts:** Font name as a string</span></span>

<span data-ttu-id="71981-124">**Valore predefinito:** `"Cascadia Mono"`</span><span class="sxs-lookup"><span data-stu-id="71981-124">**Default value:** `"Cascadia Mono"`</span></span>

### <a name="font-size"></a><span data-ttu-id="71981-125">Dimensioni del carattere</span><span class="sxs-lookup"><span data-stu-id="71981-125">Font size</span></span>

<span data-ttu-id="71981-126">Consente di impostare le dimensioni del carattere del profilo in punti.</span><span class="sxs-lookup"><span data-stu-id="71981-126">This sets the profile's font size in points.</span></span>

<span data-ttu-id="71981-127">**Nome della proprietà:** `fontSize`</span><span class="sxs-lookup"><span data-stu-id="71981-127">**Property name:** `fontSize`</span></span>

<span data-ttu-id="71981-128">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-128">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-129">**Accetta:** Intero</span><span class="sxs-lookup"><span data-stu-id="71981-129">**Accepts:** Integer</span></span>

<span data-ttu-id="71981-130">**Valore predefinito:** `12`</span><span class="sxs-lookup"><span data-stu-id="71981-130">**Default value:** `12`</span></span>

### <a name="font-weight"></a><span data-ttu-id="71981-131">Peso carattere</span><span class="sxs-lookup"><span data-stu-id="71981-131">Font weight</span></span>

<span data-ttu-id="71981-132">Questa proprietà imposta lo spessore (tratti sottili o spessi) per il tipo di carattere del profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-132">This sets the weight (lightness or heaviness of the strokes) for the profile's font.</span></span>

<span data-ttu-id="71981-133">**Nome della proprietà:** `fontWeight`</span><span class="sxs-lookup"><span data-stu-id="71981-133">**Property name:** `fontWeight`</span></span>

<span data-ttu-id="71981-134">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-134">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-135">**Accetta**  `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"` oppure un intero che corrisponde alla rappresentazione numerica dello spesso del tipo di carattere OpenType</span><span class="sxs-lookup"><span data-stu-id="71981-135">**Accepts:** `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"`, or an integer corresponding to the numeric representation of the OpenType font weight</span></span>

<span data-ttu-id="71981-136">**Valore predefinito:** `"normal"`</span><span class="sxs-lookup"><span data-stu-id="71981-136">**Default value:** `"normal"`</span></span>

## <a name="retro-terminal-effects"></a><span data-ttu-id="71981-137">Effetti per terminale retro</span><span class="sxs-lookup"><span data-stu-id="71981-137">Retro terminal effects</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="71981-138">Quando è impostata su `true`, il terminale emulerà un monitor CRT classico con linee di scansione e bordi di testo sfocati.</span><span class="sxs-lookup"><span data-stu-id="71981-138">When this is set to `true`, the terminal will emulate a classic CRT display with scan lines and blurry text edges.</span></span> <span data-ttu-id="71981-139">Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="71981-139">This is an experimental feature and its continued existence is not guaranteed.</span></span>

<span data-ttu-id="71981-140">Se `experimental.pixelShaderPath` è impostato, eseguirà l'override di questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="71981-140">If `experimental.pixelShaderPath` is set, it will override this setting.</span></span>

<span data-ttu-id="71981-141">**Nome della proprietà:** `experimental.retroTerminalEffect`</span><span class="sxs-lookup"><span data-stu-id="71981-141">**Property name:** `experimental.retroTerminalEffect`</span></span>

<span data-ttu-id="71981-142">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-142">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-143">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="71981-143">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="71981-144">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="71981-144">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="71981-145">![Terminale Windows - Effetto sperimentale per terminale retro](./../images/experimental-retro-terminal-effect.gif)
_Configurazione: [Prompt dei comandi retro](./../custom-terminal-gallery/retro-command-prompt.md)_</span><span class="sxs-lookup"><span data-stu-id="71981-145">![Windows Terminal experimental retro terminal effect](./../images/experimental-retro-terminal-effect.gif)
_Configuration: [Retro Command Prompt](./../custom-terminal-gallery/retro-command-prompt.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="cursor"></a><span data-ttu-id="71981-146">Cursore</span><span class="sxs-lookup"><span data-stu-id="71981-146">Cursor</span></span>

### <a name="cursor-shape"></a><span data-ttu-id="71981-147">Forma del cursore</span><span class="sxs-lookup"><span data-stu-id="71981-147">Cursor shape</span></span>

<span data-ttu-id="71981-148">Consente di impostare la forma del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-148">This sets the cursor shape for the profile.</span></span> <span data-ttu-id="71981-149">I possibili cursori sono i seguenti: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;), `"doubleUnderscore"` (&#x2017;)</span><span class="sxs-lookup"><span data-stu-id="71981-149">The possible cursors are as follows: `"bar"` ( &#x2503; ), `"vintage"` ( &#x2583; ), `"underscore"` ( &#x2581; ), `"filledBox"` ( &#x2588; ), `"emptyBox"` ( &#x25AF; ), `"doubleUnderscore"` ( &#x2017; )</span></span>

<span data-ttu-id="71981-150">**Nome della proprietà:** `cursorShape`</span><span class="sxs-lookup"><span data-stu-id="71981-150">**Property name:** `cursorShape`</span></span>

<span data-ttu-id="71981-151">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-151">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-152">**Accetta:** `"bar"` , `"vintage"` , `"underscore"` , `"filledBox"` , `"emptyBox"` , `"doubleUnderscore"`</span><span class="sxs-lookup"><span data-stu-id="71981-152">**Accepts:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`, `"doubleUnderscore"`</span></span>

<span data-ttu-id="71981-153">**Valore predefinito:** `"bar"`</span><span class="sxs-lookup"><span data-stu-id="71981-153">**Default value:** `"bar"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71981-154">La `"doubleUnderscore"` forma del cursore è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="71981-154">The `"doubleUnderscore"` cursor shape is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

### <a name="cursor-height"></a><span data-ttu-id="71981-155">Altezza del cursore</span><span class="sxs-lookup"><span data-stu-id="71981-155">Cursor height</span></span>

<span data-ttu-id="71981-156">Consente di impostare l'altezza percentuale del cursore a partire dalla parte inferiore.</span><span class="sxs-lookup"><span data-stu-id="71981-156">This sets the percentage height of the cursor starting from the bottom.</span></span> <span data-ttu-id="71981-157">Funziona solo se `cursorShape` è impostata su `"vintage"`.</span><span class="sxs-lookup"><span data-stu-id="71981-157">This will only work when `cursorShape` is set to `"vintage"`.</span></span>

<span data-ttu-id="71981-158">**Nome della proprietà:** `cursorHeight`</span><span class="sxs-lookup"><span data-stu-id="71981-158">**Property name:** `cursorHeight`</span></span>

<span data-ttu-id="71981-159">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-159">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-160">**Accetta:** intero compreso tra 25-100</span><span class="sxs-lookup"><span data-stu-id="71981-160">**Accepts:** Integer from 25-100</span></span>

<br />

___

## <a name="background-image"></a><span data-ttu-id="71981-161">Immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="71981-161">Background image</span></span>

### <a name="background-image-path"></a><span data-ttu-id="71981-162">Percorso dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="71981-162">Background image path</span></span>

<span data-ttu-id="71981-163">Consente di impostare il percorso del file dell'immagine da tracciare sullo sfondo della finestra.</span><span class="sxs-lookup"><span data-stu-id="71981-163">This sets the file location of the image to draw over the window background.</span></span> <span data-ttu-id="71981-164">L'immagine di sfondo può essere un file con estensione jpg, png o gif.</span><span class="sxs-lookup"><span data-stu-id="71981-164">The background image can be a .jpg, .png, or .gif file.</span></span> <span data-ttu-id="71981-165">`"desktopWallpaper"` imposta l'immagine di sfondo sullo sfondo del desktop.</span><span class="sxs-lookup"><span data-stu-id="71981-165">`"desktopWallpaper"` will set the background image to the desktop's wallpaper.</span></span>

<span data-ttu-id="71981-166">**Nome della proprietà:** `backgroundImage`</span><span class="sxs-lookup"><span data-stu-id="71981-166">**Property name:** `backgroundImage`</span></span>

<span data-ttu-id="71981-167">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-167">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-168">**Accetta:** Percorso del file sotto forma di stringa o `"desktopWallpaper"`</span><span class="sxs-lookup"><span data-stu-id="71981-168">**Accepts:** File location as a string or `"desktopWallpaper"`</span></span>

### <a name="background-image-stretch-mode"></a><span data-ttu-id="71981-169">Modalità di estensione dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="71981-169">Background image stretch mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="71981-170">Consente di impostare la modalità di ridimensionamento dell'immagine di sfondo in modo che occupi tutto lo spazio della finestra.</span><span class="sxs-lookup"><span data-stu-id="71981-170">This sets how the background image is resized to fill the window.</span></span>

<span data-ttu-id="71981-171">**Nome della proprietà:** `backgroundImageStretchMode`</span><span class="sxs-lookup"><span data-stu-id="71981-171">**Property name:** `backgroundImageStretchMode`</span></span>

<span data-ttu-id="71981-172">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-172">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-173">**Accetta:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="71981-173">**Accepts:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span></span>

<span data-ttu-id="71981-174">**Valore predefinito:** `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="71981-174">**Default value:** `"uniformToFill"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="71981-175">![Terminale Windows - Modalità di estensione dell'immagine di sfondo](./../images/background-image-stretch-mode.gif)
 _[Origine dell'immagine di sfondo](https://wallpaperhub.app/wallpapers/6287)_</span><span class="sxs-lookup"><span data-stu-id="71981-175">![Windows Terminal background image stretch mode](./../images/background-image-stretch-mode.gif)
_[Background image source](https://wallpaperhub.app/wallpapers/6287)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a><span data-ttu-id="71981-176">Allineamento dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="71981-176">Background image alignment</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="71981-177">Consente di impostare la modalità di allineamento dell'immagine di sfondo ai bordi della finestra.</span><span class="sxs-lookup"><span data-stu-id="71981-177">This sets how the background image aligns to the boundaries of the window.</span></span>

<span data-ttu-id="71981-178">**Nome della proprietà:** `backgroundImageAlignment`</span><span class="sxs-lookup"><span data-stu-id="71981-178">**Property name:** `backgroundImageAlignment`</span></span>

<span data-ttu-id="71981-179">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-179">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-180">**Accetta:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span><span class="sxs-lookup"><span data-stu-id="71981-180">**Accepts:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span></span>

<span data-ttu-id="71981-181">**Valore predefinito:** `"center"`</span><span class="sxs-lookup"><span data-stu-id="71981-181">**Default value:** `"center"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="71981-182">![Terminale Windows - Allineamento dell'immagine di sfondo](./../images/background-image-alignment.gif)
 _[Origine dell'immagine di sfondo](https://design.ubuntu.com/brand/ubuntu-logo/)_</span><span class="sxs-lookup"><span data-stu-id="71981-182">![Windows Terminal background image alignment](./../images/background-image-alignment.gif)
_[Background image source](https://design.ubuntu.com/brand/ubuntu-logo/)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a><span data-ttu-id="71981-183">Opacità dell'immagine di sfondo</span><span class="sxs-lookup"><span data-stu-id="71981-183">Background image opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="71981-184">Consente di impostare la trasparenza dell'immagine di sfondo.</span><span class="sxs-lookup"><span data-stu-id="71981-184">This sets the transparency of the background image.</span></span>

:::column-end:::
:::row-end:::

<span data-ttu-id="71981-185">**Nome della proprietà:** `backgroundImageOpacity`</span><span class="sxs-lookup"><span data-stu-id="71981-185">**Property name:** `backgroundImageOpacity`</span></span>

<span data-ttu-id="71981-186">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-186">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-187">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="71981-187">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="71981-188">**Valore predefinito:** `1.0`</span><span class="sxs-lookup"><span data-stu-id="71981-188">**Default value:** `1.0`</span></span>

<br />

___

## <a name="acrylic"></a><span data-ttu-id="71981-189">Acrilico</span><span class="sxs-lookup"><span data-stu-id="71981-189">Acrylic</span></span>

### <a name="enable-acrylic"></a><span data-ttu-id="71981-190">Abilita acrilico</span><span class="sxs-lookup"><span data-stu-id="71981-190">Enable acrylic</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="71981-191">Quando è impostata su `true`, la finestra avrà uno sfondo acrilico.</span><span class="sxs-lookup"><span data-stu-id="71981-191">When this is set to `true`, the window will have an acrylic background.</span></span> <span data-ttu-id="71981-192">Quando è impostato su `false`, la finestra avrà uno sfondo normale e senza trame.</span><span class="sxs-lookup"><span data-stu-id="71981-192">When it's set to `false`, the window will have a plain, untextured background.</span></span> <span data-ttu-id="71981-193">A causa delle limitazioni del sistema operativo, la trasparenza si applica solo alle finestre con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="71981-193">The transparency only applies to focused windows due to OS limitations.</span></span>

<span data-ttu-id="71981-194">**Nome della proprietà:** `useAcrylic`</span><span class="sxs-lookup"><span data-stu-id="71981-194">**Property name:** `useAcrylic`</span></span>

<span data-ttu-id="71981-195">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-195">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-196">**Accetta:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="71981-196">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="71981-197">**Valore predefinito:** `false`</span><span class="sxs-lookup"><span data-stu-id="71981-197">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Acrilico](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a><span data-ttu-id="71981-199">Opacità acrilico</span><span class="sxs-lookup"><span data-stu-id="71981-199">Acrylic opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="71981-200">Quando `useAcrylic` è impostata su `true`, imposta la trasparenza della finestra per il profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-200">When `useAcrylic` is set to `true`, this sets the transparency of the window for the profile.</span></span> <span data-ttu-id="71981-201">Accetta valori a virgola mobile compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="71981-201">This accepts floating point values from 0-1.</span></span>

<span data-ttu-id="71981-202">**Nome della proprietà:** `acrylicOpacity`</span><span class="sxs-lookup"><span data-stu-id="71981-202">**Property name:** `acrylicOpacity`</span></span>

<span data-ttu-id="71981-203">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-203">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-204">**Accetta:** numero come valore a virgola mobile compreso tra 0 e 1</span><span class="sxs-lookup"><span data-stu-id="71981-204">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="71981-205">**Valore predefinito:** `0.5`</span><span class="sxs-lookup"><span data-stu-id="71981-205">**Default value:** `0.5`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Opacità acrilico](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="window"></a><span data-ttu-id="71981-207">Finestra</span><span class="sxs-lookup"><span data-stu-id="71981-207">Window</span></span>

### <a name="padding"></a><span data-ttu-id="71981-208">Spaziatura interna</span><span class="sxs-lookup"><span data-stu-id="71981-208">Padding</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="71981-209">Consente di impostare la spaziatura intorno al testo all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="71981-209">This sets the padding around the text within the window.</span></span> <span data-ttu-id="71981-210">Questo accetta tre formati diversi: `"#"` e imposta `#` la stessa spaziatura interna per tutti i lati, `"#, #"` imposta la stessa spaziatura interna per Left-Right e top-bottom e `"#, #, #, #"` imposta la spaziatura interna singolarmente per left, top, Right e Bottom.</span><span class="sxs-lookup"><span data-stu-id="71981-210">This will accept three different formats: `"#"` and `#` set the same padding for all sides, `"#, #"` sets the same padding for left-right and top-bottom, and `"#, #, #, #"` sets the padding individually for left, top, right, and bottom.</span></span>

<span data-ttu-id="71981-211">**Nome della proprietà:** `padding`</span><span class="sxs-lookup"><span data-stu-id="71981-211">**Property name:** `padding`</span></span>

<span data-ttu-id="71981-212">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-212">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-213">**Accetta:** Valori come stringa nei formati seguenti: `"#"` , `"#, #"` `"#, #, #, #"` o valore come Integer: `#`</span><span class="sxs-lookup"><span data-stu-id="71981-213">**Accepts:** Values as a string in the following formats: `"#"`, `"#, #"`, `"#, #, #, #"` or value as an integer: `#`</span></span>

<span data-ttu-id="71981-214">**Valore predefinito:** `"8, 8, 8, 8"`</span><span class="sxs-lookup"><span data-stu-id="71981-214">**Default value:** `"8, 8, 8, 8"`</span></span>

:::column-end:::
:::column span="":::
![Terminale Windows - Spaziatura interna](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="scrollbar-visibility"></a><span data-ttu-id="71981-216">Visibilità della barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="71981-216">Scrollbar visibility</span></span>

<span data-ttu-id="71981-217">Consente di impostare la visibilità della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="71981-217">This sets the visibility of the scrollbar.</span></span>

<span data-ttu-id="71981-218">**Nome della proprietà:** `scrollbarState`</span><span class="sxs-lookup"><span data-stu-id="71981-218">**Property name:** `scrollbarState`</span></span>

<span data-ttu-id="71981-219">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-219">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-220">**Accetta:** `"visible"`, `"hidden"`</span><span class="sxs-lookup"><span data-stu-id="71981-220">**Accepts:** `"visible"`, `"hidden"`</span></span>

<br />

___

## <a name="color-settings"></a><span data-ttu-id="71981-221">Impostazioni per il colore</span><span class="sxs-lookup"><span data-stu-id="71981-221">Color settings</span></span>

### <a name="tab-color"></a><span data-ttu-id="71981-222">Colore delle schede</span><span class="sxs-lookup"><span data-stu-id="71981-222">Tab color</span></span>

<span data-ttu-id="71981-223">Viene impostato il colore della scheda del profilo. Se si utilizza la selezione colori scheda, questo colore verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="71981-223">This sets the color of the profile's tab. Using the tab color picker will override this color.</span></span>

<span data-ttu-id="71981-224">**Nome della proprietà:** `tabColor`</span><span class="sxs-lookup"><span data-stu-id="71981-224">**Property name:** `tabColor`</span></span>

<span data-ttu-id="71981-225">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-225">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-226">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="71981-226">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="foreground-color"></a><span data-ttu-id="71981-227">Colore primo piano</span><span class="sxs-lookup"><span data-stu-id="71981-227">Foreground color</span></span>

<span data-ttu-id="71981-228">Modifica il colore primo piano del profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-228">This changes the foreground color of the profile.</span></span> <span data-ttu-id="71981-229">Sostituisce il valore di `foreground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="71981-229">This overrides `foreground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="71981-230">**Nome della proprietà:** `foreground`</span><span class="sxs-lookup"><span data-stu-id="71981-230">**Property name:** `foreground`</span></span>

<span data-ttu-id="71981-231">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-231">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-232">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="71981-232">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="background-color"></a><span data-ttu-id="71981-233">Colore di sfondo</span><span class="sxs-lookup"><span data-stu-id="71981-233">Background color</span></span>

<span data-ttu-id="71981-234">Modifica il colore di sfondo del profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-234">This changes the background color of the profile with this setting.</span></span> <span data-ttu-id="71981-235">Sostituisce il valore di `background` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="71981-235">This overrides `background` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="71981-236">**Nome della proprietà:** `background`</span><span class="sxs-lookup"><span data-stu-id="71981-236">**Property name:** `background`</span></span>

<span data-ttu-id="71981-237">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-237">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-238">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="71981-238">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="selection-background-color"></a><span data-ttu-id="71981-239">Colore di sfondo della selezione</span><span class="sxs-lookup"><span data-stu-id="71981-239">Selection background color</span></span>

<span data-ttu-id="71981-240">Consente di impostare il colore di sfondo di una selezione nel profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-240">This sets the background color of a selection within the profile.</span></span> <span data-ttu-id="71981-241">Sostituisce il valore di `selectionBackground` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="71981-241">This will override the `selectionBackground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="71981-242">**Nome della proprietà:** `selectionBackground`</span><span class="sxs-lookup"><span data-stu-id="71981-242">**Property name:** `selectionBackground`</span></span>

<span data-ttu-id="71981-243">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-243">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-244">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="71981-244">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="cursor-color"></a><span data-ttu-id="71981-245">Colore del cursore</span><span class="sxs-lookup"><span data-stu-id="71981-245">Cursor color</span></span>

<span data-ttu-id="71981-246">Consente di impostare il colore del cursore per il profilo.</span><span class="sxs-lookup"><span data-stu-id="71981-246">This sets the cursor color of the profile.</span></span> <span data-ttu-id="71981-247">Sostituisce il valore di `cursorColor` impostato nella combinazione colori se è impostata `colorScheme`.</span><span class="sxs-lookup"><span data-stu-id="71981-247">This will override the `cursorColor` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="71981-248">**Nome della proprietà:** `cursorColor`</span><span class="sxs-lookup"><span data-stu-id="71981-248">**Property name:** `cursorColor`</span></span>

<span data-ttu-id="71981-249">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-249">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-250">**Accetta:** colore in formato stringa esadecimale: `"#rgb"` o `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="71981-250">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

<br />

___

## <a name="pixel-shader-effects-preview"></a><span data-ttu-id="71981-251">Effetti pixel shader ([Anteprima](https://aka.ms/terminal-preview))</span><span class="sxs-lookup"><span data-stu-id="71981-251">Pixel shader effects ([Preview](https://aka.ms/terminal-preview))</span></span>

<span data-ttu-id="71981-252">Questa impostazione consente a un utente di specificare il percorso di un pixel shader personalizzato da usare con il contenuto del terminale.</span><span class="sxs-lookup"><span data-stu-id="71981-252">This setting allows a user to specify the path to a custom pixel shader to use with the terminal content.</span></span> <span data-ttu-id="71981-253">Si tratta di una funzionalità sperimentale che potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="71981-253">This is an experimental feature and its continued existence is not guaranteed.</span></span> <span data-ttu-id="71981-254">Per altri dettagli sulla creazione di pixel shader personalizzati per il terminale, vedere [questa documentazione](https://github.com/microsoft/terminal/blob/main/samples/PixelShaders/README.md).</span><span class="sxs-lookup"><span data-stu-id="71981-254">For more details on authoring custom pixel shaders for the terminal, see [this documentation](https://github.com/microsoft/terminal/blob/main/samples/PixelShaders/README.md).</span></span>

<span data-ttu-id="71981-255">Se impostato, l'impostazione verrà sostituita `experimental.retroTerminalEffect` .</span><span class="sxs-lookup"><span data-stu-id="71981-255">If set, this will override the `experimental.retroTerminalEffect` setting.</span></span>

<span data-ttu-id="71981-256">**Nome della proprietà:** `experimental.pixelShaderPath`</span><span class="sxs-lookup"><span data-stu-id="71981-256">**Property name:** `experimental.pixelShaderPath`</span></span>

<span data-ttu-id="71981-257">**Obbligatoria:** Facoltativo</span><span class="sxs-lookup"><span data-stu-id="71981-257">**Necessity:** Optional</span></span>

<span data-ttu-id="71981-258">**Accetta:** Percorso di un `.hlsl` file shader sotto forma di stringa</span><span class="sxs-lookup"><span data-stu-id="71981-258">**Accepts:** A path to an `.hlsl` shader file, as a string</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71981-259">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="71981-259">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>
