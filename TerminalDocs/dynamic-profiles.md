---
title: Profili dinamici di Terminale Windows
description: Informazioni sui profili dinamici in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: concept
ms.service: terminal
ms.openlocfilehash: 7ab394cea84eaab08b14edf859ef0cd9390d7267
ms.sourcegitcommit: a489b75e14e2c123bf6b4ac2a15ff85b515564be
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/18/2020
ms.locfileid: "83553193"
---
# <a name="dynamic-profiles-in-windows-terminal"></a>Profili dinamici in Terminale Windows

Terminale Windows creerà automaticamente il sottosistema Windows per Linux (WSL) e i profili di PowerShell se queste shell sono installate nel computer. In questo modo è più facile avere tutte le shell incluse nel terminale senza dover individuare i relativi file eseguibili. Questi profili vengono generati con la proprietà `source`, che indica al terminale dove trovare il file eseguibile appropriato.

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
