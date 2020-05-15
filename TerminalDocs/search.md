---
title: Ricerca in Terminale Windows
description: Informazioni su come eseguire ricerche in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: 94932d71e6543a83650e2e2a5febcb0206e22548
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416336"
---
# <a name="how-to-search-in-windows-terminal"></a><span data-ttu-id="e7ce2-103">Come eseguire ricerche in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="e7ce2-103">How to search in Windows Terminal</span></span>

<span data-ttu-id="e7ce2-104">Terminale Windows include una funzionalità di ricerca che ti consente di cercare una parola chiave specifica nel buffer di testo.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-104">The Windows Terminal comes with a search feature that allows you to look through the text buffer for a specific keyword.</span></span> <span data-ttu-id="e7ce2-105">Questa funzionalità è utile per trovare un comando eseguito in precedenza o un nome file specifico.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-105">This is useful when trying to find a command you had run before or for a specific file name.</span></span>

## <a name="using-search"></a><span data-ttu-id="e7ce2-106">Uso della ricerca</span><span class="sxs-lookup"><span data-stu-id="e7ce2-106">Using search</span></span>

<span data-ttu-id="e7ce2-107">Per impostazione predefinita, puoi aprire la finestra di dialogo di ricerca premendo <kbd>CTRL+MAIUSC+F</kbd>.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-107">By default, you can open the search dialog by typing <kbd>ctrl+shift+f</kbd>.</span></span> <span data-ttu-id="e7ce2-108">Una volta aperta, digita la parola chiave da cercare nella casella di testo e premi <kbd>INVIO</kbd> per avviare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-108">Once opened, you can type the keyword you're looking for into the text box and hit <kbd>enter</kbd> to search.</span></span>

<span data-ttu-id="e7ce2-109">![Screenshot della ricerca in Terminale Windows](./images/search.png)
_Configurazione: [Powerline in PowerShell](./custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="e7ce2-109">![Windows Terminal search screenshot](./images/search.png)
_Configuration: [Powerline in PowerShell](./custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

## <a name="directional-search"></a><span data-ttu-id="e7ce2-110">Ricerca direzionale</span><span class="sxs-lookup"><span data-stu-id="e7ce2-110">Directional search</span></span>

<span data-ttu-id="e7ce2-111">Per impostazione predefinita, il terminale eseguirà la ricerca dal basso verso l'alto nel buffer di testo.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-111">The terminal will default to searching from the bottom to the top of the text buffer.</span></span> <span data-ttu-id="e7ce2-112">Puoi cambiare la direzione della ricerca selezionando una delle frecce nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-112">You can change the search direction by selecting one of the arrows in the search dialog.</span></span>

![Screenshot della ricerca direzionale in Terminale Windows](./images/search-direction.gif)

## <a name="case-match-search"></a><span data-ttu-id="e7ce2-114">Ricerca con corrispondenza tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="e7ce2-114">Case match search</span></span>

<span data-ttu-id="e7ce2-115">Per restringere i risultati della ricerca, puoi aggiungere la corrispondenza tra maiuscole e minuscole come opzione.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-115">If you'd like to narrow down your search results, you can add case matching as an option in your search.</span></span> <span data-ttu-id="e7ce2-116">Per attivare la corrispondenza tra maiuscole e minuscole, seleziona l'apposito pulsante. I risultati visualizzati corrisponderanno solo alla parola chiave immessa con la combinazione specifica di maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-116">You can toggle case matching by selecting the case match button, and the results that appear will only match the keyword entered with its specific letter casing.</span></span>

![Screenshot della ricerca di Terminale Windows con corrispondenza tra maiuscole e minuscole](./images/search-case-match.gif)

## <a name="searching-within-panes"></a><span data-ttu-id="e7ce2-118">Ricerca all'interno dei riquadri</span><span class="sxs-lookup"><span data-stu-id="e7ce2-118">Searching within panes</span></span>

<span data-ttu-id="e7ce2-119">La finestra di dialogo di ricerca funziona anche con i [riquadri](./panes.md).</span><span class="sxs-lookup"><span data-stu-id="e7ce2-119">The search dialog works with [panes](./panes.md) as well.</span></span> <span data-ttu-id="e7ce2-120">In un riquadro con lo stato attivo puoi aprire la finestra di dialogo di ricerca, che verrà visualizzata nel riquadro in alto a destra.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-120">When focused on a pane, you can open the search dialog and it will appear on the upper-right of that pane.</span></span> <span data-ttu-id="e7ce2-121">Quindi, qualsiasi parola chiave immessa mostrerà solo i risultati trovati all'interno di tale riquadro.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-121">Then any keyword you enter will only show results found within that pane.</span></span>

![Screenshot della ricerca nei riquadri in Terminale Windows](./images/search-panes.gif)

## <a name="customize-the-search-key-binding"></a><span data-ttu-id="e7ce2-123">Personalizzare la combinazione di tasti della ricerca</span><span class="sxs-lookup"><span data-stu-id="e7ce2-123">Customize the search key binding</span></span>

<span data-ttu-id="e7ce2-124">Puoi aprire la finestra di dialogo di ricerca con qualsiasi combinazione di tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-124">You can open the search dialog with any key binding (shortcut key combination) that you prefer.</span></span> <span data-ttu-id="e7ce2-125">Per cambiare la combinazione di tasti della ricerca, apri il file settings.json e cerca il comando `find`.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-125">To change the search key binding, open your settings.json file and search for the `find` command.</span></span> <span data-ttu-id="e7ce2-126">Per impostazione predefinita, questo comando è impostato su `ctrl+shift+f`.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-126">By default, this command is set to `ctrl+shift+f`.</span></span>

```json
// Press ctrl+shift+f to open the search box
        { "command": "find", "keys": "ctrl+shift+f" },
```

<span data-ttu-id="e7ce2-127">Puoi ad esempio sostituire "CTRL+MAIUSC+F" con "CTRL+F", in modo che premendo `ctrl+f` venga visualizzata la finestra di dialogo di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e7ce2-127">For example, you can change "ctrl+shift+f" to "ctrl+f", so when typing `ctrl+f`, the search dialog will open.</span></span>

<span data-ttu-id="e7ce2-128">Per altre informazioni, vedi la [pagina sulle combinazioni di tasti](./customize-settings/key-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="e7ce2-128">To learn more about key bindings, visit the [key bindings page](./customize-settings/key-bindings.md).</span></span>
