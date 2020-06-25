---
title: Terminale Windows - SSH
description: Questa esercitazione illustra come configurare una connessione SSH in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: 02f4704b81cd0d287c207f0138ef27c537929711
ms.sourcegitcommit: bae07a8dd2010a95de4d53b1465abe226e4ad18e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/26/2020
ms.locfileid: "83856339"
---
# <a name="tutorial-ssh-in-windows-terminal"></a>Esercitazione: SSH in Terminale Windows

Windows 10 include un client SSH predefinito che è possibile usare in Terminale Windows.

Questa esercitazione illustra come configurare un profilo che usa SSH in Terminale Windows.

## <a name="create-a-profile"></a>Creare un profilo

Per avviare una sessione SSH al prompt dei comandi, esegui `ssh user@machine`. Ti verrà richiesto di immettere la password. Per creare un profilo di Terminale Windows che esegue questa operazione all'avvio, aggiungi l'impostazione `commandline` a un profilo nel file settings.json.

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="specify-starting-directory"></a>Specificare la directory iniziale

Per specificare la directory iniziale per una sessione SSH richiamata da Terminale Windows, è possibile usare questo comando:

```bash
"commandline": "ssh -t bob@foo \"cd /data/bob && exec bash -l\""
```

Il flag `-t` forza l'allocazione del pseudo-terminale. Questa funzionalità può essere usata per eseguire programmi arbitrari basati su schermo in un computer remoto, ad esempio per l'implementazione di servizi di menu. Sarà necessario usare le virgolette doppie di escape perché le derivate di Bourne shell non eseguono analisi aggiuntive per una stringa racchiusa tra virgolette singole.

Per altre informazioni, vedere:

* [Problema di GH: Come specificare la directory iniziale per una sessione SSH?](https://github.com/MicrosoftDocs/terminal/issues/25)
* [StackOverflow: Come usare SSH per accedere direttamente a una directory specifica?](https://stackoverflow.com/questions/626533/how-can-i-ssh-directly-to-a-particular-directory)

## <a name="resources"></a>Risorse

* [Come abilitare e usare i nuovi comandi SSH predefiniti di Windows 10](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
