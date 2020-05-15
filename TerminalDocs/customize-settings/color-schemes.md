---
title: Terminale Windows - Combinazioni colori
description: Informazioni su come creare combinazioni colori per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 4c4b602f2d8d6e3da20ef0b26845517e4512fd87
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415916"
---
# <a name="color-schemes-in-the-windows-terminal"></a><span data-ttu-id="402ee-103">Combinazioni colori in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="402ee-103">Color schemes in the Windows Terminal</span></span>

## <a name="creating-your-own-color-scheme"></a><span data-ttu-id="402ee-104">Creazione di una combinazione colori personalizzata</span><span class="sxs-lookup"><span data-stu-id="402ee-104">Creating your own color scheme</span></span>

<span data-ttu-id="402ee-105">È possibile definire le combinazioni di colori nella matrice `schemes` del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="402ee-105">Color schemes can be defined in the `schemes` array of your settings.json file.</span></span> <span data-ttu-id="402ee-106">Le combinazioni vengono scritte nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="402ee-106">They are written in the following format:</span></span>

```json
{
    "name" : "Campbell",

    "cursorColor": "#FFFFFF",
    "selectionBackground": "#",

    "background" : "#0C0C0C",
    "foreground" : "#CCCCCC",

    "black" : "#0C0C0C",
    "blue" : "#0037DA",
    "cyan" : "#3A96DD",
    "green" : "#13A10E",
    "purple" : "#881798",
    "red" : "#C50F1F",
    "white" : "#CCCCCC",
    "yellow" : "#C19C00",
    "brightBlack" : "#767676",
    "brightBlue" : "#3B78FF",
    "brightCyan" : "#61D6D6",
    "brightGreen" : "#16C60C",
    "brightPurple" : "#B4009E",
    "brightRed" : "#E74856",
    "brightWhite" : "#F2F2F2",
    "brightYellow" : "#F9F1A5"
},
```

<span data-ttu-id="402ee-107">Ogni impostazione, eccetto `name`, accetta un colore in formato stringa esadecimale, ovvero `"#rgb"` o `"#rrggbb"`.</span><span class="sxs-lookup"><span data-stu-id="402ee-107">Every setting, aside from `name`, accepts a color as a string in hex format: `"#rgb"` or `"#rrggbb"`.</span></span> <span data-ttu-id="402ee-108">Le impostazioni `cursorColor` e `selectionBackground` sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="402ee-108">The `cursorColor` and `selectionBackground` settings are optional.</span></span>

<br />

___

## <a name="included-color-schemes"></a><span data-ttu-id="402ee-109">Combinazioni colori incluse</span><span class="sxs-lookup"><span data-stu-id="402ee-109">Included color schemes</span></span>

<span data-ttu-id="402ee-110">Le combinazioni colori di Terminale Windows sono incluse nel file defaults.json. Per accedervi, tieni premuto <kbd>alt</kbd> mentre fai clic sulla voce di menu Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="402ee-110">Windows Terminal includes these color schemes inside the defaults.json file, which can be accessed by holding <kbd>alt</kbd> and selecting the settings button.</span></span> <span data-ttu-id="402ee-111">Se vuoi impostare una combinazione colori all'interno di uno dei profili della riga di comando, aggiungi la proprietà `colorScheme` specificando come valore l'impostazione `name` della combinazione colori.</span><span class="sxs-lookup"><span data-stu-id="402ee-111">If you would like to set up a color scheme inside one of your command line profiles, add the `colorScheme` property with the color scheme's `name` as the value.</span></span>

```json
"colorScheme": "COLOR SCHEME NAME"
```

### <a name="campbell"></a><span data-ttu-id="402ee-112">Campbell</span><span class="sxs-lookup"><span data-stu-id="402ee-112">Campbell</span></span>

![Terminale Windows - Combinazione colori Campbell](./../images/campbell-color-scheme.png)

### <a name="campbell-powershell"></a><span data-ttu-id="402ee-114">Campbell Powershell</span><span class="sxs-lookup"><span data-stu-id="402ee-114">Campbell Powershell</span></span>

![Terminale Windows - Combinazione colori Campbell Powershell](./../images/campbell-powershell-color-scheme.png)

### <a name="vintage"></a><span data-ttu-id="402ee-116">Vintage</span><span class="sxs-lookup"><span data-stu-id="402ee-116">Vintage</span></span>

![Terminale Windows - Combinazione colori Vintage](./../images/vintage-color-scheme.png)

### <a name="one-half-dark"></a><span data-ttu-id="402ee-118">One Half Dark</span><span class="sxs-lookup"><span data-stu-id="402ee-118">One Half Dark</span></span>

![Terminale Windows - Combinazione colori One Half Dark](./../images/one-half-dark-color-scheme.png)

### <a name="one-half-light"></a><span data-ttu-id="402ee-120">One Half Light</span><span class="sxs-lookup"><span data-stu-id="402ee-120">One Half Light</span></span>

![Terminale Windows - Combinazione colori One Half Light](./../images/one-half-light-color-scheme.png)

### <a name="solarized-dark"></a><span data-ttu-id="402ee-122">Solarized Dark</span><span class="sxs-lookup"><span data-stu-id="402ee-122">Solarized Dark</span></span>

![Terminale Windows - Combinazione colori Solarized Dark](./../images/solarized-dark-color-scheme.png)

### <a name="solarized-light"></a><span data-ttu-id="402ee-124">Solarized Light</span><span class="sxs-lookup"><span data-stu-id="402ee-124">Solarized Light</span></span>

![Terminale Windows - Combinazione colori Solarized Light](./../images/solarized-light-color-scheme.png)

### <a name="tango-dark"></a><span data-ttu-id="402ee-126">Tango Dark</span><span class="sxs-lookup"><span data-stu-id="402ee-126">Tango Dark</span></span>

![Terminale Windows - Combinazione colori Tango Dark](./../images/tango-dark-color-scheme.png)

### <a name="tango-light"></a><span data-ttu-id="402ee-128">Tango Light</span><span class="sxs-lookup"><span data-stu-id="402ee-128">Tango Light</span></span>

![Terminale Windows - Combinazione colori Tango Light](./../images/tango-light-color-scheme.png)
