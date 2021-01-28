---
title: Riquadro comandi terminale di Windows
description: Informazioni su come usare il riquadro comandi nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 1/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 7260194733978b22c8d6c4d0e579c443d4bc652a
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "98981014"
---
# <a name="how-to-use-the-command-palette-in-windows-terminal"></a><span data-ttu-id="8feab-103">Come usare il riquadro comandi nel terminale di Windows</span><span class="sxs-lookup"><span data-stu-id="8feab-103">How to use the command palette in Windows Terminal</span></span>

<span data-ttu-id="8feab-104">Il riquadro comandi consente di visualizzare le azioni che è possibile eseguire nel terminale di Windows.</span><span class="sxs-lookup"><span data-stu-id="8feab-104">The command palette lets you see which actions you can run inside Windows Terminal.</span></span> <span data-ttu-id="8feab-105">Altre informazioni sulla modalità di definizione delle azioni sono disponibili nella [pagina azioni](./customize-settings/actions.md).</span><span class="sxs-lookup"><span data-stu-id="8feab-105">More information on how actions are defined can be found on the [Actions page](./customize-settings/actions.md).</span></span>

## <a name="invoking-the-command-palette"></a><span data-ttu-id="8feab-106">Richiamo del riquadro comandi</span><span class="sxs-lookup"><span data-stu-id="8feab-106">Invoking the command palette</span></span>

<span data-ttu-id="8feab-107">È possibile richiamare il riquadro comandi digitando <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>P</kbd>.</span><span class="sxs-lookup"><span data-stu-id="8feab-107">You can invoke the command palette by typing <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>.</span></span> <span data-ttu-id="8feab-108">Questa operazione può essere personalizzata aggiungendo il `commandPalette` comando alle associazioni di tasti.</span><span class="sxs-lookup"><span data-stu-id="8feab-108">This can be customized by adding the `commandPalette` command to your key bindings.</span></span>

```json
{ "command": "commandPalette", "keys": "ctrl+shift+p" }
```

## <a name="command-line-mode"></a><span data-ttu-id="8feab-109">Modalità riga di comando</span><span class="sxs-lookup"><span data-stu-id="8feab-109">Command line mode</span></span>

<span data-ttu-id="8feab-110">Se si desidera immettere un `wt` comando nel riquadro comandi, è possibile eliminare il `>` carattere nella casella di testo.</span><span class="sxs-lookup"><span data-stu-id="8feab-110">If you'd like to enter a `wt` command into the command palette, you can do so by deleting the `>` character in the text box.</span></span> <span data-ttu-id="8feab-111">Il comando verrà eseguito `wt` nella finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="8feab-111">This will run the `wt` command in the current window.</span></span> <span data-ttu-id="8feab-112">Altre informazioni sui `wt` comandi sono disponibili nella [pagina argomenti della riga di comando](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="8feab-112">More information on `wt` commands can be found on the [Command line arguments page](./command-line-arguments.md).</span></span>

![Modalità riga di comando di Windows Terminal](./images/command-palette-command-line-mode.gif)

<span data-ttu-id="8feab-114">È possibile aggiungere un'associazione di tasti personalizzata per richiamare direttamente il riquadro comandi nella modalità riga di comando.</span><span class="sxs-lookup"><span data-stu-id="8feab-114">You can add a custom key binding for invoking the command palette in the command line mode directly.</span></span>

```json
{ "command": "commandPalette", "launchMode": "commandLine", "keys": "" }
```

> [!IMPORTANT]
> <span data-ttu-id="8feab-115">L'impostazione `"launchMode"` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).</span><span class="sxs-lookup"><span data-stu-id="8feab-115">The `"launchMode"` setting is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview).</span></span>

## <a name="adding-an-icon-to-a-command"></a><span data-ttu-id="8feab-116">Aggiunta di un'icona a un comando</span><span class="sxs-lookup"><span data-stu-id="8feab-116">Adding an icon to a command</span></span>

<span data-ttu-id="8feab-117">Facoltativamente, è possibile aggiungere un'icona a un comando definito nel settings.jsin che viene visualizzato nel riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="8feab-117">You can optionally add an icon to a command defined in your settings.json that appears in the command palette.</span></span> <span data-ttu-id="8feab-118">Questa operazione può essere eseguita aggiungendo la `icon` proprietà all'azione.</span><span class="sxs-lookup"><span data-stu-id="8feab-118">This can be done by adding the `icon` property to the action.</span></span> <span data-ttu-id="8feab-119">Le icone possono essere un percorso di un'immagine, un simbolo di [SEGOE MDL2 asset](https://docs.microsoft.com/windows/uwp/design/style/segoe-ui-symbol-font)o qualsiasi carattere, incluso emoji.</span><span class="sxs-lookup"><span data-stu-id="8feab-119">Icons can be a path to an image, a symbol from [Segoe MDL2 Assets](https://docs.microsoft.com/windows/uwp/design/style/segoe-ui-symbol-font), or any character, including emojis.</span></span>

```json
{ "icon": "C:\\Images\\my-icon.png", "name": "New tab", "command": "newTab", "keys": "ctrl+shift+t" },
{ "icon": "\uE756", "name": "New tab", "command": "newTab", "keys": "ctrl+shift+t" },
{ "icon": "⚡", "name": "New tab", "command": "newTab", "keys": "ctrl+shift+t" }
```

## <a name="nested-commands"></a><span data-ttu-id="8feab-120">Comandi annidati</span><span class="sxs-lookup"><span data-stu-id="8feab-120">Nested commands</span></span>

<span data-ttu-id="8feab-121">I comandi annidati consentono di raggruppare più comandi sotto un elemento nel riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="8feab-121">Nested commands let you group multiple commands under one item in the command palette.</span></span> <span data-ttu-id="8feab-122">Nell'esempio seguente vengono raggruppati i comandi di ridimensionamento dei tipi di carattere sotto un elemento del riquadro comandi denominato "modifica dimensioni carattere...".</span><span class="sxs-lookup"><span data-stu-id="8feab-122">The example below groups the font resize commands under one command palette item called "Change font size...".</span></span>

```json
{
    "name": "Change font size...",
    "commands": [
        { "command": { "action": "adjustFontSize", "delta": 1 } },
        { "command": { "action": "adjustFontSize", "delta": -1 } },
        { "command": "resetFontSize" },
    ]
}
```

![Comandi annidati di Windows Terminal](./images/command-palette-nested-commands.gif)

## <a name="iterable-commands"></a><span data-ttu-id="8feab-124">Comandi iterable</span><span class="sxs-lookup"><span data-stu-id="8feab-124">Iterable commands</span></span>

<span data-ttu-id="8feab-125">I comandi iterable consentono di creare più comandi contemporaneamente, generati da altri oggetti definiti nelle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="8feab-125">Iterable commands let you create multiple commands at the same time, generated from other objects defined in your settings.</span></span> <span data-ttu-id="8feab-126">Attualmente, è possibile creare comandi iterati per i profili e le combinazioni di colori.</span><span class="sxs-lookup"><span data-stu-id="8feab-126">Currently, you can create iterable commands for your profiles and color schemes.</span></span> <span data-ttu-id="8feab-127">In fase di esecuzione, questi comandi verranno espansi a un comando per ogni oggetto del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="8feab-127">At runtime, these commands will be expanded to one command for each of the objects of the given type.</span></span>

<span data-ttu-id="8feab-128">È attualmente possibile eseguire l'iterazione delle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="8feab-128">You can currently iterate over the following properties:</span></span>

| `iterateOn` | <span data-ttu-id="8feab-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8feab-129">Property</span></span> | <span data-ttu-id="8feab-130">Sintassi delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8feab-130">Property syntax</span></span> |
| ----------- | -------- | --------------- |
| `profiles` | `name` | `"name": "${profile.name}"` |
| `profiles` | `icon` | `"icon": "${profile.icon}"` |
| `schemes` | `name` | `"name": "${scheme.name}"` |

### <a name="example"></a><span data-ttu-id="8feab-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="8feab-131">Example</span></span>

<span data-ttu-id="8feab-132">Creare un nuovo comando TAB per ogni profilo.</span><span class="sxs-lookup"><span data-stu-id="8feab-132">Create a new tab command for each profile.</span></span>

![Comandi Windows Terminal iterable](./images/command-palette-iterable-commands.gif)

```json
{
    "name": "New tab",
    "commands": [
        {
            "iterateOn": "profiles",
            "icon": "${profile.icon}",
            "name": "${profile.name}",
            "command": { "action": "newTab", "profile": "${profile.name}" }
        }
    ]
}
```

<span data-ttu-id="8feab-134">Nell'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="8feab-134">In the above example:</span></span>

- <span data-ttu-id="8feab-135">`"iterateOn": "profiles"` genererà un comando per ogni profilo.</span><span class="sxs-lookup"><span data-stu-id="8feab-135">`"iterateOn": "profiles"` will generate a command for each profile.</span></span>
- <span data-ttu-id="8feab-136">In fase di esecuzione, il terminale sostituirà `${profile.icon}` con l'icona di ogni profilo e `${profile.name}` con il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="8feab-136">At runtime, the terminal will replace `${profile.icon}` with each profile's icon and `${profile.name}` with each profile's name.</span></span>

<span data-ttu-id="8feab-137">Se si disponesse di tre profili:</span><span class="sxs-lookup"><span data-stu-id="8feab-137">If you had three profiles:</span></span>

```json
"profiles": [
    { "name": "Command Prompt", "icon": null },
    { "name": "PowerShell", "icon": "C:\\path\\to\\icon.png" },
    { "name": "Ubuntu", "icon": null },
]
```

<span data-ttu-id="8feab-138">Il comando precedente si comporterebbe come i tre comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8feab-138">The above command would behave like the following three commands:</span></span>

```json
{
    "name": "New tab...",
    "commands": [
        {
            "icon": null,
            "name": "Command Prompt",
            "command": { "action": "newTab", "profile": "Command Prompt" }
        },
        {
            "icon": "C:\\path\\to\\icon",
            "name": "PowerShell",
            "command": { "action": "newTab", "profile": "PowerShell" }
        },
        {
            "icon": null,
            "name": "Ubuntu",
            "command": { "action": "newTab", "profile": "Ubuntu" }
        }
    ]
}
```

## <a name="hiding-a-command"></a><span data-ttu-id="8feab-139">Nascondere un comando</span><span class="sxs-lookup"><span data-stu-id="8feab-139">Hiding a command</span></span>

<span data-ttu-id="8feab-140">Se si vuole che un comando nell'elenco dei tasti di scelta delle chiavi non venga visualizzato nel riquadro comandi, è possibile nasconderlo impostando `name` su `null` .</span><span class="sxs-lookup"><span data-stu-id="8feab-140">If you would like to keep a command in your key bindings list but not have it appear in the command palette, you can hide it by setting its `name` to `null`.</span></span> <span data-ttu-id="8feab-141">Nell'esempio seguente viene nascosta l'azione "nuova scheda" dal riquadro comandi.</span><span class="sxs-lookup"><span data-stu-id="8feab-141">The example below hides the "New tab" action from the command palette.</span></span>

```json
{ "name": null, "command": "newTab", "keys": "ctrl+shift+t" }
```
