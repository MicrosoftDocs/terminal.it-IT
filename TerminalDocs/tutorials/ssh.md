---
title: Terminale Windows - SSH
description: Questa esercitazione illustra come configurare una connessione SSH in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: c418460cd47935ed8b8eb57ebdb89322d543a20e
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415866"
---
# <a name="tutorial-ssh-in-windows-terminal"></a>Esercitazione: SSH in Terminale Windows

Windows 10 include un client SSH predefinito che è possibile usare in Terminale Windows.

Questa esercitazione illustra come configurare un profilo che usa SSH in Terminale Windows.

## <a name="create-a-profile"></a>Creare un profilo

Per avviare una sessione SSH al prompt dei comandi, esegui `ssh user@machine`. Ti verrà richiesto di immettere la password. Per creare un profilo di Terminale Windows che esegue questa operazione all'avvio, aggiungi l'impostazione `commandline` a un profilo nel file settings.json.

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="resources"></a>Risorse

* [Come abilitare e usare i nuovi comandi SSH predefiniti di Windows 10](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
