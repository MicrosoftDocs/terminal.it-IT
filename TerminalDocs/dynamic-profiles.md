---
title: Profili dinamici di Terminale Windows
description: Informazioni sui profili dinamici in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: concept
ms.openlocfilehash: 97321776506e2616c48922aaf9d50001641fa565
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "98980954"
---
# <a name="dynamic-profiles-in-windows-terminal"></a>Profili dinamici in Terminale Windows

Terminale Windows creerà automaticamente il sottosistema Windows per Linux (WSL) e i profili di PowerShell se queste shell sono installate nel computer. In questo modo è più facile avere tutte le shell incluse nel terminale senza dover individuare i relativi file eseguibili. Questi profili vengono generati con la proprietà `source`, che indica al terminale dove trovare il file eseguibile appropriato.

Dopo l'installazione, il terminale imposterà PowerShell come profilo predefinito. Per informazioni su come modificare il profilo predefinito, visitare la [pagina di avvio](./customize-settings/startup.md).

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

Per impedire la generazione di un profilo dinamico, puoi aggiungere il generatore di profili alla matrice `disabledProfileSources` nelle impostazioni globali. Per altre informazioni su questa impostazione, vedi la [pagina delle impostazioni globali](./customize-settings/startup.md#disable-dynamic-profiles).

```json
"disabledProfileSources": ["Windows.Terminal.Wsl", "Windows.Terminal.Azure", "Windows.Terminal.PowershellCore"]
```
