---
title: Risoluzione dei problemi di Terminale Windows
description: Informazioni sulle correzioni per i problemi comuni di Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 29d3ce72210c30fcbf38393d733c6157670465bb
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415876"
---
# <a name="troubleshooting-in-windows-terminal"></a>Risoluzione dei problemi di Terminale Windows

Questa guida descrive alcuni errori e problemi comuni che possono verificarsi in Terminale Windows.

## <a name="set-your-wsl-distribution-to-start-in-the-home--directory-when-launched"></a>Impostare la distribuzione di WSL in modo che venga avviata nella home directory `~`

Per impostazione predefinita, la directory `startingDirectory` di un profilo è `%USERPROFILE%` (`C:\Users\<YourUsername>`), ovvero un percorso di Windows. Per WSL, tuttavia, è consigliabile usare invece il percorso della home directory WSL. `startingDirectory` accetta solo un percorso di tipo Windows, quindi l'impostazione per l'avvio in una distribuzione WSL richiede un prefisso.

A partire da Windows 10 versione 1903, puoi gestire i file system delle distribuzioni WSL usando il prefisso `\\wsl$\`. Per qualsiasi distribuzione WSL con il nome `DistroName`, usa `\\wsl$\DistroName` come percorso di Windows che punta alla radice del file system della distribuzione.

Ad esempio, l'impostazione seguente avvierà la distribuzione "Ubuntu-18.04" nel percorso file della home directory:

```json
{
    "name": "Ubuntu-18.04",
    "commandline" : "wsl -d Ubuntu-18.04",
    "startingDirectory" : "//wsl$/Ubuntu-18.04/home/<Your Ubuntu Username>",
}
```

## <a name="setting-the-tab-title"></a>Impostazione del titolo della scheda

Per fare in modo che il titolo della scheda venga impostato automaticamente dalla shell, [vedi questa esercitazione](./tutorials/tab-title.md). Se vuoi impostare un titolo personalizzato per la scheda, apri il file settings.json e segui questa procedura:

1. Nel profilo di una riga di comando a scelta aggiungi `"suppressApplicationTitle": true` per eliminare gli eventi di modifica del titolo che vengono inviati dalla shell. Se aggiungi *solo* questa impostazione al profilo, il titolo della scheda verrà impostato sul nome del profilo.

2. Se vuoi impostare un titolo di scheda personalizzato e non il nome del profilo, aggiungi `"tabTitle": "TITLE"`. Sostituisci "TITLE" con il titolo preferito per la scheda.

## <a name="command-line-arguments-in-powershell"></a>Argomenti della riga di comando in PowerShell

Per informazioni sul funzionamento degli argomenti della riga di comando in PowerShell, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).

## <a name="command-line-arguments-in-wsl"></a>Argomenti della riga di comando in WSL

Per informazioni sul funzionamento degli argomenti della riga di comando in WSL, vedi la [pagina Argomenti della riga di comando](./command-line-arguments.md).

## <a name="problem-setting-startingdirectory"></a>Problema con l'impostazione di `startingDirectory`

Se l'impostazione di `startingDirectory` viene ignorata nel profilo, verifica prima di tutto che la sintassi del file settings.json sia corretta. Per semplificare la verifica della sintassi, `"$schema": "https://aka.ms/terminal-profiles-schema"` viene inserito automaticamente. Alcune applicazioni, ad esempio [Visual Studio Code](https://code.visualstudio.com/download), possono usare lo schema inserito per convalidare il file JSON durante le modifiche.

Se le impostazioni sono corrette, è possibile che sia in esecuzione uno script di avvio che imposta separatamente la directory iniziale del terminale. PowerShell, ad esempio, prevede un proprio concetto separato dei profili. Se cambi qui la directory iniziale, questa impostazione avrà la precedenza su quella definita in Terminale Windows.

In alternativa, se esegui uno script usando l'impostazione del profilo `commandline`, è possibile che stia impostando qui la posizione. Analogamente ai profili PowerShell, i comandi hanno la precedenza sull'impostazione del profilo `startingDirectory`.

Lo scopo di `startingDirectory` è avviare una nuova istanza di Terminale Windows nella directory specificata. Se il terminale esegue qualsiasi codice che cambia la directory, potrebbe essere questa la causa del problema.

## <a name="ctrl-does-not-increase-the-font-size"></a>CTRL+= non aumenta le dimensioni del carattere

Se usi un layout di tastiera tedesco, potresti riscontrare questo problema. La combinazione <kbd>CTRL+=</kbd> viene deserializzata come <kbd>CTRL+MAIUSC+0</kbd> se il layout di tastiera principale è impostato sul tedesco. Si tratta del mapping corretto per le tastiere tedesche.

Ancora più importante, l'app non riceve mai la sequenza di tasti <kbd>CTRL+MAIUSC+0</kbd>. Il motivo è che la combinazione <kbd>CTRL+MAIUSC+0</kbd> è riservata da Windows se sono attivi più layout di tastiera.

Se vuoi disabilitare questa funzionalità per il corretto funzionamento di `Ctrl+=`, segui le istruzioni su come cambiare i tasti di scelta rapida per sostituire il layout della tastiera in Windows 10 in questo [post di blog](https://winaero.com/blog/change-hotkeys-switch-keyboard-layout-windows-10/).

Imposta l'opzione 'Cambia layout di tastiera' su 'Non assegnato' (o su una combinazione senza <kbd>CTRL+MAIUSC</kbd>), quindi seleziona **OK** e poi **Applica**. La combinazione di tasti <kbd>CTRL+MAIUSC+0</kbd> dovrebbe ora funzionare e viene passata al terminale.

Se al contrario usi questa funzionalità di tasti di scelta rapida per più lingue di input, puoi [configurare combinazioni di tasti personalizzate](./customize-settings/key-bindings.md) nel file settings.json.
