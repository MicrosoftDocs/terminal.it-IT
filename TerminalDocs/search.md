---
title: Ricerca in Terminale Windows
description: Informazioni su come eseguire ricerche in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 09/22/2020
ms.topic: how-to
ms.openlocfilehash: 6e7748e6898ab2a6c7a78d8833179fb694ef66f2
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988800"
---
# <a name="how-to-search-in-windows-terminal"></a>Come eseguire ricerche in Terminale Windows

Terminale Windows include una funzionalità di ricerca che consente di cercare una parola chiave specifica nel buffer di testo. Questa funzionalità è utile per trovare un comando eseguito in precedenza o un nome file specifico.

## <a name="using-search"></a>Uso della ricerca

Per impostazione predefinita, puoi aprire la finestra di dialogo di ricerca premendo <kbd>CTRL+MAIUSC+F</kbd>. Una volta aperta, digita la parola chiave da cercare nella casella di testo e premi <kbd>INVIO</kbd> per avviare la ricerca.

![Screenshot della ricerca in Terminale Windows](./images/search.png)
_Configurazione: [Powerline in PowerShell](./custom-terminal-gallery/powerline-in-powershell.md)_

## <a name="directional-search"></a>Ricerca direzionale

Per impostazione predefinita, il terminale eseguirà la ricerca dal basso verso l'alto nel buffer di testo. Puoi cambiare la direzione della ricerca selezionando una delle frecce nella finestra di dialogo.

![Screenshot della ricerca direzionale in Terminale Windows](./images/search-direction.gif)

## <a name="case-match-search"></a>Ricerca con corrispondenza tra maiuscole e minuscole

Per restringere i risultati della ricerca, puoi aggiungere la corrispondenza tra maiuscole e minuscole come opzione. Per attivare la corrispondenza tra maiuscole e minuscole, seleziona l'apposito pulsante. I risultati visualizzati corrisponderanno solo alla parola chiave immessa con la combinazione specifica di maiuscole e minuscole.

![Screenshot della ricerca di Terminale Windows con corrispondenza tra maiuscole e minuscole](./images/search-case-match.gif)

## <a name="searching-within-panes"></a>Ricerca all'interno dei riquadri

La finestra di dialogo di ricerca funziona anche con i [riquadri](./panes.md). In un riquadro con lo stato attivo puoi aprire la finestra di dialogo di ricerca, che verrà visualizzata nel riquadro in alto a destra. Quindi, qualsiasi parola chiave immessa mostrerà solo i risultati trovati all'interno di tale riquadro.

![Screenshot della ricerca nei riquadri in Terminale Windows](./images/search-panes.gif)

## <a name="customize-the-search-key-binding"></a>Personalizzare la combinazione di tasti della ricerca

Puoi aprire la finestra di dialogo di ricerca con qualsiasi combinazione di tasti di scelta rapida. Per cambiare la combinazione di tasti della ricerca, apri il file settings.json e cerca il comando `find`. Per impostazione predefinita, questo comando è impostato su `ctrl+shift+f`.

```json
// Press ctrl+shift+f to open the search box
        { "command": "find", "keys": "ctrl+shift+f" },
```

Puoi ad esempio sostituire "CTRL+MAIUSC+F" con "CTRL+F", in modo che premendo `ctrl+f` venga visualizzata la finestra di dialogo di ricerca.

Per ulteriori informazioni sui tasti di scelta, visitare la [pagina azioni](./customize-settings/actions.md).
