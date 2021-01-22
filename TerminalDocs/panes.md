---
title: Riquadri di Terminale Windows
description: Informazioni su come dividere i riquadri in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 09/22/2020
ms.topic: how-to
ms.openlocfilehash: 07badec2c42ace043544ae539c4b586a3c5f08d9
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988541"
---
# <a name="panes-in-windows-terminal"></a><span data-ttu-id="69e90-103">Riquadri in Terminale Windows</span><span class="sxs-lookup"><span data-stu-id="69e90-103">Panes in Windows Terminal</span></span>

<span data-ttu-id="69e90-104">I riquadri offrono la possibilità di eseguire più applicazioni da riga di comando una accanto all'altra all'interno della stessa scheda. Questa opzione riduce la necessità di spostarsi tra schede e ti consente di vedere più prompt contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="69e90-104">Panes give you the ability to run multiple command-line applications next to each other within the same tab. This minimizes the need to switch between tabs and lets you see multiple prompts at once.</span></span>

## <a name="creating-a-new-pane"></a><span data-ttu-id="69e90-105">Creazione di un nuovo riquadro</span><span class="sxs-lookup"><span data-stu-id="69e90-105">Creating a new pane</span></span>

### <a name="using-the-keyboard"></a><span data-ttu-id="69e90-106">Uso della tastiera</span><span class="sxs-lookup"><span data-stu-id="69e90-106">Using the keyboard</span></span>

<span data-ttu-id="69e90-107">In Terminale Windows è possibile creare un nuovo riquadro verticale o orizzontale.</span><span class="sxs-lookup"><span data-stu-id="69e90-107">You can either create a new vertical or horizontal pane in Windows Terminal.</span></span> <span data-ttu-id="69e90-108">La divisione in verticale apre un nuovo riquadro a destra di quello con lo stato attivo, mentre la divisione in orizzontale ne apre uno nuovo sotto quello con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="69e90-108">Splitting vertically will open a new pane to the right of the focused pane and splitting horizontally will open a new pane below the focused pane.</span></span> <span data-ttu-id="69e90-109">Per creare un nuovo riquadro verticale del profilo predefinito, è possibile premere la combinazione di tasti <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>=</kbd> .</span><span class="sxs-lookup"><span data-stu-id="69e90-109">To create a new vertical pane of your default profile, you can press the <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>=</kbd> key combination.</span></span> <span data-ttu-id="69e90-110">Per un riquadro orizzontale del profilo predefinito, è possibile utilizzare <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>-</kbd> .</span><span class="sxs-lookup"><span data-stu-id="69e90-110">For a horizontal pane of your default profile, you can use <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>-</kbd>.</span></span>

<span data-ttu-id="69e90-111">![Creazione di riquadri di Terminale Windows](./images/open-panes.gif)
_Configurazione: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="69e90-111">![Windows Terminal create pane](./images/open-panes.gif)
_Configuration: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

<span data-ttu-id="69e90-112">Se si desidera modificare questi tasti di scelta, è possibile crearne di nuovi utilizzando l' `splitPane` azione e `vertical` `horizontal` i valori, o `auto` per la `split` proprietà nel profiles.jssu file.</span><span class="sxs-lookup"><span data-stu-id="69e90-112">If you would like to change these key bindings, you can create new ones using the `splitPane` action and `vertical`, `horizontal`, or `auto` values for the `split` property in your profiles.json file.</span></span> <span data-ttu-id="69e90-113">Il `auto` Metodo sceglierà la direzione che fornisce i riquadri al quadrato.</span><span class="sxs-lookup"><span data-stu-id="69e90-113">The `auto` method will choose the direction that gives you the squarest panes.</span></span> <span data-ttu-id="69e90-114">Per ulteriori informazioni sui tasti di scelta, visitare la [pagina azioni](./customize-settings/actions.md).</span><span class="sxs-lookup"><span data-stu-id="69e90-114">To learn more about key bindings, visit the [Actions page](./customize-settings/actions.md).</span></span>

```json
{ "command": { "action": "splitPane", "split": "vertical" }, "keys": "alt+shift+=" },
{ "command": { "action": "splitPane", "split": "horizontal" }, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "auto" }, "keys": "alt+shift+d" }
```

### <a name="using-the-new-tab-button-and-dropdown-menu"></a><span data-ttu-id="69e90-115">Utilizzando il pulsante nuova scheda e il menu a discesa</span><span class="sxs-lookup"><span data-stu-id="69e90-115">Using the new tab button and dropdown menu</span></span>

<span data-ttu-id="69e90-116">Se si vuole aprire un nuovo riquadro del profilo predefinito, è possibile mantenere il tasto <kbd>ALT</kbd> e fare clic sul pulsante nuova scheda.</span><span class="sxs-lookup"><span data-stu-id="69e90-116">If you'd like to open a new pane of your default profile, you can hold the <kbd>alt</kbd> key and click the new tab button.</span></span> <span data-ttu-id="69e90-117">Per aprire un nuovo riquadro tramite il menu a discesa, tenere premuto <kbd>ALT</kbd> e fare clic sul profilo desiderato.</span><span class="sxs-lookup"><span data-stu-id="69e90-117">If you'd like to open a new pane through the dropdown menu, you can hold <kbd>alt</kbd> and click on your desired profile.</span></span> <span data-ttu-id="69e90-118">Entrambe queste opzioni `auto` suddivideranno la finestra o il riquadro attivo in un nuovo riquadro del profilo selezionato.</span><span class="sxs-lookup"><span data-stu-id="69e90-118">Both of these options will `auto` split the active window or pane into a new pane of the selected profile.</span></span> <span data-ttu-id="69e90-119">La divisione in modalità `auto` viene applicata nella direzione con il bordo più lungo per creare un riquadro.</span><span class="sxs-lookup"><span data-stu-id="69e90-119">The `auto` split mode splits in the direction that has the longest edge to create a pane.</span></span>

![Riquadro a discesa di Terminale Windows](./images/alt-click-pane.gif)

## <a name="switching-between-panes"></a><span data-ttu-id="69e90-121">Passaggio tra riquadri</span><span class="sxs-lookup"><span data-stu-id="69e90-121">Switching between panes</span></span>

<span data-ttu-id="69e90-122">Il terminale ti consente di spostarti tra i riquadri usando la tastiera.</span><span class="sxs-lookup"><span data-stu-id="69e90-122">The terminal allows you to navigate between panes by using the keyboard.</span></span> <span data-ttu-id="69e90-123">Se si tiene premuto il tasto <kbd>ALT</kbd> , è possibile usare i tasti di direzione per spostare lo stato attivo tra i riquadri.</span><span class="sxs-lookup"><span data-stu-id="69e90-123">If you hold the <kbd>Alt</kbd> key, you can use your arrow keys to move your focus between panes.</span></span> <span data-ttu-id="69e90-124">Il riquadro con lo stato attivo è identificabile dal colore in risalto del bordo che lo circonda.</span><span class="sxs-lookup"><span data-stu-id="69e90-124">You can identify which pane is in focus by the accent color border surrounding it.</span></span> <span data-ttu-id="69e90-125">Questo colore è configurato nelle impostazioni dei colori di Windows.</span><span class="sxs-lookup"><span data-stu-id="69e90-125">Note that this accent color is set in your Windows color settings.</span></span>

![Passaggio tra i riquadri di Terminale Windows](./images/navigate-panes.gif)

<span data-ttu-id="69e90-127">Puoi personalizzare questa impostazione aggiungendo combinazioni di tasti per il comando `moveFocus` e impostando `direction` su `down`, `left`, `right` o `up`.</span><span class="sxs-lookup"><span data-stu-id="69e90-127">You can customize this by adding key bindings for the `moveFocus` command and setting the `direction` to either `down`, `left`, `right` or `up`.</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

## <a name="resizing-a-pane"></a><span data-ttu-id="69e90-128">Ridimensionamento di un riquadro</span><span class="sxs-lookup"><span data-stu-id="69e90-128">Resizing a pane</span></span>

<span data-ttu-id="69e90-129">È possibile modificare le dimensioni dei riquadri tenendo premuto <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> e utilizzando i tasti di direzione per ridimensionare il riquadro con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="69e90-129">You can adjust the size of your panes by holding <kbd>Alt</kbd>+<kbd>Shift</kbd> and using your arrow keys to resize the focused pane.</span></span>

![Riquadro di ridimensionamento del terminale di Windows](./images/resize-panes.gif)

<span data-ttu-id="69e90-131">Per personalizzare questa combinazione di tasti, puoi aggiungerne altre usando l'azione `resizePane` e impostando `direction` su `down`, `left`, `right` o `up`.</span><span class="sxs-lookup"><span data-stu-id="69e90-131">To customize this key binding, you can add new ones using the `resizePane` action and setting the `direction` to either `down`, `left`, `right`, or `up`.</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

## <a name="closing-a-pane"></a><span data-ttu-id="69e90-132">Chiusura di un riquadro</span><span class="sxs-lookup"><span data-stu-id="69e90-132">Closing a pane</span></span>

<span data-ttu-id="69e90-133">È possibile chiudere il riquadro con lo stato attivo digitando <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>W</kbd>.</span><span class="sxs-lookup"><span data-stu-id="69e90-133">You can close the focused pane by typing <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>W</kbd>.</span></span> <span data-ttu-id="69e90-134">Se è presente un solo riquadro, <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>W</kbd> chiuderà la scheda. Come sempre, chiudendo l'ultima scheda si chiude la finestra.</span><span class="sxs-lookup"><span data-stu-id="69e90-134">If you only have one pane, <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>W</kbd> will close the tab. As always, closing the last tab will close the window.</span></span>

![Chiusura dei riquadri di Terminale Windows](./images/close-panes.gif)

<span data-ttu-id="69e90-136">Puoi cambiare i tasti di chiusura del riquadro aggiungendo una combinazione che usa il comando `closePane`.</span><span class="sxs-lookup"><span data-stu-id="69e90-136">You can change which keys close the pane by adding a key binding that uses the `closePane` command.</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

## <a name="customizing-panes-using-key-bindings"></a><span data-ttu-id="69e90-137">Personalizzazione dei riquadri con le combinazioni di tasti</span><span class="sxs-lookup"><span data-stu-id="69e90-137">Customizing panes using key bindings</span></span>

<span data-ttu-id="69e90-138">Puoi personalizzare cosa aprire all'interno di un nuovo riquadro a seconda delle combinazioni di tasti personalizzate.</span><span class="sxs-lookup"><span data-stu-id="69e90-138">You can customize what opens inside a new pane depending on your custom key bindings.</span></span>

### <a name="duplicating-a-pane"></a><span data-ttu-id="69e90-139">Duplicazione di un riquadro</span><span class="sxs-lookup"><span data-stu-id="69e90-139">Duplicating a pane</span></span>

<span data-ttu-id="69e90-140">Il terminale ti consente di duplicare il profilo del riquadro con lo stato attivo in un altro riquadro.</span><span class="sxs-lookup"><span data-stu-id="69e90-140">The terminal allows you to duplicate the focused pane's profile into another pane.</span></span>

![Riquadri duplicati in Terminale di Windows](./images/duplicate-panes.gif)

<span data-ttu-id="69e90-142">A questo scopo, aggiungi la proprietà `splitMode` con `duplicate` come valore a una combinazione di tasti `splitPane`.</span><span class="sxs-lookup"><span data-stu-id="69e90-142">This can be done by adding the `splitMode` property with `duplicate` as the value to a `splitPane` key binding.</span></span>

```json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
```

[!INCLUDE [new-terminal-arguments](./new-terminal-arguments.md)]
