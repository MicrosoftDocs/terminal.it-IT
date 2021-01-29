---
title: Impostazioni di avvio del terminale di Windows
description: Informazioni su come personalizzare le impostazioni di avvio nel terminale di Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 01/28/2021
ms.topic: how-to
ms.localizationpriority: high
ms.openlocfilehash: 1a16946a0b43a4fadd8e68014a13e6f13a79ae1e
ms.sourcegitcommit: 7855b73a8b3f84ee6bd42797e40281a3dadb152a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "99041968"
---
# <a name="startup-settings-in-windows-terminal"></a>Impostazioni di avvio nel terminale Windows

Le proprietà elencate di seguito interessano l'intera finestra del terminale, indipendentemente dalle impostazioni del profilo. Queste proprietà devono essere inserite nella radice del file settings.json.

> [!IMPORTANT]
> L'interfaccia utente delle impostazioni è disponibile solo in [Windows Terminal Preview](https://aka.ms/terminal-preview). Per istruzioni dettagliate su come abilitare l'interfaccia utente delle impostazioni, vedere la [pagina relativa alla risoluzione dei problemi](./../troubleshooting.md#open-the-settings-ui).

## <a name="default-profile"></a>Profilo predefinito

Imposta il profilo predefinito che viene aperto quando si digita <kbd>ctrl+shift+t</kbd>, si digita il tasto di scelta rapida assegnato a `newTab`, si esegue `wt new-tab` senza specificare un profilo o si fa clic sull'icona '+'.

**Nome della proprietà:** `defaultProfile`

**Obbligatoria:** Obbligatoria

**Accetta:** GUID o nome del profilo in formato stringa

**Valore predefinito:** GUID di PowerShell

<br />

___

## <a name="launch-on-machine-startup"></a>Avvia all'avvio del computer

Se questa proprietà è impostata su `true`, abilita l'avvio di Terminale Windows all'avvio del sistema. L'impostazione su `false` disabiliterà la voce dell'attività di avvio del sistema.

Nota: se la voce dell'attività di avvio del sistema di Terminale Windows viene disabilitata da criteri dell'organizzazione o da un'azione dell'utente, questa impostazione non avrà effetto.

**Nome della proprietà:** `startOnUserLogin`

**Obbligatoria:** Facoltativo

**Accetta:** `true`, `false`

**Valore predefinito:** `false`

<br />

___

## <a name="launch-mode"></a>Modalità di avvio

Definisce se il terminale verrà avviato come ingrandito, a schermo intero o in una finestra. L'impostazione di questa opzione su `focus` equivale all'avvio del terminale in `default` modalità, ma con la [modalità messa a fuoco](./actions.md#toggle-focus-mode) abilitata. Analogamente, l'impostazione di questa opzione su comporterà `maximizedFocus` l'avvio del terminale in una finestra ingrandita con la modalità messa a fuoco abilitata.

**Nome della proprietà:** `launchMode`

**Obbligatoria:** Facoltativo

**Accetta:** `"default"`, `"maximized"`, `"fullscreen"`, `"focus"`, `"maximizedFocus"`

**Valore predefinito:** `"default"`

<br />

___

## <a name="launch-size"></a>Dimensioni all'avvio

### <a name="columns-on-first-launch"></a>Colonne al primo avvio

Numero di colonne di tipo carattere visualizzate nella finestra al primo caricamento. Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.

**Nome della proprietà:** `initialCols`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `120`

### <a name="rows-on-first-launch"></a>Righe al primo avvio

Numero di righe visualizzate nella finestra al primo caricamento. Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , questa proprietà viene ignorata.

**Nome della proprietà:** `initialRows`

**Obbligatoria:** Facoltativo

**Accetta:** Intero

**Valore predefinito:** `30`

<br />

___

## <a name="launch-position"></a>Posizione di avvio

Consente di impostare la posizione in pixel dell'angolo superiore sinistro della finestra al primo caricamento. In un sistema con più schermi queste coordinate si riferiscono all'angolo superiore sinistro dello schermo principale. Se non viene specificata una coordinata X o Y, il terminale userà l'impostazione predefinita del sistema per tale valore. Se `launchMode` è impostato su `"maximized"` o `"maximizedFocus"` , la finestra verrà ingrandita sul monitoraggio specificato da tali coordinate.

**Nome della proprietà:** `initialPosition`

**Obbligatoria:** Facoltativo

**Accetta:** coordinate nei formati stringa seguenti: `","`, `"#,#"`, `"#,"`, `",#"`

**Valore predefinito:** `","`

<br />

___

## <a name="disable-dynamic-profiles"></a>Disabilita i profili dinamici

Consente di impostare i generatori di profili dinamici da disabilitare, per evitare che aggiungano profili all'elenco di profili all'avvio. Per informazioni sui profili dinamici, vedi la [pagina Profili dinamici](./../dynamic-profiles.md).

**Nome della proprietà:** `disabledProfileSources`

**Obbligatoria:** Facoltativo

**Accetta:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` e/o `"Windows.Terminal.PowershellCore"` all'interno di una matrice

**Valore predefinito:** `[]`

<br />

___

## <a name="startup-actions-preview"></a>Azioni di avvio ([Anteprima](https://aka.ms/terminal-preview))

In questo modo viene impostato l'elenco di azioni da eseguire all'avvio, consentendo al terminale di avviarsi con un set personalizzato di schede e riquadri per impostazione predefinita. Queste azioni verranno applicate solo se non è stato fornito alcun argomento della riga di comando. L'elenco di azioni è rappresentato da una stringa con lo stesso formato dei comandi negli argomenti della riga di comando. Per ulteriori informazioni sul formato dei comandi, visitare la [pagina argomenti della riga di comando](./../command-line-arguments.md).

**Nome della proprietà:** `startupActions`

**Obbligatoria:** Facoltativo

**Accetta:** Stringa che rappresenta un elenco di comandi da eseguire

**Valore predefinito:** `""`

> [!IMPORTANT]
> Questa funzionalità è disponibile solo in [Terminale Windows (anteprima)](https://aka.ms/terminal-preview).
