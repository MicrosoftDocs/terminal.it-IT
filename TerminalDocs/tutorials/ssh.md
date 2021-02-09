---
title: Terminale Windows - SSH
description: Questa esercitazione illustra come configurare una connessione SSH in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.openlocfilehash: 9cbbd4411c1890b673d1dd2bed88bbd42cf0f6f4
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974862"
---
# <a name="tutorial-ssh-in-windows-terminal"></a>Esercitazione: SSH in Terminale Windows

Windows 10 include un client SSH predefinito che è possibile usare in Terminale Windows.

Questa esercitazione illustra come configurare un profilo che usa SSH in Terminale Windows.

## <a name="create-a-profile"></a>Creare un profilo

Per avviare una sessione SSH al prompt dei comandi, esegui `ssh user@machine`. Ti verrà richiesto di immettere la password. È possibile creare un profilo terminale di Windows che esegue questa operazione all'avvio aggiungendo l' `commandline` impostazione a un profilo nel settings.jssu file all'interno `list` di oggetti profilo.

```json
{
  "name": "user@machine ssh profile",
  "commandline": "ssh user@machine",
}
```

Per altre informazioni, vedere:

* [Profilo terminale Windows-impostazioni generali](./../customize-settings/profile-general.md)

## <a name="specify-starting-directory"></a>Specificare la directory iniziale

Per specificare la directory iniziale per una sessione SSH richiamata da Terminale Windows, è possibile usare questo comando:

```json
{
  "commandline": "ssh -t bob@foo \"cd /data/bob && exec bash -l\""
}
```

Il flag `-t` forza l'allocazione del pseudo-terminale. Questa funzionalità può essere usata per eseguire programmi arbitrari basati su schermo in un computer remoto, ad esempio per l'implementazione di servizi di menu. Sarà necessario usare le virgolette doppie di escape perché le derivate di Bourne shell non eseguono analisi aggiuntive per una stringa racchiusa tra virgolette singole.

Per altre informazioni, vedere:

* [Problema di GH: Come specificare la directory iniziale per una sessione SSH?](https://github.com/MicrosoftDocs/terminal/issues/25)
* [StackOverflow: Come usare SSH per accedere direttamente a una directory specifica?](https://stackoverflow.com/questions/626533/how-can-i-ssh-directly-to-a-particular-directory)

## <a name="resources"></a>Risorse

* [Come abilitare e usare i nuovi comandi SSH predefiniti di Windows 10](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
