---
title: Riquadri di Terminale Windows
description: Informazioni su come dividere i riquadri in Terminale Windows.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 09/22/2020
ms.topic: how-to
ms.openlocfilehash: 07badec2c42ace043544ae539c4b586a3c5f08d9
ms.sourcegitcommit: 8e0901b83a8cc437f090fe58688b86acb73f3cb3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2020
ms.locfileid: "90988541"
---
# <a name="panes-in-windows-terminal"></a>Riquadri in Terminale Windows

I riquadri offrono la possibilità di eseguire più applicazioni da riga di comando una accanto all'altra all'interno della stessa scheda. Questa opzione riduce la necessità di spostarsi tra schede e ti consente di vedere più prompt contemporaneamente.

## <a name="creating-a-new-pane"></a>Creazione di un nuovo riquadro

### <a name="using-the-keyboard"></a>Uso della tastiera

In Terminale Windows è possibile creare un nuovo riquadro verticale o orizzontale. La divisione in verticale apre un nuovo riquadro a destra di quello con lo stato attivo, mentre la divisione in orizzontale ne apre uno nuovo sotto quello con lo stato attivo. Per creare un nuovo riquadro verticale del profilo predefinito, è possibile premere la combinazione di tasti <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>=</kbd> . Per un riquadro orizzontale del profilo predefinito, è possibile utilizzare <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> + <kbd>-</kbd> .

![Creazione di riquadri di Terminale Windows](./images/open-panes.gif)
_Configurazione: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_

Se si desidera modificare questi tasti di scelta, è possibile crearne di nuovi utilizzando l' `splitPane` azione e `vertical` `horizontal` i valori, o `auto` per la `split` proprietà nel profiles.jssu file. Il `auto` Metodo sceglierà la direzione che fornisce i riquadri al quadrato. Per ulteriori informazioni sui tasti di scelta, visitare la [pagina azioni](./customize-settings/actions.md).

```json
{ "command": { "action": "splitPane", "split": "vertical" }, "keys": "alt+shift+=" },
{ "command": { "action": "splitPane", "split": "horizontal" }, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "auto" }, "keys": "alt+shift+d" }
```

### <a name="using-the-new-tab-button-and-dropdown-menu"></a>Utilizzando il pulsante nuova scheda e il menu a discesa

Se si vuole aprire un nuovo riquadro del profilo predefinito, è possibile mantenere il tasto <kbd>ALT</kbd> e fare clic sul pulsante nuova scheda. Per aprire un nuovo riquadro tramite il menu a discesa, tenere premuto <kbd>ALT</kbd> e fare clic sul profilo desiderato. Entrambe queste opzioni `auto` suddivideranno la finestra o il riquadro attivo in un nuovo riquadro del profilo selezionato. La divisione in modalità `auto` viene applicata nella direzione con il bordo più lungo per creare un riquadro.

![Riquadro a discesa di Terminale Windows](./images/alt-click-pane.gif)

## <a name="switching-between-panes"></a>Passaggio tra riquadri

Il terminale ti consente di spostarti tra i riquadri usando la tastiera. Se si tiene premuto il tasto <kbd>ALT</kbd> , è possibile usare i tasti di direzione per spostare lo stato attivo tra i riquadri. Il riquadro con lo stato attivo è identificabile dal colore in risalto del bordo che lo circonda. Questo colore è configurato nelle impostazioni dei colori di Windows.

![Passaggio tra i riquadri di Terminale Windows](./images/navigate-panes.gif)

Puoi personalizzare questa impostazione aggiungendo combinazioni di tasti per il comando `moveFocus` e impostando `direction` su `down`, `left`, `right` o `up`.

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

## <a name="resizing-a-pane"></a>Ridimensionamento di un riquadro

È possibile modificare le dimensioni dei riquadri tenendo premuto <kbd>ALT</kbd> + <kbd>MAIUSC</kbd> e utilizzando i tasti di direzione per ridimensionare il riquadro con lo stato attivo.

![Riquadro di ridimensionamento del terminale di Windows](./images/resize-panes.gif)

Per personalizzare questa combinazione di tasti, puoi aggiungerne altre usando l'azione `resizePane` e impostando `direction` su `down`, `left`, `right` o `up`.

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

## <a name="closing-a-pane"></a>Chiusura di un riquadro

È possibile chiudere il riquadro con lo stato attivo digitando <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>W</kbd>. Se è presente un solo riquadro, <kbd>CTRL</kbd> + <kbd>MAIUSC</kbd> + <kbd>W</kbd> chiuderà la scheda. Come sempre, chiudendo l'ultima scheda si chiude la finestra.

![Chiusura dei riquadri di Terminale Windows](./images/close-panes.gif)

Puoi cambiare i tasti di chiusura del riquadro aggiungendo una combinazione che usa il comando `closePane`.

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

## <a name="customizing-panes-using-key-bindings"></a>Personalizzazione dei riquadri con le combinazioni di tasti

Puoi personalizzare cosa aprire all'interno di un nuovo riquadro a seconda delle combinazioni di tasti personalizzate.

### <a name="duplicating-a-pane"></a>Duplicazione di un riquadro

Il terminale ti consente di duplicare il profilo del riquadro con lo stato attivo in un altro riquadro.

![Riquadri duplicati in Terminale di Windows](./images/duplicate-panes.gif)

A questo scopo, aggiungi la proprietà `splitMode` con `duplicate` come valore a una combinazione di tasti `splitPane`.

```json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
```

[!INCLUDE [new-terminal-arguments](./new-terminal-arguments.md)]
