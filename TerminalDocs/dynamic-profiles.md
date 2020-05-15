---
title: Profili dinamici di Terminale Windows
description: Informazioni sui profili dinamici in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: concept
ms.service: terminal
ms.openlocfilehash: 9c54dc2182584873d9d0c1358083d5142d07ef48
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416126"
---
# <a name="dynamic-profiles-in-windows-terminal"></a>Profili dinamici in Terminale Windows

Terminale Windows creerà automaticamente il sottosistema Windows per Linux (WSL) e i profili di PowerShell se hai installato queste shell nel computer. In questo modo è più facile avere tutte le shell incluse nel terminale senza dover individuare i relativi file eseguibili. Questi profili vengono generati con la proprietà `source`, che indica al terminale dove trovare il file eseguibile appropriato.

Dopo l'installazione, il terminale imposterà PowerShell come profilo predefinito. Per informazioni su come cambiare il profilo predefinito, vedi la [pagina delle impostazioni globali](./customize-settings/global-settings.md).

![Profili dinamici di Terminale Windows](./images/dynamic-profiles.png)
_Configurazione: [tema chiaro](./custom-terminal-gallery/frosted-glass-theme.md)_

## <a name="installing-a-new-shell-after-installing-windows-terminal"></a>Installazione di una nuova shell dopo l'installazione di Terminale Windows

Dopo l'installazione di una nuova shell, indipendentemente dal fatto che venga eseguita prima o dopo l'installazione del terminale, verrà creato un nuovo profilo corrispondente.

## <a name="hide-a-profile"></a>Nascondere un profilo

Per nascondere un profilo nel menu a discesa del terminale, aggiungi la proprietà `hidden` all'oggetto profilo nel file settings.json e impostala su `true`.

```json
"hidden": true
```

Se elimini un profilo creato dinamicamente, il terminale lo rigenererà automaticamente e lo sostituirà nel file settings.json.

## <a name="prevent-a-profile-from-being-generated"></a>Impedire la generazione di un profilo

Per impedire la generazione di un profilo dinamico, puoi aggiungere il generatore di profili alla matrice `disabledProfileSources` nelle impostazioni globali. Per altre informazioni su questa impostazione, vedi la [pagina delle impostazioni globali](./customize-settings/global-settings.md#disable-dynamic-profiles).

```json
"disabledProfileSources": ["Windows.Terminal.Wsl", "Windows.Terminal.Azure", "Windows.Terminal.PowershellCore"]
```
