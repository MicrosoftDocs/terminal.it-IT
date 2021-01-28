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
# <a name="how-to-use-the-command-palette-in-windows-terminal"></a>Come usare il riquadro comandi nel terminale di Windows

Il riquadro comandi consente di visualizzare le azioni che è possibile eseguire nel terminale di Windows. Altre informazioni sulla modalità di definizione delle azioni sono disponibili nella [pagina azioni](./customize-settings/actions.md).

## <a name="invoking-the-command-palette"></a>Richiamo del riquadro comandi

È possibile richiamare il riquadro comandi digitando <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>P</kbd>. Questa operazione può essere personalizzata aggiungendo il `commandPalette` comando alle associazioni di tasti.

```json
{ "command": "commandPalette", "keys": "ctrl+shift+p" }
```

## <a name="command-line-mode"></a>Modalità riga di comando

Se si desidera immettere un `wt` comando nel riquadro comandi, è possibile eliminare il `>` carattere nella casella di testo. Il comando verrà eseguito `wt` nella finestra corrente. Altre informazioni sui `wt` comandi sono disponibili nella [pagina argomenti della riga di comando](./command-line-arguments.md).

![Modalità riga di comando di Windows Terminal](./images/command-palette-command-line-mode.gif)

È possibile aggiungere un'associazione di tasti personalizzata per richiamare direttamente il riquadro comandi nella modalità riga di comando.

```json
{ "command": "commandPalette", "launchMode": "commandLine", "keys": "" }
```

> [!IMPORTANT]
> L'impostazione `"launchMode"` è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).

## <a name="adding-an-icon-to-a-command"></a>Aggiunta di un'icona a un comando

Facoltativamente, è possibile aggiungere un'icona a un comando definito nel settings.jsin che viene visualizzato nel riquadro comandi. Questa operazione può essere eseguita aggiungendo la `icon` proprietà all'azione. Le icone possono essere un percorso di un'immagine, un simbolo di [SEGOE MDL2 asset](https://docs.microsoft.com/windows/uwp/design/style/segoe-ui-symbol-font)o qualsiasi carattere, incluso emoji.

```json
{ "icon": "C:\\Images\\my-icon.png", "name": "New tab", "command": "newTab", "keys": "ctrl+shift+t" },
{ "icon": "\uE756", "name": "New tab", "command": "newTab", "keys": "ctrl+shift+t" },
{ "icon": "⚡", "name": "New tab", "command": "newTab", "keys": "ctrl+shift+t" }
```

## <a name="nested-commands"></a>Comandi annidati

I comandi annidati consentono di raggruppare più comandi sotto un elemento nel riquadro comandi. Nell'esempio seguente vengono raggruppati i comandi di ridimensionamento dei tipi di carattere sotto un elemento del riquadro comandi denominato "modifica dimensioni carattere...".

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

## <a name="iterable-commands"></a>Comandi iterable

I comandi iterable consentono di creare più comandi contemporaneamente, generati da altri oggetti definiti nelle impostazioni. Attualmente, è possibile creare comandi iterati per i profili e le combinazioni di colori. In fase di esecuzione, questi comandi verranno espansi a un comando per ogni oggetto del tipo specificato.

È attualmente possibile eseguire l'iterazione delle proprietà seguenti:

| `iterateOn` | Proprietà | Sintassi delle proprietà |
| ----------- | -------- | --------------- |
| `profiles` | `name` | `"name": "${profile.name}"` |
| `profiles` | `icon` | `"icon": "${profile.icon}"` |
| `schemes` | `name` | `"name": "${scheme.name}"` |

### <a name="example"></a>Esempio

Creare un nuovo comando TAB per ogni profilo.

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

Nell'esempio precedente:

- `"iterateOn": "profiles"` genererà un comando per ogni profilo.
- In fase di esecuzione, il terminale sostituirà `${profile.icon}` con l'icona di ogni profilo e `${profile.name}` con il nome del profilo.

Se si disponesse di tre profili:

```json
"profiles": [
    { "name": "Command Prompt", "icon": null },
    { "name": "PowerShell", "icon": "C:\\path\\to\\icon.png" },
    { "name": "Ubuntu", "icon": null },
]
```

Il comando precedente si comporterebbe come i tre comandi seguenti:

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

## <a name="hiding-a-command"></a>Nascondere un comando

Se si vuole che un comando nell'elenco dei tasti di scelta delle chiavi non venga visualizzato nel riquadro comandi, è possibile nasconderlo impostando `name` su `null` . Nell'esempio seguente viene nascosta l'azione "nuova scheda" dal riquadro comandi.

```json
{ "name": null, "command": "newTab", "keys": "ctrl+shift+t" }
```
