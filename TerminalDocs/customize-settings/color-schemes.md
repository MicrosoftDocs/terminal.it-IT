---
title: Terminale Windows - Combinazioni colori
description: Informazioni su come creare combinazioni colori per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 9f7e6133a08a21c3b77689cd8dce32dacbf80351
ms.sourcegitcommit: d8e23557224bc50a82a36dc80ac68b9d11dfdde9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720137"
---
# <a name="color-schemes-in-windows-terminal"></a>Combinazioni colori in Terminale Windows

## <a name="creating-your-own-color-scheme"></a>Creazione di una combinazione colori personalizzata

È possibile definire le combinazioni di colori nella matrice `schemes` del file settings.json. Le combinazioni vengono scritte nel formato seguente:

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

Ogni impostazione, eccetto `name`, accetta un colore in formato stringa esadecimale, ovvero `"#rgb"` o `"#rrggbb"`. Le impostazioni `cursorColor` e `selectionBackground` sono facoltative.

<br />

___

## <a name="included-color-schemes"></a>Combinazioni colori incluse

Le combinazioni colori di Terminale Windows sono incluse nel file defaults.json. Per accedervi, tieni premuto <kbd>alt</kbd> mentre fai clic sulla voce di menu Impostazioni. Per impostare una combinazione colori all'interno di uno dei profili della riga di comando, aggiungere la proprietà `colorScheme` specificando come valore l'impostazione `name` della combinazione colori.

```json
"colorScheme": "COLOR SCHEME NAME"
```

### <a name="campbell"></a>Campbell

![Terminale Windows - Combinazione colori Campbell](./../images/campbell-color-scheme.png)

### <a name="campbell-powershell"></a>Campbell Powershell

![Terminale Windows - Combinazione colori Campbell Powershell](./../images/campbell-powershell-color-scheme.png)

### <a name="vintage"></a>Vintage

![Terminale Windows - Combinazione colori Vintage](./../images/vintage-color-scheme.png)

### <a name="one-half-dark"></a>One Half Dark

![Terminale Windows - Combinazione colori One Half Dark](./../images/one-half-dark-color-scheme.png)

### <a name="one-half-light"></a>One Half Light

![Terminale Windows - Combinazione colori One Half Light](./../images/one-half-light-color-scheme.png)

### <a name="solarized-dark"></a>Solarized Dark

![Terminale Windows - Combinazione colori Solarized Dark](./../images/solarized-dark-color-scheme.png)

### <a name="solarized-light"></a>Solarized Light

![Terminale Windows - Combinazione colori Solarized Light](./../images/solarized-light-color-scheme.png)

### <a name="tango-dark"></a>Tango Dark

![Terminale Windows - Combinazione colori Tango Dark](./../images/tango-dark-color-scheme.png)

### <a name="tango-light"></a>Tango Light

![Terminale Windows - Combinazione colori Tango Light](./../images/tango-light-color-scheme.png)
