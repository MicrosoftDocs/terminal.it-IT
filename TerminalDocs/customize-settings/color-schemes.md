---
title: Terminale Windows - Combinazioni colori
description: Informazioni su come creare combinazioni colori per Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 7/28/2020
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: aa914d1bd92a2afab307142150f6fa096c2936c7
ms.sourcegitcommit: ebbf6cc7aaf26ebe4d96d87d4478e94357025a71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/19/2020
ms.locfileid: "92174579"
---
# <a name="color-schemes-in-windows-terminal"></a>Combinazioni colori in Terminale Windows

Il terminale di Windows consente di definire le proprie combinazioni di colori usando gli schemi predefiniti predefiniti oppure creando uno schema personalizzato da zero. Per modificare gli schemi, è necessario modificare il settings.jssu file in un editor, ad esempio [Visual Studio Code](https://code.visualstudio.com/).

## <a name="switching-to-a-different-color-scheme"></a>Passare a una combinazione di colori diversa

Avviare Windows Terminal, quindi selezionare la piccola freccia rivolta verso il basso nella barra del titolo. Verrà aperto un menu a discesa che elenca i profili disponibili nel sistema (ad esempio, Windows PowerShell e prompt dei comandi) e altre opzioni. Selezionare **Settings (impostazioni**). l'settings.jsnel file si aprirà nell'editor di testo predefinito.

In questo file è possibile definire diverse opzioni per finestra o per profilo. Per dimostrare, modificare la combinazione di colori per il profilo del prompt dei comandi.

Esaminare il file JSON fino a trovare la sezione che include:

```json
"commandline": "cmd.exe",
"hidden": false
```

Modificarlo in lettura:

```json
"commandline": "cmd.exe",
"hidden": false,
"colorScheme": "Tango Light"
```

Si noti la virgola aggiuntiva nella riga **nascosta** . Dopo aver salvato il file, il terminale di Windows aggiornerà tutte le finestre aperte. Aprire una scheda del prompt dei comandi, se non è già stato fatto, e si noterà immediatamente che i colori sono stati modificati.

## <a name="creating-your-own-color-scheme"></a>Creazione di una combinazione colori personalizzata

Lo schema "Tango Light" è incluso come opzione predefinita, ma è possibile creare un proprio schema da zero o copiando uno schema esistente.

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

Le combinazioni colori di Terminale Windows sono incluse nel file defaults.json. Per accedervi, tieni premuto <kbd>alt</kbd> mentre fai clic sulla voce di menu Impostazioni. 


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

### <a name="tango-dark"></a>Tango Dark

![Terminale Windows - Combinazione colori Tango Dark](./../images/tango-dark-color-scheme.png)

### <a name="tango-light"></a>Tango Light

![Terminale Windows - Combinazione colori Tango Light](./../images/tango-light-color-scheme.png)


## <a name="more-schemes"></a>Altri schemi

Per altri schemi, vedere la sezione [raccolta di terminali personalizzati](../custom-terminal-gallery/custom-schemes.md) .
