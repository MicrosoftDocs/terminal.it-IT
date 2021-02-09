---
title: Risoluzione dei problemi di Terminale Windows
description: Informazioni sulle correzioni per i problemi comuni di Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 1/28/2021
ms.topic: overview
ms.localizationpriority: high
ms.openlocfilehash: da843d477659a17f28be8df27c122e4e8fbfe3a6
ms.sourcegitcommit: 85519c60d559160a7847cf99971b90eb5cb94b4e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "99974882"
---
# <a name="troubleshooting-in-windows-terminal"></a>Risoluzione dei problemi di Terminale Windows

Questa guida descrive alcuni errori e problemi comuni che possono verificarsi in Terminale Windows.

## <a name="open-the-settings-ui"></a>Aprire l'interfaccia utente delle impostazioni

Al momento, l'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview). Per aprire l'interfaccia utente delle impostazioni, è necessario aggiungere l' `"openSettings"` azione alla `"actions"` matrice per aprirla con il riquadro comandi o la tastiera.

```
{ "command": { "action": "openSettings", "target": "settingsUI" }, "keys": "ctrl+shift+," },
```

## <a name="set-your-wsl-distribution-to-start-in-the-home--directory-when-launched"></a>Impostare la distribuzione di WSL in modo che venga avviata nella home directory `~`

Per impostazione predefinita, la directory `startingDirectory` di un profilo è `%USERPROFILE%` (`C:\Users\<YourUsername>`), ovvero un percorso di Windows. Per WSL, tuttavia, è consigliabile usare invece il percorso della home directory WSL. `startingDirectory` accetta solo un percorso di tipo Windows, quindi l'impostazione per l'avvio in una distribuzione WSL richiede un prefisso.

A partire da Windows 10 versione 1903, puoi gestire i file system delle distribuzioni WSL usando il prefisso `\\wsl$\`. Per qualsiasi distribuzione WSL con il nome `DistroName`, usa `\\wsl$\DistroName` come percorso di Windows che punta alla radice del file system della distribuzione.

Ad esempio, l'impostazione seguente avvierà la distribuzione "Ubuntu-18.04" nel percorso file della home directory:

```json
{
    "name": "Ubuntu-18.04",
    "commandline" : "wsl -d Ubuntu-18.04",
    "startingDirectory" : "//wsl$/Ubuntu-18.04/home/<Your Ubuntu Username>"
}
```

## <a name="setting-the-tab-title"></a>Impostazione del titolo della scheda

Per fare in modo che il titolo della scheda venga impostato automaticamente dalla shell, [vedi questa esercitazione](./tutorials/tab-title.md). Se vuoi impostare un titolo personalizzato per la scheda, apri il file settings.json e segui questa procedura:

1. Nel profilo di una riga di comando a scelta aggiungi `"suppressApplicationTitle": true` per eliminare gli eventi di modifica del titolo che vengono inviati dalla shell. Se aggiungi *solo* questa impostazione al profilo, il titolo della scheda verrà impostato sul nome del profilo.

2. Se vuoi impostare un titolo di scheda personalizzato e non il nome del profilo, aggiungi `"tabTitle": "TITLE"`. Sostituisci "TITLE" con il titolo preferito per la scheda.

## <a name="command-line-arguments-in-powershell"></a>Argomenti della riga di comando in PowerShell

Per informazioni sul funzionamento degli argomenti della riga di comando in PowerShell, vedere la [pagina Argomenti della riga di comando](./command-line-arguments.md).

## <a name="command-line-arguments-in-wsl"></a>Argomenti della riga di comando in WSL

Per informazioni sul funzionamento degli argomenti della riga di comando in WSL, vedere la [pagina Argomenti della riga di comando](./command-line-arguments.md).

## <a name="problem-setting-startingdirectory"></a>Problema con l'impostazione di `startingDirectory`

Se l'impostazione di `startingDirectory` viene ignorata nel profilo, verifica prima di tutto che la sintassi del file settings.json sia corretta. Per semplificare la verifica della sintassi, `"$schema": "https://aka.ms/terminal-profiles-schema"` viene inserito automaticamente. Alcune applicazioni, ad esempio [Visual Studio Code](https://code.visualstudio.com/download), possono usare lo schema inserito per convalidare il file JSON durante le modifiche.

Se le impostazioni sono corrette, è possibile che sia in esecuzione uno script di avvio che imposta separatamente la directory iniziale del terminale. PowerShell, ad esempio, prevede un proprio concetto separato dei profili. Se cambi qui la directory iniziale, questa impostazione avrà la precedenza su quella definita in Terminale Windows.

In alternativa, se esegui uno script usando l'impostazione del profilo `commandline`, è possibile che stia impostando qui la posizione. Analogamente ai profili PowerShell, i comandi hanno la precedenza sull'impostazione del profilo `startingDirectory`.

Lo scopo di `startingDirectory` è avviare una nuova istanza di Terminale Windows nella directory specificata. Se il terminale esegue qualsiasi codice che cambia la directory, potrebbe essere questa la causa del problema.

## <a name="deleting-a-profile"></a>Eliminazione di un profilo

Per impostazione predefinita, il terminale di Windows viene fornito con PowerShell incorporato e un profilo del prompt dei comandi. Il terminale rileva automaticamente anche se sono installate altre applicazioni della riga di comando, ad esempio PowerShell core, distribuzioni WSL (Ubuntu, Debian e così via) e Azure Cloud Shell. Questi tipi di profili generati automaticamente vengono chiamati "profili dinamici".

Per i profili predefiniti e dinamici, l'eliminazione del profilo dal settings.jssul file non lo rimuoverà dai profili. I profili predefiniti sono definiti in `defaults.json` , quindi sono sempre disponibili. I profili dinamici tenterà di creare uno stub JSON per il proprio profilo nel `settings.json` file ogni volta che un profilo non è già presente nel file.

L'unico modo per rimuovere effettivamente questi profili dall'elenco è "nasconderli". Per nascondere un profilo, aggiungere la proprietà `"hidden": true` al profilo.

## <a name="ctrl-does-not-increase-the-font-size"></a>CTRL+= non aumenta le dimensioni del carattere

Se usi un layout di tastiera tedesco, potresti riscontrare questo problema. La combinazione <kbd>CTRL+=</kbd> viene deserializzata come <kbd>CTRL+MAIUSC+0</kbd> se il layout di tastiera principale è impostato sul tedesco. Si tratta del mapping corretto per le tastiere tedesche.

Ancora più importante, l'app non riceve mai la sequenza di tasti <kbd>CTRL+MAIUSC+0</kbd>. Il motivo è che la combinazione <kbd>CTRL+MAIUSC+0</kbd> è riservata da Windows se sono attivi più layout di tastiera.

Se vuoi disabilitare questa funzionalità per il corretto funzionamento di `Ctrl+=`, segui le istruzioni su come cambiare i tasti di scelta rapida per sostituire il layout della tastiera in Windows 10 in questo [post di blog](https://winaero.com/blog/change-hotkeys-switch-keyboard-layout-windows-10/).

Imposta l'opzione 'Cambia layout di tastiera' su 'Non assegnato' (o su una combinazione senza <kbd>CTRL+MAIUSC</kbd>), quindi seleziona **OK** e poi **Applica**. La combinazione di tasti <kbd>CTRL+MAIUSC+0</kbd> dovrebbe ora funzionare e viene passata al terminale.

Se al contrario usi questa funzionalità di tasti di scelta rapida per più lingue di input, puoi [configurare combinazioni di tasti personalizzate](./customize-settings/actions.md) nel file settings.json.

## <a name="the-text-is-blurry"></a>Il testo è sfocato

Alcuni driver video e combinazioni di hardware non gestiscono lo scorrimento e/o le aree modificate senza sfocare i dati del frame precedente. Per ovviare a questo problema, è possibile aggiungere una combinazione di [queste impostazioni di rendering globali](./customize-settings/rendering.md) per ridurre la pressione esercitata sull'hardware dal renderer di testo del terminale.

## <a name="my-colors-look-strange-there-are-black-bars-on-my-screen"></a>I miei colori hanno un aspetto strano. Sono presenti barre nere sullo schermo.

> [!IMPORTANT]
> Si applica solo alla versione 1.2 + del terminale di Windows. Se si verificano problemi di colore nel terminale di Windows 1,0 o 1,1 o problemi che non vengono acquisiti qui, inviare un bug.

Windows Terminal 1,2 e versioni successive hanno migliorato la conoscenza di determinate impostazioni dei colori dell'applicazione. Grazie a questa migliore comprensione, è stato possibile rimuovere una serie di blocchi di compatibilità che hanno comportato un'esperienza utente insufficiente. Sfortunatamente, c'è un numero ridotto di applicazioni che possono riscontrare problemi.

Questo elemento di risoluzione dei problemi verrà mantenuto aggiornato con l'elenco dei problemi noti e delle relative soluzioni alternative.

### <a name="black-lines-in-powershell-51-6x-70"></a>Righe nere in PowerShell (5,1, 6. x, 7,0)

Quando il terminale è associato alla libreria di modifica della riga di PowerShell [PSReadline](https://www.powershellgallery.com/packages/PSReadLine), può creare linee nere sullo schermo. Queste aree non colorate si estendono sullo schermo oltre la richiesta, ovunque ci siano parametri del comando, stringhe o operatori.

PSReadline versione **2.0.3** è stata rilasciata e contiene una correzione per questo problema. Se si usa la versione provvisoria di PSReadline, si noti che una correzione non è ancora disponibile.

Per eseguire l'aggiornamento alla versione più recente di PSReadline, eseguire il comando seguente:

```powershell
Update-Module PSReadline
```

## <a name="why-are-my-emojis-not-appearing-as-icons-in-the-jumplist"></a>Perché i emoji non vengono visualizzati come icone in JumpList?

Solo le immagini collegate da un percorso di file possono essere sottoposte a rendering come icone del profilo nell'oggetto JumpList. Emoji non sono supportati per le icone JumpList.

## <a name="technical-notes"></a>Note tecniche

Le applicazioni che usano la [ `GetConsoleScreenBufferInfo` famiglia di API](https://docs.microsoft.com/windows/console/getconsolescreenbufferinfoex) per recuperare i colori della console attiva in formato Win32 e quindi provare a trasformarle in sequenze VT multipiattaforma (ad esempio, trasformando `BACKGROUND_RED` in `\x1b[41m` ) potrebbero interferire con la capacità del terminale di rilevare il colore di sfondo che l'applicazione sta tentando di usare.

Gli sviluppatori di applicazioni sono invitati a scegliere le funzioni dell'API Windows _o_ le sequenze VT per la regolazione dei colori senza provare a combinarli.

### <a name="keyboard-service-warning"></a>Avviso servizio tastiera

A partire da Windows Terminal 1,5, il terminale visualizzerà un avviso se la tastiera touch e il servizio pannello grafia sono disabilitati. Questo servizio è necessario per il sistema operativo per indirizzare correttamente gli eventi di input all'applicazione Terminal (così come molte altre applicazioni in Windows). Se viene visualizzato questo avviso, è possibile eseguire la procedura seguente per abilitare nuovamente il servizio:
1. Nella finestra di dialogo Esegui eseguire `services.msc`

  ![Services. msc nella finestra di dialogo Esegui](https://user-images.githubusercontent.com/18356694/97891741-c81eed00-1cf4-11eb-9d48-7b94fede5294.png)

2. Trovare il servizio "Touch Keyboard and grafia Panel Service"

  ![Toccare tastiera e servizio pannello grafia in Services. msc](https://user-images.githubusercontent.com/18356694/97891813-e1279e00-1cf4-11eb-91c8-69a5c6da6c3d.png)

3. Apre "Properties" per questo servizio

  ![Proprietà del servizio](https://user-images.githubusercontent.com/18356694/97891923-03212080-1cf5-11eb-90cc-821a4fbf16ba.png)

4. Modificare il "tipo di avvio" in "automatico"

  ![tipo di avvio del servizio](https://user-images.githubusercontent.com/18356694/97892043-25b33980-1cf5-11eb-8833-a2e65a306a79.png)

5. Fare clic su "OK" e riavviare il computer.

Dopo il riavvio del computer, il servizio dovrebbe avviarsi automaticamente e la finestra di dialogo non dovrebbe più essere visualizzata.
