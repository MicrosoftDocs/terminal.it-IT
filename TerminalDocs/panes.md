---
title: Riquadri di Terminale Windows
description: Informazioni su come dividere i riquadri in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: 0e2d7a50e1a3c933f7ab2d98bda5be6b8ee44e7e
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994333"
---
# <a name="panes-in-windows-terminal"></a><span data-ttu-id="3a847-103">Riquadri in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="3a847-103">Panes in Windows Terminal</span></span>

<span data-ttu-id="3a847-104">I riquadri offrono la possibilità di eseguire più applicazioni da riga di comando una accanto all'altra all'interno della stessa scheda. Questa opzione riduce la necessità di spostarsi tra schede e ti consente di vedere più prompt contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="3a847-104">Panes give you the ability to run multiple command-line applications next to each other within the same tab. This minimizes the need to switch between tabs and lets you see multiple prompts at once.</span></span>

## <a name="creating-a-new-pane"></a><span data-ttu-id="3a847-105">Creazione di un nuovo riquadro</span><span class="sxs-lookup"><span data-stu-id="3a847-105">Creating a new pane</span></span>

### <a name="using-the-keyboard"></a><span data-ttu-id="3a847-106">Uso della tastiera</span><span class="sxs-lookup"><span data-stu-id="3a847-106">Using the keyboard</span></span>

<span data-ttu-id="3a847-107">In Terminale Windows è possibile creare un nuovo riquadro verticale o orizzontale.</span><span class="sxs-lookup"><span data-stu-id="3a847-107">You can either create a new vertical or horizontal pane in Windows Terminal.</span></span> <span data-ttu-id="3a847-108">La divisione in verticale apre un nuovo riquadro a destra di quello con lo stato attivo, mentre la divisione in orizzontale ne apre uno nuovo sotto quello con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="3a847-108">Splitting vertically will open a new pane to the right of the focused pane and splitting horizontally will open a new pane below the focused pane.</span></span> <span data-ttu-id="3a847-109">Per creare un nuovo riquadro verticale del profilo predefinito, premi <kbd>ALT+MAIUSC++</kbd>.</span><span class="sxs-lookup"><span data-stu-id="3a847-109">To create a new vertical pane of your default profile, you can type <kbd>alt+shift+plus</kbd>.</span></span> <span data-ttu-id="3a847-110">Per creare un riquadro orizzontale del profilo predefinito, premi <kbd>ALT+MAIUSC+-</kbd>.</span><span class="sxs-lookup"><span data-stu-id="3a847-110">For a horizontal pane of your default profile, you can type <kbd>alt+shift+-</kbd>.</span></span>

<span data-ttu-id="3a847-111">![Creazione di riquadri di Terminale Windows](./images/open-panes.gif)
_Configurazione: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="3a847-111">![Windows Terminal create pane](./images/open-panes.gif)
_Configuration: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

<span data-ttu-id="3a847-112">Per cambiare queste combinazioni di tasti, puoi crearne altre usando l'azione `splitPane` e i valori `vertical` o `horizontal` per la proprietà `split` nel file profiles.json.</span><span class="sxs-lookup"><span data-stu-id="3a847-112">If you would like to change these key bindings, you can create new ones using the `splitPane` action and `vertical` or `horizontal` values for the `split` property in your profiles.json file.</span></span> <span data-ttu-id="3a847-113">Per avere un unico riquadro con la quantità massima di area disponibile, imposta `split` su `auto`.</span><span class="sxs-lookup"><span data-stu-id="3a847-113">If you just want a pane with the maximum amount of surface area, you can set `split` to `auto`.</span></span> <span data-ttu-id="3a847-114">Per altre informazioni, vedi la [pagina sulle combinazioni di tasti](./customize-settings/key-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="3a847-114">To learn more about key bindings, visit the [key bindings page](./customize-settings/key-bindings.md).</span></span>

```json
{ "command": { "action": "splitPane", "split": "vertical" }, "keys": "alt+shift+plus" },
{ "command": { "action": "splitPane", "split": "horizontal" }, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "auto" }, "keys": "alt+shift+|" }
```

### <a name="using-the-dropdown-menu-preview"></a><span data-ttu-id="3a847-115">Uso del menu a discesa ([anteprima](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="3a847-115">Using the dropdown menu ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="3a847-116">Per aprire un nuovo riquadro tramite il menu a discesa, tenere premuto <kbd>ALT</kbd> e fare clic sul profilo desiderato.</span><span class="sxs-lookup"><span data-stu-id="3a847-116">If you'd like to open a new pane through the dropdown menu, you can hold <kbd>alt</kbd> and click on your desired profile.</span></span> <span data-ttu-id="3a847-117">In questo modo la finestra o il riquadro attivo viene diviso in modalità `auto` in un nuovo riquadro del profilo selezionato.</span><span class="sxs-lookup"><span data-stu-id="3a847-117">This will `auto` split the active window or pane into a new pane of the selected profile.</span></span> <span data-ttu-id="3a847-118">La divisione in modalità `auto` viene applicata nella direzione con il bordo più lungo per creare un riquadro.</span><span class="sxs-lookup"><span data-stu-id="3a847-118">The `auto` split mode splits in the direction that has the longest edge to create a pane.</span></span>

![Riquadro a discesa di Terminale Windows](./images/alt-click-pane.gif)

> [!IMPORTANT]
> <span data-ttu-id="3a847-120">Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview/).</span><span class="sxs-lookup"><span data-stu-id="3a847-120">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

## <a name="switching-between-panes"></a><span data-ttu-id="3a847-121">Passaggio tra riquadri</span><span class="sxs-lookup"><span data-stu-id="3a847-121">Switching between panes</span></span>

<span data-ttu-id="3a847-122">Il terminale ti consente di spostarti tra i riquadri usando la tastiera.</span><span class="sxs-lookup"><span data-stu-id="3a847-122">The terminal allows you to navigate between panes by using the keyboard.</span></span> <span data-ttu-id="3a847-123">Se tieni premuto <kbd>ALT</kbd>, puoi usare i tasti di direzione per spostare lo stato attivo tra i riquadri.</span><span class="sxs-lookup"><span data-stu-id="3a847-123">If you hold the <kbd>alt</kbd> key, you can use your arrow keys to move your focus between panes.</span></span> <span data-ttu-id="3a847-124">Il riquadro con lo stato attivo è identificabile dal colore in risalto del bordo che lo circonda.</span><span class="sxs-lookup"><span data-stu-id="3a847-124">You can identify which pane is in focus by the accent color border surrounding it.</span></span> <span data-ttu-id="3a847-125">Questo colore è configurato nelle impostazioni dei colori di Windows.</span><span class="sxs-lookup"><span data-stu-id="3a847-125">Note that this accent color is set in your Windows color settings.</span></span>

![Passaggio tra i riquadri di Terminale Windows](./images/navigate-panes.gif)

<span data-ttu-id="3a847-127">Puoi personalizzare questa impostazione aggiungendo combinazioni di tasti per il comando `moveFocus` e impostando `direction` su `down`, `left`, `right` o `up`.</span><span class="sxs-lookup"><span data-stu-id="3a847-127">You can customize this by adding key bindings for the `moveFocus` command and setting the `direction` to either `down`, `left`, `right` or `up`.</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

## <a name="resizing-a-pane"></a><span data-ttu-id="3a847-128">Ridimensionamento di un riquadro</span><span class="sxs-lookup"><span data-stu-id="3a847-128">Resizing a pane</span></span>

<span data-ttu-id="3a847-129">Per modificare le dimensioni dei riquadri, tieni premuto <kbd>ALT+MAIUSC</kbd> e usa i tasti di direzione per ridimensionare il riquadro con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="3a847-129">You can adjust the size of your panes by holding <kbd>alt+shift</kbd> and using your arrow keys to resize the focused pane.</span></span>

![Creazione di riquadri di Terminale Windows](./images/resize-panes.gif)

<span data-ttu-id="3a847-131">Per personalizzare questa combinazione di tasti, puoi aggiungerne altre usando l'azione `resizePane` e impostando `direction` su `down`, `left`, `right` o `up`.</span><span class="sxs-lookup"><span data-stu-id="3a847-131">To customize this key binding, you can add new ones using the `resizePane` action and setting the `direction` to either `down`, `left`, `right`, or `up`.</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

## <a name="closing-a-pane"></a><span data-ttu-id="3a847-132">Chiusura di un riquadro</span><span class="sxs-lookup"><span data-stu-id="3a847-132">Closing a pane</span></span>

<span data-ttu-id="3a847-133">Per chiudere il riquadro con lo stato attivo, premi <kbd>CTRL+MAIUSC+W</kbd>.</span><span class="sxs-lookup"><span data-stu-id="3a847-133">You can close the focused pane by typing <kbd>ctrl+shift+w</kbd>.</span></span> <span data-ttu-id="3a847-134">Se è aperto un solo riquadro, <kbd>CTRL+MAIUSC+W</kbd> chiuderà la scheda. Come sempre, chiudendo l'ultima scheda si chiuderà la finestra.</span><span class="sxs-lookup"><span data-stu-id="3a847-134">If you only have one pane, <kbd>ctrl+shift+w</kbd> will close the tab. As always, closing the last tab will close the window.</span></span>

![Chiusura dei riquadri di Terminale Windows](./images/close-panes.gif)

<span data-ttu-id="3a847-136">Puoi cambiare i tasti di chiusura del riquadro aggiungendo una combinazione che usa il comando `closePane`.</span><span class="sxs-lookup"><span data-stu-id="3a847-136">You can change which keys close the pane by adding a key binding that uses the `closePane` command.</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

## <a name="customizing-panes-using-key-bindings"></a><span data-ttu-id="3a847-137">Personalizzazione dei riquadri con le combinazioni di tasti</span><span class="sxs-lookup"><span data-stu-id="3a847-137">Customizing panes using key bindings</span></span>

<span data-ttu-id="3a847-138">Puoi personalizzare cosa aprire all'interno di un nuovo riquadro a seconda delle combinazioni di tasti personalizzate.</span><span class="sxs-lookup"><span data-stu-id="3a847-138">You can customize what opens inside a new pane depending on your custom key bindings.</span></span>

### <a name="duplicating-a-pane"></a><span data-ttu-id="3a847-139">Duplicazione di un riquadro</span><span class="sxs-lookup"><span data-stu-id="3a847-139">Duplicating a pane</span></span>

<span data-ttu-id="3a847-140">Il terminale ti consente di duplicare il profilo del riquadro con lo stato attivo in un altro riquadro.</span><span class="sxs-lookup"><span data-stu-id="3a847-140">The terminal allows you to duplicate the focused pane's profile into another pane.</span></span>

![Riquadri duplicati in Terminale di Windows](./images/duplicate-panes.gif)

<span data-ttu-id="3a847-142">A questo scopo, aggiungi la proprietà `splitMode` con `duplicate` come valore a una combinazione di tasti `splitPane`.</span><span class="sxs-lookup"><span data-stu-id="3a847-142">This can be done by adding the `splitMode` property with `duplicate` as the value to a `splitPane` key binding.</span></span>

```json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
```

### <a name="new-terminal-arguments"></a><span data-ttu-id="3a847-143">Nuovi argomenti del terminale</span><span class="sxs-lookup"><span data-stu-id="3a847-143">New terminal arguments</span></span>

[!INCLUDE [new-terminal-arguments](./new-terminal-arguments.md)]
