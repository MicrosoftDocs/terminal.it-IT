---
title: Terminale Windows - Combinazioni colori
description: Informazioni su come creare combinazioni colori per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 6b6741c012a30afa99a17129524d70d72b531f98
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "98981024"
---
# <a name="color-schemes-in-windows-terminal"></a><span data-ttu-id="96855-103">Combinazioni colori in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="96855-103">Color schemes in Windows Terminal</span></span>

<span data-ttu-id="96855-104">Il terminale di Windows consente di definire le proprie combinazioni di colori usando gli schemi predefiniti predefiniti oppure creando uno schema personalizzato da zero.</span><span class="sxs-lookup"><span data-stu-id="96855-104">Windows Terminal lets you define your own color schemes, either by using the built-in preset schemes, or by creating your own scheme from scratch.</span></span> <span data-ttu-id="96855-105">Per modificare gli schemi, è necessario modificare il settings.jssu file in un editor, ad esempio [Visual Studio Code](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="96855-105">To change schemes, you'll need to edit the settings.json file in an editor such as [Visual Studio Code](https://code.visualstudio.com/).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96855-106">L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="96855-106">The settings UI is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span> <span data-ttu-id="96855-107">Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).</span><span class="sxs-lookup"><span data-stu-id="96855-107">Detailed instructions on how to enable the settings UI can be found on the [Troubleshooting page](./../troubleshooting.md#open-the-settings-ui).</span></span>

## <a name="switching-to-a-different-color-scheme"></a><span data-ttu-id="96855-108">Passare a una combinazione di colori diversa</span><span class="sxs-lookup"><span data-stu-id="96855-108">Switching to a different color scheme</span></span>

<span data-ttu-id="96855-109">Avviare Windows Terminal, quindi selezionare la piccola freccia rivolta verso il basso nella barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="96855-109">Launch Windows Terminal and then select the small downward-facing arrow in the title bar.</span></span> <span data-ttu-id="96855-110">Verrà aperto un menu a discesa che elenca i profili disponibili nel sistema (ad esempio, Windows PowerShell e prompt dei comandi) e altre opzioni.</span><span class="sxs-lookup"><span data-stu-id="96855-110">This will open a pull-down menu that lists the available profiles on your system (for example, Windows PowerShell and Command Prompt) and some other options.</span></span> <span data-ttu-id="96855-111">Selezionare **Settings (impostazioni**). l'settings.jsnel file si aprirà nell'editor di testo predefinito.</span><span class="sxs-lookup"><span data-stu-id="96855-111">Select **Settings**, and the settings.json file will open in your default text editor.</span></span>

<span data-ttu-id="96855-112">In questo file è possibile definire diverse opzioni per finestra o per profilo.</span><span class="sxs-lookup"><span data-stu-id="96855-112">This file is where you can define various options per window or per profile.</span></span> <span data-ttu-id="96855-113">Per dimostrare, modificare la combinazione di colori per il profilo del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="96855-113">To demonstrate, let's change the color scheme for the Command Prompt profile.</span></span>

<span data-ttu-id="96855-114">Esaminare il file JSON fino a trovare la sezione che include:</span><span class="sxs-lookup"><span data-stu-id="96855-114">Look down the JSON file until you find the section that includes:</span></span>

```json
"commandline": "cmd.exe",
"hidden": false
```

<span data-ttu-id="96855-115">Modificarlo in lettura:</span><span class="sxs-lookup"><span data-stu-id="96855-115">Change it to read:</span></span>

```json
"commandline": "cmd.exe",
"hidden": false,
"colorScheme": "Tango Light"
```

<span data-ttu-id="96855-116">Si noti la virgola aggiuntiva nella riga **nascosta** .</span><span class="sxs-lookup"><span data-stu-id="96855-116">Notice the extra comma in the **hidden** line.</span></span> <span data-ttu-id="96855-117">Dopo aver salvato il file, il terminale di Windows aggiornerà tutte le finestre aperte.</span><span class="sxs-lookup"><span data-stu-id="96855-117">Once you save this file, Windows Terminal will update any open window.</span></span> <span data-ttu-id="96855-118">Aprire una scheda del prompt dei comandi, se non è già stato fatto, e si noterà immediatamente che i colori sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="96855-118">Open a Command Prompt tab if you haven't already, and you'll immediately see that the colors have changed.</span></span>

## <a name="creating-your-own-color-scheme"></a><span data-ttu-id="96855-119">Creazione di una combinazione colori personalizzata</span><span class="sxs-lookup"><span data-stu-id="96855-119">Creating your own color scheme</span></span>

<span data-ttu-id="96855-120">Lo schema "Tango Light" è incluso come opzione predefinita, ma è possibile creare un proprio schema da zero o copiando uno schema esistente.</span><span class="sxs-lookup"><span data-stu-id="96855-120">The "Tango Light" scheme is included as a default option, but you can create your own scheme from scratch or by copying an existing scheme.</span></span>

<span data-ttu-id="96855-121">È possibile definire le combinazioni di colori nella matrice `schemes` del file settings.json.</span><span class="sxs-lookup"><span data-stu-id="96855-121">Color schemes can be defined in the `schemes` array of your settings.json file.</span></span> <span data-ttu-id="96855-122">Le combinazioni vengono scritte nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="96855-122">They are written in the following format:</span></span>

```json
{
    "name" : "Campbell",

    "cursorColor": "#FFFFFF",
    "selectionBackground": "#FFFFFF",

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

<span data-ttu-id="96855-123">Ogni impostazione, eccetto `name`, accetta un colore in formato stringa esadecimale, ovvero `"#rgb"` o `"#rrggbb"`.</span><span class="sxs-lookup"><span data-stu-id="96855-123">Every setting, aside from `name`, accepts a color as a string in hex format: `"#rgb"` or `"#rrggbb"`.</span></span> <span data-ttu-id="96855-124">Le impostazioni `cursorColor` e `selectionBackground` sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="96855-124">The `cursorColor` and `selectionBackground` settings are optional.</span></span>

<br />

___

## <a name="included-color-schemes"></a><span data-ttu-id="96855-125">Combinazioni colori incluse</span><span class="sxs-lookup"><span data-stu-id="96855-125">Included color schemes</span></span>

<span data-ttu-id="96855-126">Le combinazioni colori di Terminale Windows sono incluse nel file defaults.json. Per accedervi, tieni premuto <kbd>alt</kbd> mentre fai clic sulla voce di menu Impostazioni.</span><span class="sxs-lookup"><span data-stu-id="96855-126">Windows Terminal includes these color schemes inside the defaults.json file, which can be accessed by holding <kbd>alt</kbd> and selecting the settings button.</span></span> 


### <a name="campbell"></a><span data-ttu-id="96855-127">Campbell</span><span class="sxs-lookup"><span data-stu-id="96855-127">Campbell</span></span>

![Terminale Windows - Combinazione colori Campbell](./../images/campbell-color-scheme.png)

### <a name="campbell-powershell"></a><span data-ttu-id="96855-129">Campbell Powershell</span><span class="sxs-lookup"><span data-stu-id="96855-129">Campbell Powershell</span></span>

![Terminale Windows - Combinazione colori Campbell Powershell](./../images/campbell-powershell-color-scheme.png)

### <a name="vintage"></a><span data-ttu-id="96855-131">Vintage</span><span class="sxs-lookup"><span data-stu-id="96855-131">Vintage</span></span>

![Terminale Windows - Combinazione colori Vintage](./../images/vintage-color-scheme.png)

### <a name="one-half-dark"></a><span data-ttu-id="96855-133">One Half Dark</span><span class="sxs-lookup"><span data-stu-id="96855-133">One Half Dark</span></span>

![Terminale Windows - Combinazione colori One Half Dark](./../images/one-half-dark-color-scheme.png)

### <a name="one-half-light"></a><span data-ttu-id="96855-135">One Half Light</span><span class="sxs-lookup"><span data-stu-id="96855-135">One Half Light</span></span>

![Terminale Windows - Combinazione colori One Half Light](./../images/one-half-light-color-scheme.png)

### <a name="tango-dark"></a><span data-ttu-id="96855-137">Tango Dark</span><span class="sxs-lookup"><span data-stu-id="96855-137">Tango Dark</span></span>

![Terminale Windows - Combinazione colori Tango Dark](./../images/tango-dark-color-scheme.png)

### <a name="tango-light"></a><span data-ttu-id="96855-139">Tango Light</span><span class="sxs-lookup"><span data-stu-id="96855-139">Tango Light</span></span>

![Terminale Windows - Combinazione colori Tango Light](./../images/tango-light-color-scheme.png)


## <a name="more-schemes"></a><span data-ttu-id="96855-141">Altri schemi</span><span class="sxs-lookup"><span data-stu-id="96855-141">More schemes</span></span>

<span data-ttu-id="96855-142">Per altri schemi, vedere la sezione [raccolta di terminali personalizzati](../custom-terminal-gallery/custom-schemes.md) .</span><span class="sxs-lookup"><span data-stu-id="96855-142">For more schemes, see the [Custom Terminal Gallery](../custom-terminal-gallery/custom-schemes.md) section.</span></span>
